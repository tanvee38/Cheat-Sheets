
## Creating SSH keys for remotely login to remote server

First, open mac terminal

1. To see all the existing keys:
ls ~/.ssh/*.pub

2. Generate ssh keys
ssh-keygen -t rsa -C "moin@stetsolutions.com"

3. See keys
cat ~/.ssh/id_rsa.pub

### Basic SH commands: basic SH commands: https://www.hostinger.com/tutorials/ssh/basic-ssh-commands

### Some useful links about deploying node js app in digitalocean server.

1. deploy node js app digital ocean: https://code.lengstorf.com/deploy-nodejs-ssl-digitalocean/

To know about command: git config --global credential.helper "cache --timeout=3600"

https://help.github.com/articles/caching-your-github-password-in-git/

git config --global credential.helper cache
... which tells Git to keep your password cached in memory for (by default) 15 minutes. You can set a longer timeout with:
git config --global credential.helper "cache --timeout=3600"
(That example was suggested in the GitHub help page for Linux.) You can also store your credentials permanently if so desired, see the other answers below.

https://git-scm.com/book/en/v2/Git-Tools-Credential-Storage

Crontab

http://www.adminschoice.com/crontab-quick-reference

cron is a Unix, solaris, Linux utility that allows tasks to be automatically run in the background at regular intervals by the cron daemon. 

Crontab (CRON TABle) is a file which contains the schedule of cron entries to be run and at specified times. File location varies by operating systems, See Crontab file location at the end of this document.

sudo crontab -e the commands are schedule with root user's credentials. So that the commands in the sudo's cron table are executed as root user.
But with crontab -e, the commands are scheduled with the regular user who is logged in.

crontab -e    Edit crontab file, or create one if it doesn’t already exist.

what is ache- challenge:

We try to automatically add SSL certificates to your domains so you rank better on search engines and have a more secure site.  The process of generating these certificates creates the .well-known/acme-challenge/ folder on the domain.  It is safe to remove the folder if you want, however when the certificate is renewed every 90 days the folder will be re-created.

curl: curl is like postman to test the restful apis. but it is a command line approach using which we can test a restful api

UFW: ubuntu fire wall tool 

https://www.digitalocean.com/community/tutorials/ufw-essentials-common-firewall-rules-and-commands

UFW is a firewall configuration tool for iptables that is included with Ubuntu by default. UFW  allowing and blocking various services by port, network interface, and source IP address 

ufw allow 80   => Allow All Incoming HTTP

ufw allow 443 => Allow All Incoming HTTPS

web server listen for requests on port 80 and 443 for HTTP and HTTPS connections, respectively. 

Generate SSL certificate:

https://gist.github.com/harryfinn/e36e41cdbfba5a6e1d69d6498a4fc5ee

letsencrypt certonly --webroot -w ./static -d oms-staging.gldn.com (here you have put the ip address of your site)

* --webroot is the type of authentication we want to use in order to check our domain against with the SSL. This option comes back to the CloudFlare issue, whereby a CloudFlare protected server won't respond with the origin server's IP address, but instead with a dynamic CloudFlare IP, causing the SSL to fail verification.


* certonly =>  is the command we are running, telling certbot to generate a letsencrypt SSL manually, i.e. without the apache configuration (we'll do this ourselves!)


-d => sets the domain you which to assign this SSL to, multiple domains can be registered at the same time by passing additional -d flags after each domain.

-w = > write

To see all the hosts command: nano /etc/hosts

APT = ADVANCED PACKAGING TOOL. There are lots of apt commands.
apt get :

sudo : stands for superuser do, - means asking for root permission. apt : apt stands for advanced packaging tool , and is a package manager for debian/debian based flavours. apt-get : apt-get allows to download the package. install: install package .

Information about add-apt-repository:

helps developers to get the latest version of any software package quickly.

What does add-apt-repository mean?

Add software repositories
Software is available from third-party sources, as well as from the default Ubuntu software repositories. If you want to install software from a third-party software repository, you must add it to Ubuntu's list of available repositories.

probably linux repository resides : sources.list is in /etc/apt/

what is >> symbol and >& in unix/Linux?

> redirects output to a file, overwriting the file.
>> redirects output to a file appending the redirected output at the end.

postgres install in ubuntu:

PostgreSQL is available in all Ubuntu versions by default. However, Ubuntu "snapshots" a specific version of PostgreSQL that is then supported throughout the lifetime of that Ubuntu version. Other versions of PostgreSQL are available through the PostgreSQL apt repository.

https://www.postgresql.org/download/linux/ubuntu/

its like first add the repository of any particular software application to the default repository of your 
ubuntu. Then install the software. all application softwares are like package.


To check if postgres is running on remote server:

sudo service postgresql status

some queuing commands after psql command :

Now in Psql you could run commands such as:
1. \? list all the commands
2. \l list databases
3. \conninfo display information about current connection
4. \c [DBNAME] connect to new database, e.g., \c template1
5. \dt list tables
6. \q quit psql
https://stackoverflow.com/questions/769683/show-tables-in-postgresql

What is process.env.PORT in Node.js?

In many environments (e.g. Heroku), and as a convention, you can set the environment variable PORT to tell your web server what port to listen on.
So process.env.PORT || 3000 means: whatever is in the environment variable PORT, or 3000 if there's nothing there.
So you pass that app.listen, or to app.set('port', ...), and that makes your server be able to accept a parameter from the environment what port to listen on.
If you pass 3000 hard-coded to app.listen(), you're always listening on port 3000, which might be just for you, or not, depending on your requirements and the requirements of the environment in which you're running your server.


adding api makes it a api gateaway

I am using oms_staging as database

domain subdomain basics: different parts of domain

http://slides.com/jameyhoff/different-parts-of-a-domain-name#/13

There are several environment variables:

https://dzone.com/articles/what-you-should-know-about-node-env

Setting environment variable through mac termianl: use export command

export NODE_ENV=development && export SERVER_PORT=80

some of the  node enviroment variables are below.
NODE_ENV
SERVER_PORT
DB_DATABASE
URL_ORIGIN

to display any environment variable on mac terminal, for example: echo $NODE_ENV

how to know domain owner:

https://www.hostgator.com/blog/find-out-who-domain-owner/

https://whois.icann.org/en/lookup?name=

What is PPA (https://www.youtube.com/watch?v=LBXIz6ybt9U)

# nano basics in ubuntu:

1. open a file with nano = > example: nano /etc/hosts

2. after updating the the file, save it. => control + o

3. To exit after saving = > control + x

pm2 quick start: http://pm2.keymetrics.io/docs/usage/quick-start/

how to delete digital ocean droplets: https://www.youtube.com/watch?v=SaZXtP9Fsq4
















