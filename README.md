## Diagram of the application
![multi_containers drawio](https://user-images.githubusercontent.com/114280300/221228425-9e0a7991-4cee-43fd-ae1f-ab955d1f8578.png)
1. We have a browser/client makes a request to the **nginx server**
2. **Nginx server** will forward requests that have `/` to **react application(hosted by nginx)** and `/api` to **express server**. 
**NOTE**: In development, **react app** will be started in **react server** itself and need to keep the connection active from **react server** to **browser/client** through **nginx server** to instantly refresh when codes changed 
3. **Express server** will connect to **redis server** and **postgres db**
4. **Worker** will listen to **redis server** for any changes by using subscription and do some logics there

## Deployment workflow
![deployment_workflow_for_multi_containers drawio](https://user-images.githubusercontent.com/114280300/221237940-f4aa17ea-99c3-46e3-95e6-f5e061a39fbc.png)
