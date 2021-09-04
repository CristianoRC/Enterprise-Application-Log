# Enterprise Application Log

- [Exemplo com .NET + NEST + ElasticSearch + Kibana](./Elastic-Kibana)


## Estrategias para guarda log

- O ideia é a aplicação não escrever o log diretamente no ElasticSearch, pois, é uma tarefa muito custosa computacionalmente.
- Para resolver o problema de não enviar uma request HTTP toda vez podemos colocar no lugar uma fila(custo muito menor).
- 

## Elastic Search
- É o nosso Back-end, local que gerencia o nosso Log.
- Não é um banco de dados é um índice, podemos perder dados que estão lá, serve para log e não para dados de auditoria.
- Vem do projeto Apache Lucene.


## LogStash
- Seu trabalho é pegar os dados de diversos lugares e guardar no Elastic
- Com isso redusimos o processo da API e deixamos para processar quando der e no tempo que der.

## Kibana

- Forma de organizar os logs e gerar relatórios
- Relatórios podem ser técnicos ou com foco em negócio.
- Para ter uma parte autenticada precisamos usar a versão paga da aplicação, ou bloquear o acesso por IP.