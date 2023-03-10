# Crea tu propio CV con Json-Resume

Puedes crear tu propio CV para desarrolladores con [jsonresume](https://jsonresume.org/).

## Instalacion/actualizacion de npm

Asegurate de tener la version 18 de npm. Puedes actualizarla ejecutando los siguientes comandos:

```
sudo npm cache clean -f
```

```
sudo npm install -g n
```

```
sudo n stable
```

## Instalacion de resume cli

Una vez que tenemos actualizado el npm instalamos resume-cli:

```
npm install -g resume-cli
```

## Creando el archivo resume.json

Debemos crear el archivo resume.json:

```
resume init
```

Validamos que no tenga errores:

```
validate resume.json
```

## Correr el CV

Para correr el CV:

```
resume serve 
```
> Lo muestra con el theme por defecto


Si desea visualizar otro theme debe agregar --theme [nombre theme]

```
resume serve --theme elegant 
```
> Ejemplo utilizando el tema elegant

```
resume serve --theme even 
```
> Ejemplo utilizando el tema event


```
resume serve --theme kendall 
```
> Ejemplo utilizando el tema kendall

## Exportar el PDF usando un tema:

- Se necesita instalar primero el theme que queres descargar como PDF, para eso seguimos los siguentes pasos suponiendo que vamos a descargarlo con el tema kendall:

- Crea la carpeta `node_modules` (en el directorio donde esta public, package y resume)
- Dentro de la carpeta `node_modules` crea la carpeta `jsonresume-theme-kendall`
- Por ultimo, creamos el archivo `index.js` en la carpeta `jsonresume-theme-kendall`

Por ultimo, ejecutamos los siguientes comandos:

```
npm install jsonresume-theme-kendall
```

```
resume export resume.pdf --theme ./node_modules/jsonresume-theme-kendall
```

> El ejemplo exporta con el theme kendall