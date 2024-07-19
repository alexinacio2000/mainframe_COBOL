# Criando um mainframe COBOL <img src="https://static-00.iconduck.com/assets.00/file-type-cobol-icon-2048x1753-5yvlgc33.png" alt="Logo COBOL" width="100" height="100" style="vertical-align: middle; margin-top: 10px;">

## Contextualizando

# O que é um mainframe
Um mainframe COBOL é um sistema de computação de grande porte que usa a linguagem de programação COBOL (Common Business-Oriented Language) para desenvolver e gerenciar aplicações. Mainframes são conhecidos por sua robustez, capacidade de processamento em larga escala e alta disponibilidade, frequentemente utilizados por grandes instituições, como bancos e empresas de seguros, para gerenciar grandes volumes de transações e dados.<br>
<b>Resumidamente:</b> são computadores de alta performance projetados para lidar com grandes volumes de dados e executar milhares de processos simultaneamente. Eles têm grande capacidade de processamento, memória e armazenamento e são amplamente utilizados para tarefas críticas como processamento de transações financeiras, gerenciamento de bases de dados de grandes dimensões e execução de aplicações empresariais complexas.<br>

# Cobol
COBOL é uma linguagem de programação desenvolvida nos anos 1950, projetada especificamente para aplicações empresariais, financeiras e administrativas. É conhecida por sua legibilidade e estrutura orientada a dados.Sendo eficaz para manipulação de grandes volumes de dados e relatórios detalhados. Ela suporta operações de entrada e saída, manipulação de arquivos e controle de dados, sendo adequada para ambientes corporativos.

# Idealização de projeto
Minha jornada no mundo dos mainframes e COBOL começou com uma curiosidade sobre esses sistemas robustos, amplamente utilizados por grandes instituições financeiras. No entanto, a verdadeira fonte de inspiração para o meu projeto é uma ideia ousada: criar um sistema mainframe COBOL para simular uma crise global provocada por uma pandemia zumbi! <img src="https://images.emojiterra.com/google/noto-emoji/unicode-15.1/color/svg/1f9df.svg" alt="Zombie" style="width: 50px; height: 20px;">

Este projeto vai explorar um ecossistema dinâmico composto por quatro países interconectados, cada um lidando com requisições diárias e desafios complexos de criptografia. Através dessa simulação, busco não apenas entender as intricadas operações de um mainframe COBOL, mas também testar a resiliência e a segurança de sistemas em um cenário de alta tensão. Prepare-se para uma jornada épica no mundo da tecnologia e da ficção!

# Instalação

Agora irei ensinar um passo a passo para se criar um mainframe cobol.

1 - Baixar tk4.
[[tk4](tk4-_v1.00_current.zip)](https://drive.google.com/file/d/17hvKRkBXBsumZW356iOT0QjspcofPTUF/view)

2 - Baixar TN3270
[Download ZOC8 (Windows, 64 bit)](https://www.emtec.com/common/downloadfile.html?what=ZOC8%20(Windows,%2064%20bit)&link=zoc/zoc8034_x64.exe&ext=html&actual=1)


3- Crie uma pasta no diretório C com o nome TK4

4 - Descompacte o arquivo tk4 na pasta criada no diretório

## Configuração no ambiente windows
    Abra o CMD na pasta do diretório após descmpactar o arquivo ZIP.
    Digite e execute nessa ordem.
    -> cd unattended
    ->cd set_console_mode.bat
---
    Agora volte para o diretório é va para a pasta conf e faça as seguintes alterações
    Localize o parâmetro NUMCPU e altere o valor do parâmetro de "1" para "2" - Resultado final: NUMCPU ${NUMCPU:=2}
    Localize o parâmetro MAXCPU e altere o valor do parâmetro de "1" para "2" - Resultado final: MAXCPU ${MAXCPU:=2}
    Localize o parâmetro CNSLPORT e veja a porta TCP/IP da comunicação CNSLPORT ${CNSLPORT:=3270}
    Localize o parâmetro HTTPPORT e veja a porta TCP/IP da comunicação HTTP PORT ${HTTPPORT:=8038}

---
# Inicializando a conexão
Entre no diretório C/tk4 e abra o cmd e execute o script mvs.bat.
obs: enquanto estiver usando o sistema, não feche esse cmd.

# Usando o TN3270 e configurando acesso
 1. Veja seu endereço ip
 2. Crie uma conexão no TN3270 para o seu IP e a porta 3270 e conecte;

# Agora faça login quando acessar o terminal
Segundo a documentação oficial essas são os logins e senhas de acesso.

HERC01 é um usuário totalmente autorizado com acesso completo às tabelas de usuários e perfis RAKF. A senha de login é CUL8TR.<br>
HERC02 é um usuário totalmente autorizado sem acesso às tabelas de usuários e perfis RAKF. A senha de login é CUL8TR.<br>
HERC03 é um usuário comum. A senha de login é PASS4U.<br>
HERC04 é um usuário comum. A senha de login é PASS4U.<br>
IBMUSER é um usuário totalmente autorizado sem acesso às tabelas de usuários e perfis RAKF. A senha de login é IBMPASS. Esta conta é destinada apenas para fins de recuperação.

# Menção
Nessa trilha de estudo aprendi esse conteúdo assistindo as aulas do brilhante professor @ANDRE COSTA do canal Aprenda Cobol [![Aprenda Cobol](https://media.licdn.com/dms/image/C4D03AQGA_s_FVM8u4Q/profile-displayphoto-shrink_200_200/0/1610480798405?e=1726704000&v=beta&t=woBsjyFLvEncZyIuAE13mhjV2F_mt1ZhPz7Wu_IWJkI)]([[URL-do-Link](https://www.youtube.com/@AprendaCOBOL)](https://www.youtube.com/@AprendaCOBOL))
