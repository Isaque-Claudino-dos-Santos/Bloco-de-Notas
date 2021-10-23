<body style="background: #220000dd;">

<div style="display: flex; justify-content: center; align-iteams: center;>

# <img src="https://laravel.com/img/logomark.min.svg" style="margin-right: 20px; width: 79px;"> 
<a href="https://laravel.com/docs/8.x" style="color: red; text-decoration: none; font-size: 3rem;">Laravel</a>

</div>



> ### Primeira Instalações!
>- compose
>- php,php-apache,php-mysql e etc
>
>### Instalar laravel 
>- composer create-project laravel/laravel exemplo-app 
>
>### Rodar server 
>- php artisan serve

>## Arquitetura de Arquivos
>##### base de exemplo aquivo cadastro.php
>- Resources
>   - Folder view cadastro.blade.php
>- Controller
>   - cadastroControler.php
>   - Create File > php artisan make:controller cadastroComtroler
>- Routes
>   - Default file web.php
> - Migration
>   - Create File > php artisan make:migration created_cadastro
>   - Exec file > php artisan migrate
>- Models
>   - Cadastro.php
>   - Create File > php artisan make:model Cadastro

>## Codigos dos arquivos 
>### Controller
> ```php
>   
>   namespace App\Http\Controllers;
>
>   class cadastroController extends Controller 
> {
>   public function index() {
>          return view("cadastro"); //arquivo dentro de Resources
>   }
> }
>```


</body>








