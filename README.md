<p align="center"><img src="public/images/logo/AJ3M%20Logo.png"></p>

## About The AJ3M Hotel System

AJ3M is a Laravel hotel system project for Information Technology Institute (ITI) Alexandria Branch.

## Introduction

Managing the hotel system. we can expand the featueres in the system to add any if needed.  
The hotel has basic roles `1.Admin`, `2.Manager`, `3.Receptionist`, `4.Client`.  
Each role with higher permissions can control the role below it ,by banning or deleting, or even to update the data.  
Roles are added easliy through the Admin Dashboard to control the full system.  
Clients can reserve rooms through the main website with easy payment.

## Installation

For installing AJ3M Hotel system.

1. You must first clone the current repository from the following command if you don't have git run the following command
   `sudo apt-get install git`
   `git clone https://github.com/MalikHesham/Laravel-Hotel-System-Project`
2. Run composer install to install third party libraries if you dont have composer you can download it from this link [Composer Installer](https://getcomposer.org/)
   `composer install`
3. Start migrating database files via this command:
   `php artisan migrate`
4. For starting the application, run the following command:
   `php artisan serve`
5. To create a system admin you can do one of the following commands:
   `php artisan db:seed`
   or
   `php artisan create:admin --email:admin@example.com --password=password`

## Project Depedencies

The project need the following dependences with by default get installed with running `composer install`

### Front-end libraries

-   Admin-LTE - you can get the package from this URL [Admin-LTE](https://adminlte.io/)
-   DataTables - you can obtain it from this URL [Get DataTables](https://datatables.net/)
-   Font Awesome 4 which already comes with Admin-LTE by default but you can obtain it from this URL [Font Awesome Library](https://fontawesome.com/)
-   Bootstrap 4 you can get it from this URL [Get Bootstrap](https://getbootstrap.com/docs/4.6/getting-started/introduction/)
-   JQuery you can get it from this URL [Get JQuery](https://jquery.com/)

### Laravel Packages

-   [Yajra DataTables](https://datatables.yajrabox.com/)
-   [Laravel Ban](https://github.com/cybercog/laravel-ban)
-   [Laravel Sanctum](https://laravel.com/docs/8.x/sanctum)
-   [Laravel Permission](https://github.com/spatie/laravel-permission)
-   [Stripe Payment](https://stripe.com/)
-   [Countries](https://github.com/rinvex/country)
-   [Excel](https://github.com/Maatwebsite/Laravel-Excel) exists by default in Yajra DataTables

## AJ3M Hotel System Roles

### Client

The client role can:

1. Register an account.
2. Wait their account to be accepted by any of the administrative roles.
3. Start browsing rooms after being accepted (An email is sent automatically after approval).
4. Get redirected to our-rooms checkout page finally get redirected to stripe to pay for the room.
5. Success message is shown if the payment operation is successfully done.

### Receptionist

1. Must be created by a manager or an admin.
2. Can approve pending clients' requests. The accpeted client is automatically assigned to the receptionist who accepted the request.
3. Rejecting a client will automatically delete it from database.
4. Can see their approved clients.
5. Can read their clients reservations.
6. Can update their own info.

### Manager

1. Can do receptionists' job.
2. Can do CRUD opreations on receptionist, rooms and floors.
3. Can't delete rooms that have reservations or floors having rooms (Referential Integrity).
4. Can ban a receptionist.
5. Can update their own info.
6. Accepting a client must be assigned to a receptionist.

### Admin

1. Can do both of receptionists' and managers' job.
2. Can do CRUD operations on managers and receptionists.
3. Can update their own info.
4. Can be created by seeding database or running `php arisan create:admin` command.

## Contributers

<a href="https://github.com/bin0mial"><img src="https://github.com/bin0mial.png" width="7%" style="border-radius:50%;margin-right:10px;" /></a> <a href="https://github.com/abdelrahmany0"><img src="https://github.com/abdelrahmany0.png" width="7%" style="border-radius:50%;margin-right:10px;" /></a> <a href="https://github.com/mahmoudm4"><img src="https://github.com/mahmoudm4.png" width="7%" style="border-radius:50%;margin-right:10px;" /></a> <a href="https://github.com/MalikHesham"><img src="https://github.com/MalikHesham.png" width="7%" style="border-radius:50%;margin-right:10px;" /></a> <a href="https://github.com/MohammedHieba"><img src="https://github.com/MohammedHieba.png" width="7%" style="border-radius:50%;margin-right:10px;" /></a>
