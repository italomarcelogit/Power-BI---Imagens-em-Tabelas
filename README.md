# **Power BI**

## Passo a Passo
* Importar pasta de imagens de vendedores
  - Obter Dados, Pasta, Conectar
  - Insira o local onde estão as imagens e OK
  - Transformar Dados

* Converter Content Binário em imagem
  - Nova Fonte
  - Consulta Nula

<div>=(BinaryContent as binary) as text=></div>
<div>let</div>
  <div>  Base64 = "data:image/jpeg;base64, " & Binary.ToText(BinaryContent, BinaryEncoding.Base64)</div>
<div>in</div>
<div>  Base64</div>


  - Renomear a Consulta1 para **fxBINtoIMG**
  - Clique novamente na tabela vendedores
  - Veja que a primeira coluna chama-se Content, é ela que iremos converter. Então clique em:
    - Adicionar coluna,
    - Invocar função personalizada,
    - Coloque o nome Imagem Convertida
    - Consulte a função **fxBINtoIMG**
    - Selecoine o campo BinaryContent **Content**
    - OK e veja que foi criada uma nova coluna chamada Imagem Convertida
    - Clique na aba Pagina Inicial, em Fechar e Aplicar

* Criando uma tabela com imagens
  - expanda a tabela importada,
  - selecione o campo Imagem Convertida
  - em Categoria de Dados, selecione URL da Imagem
  - adicione o visual tabela, por exemplo
  - e arraste o campo Imagem Convertida

* Utilizando VISUAL Chicet Slicer
  - caso não o tenha, adicione esse visual ao seu PBI
  - Em imagem, arraste o campo Imagem Convertida
  - Em categoria, arraste o campo Nome 

* aqui vai a dica,
**crie uma um campo ta tabela vendedores que se relacione com os seus dados de vendas. Assim, você poderá selecionar nas imagens, tanto em uma tabela, matriz, chiclet slicer, e visualizará o report de forma dinâmica conectada com seus dados**
  
