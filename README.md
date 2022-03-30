# Composite Key ( Chave Composta )
## I. É uma combinação de Colunas da Tabela do Database
### 1. Como por exemplo: há uma tabela chamada Cliente e em vez de só usar o campo ID como uma Primary Key, é possível usar o Email e o ID de mais de duas Colunas.
### 2. A tabela CLIENTE tem id e email, mas também é possível colocar email como parte do ID, já que email é único para todo CLIENTE e é not null.
|   CLIENTE   | :---: | :---: |
|   :---:     |   :---:     | :---: |
|id  |  :---:| :---: |
|email |  :---:| :---: |
|name  |  :---:| :---: |
|PRIMARY KEY (id, email) |  :---:| :---: |
|   | |  |
### 3. Em PRIMARY KEY colocamos entre paretêses id e email. Isso é uma Composite Key (chave Composta).
## II. As anotações envolvidas:
### A. @IdClass
### B. @Embeddable
### C. @EmbeddedId
### D. @ID = é possível utilizar também. Apesar de na maioria ser utilizadas: @Embeddable e @EmbeddedId routs.
## III. Passos:
### 1. Criar a Classe Key: Então o Composite Key ( chave composta ) terá sua própria Classe.
### 2. Usar a Classe Key. E e então usaremos a Classe Key dentro das Entidades através das anotações acima.
### 3. Criar Repository
### 4. Configurar Datasource ( application.properties )
### 5. Testar a aplicação.