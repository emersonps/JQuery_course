# CursoJQuery
Curso básico de JQuery<br>
<br>
http://jquery.com/download/<br>

Modo de Download do JQuery:<br>
Baixar direto para o computador;<br>
Usar uma CDN:<br>
  Google CDN<br>
  Microsoft CDN<br>
  CDNJS CDN<br>
  jsDelivr CDN<br>

<strong>Instalando o JQuery</strong><br>
<br>
1. Google CND: <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script> <br>
Copia e cola no cabeçalho do site <br>
  Obs: o sistema só irá funcionar de houver uma conexão com a internet.<br>

2. Baixando o arquivo:<br>
  2.1 No site clique no link: Download the compressed, production jQuery 3.3.1<br>
  2.2 Ao exibir os comando na página web, pressiona CTRL+S e salva na paste do projeto (JS).<br>
  2.3 No cabeçalho do site digite a seguinte linha:<br>
      <script src="js/jquery-3.3.1.min.js"></script><br>
  Obs.: Nesse caso, toda vez que o o JQuery fir atualizado, essa linha terá que ser atualizada manualmente.<br>
3. Baixando e renomeando:<br>
  Para evitar problemas com acesso ou atualização, basta renomear e deixar apenas como mostra abaixo:<br>
      3.1 Copiar e colar o arquivo: jquery-3.3.1.min.js;<br>
      3.2 Renomear o arquivo: jquery.js no diretório e no cabeçalho do site:<br>
      <script type="text/javascript" src="js/jquery.js"></script><br>
<br>
Notas Finais: Tente trabalhar usando apenas uma das 3 opções.<br>
<br>
<strong>Métodos de Inicialização e Carregamento</strong><br>
   DOM (document object Model) - São objetos carregados. <br>
<br>   
   <script type="text/javascript"><br>
	$(document).ready(function(){<br>
		alert('DOM Carregado!!! - Executa antes mesmo dos elementos serem carregados');<br>
	});<br>
<br>
	$(window).load(function(){<br>
		alert('Elementos Carregados!!! - Executa quando todos os elementos forem carregados!!!');<br>
	});<br>
    </script><br>

Obs.: Abaixo está o método resumido do primeiro exemplo anterior:<br>
$(function(){<br>
  //scripts<br>
})<br>


<strong>AULA 2</strong>	<br>
Pra trabalhar com JQuery, preciamos ter uma base de seleção. Vamos aplicar de uma forma simples, diferentes soluições para o problema a seguir: Fazer a seleção de um elemento, seja ele uma classe ou tag:<br>
<strong>1. Selector: <br></strong>
$("") <br>
ou:<br>
$('')<br>
<br>
Exemplo:<br>
$(document).ready(function)(){<br>
   $('h1');<br>
});<br>
<br>
Nota: Quando fazemos isso estamos usando o método de encapsulamento, ou seja, estamos pegando o DOM desse H1 e passando pra ele todas as funções nativas do JQuery.<br>
<br>
<strong>2. Atribuíndo uma função ou interação ao Seletor ou item selecionado:<br></strong>
$(''). <br>
Usamos o ponto após a aspas, no fim do seletor.<br>
<br>
Exemplo:<br>
$('h1').css("color","#f66");<br>
$('h1').css("color","#f66");<br>
<br>
Aplicando Funções nativas do JQuery<br>
$('h1').hide();<br>
$('h1').delay('1000');<br>
$('h1').fadeIn("slow");<br>
$('h1').text('Curso JQuery');<br>
<br>
<strong>3. Desencadeando as funções em apenas uma linha de comando:<br></strong>
Basta separar as funções por ponto:<br>
<br>
$('h1').css("color","#f66").hide().delay('1000').fadeIn("slow").text('Curso JQuery');<br>
<br>
<strong>4. Desencadeando as funções em bloco (indicado para melhor revisar o código:<br></strong>
<br>
$('h1')<br>
	.css("color","#f66")<br>
	.hide()<br>
	.delay('1000')<br>
	.fadeIn("slow")<br>
	.text('Curso JQuery');<br>
<br>
<strong>5. Colocando uma função dentro da função principal:<br></strong>
<br>
$(document).ready(function(){<br>
$('h1')<br>
&nbsp&nbsp.click(function(){<br>
<br>
});<br>
});<br>
<br>
Exemplo:<br>
<strong>Criaremos uma função para quando clicarmos no H1 ele mude a cor do Body:</strong><br>
<br>
$('h1')<br>
.click(function(){<br>
	$('body').css("background","#c30");<br>
});<br>
<br>
<strong>Mais exemplos:</strong><br>
.click(function(){<br>
	$('body').css("background","#c30")<br>
	$('h1').css("color","#fff")<br>
	$('h1').text("Emerson");<br>
});<br>
<br>
<strong>6. Colocando Várias Instruções CSS numa função:</strong><br>
Exemplo:<br>
$('a').css({color: "red', display:"block"});<br>
<br>
<strong>7. Atribuíndo uma Função Jquery a uma classe ou Id:</strong><br>
$('.nomeDaClasse);<br>
$('#nomeDaClasse);<br>
<br>
Exemplo:<br>
$('.link2').css("color","green")<br>
$('#link3').css("color","black");<br>
<br>
<strong>8. Atacando todos os Elementos da Página:</strong><br>
Exemplo para resetar o margin e o padding da página:<br>
<br>
$('*')<br>
.css("margin","0");<br>
.css("padding","0");<br>
<br>
$('*')<br>
.css({margin:"0",padding:"10"});<br>
<br>
<strong>8. Selecionar mais de um Elemento:</strong><br>
$('h1, #link3').css("border-bottom","solid 3px blue");<br>
<br>

      
      
     

