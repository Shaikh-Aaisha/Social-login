<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

##About

Laravel 9 Socialite with User Authentication

laravel/socialite 
"version": "v5.6.1"
"php": "^7.2|^8.0"

##Steps For Social Login

Login with Google
Create Laravel project => composer create-project laravel/laravel example-app
Install Jetstream => 
composer require laravel/jetstream
php artisan jetstream:install livewire
npm install
npm run dev
php artisan migrate
Install Socialite => composer require laravel/socialite
Create Google App on https://console.cloud.google.com
After creating an account on above website create new project 
In your brand new project click on APIs and Services

https://www.itsolutionstuff.com/upload/laravel-login-google-1.png?ezimgfmt=rs:836x390/rscb5/ng:webp/ngcb5

Select credentials and choose first option OAuth Client ID here

https://www.itsolutionstuff.com/upload/laravel-login-google-2.png?ezimgfmt=rs:836x360/rscb5/ng:webp/ngcb5

add your Application Type,Name and Authorized Redirect URIs

https://www.itsolutionstuff.com/upload/laravel-login-google-3.png?ezimgfmt=rs:836x390/rscb5/ng:webp/ngcb5

After creating this account you can find client id and secret


Login with Facebook
Create Facebook App on https://developers.facebook.com/
After registering to this website click on My app and Create app

https://www.itsolutionstuff.com/upload/laravel-login-with-facebook-1.png?ezimgfmt=rs:836x394/rscb5/ng:webp/ngcb5

https://www.itsolutionstuff.com/upload/laravel-login-with-facebook-2.png?ezimgfmt=rs:836x394/rscb5/ngcb5/notWebP

Select consumer and add App Display Name,App Contact Email now 

https://www.itsolutionstuff.com/upload/laravel-login-with-facebook-3.png?ezimgfmt=rs:836x394/rscb5/ngcb5/notWebP

click on create App ID
After creating app select facebook login click on web option
Enter your site URL and save
Now go to facebook login inside this click on settings option
Enter Valid OAuth Redirect URIs and click on save changes button
Enter Redirect URI validator and click on Check URI button and then save
Click on Settings option and select Basic here you can find your
APP ID and APP SECRET

https://www.itsolutionstuff.com/upload/laravel-login-with-facebook-4.png?ezimgfmt=rs:836x394/rscb5/ngcb5/notWebP

You can copy it and congigure in .env file 
Now in your laravel project set your google and facebook Client_id,Client_secret,redirect URL in config/services.php file
You need to add GOOGLE_CLIENT_ID, GOOGLE_CLIENT_SECRET and FACEBOOK_CLIENT_ID, FACEBOOK_CLIENT_SECRET in .env file
Add column in table using this command 
php artisan make:migration add_google_id_column
php artisan make:migration add_facebook_id_column
Also add this google_idand facebook_id in your model
Creae routes and Define functions in Controller
Update blade login with google and facebook button and set the route
All the required step is done now you have to run the command php artisan serve


