# Configuring a static website on Amazon S3

- Step 1 - Create a Bucket

 ![image](https://user-images.githubusercontent.com/85761276/200045125-de0d468b-abe4-4845-9ea6-2b15e9c1959b.png)

- Step 2 - Enable static website hosting

 ![image](https://user-images.githubusercontent.com/85761276/200045389-476ef699-6a25-4816-ad47-4d29e6d09900.png)

- Step 3 - Edit Block Public Access settings : Clear Block all public access, and choose Save changes.

 ![image](https://user-images.githubusercontent.com/85761276/200045651-e618769e-d88d-4401-a394-63a82082658e.png)


- Step 4 - Add a bucket policy that makes your bucket content publicly available

 ![image](https://user-images.githubusercontent.com/85761276/200045791-f37e2ad3-1c00-459d-a998-f29a500f8b67.png)

- Step 5 and 6 - Configure an index document and error document
 
 ![image](https://user-images.githubusercontent.com/85761276/200045904-8132781e-097b-4089-bcbe-040f9f9e8c02.png)


- Step 7 - Test your website endpoint

 ![image](https://user-images.githubusercontent.com/85761276/200046107-b9acb8b7-9775-4126-b141-89eb25c3065d.png)

- Step 8: Clean up <br/>

References: https://docs.aws.amazon.com/AmazonS3/latest/userguide/HostingWebsiteOnS3Setup.html
