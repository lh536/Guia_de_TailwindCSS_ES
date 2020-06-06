# **GUÍA RÁPIDA DE TailwindCSS**

[TOC]

##### <u>**INSTALACIÓN**</u>

 

Para usar tailwindcss en nuestro proyecto tenemos dos maneras de incluirlo:



\1.   A través de un CDN. ( [](https://unpkg.com/tailwindcss@^1.0/dist/tailwind.min.css))

\2.   Instalando tailwindcss como un módulo de node. 

 

*Se recomienda hacerlo como un módulo de node porque con el CDN perderemos características de tailwindcss.*



Siguiendo dicha recomendación instalaremos tailwindcss como un módulo de node (no te preocupes si no eres experto en nodejs, solo necesitas tener instalada la versión más reciente de node y npm en tú maquina): 



- Abrimos la consola y nos situamos en la carpeta del proyecto e inicializamos el directorio para trabajar con node: 

  ```
  npm init
  ```

  

- Luego instalamos tailwindcss como dependencia de nuestro proyecto:

  ```
  npm i -D tailwindcss
  ```





------

**Nota:**

![](C:\Users\Invitados_\Downloads\oie_transparent(1).png)

------



Ahora aparecerá en la carpeta ***node_modules*** de nuestro proyecto la dependencia de tailwindcss. Si tienes preferencia por trabajar con **PostCSS** tendrás que incluir tailwindcss con la declaración:

```css
/*A este fichero lo nombraremos tailwind.css*/
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";
```



De lo contrario debemos usar la directiva **@tailwind** así:

```css
/*A este fichero lo nombraremos tailwind.css*/
@tailwind base;       
@tailwind components; 
@tailwind utilities; 
```



Te estarás preguntando porqué si ya tengo declaradas las directivas de tailwindcss en mi css aún no funciona, esto se debe a que primero tenemos que compilar nuestro fichero principal a otro de salida. 



**¿Recuerdas que al fichero css lo nombramos tailwind.css?**

Usaremos ese fichero para producir la salida a un fichero nuevo llamado styles.css. 



Para compilarlo al fichero de salida styles.css escribimos el siguiente comando en nuestra consola:

```
npx tailwindcss build tailwind.css –o styles.css
```



El anterior comando permite usar el CLI de tailwindcss para generar el fichero de salida con el código compilado de las clases de tailwind.

 

Ya con esto podemos empezar a utilizar todas las clases que nos ofrece tailwindcss. 

 

A continuación veremos algunos ejemplos prácticos para que pruebes algunas características. Para conocer todas las características que contiene tailwindcss en sus directivas visita https://tailwindcss.com/.



------

**Nota:**

![oie_transparent(2)](C:\Users\Invitados_\Downloads\oie_transparent(2).png)



Si quieres personalizar tailwindcss cambiando por ejemplo el ancho de los breakpoints de las mediaqueries o el tamaño base de una fuente ingresa el siguiente comando en consola:

```
npx tailwindcss init
```



El anterior comando crea el siguiente fichero tailwind-config.js:

![configtail](C:\Users\Invitados_\Documents\Rodrigo\configtail.png)



Si deseas un fichero de configuración con un nombre diferente ejecuta el siguiente comando:

```
npx tailwindcss init nuevonombre-config.js
```



Dentro de tailwind.config.js encontraremos las propiedades theme, variants y plugins. 



En **theme** podemos cambiar la paleta de colores, los breakpoints, fuentes tipográficas, valores de border radius, opacidad, espaciados entre otros (visita https://tailwindcss.com/docs/theme para conocer toda la configuración que puedes modificar en theme).

 

En **variants** controlaremos los elementos que tendrán una variante al implementar el responsive en nuestro sitio, además de los elementos que van a tener cambios cuando se les agregan pseudo-clases (visita https://tailwindcss.com/docs/configuring-variants para conocer toda la configuración que puedes modificar en variants).

 

En **plugins** tendremos la capacidad de inyectar código css de terceros o nuestro a través de Javascript lo que nos va permitir adicionar componentes y utilidades, entre otros (visita [https://tailwindcss.com/docs/plugins](https://tailwindcss.com/docs/plugins ) para conocer  toda la configuración que puedes modificar en plugins).



Y así es como luce un fichero de configuración personalizada de tailwindcss, recuerda que tanto theme como variants y plugins son opcionales:

![exampletail](C:\Users\Invitados_\Documents\Rodrigo\exampletail.png)

------



##### <u>**EJEMPLOS PRÁCTICOS**</u>

