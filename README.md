# PyQt5-and-QtDesigner
Pequeno repositório com códigos de teste de uma breve introdução ao PyQt e ao Qt Designer, apenas para saber melhor o que é, como funciona e alguns dos recursos que oferece.
<h3>Instalação via linha de comando com o pip:</h3>
	Abra o prompt de comando e instale os seguintes pacotes:
		C:\> pip install PyQt5
		C:\> pip install pyqt5-tools

	OBS: Caso tenha mais de uma versão do Python instaladas simultaneamente, que foi o meu caso, recomendo instalar manualmente, os passos estão descritos abaixo.
		
<h3>Link para baixar os pacotes para a instalação manual:</h3>
	https://pypi.python.org/pypi/PyQt5
	https://pypi.python.org/pypi/pyqt5-tools
	
<b>Os pacotes estão na extensão .whl, para instalar, navegue até o diretório onde o Python esta instalado em seu pc, copie os arquivos baixados para o diretório principal, abra um prompt de comando dentro da pasta onde copiou e use o seguinte comando:</b>
	py -version -m pip install nome_do_pacote
	Exemplo: C:\Python36-32> py -3.6 -m pip nome_completo_do_pacote.whl
	
<b>O Qt Designer vai estar instalado dentro de uma das pastas dos pacotes instalados, para localiza lo, siga até onde o Python esta instalado, navegue até "Lib\site-packages\", procure as pastas PyQt5 e pyqt5-tools, procure por designer.exe e crie um atalho para onde desejar.</b>
 
<h3>Converter de .ui para .py</h3>
No PyQt5, é utilizado o uic para a conversão(Pelo menos na versão do que instalei), para facilitar o processo e para que seja possível executado de qualquer diretório, faça o seguinte:
	Dentro do diretório onde o Python esta instalado, navegue novamente até "Lib\site-packages\", e os diretórios PyQt5 e pyqt5-tools, verifique em qual das duas o "uic.exe" esta, apos localizado, copie o caminho da pasta ( Exemplo: C:\Python36-32\Lib\site-packages\pyqt5-tools), abra "Meu computador > propriedades > Configurações avançadas do sistema > Variáveis de Ambiente" e procure a variável PATH, vá em Editar e siga as instruções de acordo com o sistema utilizado.
		Para Windows 7, apos clicar em Editar, vá com o cursor até o final do que já estiver, coloque ; que serve como separador e cole C:\Python36-32\Lib\site-packages\pyqt5-tools. OBS: Muito cuidado para não apagar o que já estiver lá. 
		Para Windows 10, só clicar em novo e adicionar o caminho.
		
	*Teste dando o seguinte comando: uic --version no prompt de comando, se estiver tudo configurado corretamente, vai exibir a versão.
		
Apos estar configurado, abra o prompt de comando na pasta onde estiverem os arquivos .ui a serem convertidos e digite o seguinte comando.
	uic input.ui -o output.py
	Exemplo: C:\main> uic nome_layout.ui -o nome_que_desejar.py