### For security reasons the xFusionCorp Industries security team has decided to use custom Apache users for each web application hosted, rather than its default user. This will be theApache user, so it shouldn't use the default home directory. Create the user as per requirements given below:


#### a. Create a user named anita on the App server 2 in Stratos Datacenter.

#### b. Set UID to 1306 and its home directory to /var/www/anita.

``` shell
# Create a user named anita with uid 1306

> $ useradd -u 1306 anita 

```

```shell
# Change the path inside /etc/passwd to /var/www/anita

> $ usermod -d /var/www/anita -m anita

```

``` shell
# Check the path inside /etc/passwd

> $ cat /etc/passwd | grep anita

```