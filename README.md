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