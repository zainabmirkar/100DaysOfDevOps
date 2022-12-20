- If you make any changes to the code, and start the container again it will still be running the same old image and no new changes will be made to the container.
- You have to recreate the image in order to see the changes.
- This won't be beneficial when working in production.
- To see the update without having to rebuild the image we have docker volumes.

    ![image](https://user-images.githubusercontent.com/85761276/208603830-6f6ef2c4-2684-45ae-b89f-fbf68f677b60.png)
- --rm flag deletes the container automatically if it is stopped.

## Docker Volumes
- map the api folder in your local computer to the /app folder in your container.

    ![image](https://user-images.githubusercontent.com/85761276/208604940-1322e439-9d7d-4a11-b123-12d268eaebf2.png)

- Here we can see that nodemon restarting again due to changes and the changes will be reflected in our app without having to rebuild the image.
