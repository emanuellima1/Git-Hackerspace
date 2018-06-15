# Começando com o Git (resumo)

## Inicializando um repositório:
1. Você pode transformar um diretório local em um repositório Git, ou
2. Você pode clonar um repositório Git existente.

> $ cd /home/user/my_project  
> $ git init  

> $ git clone https://github.com/emanuellima1/hello-world  

Agora você tem uma *working copy* dos arquivos. Você pode modificá-los à vontade.  

Os arquivos podem estar *tracked* ou *untracked*. Um arquivo *tracked* está sendo monitorado por mudanças pelo Git. 

## Verificando o status:  
> $ git status  

Verifica o estado de cada arquivo.  

## Monitorando novos arquivos:
> $ git add [arquivo]  

## Pondo no staging:
> $ git add [arquivo]   

## Arquivos a serem ignorados:
> [editor] .gitignore  

> An asterisk (*) matches zero or more characters; [abc] matches any character inside the brackets (in this case a, b, or c); a question mark (?) matches a single character; and brackets enclosing characters separated by a hyphen ([0-9]) matches any character between them (in this case 0 through 9). You can also use two asterisks to match nested directories; a/**/z would match a/z, a/b/z, a/b/c/z, and so on.  

## Vendo mudanças:
> $ git diff  

> git diff --staged  

## Commitando:
> $ git commit  

> $ git commit -m "[bla]"   

## Deletando arquivos:
> $ git rm [arquivo]  

## Renomeando arquivos:
> $ git mv [arquivo_antigo] [arquivo_novo]  

## Histórico de commits:
> $ git log [--reverse] [--pretty=short/full/fuller/oneline] [--graph] [-p] [-2] [arquivo]  

## Desfazendo coisas:
> $ git commit --amend  
Refaz um commit com pequenas mudanças  

> $ git reset HEAD [arquivo]  
Unstage um arquivo  

> $ git checkout -- [arquivo]  
Descarta mudanças num arquivo

## Mostrando repositórios remotos:
> $ git remote [-v]    
origin é o servidor de onde veio o repositório

> $ git remote add [nome] [url]  
Adiciona um repositorio remoto  

## Mais ações com o repositório remoto:
> $ git fetch [repo_remoto]  
Baixa o repositório, mas não faz merge automático  

> $ git pull [repo_remoto]  
Baixa o repositório e faz merge automático   

> $ git push [repo_remoto] [branch_do_remoto]  
Upload do meu repo para o remoto  

> $ git remote show [repo_remoto]  
Infos do repositório remoto  

> $ git remote rename [nome_antigo] [nome_novo]  
Renomeia o repositório remoto  

> $ git remote rm [nome_repo]  
Remove um repositório remoto  

## Tags:
> $ git tag -l ["regex"]  
Lista as tags  

> $ git tag -a [nome_tag] [commit_checksum] -m ["mensagem_tag"]  
Tag anotada  

> $ git show [nome_tag]  
Mostra informações da tag  

> $ git push origin [tag_name]  
Manda uma tag para o repositório remoto  

> $ git push origin --tags  
Manda todas as tags para o repositório remoto   
