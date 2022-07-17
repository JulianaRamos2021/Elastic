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


c) Nome = hd e descrição = windows


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


6. Reindexar o índice produto para concessionaria2, com o campo quantidade para o tipo short


Criando o index concessionaria2
![image](https://user-images.githubusercontent.com/78691172/179399310-294e4805-1aae-4f5f-8505-235a1faaf823.png)




7. Visualizar o mapeamento do índice produto2

8. Fechar o índice produto

9. Pesquisar todos os documentos no índice produto

10. Abrir o índice produto
