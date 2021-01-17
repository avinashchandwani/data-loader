"# data-loader" 
API Postman Collection : https://www.getpostman.com/collections/28943747770f43281974

# Start Database
1. docker pull mysql
2. docker run -p 33060:3306 --name dl-mysql mysql

Build and start the app image
1. mvn clean install
2. docker build -t dataloader-app .
3. docker run -p 8000:8000 --name dataloader-app --link dl-mysql:mysql -d dataloader-app

