
<b>##About</b>

Laravel 9 Socialite with User Authentication

laravel/socialite 
"version": "v5.6.1"
"php": "^7.2|^8.0"

<b>##Steps For Social Login</b>

<b>Login with Google</b><br>
Create Laravel project => composer create-project laravel/laravel example-app<br>
Install Jetstream => <br>
composer require laravel/jetstream<br>
php artisan jetstream:install livewire<br>
npm install<br>
npm run dev<br>
php artisan migrate<br>
Install Socialite => composer require laravel/socialite<br>
Create Google App on https://console.cloud.google.com<br>
After creating an account on above website create new project <br>
In your brand new project click on APIs and Services<br>

<img src="https://www.itsolutionstuff.com/upload/laravel-login-google-1.png?ezimgfmt=rs:836x390/rscb5/ng:webp/ngcb5"><br>

Select credentials and choose first option OAuth Client ID here<br>

<img src="https://www.itsolutionstuff.com/upload/laravel-login-google-2.png?ezimgfmt=rs:836x360/rscb5/ng:webp/ngcb5"><br>

add your Application Type,Name and Authorized Redirect URIs<br>

<img src="https://www.itsolutionstuff.com/upload/laravel-login-google-3.png?ezimgfmt=rs:836x390/rscb5/ng:webp/ngcb5"><br>

After creating this account you can find client id and secret<br>

<b>Login with Facebook</b><br>
Create Facebook App on https://developers.facebook.com/<br>
After registering to this website click on My app and Create app<br>

<img src="https://www.itsolutionstuff.com/upload/laravel-login-with-facebook-1.png?ezimgfmt=rs:836x394/rscb5/ng:webp/ngcb5"><br>

<img src="https://www.itsolutionstuff.com/upload/laravel-login-with-facebook-2.png?ezimgfmt=rs:836x394/rscb5/ngcb5/notWebP"><br>

Select consumer and add App Display Name,App Contact Email now <br>

<img src="https://www.itsolutionstuff.com/upload/laravel-login-with-facebook-3.png?ezimgfmt=rs:836x394/rscb5/ngcb5/notWebP"><br>

click on create App ID<br>
After creating app select facebook login click on web option<br>
Enter your site URL and save<br>
Now go to facebook login inside this click on settings option<br>
Enter Valid OAuth Redirect URIs and click on save changes button<br>
Enter Redirect URI validator and click on Check URI button and then save<br>
Click on Settings option and select Basic here you can find your<br>
APP ID and APP SECRET<br>

<img src="https://www.itsolutionstuff.com/upload/laravel-login-with-facebook-4.png?ezimgfmt=rs:836x394/rscb5/ngcb5/notWebP"><br>

You can copy it and configure in .env file <br>
Now in your laravel project set your google and facebook Client_id,Client_secret,redirect URL in config/services.php file<br>
You need to add GOOGLE_CLIENT_ID, GOOGLE_CLIENT_SECRET and FACEBOOK_CLIENT_ID, FACEBOOK_CLIENT_SECRET in .env file<br>
Add column in table using this command <br>
php artisan make:migration add_google_id_column<br>
php artisan make:migration add_facebook_id_column<br>
Also add this google_idand facebook_id in your model<br>
Create routes and Define functions in Controller<br>
Update blade login with google and facebook button and set the route<br>
All the required step is done now you have to run the command php artisan serve<br>


