First, we need a website that we want to monitor first

I choose [OWASP JUICE SHOP](https://demo.owasp-juice.shop/#/)

At `Proxy`, go to the `option` tab

![image](https://github.com/user-attachments/assets/444e0db0-0cd6-4a28-9bf5-34ca190cd27e)

And you see that Burp has a proxy listener which is used to receive incoming HTTP requests from your browser

Click on `import/export CA certificate` 

![image](https://github.com/user-attachments/assets/82cfd557-1657-49ff-9666-c845d8faac98)

Click on `Certificate in DER format`

Choose `next` -> `select file` -> create a file and just make sure it has a `der` ending

I use Firefox. At `Settings`, find `cerificate` -> view certificate
At `Authorities`, immport your certificates that u have created 
Click this check box

![image](https://github.com/user-attachments/assets/12eac7d3-94b1-4062-b827-fe8db55934b5)

If u see PortSwigger here, u have now successfully imported ur cert into the web browser

![image](https://github.com/user-attachments/assets/331d0d85-1b9a-44b3-97be-ca6e202688f6)

Now let's go back to burp and make sure that we are checking the config for the listener. Here is the listener is running in our local host on our local machine on port 8080

![image](https://github.com/user-attachments/assets/d3c022f4-de6f-4029-8ade-7db107556948)

Next, we have to tell and allow the browser know that it has to communicate with our local machine on prt 8080. I use [FoxyProxy](https://addons.mozilla.org/en-US/firefox/addon/foxyproxy-basic/). 

![image](https://github.com/user-attachments/assets/112aca4e-c73d-470e-a8f1-1539c46491ae)

![image](https://github.com/user-attachments/assets/390c32ed-760d-4fe2-a30e-2f5f0d291bef)

Now we can see the the requests appear in burpsuite 

![image](https://github.com/user-attachments/assets/980ef53c-ddcb-4948-a747-3e7d6dc94057)

