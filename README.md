# Qué Me Pongo 7



## Requerimiento 1
> Como usuarie de QueMePongo quiero ver todas las prendas que tengo en mi guardarropas desde el navegador para poder administrarlas
```
$ GET 'http://qmp.com/prendas'

[
 {
  "id": 1,
  "tipo": "pantalon",
  "talle": 35
  },
{
  "id": 2,
  "tipo": "pantalon",
  "talle": 35
 }
]
```
Códigos de respuesta posibles: 200



## Requerimiento 2
> Como usuario de QueMePongo, quiero crear una prenda desde el navegador
```
POST 'http://qmp.com/prendas'
```
Body:
```
{
  "tipo": "pantalon",
  "talle": 35
}
```
Respuesta posible:
```
[
 {
  "id": 3,
  "tipo": "pantalon",
  "talle": 35
  }
]
```

Códigos de respuesta posibles: 201



## Requerimiento 3
> Como usuarie de QueMePongo quiero ver una prenda en particular que tengo en mi guardarropas para poder editarla

- Ver la prenda
```
$ 'GET http://qmp.com/prendas/{id}'

[
 {
  "id": 1,
  "tipo": "pantalon",
  "talle": 35
  }
]
```
Códigos de respuesta posibles: 404, 200

- Editar la prenda

```
$ 'PUT http://qmp.com/prendas/{id}'
```
Body:
```
{
  "tipo": "pantalon",
  "talle": 35
}
```
Respuesta posible (si se encuentra el id):
```
[
 {
  "id": 1,
  "tipo": "pantalon",
  "talle": 35
  }
]
```
Códigos de respuesta posibles: 404, 200


## Requerimiento 4
> Como usuarie de QueMePongo, quiero poder eliminar una prenda de mi guardarropas
```
$ DELETE 'http://qmp.com/prendas/{id}'
```

Códigos de respuesta posibles: 404, 200



## Requerimiento 5
> Como usuarie de QueMePongo, quiero poder ver mis eventos para administrarlos
```
$ GET 'https://qmp.com/eventos'

[
 {evento},
 {evento},
 {evento}
]
```
(Un evento podria tener un Lugar, una Fecha, un Horario, un identificador, etc)
Códigos de respuesta posibles: 200



## Requerimiento 6
> Como usuarie de QueMePongo, quiero poder abrir las sugerencias de prendas para un evento en mi navegador

```
$ GET 'https://qmp.com/eventos/{id}/sugerencias'

[
 {sugerencia},
 {sugerencia},
 {sugerencia}
]
```
Códigos de respuesta posibles: 404 , 200
