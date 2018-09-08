<template>
  <container style="margin-top: 90px;">
    <section class="my-5">
      <h2 class="h1-responsive font-weight-bold text-center my-5 margin-contact">Contato</h2>
      <p class="text-center w-responsive mx-auto pb-5">Entre em contato conosco.</p>
      <row>
        <column md="9" class="md-0 mb-5">
          <form>
            <row>
              <column md="6">
                <div class="md-form mb-0">
                  <md-input type="text" id="contact-name" label="Your name" />
                </div>
              </column>
              <column md="6">
                <div class="md-form mb-0">
                  <md-input type="text" id="contact-email" label="Your email" />
                </div>
              </column>
            </row>
            <row>
              <column md="12">
                <div class="md-form mb-0">
                  <md-input type="text" id="contact-subject" label="Subject" />
                </div>
              </column>
            </row>
            <row>
              <column md="12">
                <div class="md-form mb-0">
                  <md-textarea id="contact-message" label="Your message" />
                </div>
              </column>
            </row>
          </form>
          <div class="text-center text-md-left">
            <btn color="primary" size="md">Send</btn>
          </div>
        </column>
        <column md="3" class="text-center">
          <ul class="list-unstyled mb-0">
            <li>
              <fa icon="map-marker" size="2x" class="blue-text"/>
              <p>San Francisco, CA 94126, USA</p>
            </li>
            <li>
              <fa icon="phone" size="2x" class="blue-text mt-4"/>
              <p>+ 01 234 567 89</p>
            </li>
            <li>
              <fa icon="envelope" size="2x" class="blue-text mt-4"/>
              <p>contact@example.com</p>
            </li>
          </ul>
        </column>
      </row>
    </section>
  </container>
</template>

<script>
import { Container, Row, Column, Btn, Fa, MdInput, MdTextarea, Card, CardBody } from 'mdbvue';

export default {
  name: 'ContactPage',
  components: {
    Container,
    Row,
    Column,
    Btn,
    Fa,
    MdInput,
    MdTextarea,
    Card,
    CardBody
  }

};
</script>

<style scoped>
</style>