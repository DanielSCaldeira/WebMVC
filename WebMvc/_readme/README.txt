﻿CONNECTED SERVICES -> são servicos conectados com o projeto como por exemplo o azure (serviços online).
DEPENDENCIES-> ANALYZERS -> são ferramentas de analise.
			-> PACKGES -> são pacotes do asp net core.
			-> SDK -> são pacotes que já foram instalados na maquina sobre o asp net core.
PROPERTIES -> padrao do projeto que podem serem modificadas.
WWWROOT -> nessa pasta está a todos os recursos do front-end.
CONTROLLERS-> vai estar as classes controladoras da aplicação.
MODELS-> vai quardar as view e view-models.
VIEWS-> vai estar as telas da aplicação.
	 -> SHARED-> são paginas compartilhadas por varios comtroladores como por exemplo o header que é o mesmo para todas as telas
			  -> LAYOUT-> é aonde é determinado todo o layout de todas as paginas aonde se dertemina o css, javascript e etc. Como se fosse o Index
	 -> VIEWSTART-> é aonde se define o arquivo que vai inicializar o projeto
	 -> VIEWIMPORTS-> é aonde se define quais bibliotecas gerais meu projeto vai utilizar

APPSETTINGS-> arquivo que vai conter a configuração de recursos externos exemplo conexão com o banco de dados.
PROGRAM-> ponto inicial do projeto
STARTUP-> configurações do projeto
	   -> CONFIGURESERVICES-> configura os serviços da aplicação
	   -> CONFIGURE-> configura o comportamento das requisiçoes HTTP ele pode por exemplo interceptar as requisições 

ASP NET MVC TEM PAGINAS RAZOR

------------------------------------------------------------------------------------------------------------------------

VIEWDATA-> É um objeto c# chave/valor
	CONTROLLER
Usa o objeto @VIERDATA para transportar os dados

IActionResult-> é um tipo generico que suporta todo tipo de ação

							IActionResult

|	TYPE					|		METHOD BUILDER														|
|	VIEW RESULT				|		VIEW																|
|	PartialViewResult		|		PartialView															|
|	ContentResult			|		Content																|
|	RedirectResult			|		Redirect															|
|	RedirectToRouteResult	|		RedirectToAction													|
|							|	Ex: RedirectToAction("Index", "Home", new {page = 1, sortBy = price})	|
|	JsonResult				|		Json																|
|	FileResult				|		File																|
|   HttpNotFoundResult		|		HttpNotFound														|
|	EmptyResult				|				-															|

	
	HTML
CSHTML-> aceita tags Html e codigo C#

@VIEWDATA["CHAVE"] ->	vai mostrar o valor na tela do html.
@{}-> dentro da chave pode fazer operações logicas

Gerador de codigo pela IDE
-------------------------------------------------------------------------------------------------------------
CRIACAO DE CONTROLLER
ADD -> CONTROLLER -> EMPTY
-------------------------------------------------------------------------------------------------------------
CRIAR UMA PASTA COM O MESMO NOME DA CONTROLLER NA PASTA VIEW
COLOCAR O MESMO NOME DO METODO DA CONTROLLER QUANDO CRIAR A VIEW
ADD -> VIEW -> RAZOR VIEW -> LIST
-------------------------------------------------------------------------------------------------------------
CRIACAO DE CRUD COMPLETO 
CONTROLLER-> ADD-> NEW SCANFFOLDED ITEM-> MVC CONTROLLER WITH VIEW USING ENTITY FRAMEWORK
CLICAR NO + PARA ADICIONAR O DB_CONTEXT DO ENTITY FRAMEWORK
-------------------------------------------------------------------------------------------------------------
Cria a migration
Gerar o Midration -> abrir o package Manager Console -> execultar o comando "Add-Migration Initial"
											   Ele vai gerar a pasta migration
Atualiza a migration 
xecultar o comando "Update-Database"


ModelSnapshot - é o arquivo que gerencia como está a base de dados