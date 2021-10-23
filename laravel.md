<body style="background: #220000dd;">

<div style="display: flex; align-items: center; justify-content: center">

<img src="https://laravel.com/img/logomark.min.svg" width="70" style="margin-right: 25px;"> 

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
>   - CadastroControler.php
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
>### Resources
>```html
>   <h1>O html no arquivo cadastro.blade.php</h1>
>```

>### Controller
> ```php
>   
>   namespace App\Http\Controllers;
>   use Illuminate\Http\Request;
>   use App\Models\Pessoa;
>
>   class CadastroController extends Controller 
> {
>   public function index() {
>          return view("cadastro"); //arquivo dentro de Resources
>   }
>   
>   public function cadastrar(Request $request) {
>       dd(Pessoa::create($request->all()));
>   }
> }
>```

>### Routes
> ```php
>   use App\Http\Controllers\HomeController;
>   use App\Http\Controllers\StudentController;
>   use Illuminate\Support\Facades\Route;
>
>   Route::get("/cadastro",["CadastroController"::class,"index"]);
>   Route::post("/cadastro",["CadastroController"::class,"cadastrar"]);
> 
> ```

>### Migration
>```php
>    use Illuminate\Database\Migrations\Migration;
>    use Illuminate\Database\Schema\Blueprint;
>    use Illuminate\Support\Facades\Schema;
>
>   class CreatedStudentLastAcess extends Migration
>   {
>       public function up()
>       {
>           Schema::create("pessoas", function ($table) {
>                $table->id();
>                $table->string("nome");
>                $table->timestamps();
>            });
>        }
> 
>        public function down()
>        {
>        
>        }
>   }
>```

>## Models
>```php
>    namespace App\Models;
>
>    use Illuminate\Database\Eloquent\Factories\HasFactory;
>    use Illuminate\Database\Eloquent\Model;
>
>    class Pessoa extends Model
>    {
>            use HasFactory;
>            protected $fillable = ["nome"];
>    }
>```

</body>








