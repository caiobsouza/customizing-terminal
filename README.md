# Configurando o Terminal no MacOS

O Terminal do Mac OS funciona, mas poderia ser melhor. Esse guia rápido pode te ajudar a melhorar essa experiência.

## iTerm2

O iTerm2 é uma alternativa ao terminal nativo do MacOS. É o primeiro passo para ter uma boa experiência de linha de comando no Mac.
https://iterm2.com/

## Homebrew

O [Homebrew](https://brew.sh/) é um gerenciador de pacotes para o MacOS (como o `apt-get` do Linux). É bastante útil para instalar diversas ferramentas, CLI, etc e muitos tutoriais acabam utilizando o `brew`. Nós vamos utilizar-lo para instalar o **Zsh**

## Zsh (Z Shell)

O [Zsh](http://zsh.sourceforge.net/) é um shell projetado para uso interativo, embora também seja uma linguagem de script poderosa. Suporta todas as features do `bash` e implementa novas funções. 
Para instalar o Zsh vamos utilizar o **Homebrew**.

    brew install zsh

## Oh-My-Zsh

O [Oh-My-Zsh](https://github.com/ohmyzsh/ohmyzsh) é um framework open-source para gerenciamento da configuração do Zsh. De cara, já inclui 300+ plugins que ajudam (e muito) o dia-a-dia de desenvolvimento.
A instalação do **oh-my-zsh** é feita diretamente via script no terminal:

    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

No GitHub do **oh-my-zsh** há mais informações de [como configurar Zsh e gerenciar os plugins.](https://github.com/ohmyzsh/ohmyzsh#using-oh-my-zsh). Vou listar algumas coisas que eu acho que merecem mais destaque:

**As configurações ficam armazenadas no arquivo** ``~/.zshrc`` **e as alterações devem ser feitas lá.**

### Aliases
É possível criar aliases para comandos longos que são usados com frequência. Ao invés de digitar todas as vezes

    git pull --rebase
   é possível criar um alias e substituir o comando por 
   

    pull

Como? Editando o arquivo de configuração do **Zsh** e criando um alias:

    alias pull="git pull --rebase"
Aqui você encontra a [Cheatsheet de aliases predefinidos](https://github.com/ohmyzsh/ohmyzsh/wiki/Cheatsheet)

### Temas
É possível alterar o tema do Terminal. O **oh-my-zsh** já vem com vários temas pré-instalados. Mais informações sobre os temas [podem ser encontradas aqui.](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)


## Vim | vi (Editor de textos) 
Também é possível melhorar o editor de textos do terminal (caso você utilize o [Vim](https://github.com/vim/vim)).
### "Eu uso o Vim?" 
Se você edita utilizando o comando `vi ~/file.txt`, você já usa o Vim.
### "Como finalmente editar o arquivo!?" 
Para entrar no modo de edição, aperte a tecla `i`. Para sair do modo edição (ou modo `INSERT`) use a tecla `Esc`.
### "Estou preso no Vim! Como saio daqui?"
Primeiro saia do modo `INSERT` usando a tecla `Esc`. Para executar comando dentro do Vim, é preciso começar digitando `:`
|Ação|Comando|
|--|--|
|Sair (caso não haja alterações)|`:q`|
|Sair **sem salvar** alterações|`:q!`|
|Apenas salvar alterações|`:w`|
|**Sair e salvar**|`:wq` ou `:x`| 

### Customizando o Vim
Esse artigo lista [10 plugins essenciais para  Vim](https://medium.com/@huntie/10-essential-vim-plugins-for-2018-39957190b7a9) (alguns nem tanto). Antes de instalar individualmente os que lhe interessar, **sugiro seguir o tutorial no final de artigo sobre [como instalar os plugins](https://medium.com/@huntie/10-essential-vim-plugins-for-2018-39957190b7a9#cff4)** utilizando o **vim-plug**, uma ferramenta de gerenciamento de plugins para o Vim.


## Compartilhe
É isso, espero ter ajudado. **Compartilhe esse documento e ajude outras pessoas** a ter uma melhor experiência com o Terminal no MacOS.
