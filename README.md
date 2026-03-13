<div align="Center"> 
<br>

<h4>

░██████╗░██╗████████╗██╗░░██╗██╗░░░██╗██████╗░
██╔════╝░██║╚══██╔══╝██║░░██║██║░░░██║██╔══██╗
██║░░██╗░██║░░░██║░░░███████║██║░░░██║██████╦╝
██║░░╚██╗██║░░░██║░░░██╔══██║██║░░░██║██╔══██╗
╚██████╔╝██║░░░██║░░░██║░░██║╚██████╔╝██████╦╝
░╚═════╝░╚═╝░░░╚═╝░░░╚═╝░░╚═╝░╚═════╝░╚═════╝░
</div>

----

<details>
  <summary><b> 1. GitHub </b></summary>
<div align="Left">  
<br>  

G1.1 - Git e GitHub
 > - Git é um VCS (Version Control System), gratuito e open-source;
 > - Frequentemente é usado em conjunto com serviços de repositórios remotos: GitHub, GitLab e Bitbucket.
 >   - Repositórios Remotos ofertam algumas funções a mais, como gerenciamento de tarefas, etc. 
 > - Git e GitHub possuem três características chaves: 
 >   - Controle de Versionamento;
 >   - Codificação Colaborativa;
 >   - Gerenciamento de Tarefas e Automação. 
 >
 > - Existem dois tipos de Repositórios:
 >   - Local - Instalado na máquina local;
 >   - Remoto - GitHub.
 >
 > - Commit | Cometer
 >   - Commit cria um Snapshot para registrar o status do código no repositório;
 >   - Apenas arquivos cometidos são registrados no Log do Git;
 >   - Arquivos cometidos possuem essas informações:
 >     - Hash do Commit;
 >     - Informação do Autor;
 >     - Data e Hora; 
 >     - Mensagem de Commit. 
 >   - O processo de enviar os arquivos ao repositório remoto se chama "Push" / "Empurrar";
 >   - O processo de baixar os arquivos ao repositório local se chama "Pull" / "Puxar". 
 >
 > - Branch | Ramo
 >   - Linha independente de desenvolvimento, com histórico de Commits;
 >   - Ramificações permitem gerenciar versões diferentes do mesmo projeto;
 >   - Por padrão, Git fornece o "Master Branch" como padrão;
 >     - Normalmente, um ramo para uma nova função se chama "Topic Branch";
 >     - Quando o desenvolvimento está completo no Topic Branch, é possível fundir com a Master Branch;
 >   - A ideia de ramificações permite desenvolver recursos simultaneamente. 
 > - Obs.: Master Branch e Main Branch são a mesma coisa. "main branch" é o padrão do GitHub. 
 >
 > - Commandos 

```
# Editar e Comitar
git init - Cria um repositório local 
git add - Adiciona alterações para a área de Stage
git status - Estado atual do repositório
git commit - Commit das alterações que estão no Stage
git log - Histórico de Commits (Autor, Data, Hash e Mensagem)
git diff - Diferenças entre Stage e último Commit
git restore - Restaura arquivos para a versão do último Commit
git rm - Remove arquivos do Projeto
git reset - Desfaz alterações de Commit ou Remove arquivos da área de stage

# Trabalhando com Ramificações
git branch - Lista, Cria ou Deleta Branches
git checkout - Troca de Branch ou Restaura Arquivos (Comando antigo, hoje se usa mais switch e restore)
git switch - Trocar ou criar Branches
git merge - Unificação de Branches
git rebase - Reaplica commits de uma Branch sobre outra
git stash - Guarda alterações não comitadas 

# Colaboração Remota
git remote - Gerencia repositórios remotos
git push - Envia commits locais para o repositório remoto
git pull - Baixa alterações do repositório e aplica merge automaticamente 
git fetch - Baixa alterações do repositório remoto sem aplicar merge  

```
 >- Arquitetura de Três Níveis
 >   - Git usa a arquitetura de três níveis:
 >     - Working Directory: Edição dos arquivos em desenvolvimento;
 >     - Staging Area: Area de preparação para comitar;
 >     - Local Repository: Armazenamento nos arquivos comitados. 
 > 
 > - Head e Index 
 >   - O último commit se chama HEAD;
 >   - A área de preparação (staging), se chama Index. 

</br>
</div>
</details>

----

<details>
  <summary><b> 2. GitHub Advanced Security (GHAS) </b></summary>
<div align="Left">  
<br>  

G2.1 - GitHub Advanced Security (GHAS) 
 > - Solução para segurança de aplicação;
 >   - Inclui capacidades ofertadas em dois produtos distintos:
 >     - GitHub Secret Protection; 
 >     - GitHub Code Security. 
 > - Advanced Security é integrado no fluxo de trabalho, prevenindo vulnerabilidades e vazamento de credenciais; 
 > - Existem 3 características do GHAS - que são ativados na aba "Security": 
 >   - Secret Scanning;
 >   - Code Scanning;
 >   - Dependabot. 

