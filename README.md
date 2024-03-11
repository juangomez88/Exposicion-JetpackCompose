# Exposicion-JetpackCompose

## Creación del proyecto en Android Studio
Inicialmente abrimos el Android Studio, y en el boton de ***New Project*** iniciamos el proyecto:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/41c37142-36ce-499a-a040-a12f018f3cfd)


Posterioremente seleccionamos ***Empty Activity*** y presionamos en el boton ***Next***:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/3ea8e86e-135a-4ce7-a4f3-9327f97b4acb)

La siguiente ventana en abrir, mostrará:
*nombre de la aplicación
*nombre de paquete de la aplicación
*Ubicación de guardado
*El SDK minimo
*Y la configuración lenguaje
Para este ejemplo podemos colocar los siguientes datos:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/ea63e4b9-4e27-4bdb-9c78-f38e0704bb25)

Siguiendo estas indicaciones se creara la aplicacion por defecto de Android Studio.

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/02189b65-de51-46b3-8f36-686a1b45a02d)

Vamos a crear inicialmente el ``Header`` de una aplicación que simulará el inicio de instagram:
Inicialemte crearemos la clase ``LoginScreen()`` con los Composable ``LoginScreen(){}`` que será el composable contenedor de cada uno de los componentes que en conjunto conformará ``Login``:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/764949c5-fd32-44bf-aca9-0c73cbfe7c56)


![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/f8651c1e-993a-48a1-982a-529dd0f73082)

El primer componente que vamos a crear será composable ``Header(){}`` este componente contendra un icono de cierre en la parte superior derecha de la pantalla, para ellos este será el codigo que usaremos:


![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/6e4d7d00-bb17-4cb7-947d-b1a1f6d05394)


El resultado que obtendremos será el siguiente: 

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/b0d5beee-5686-4fac-84ee-c09531682fef)


Ahora crearemos el componente más grande de esta pequeña aplicación el composabel ``Body(){}``, este componente contendrá a su vez de manera atomizada pequeños componentes que en su conjunto hacen nuestro `Body` asi iniciamos el componente:


![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/31c1952e-f289-4dfa-9637-ceba58b80a33)


Lo primero es crear el componete que contiene la imagen del logo, para ello con un llamamos un componente Image con un painterResource, así:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/02db9f0c-1b4c-4ec3-b732-5a8b7d4c7666)

La imagen de intagram es la siguiente:

![insta](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/d6953343-ebc6-48eb-b467-01dc72e490a8)

Esta imagen la podemos guardar en la siguiente ruta del proyecto:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/c1d3bb80-8e56-492e-9816-57388e01aa7e)

Ahora crearemos los composable de serán los inputs del ``Password()`` y el ``Email()``, estos componentes son practicamente iguales solo varian en los parametros que reciben, de la siguiente manera:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/e1705c6e-6ca4-41d7-b891-921e46942146)

Lo siguiente que crearemos será el texto de ``Forgot password?`` este componente no tiene ningun comportamiento especial de momento solo es una texto de color, para ello creamos el siguiente código:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/44080ffe-7197-433f-9519-4af7ef5b0b65)

Ahora el componente final de este ``Body(){}`` será el composable ``LoginButton(){}`` de la siguiente manera:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/2dbe3d5e-d986-453d-8db8-73ed49106a31)

Ya con estos elementos construidos llamamos todos estos elementos dentro del componente ``Body(){}``, es de anotar que en el siguiente código se crearon las variables `email`, `password` y `ìsLoginEnable`, estas variables se usan para que los componetes composable `Email(){}`, `Password(){}` y el `LoginButton(){}` funcionen de manera adecuada, tambien se usan los componentes Spacer para dar un espaciado entre componentes, así quedaría nuestro componente:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/bc8bc391-2d9b-43af-a3a0-5194983bf0e2)

Y este es el resultado de lo que llevamos al momento:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/5f520b11-bfaa-4ae4-a715-397be50c89b0)

Antes de terminar el `Body(){}` debemos crear un par de componentes, el componente `LoginDivider(){}` que es un separador entre login y el login por medio de redes, el otro componente a crear el el `SocialLogin(){}` que para este ejercicio solo tendra elementos quemados. Estos son los códigos de los composable creados:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/904d98b1-f60e-4360-a266-570845467771)


![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/462b151e-fbfb-4576-adf3-f3e44085b73a)

Para el elemento `SocialLogin(){}` se puede guardar la imagen en la carpeta `drawable` como en el anterior componente que usaba la imagen de instagram, asi:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/926732ad-f55c-49ef-80a0-02708b91deee)

La imagen usada es la siguiente:

![fb](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/9fc71427-4747-4459-a959-2a4a94fcd6da)

Y el resultado obtenido hasta el momento es el siguiente:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/61a7d328-a463-462f-bc2a-ac316c626041)

Ahora vamos a crear el composable `Footer(){}` este será el código que usaremos:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/0114bffc-ad15-496a-90e3-d81bb2be1967)

Notese que en este composable se hace el llamado a otra función, la función `SingUp()`, esta es otro composable que básicamente tendrá dos textos, uno de color gris(0xFFB5B5B5) y otro de color azul claro(0xFF4EA9E9). Este será nuestro composable `SingUp(){}`:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/802b19fd-0f65-4be9-8332-6046b90aade8)


Este es el resultado de lo que llevamos construido hasta el momento:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/e0876399-45f1-4dcd-8ab4-ae2be189d794)

Finalmente hacemos unos cambios esteticos a nuestro Log In de la siguiente manera:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/7cf60c74-41bc-47d0-a036-211631b2ff6c)


![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/0cff7d81-405e-4dc5-911b-d6969bfcf563)

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/bc36b55b-b93e-44e2-b2ae-f432947adf4b)

Y este es nuestro resultado final:

![image](https://github.com/juangomez88/Exposicion-JetpackCompose/assets/60585685/fd60541e-e7ae-4b7e-8a99-bb3939b1b56f)



