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
 > - Automaticamente escaneia todo o histórico do Git, em todas as branches do repositório;
 >   - Lembrando que o Secret Scanning procura por credenciais de autenticação; 
 >   - O Escâner procura:
 >     - Descrições e Comentários em Issues;
 >     - Títulos, descrições e comentários, em issues abertos ou fechados;
 >     - Títulos, descrições e comentários em PRs; 
 >     - Títulos, descrições e comentários em Discussões. 
 >    - Quando algum segredo é identificado, envia uma notificação a todos os administradores sobre o commit; 
 >    - Para ver o alerta, entrar na aba "Security";
 >    - GitHub também notifica o provedor de serviço, se tiver parceria com o GitHub. 
 > 
 > - Push Protection
 >   - Previne Pushes que contenham segredos detectados no código; 
 >   - Contribuidores são solicitados diretamente no IDE ou CLI para remediar a exposição; 
 >   - Para proceder, contribuidores devem remover o segredo, ou permitir. 
 > - É automaticamente ativo em projetos públicos; 
 > - Para repositórios privados, precisa ser ativado manualmente - e possuir o GHAS. 
 >
 > - Validity Checks 
 >   - Determina se um token ainda é ativo, e quando foi ativo. 
 >
 > - Para evitar que determinados arquivos sejam escaneados, criar um arquivo secret_scanning.yml;
 >   - Nesse arquivo, usar o "paths-ignore". 
 > - O Secret Scanning exclue os primeiros 1.000 diretórios dos escaneamentos, se tiver mais de 1.000 registros; 
 > - Se for maior que 1 MB, vai ignorar o arquivo todo. 
 >
 > - Depois de ativar o Secret Scanning, existem mais configurações para afinar a detecção:
 >   - Validity Check: Verifica se os segredos expostos ainda estão ativos;
 >   - Non-Provider Patterns: Escaneia por formatos fora do padrão;
 >   - Scan for Generic Passwords: IA detecta senhas genéricas ou fracas nos códigos;
 >   - Push Protection: Bloqueia commits contendo tipos de segredos. 
 > - Há outras possibilidades, como:
 >   - Regras de Bypass: Permite que cargos ou times ignorem a proteção;
 >   - Alert Dismissal Rules: Requisita justificativa antes de liberar os alertas;
 >   - Custom Patterns: Definir até 100 padrões customizáveis, para detecção de segredos. 
 >
 > - Existem 4 razões para fechamento de um alerta:
 >   - Revogado;
 >   - Usado em Testes;
 >   - Falso Positivo;
 >   - Não será arrumado. 
 >
 > - Secret Scanning suporta até 500 padrões customizados para cada organização ou empresa; 
 > - Até 100 para repositórios privados. 

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
 >
 > - Dependabot mantém as dependências atualizadas, informando sobre vulnerabilidades nas dependências; 
 >   - Quando um alerta é ativado, automaticamente abre um pR para atualizar as dependências;
 >     - Seja para a próxima versão segura ou para a última versão.
 > 
 > - Alertas são gerados quando: 
 >   - Um novo Advisory é adicionado no GitHub Advisory Database;
 >   - O gráfico de dependência por um repositório, muda.
 >
 > - Arquivos Manifesto e Lock são importantes, precisam ficar atualizados.
 >
 > - Dependabot usa Read-Only Analysis nos repositórios em que é ativado; 
 >   - Precisa ativar tanto o Dependabot, como também o Dependency Graph. 
 > - O Usuário precisa ter permissão de Write, Maintain ou Admin. 
 >
 > - Os alertas do Dependabot possuem:
 >   - Classificação e Pontuação de Severidade; 
 >   - Métricas Base de CVSS; 
 >   - CWE; 
 >   - CVE ID;
 >   - GHSA ID.
 >
 > - Atualizações do Dependabot:
 >   - Security Updates: PRs que ajudam a atualizar dependências inseguras;
 >   - Version Updates: PRs que matém as dependências atualizadas, mesmo sem inseguranças.
 >
 > - Há um arquivo: dependabot.yml, que fica no diretório .github;
 >   - Usuários com permissão de Write, podem permitir o version updates; 
 >   - Esse arquivo possui:
 >     - version: Deve ser a versão 2;
 >     - registries: Opcional - dependência em um registro privado, aqui se colocam as autenticações;
 >     - updates: Inclui uma entrada para cada dependência que o Dependabot monitorará. 
 > - Para cara gerenciador de pacote, há:
 >   - package-ecosystem: identifica o gerenciador de pacote;
 >   - directory: Especifica o local do manifesto ou outros arquivos de definição;
 >   - schedule.interval: Especifica quão frequente se deve verificar por novas versões. 

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
 >
 > - Dependency Graph é um resumo de arquivos Manifest e Lock, armazenados no repositório e em qualquer dependência submetidas ao repositório usando a API de Submissão;
 >   - Esses arquivos contém metadado sobre o projeto;
 >   - O Dependency Graph é automaticamente gerado para repositórios públicos, e incluem:
 >     - Dependencies: Ecosistema e pacotes no qual o repositório depende; 
 >     - Dependents: Repositórios e Pacotes que dependem do repositório. 
 >
 > - Existem dois tipos de Dependências:
 >   - Diretas: Explicitamente definidas nos arquivos Lock e Manifesto, ou submetidas com a API de DS (Dependency Submission)
 >   - Indiretas / Transitivas / Subdependências: Dependências usadas por pacotes que são dependências do projeto. 
 >
 > - Arquivos Lock geram o gráfico de dependência mais confiável;
 >   - Isso porque definem quais versões das dependências diretas e indiretas o projeto usa. 
 >
 > - Para repositórios privados, precisa ativar o gráfico de dependências. 

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

