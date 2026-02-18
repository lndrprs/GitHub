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
  <summary><b> 1. Tópicos </b></summary>
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
 > - Obs.: Master Branch e Main Branch é a mesma coisa. "main branch" é o padrão do GitHub. 
 >
 > - Commandos 

```
# Editar e Comitar 
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

</br>
</div>
</details>

----
