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
            <fa icon="area-chart" size="3x" class="red-text"/>
            <h5 class="font-weight-bold my-4">Qualidade</h5>
            <p class="grey-text mb-md-0 mb-5">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reprehenderit maiores aperiam minima assumenda deleniti hic.</p>
          </column>
          <column md="4">
            <fa icon="book" size="3x" class="cyan-text"/>
            <h5 class="font-weight-bold my-4">Padrão da Raça</h5>
            <p class="grey-text mb-md-0 mb-5">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reprehenderit maiores aperiam minima assumenda deleniti hic.</p>
          </column>
          <column md="4">
            <fa icon="comments-o" size="3x" class="orange-text"/>
            <h5 class="font-weight-bold my-4">Credenciado</h5>
            <p class="grey-text mb-md-0 mb-5">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Reprehenderit maiores aperiam minima assumenda deleniti hic.</p>
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
        <p class="grey-text w-responsive mx-auto mb-5">Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit est laborum.</p>
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
              <btn color="indigo" size="sm"><fa icon="clone" class="left"/> View project</btn>
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
              <btn color="indigo" size="sm"><fa icon="clone" class="left"/> View project</btn>
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
              <btn color="indigo" size="sm"><fa icon="clone" class="left"/> View project</btn>
            </card-body>
          </column>
        </row>
      </section>
    </container>
    <!-- End of Section 2 -->
  </div>
</template>

<script>
// @ is an alias to /src
import Carousel from "@/components/Carousel.vue";
import { Container, Row, Column, Fa, Btn, ViewWrapper, MdMask, Card, CardBody } from 'mdbvue';

export default {
  name: "home",
  components: {
    Carousel,
    Container,
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
</style>
