TMUX - Terminal Multiplexer </b></b>
link: https://dev.to/collabcode/tmux-para-iniciantes-4kg8

-Abrir TMUX:
```
$ tmux
```

Tecla Padrão de Prefixo: __ctrl + b__

-Dividindo a tela em painéis

Agora que criamos nossa primeira sessão, podemos ter uma ideia dos painéis. Quando você cria uma nova sessão, o tmux inicia por padrão com uma janela e um único painel dentro, mas queremos dividir nossa tela.

Todos os comandos no tmux são acionados por uma chave de prefixo seguida por uma chave de comando (bastante semelhante ao emacs). Por padrão, a chave de prefixo do tmux é C-b (Ctrl+b).

Essa notação pode parecer um pouco estranha se você não estiver acostumado, mas C- significa "pressione e segure a tecla Ctrl", portanto C-b significa pressionar as teclas Ctrl e b ao mesmo tempo.

Para dividir a tela com dois painéis horizontais use o comando:

**C-b + %**

Lembrando o que acabei de lhe contar sobre a sequência de prefixo e tecla de comando do tmux, com o comando acima vamos dividir seu painel único em dois painéis, um esquerdo e outro direito, pressionando Ctrl e b ao mesmo tempo, solte os dois e digite a tecla %.

Voilà! Você acabou de invocar um atalho do tmux e dividir seu painel em dois.

    Criar Aba Inferior: uma divisão de painéis superior e inferior.
```
ctrl + b + "
```

    Criar Aba Inferior e a divide (caso já haja alguma criada na bse inferior):

ctrl + b + %

    Navegação:

    Criar Aba Inferior:

ctrl + b + sete pra cima 

ctrl + b + sete pra baixo 

ctrl + b + sete pra esquerda 

ctrl + b + sete pra direita 

    Fechar um terminal:

$ exit 

    Desconecta da sessão e roda em segundo plano, mas não fechar:

ctrl + b + d 

Reaparece:

$ tmux a 

Visualizar terminais rodando em segundo plano: Reconectando a sua antiga sessão

Para se conectar a uma sessão antiga acredito que você precisa encontrar o seu nome ou número. O tmux possui um comando muito útil que nos permite obter uma lista das sessões em execução no momento, digite:

$ tmux ls 

Para me anexar a sessão artigo basta executar o comando:

$ tmux a -t session_name

    Abrindo uma Nova Janela:

ctrl + b + c 

    Para criar uma nova sessão nomeada, execute o comando tmux com os seguintes argumentos:

$ tmux new -s session_name

    Criando uma nova sessão sem sair da antiga

Por padrão o tmux sempre espera que você esteja desanexado de uma sessão para se criar outra, por isso precisamos adicionar mais um parâmetro no comando assim:

$ tmux new -s session_name -d

    Navegando dieratamente para uma cojunto de terminais: 0:bash - numero do terminal 0 1:bash - numero do terminal 1

ctrl + b + <numero do terminal> 

    Modificação na Janela:

ctrl + b + : 

A janela espera comandos como renomea-la por exemplo.

rename-window <nome deseja>

ou caindo direto no rename-window:

ctrl + b + , 

    Recarregar Configuraçẽos do Tmux;

$ tmux source .tmux.conf  

