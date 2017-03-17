# Maxcondo

Esta é uma api de desenvolvimento para o sistema de condominios.

## Create User

para criar um usuario precisamos enviar um post com o nome dele para a url /user/create e o post deve retornar um json com o usuario criado e seu respectivo ID.

>chamada: curl -d "name=admin&apt=303" http://localhost:5000/user/create

>retorno: {
        "name": "dusty",
        "id": "1",
        "apt": "303"
      }


## Get User

chamada de um usuario por id /user/#id

>chamada: curl http://localhost:8000/user/1

>retorno: {
        "username": "dusty",
        "id": "1",
        "apt": "303"
      }


## Create Edificio

para criar um residencial precisamos enviar um post com o nome dele, o id do sindico para a url /edificio/create e o post deve retornar um json com o edificio criado e seu respectivo ID.

>chamada: curl -d "user_id=1&name=Residencial dos Testes" http://localhost:5000/edificio/create

>retorno: {
        "user_id": "1",
        "id": "1",
        "name": "Residencial dos Testes",
        "apt": "303"
      }

### Get Edificio por sindico

>chamada: curl http://localhost:5000/edificio/by_sindico/1

>retorno: [
              {
                "user_id": "1",
                "id": "1",
                "name": "Residencial dos Testes",
                "apt": "303"
              },
              {
                "user_id": "1",
                "id": "2",
                "name": "Residencial dos Testes 2",
                "apt": "201"
              },
      ]
