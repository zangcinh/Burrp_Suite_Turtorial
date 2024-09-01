![image](https://github.com/user-attachments/assets/32a607ed-57a0-4e05-b5a7-e780cc10f3fe)First, let's go to the JuiceShop and ;et's try to login. 

Now I have already pre created a user with the email `testme@gmail.com`

![image](https://github.com/user-attachments/assets/9a16869b-cc69-4cbf-9227-dce854b70d72)

I'm trying to guess the user pasword and I'm gonna try with `abcabc` and hit enter the login

![image](https://github.com/user-attachments/assets/1d20e5c4-a0eb-4f38-b8cf-8c1b2a242c20)

What we see it the email or password is invalid. So let's go to Burp and go to a proxy tab, find that login request and sedn it to the intruder

![image](https://github.com/user-attachments/assets/53bbc167-9cf8-4e88-95e2-9ff72bf665fb)

Now we see here is the intrudder is trying to spot interesting injection points for you

![image](https://github.com/user-attachments/assets/1049fa15-5e9f-487c-9cf2-ddf1edaa63e7)

At the top of the screen, you can select different attack types

![image](https://github.com/user-attachments/assets/cfce71a5-8f1b-40bc-8ae6-4331d52c2135)

I choose the `Sniper`. Now, I just select the password field to be the injection points

We gonna brute force the actual password of my test user. So in order to do that, we need a good list of payload 

In this tutorial, I gonna use this [password list](https://github.com/fuzzdb-project/fuzzdb/blob/master/wordlists-user-passwd/passwds/john.txt)
Copy all of that and simply click on `paste` in `Payload settings`

![image](https://github.com/user-attachments/assets/bd727900-a53f-4915-b131-c7f707b1eb09)

At the `settings` of intruder, go to the `Grep - Extract`, it will show you the response of the request yoou have sent to the intruder

![image](https://github.com/user-attachments/assets/818b59b0-9cbf-4167-804b-7e3e94fa74a1)

Now we can see almost all of is invalid but I notice that there is one different entry here. We see a different status and we see a different length and our Burp found sth different

![image](https://github.com/user-attachments/assets/dc111cd7-d24d-4dba-9dd0-12037173b22d)

I have tried this `password:123abc` and successfully access to the test account

![image](https://github.com/user-attachments/assets/cc93ad2e-8f6a-4747-8b81-8eedeb6098be)

