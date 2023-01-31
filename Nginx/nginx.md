#### Simple load balancing
- With this configuration, NGINX will distribute incoming client requests evenly among the backend servers in the upstream block


#### Weighted approach
``` 
upstream backend {
    server backend1.example.com weight=2;
    server backend2.example.com weight=1;
}
```
- With this configuration, NGINX will direct twice as many client requests to backend1.example.com as it does to backend2.example.com. 
- You can adjust the weights as needed to fine-tune the load balancing according to your specific requirements.



#### Least connections
- It will forward requests to the server which has least connections
