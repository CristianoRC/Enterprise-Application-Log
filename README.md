# Enterprise Application Log

![imagem](https://cdn2.iconfinder.com/data/icons/data-analytics-volume-2/512/LOG_FILE-128.png)

 
## Emplos

- [Exemplo com .NET + NEST + ElasticSearch + Kibana](./Elastic-Kibana)

## Estrategias para guarda log

- O ideia é a aplicação não escrever o log diretamente no ElasticSearch, pois, é uma tarefa muito custosa computacionalmente.
- Para resolver o problema de não enviar uma request HTTP toda vez podemos colocar no lugar uma fila(custo muito menor).
- 

## Elastic Search
- É o nosso Back-end, local que gerencia o nosso Log.
- Não é um banco de dados é um índice, podemos perder dados que estão lá, serve para log e não para dados de auditoria.
- Vem do projeto Apache Lucene.
- Um índice é como se fosse um particionamento


## LogStash
- Seu trabalho é pegar os dados de diversos lugares e guardar no Elastic
- Pega os dados, trata e manda para o Elastic
- Com isso redusimos o processo da API e deixamos para processar quando der e no tempo que der.


## Kibana

- Forma de organizar os logs e gerar relatórios
- Relatórios podem ser técnicos ou com foco em negócio.
- Pode ser usado para criar um dash de infra(RAM, Containers...)
- Para ter uma parte autenticada precisamos usar a versão paga da aplicação, ou bloquear o acesso por IP.


## Metricbeat
- Monitora a infra e manda dados para o ElasticSearch


## ElasticHQ
- Ferramenta para monitorar o ElasticSearch
- O Kibana serve para ver os dados que chegam e o ElasticHQ serve para monitar índice, espaço em disco e coisas do tipo.


---

Usado como base o projeto Enterprise Application Log criado por Gago.io, quem quiser dar uma olhada no assunto: [Artigo](https://gago.io/blog/projetos/enterprise-application-log/)