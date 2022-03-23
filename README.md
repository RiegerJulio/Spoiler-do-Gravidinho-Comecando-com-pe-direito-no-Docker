Spoiler do Gravidinho: Começando com pé direito no docker.

Bom… eu sei que o back-end é um grande enigma pra todos aqui (assim como é pra mim também) mas eu dei uma pisadinha em primeira mão e pra confortar um pouco vocês nesse caminho, eu preparei um Pré Natal pra você começar a sua gestação no Back-End bem e o Assunto do 1o bloco é Docker.

Eu separei um pequeno roadmap pra tentar ajudar a complementar os estudos da trybe (ou falar de uma forma um pouco menos academica) então sem mais delongas, vamos direto ao assunto.

1- Containers - O pacotinho que você ta esperando.

Pensa no seu bebê como uma aplicação (o seu app de receitas por exemplo) a sua aplicação precisa de um sistema operacional (ubuntu, Pop-os), bibliotecas (node), instalações (npm install) entre outros pra funcionar. O docker pega seu bebê e coloca dentro da sua barriga com todos os nutrientes necessários pra ele nascer de boas, ou seja, ele pega todas as dependências necessárias e transforma em um binário (em um código) que tem tudo o que você precisa para sua aplicação funcionar.

2- Beleza, mas porque diabos eu colocaria meu bebê (aplicação) num container?

Para além da ciência que diz que a infertilidade de casais são de 20%, vou segurar nesse tópico a analogia com gravidez e me atentar só a responder a sua pergunta. Imagina sua aplicação funciona 100% de forma eficaz na sua maquina (com o Ubuntu, node na versão 16 e com o plano de fundo de uma mulher grávida). Colocar essas informações num container garante que essa estrutura seja usada exatamente do jeito que ela deve ser pois pode ser que a sua aplicação não funcione em outra distribuição ou versão do node entende?

3- ok, mas como eu coloco minha aplicação num container? - Pelo Docker.

Um belo dia um nerdão cansou de ter que ficar usando maquinas virtuais* pra poder acessar aplicações porque o pc dele era um positivo e a memória dele não aguentaria tamanho processamento então ele criou uma ferramenta chamada docker que transforma suas aplicações em containers e usando sua engine, faz com que o processamento seja muito menor do que utilizando uma maquina virtual por exemplo. Com isso, você conseguiria abrir sua aplicação em qualquer outro lugar já que todas as informações estão nele. Ou seja, PORTABILIDADE.

maquina virtual é basicamente um computador completo. é o que você precisa saber por hora.

Resumo: Ao invés de precisar emular uma maquina inteira num pc da positivo, eu estou emulando apenas uma aplicação (ou seja, APENAS O NECESSÁRIO). Parece bem menos leve só de ler certo?

3- e Como eu alimento essas bibliotecas e sistemas? - O uso do conceito de IMAGEM.
Isso ta ficando mais complicado do que voce imaginava? Relaxa, imagem é algo simples.
Supondo que sua aplicação roda no ubuntu versão 20.0. Existe um site chamado DockerHub (uma espécie de instagram de imagens) e lá, você vai falar “eu quero a imagem do ubuntu 20.0 voce tem ai?” e lá você vai achar muito provavalmente ela e voce vai utilizar ela pra inseminar o seu bebê.

4- Como eu insemino o bebê (container) com essa imagem?
Boa pergunta. Quando você estiver configurando o container, basicamente você vai apontar que a imagem utilizada é a X (onde x é esse comando levemente marcado na imagem abaixo). Então o conjunto de imagens fará com que seu container esteja pronto para ser utilizado em outra máquina.

https://imgur.com/a/h2QvTXp

5- Muita teoria e pouca prática Rieger. Como eu boto esse bebê no mundo?

Então gravidinhos, o intuito desse artigo não é me concentrar na parte prática pois estou mais desconstruindo a teoria por trás do docker ok? Porém, alimento vocês com os links abaixos que utilizei para reforçar meus estudos e para entender um pouco mais de como o docker funciona e todos eles em português. Alguns são mais curtos e outros mais completos mas sugiro também que vocês procurem mais conteúdo por fora pois é um assunto muito extenso e nem todos os assuntos serão cobertos durante o curso ou esses vídeos.

https://www.youtube.com/watch?v=RE31GWJGkwA

https://www.youtube.com/watch?v=Kzcz-EVKBEQ&t=526s

https://www.youtube.com/watch?v=np_vyd7QlXk&ab

Bom, esse é o fim desse resumo e espero que eu tenha ajudado vocês de alguma forma. Se vocês curtiram, sinalizem pra mim favoritando o repositório com uma estrelinha ou até mesmo compartilhando com outras pessoas e me deem um feedback sobre pois é muito importante pra mim. Caso você tenha achado um erro e queira editar ou até mesmo contruibir pro crescimento desse artigo, sinta-se a vontade em abrir um issue ou um PR aqui pois o intuito é somente ajudar mesmo.

TMJ e até o próximo artigo!
