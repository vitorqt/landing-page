<template>
    <Footer color="unique-color-dark" class="page-footer font-small pt-0">
        <div style="backgroundColor: #6351ce">
            <container class="text-left">
                <row class="py-4 d-flex align-items-center">
                    <column md="6" lg="5" class="text-center text-md-left mb-4 mb-md-0">
                        <h6 class="mb-0 white-text">Entre em contato conosco através de nossas redes sociais !</h6>
                    </column>
                    <column md="6" lg="7" class="text-center text-md-right">
                        <a class="fb-ic ml-0"><i class="fa fa-facebook white-text mr-lg-4"> </i></a>
                        <a class="ins-ic"><i class="fa fa-instagram white-text mr-lg-4"> </i></a>
                    </column>
                </row>
            </container>
        </div>
        <container class="mt-5 mb-4 text-center text-md-left">
            <row class="mt-3">
                <column md="3" lg="4" xl="3" class="mb-4">
                    <h6 class="text-uppercase font-weight-bold"><strong>Roysberg Kennel</strong></h6>
                    <hr class="deep-purple accent-2 mb-4 mt-0 d-inline-block mx-auto" style="width: 60px"/>
                    <p>O Roysberg Kennel ao longo dos anos vem investindo para que o plantel fosse formado por cães de alta qualidade,
                         e com o passar dos anos foi possível chegar a maioria de cães do plantel formada por animais nascidos no 
                         próprio canil e de linhagem internacional.</p>
                </column>
                <column md="2" lg="2" xl="2" class="mb-4">
                    <h6 class="text-uppercase font-weight-bold"><strong>Products</strong></h6>
                    <hr class="deep-purple accent-2 mb-4 mt-0 d-inline-block mx-auto" style="width: 60px"/>
                    <p><a href="#!">MDBootstrap</a></p>
                    <p><a href="#!">MDWordPress</a></p>
                    <p><a href="#!">BrandFlow</a></p>
                    <p><a href="#!">Bootstrap Angular</a></p>
                </column>
                <column md="3" lg="2" xl="2" class="mb-4">
                    <h6 class="text-uppercase font-weight-bold"><strong>Useful links</strong></h6>
                    <hr class="deep-purple accent-2 mb-4 mt-0 d-inline-block mx-auto" style="width: 60px"/>
                    <p><a href="#!">Your Account</a></p>
                    <p><a href="#!">Become an Affiliate</a></p>
                    <p><a href="#!">Shipping Rates</a></p>
                    <p><a href="#!">Help</a></p>
                </column>
                <column md="4" lg="3" xl="3" class="mb-4">
                    <h6 class="text-uppercase font-weight-bold"><strong>Contato</strong></h6>
                    <hr class="deep-purple accent-2 mb-4 mt-0 d-inline-block mx-auto" style="width: 60px"/>
                    <p><i class="fa fa-home mr-3"></i> Ferraz de Vasconcelos, SP</p>
                    <p><i class="fa fa-envelope mr-3"></i> contato@roysberg.com.br</p>
                    <p><i class="fa fa-phone mr-3"></i> 11 96507-3342</p>
                    <p><i class="fa fa-phone mr-3"></i> 11 4674-5576</p>
                </column>
            </row>
        </container>
        <div class="footer-copyright text-center py-3">
            <container fluid>
                &copy; 2018 Todos os direitos reservados: <a href="#"> RosybergKennel </a>
            </container>
        </div>
    </Footer>
</template>

<script>
import { Footer, Container, Row, Column } from 'mdbvue';

export default {
  name: 'FooterPage',
  components: {
    Footer,
    Container,
    Row,
    Column
  }
};
</script>