DATA SCIENCE-ARMAZENAMENTO E ESCRITA

Apresentação do Treinamento
Seja bem vindo ao segundo módulo da trilha de Big Data Science.

Neste módulo iremos aprender o básico das seguintes ferramentas:

•MongoDB

•Redis

•Kafka

•Elastic

Não é obrigatório fazer a instalação de todas as ferramentas para concluir o treinamento, algumas aulas estão como opcionais.

### #Nosql- Schema bem flexivel,Alta performace,NoSQL

### •Banco de dados não relacionais
### - Características
    •Alto desempenho
    •Arquitetura distribuída
    •Schema não é rígido

### -Tipos de banco de dados
    •SQL Relacional
    •NoSQL
 

## NoSQL Armazenamento

#### SQL Relacional
    •Orientado a Linha
   
#### NoSQL
    •Orientado a Colunas

    •Chave Valor

    •Orientado a Grafos

    •Orientado a Documentos

# BASE x ACID
## Atomicidade
•A transação será executada totalmente ou
não será executada

## Consistência
•Garantir visão única dos dados
## Isolamento
•Garantir que a transação não será interferida
por outra concorrente

## Durabilidade
•Garantir o que está salvo, não será mais
perdido

## Basically A vailable
•Basicamente disponível Aplicação funciona
sempre

## Soft State
•Estado leve Não precisa ser consistente
sempre
oEventually Consistent
•Eventualmente consistente Aplicação
torna se consistente em um momento

# Teorema CAP
Impossível no armazenamento de dados distribuído garantir mais de duas das três garantias:

•Consistency 

    Quando armazenar o dado
        •Todos os usuário tem acesso

•A vailability 

    Quando solicitar o dado         
        •Sempre irá ser retornado

•Partition Tolerance(Tolerância a Partição de Rede / Tolerância a falhas)
    
    Quando falhar a rede
        •O sistema continuará funcionando

MongoDB
Banco de dados
 
    •Distribuído
    •NoSQL
    •Orientado a documentos

Formato BSON (JSON Binário)
Esquema flexível
Criado em 2007 pela 10gen, hoje MongoDB Inc.

Primeira versão liberada em 2009
https://www.mongodb.com/

Versões
MongoDB 11
MongoDB Community

Gratuito
•Open source

Github : https://github.com/mongodb/mongo/

oMongoDB Enterprise

•Assinatura MongoDB Enterprise Advanced
•Inclui suporte para implantação do MongoDB
•Recursos adicionais
    o LDAP
    o Kerberos
    o Criptografia em disco
    o A uditoria

Banco Relacional x MongoDB 12
oVersão 3.2 Validação de esquema
oVersão 4.2 Transações Distribuídas
o https://docs.mongodb.com/manual/release 

notes/Relacional
MongoDB
Banco de dados

Banco de dados
Tabela
Coleção
Registro (Linha)
Documento
Coluna
Atributo
Índice
Índice

