## instrumentation
-----------------------------------------------------------------------------------------
* the applications in u r organization ommiting the metrics,logging is not done to application,traces are not provided to the application, it doesnt matter if u have prometheus nagios.
* exporters doesnt pull the specific information of application.
![preview](./images/obs1.png)
![preview](./images/obs2.png)
![preview](./images/obs3.png)
* why prometheus no writing the custom metrics we written.
* how does prometheus know which application service get the custom metrics? for that prometheus has `service discovery`.
* to make service discovery u need to deploy a custom resource or a yaml file.
![preview](./images/obs4.png)
![preview](./images/obs5.png)
![preview](./images/obs6.png)
![preview](./images/obs7.png)
* to get the alerts from alert manager we configure alert manager.
![preview](./images/obs8.png)
![preview](./images/obs9.png)
* to confiure the email from the google.for smtp server we need password.
* goto gmail and manage google account.
![preview](./images/obs10.png)
* enable 2 factor authentication in u r email.
![preview](./images/obs11.png)
![preview](./images/obs12.png)
* take the password and convert to base64 encoded formart.
![preview](./images/obs13.png)
* after that change email details in alertmanager and again run the kustomize.
![preview](./images/obs14.png)
![preview](./images/obs15.png)
* use the endpoint `crash` in the url. the app will be crashed.
![preview](./images/obs16.png)
