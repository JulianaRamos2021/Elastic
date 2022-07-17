# Elastic
Elasticsearch é um mecanismo de busca e análise de dados distribuído, gratuito e aberto para todos os tipos de dados, incluindo textuais, numéricos, geoespaciais, estruturados e não estruturados. 


## Como funciona
Os dados brutos fluem para o Elasticsearch de uma variedade de fontes, incluindo logs, metrics de sistema e aplicações web. Ingestão de dados é o processo pelo qual os dados brutos são analisados, normalizados e enriquecidos antes de serem indexados no Elasticsearch. Depois que os dados são indexados no Elasticsearch, os usuários podem executar consultas complexas com base em seus dados e usar agregações para recuperar resumos complexos dos dados. Do Kibana, os usuários podem criar visualizações avançadas dos dados, compartilhar dashboards e gerenciar o Elastic Stack. (Fonte: https://www.elastic.co/pt/what-is/elasticsearch)


Para este treinamento utilizei a avaliação gratuita do Elastic, o cadastro pode ser efetuado no site (https://www.elastic.co/pt/)


### Carregando dados

Já com o cadastro pronto acessei Home > Machine Learning.

![image](https://user-images.githubusercontent.com/78691172/179357928-230b3866-5608-4b5b-87a7-cadaafd02bfa.png)  


Em seguida File.
![image](https://user-images.githubusercontent.com/78691172/179358145-5ba0eecf-9779-4106-92c6-0771f5a2def2.png)  

     
Aqui estou baixando dois arquivos: cars.bulk e populacao.LA (arquivo disponibilizado no bootcamp data engineer Semantix)
![image](https://user-images.githubusercontent.com/78691172/179357106-e60e036a-e82a-4ab3-a5c7-7f6ac12cf7b5.png)  
      
Ao baixar o arquivo a ferramenta apresenta um resumo geral dos dados apresentados.
![image](https://user-images.githubusercontent.com/78691172/179357139-c960ea33-69cd-4714-915c-ddc59dc6c23d.png)  
   

Em seguida é necessário definir o nome do indeex (seu arquivo).
![image](https://user-images.githubusercontent.com/78691172/179357158-7fef612a-d86b-4bc9-8aa5-ac6509d41454.png)  





### Visualizando dados

Após baixar vamos acessar os dados através de Management> Dev tools.
![image](https://user-images.githubusercontent.com/78691172/179357303-b058a91c-9cf0-4717-b7cf-6817fb8c1c0a.png)   

   
Verificando o número de documentos no index concessionária.
![image](https://user-images.githubusercontent.com/78691172/179357385-b6e808f1-f43a-4692-adad-5588e349abc9.png)   
   

Verificando o número de documentos no index população.
![image](https://user-images.githubusercontent.com/78691172/179357457-960169cb-165a-4477-8cc1-8c2abc53a8a9.png)   

Visualizando os documentos no index concessionária.    
![image](https://user-images.githubusercontent.com/78691172/179357571-8f0e123f-a22d-47f3-9a99-9066c35c138c.png)   
   
Visualizando os documentos no index população. 
![image](https://user-images.githubusercontent.com/78691172/179357648-65ad6239-402b-45ea-bddf-d4b1df87abc6.png)   



### Pesquisa e Paginação

1. Pesquisar no índice produto os documentos com os seguintes atributos:

a) Make = Honda   
  
![image](https://user-images.githubusercontent.com/78691172/179367045-80c95aed-40e9-4154-8eb9-a4d0f3dbac5f.png)





b) Cor = vermelho

![image](https://user-images.githubusercontent.com/78691172/179368889-01455f7f-27ac-4f39-bb67-77def60326c9.png)


c) cor = azul e fabricante = Toyota


![image](https://user-images.githubusercontent.com/78691172/179369047-8e7d8799-be91-49bd-bf65-23a9a4f2108b.png)
     

2. Pesquisar todos os índices, limitando a pesquisa em 5 documentos em cada página e visualizar a 4 página (Documentos entre 16 á 20 )

![image](https://user-images.githubusercontent.com/78691172/179369519-a1b66bbc-805b-423b-be9e-28693ad8cba4.png)



### Índices

1. Visualizar as configurações do índice população

![image](https://user-images.githubusercontent.com/78691172/179370405-f383dbbc-e316-4563-a165-cb4afa082f3d.png)



2. Visualizar o mapeamento do índice população

![image](https://user-images.githubusercontent.com/78691172/179370466-035039d8-6de3-4421-bd42-d267eed8d53e.png)



3. Visualizar o mapeamento do atributo color do índice concessionária

![image](https://user-images.githubusercontent.com/78691172/179370554-51a85264-9a4d-4eac-ab37-886bfd215f80.png)



4. Inserir o campo data do tipo date no índice concessionária

![image](https://user-images.githubusercontent.com/78691172/179370684-f3729839-b695-48c4-8d3a-55985da2fc3a.png)


5. Adicionar o documento:

_id: 6,  "make": "Lego",  "price": 10000,  "color": "orange",  "sold":"2020-09-18"

![image](https://user-images.githubusercontent.com/78691172/179370916-e5b71eea-98a9-427a-aedf-6379fe0ef4fb.png)


6. Reindexar o índice concessionaria para concessionaria2.

![image](https://user-images.githubusercontent.com/78691172/179399585-9717633b-7ee5-44fc-a2e2-af8ebdaaf5ac.png)


Criando o index concessionaria2
![image](https://user-images.githubusercontent.com/78691172/179399310-294e4805-1aae-4f5f-8505-235a1faaf823.png)

Copiando propriedades para o novo index
![image](https://user-images.githubusercontent.com/78691172/179399459-0a8ec9c8-53da-481b-9c3a-fc4639827c32.png)

Reindexando...
![image](https://user-images.githubusercontent.com/78691172/179399818-0ee24746-303a-49be-8b5f-4ffe2c72970c.png)


7. Visualizar o mapeamento do índice concessionaria2
![image](https://user-images.githubusercontent.com/78691172/179399927-ad3ebeca-16ba-4cbf-a16c-c17e15945434.png)


8. Fechar o índice concessionaria

![image](https://user-images.githubusercontent.com/78691172/179400112-d4e3c676-66ff-42e7-a175-9091aa80ad4b.png)


9. Pesquisar todos os documentos no índice concessionaria

Visto que o índice foi fechado não é possível acessar, por isso retornou mensagem de erro.
![image](https://user-images.githubusercontent.com/78691172/179400223-13e5762f-bb6e-408e-b787-5b462377bf5a.png)


10. Abrir o índice produto
![image](https://user-images.githubusercontent.com/78691172/179400622-c1b2af91-0299-43cf-80fc-ed03c5c6b18b.png)



### Query e Filtros

Realizar todas as buscas a seguir no índice concessionaria

Primeiro vamos confirmar se temos o índice
![image](https://user-images.githubusercontent.com/78691172/179401755-7e94d435-936e-4236-8a86-36ab9a3450d3.png)



1. Buscar no termo cor o valor verde

![image](https://user-images.githubusercontent.com/78691172/179401940-56ca4e9a-f92a-4f73-bf84-ce5aad044385.png)


2. Buscar no termo cor os valores verde e vermelho

![image](https://user-images.githubusercontent.com/78691172/179402354-f38e139e-864f-41a5-833b-b71c6c350778.png)


3. Realizar a mesma busca do item 1 e 2, desconsiderando o score


![image](https://user-images.githubusercontent.com/78691172/179403235-e754a118-9b4e-4b34-996c-f371935c640f.png)


![image](https://user-images.githubusercontent.com/78691172/179403339-de9f5971-97d8-46a7-acb8-dece158d5ea3.png)


4. Buscar os documentos que contenham a palavra “ford” no atributo fabricante
![image](https://user-images.githubusercontent.com/78691172/179403507-e74aaffb-0369-4515-bda8-93d82256afd8.png)

5. Buscar os documentos que contenham a palavra “ford” e não contenham a palavra “blue” no atributo color

![image](https://user-images.githubusercontent.com/78691172/179403776-515b09e5-4704-4947-8baf-2ecc263588a5.png)


6. Buscar os documentos que podem ter a palavra “toyota” no atributo make ou contenham a palavra “ford” e não contenham a palavra “bmw” no atributo make


![image](https://user-images.githubusercontent.com/78691172/179404348-aa633d34-4864-483a-8bcf-656c00a07de0.png)


### Consultas por Intervalo

1. Verificar se existe o índice população
O retorno como 200 significa que deu certo e 404 que houve erro na consulta.
![image](https://user-images.githubusercontent.com/78691172/179404657-f6141012-d0e6-4b7e-9a89-24bf39f17143.png)


2. Executar as consultas no índice população


a) Mostrar os documentos com o atributo "Total Population" menor que 100

![image](https://user-images.githubusercontent.com/78691172/179404767-5c312343-1f9b-4013-9cac-2660ce5ffd55.png)


b) Mostrar os documentos com o atributo "Median Age" maior que 70

![image](https://user-images.githubusercontent.com/78691172/179404892-64c66ce3-96ff-47df-8602-9085c6b810ab.png)


c) Mostrar os documentos 50 (Zip Code: 90056) à 60 (Zip Code: 90067) do índice de populacao


![image](https://user-images.githubusercontent.com/78691172/179405053-db4c2c17-7f16-469d-ae2f-7c0f93e6ebfd.png)


3. Importar através do Kibana o arquivo weekly_MSFT.csvPré-visualizar o documento (Guia Arquivos/dataset/weekly_MSFT.csv) com o índice bolsa
![image](https://user-images.githubusercontent.com/78691172/179405586-a80b7f4f-5fd6-4282-b71e-e7dcc3511629.png)


4. Executar as consultas no índice bolsa

a) Visualizar os documentos do dia 2019-01-01 à 2019-03-01. (hits = 9)
![image](https://user-images.githubusercontent.com/78691172/179405502-279cba82-2520-4238-9b3c-dc1f27c1a948.png)

b) Visualizar os documentos do dia 2019-04-01 até agora. (hits = 3)

![image](https://user-images.githubusercontent.com/78691172/179405665-f67235dc-e448-4986-b7ff-d6372700ce30.png)


### Analyzer

1. Criar os Analyzer simple, standard, brazilian e portuguese para a seguinte frase:
O elasticsearch surgiu em 2010

![image](https://user-images.githubusercontent.com/78691172/179410105-d01a04c6-00e2-4b49-a7cf-5b2a7e368fed.png)


![image](https://user-images.githubusercontent.com/78691172/179409827-51e8d94a-d72f-443a-8f74-bf24a968e70f.png)


![image](https://user-images.githubusercontent.com/78691172/179410449-47805a3c-e2b4-4a5c-a2cd-b130cbced865.png)


![image](https://user-images.githubusercontent.com/78691172/179410735-4ebf8db0-1e37-4a43-9e9b-c54d324a9fd3.png)





### Agregações

Realizar os exercícios no índice bolsa

1. Calcular a média do campo volume

![image](https://user-images.githubusercontent.com/78691172/179416645-201d9d40-db2e-4ea2-8386-83257c6be08a.png)


2. Calcular a estatística do campo close

3. Visualizar os documentos do dia 2019-04-01 até agora. (hits = 3)

4. Calcular a estatística do campo open do período do dia 2019-04-01 até agora

5. Calcular a mediana do campo open

6. Contar a quantidade de documentos agrupados por ano

7. Contar a quantidade de documentos de 2 anos atrás até hoje

