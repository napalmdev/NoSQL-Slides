#Conceito de NoSQL e intro ao MongoDB


#NO-SQL
>Apesar do impacto do termo o mesmo não significa não ao SQL e sim Not Only SQL 
e é um movimento de Bancos de Dados que não trabalham no modelo Relacional.

####1. Como eu conheci NoSQL
>Quando comecei com Web e mesmo após um tempo de desenvolvimento sempre me perguntava porque meu sistema rodando localmente era tão mais lento quanto sistemas grandes como Orkut(=p), Hotmail, Google e etc, é claro que em questão de hardware esses sistemas eram imcomparáveis, porém, eles proviam a aplicação para milhões de usuários e meu sistema somente para mim e mesmo assim era incrivelmente mais lento, sabia que tinha alguma coisa que não estava certa, foi quando eu li uma matéria sobre bancos NoSQL e logo em seguida descobri o MongoDB, e então tudo fez sentido, usar a Liguagem certa com o Banco de Dados certo para determinada aplicação dentre outras coisas é o que a fará mais rápida ou mais lenta.


####2. Todo desenvolvedor deve conhecer NoSQL
>A assimilação do conceito de NoSQL é essencial para todo desenvolvedor, seja para Web,Desktop ou Mobile. Conhecendo as possibilidades oferecidas por Bancos de Dados NoSQL, o leque de escolhas do desenvolvedor aumenta exponencialmente, possibilitando ao desenvolvedor escolher a melhor opção de Banco de Dados para uma aplicação que precise por exemplo ser escalável.  


##Por que usar NoSQL?
####1. Funcionalidades e Forma de Modelagem diferenciada
>Diferente dos bancos relacionais os bancos NoSQL tem formas de modelagem diferentes uns dos outros, não existe um só padrão, pois não existe apenas uma categoria de banco NoSQL.


####2. Escalabilidade
>Os bancos NoSQL surgiram da necessidade de escalar mais facilmente as aplicações, visto que os sistemas crescem rapidamente nos dias de hoje. Escalar bancos relacionais é complexo e não muito eficaz  então os bancos NoSQL caíram como uma luva para esta necessidade, a escalabilidade que até então só era feita verticalmente(Aumento de Hardware) começou a ser utilizada horizontalmente(distribuindo a aplicação).


####3. Atende a Necessidades Específicas
>Os bancos relacionais foram criados com o intuito de atender a todas a situações, e era o que precisava ser feito na época. Os mesmos sempre foram utilizados com "Balas de Prata", porém como desenvolvedores já devemos estar cientes de que não existe Bala de Prata, e é nisso que os bancos NoSQL se diferem dos Relacionais, em NoSQl como já citado não existe apenas uma categoria de DB, são várias delas cada uma com forma de trabalho completamente diferente da outra, a cada uma delas atende a uma necessidade de aplicação diferente ex: 

>Cache; 
Alto Índice de I/O; 
Cargas Gigantescas de Dados;
Relacionamentos Complexos entre Elementos do DB;
etc..


####4. Sistemas de Alta Performance
>Todas as grandes aplicações criadas nos dias de hoje utilizam algum banco NoSQL, empresas como Google, Facebook, Twitter, Linkedin e Amazon estão fortemente envolvidas no movimento NoSQL e a maioria delas tem seu próprio DB, abaixo segue alguns modelos de DB's NoSQLe quais empresas utilizam.





##Modelos de Bancos NoSQL

####1. 	Chave-Valor
<ul>
	<li>Redis - http://redis.io/</li>
	<li>Riak - http://basho.com/riak/</li>
	<li>Memcached - http://memcached.org/</li>
</ul>		
####2. 	Coluna
<ul>
	<li>HBase(Yahoo) - http://hbase.apache.org/</li>
	<li>Cassandra(Facebook) - http://cassandra.apache.org/</li>
	<li>BigTable(Google) - http://en.wikipedia.org/wiki/BigTable</li>
</ul>		
####3. 	Documento
<ul>
	<li>CouchDB - http://couchdb.apache.org/</li>
	<li>MongoDB - http://www.mongodb.org/  \o/</li>
</ul>
####4. 	Grafo
<ul>
	<li>Neo4J - http://www.neo4j.org/</li>
	<li>OrirenteDB(Misto) - http://www.orientechnologies.com/orientdb/</li>
</ul>








#MongoDB
>O MongoDB é um banco NoSQL orientado a documentos feito em C++ e criado em 2007 pelos criadores da DoubleClick. Os mesmos após vender a  empresa para a Google e ficar fora do mercado por um ano criaram o MongoDB pois estavam cansados da dificuldade de escalar bancos relacionais.


###JavaScript
>Apesar de ser escrito em C++ o shell do MongoDB roda JavaScript o que facilita muito na manutenção inicial do banco pois pode-se criar desde variáveis até funções e etc, fora é claro que o JSON utilizado pelo MongoDB equivale a um Objeto Literal no JS.


