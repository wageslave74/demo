# Demo of a flask/redis app in docker

First build the retwis image
cd retwis
docker build -t retwis:latest .

Then use docker-compose to install the app
cd ..
docker-compose up -d 

Then hit http://localhost:9001/ in your web browser
Create a user and pass
Then make some posts. All posts are stored in redis. 
