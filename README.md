# Desafio DIO Repositório	

## Um repositório contendo algumas informações sobre o que foi aprendido durante o módulo de Git e Github :happy:



### Entendendo o SHA1 e um dos motivos dele ser tão seguro 

A sigla SHA significa Secure Hash Algorithm (Algoritmo de hash seguro) é um conjunto de funções hash criptográficas projetadas pela NSA (Agência de Segurança Nacional dos EUA). o SHA1 embaralha determinado arquivo, imagem ou texto para que seja gerado um conjunto de caracteres identificadores, caracteres esses que possuem 40 dígitos.

Esses quarenta dígitos são sempre únicos. Se você pegar um texto enorme e passar ele por esse algoritmo, ele vai gerar esse conjunto de caracteres, se você alterar uma vírgula que seja desse texto, já será gerado outro conjunto.

[Quero entender mais sobre o SHA1](https://blog.minhastack.com/sha1-um-dos-motivos-pelo-qual-o-git-e-tao-seguro-entenda/)

## Funcionamento Interno e Objetos do Git

• Objetos internos (Objetos Fundamentais).
    
    
    -> Blobs 
    -> Trees
    -> Commits
    
    Esses são os 3 tipos básicos do Git responsáveis pelo versionamento dos códigos.
    
    (Blobs) -> O blob é um objeto do GIT que contém metadados que são tipo do objeto, o tamanho do arquivo, tamanho da string entre outros.


​    
    (Tree) -> As tree, são objetos que armazenam as blobs, as blobs sendo o tipo básico de composição e as tree armazenando e apontando para tipos de blobs diferentes e um outro tipo de estruturas de dados que são os commits.
    Uma arvore pode apontar para outra arvore da mesma forma que um diretório pode ter outro diretório.
    As arvores também tem um sha1 desse metadado


​    
    Ou seja as tree tem um sha1 e possuem blobs que possuem sha1 quando alteramos o sha1 de uma blob dentro da tree mudamos todo o contexto de encriptação de um arquivo.


Uma blob é um objeto que encapsula todo comportamentos de diretórios e ela é usada para apontar para diretórios que contém arquivos e por consequência apontar para arquivos também.


(Commit) -> Commit é o objeto que vai juntar tudo que vai dar sentido para alteração que estamos fazendo, então o commit aponta para um arvore, o commit aponta para um parente ou seja o ultimo commit realizado antes dele, o commit aponta para um autor e aponta para uma mensagem também

O commit ele leva o nome do autor e também possuem um timestemp (Carimbo de tempo).
O commit possuem um sha1 e é único para cada autor.

[Quero saber mais sobre os objetos internos do Git](https://git-scm.com/book/pt-br/v2/Funcionamento-Interno-do-Git-Objetos-do-Git)

## O que são as Chaves SSH Git?

O **SSH** é um protocolo de rede que permite que a conexão com determinados servidores por meio de uma comunicação criptografada, trazendo mais segurança para as transações de dados.
