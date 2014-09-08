#Conceito de NoSQL e intro ao MongoDB


##NO-SQL
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
	<li>Redis</li>
	<li>Riak</li>
	<li>Memcached</li>
</ul>		
####2. 	Coluna
<ul>
	<li>HBase(Yahoo)</li>
	<li>Cassandra(Facebook)</li>
	<li>BigTable(Google)</li>
</ul>		
####3. 	Documento
<ul>
	<li>CouchDB</li>
	<li>MongoDB  \o/</li>
</ul>
####4. 	Grafo
<ul>
	<li>Neo4J</li>
	<li>OrirenteDB(Misto)</li>
</ul>



##MongoDB
>O MongoDB é um banco NoSQL orientado a documentos feito em C++ e criado em 2007 pelos criadores da DoubleClick. Os mesmos após vender a  empresa para a Google e ficar fora do mercado por um ano criaram o MongoDB pois estavam cansados da dificuldade de escalar bancos relacionais.


###JavaScript
>Apesar de ser escrito em C++ o shell do MongoDB roda JavaScript o que facilita muito na manutenção inicial do banco pois pode-se criar desde variáveis até funções e etc, fora é claro que o JSON utilizado pelo MongoDB equivale a um Objeto Literal no JS.


###JSON
>O MongoDB manipula os dados através de JSON(JavaScript Object Notation), o JSON é um formato utilizado para integrar aplicações assim como o XML porém com uma sintaxe mais limpa e simples de se trabalhar, principalmente para quem utiliza JavaScript.


###BSON X JSON
>Operacionalmente o MongoDb utiliza JSON, porém, ao salvar os dados no disco o formato utilizado pelo MongoDB é o BSON, que é a forma binária do JSON, ao salvar os dados o MongoDB pré-aloca um espaço para que os dados sejam salvos no mesmo setor do HD, agilizando assim tanto leitura quanto escrita de informação.