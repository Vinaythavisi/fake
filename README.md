# deploy
This project uses the MEAN stack:

Mongoose.js (MongoDB): database
Express.js: backend framework
Angular 2+: frontend framework
Node.js: runtime environment
Other tools and technologies used:

Angular CLI: frontend scaffolding
Bootstrap: layout and styles
Font Awesome: icons
JSON Web Token: user authentication
Angular 2 JWT: JWT helper for Angular 2+
Bcrypt.js: password encryption
Prerequisites
Install Node.js and MongoDB
Install Angular CLI: npm i -g @angular/cli
From project root folder install all the dependencies: npm i
Run
Development mode with files watching
npm run dev: concurrently execute MongoDB, Angular build, TypeScript compiler and Express server.

A window will automatically open at localhost:4200. Angular and Express files are being watched. Any change automatically creates a new bundle, restart Express server and reload your browser.

Production mode
npm run prod: run the project with a production bundle listening at localhost:3000

Manual mode
1.Run MongoDB: mongod
2.Run the app: npm start
Docker
1.sudo docker-compose up
2.Go to localhost:3000
AWS EC2
1.Create a EC2 Linux machine on AWS
2.Edit the EC2 Security Group and add TCP port 3000 as an Inbound rule for Source 0.0.0.0/0
3.Clone this repo into the EC2 machine
4.If you use a remote MongoDB instance, edit .env file
5.Run npm ci
6.Run npm run build
7.Run npm start
8.The app is now running and listening on port 3000
9.You can now visit the public IP of your AWS EC2 followed by the port, eg: 12.34.56.78:3000
10.Tip: use pm2 to run the app instead of npm start, eg: pm2 start dist/server/app.js
