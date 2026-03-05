  <!-- 1º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/1.png"
       width="80"
       style="margin-right: 30px;">
<strong>Qual é a versão e o ano da máquina Windows?</strong> <br><br>
Para descobrir a versão e o ano da máquina Windows, abri o menu <code>iniciar</code> e digitei <code>winver</code>, que é um comando que apresenta informações detalhadas sobre o sistema operativo.<br>
Ao executá-lo, surge uma janela que indica a versão exata do Windows e o ano da atualização instalada.<br>
Esta ferramenta é útil porque fornece dados oficiais do próprio sistema, sem necessidade de recorrer a software externo.
 
  <!-- 2º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/2.png"
       width="80"
       style="margin-right: 30px;">
<strong>Qual utilizador logou por último?</strong> <br><br>
Para identificar o último utilizador que iniciou sessão, utilizei o Visualizador de Eventos <code>Event Viewer</code> do Windows, acedendo aos <code>Registos de Segurança</code>.<br>
Depois, organizei os eventos por data para encontrar os inícios de sessão mais recentes.<br> 
Ao analisar o separador de detalhes de cada evento, consegui determinar qual utilizador realizou o último login no sistema.<br>
Esta abordagem é confiável porque regista todas as sessões do sistema.

 <!-- 3º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/3.png"
       width="80"
       style="margin-right: 30px;">
<strong>Quando John entrou no sistema pela última vez?</strong> <br><br>
Para descobrir a última vez que o utilizador John iniciou sessão, abri a linha de comandos <code>CMD</code> e utilizei o comando:<br>
<code>net user john</code>.<br> 
O resultado mostra várias informações sobre a conta, incluindo a linha <code>Last logon</code>, que indica a data e hora do último login.<br> 
Este método permite obter rapidamente dados precisos diretamente do sistema.

  <!-- 4º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/4.png"
       width="80"
       style="margin-right: 30px;">
<strong>A qual IP o sistema se conecta quando é iniciado?</strong> <br><br>
Primeiro, analisei o ficheiro <code>hosts</code>, mas não encontrei informação relevante.<br>
Depois, abri o <code>regedit</code> através de Executar <code>run</code> e fui até:<br>
<code>HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Run</code><br>
Neste caminho, encontrei os programas configurados para iniciar com o Windows e os endereços IP associados, permitindo identificar a ligação que ocorre automaticamente quando o sistema arranca.

<!-- 5º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/5.png"
       width="80"
       style="margin-right: 30px;">
<strong> Quais duas contas tiveram privilégios administrativos (exceto o utilizador Administrador)?</strong> <br><br>
Para obter esta informação, utilizei a linha de comandos <code>CMD</code> e executei o comando:<br>
<code>net localgroup Administradores</code><br>
Este comando lista todas as contas que pertencem ao grupo de administradores locais. A partir da lista, é possível identificar quais utilizadores têm privilégios administrativos além do utilizador Administrador.

  <!-- 6º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/6.png"
       width="80"
       style="margin-right: 30px;">
<strong> Qual é o nome da tarefa agendada que é mal-intencionada?</strong> <br><br>
Para identificar a tarefa agendada mal-intencionada, utilizei o <code>PowerShell </code>e executei o comando:<br>
<code><br>Get-ScheduledTask.</code><br>
Este comando permite listar todas as tarefas agendadas no sistema.
Depois de obter a lista, analisei quais tarefas não pertenciam ao funcionamento normal do Windows.<br>
As tarefas suspeitas foram então investigadas individualmente, tendo em conta o nome, a ação executada e a sua finalidade.

<!-- 7º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/7.png"
       width="80"
       style="margin-right: 30px;">
<strong> Qual ficheiro a tarefa estava a tentar executar diariamente?</strong> <br><br>
Para descobrir qual o ficheiro executado diariamente, abri o <code>Task Scheduler</code> e fui até: <br>
→ <code> Task Scheduler Library</code>.<br>
De seguida, analisei cada tarefa e observei o campo <code>Action</code>, que indica qual o programa ou script que é executado.<br>
Ao comparar as ações das tarefas existentes, foi possível identificar qual delas executava um ficheiro fora do comportamento normal do sistema e, assim, determinar qual era o ficheiro executado diariamente.

<!-- 8º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/8.png"
       width="80"
       style="margin-right: 30px;">
<strong> Em que porta este ficheiro estava a ouvir localmente?</strong> <br><br>
Para identificar a porta utilizada pelo ficheiro, voltei a analisar a informação presente no campo <code>Action</code> da tarefa identificada anteriormente.<br>
A partir dos parâmetros do comando ou do script indicado nessa ação, foi possível perceber em que porta o ficheiro estava configurado para escutar localmente.

<!-- 9º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/9.png"
       width="80"
       style="margin-right: 30px;">
<strong> Quando é que a Jenny fez o último logon?</strong> <br><br>
Para obter esta informação, utilizei o <code>PowerShell</code> e executei o comando:<br>
<code>net user jenny</code><br>
Este comando apresenta informações detalhadas sobre a conta especificada, incluindo a data e hora do último início de sessão, permitindo responder diretamente a esta questão.

  <!-- 10º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/10.png"
       width="80"
       style="margin-right: 30px;">
