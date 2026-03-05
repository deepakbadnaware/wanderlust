Starting using docker in ubuntu ->
$
# Download and install nvm:
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash

# in lieu of restarting the shell
$ \. "$HOME/.nvm/nvm.sh"

# Download and install Node.js:
$ nvm install 24

# Verify the Node.js version:
$ node -v # Should print "v24.13.1".

# Verify npm version:
$ npm -v # Should print "11.8.0".

# Mongodb
$ sudo apt-get install gnupg curl

$ curl -fsSL https://www.mongodb.org/static/pgp/server-8.0.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-8.0.gpg \
   --dearmor

$ echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-8.0.gpg ] https://repo.mongodb.org/apt/ubuntu noble/mongodb-org/8.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-8.2.list

$ sudo apt-get update

$ sudo apt-get install -y mongodb-org


$ systemctl start mongod
$ systemctl status mongod

$ cd /backend

$ mongoimport --db wanderlust --collection posts --file ./data/sample_posts.json --jsonArray

$ npm install 

$ cp .env.sample .env

$ npm run dev

$ cd /frontend

$ npm install 

$ cp .env.sample .env.local

$ nohup npm run dev -- --host &
 
Starting using docker-compose ->

$ docker-compose up

$ docker exec -it <Mongo container id> mongoimport --db wanderlust --collection posts --file ./data/sample_posts.json --jsonArray

