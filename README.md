<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

# About Laravel-Discord Authentication
<strong>Laravel-Discord Authentication</strong> is a project that uses Laravel's built-in authentication system to authenticate users with Discord.

# Installation
## Discord
### Step #1
- Go to [Discord Developer Portal](https://discord.com/developers/applications) and create a new application. <br>
![](https://i.imgur.com/8nIRrEZ.png)
### Step #2
Go to OAuth2 and create a new redirect for your application.<br>
![](https://i.imgur.com/NiuDxmp.png) <br>
It should point to your application's authentication endpoint. (https://domain.com/api/login)

## Laravel
### Step #1

Get the project:
```batch
git clone https://github.com/JakyeRU/Laravel-Discord-Authentication.git

cd Laravel-Discord-Authentication
```

Setup the project; run the following commands within your project:
```batch
copy .\.env.example .\.env
```

Install the required dependencies:
```batch
composer install
```

Generate a new key for your application:

```batch
php artisan key:generate
```
<i>Update `.env` with your database credentials before running the migrations. </i>

```batch
php artisan migrate
```

### Step #2
Update `.env` with your Discord application details. (DISCORD_CLIENT_ID, DISCORD_CLIENT_SECRET DISCORD_REDIRECT_URI) <br>
![](https://i.imgur.com/VCEt9tX.png) <br>

```
DISCORD_CLIENT_ID=123456789012345678
DISCORD_CLIENT_SECRET=DPn_n4-3Aol8ZwjDoigrEQN2jtAj4f_
DISCORD_REDIRECT_URI=http://localhost:8000/api/login
```

### Step #3
Start the server and go to your application.
```batch
php artisan serve
```

---

# Preview

## Homepage
![](https://i.imgur.com/w0vNgR0.png)

## Discord OAuth2
![](https://i.imgur.com/EbxA88y.png)

## Authenticated Homepage
![](https://i.imgur.com/ctJmb4X.png)