<strong> Em que data se realizou a invasão?</strong> <br><br>
Dentro de <code>Task Scheduler</code> em:<code>Task Scheduler Library</code> analisei novamente as tarefas suspeitas identificadas anteriormente.<br>
Uma dessas tarefas estava configurada para abrir o <code>PowerShell</code> e exportar informação para um ficheiro TXT.<br>
No separador <code>Triggers</code>, é possível ver a data e hora em que essa tarefa foi configurada para ser executada, o que permite determinar a data da invasão.

<!-- 11º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/11.png"
       width="80"
       style="margin-right: 30px;">
<strong> Em que momento o Windows atribuiu pela primeira vez privilégios especiais a um novo logon?</strong> <br><br>
Para responder a esta questão, utilizei o <code>Event Viewer</code> e apliquei um filtro pelo <code>ID de evento 4672</code>, 
que corresponde a logins com privilégios elevados (por exemplo, administrador).<br>
Como existem muitos registos, ordenei os resultados por data, do mais antigo para o mais recente.<br>
Depois, observei a secção <code>General</code> de cada evento e procurei a mensagem:<br>
<code>“Special privileges assigned to new logon”</code><br>
Por fim, utilizei a dica da pergunta <code>*Question Hint*</code> para garantir que o formato da data e hora correspondia ao exigido.

  <!-- 12º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/12.png"
       width="80"
       style="margin-right: 30px;">
<strong> Que ferramenta foi usada para obter palavras-passe do Windows?</strong> <br><br>
Comecei por analisar os ficheiros presentes no disco <code>C:</code>, em especial a pasta <code>Temp(TMP)</code>.<br>
Durante essa análise, encontrei um ficheiro suspeito chamado <code>mim-out</code>.<br> 
Ao inspecionar o seu conteúdo, verifiquei que estava associado ao ficheiro <code>mimikatz 2.0 alpha</code>.<br>
Com uma breve pesquisa sobre este nome, foi possível confirmar que se trata de uma ferramenta conhecida por explorar 
a segurança do Windows e extrair credenciais de autenticação.<br> 
Assim, a partir da análise do ficheiro e da sua origem, foi possível identificar a ferramenta utilizada.
  
<!-- 13º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/13.png"
       width="80"
       style="margin-right: 30px;">
<strong> Qual foi o IP de controlo externo e servidor de comando do invasor?</strong> <br><br>
Para obter esta informação, comecei por analisar o ficheiro <code>hosts</code>, localizado em:<br>
<code>C:\Windows\System32\drivers\etc\hosts</code>.<br>
Nesse ficheiro, é necessário observar as entradas que não correspondem às configurações normais do sistema, 
nomeadamente associadas a serviços legítimos conhecidos.

  <!-- 14º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/14.png"
       width="80"
       style="margin-right: 30px;">
<strong> Qual foi a extensão do shell carregado através do site do servidor?</strong> <br><br>
Como a questão refere-se ao servidor ao qual está ligado por RDP, considerei que o shell web teria de estar numa pasta acessível pelo servidor web.<br>
Por esse motivo, fui até:
<code>C:\inetpub\wwwroot</code><br>
Esta pasta contém os ficheiros que o servidor web disponibiliza.<br>
Ao observar os ficheiros presentes nesse directório, foi possível identificar a extensão do ficheiro utilizado como shell.<br>
A extensão do shell carregada pelo atacante é aquela que serve para criar páginas web dinâmicas e interativas, 
permitindo a incorporação de código Java diretamente dentro de arquivos HTML.

<!-- 15º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/15.png"
       width="80"
       style="margin-right: 30px;">
<strong> Qual foi a última porta que o atacante abriu?</strong> <br><br>
A dica da pergunta <code>*Question Hint*</code> indicava que a resposta estava relacionada com a <code>Firewall</code>.<br>
Por isso, abri o <code>Windows Firewall with Advanced Security</code> e acedi a:<br>
<code>Inbound Rules</code><br>
Nesta secção, encontram-se todas as regras que permitem ligações externas ao sistema.
Ao analisar as regras existentes, identifiquei uma regra recentemente criada, marcada como suspeita, 
que indicava explicitamente a porta aberta para permitir acesso remoto à máquina.<br>
Assim, foi possível determinar a última porta aberta pelo atacante.

<!-- 16º pergunta e resposta -->
<p style="margin: 0 0 14px 0; font-size: 12px; font-weight: normal; display: flex; align-items: center;">
  <img src="https://github.com/ClauPereira/Icons/raw/main/InvestWindows/16.png"
       width="80"
       style="margin-right: 30px;">
<strong> Verifique se existe envenenamento de DNS: que site foi redirecionado?</strong> <br><br>
Esta resposta está relacionada com a análise feita anteriormente à questão sobre o IP de controlo externo (13º questão).<br>
Voltei a consultar o ficheiro <code>hosts</code>, em:<br>
<code>C:\Windows\System32\drivers\etc\hosts</code><br>
Nesse ficheiro, foi possível confirmar a existência de entradas alteradas que redirecionavam um domínio legítimo para um endereço IP malicioso.<br>
Através dessa verificação, foi possível identificar qual o site que foi afetado pelo envenenamento de DNS.