G2.2 - Secret Scanning 
 > - Identifica e ajuda a prevenir exposição acidental de informações sensíveis - como Chaves de API e Tokens, dentro do código; 
 > - Disponível para todos os repositórios públicos, de forma gratuita;
 > - Para repositórios privados, precisa ter uma licença GHAS. 
 >
 > - Procura por padrões predefinidos e sinais indicativos de informações sensíveis;
 > - Por padrão, os padrões são providenciados por um GitHub Partner, mas é possível criar padrões customizáveis. 
 >
 > - Secret Scanning inclui:
 >   - Push Protection: Previne vazamento de segredos escaneando o código no commit, e bloqueando o push;
 >   - Visão de alertas e remediações sem precisar sair do GitHub. 
 >

G2.3 - Code Scanning 
 > - Analiza o código por vulnerabilidades e erros; 
 >   - Usa SAT (Static Analysis Techniques), para vulnerabilidades como SQL Injection, SSX e Buffer Overflows; 
 >   - Providencia feedback automatizado diretamente no fluxo de Pull Request;
 >   - Pode também detectar vulnerabilidades que já existem em Produção. 

G2.4 - Dependabot 
 > - Ferramenta de Gerenciamento Automatizado de Dependências;
 >   - Mantém as dependências sempre atualizadas;
 >   - Verifica regularmente atualizações em bibliotecas e frameworks usados no projeto;
 >   - Além disso, também abre Pull Requests automaticamente, atualizando dependências e mantendo a segurança delas.
 >
 > - Dependabot possui:
 >   - Alertas para vulnerabilidades conhecidas;
 >   - Atualizações de segurança para pacotes vulneráveis;
 >   - Atualizações de versão, para manter as dependênciais atuais. 
 >
 > - Dependabot trabalha junto com o Dependency Graph;
 >   - Determinando quais dependências estão em uso, e as referenciar no GitHub Advisory Database para detectar vulnerabilidades. 
 >
 > - Com o GHAS, Dependabot possui Dependency Review;
 >   - Permite prever pacotes vulneráveis no Pull Request, antes do merging. 

G2.5 - Dependency Graph
 > - Identifica todas as dependências de um repositório ou pacote; 
 >   - Permite visualizar as dependências e algumas informações, como vulnerabilidade, no Dependendy Graph para o repositório; 
 >   - Para gerar o gráfico, GitHub analisa as dependências explícitas declaradas no arquivo Manifest e Lock ; 
 >   - Quando ativo, o Dependency Graph automaticamente analisa os pacotes no manifesto, e usa isso para construir o gráfico com os nomes e versões.
 >
 > - Pontos-chave:
 >   - Inclui informação nas dependências diretas e transitivas;
 >   - Automaticamente atualizado, quando commita mudanças ou adiciona manifesto / lock;
 >   - Para ver o gráfico, é só abrir o repositório e ir na aba "Insights";
 >   - Com o acesso de Leitura ao repositório, é possível exportar o gráfico como SPDX. 
 >
 > - É possível usar a API de Submissão de Dependency para analisar manifest ou arquivo lock;
 >
 > - Outras características do GitHub dependem do Dependency Graph, como:
 >   - Dependency Review: Para identificar mudanças em dependências, e entender o impacto na segurança, durante a revisão de PR;
 >   - Dependabot Alerts: Dependabot faz uma referência cruzada nos dados da dependência, com o GitHub Advisory Database;
 >     - O Dependency Graph escaneia as dependências e gera alertas no Dependabot, quando há vulnerabilidade. 
 >   - Dependabot Security Updates: Usa o Dependency Graph e Dependabot Alerts, para ajudar na atualização de dependências com vulnerabilidades. 
 >
 > - Dependabot Version Updates não usa o Dependency Graph, esse depende do Versionamento de Semântica das dependências;
 >   - Version Updates ajuda a manter as dependências atualizadas, mesmo quando não possuem vulnerabilidades. 

G2.6 - GHAS Alerts 
 > - Code Scanning Alerts
 >   - CodeQL Analysis Alerts: Gerado por CodeQL, mecanismo de análise semântica de código;
 >   - Identificam vulnerabilidades de segurança no código (Como SQL Injection, SSX, etc.)
 >
 > - Secret Scanning Alerts
 >   - Exposed Secrets  Alerts: Alertas ativados quando informações sensíveis - como chaves API ou Credenciais -, são identificadas num repositório.
 >
 > - Dependency Alerts 
 >   - Dependabot Alerts: Automaticamente detecta dependências desatualizadas e cria pull requests para atualizá-las para a última / segura versão.
 >
 > - Security Overview Alerts 
 >   - Providencia um dashboard resumindo o estado de segurando de um repositório.   
 >
 > - Third Party Alerts
 >   - Possibilidade de integrar ferramentas de análise de código no GitHub, fazendo o upload dos arquivos SARIF. 
 >
 > - Access to Alerts
 >   - Code Scanning e Dependabot Alerts: Qualquer um com permissão de Write no repositório;
 >   - Secret Scanning: Apenas Admins do repositório;
 >   - Qualquer pessoa ou time pode ter acesso para ver e modificar os alertas no repositório, ajustando em "Access to Alerts". 

</br>
</div>
</details>

----
