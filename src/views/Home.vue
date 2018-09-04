<template>
  <div class="home">
    <Carousel/>
    <!-- Section 1 -->
    <container>
      <section class="text-center my-5">
        <h2 class="h1-responsive font-weight-bold my-5">Especializado na criação de Bulldog Inglês há mais de 12 anos</h2>
        <p class="lead grey-text w-responsive mx-auto mb-5">O Roysberg Kennel ao longo dos anos vem investindo para que o plantel 
          fosse formado por cães de alta qualidade, e com o passar dos anos foi possível chegar a maioria de cães do plantel 
          formada por animais nascidos no próprio canil e de linhagem internacional. Esse objetivo se traduz nos cães que hoje 
          fazem parte deste excelente plantel, formado por cerca de 20 fêmeas entre filhotes e adultas e 03 machos adultos, sendo 
          na maioria campeões e com filhos campeões no Brasil e exterior.</p>
        <row>
          <column md="4">
            <fa icon="heartbeat" size="3x" class="red-text"/>
            <h5 class="font-weight-bold my-4">Cuidados</h5>
            <p class="grey-text mb-md-0 mb-5">Nossos cachorros são muito bem cuidados por profissionais altamente qualificados e que possuem muito amor por cachorros.</p>
          </column>
          <column md="4">
            <fa icon="paw" size="3x" class="green-text"/>
            <h5 class="font-weight-bold my-4">Padrão da Raça</h5>
            <p class="grey-text mb-md-0 mb-5">Uma das raças autóctones mais antigas, conhecido como o Cão Nacional da Grã-Bretanha e associado em todo o mundo com a determinação britânica e do lendário John Bull.</p>
          </column>
          <column md="4">
            <fa icon="arrow-up" size="3x" class="orange-text"/>
            <h5 class="font-weight-bold my-4">Experiência</h5>
            <p class="grey-text mb-md-0 mb-5">Possuímos muitos anos de experiência no mercado de cães, buscamos sempre oferecer o melhor serviço para nossos clientes.</p>
          </column>
        </row>
      </section>
    </container>
    <!-- End of Section 1 -->
    <hr class="line">
    <!-- Section 2 -->
    <container>
      <section class="text-center my-5">
        <h2 class="h1-responsive font-weight-bold my-5">Conheça nossos cães</h2>
        <p class="grey-text w-responsive mx-auto mb-5">Veja abaixo uns dos melhores padreadores e matrizes que já tivemos.</p>
        <row class="text-center">
          <column lg="4" md="12" class="mb-lg-0 mb-4">
            <view-wrapper class="overlay rounded z-depth-1">
              <img src="https://mdbootstrap.com/img/Photos/Others/images/58.jpg" alt="sample photo" class="img-fluid"/>
              <a>
                <md-mask waves overlay="white-slight"/>
              </a>
            </view-wrapper>
            <card-body class="pb-0">
              <h4 class="font-weight-bold my-3">Title of the news</h4>
              <p class="grey-text">Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae.</p>
              <btn color="indigo" size="sm"><fa icon="clone" class="left"/> Saber mais</btn>
            </card-body>
          </column>
          <column lg="4" md="12" class="mb-lg-0 mb-4">
            <view-wrapper class="overlay rounded z-depth-1">
              <img src="https://mdbootstrap.com/img/Photos/Others/project4.jpg" alt="sample photo" class="img-fluid"/>
              <a>
                <md-mask waves overlay="white-slight"/>
              </a>
            </view-wrapper>
            <card-body class="pb-0">
              <h4 class="font-weight-bold my-3">Title of the news</h4>
              <p class="grey-text">Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae.</p>
              <btn color="indigo" size="sm"><fa icon="clone" class="left"/> Saber mais</btn>
            </card-body>
          </column>
          <column lg="4" md="12" class="mb-lg-0 mb-4">
            <view-wrapper class="overlay rounded z-depth-1">
              <img src="https://mdbootstrap.com/img/Photos/Others/images/88.jpg" alt="sample photo" class="img-fluid"/>
              <a>
                <md-mask waves overlay="white-slight"/>
              </a>
            </view-wrapper>
            <card-body class="pb-0">
              <h4 class="font-weight-bold my-3">Title of the news</h4>
              <p class="grey-text">Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae.</p>
              <btn color="indigo" size="sm"><fa icon="clone" class="left"/> Saber mais</btn>
            </card-body>
          </column>
        </row>
      </section>
    </container>
    <!-- End of Section 2 -->
    <!-- Section 2 -->
      <section class="container-fluid">
        <div class="row">
          <div class="divisoria">
            <h2 class="h1-responsive font-weight-bold my-5 text-div">Atuando no mercado de cães à mais de 20 anos</h2>
          </div>
        </div>
      </section>
    <!-- End of Section 2 -->
    <!-- Section 3 -->
    <container>
      <section class="text-center my-5">
        <h2 class="h1-responsive font-weight-bold my-5">Filhotes disponíveis</h2>
        <p class="grey-text w-responsive mx-auto mb-5">Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit est laborum.</p>
        <puppy-carousel/>
      </section>
    </container>
    <!-- End of Section 3 -->
  </div>
</template>

<script>
// @ is an alias to /src
import Carousel from "@/components/Carousel.vue";
import { Container, Row, Column, Fa, Btn, ViewWrapper, MdMask, Card, CardBody } from 'mdbvue';
import PuppyCarousel from "@/components/PuppyCarousel.vue";

export default {
  name: "home",
  components: {
    Carousel,
    Container,
    PuppyCarousel,
    Row,
    Column,
    Fa,
    Btn,
    ViewWrapper,
    MdMask,
    Card,
    CardBody
  }
};
</script>

<style>
.h1-responsive {
  font-size: 200%!important;
}

.line {
  width: 80%;
}

.divisoria {
  background-color: rgb(11, 43, 11);
  width: 100%;
  height: 400px;
}

.text-div {
  color: white;
}
</style>
