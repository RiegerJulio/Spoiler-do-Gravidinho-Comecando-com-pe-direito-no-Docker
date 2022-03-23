<h1>Spoiler do Gravidinho: Começando com pé direito no docker.</h1>

Spoiler do Gravidinho: Começando com pé direito no docker.

Bom… eu sei que o back-end é um grande enigma para todos aqui <strong>(assim como é pra mim também)</strong> mas eu dei uma pisadinha em primeira mão e pra confortar um pouco vocês nesse caminho, eu preparei um Pré Natal para você começar a sua gestação no Back-End bem e o Assunto do 1o bloco é <strong>Docker</strong>.

Eu separei um pequeno roadmap para tentar ajudar a complementar os estudos <strong>(ou falar de uma forma um pouco menos acadêmica, leia-se carioca)</strong> então sem mais delongas, vamos direto ao assunto.

<strong>E se esse artigo te ajudou, não esquece de marcar com um Star ali em cima pois indica que meu conteúdo esta sendo útil de alguma forma. E leia também a sessão final do artigo!</strong>

<h1>1- Containers - O pacotinho que você tá esperando.</h1>

Pensa no seu bebê como uma aplicação (o seu app de receitas por exemplo) a sua aplicação precisa de um <strong>sistema operacional</strong> (ubuntu, Pop-os), <strong>bibliotecas</strong> (node), <strong>instalações</strong> (npm install) entre outros pra funcionar. O docker pega seu bebê e coloca dentro da sua barriga com todos os nutrientes necessários para ele nascer de boas, ou seja, <strong>ele pega todas as dependências necessárias e transforma em um binário</strong> (em um código) que tem tudo o que você precisa para sua aplicação funcionar.

<h1>2- Beleza, mas porque diabos eu colocaria meu bebê (aplicação) num container?</h1>

Para além da ciência que diz que a infertilidade de casais é de 20%, vou segurar nesse tópico a analogia com gravidez e me atentar só a responder a sua pergunta. Imagina que sua aplicação funciona 100% de forma eficaz na sua máquina (considerando que voce esta com o Ubuntu, node na versão 16 e com o plano de fundo de uma mulher grávida). <strong>Colocar essas informações num container garante que essa estrutura seja usada exatamente do jeito que ela deve ser</strong>, pois pode ser que a sua aplicação não funcione em outra distribuição ou versão do node entende?

<h1>3- Ok, mas como eu coloco minha aplicação num container? - Pelo Docker.</h1>

Um belo dia um nerdão cansou de ter que ficar usando <strong>máquinas virtuais*</strong> Para poder acessar aplicações porque o pc dele era um positivo e a memória dele não aguentaria tamanho processamento então ele criou uma ferramenta chamada docker que transforma suas aplicações em containers e usando seu motor docker, faz com que o processamento seja muito menor do que utilizando uma máquina virtual por exemplo. Com isso, você consegue abrir sua aplicação em qualquer outro lugar já que todas as informações estão nele. Ou seja, <strong>ELE RESOLVE UM PROBLEMA DE PORTABILIDADE</strong>.

<strong>*máquina virtual é basicamente um computador completo. é o que você precisa saber por hora.</strong>

<strong>Resumo: Ao invés de precisar emular uma máquina inteira num pc da positivo, eu estou emulando apenas uma aplicação (ou seja, APENAS O NECESSÁRIO). Parece bem menos leve só de ler, certo?</strong>

<h1>3- E Como eu alimento essas bibliotecas e sistemas? - O uso do conceito de IMAGEM.</h1>

Isso está ficando mais complicado do que você imaginava? Relaxa, imagem é algo simples.
Supondo que sua aplicação roda no ubuntu versão 20.0. Existe um site chamado <strong>DockerHub*</strong> (uma espécie de instagram de imagens) e lá, você vai falar “eu quero a imagem do ubuntu 20.0 você tem aí?" e lá você vai achar ela e vai utilizar-la para inseminar o seu bebê. Você pode também usar um arquivo chamado <strong>Dockerfile</strong> que é simplesmente a versão ‘receita de bolo’ do seu container dando toda e qualquer instrução nele. Fica bem fácil de entender com a img abaixo

<p text-align="center">
          <img src="">
</p>

Nesse caso a receita de bolo funciona assim: 
  - From é qual SO que nós vamos usar
  - workdir é o diretório dentro desse sistema operacional que a gente vai trabalhar (suponha que tu quer trabalhar no diretório de imagens. tu colocaria ./images por exemplo
  - ADD e "adicione algo"
  - Copy é copie
  - expose é pra você abrir uma porta (quando a gente dá o npm start la no vscode ele expõe essa porta 3000 pra gente conseguir ver o site. é a mesma lógica)
  - e por último CMD é "rode esse comando no terminal"

<strong>ou no jeito carioca de ser:
koe, instala o node pra mim e entra no diretório X. Depois tu adiciona esse arquivo aqui chamado node_modules. Copia ele para esse diretório ai de cima e expõe a porta 3000 pra mim. Fez tudo isso? Agr roda o npm install ai pfvr pra instalar as dependências. Vlw Flw</strong>

<h1>4- Como eu insemino o bebê (container) com essa imagem?</h1>

Boa pergunta. Quando você estiver configurando o container, basicamente você vai apontar que a imagem utilizada é a X (onde x é esse comando levemente marcado na imagem abaixo). Então o conjunto de imagens fará com que seu container esteja pronto para ser utilizado em outra máquina.

<p text-align="center">
          <img src="">
</p>


<h1>5- Muita teoria e pouca prática Rieger. Como eu boto esse bebê no mundo?</h1>

Então gravidinhos, o intuito deste artigo não é me concentrar na parte prática pois estou mais desconstruindo a teoria por trás do docker ok? Porém, alimento vocês com os links abaixo que utilizei para reforçar meus estudos e para entender um pouco mais sobre como o docker funciona e todos eles em português. Alguns são mais curtos e outros mais completos, mas sugiro também que vocês procurem mais conteúdo por fora pois é um assunto muito extenso e nem todos os assuntos serão cobertos durante o curso ou esses vídeos. Além disso, essa imagem abaixo é um grande "esqueceu de algo ou de algum comando? da uma olhada aqui ou no último link"

<p text-align="center">
          <img src="">
</p>

<strong>Mateus Muller - TUDO O QUE VOCÊ PRECISA SABER PARA COMEÇAR COM DOCKER</strong>
https://www.youtube.com/watch?v=RE31GWJGkwA

<strong>Programador a Bordo - Docker em 22 minutos - teoria e prática (Rápido!)</strong>
https://www.youtube.com/watch?v=Kzcz-EVKBEQ&t=526s

<strong>Hora de Codar - Curso de Docker para iniciantes - aprenda Docker em 1 hora</strong>
https://www.youtube.com/watch?v=np_vyd7QlXk&ab

<strong>Documentação. Essa é pra imprimir e botar na sua parede pra consultar toda hora que esquecer um comando!</strong>
https://dockerlabs.collabnix.com/docker/cheatsheet/
<br>
<br>
<h3><strong>Bom, esse é o fim desse resumo e espero que eu tenha ajudado vocês de alguma forma. Se vocês curtiram, sinalizem pra mim favoritando o repositório com uma estrelinha ou até mesmo compartilhando com outras pessoas e me deem um feedback sobre pois é muito importante pra mim. Caso você tenha achado um erro e queira editar ou até mesmo contribuir pro crescimento deste artigo, sinta-se à vontade em abrir um issue ou um PR aqui pois o intuito é somente ajudar mesmo.

TMJ e até o próximo artigo!</strong></h3>
