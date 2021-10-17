comandos que EU (iniciante) mais usei:

abra o terminal: ctrl+shift+` (user linux ou abra o git bash here)

git help - ver comandos (também da pra ver comandos específicos, ex: git help add)

iniciar/encerrar repositorio{
    git init - inicia um repositório

    rm -rf .git - para desfazer o git init
}

adicionar dir/arquivo{
    git add meu_arquivo.txt - adicionar um arquivo específico

    git add meu_diretorio - adicionar um diretório específico

    git add - adicionar todos os arquivos/diretórios
}

commitar{
    git commit meu_arquivo.txt - commitar um arquivo

    git commit meu_arquivo.txt meu_outro_arquivo.txt - commmitar varios arquivos

    git commit meu_arquivo.txt -m "estou adicionando tal função" - commitar com um comentário
}

exibição de histórico{
    git log - exibir o histórico do que foi feito

    git log --stat - exibir histórico completo (quem postou, data...)

    git log --<caminho_arquivo> - histórico de um arqivo específico

    git log --diff-filter=M --<caminho_do_arquivo> - histórico de modificações (
        'M' significa modificado(M) e pode ser substituido por: adicionado(A), copiado(C), apagado(D), renomeado(r) entre outros. 
    )
}

repositorio remoto{
    git remote - exibir repositórios remotos

    git remote add origin git@github.com:Ruan-Gabriel/learn-project.git - vincular um repositório local a um remoto

    git remote rm learn-project - desvincular repositório
}

enviar files/dir para repositiorio remoto{
    git push -u origin master - enviar arquivos para repositorio remoto (no primeiro push deve conter o nome do repositorio remoto e da branch)

    git push - mesma função do anterior (porém, agora não precisa mais especificar o repositorio e nem a branch)
}

atualizar repositório remoto{
    git pull - atualizar os arquivos na branch atual

    git fetch - buscar alterações mas não atualizar
}

clonar repositorio{
    git clone git@github.com:rafaballerini/guitTutorial.git - clonar um repositório ja existente na sua máquina
}

branches{
    O master é o branch principal do git
    o HEAD indica qual é a branch principal

    git branch [nome] branch - criar um novo branch

    git checkout linux_life - trocar para uma branche ja existente (neste caso o HEAD vai estar na branch em uso)

    git checkout -b bug-456 - criar e trocar para esta branch

    git checkout master - voltar para a branch original

    git merge bug-123 - integrando uma branch na outra (neste caso o merge deve ser feito na branch que irá receber as alterações)

    git branch -d bug-123 - apagando branch

    git branch - listando branches

    git branch -v - listando branch com info dos ultimos commits

    git branch --merged - listando branches que ja foram fundidos

    git branch --no-merged - listando branch que não foram fundidos
}

criar/dell repositorios{
    git push origin bug-123 - criar branch no repositorio remoto com o mesmo nome

    git push origin bug-123:new-branch - criar branch no repositorio remoto com nome diferente

    git checkout -b bug-123 origin/bug-123 - baixar branch para edição

    git push origin:bug-123 - apagar branch remoto
}

clonando repositorio{
    git clone <caminho do arquivo>
    cd  <nome da pasta>
    (depois disso, esta pronto para ser usado)
}

algumas soluções para possiveis problemas{
    git remote add origin https://[hostname]/user/[repo].git - para adicionar um repositorio novo
        se já existir entao, tente isso:
    git remote set-url https://user:token@[hostname]/user/[repo].git - serve para alterar o repo já existente.
}