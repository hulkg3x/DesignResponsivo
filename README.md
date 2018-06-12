# DesignResponsivo
Curso Web Design Responsivo: Páginas que se adaptam do mobile ao desk: https://cursos.alura.com.br/course/web-design-responsivo


<p align="center">
  <img src="https://cdn-images-1.medium.com/max/1734/1*qF8LfAwUhl57g9T0BVvVdg.jpeg" width="500px" height="250px">
</p>

# Aula 1: Design Fluído

> O foco hoje em dia para sites é o Responsive, sites que se adapta em Mobile, dispositivos moveis.

- Layout Fluidos ultiliza medidas flexiveis.
- As mais ultilizadas são ```"%"``` e ```"em"``` .
 
- Medidas Flexíveis ```"%"``` Utilizado para determinar as larguras dos elementos. A porcentagem é em relação ao tamanho do elemento pai. Pode ser utilizado para fontes, tamanho relativo ao tamanho da fonte do elemento pai

- Medidas Flexíveis ```"em"``` Normalmente utilizado para fontes. Medida sempre está relacionado à fonte base, um font-size implícito equivale a 16px na maioria dos navegadores.

# Aula 2: Mais Design Fluídos.

> Como dito são medidas bastante flexiveis, podendo usar medias de ```porcetagens``` e medias ```em```

<p align="center">
  <img src="https://s3.amazonaws.com/caelum-online-public/responsivo/aula-2/image8.jpg" width="500px" height="250px">
</p>

- Como exemplo acima. temos o ```<body>``` onde seu tamanho é ```1280px``` e que onde no mobile pode chegar a ```360px```.
- Temos o ```<main>``` onde sua largura é de ```90%``` em relação ao Pai que é o ```<body>```, que no px equivale a ```1152px``` e ambos os lados que sobra de ```5%``` que equivale a ```54px``` e em telas menores de ```18px``` em cada lado.

- Tudo é pixel, claro mais usando os calculos em ```%``` teremos esses calculos sendo feitos automaticamente, conforme a resolução ultilizada.

<p align="center">
  <img src="https://s3.amazonaws.com/caelum-online-public/responsivo/aula-2/image9.jpg" width="500px" height="250px">
</p>

- Vendo acima temos dois elementos dentro da tag ```<main>``` onde temos um ```width: 50%;``` em 2 elementos. Ou seja esses dois elementos vai ocupar ```100%``` do elemento ```<main>```. Não importa se o ```<main>``` tem ```90%```, (**não faz sentido, mas para o navegador sim.**) entao é ```100%``` de ```90%```.

- Cuidado porque estamos definindo ```100%```do elemento ```<main>``` e nao do ```<body>```, entao não é ```45%``` e sim ```50%```.

<p align="center">
  <img src="https://s3.amazonaws.com/caelum-online-public/responsivo/aula-2/image10.jpg" width="500px" height="250px">
</p>

- Por isso é fácil, se eu quiser dentro de cada uma dessas sections um grid de três colunas, que estão dentro de um elemento composto de duas colunas, dentro de outro elemento que é 90%, parece meio confuso, mas não, é fácil: três colunas, 33%:

> Podemos limitar o tamanho do nosso navegador, para casos como TV de alta resolução 4K de 3800 pixels, e claro não queremos ter tanto trabalho para **Varios tipos de telas maiores** o foco é sempre os menores. entao podemos limitar o tamanho do nosso site.


<p align="center">
  <img src="https://s3.amazonaws.com/caelum-online-public/responsivo/aula-2/image24.jpg" width="500px" height="250px">
</p>

- como exemplo acima estamos limitando o site ate ```1200px```.

# Aula 3: Media Queries

> DESIGN FLUÍDO RESOLVE SÓ METADE DO PROBLEMA. Com Media queries podemos deixar o nosso site muito, mais muito flexivel..

- Para isso usamos o Media Querie. Com ele podemos adaptar nosso site a diversas resolução de dispositivos.

> Para implementar o media querie podemos por ```@media ();```, sem contar outros valores que precisamos especificar no @media.
> - Assim surgindo o ```"Layout Condicional"```, onde podemos especificar um determinado estilo a tela.

- exemplo 

```css
  .secao {
    width: 100%;
  }
  .secao {
    width: 50%;
  }
  .secao {
    width: 33.333%;
  }
```

 - Imagine-se esses três códigos, todos corretos, porém cada um para um tipo de cenário específico: desktop, mobile e tablet.

```css
    .secao {
    width: 100%;
  }
  @media (min-width: 768px) {
    .secao {
      width: 50%;
    }
  }
  @media (min-width: 1024px) {
    .secao {
      width: 33.333%;
    }
  }
``` 

- Podemos entrar nesse link e saber mais sobre os @media query <a href="https://developer.mozilla.org/pt-BR/docs/Web/Guide/CSS/CSS_Media_queries">Media Query </a>

# Aula 4: Workflow & Viewport

> Viewport o fluxo para desenvolvimento quando referece a sites mobile responsivo, onde podemos acompanhar todo o desenvolvimento e teste em algum emulador ou no proprio mobile.

 - Quando testamos um site em algum celular, notamos que algums abre em versao desktop, isso porque celulares ate mesmo com o iphone suporta duas formas de vizualizar o site, desktop e mobile. 

- para sinalizar que queremos q aquele site seja vizualizado no mobile quando estiver em um celular precisamos informar ao nosso HTML.

```html
  <meta name="*viewport*" content="width=device-width">
```

- Assim terá suporte a todos os dispositivos mobile.

> Podemos Realizar varios teste com emuladores , consoles dos navegadores o inspect, fazer compartibilidade com dispositivo no computador abilitando as  opçoes de simuladores. Ou conexões remotas com o weinre...

# Aula 5: Menu Responsivo

> Podemos Criar menu responsivo com as propriedades que vimos o ```@media``` que possibilita fazer menu diferente dependendo do tipo de tela.

- Como Exemplo esse site abaixo temos ele aberto em plataforma desktop onde o menu esta estendido com todos seus efeitos de estilo e etc..

**Foto ilustrativa**
<p align="center">
  <img src="http://www.vmaffluence-shoptechnology.biz/wp-content/uploads/2017/03/w4.png" width="500px" height="250px">
</p>

  

- ao abrir ou redimencionar o site ele vai fazer o menu colapsar.

**Foto ilustrativa**
<p align="center">
  <img src="https://inspirationalpixels.com/wp-content/uploads/2014/08/responsive-menu-thumb1-910x540.png" width="500px" height="250px">
</p>

- Ou da forma que achar melhor...

# Aula 6 : Imagens Responsivas

> As imagens são parte essencial de todas as páginas da Web e quando falamos de Design Responsivo.

- como em tela as image também tem uma enorme importancia em relação aos pixeis.