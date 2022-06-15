<h1> 🖥Projeto final disciplina de Fundamentos de informática🖥 </h1>


<h2>  Tutorial básico de como instalar e usar o GitHub no Linux. (kali-linux neste caso)🐉 </h2>

<br>

<li> 1. Abra o terminal na sua máquina com linux, instale o GitHub utilizando os seguintes comandos.(siga o passo-a-passo):🕶

>$sudo apt-get update

O comando apt-get update atualiza a lista de pacotes e programas que podem ser instalados na máquina.

![kali01](https://user-images.githubusercontent.com/104872043/170814550-e0efaf54-2df9-413f-b6ab-41eafe7d3710.png)

<br>
<hr>
    
<li> 2. Digite:🕶

>$sudo apt-get install git

O comando apt-get install git instala a última versão do git na máquina. E em seguida escreva o comando:

>$git --version

Que serve para você confirmar que o git foi instalado.

![kali02](https://user-images.githubusercontent.com/104872043/170814552-188c2e63-e364-4b55-bd61-f6eafb5568b4.png)

<br>
<hr>

<li> 3. Digite:🕶

>$git config --global user.name "seunome"

>$git config --global user.email "seuemail"

Estes comandos servem para logar na sua conta do GitHub(se você não tem crie no site: https://github.com).

![kali03](https://user-images.githubusercontent.com/104872043/170814553-2bdcd44b-1512-4034-ae10-b0560cabb7cd.png)

<br>

<h2>Bom, com nosso GitHub instalado e logado, precisaremos de uma chave SSH para que possamos mexer no GitHub com segurança.</h2>

<br>
<hr>
    
<li> 4. Digite os seguintes comandos para ir a pasta das SSH (Chaves do git):🕶

>$ cd

>$ ~/.ssh/

>$ls 

(Se é a primeira vez que você baixou o github no computador provavelmente terá apenas "know_hosts" dentro da pasta.)

>$ssh-keygen

(Após colocar o comando, você deverá colocar um nome para sua chave.)
(Para gerar duas chaves SSH, uma pública e outra privada. A pública será usada no git e a privada apenas no seu computador.)

![imagem_2022-05-31_052331596](https://user-images.githubusercontent.com/104872043/171127607-41d04403-7c18-4f0b-b022-f3376edca636.png)

<br>
<hr>
    
<li> 5. Com a chave criada, iremos abrir a chave .pub para que possamos colocar no site do GitHub.🕶

>$cat "nomequevocêcolocou.pub"

E copiara esta chave:

![kali04](https://user-images.githubusercontent.com/104872043/170814554-e01c1ae1-ee5b-4abe-8ce9-73a722e435ec.png)

<br>
    
<li> 6. Irá até o site do GitHub -> Settings ->SSH and GPG keys -> New SSH Key -> coloque um nome para sua chave e cole ela abaixo.🕶

<br>
<hr>
    
<li> 7. Pronto com sua chave pública no site, você deve colocar a sua chave privada no computador. Assim:🕶

No terminal digite:
>$ssh-add "suachave" 

(desta vez sem .pub!), coloque a senha que você colocou.

![kali05](https://user-images.githubusercontent.com/104872043/170814555-71a6ad9f-c98b-4dfa-87e4-64406acff725.png)

<br>
    
<h2> Depois de criado suas chaves SSH o próximo passo no nosso tutorial é como criar um repositório, clonar e enviar pro GitHub. </h2>

<br>
<hr>
    
<li> 8. Você deve ir ao site do GitHub, logar e procurar pelo botão "New".🕶

<br>
<hr>
    
<li> 9. Lá você irá escolher as seguintes opções:🕶

![diretorio](https://user-images.githubusercontent.com/104872043/170817985-4e509405-6adf-4509-8fe6-2fc7d969daa4.png)

<br>
<hr>
    
<li> 10. Criado o repositório, você entrará nele, clicará em Code, em seguida SSH e copiará o link que estará lá. Como mostram as imagens abaixo:🕶

![code](https://user-images.githubusercontent.com/104872043/170818225-5859070c-73af-4347-bc44-ce5037170e19.png)

<br>
<hr>
<br>
    
![ssh](https://user-images.githubusercontent.com/104872043/170818235-aef7cf37-57d5-4e79-b903-1ad7be9555ed.png)

<br>
<hr>
    
<li> 11. Feito isso, abriremos o terminal do Linux, escolheremos um local para fazer o clone do repositório por meio de navegação com o comando cd que já foi ensinado antes.🕶

>$cd
>$cd/
    
<br>
<hr>

<li> 12. Assim que escolher a sua pasta, usará o seguinte comando:🕶

>$git clone "e o link que você copiou"

(no linux você pode usar o botão de scroll do mouse para colar algo que foi copiado no terminal)

![giclone](https://user-images.githubusercontent.com/104872043/170818228-2538bf71-46e8-4a70-b773-c3b8275e0ddb.png)

<br>
<hr>
    
<li> 13. Entre dentro do projeto com:🕶

>$cd/"nome do projeto que você colocou".

<br>
<hr>
    
<li> 14. Para versionar um arquivo você pode usar o comando:🕶

>$git add .          (este comando é para adicionar todos arquivos que você criou novo.)

![gitadd](https://user-images.githubusercontent.com/104872043/170818229-c99bcdb4-ae0b-4808-b431-982656a9f9b7.png)

Para versionar só 1 arquivo, por exemplo o "main.py", você usaria:

>$git add main.py

![gitaddmain](https://user-images.githubusercontent.com/104872043/170818230-c5e3d0ab-2a4e-4175-b36d-9c5a8cc1e62a.png)

<br>
<hr>
    
<li> 15. Para commitar algo, você pode utilizar:🕶

>$git commit -m "mensagem que você deseja commitar"

![gitcommit](https://user-images.githubusercontent.com/104872043/170818231-82754591-33cb-4b98-865f-5a731bb5d309.png)

<br>
<hr>
    
<li> 16. Para ver os logs utilize o comando:🕶

>$git log

![gitlog](https://user-images.githubusercontent.com/104872043/170818233-6f0c494e-1bd8-4dce-bd53-d4330c1bf3d8.png)

<br>
<hr>
    
<li> 17. "Okay. Adicionei meus arquivos, commitei, pronto?" -Não, na verdade você deve dar um comando para levar estes arquivos para o GitHub agora. 
O comando:🕶

>$git push

![gitpush](https://user-images.githubusercontent.com/104872043/170818234-28a6d101-3796-4195-9c20-108965247f8b.png)

<br>
<hr>
    
<h2>Agora explicarei um pouco sobre fluxo de trabalho, main(master), branch, merge e tags.🧐</h2>

<br>
    
  Existem formas de trabalhar no GitHub e a mais usada delas é com um *branch*(galho) principal chamado *main*. Todas principais modificações da aplicação ficará no main, que é como se fosse uma linha reta, porém, quando criamos uma branch geraremos uma ramificação no main haverá 2 main's, ou seja, 2 branchs, - 1 branch - main e - 1 branch ramificado.
  
  Isto serve para que mais de uma pessoa possa trabalhar em um único projeto e fazer modificações no projeto. Assim que modificamos, criamos outro branch, podemos unir ele denovo com o main, este movimento de unir um branch com o main se chama *merge*.
  
  Não necessáriamente um branch deve partir do main, ele pode partir de outro branch, oque importa é que no fim o projeto una todos os branch's para o main. (Supondo que todos estejam corretos e sem bugs).
  Este momento que se unem vários branches para entrega de algum prazo, ou algo do tipo, se chama *tag*, que pode ser chamado de etiqueta. Esta etiqueta é útil caso ocorram bugs no programa e os desenvolvedores precisem "voltar no tempo" o código, permitindo rastrear o bug.
  
<br>
<hr>
    
<h2> Comandos para fazer um branch, subir o branch, fazer pull-request, merge e gerar uma tag (release).📄 </h2>
    
<br>
<hr>
    
<li> 18. Neste caso vamos criar um branch chamado "HelloWorld" digitando os seguintes códigos no terminal:🕶

>$git checkout -b HelloWorld

![checkout](https://user-images.githubusercontent.com/104872043/171126038-8379a6c8-12fe-455c-9abf-87b84b0da500.png)
    
<br>
<hr>

<li> 19. Para publicar o branch usaremos:🕶

>$git push --all

![pushall](https://user-images.githubusercontent.com/104872043/171125054-207553db-0a2c-48a1-9b59-285083c2261a.png)
    
<br>
<hr>
    
<li> 20. Para fazer um Pull-Request(Isto é, pediremos para alguém revisar e subir nosso branch para main, geralmente em uma empresa tem alguém responsável por fazer essa revisão) iremos no nosso diretório no github, selecionaremos o nosso branch clicando em main e em seguida selecionando a sua branch.🕶

![pullrequest](https://user-images.githubusercontent.com/104872043/171125310-f9e68b29-b3c2-484c-8392-cc1e1c6c54e3.png)
    
<br>
    
![pullre2](https://user-images.githubusercontent.com/104872043/171125306-dd5d0ed8-e76d-4ae9-bf5a-ce3739f75f5f.png)
    
<br>
<hr>
    
<li> 21. Feito isso, você terá seus arquivos no git, caso você esteja em outro computador sem os arquivos ou queira os arquivos atualizados do git, você deve fazer um Pull(buscar), deste jeito:🕶
    
>$git pull
   
![pull22222](https://user-images.githubusercontent.com/104872043/171125305-6abc6821-88b8-4705-a193-bf6a5ac1ecbd.png)

<br>
<hr>

<li> 22. Outros 2 códigos importantes são o diff e o log que basicamente usamos eles para ver as "diferenças" de uma versão do projeto para outra.🕶
        
>$git log
    
Para vermos as modificações. Assim que mostrar no terminal você deve copiar oque está do lado do commit (geralmente é uma texto como "ssqçdlkqsçldjkqskjs516d5q1561sds1q65161s56") e em seguida usar ele no diff, deste jeito:
    
>$git diff "ssqçdlkqsçldjkqskjs516d5q1561sds1q65161s56"
    
<br>
<hr>
    
<li> 22. Para gerar uma tag(entrega) usaremos: 🕶

>$git tag -m "mensagem da tag" "versão/nome tag"

![taggit](https://user-images.githubusercontent.com/104872043/171124930-50569a25-d32d-4bd9-a406-51b51f0cd6c6.png)
    
<br>

Para vermos as tag's, basta usar:

<br>

>$git tag

<br>
<hr>
    
<li> 23. E por fim devemos subir a tag, ela apenas existirá no nosso computador por enquanto, então devemos subila para o git. Para subir basta executar:🕶

>$git push --tags
    
![gitpushtags](https://user-images.githubusercontent.com/104872043/171125294-19e8aeb2-c690-4f8e-9f01-a05ae033d629.png)
    
<br>
<hr>

<h3>📚Finalizado nosso tutorial aprendemos como:📚 </h3>

<ul>
<li>Criar nosso primeiro repositório</li>
<li>Clonar repositórios</li>
<li>Criar chaves SSH</li>
<li>Branches</li>
<li>Commitar</li>
<li>Enviar modificações</li>
<li>Fazer marge</li>
<li>Criar tag's</li>
<li>Realizar pull request</li>
<li>Sobre fluxo de trabalho</li>   
</ul>
    
<hr>
    
<h2>Bom, este é o fim do meu tutorial de como usar o GitHub via terminal do linux, espero que tenham gostado e aprendido, qualquer dúvida consulte o vídeo do meu professor Felipe Vargas ensinando passo-a-passo explicado clicando: </h2> 
<a href="https://youtu.be/eaUnh8JbRbc">--> 📌 AQUI 📌<-- </a>