###Quem usa?
>Antes de falar sobre as funcionalidades do MongoDB, é interessante avaliar quais empresas hoje utilizam o mesmo, e tirar as dúvidas sobre a credibilidade dele no mercado, vamos a alguns cases:<br />
[Clique aqui](http://www.mongodb.com/customers) para conhecer alguns cases de sucesso com MongoDB e inclusive depoimentos sobre como foi a implantação do mesmo nestas empresas.<br />
No Brasil também temos grandes empresas utilizando o MongoDB como Globo.com e EasyTaxi.



###Equivalentes de DB's Relacionais em MongoDB
<table>
	<tr><td>DATABASE</td><td>DATABASE</td></tr>
	<tr><td>TABLE</td><td>COLLECTION</td></tr>
	<tr><td>ROWS</td><td>DOCUMENT JSON</td></tr>
	<tr><td>QUERY</td><td>QUERY</td></tr>
	<tr><td>INDEX</td><td>INDEX</td></tr>
	<tr><td>PARTITION</td><td>SHARD</td></tr>
</table>



###JSON
>O MongoDB retorna os dados no formato JSON(JavaScript Object Notation), o JSON é um formato utilizado para integrar aplicações assim como o XML, porém com uma sintaxe mais limpa e simples de se trabalhar, principalmente para quem utiliza JavaScript, veja a seguir um exemplo de JSON:


	{
	    "glossary": {
	        "title": "example glossary",
			"GlossDiv": {
	            "title": "S",
				"GlossList": {
	                "GlossEntry": {
	                    "ID": "SGML",
						"SortAs": "SGML",
						"GlossTerm": "Standard Generalized Markup Language",
						"Acronym": "SGML",
						"Abbrev": "ISO 8879:1986",
						"GlossDef": {
	                        "para": "A meta-markup language, used to create markup languages such as DocBook.",
							"GlossSeeAlso": ["GML", "XML"]
	                    },
						"GlossSee": "markup"
	                }
	            }
	        }
	    }
	}





###BSON X JSON
>Apesar de o MongoDB retornar os dados em JSON, internamente o formato utilizado é o BSON( forma binária do JSON ).




###Schemaless
>O MongoDB é considerado um banco **Schemaless**, ou ainda, **Dynamic Schema**, ou seja, não possui uma estrutura fixa. Diferentemente do que é feito em Bancos de Dados Relacionais, no MongoDB é possível criar estruturas inteiramente heterogêneas, cada **Documento** da **Collection** pode ter campos que não existem em outros documentos, e para localizar campos que podem ou não existir em determinado documento utilizamos o operador **$exist**.




###Pré-alocação de Espaço no HD
>Quando criamos uma base de dados nova no MongoDB ele pré-aloca um espaço no HD para que os dados sejam salvos no mesmo setor do disco, fazendo isto ele previne a fragmentação de dados agilizando assim tanto leitura quanto escrita de informação. Quando o tamanho da base está quase sendo preenchido este espaço de pré-alocação é dobrado automaticamente pelo MongoDB.




###Schema Design
>Apesar do MongoDB ser **Dynamic Schema**, é interessante definir uma estrutura a qual sua aplicação irá seguir para inserir dados no Banco, é bom lembrar também que ao pensar em **Schema Design** em MongoDB, deve-se primeiro livrar-se do pensamento relacional, pois uma banco NoSQL qualquer criado com Schema baseado em banco relacional não utlizará todos seus recursos, e isso acabaria invalidando o uso de um Banco de Dados  Não-Relacional.<br> 
**Obs:** Os drivers de MongoDB para qualquer linguagem já vem com esta opção de criar Schemas.




###Capped Collection
>Existe um tipo especial de Collection em MongoDB conhecido como **Capped Collection**, o que ela faz é trabalhar em modo cíclico, ou seja, quando seu tamanho total(Fixo e Determinado pelo DBA) for preenchido, ela começará a se sobrescrever, causando um efeito de loop. A Capped Collection é muito utilizada para gravação de Log's do sistema, após um estudo apurado da carga de dados que a empresa poderá gerar, é decidido qual o tamanho terá a Collection, e esta gravará **n** anos de Log até ser preenchida e começar a se sobrescrever.




###Não-SQL
>O MongoDB é um banco de dados literalmente **Não-SQL**, ou seja ele não utiliza a linguagem SQL em suas Queries, em vez disso ele utiliza funções próprias, algumas delas listadas abaixo:


|Comando  |  Sintaxe  |  Descrição|
|----------------|---------------|--------------------------------------------------------------------------------------------------------------|
FIND 	|  db.example.find({});  |  Busca todos os documentos na Collection **example**  
COUNT  |  db.example.count();  |  Conta quantos Documentos existem na Collection **example** 
SORT  |  db.example.find().sort({"_id":1});  |  Busca todos os documentos na Collection **example** e ordena pelo campo _id em ordem crescente
INSERT  |  db.example.insert({"Nome":"Denis Nunes"}); | Insere um novo Documento na Collection **example** com os campos _id e nome(Denis Nunes) 
REMOVE | db.example.remove({"Nome":"Denis Nunes"}); | Deleta o Documento filtrado pelo parâmetro, neste caso o Documento inserido anteriormente
SAVE  |  db.example |  