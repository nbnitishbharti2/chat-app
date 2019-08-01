Realtime Private Chat
Here I have showing you that how to create realtime private chat application using socket io, Node JS, VueJS, Laravel.

System Requirements
The following are required to function properly.

Node v8.4.0+
Socket io v2.0
Vue.js v2.4.0
Laravel 5.4+
Chat application features
Private chatting
File send and receive
Online Offline status
Typing indicator
Messages stored in database(MYSQL)
Getting Started
Step : 1

git clone https://github.com/sagarankoliya/realtime-private-chat-nodejs-socketio-vuejs-laravel.git
Step : 2

Go to project directory using Terminal / CMD

composer install
Step : 3

In project directory find .env.example and rename to .env

Generate laravel application key

php artisan key:generate
Also change DB_DATABASE, DB_USERNAME, DB_PASSWORD in .env

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your db name
DB_USERNAME=your db username
DB_PASSWORD=your db password
Also add below line in your .env

WS_URL=http://localhost:3000/
Step : 4

Run Migration & Seeder

php artisan migrate
php artisan db:seed --class=UserTableSeeder

Step : 5

Go to project directory using Terminal / CMD

Open nodejs folder

install node dependencies

npm install
Step : 6

In nodejs directory open config/dev.json file

change database, user, password

below database configuration is same as above.

"host": "localhost",
"port": 3306,
"user": "your db username",
"password": "your db password",
"database": "your db name"
Step : 7

Start Node JS Chat Server

Go to project directory using Terminal / CMD Open nodejs folder

export NODE_ENV=dev
npm start
Start Laravel Server

Open Second Terminal / CMD Go to project directory

php artisan serve
Open http://127.0.0.1:8000 url in multipal browser

Login with below Users

No	Username	Password
1	user1@gmail.com	123456
2	user2@gmail.com	123456
3	user3@gmail.com	123456
Login at least 2 user in different browser.

After login you can see all users in right sidebar click anyone user and start private chatting.
Thats it.