# Como crear una web api con Asp.net Core 7 Y Entity Framework
En este tutorial vamos aprender a como crear una web api con Asp.net Core 7 y Entity Framework.

Paso 1: Abrimos el visual studio.

Paso 2: Creamos un proyecto nuevo y seleccionamos el proyecto de Asp.net (Modelo-Vista-Controlador).

![image](https://github.com/brian-duarte-01/Como-crear-una-web-api-con-Asp.net-Core-7-Y-Entity-Framework/assets/81836728/d0f4bf20-69e1-4d17-8798-250a7667f927)

Paso 3: Descargamos los paquetes Nuget.

![image](https://github.com/brian-duarte-01/Como-crear-una-web-api-con-Asp.net-Core-7-Y-Entity-Framework/assets/81836728/85e997f6-9e98-41eb-8772-48e815e4993d)

Paso 4: Abrimos la consola del administrador de paquetes nuget para ingresar el siguiente comando para crear el modelo de nuestro proyecto.

Comando con usuario de SQL:

Scaffold-DbContext "server=.; database=pruebaAPI; user id=sa; password=Admin1; integrated security=true; TrustServerCertificate=true;" Microsoft.EntityFrameworkCore.SqlServer -OutPutDir Models

Comando con autenticador de Windows:

Scaffold-DbContext "server=.; database=pruebaAPI; integrated security=true; TrustServerCertificate=true;" Microsoft.EntityFrameworkCore.SqlServer -OutPutDir Models

![image](https://github.com/brian-duarte-01/Como-crear-una-web-api-con-Asp.net-Core-7-Y-Entity-Framework/assets/81836728/687395c7-c283-46a1-8f95-ac1af19a02a9)

Paso 5: Nos vamos al siguiente enlace.

Enlace:

http://go.microsoft.com/fwlink/?LinkId=723263

Paso 6: Seleccionamos el siguiente código para realizar la cadena de conexión de nuestra base de datos al modelo.

![image](https://github.com/brian-duarte-01/Como-crear-una-web-api-con-Asp.net-Core-7-Y-Entity-Framework/assets/81836728/36e7a113-d2d9-4c87-ab6b-ff7077aef892)

Paso 7: Abrimos el archivo appsetings.json e ingresamos el código anterior de la pagina.

Codigo:

Con usuario de SQL SERVER:

"ConnectionStrings": {
    "CadenaConexion": "Server=.; Database=pruebaAPI; user id=sa; password=Admin1; integrated security=true; TrustServerCertificate=true;"
  }

Con usuario de Windows:

"ConnectionStrings": {
    "CadenaConexion": "Server=.; Database=pruebaAPI; integrated security=true; TrustServerCertificate=true;"
    }

![image](https://github.com/brian-duarte-01/Como-crear-una-web-api-con-Asp.net-Core-7-Y-Entity-Framework/assets/81836728/339df0b4-5b7b-49ee-b920-710b56b72e5f)

Paso 8: Abrimos el archivo de program.cs ingresamos el siguiente código.

Código:

builder.Services.AddDbContext<PruebaApiContext>(options =>
        options.UseSqlServer(builder.Configuration.GetConnectionString("CadenaConexion")));

![image](https://github.com/brian-duarte-01/Como-crear-una-web-api-con-Asp.net-Core-7-Y-Entity-Framework/assets/81836728/76d6db81-0b28-40c8-b7df-fc5e9803006c)

Paso 9: Creamos el controlador por medio de Entity Framework.

![image](https://github.com/brian-duarte-01/Como-crear-una-web-api-con-Asp.net-Core-7-Y-Entity-Framework/assets/81836728/832f39a1-17c0-4f93-9e08-9485771a47fb)

![image](https://github.com/brian-duarte-01/Como-crear-una-web-api-con-Asp.net-Core-7-Y-Entity-Framework/assets/81836728/51c4e370-cd75-448a-9f75-d0b915fc49a0)

![image](https://github.com/brian-duarte-01/Como-crear-una-web-api-con-Asp.net-Core-7-Y-Entity-Framework/assets/81836728/e521666f-b067-47bb-9237-eb67eda5cb4a)

Paso 10: automáticamente se creó el controlador de nuestra web api solo corremos el proyecto.

![image](https://github.com/brian-duarte-01/Como-crear-una-web-api-con-Asp.net-Core-7-Y-Entity-Framework/assets/81836728/b7cbdcca-e33a-44c6-9d9c-674f7d6e8e10)

![image](https://github.com/brian-duarte-01/Como-crear-una-web-api-con-Asp.net-Core-7-Y-Entity-Framework/assets/81836728/1eeaaf87-93d0-4c9f-99c7-db1e62dbfb2b)

Gracias por ver el tutorial. Les desea un feliz dia Brian Duarte!!
