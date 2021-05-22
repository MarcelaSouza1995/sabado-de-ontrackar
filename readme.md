## Bloco 23 - Introdução ao MongoDB


## Dia23.1 Introdução

O MongoDb possui diversas ferramentas como, por exemplo, mongo , mongosh , Compass e outras ferramentas de terceiros. Você pode utilizar o que achar melhor para executar as queries , o importante é realizá-las.
Utilizando a coleção bios , construa queries para retornar os seguintes itens:

[Coleção bios](https://docs.mongodb.com/manual/reference/bios-example-collection/)



#### Exercício 1 : Retorne o documento com _id igual a 8.

#### Exercício 2 : Retorne o documento com _id igual a 8, mas só exiba os campos: _id e name .
#### Exercício 3 : Retorne apenas os campos name e birth do documento com _id igual a 8.
#### Exercício 4 : Retorne todos os documentos em que o campo name.first seja igual a John , utilizando o método pretty() .
#### Exercício 5 : Retorne os 3 primeiros documentos da coleção bios utilizando o método pretty() .
#### Exercício 6 : Retorne 2 documentos da coleção bios pulando os 5 primeiros documentos.

Utilizando o mongoimport , importe o arquivo books.json para a sua instância local do MongoDB e utilize a coleção books para construir queries para as seguintes questões:

#### Exercício 7 : Retorne a quantidade de documentos da coleção books .
#### Exercício 8 : Conte quantos livros existem com o status "PUBLISH" .
#### Exercício 9 : Exiba os campos title , isbn e pageCount dos 3 primeiros livros. NÃO retorne o campo _id .
#### Exercício 10: Pule 5 documentos e exiba os campos _id , title , authors e status dos livros com status "MEAP" , limitando-se a 10 documentos.



## Dia 23.2 Filter Operators

Para os exercícios a seguir, utilizaremos um dataset que contém dados de Super-Heróis.
Faça o download do arquivo JSON:
[Coleção superheros](https://s3.us-east-2.amazonaws.com/assets.app.betrybe.com/back-end/mongodb/superheroes-957c961ea234d06d7cfdae73c87d47a6.json)

Após fazer o download do arquivo, importe-o para o MongoDB através da ferramenta mongoimport.
No seu terminal, utilize o seguinte comando (lembre-se de substituir o caminho do arquivo):

```
mongoimport --db class --collection superheroes <caminho_do_arquivo>
```
Pronto! Você já tem uma base de dados com 734 super-heróis.
Para conferir, conecte-se à instância do seu banco de dados utilizando o Mongo Shell e execute os seguintes comandos:

```
use class;

db.superheroes.count();
```
Os documentos têm a seguinte estrutura:

```
{
    "_id" : ObjectId("5e4ed2b2866be74b5b26ebf1"),
    "name" : "Abin Sur",
    "alignment" : "good",
    "gender" : "Male",
    "race" : "Ungaran",
    "aspects" : {
        "eyeColor" : "blue",
        "hairColor" : "No Hair",
        "skinColor" : "red",
        "height" : 185,
        "weight" : 40.82
    },
    "publisher" : "DC Comics"
}
```

### Exercícios

O MongoDb possui diversas ferramentas, como, por exemplo, mongo , mongosh , Compass e outras ferramentas de terceiros. 
Você pode utilizar o que achar melhor para executar as queries , o importante é realizá-las.

#### Exercício 1: Inspecione um documento para que você se familiarize com eles. Entenda os campos e os níveis existentes no documento escolhido.
#### Exercício 2: Selecione todos os super-heróis com menos de 1.80m de altura. Lembre-se de que essa informação está gravada em centímetros.
#### Exercício 3: Retorne o total de super-heróis menores que 1.80m.
#### Exercício 4: Retorne o total de super-heróis com até 1.80m.
#### Exercício 5: Selecione um super-herói com 2.00m ou mais de altura.
#### Exercício 6: Retorne o total de super-heróis com 2.00m ou mais.
#### Exercício 7: Selecione todos os super-heróis que têm olhos verdes.
#### Exercício 8: Retorne o total de super-heróis com olhos azuis.
#### Exercício 9: Utilizando o operador $in , selecione todos os super-heróis com cabelos pretos ou carecas ( "No Hair" ).
#### Exercício 10: Retorne o total de super-heróis com cabelos pretos ou carecas ( "No Hair" ).
#### Exercício 11: Retorne o total de super-heróis que não tenham cabelos pretos ou não sejam carecas.
#### Exercício 12: Utilizando o operador $not , retorne o total de super-heróis que não tenham mais de 1.80m de altura.
#### Exercício 13: Selecione todos os super-heróis que não sejam humanos ou que não sejam maiores do que 1.80m .
#### Exercício 14: Selecione todos os super-heróis com 1.80m ou 2.00m de altura e que sejam publicados pela Marvel Comics .
#### Exercício 15: Selecione todos os super-heróis que pesem entre 80kg e 100kg , sejam Humanos ou Mutantes e não sejam publicados pela DC Comics .
#### Exercício 16: Retorne o total de documentos que não contêm o campo race .
#### Exercício 17: Retorne o total de documentos que contêm o campo hairColor .
#### Exercício 18: Remova apenas um documento publicado pela Sony Pictures .
#### Exercício 19: Remova todos os documentos publicados pelo George Lucas .
