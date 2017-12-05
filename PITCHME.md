<!-- $theme: default -->

# GraphQL

![](assets/graphql_logo.png)

*"query language for APIs"*

---

## Historia

Anunciado por Facebook en 2015 (usado internamente desde 2012)

Usado actualmente por:
- Github
- Pinterest
- Coursera
- Shopify

---

## Qué no es

No es una librería o un framework

__*Es una especificación*__

Que está ya implementada en múltiples lenguajes:
* Python
* Scala
* Ruby
* Java
* ...

---

## GraphQL ventajas

* __Reduce el número de peticiones__

---

## Reduce el número de peticiones: REST

```
GET /api/user/me
GET /api/user/me/groups
```

---

## Reduce el número de peticiones: GraphQL

```
query {
    User(id: "me") {
        id
        avatar
        groups(last: 1) {
            name
        }
    }
}
```

---

## GraphQL ventajas

* Reduce el número de peticiones
* __Solo envío de datos necesarios__

---

## Solo envío de datos necesarios

```
{
    "data": {
        "User": {
            "id": "user.1234",
            "avatar": "http://example.com/avatar/1234",
            "groups": [
                {"name": "My group"}
            ]
        }
    }
}
```

---

## GraphQL ventajas

* Reduce el número de peticiones
* Solo envío de datos necesarios
* __Esquema & Tipado__

---

## Esquema & Tipado

```
type Group {
  id: ID!
  createdAt: String!
  name: String!
  members: [User]
}
```

---

## GraphQL ventajas

* Reduce el número de peticiones
* Solo envío de datos necesarios
* Esquema & Tipado

---

## GraphQL

* Un único end-point: `/graphql`
* Enviamos datos usando http method `POST`
* Tipos básicos:
    * Query: Consulta de datos
    * Mutation: Crear, modificar o eliminar datos
    * Subscription: Recibir eventos en tiempo real

---

## En cliente

* [vue-apollo](https://github.com/Akryum/vue-apollo)
* [apollo-android](https://github.com/apollographql/apollo-android)
* [apollo-ios](https://github.com/apollographql/apollo-ios)
* [relay](https://facebook.github.io/relay/)

---

## GraphiQL

![](assets/graphiql.png)

---

# EOF
