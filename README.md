To update the front end, we must extract a static template folder to the ```wass-static``` volume folder.    
```/var/lib/docker/volumes/home_waas-static/_data```    
the ```home_waas-static``` foldername will be different on your machine 'home' is just the foldername you ran ```docker-compose.yml``` from.    

We do not need to be inside the docker container for these changes.    

In your ```/home``` directory clone this git repo (install if not already with ```sudo apt-get install git```):
```
git clone https://github.com/plowsof/waas-templates
```
```
cd waas-templates/Rucknium-static
```
```
cp -r . /var/lib/docker/volumes/home_waas-static/_data
```
You will need to refresh your donate page with ```ctrl+f5```.     
If you are still not seeing changes, then check your DNS' cache settings (purge them).    

Note that some changes may take 5 minutes to appear ( this is how often the static page is refreshed ) but others should be instant.

example 1 liner after your cloned repo is set up (please change the directory names accordingly)
```
cd /home/waas-templates & \
git pull & \
cd Rucknium-static & \
cp -r . /var/lib/docker/volumes/home_waas-static/_data
```
