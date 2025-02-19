<p  align="center"><img  src="https://user-images.githubusercontent.com/1039236/36820389-964422c0-1d13-11e8-8dac-d58014f59c24.png"></p>

<p align="center">
<a href="https://github.com/lubusIN/laravel-gymie/releases"><img src="https://img.shields.io/github/release/lubusIN/laravel-gymie.svg?style=flat-square" alt="Latest Stable Version"></a>
<a href="https://scrutinizer-ci.com/g/lubusIN/laravel-gymie/build-status/master"><img src="https://img.shields.io/scrutinizer/build/g/lubusIN/laravel-gymie.svg?style=flat-square" alt="Build Status"></a>
<a href="https://styleci.io/repos/123349662"><img src="https://styleci.io/repos/123349662/shield" alt="StyleCI Status"></a>
<a href="https://scrutinizer-ci.com/g/lubusIN/laravel-gymie"><img src="https://img.shields.io/scrutinizer/g/lubusin/laravel-gymie.svg?style=flat-square" alt="Scrutinizer Code Quality"></a>
<a href="https://github.com/lubusIN/laravel-gymie/blob/master/LICENSE.md"><img src="https://img.shields.io/badge/License-MIT-brightgreen.svg?style=flat-square" alt="License"></a>
<a href="https://github.com/lubusin/laravel-gymie/blob/master/contributing.md"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square" alt="PRs"></a>
</p>

<center>
<a href="https://lubus.in/">
<img src="https://user-images.githubusercontent.com/1039236/40877801-3fa8ccf6-66a4-11e8-8f42-19ed4e883ce9.png" />
</a>
</center>

# Gymie

Laravel based web application for gym & club management. Currently being used by many fitness centers. For more information, visit - https://www.gymie.in
 
![gymie-device-mockup](https://user-images.githubusercontent.com/1039236/36820312-3f709262-1d13-11e8-8ee6-0529120b8ac1.png)

  

> ***Note:***
>
> Currently, we are in the process of polishing the code to be ready for general use. Check [issues](https://github.com/lubusIN/laravel-gymie/issues) & [milestone](https://github.com/lubusIN/laravel-gymie/milestones) to know more about upcoming changes, features and improvements.

## Requirements
- PHP >= 7.1.3
- OpenSSL PHP Extension
- PDO PHP Extension
- Mbstring PHP Extension
- Tokenizer PHP Extension
- XML PHP Extension
- Ctype PHP Extension
- JSON PHP Extension
- GD PHP Extension
- Imagick PHP Extension 

***Note:***
Improper permission on `storage` & `public` folder will lead to server & application errors

##  Installation
1. Clone to your server root `git clone -b master git@github.com:lubusIN/laravel-gymie.git`
> For faster updates and bleeding edge features, or if you want to help test the next version, use the `develop` branch instead of the `master` branch.
2. Run `composer install` to install all dependencies
3. Create `.env` in application root 
```cp .env.example .env```
4. Update database details and optional sentry DNS in `.env`
5. Run `php artisan key:generate` to generate key
6. Run `php artisan migrate --seed` to install the database & required data
7. Add cron entry for scheduled task to update status for various modules (subscription expiration etc)
```
* * * * * cd /path-to-gymie && php artisan schedule:run >> /dev/null 2>&1
```
