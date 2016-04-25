# Interfaces con el Mundo Exterior

Los datos son leídos por medio de las interfaces _connection_. Las conexiones pueden ser archivos (la más común) o otro tipo de conexiones más "exóticas".

+ _file_, abre una conexión para un archivo
+ _gzfile_, abre una conexión para un archivo comprimido en formato gzip
+ _bzfile_, abre una conexión para un archivo comprimido en formato bzip2
+ _url_, abre una conexión a una página web

En general, las conexiones son un mecanismo que te permiten navegar en archivos u otros objetos externos. Las conexiones puedes ser vistas como traductores que nos permiten comunicarnos con objetos fuera del entorno de __R__. Esto objetos pueden ser cualquier cosa, desde una base de datos, un simple archivo de texto, o un servicio web. Las conexiones permiten a las funciones de __R__ comunicarse con objetos externos sin tener que escribir código propio para cada uno de los objetos.
