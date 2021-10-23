<body style="background: #112233;" id="body">

<div style="background: #00000044; width: 40px; height: 40px; position: fixed; z-index: 4; font-size: 3rem; display: flex; justify-content: center; align-items: center; right: 10px; bottom: 10px;"><a href="#body" style="outline: none;">^</a></div>

<div style="display: flex; align-items: center; justify-content: center">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" width="100">

<h1> MySql-Server </h1>

</div>

<nav>
    <ul>
        <li><a href="#1">Conectar-se ao Banco de Dados</a></li>
        <li><a href="#2">Exibi Todos os Banco de Dados</a></li>
        <li><a href="#3">Usar o Banco de Dados</a></li>
        <li><a href="#4">Exibi Todas as Tabelas</a></li>
        <li><a href="#5">Criar Banco de Dados e Definir Tipo UTF-8</a></li>
        <li><a href="#6">Criar Tabela</a></li>
        <li><a href="#7">Inserir Dados na Tabela</a></li>
        <li><a href="#8">Selecionar Dados da Tabela</a></li>
        <li><a href="#9">Excluir Dados da Tabela</a></li>
        <li><a href="#10">Auterar Dados da Tabela</a></li>
        <li><a href="#11">Adicionar Colunas na Tabela</a></li>
        <li><a href="#12">Excluir Colunas da Tabela</a></li>
        <li><a href="#13">DATA TYPE</a></li>
        <li><a href="#14">Propriedade</a></li>
    </ul>
</nav>

----------

## Comandos

>## <div id="1">Conectar-se ao Banco de Dados</div>
>```sql
>    mysql -h localhost -u root -p;
>```
>

>## <div id="2">Exibi Todos os Banco de Dados</div>
>```sql
>    show databases;
>```

>## <div id="3">Usar o Banco de Dados</div> 
>##### sempre antes de criar,modificar e etc.
>```sql
>    use <dbname>
>```

>## <div id="4">Exibi Todas as Tabelas</div>
>```sql
>    show tables;
>```


>## <div id="5">Criar Banco de Dados e Definir Tipo UTF-8</div> 
>```sql
>    create database <dbname>
>    default character set utf8
>    default collate utf8_general_ci;
>```


>## <div id="6">Criar Tabela</div> 
>```sql
>    create table <dbtable> ( 
>       id int primary key auto_increment; 
>       nome varchar(50),        
>       idade int(3)
>    );
>```

>## <div id="7">Inserir Dados na Tabela</div> 
>```sql
>insert into <dbtable>(nome,email,idade) values( 
>    "Maria",
>    "maria324@gmail.com",
>    40
>);
>```

>## <div id="8">Selecionar Dados da Tabela </div> 
>#### Exibe todos os dados da tabela
> ```sql
>    select * from <dbtable>;
> ```
> #### Exibe todos os dados que o nome e igual a maria 
>```sql
>    select * from <dbtable> where nome = "maria";
>```
>#### ordernar DESC = decresente o id
>```sql
>    select * from <dbtable> order by id desc;
>```

>## <div id="9">Excluir Dados da Tabela</div> 
>#### cuido para não deletar a tabela toda !!!
> ```sql
>   delete from <dbtable> where;
> ```
> #### faça isso
> ```sql
>   delete from <dbtable> where nome = "Nome de teste"; 
> ```


>## <div id="10">Auterar Dados da Tabela</div> 
>```sql
>    update <dbtable> set nome = "o que eu quero altera" where nome = "o novo";
>```

>## <div id="11">Adicionar Colunas na Tabela</div> 
>    alter table <dbtable>
>    add column myColumn
>
>### Especificar onde colocar a coluna
>```sql
>   alter table <table> 
>   add column myColumn [first/after myNewColumn]
>``` 

>## <div id="12">Excluir Colunas da Tabela</div> 
>```sql
>    alter table <dbtable> 
>    drop column myColumn
>```

>## <div id="13">DATA TYPE</div> 
>```sql
> varchar() -- texto.
> int() -- números inteiros.
> float() -- números decimais.
> bool() -- true ou false.
> date() -- YYYY-MM-DD.
>```

>## <div id="14">Propriedade</div> 
>```sql
>   auto_increment --autom incremento ex:1,2,3.
>   primary key -- chave primaria.
>   not null -- campo nunca ficara nulo. 
>```
</body>