G2.7 - GitHub Advisory Database
 > - Banco de dados de vulnerabilidades de segurança;
 > - Inclusivo de CVE's e Security Advisories do GitHub, do Open Source; 
 > - GitHub coleta informação nas vulnerabilidades, e inclui no Adv. Database:
 >   - Repositório de  Avisos de Segurança Open Source, e gratuito;
 >   - Permite a comunidade colaborar nos avisos;
 >   - Formato padrão aceito pela industria; 
 >
 > - Advisory Database contém informações de cada vulnerabilidade;
 >   - Incluindo Descrição, Severidade, e pacote afetado;
 >   - O banco de dados usa o CVSS - Common Vulnerability Scoring System para atribuir Severidade; 
 >   - Graus de severidade: Low, Medium, High e Critical; 
 > 
 > - O Banco de Dados é populado pelas seguintes fontes:
 >   - Security Advisories Reported on GitHub; 
 >   - National Vulnerability Database;
 >   - NPM Security Advisories Database;
 >   - FriendsOfPHP Database;
 >   - Go Vulncheck Database;
 >   - Python Packaging Advisory Database;
 >   - Ruby Advisory Database;
 >   - RustSec Advisory Database;
 >   - Community Contributions;
 >   - Combination of Machine Learning and Human Reviews in Public Commit on GitHub. 

G2.8 - Software Bill of Materials (SBOM)
 > - Inventório de dependências de um projeto e informações associadas, como:
 >   - Versão, identificadores de pacote, e licenças;
 > - SBOMs ajuda a reduzir os riscos de Supply Chain, por:
 >   - Prover transparência sobre dependências usadas no repositório;
 >   - Identificar vulnerabilidades antecipadamente;
 >   - Prover percepções sobre qualidade, segurança e compliance; 
 >   - Ajuda em cumprir padrões de proteção de dados.
 >
 > - GitHub fornece duas formas de exportar o SBOM para o repositório:
 >   - GitHub UI;
 >   - REST API;
 > - Também é possível exportar o gráfico de dependências como SBOM, usando o SPDX: Software Package Data Exchange 

G2.9 - Dependency Review
 > - Verificação de Vulnerabilidades em Dependências antes de serem adicionados na main branch; 
 > - Ajuda a entender mudanças na dependência, e o impacto na segurança, dessas mudanças; 
 > - Fácil visualização das diferenças em "Files Changed", no PR;
 > - Informa sobre: 
 >   - Dependências adicionadas, removidas ou atualizadas; 
 >   - Número de projetos que usam esses componentes;
 >   - Dados das vulnerabilidades dessas dependências. 
 > - A diferença entre o Review e o Bot, é que o Bot é automaticamente, e o Review é no PR.

G2.10 - GraphQL Explorer 
 > - Ferramenta recomendada para se comunicar com o GraphQL API; 
 > - É um IDE interativo e gráfico, de GraphQL.   


https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/

</br>
</div>
</details>

----
