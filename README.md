# Laravel-5-Simple-Roles-Management-ACL-
Laravel 5 Simple Roles Management(ACL) Protect your routes with user roles. Simply add a 'role_id' to the User model, install the roles table and seed if you need some example roles to get going.  If the user has a 'Root' role, then they can perform any actions.


Installation

Simply copy the files across into the appropriate directories, and register the middleware in App\Http\Kernel.php

Then specify a 'roles' middleware on the route you'd like to protect, and specify the individual roles as an array:

Route::get('user/{user}', [
     'middleware' => ['auth', 'roles'],
     'uses' => 'UserController@index',
     'roles' => ['administrator', 'manager']
]);
If you found this ACL manager helpful please give this repo a star, and give me a follow. Any questions, please leave a comment.
