# Maxcondo

Esta é uma api de desenvolvimento para o sistema de condominios.

## Create User

para criar um usuario precisamos enviar um post com o nome dele para a url /user/create e o post deve retornar um json com o usuario criado e seu respectivo ID.

>chamada: curl -d "username=admin&apt=303" http://localhost:8000/user/create

>retorno: {
        "username": "dusty",
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
