<https://www.fail2ban.org/wiki/index.php/Commands>

```
docker exec -it swag fail2ban-client <command>
```

I have created an alias to easily interact with fail2ban:

```
alias fail2ban="docker exec -it swag fail2ban-client"
```

There are 5 jails in total.

```
nginx-badbots, nginx-botsearch, nginx-deny, nginx-http-auth, nginx-unauthorized
```

nginx-unauthorized is the jail for invalid login information. I have increased max retries to 10 attempts. After which you get IP banned for 10 minutes. I checked the bantime with the following command:

```
fail2ban get nginx-unauthorized bantime
600
```

"600" was the output in seconds, which is 10 minutes.