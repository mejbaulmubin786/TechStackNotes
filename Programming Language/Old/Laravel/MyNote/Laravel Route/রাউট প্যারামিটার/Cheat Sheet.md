# Basic Route
```php
//web.php
Route::get('/myname', function () {
    return 'Mejbaul Mubin';
});
// localhost/myname -> output: Mejbaul Mubin

Route::get('/myname', function () {
    return '<h1>Mejbaul Mubin</h1>';
});
```

```php
//web.php
Route::get('/about', function () {
    return view('information');
});

// \resources\views\information.blade.php
<h1>Mejbaul Mubin</h1>
```
```php
//web.php
Route::get('/about', function () {
    return view('about');
});

// \resources\views\about.blade.php
<h1>Mejbaul Mubin</h1>
```
# Alternative to call view file if there are not any controller
```php
//web.php
Route::view('/about', 'information');

// \resources\views\information.blade.php
<h1>Mejbaul Mubin</h1>
```
# Make Link
```php
//web.php
Route::get('/', function () {
    return view('welcome');
});

Route::get('/about', function () {
    return view('information');
});

// \resources\views\information.blade.php
<h1>Mejbaul Mubin</h1>
<a href="/">Home</a>

// \resources\views\welcome.blade.php
<h1>Welcom Page</h1>
<a href="/about">about</a>
```

# make subroute
```php
//web.php
Route::get('/about/contact', function () {
    return view('contact');
});

// \resources\views\contact.blade.php
<h1>This is my contact page</h1>


Route::get('/about/contact', function () {
    return view('about'); // if we want to show about page. 
});

//http://127.0.0.1:8000/about/contact
```

```
php artisan route:list
php artisan route:list --except-vendor
```
# Laravel Routing Parameters & Constraints Tutorial in Hindi

```php
//http://127.0.0.1:8000/post/10
//http://127.0.0.1:8000/post/mubin
//http://127.0.0.1:8000/post/news10
//http://127.0.0.1:8000/post/@news10

Route::get('/post/{id}', function(string $id){
	return 'User'.$id;
});
```


Laravel-এ আপনি রুট প্যারামিটারের নাম এবং ফাংশনের প্যারামিটারের নাম ভিন্ন রাখতে পারেন। 
```php
Route::get('/post/{stid}', function(string $id){
	return "<h1>Post ID: ".$id."</h1>";
});
```
তবে, নিচের ক্ষেত্রে আপনাকে রুট প্যারামিটারের মান ফাংশনের প্যারামিটারে পাওয়ার জন্য নির্দিষ্টভাবে রুট প্যারামিটার ম্যাপ করতে হবে।

আপনি `Route::get()` ফাংশনে `{id}` ব্যবহার করতে পারেন, আর ফাংশনের প্যারামিটার `$value` হতে পারে, কিন্তু আপনাকে `request()->route()` ফাংশন দিয়ে রুট প্যারামিটার অ্যাক্সেস করতে হবে।

```php
Route::get('/post/{id}', function(string $value){  //optional paramitter string
    $id = request()->route('id'); // {id} প্যারামিটার থেকে মান পাবেন
    return 'User' . $id;
});


Route::get('/post/{id}', function(string $id){
	return "<h1>Post ID: ".$id."</h1>";
});
```

//http://127.0.0.1:8000/post/10
//http://127.0.0.1:8000/post/mubin
//http://127.0.0.1:8000/post/news10
//http://127.0.0.1:8000/post/@news10

```php
Route::get('/post/{id?}', function(string $id=null){
if($id){
	return "<h1>Post ID: ".$id."</h1>";
}else{
	return "No data found";
	}
});
```

```php
Route::get('/post/{id?}/commet/{commetnid?}', function(string $id=null, string $comment = null){
if($id){
	return "<h1>Post ID: ".$id."</h1><h2>Post ID: ".$comment."</h2>";
}else{
	return "No data found";
	}
});
```

### Regular Expression Constraints
You may constrain the format of your route parameters using the `where` method on a route instance. The `where` method accepts the name of the parameter and a regular expression defining how the parameter should be constrained:
```php
Route::get('/user/{name}', function (string $name) {

// ...

})->where('name', '[A-Za-z]+');

Route::get('/user/{id}', function (string $id) {

// ...

})->where('id', '[0-9]+');

Route::get('/user/{id}/{name}', function (string $id, string $name) {

// ...

})->where(['id' => '[0-9]+', 'name' => '[a-z]+']);
```

For convenience, some commonly used regular expression patterns have helper methods that allow you to quickly add pattern constraints to your routes:
```php
Route::get('/user/{id}/{name}', function (string $id, string $name) {

// ...

})->whereNumber('id')->whereAlpha('name');

Route::get('/user/{name}', function (string $name) {

// ...

})->whereAlphaNumeric('name');

Route::get('/user/{id}', function (string $id) {

// ...

})->whereUuid('id');

Route::get('/user/{id}', function (string $id) {

//

})->whereUlid('id');

Route::get('/category/{category}', function (string $category) {

// ...

})->whereIn('category', ['movie', 'song', 'painting']);
```
If the incoming request does not match the route pattern constraints, a 404 HTTP response will be returned.
#### Global Constraints
If you would like a route parameter to always be constrained by a given regular expression, you may use the `pattern` method. You should define these patterns in the `boot` method of your `App\Providers\RouteServiceProvider` class:

```php
/**

* Define your route model bindings, pattern filters, etc.

*/

public function boot(): void

{

Route::pattern('id', '[0-9]+');

}
```

Once the pattern has been defined, it is automatically applied to all routes using that parameter name:
```php
Route::get('/user/{id}', function (string $id) {

// Only executed if {id} is numeric...

});
```

#### [Encoded Forward Slashes](https://laravel.com/docs/10.x/routing#parameters-encoded-forward-slashes)

The Laravel routing component allows all characters except `/` to be present within route parameter values. You must explicitly allow `/` to be part of your placeholder using a `where` condition regular expression:

```php
Route::get('/search/{search}', function (string $search) {

return $search;

})->where('search', '.*');
```

### Named Routes
Named routes allow the convenient generation of URLs or redirects for specific routes. You may specify a name for a route by chaining the `name` method onto the route definition
```php
Route::get('/user/profile', function () {

// ...

})->name('profile');
```
You may also specify route names for controller actions:
```php
Route::get(

'/user/profile',

[UserProfileController::class, 'show']

)->name('profile');
```
