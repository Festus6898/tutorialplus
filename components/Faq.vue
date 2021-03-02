<template>
<b-container class="container-fluid">
  <b-row>
    <b-col sm="12">
      <div class="consult-section container-fluid p-0 mt-4" id="faq">
        <div class="p-4 text-center">          
          <div class="container px-lg-5">
            <div
              class="accordion"
              role="tablist"
              v-for="(faq, key) in faqs"
              :key="key"
            >
              <b-card no-body class="mb-3">
                <b-card-header
                  header-tag="header"
                  class="p-1 accordion-head"
                  role="tab"
                >
                  <b-button
                    block
                    variant="white"
                    class="text-left"
                    @click.prevent
                    v-b-toggle
                    :href="`#accordion-${key}`"
                  >
                    <h4>
                      {{ faq.q }}                                          
                    </h4>
                    <b-icon icon="clock"></b-icon>
                      {{ faq.t }}
                  </b-button>
                </b-card-header>
                <b-collapse
                  :id="`accordion-${key}`"
                  accordion="my-accordion"
                  role="tabpanel"
                >
                  <b-card-body class="text-left">
                    <b-card-text>                      
                      <h6 v-html="faq.a1"></h6>                                                              
                      <h6 v-html="faq.a2"></h6>                  
                      <h6 v-html="faq.a3"></h6>                      
                      <h6 v-html="faq.a4"></h6>                     
                      <h6 v-html="faq.a5"></h6> 
                      <h6 v-html="faq.a6"></h6> 
                    </b-card-text>
                  </b-card-body>
                </b-collapse>
              </b-card>
            </div>
          </div>
        </div>
      </div>
    </b-col>
  </b-row>
</b-container> 
</template>

<script>
import { defineComponent } from "@nuxtjs/composition-api";
export default defineComponent({
  props: {
    faqs: {
      type: Array
    }
  }
});
</script>

<style>

h4 {
  font-size: 1rem;
  font-weight: 500;
  color: #111957;
  cursor: pointer;
  margin: 0;
  padding: 0.4rem;
  transition: all 0.3s ease-out;
  transition-property: all;
  transition-duration: 0.3s;
  transition-timing-function: ease-out;
  transition-delay: 0s;
}
#faq{
  color: #35495e;
}
.card:hover h4 {
  padding-left: 2.6666666667rem;
}

.card {
  border: none;
  border-radius: 14px;
  box-shadow: 3px 3px 20px 3px rgb(83 67 167 / 29%);
}

.btn:focus,
.btn.focus {
  outline: 0;
  box-shadow: 0 0 0 0.2rem rgba(0, 123, 255, 0);
}

.accordion-head:hover {
  color: white;
  background: linear-gradient(to right, #2f8ce2, #4e42ff);
}

.accordion-head:hover h4 {
  color: white;
}

@media only screen and (max-width: 600px) {
.mid-text {
    width: 100%;
    font-size: 1.1rem;
  }
.accordion {
    margin: 2px;
  }
};
</style>
