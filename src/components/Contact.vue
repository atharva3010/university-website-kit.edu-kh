<template>
  <v-container>
    <v-layout row wrap>
      <v-flex xs12 md6>
        <h1 style="font-size: 36px; line-height: 49px; color: #FFFFFF;" class="mt-4 mb-4">
          Contact
        </h1>
        <v-form name="Contact" method="post" netlify ref="form" action="/thanks" v-model="valid" data-netlify="true">
          <input type="hidden" name="form-name" value="Contact"/>
          <v-flex xs12>
            <v-text-field
              v-model="name"
              outline
              label="Full Name"
              name="name"
              color="#B9BCC1"
              required
              dark
              :rules="nameRules"
            >
              <v-icon slot="append" color="#B9BCC1">person</v-icon>
            </v-text-field>
          </v-flex>
          <v-flex xs12>
            <v-text-field
              v-model="email"
              outline
              color="#B9BCC1"
              label="E-Mail"
              name="email"
              required
              dark
              :rules="emailRules"
            >
            <v-icon slot="append" color="#B9BCC1">email</v-icon>
            </v-text-field>
          </v-flex>
          <v-flex xs12>
            <v-text-field
              v-model="phone"
              outline
              label="Phone Number"
              name="phone"
              color="#B9BCC1"
              required
              dark
              :rules="phoneRules"
            >
              <v-icon slot="append" color="#B9BCC1">local_phone</v-icon>
            </v-text-field>
          </v-flex>
          <v-flex xs12 class="mb-4">
            <v-textarea
              outline
              hide-details
              dark
              v-model="message"
              color="#B9BCC1"
              name="message"
              label="Message"
            >
            </v-textarea>
          </v-flex>
          <v-flex xs12 class="mt-4 mb-4">
            <v-btn 
              dark 
              block 
              large 
              depressed 
              style="padding:0; margin:0; background: #AC3931; box-shadow: 0px 9px 24px rgba(0, 0, 0, 0.25), 0px 4px 4px rgba(0, 0, 0, 0.25); border-radius: 4px; text-transform:capitalize; font-size: 16px; height:74px;" 
              color="#4B7F52"
              type="submit"
              :disabled="!valid"
            >
              Send<v-icon>keyboard_arrow_right</v-icon>
            </v-btn>
          </v-flex>
        </v-form>
      </v-flex>
    </v-layout>
    <v-layout row wrap>
      <v-flex xs12 md6>
        <v-card 
          width="300px" 
          color="#191C21" 
          dark
          class="hidden-sm-and-down pa-1"
          style="position:absolute; top:10%; left:59%; border: 1px solid #E1E7ED; box-sizing: border-box; border-radius: 3px;">
          <v-card-text>
            <!-- <v-flex xs12>
              <h1 style="font-size: 28px; color: #D8DADE;">
                Contact
              </h1>
              <p style="font-size: 14px; color: #B9BCC1;">
                Kirirom Institute of Technology
              </p>
            </v-flex> -->
            <v-flex xs12 class="mb-4">
              <h2 style="font-size: 20px; color: #D8DADE;">
                Address
              </h2>
              <p style="font-size: 14px; color: #B9BCC1;">
                #253, 255 E0, 
                <br> 
                Borey BipupThmey-Boeung Chhouk Road 2011 (Ouknhar Tri Heng Road), 
                <br>
                Street E; Khan Sen Sok, 
                <br>
                Phnom Penh, Cambodia
                <br>
                <a href="https://www.google.com/maps/dir//kirirom+institute+of+technology+maps/data=!4m6!4m5!1m1!4e2!1m2!1m1!1s0x3108e8f0cdf32b35:0xadc8d363bd3d1c6c?sa=X&ved=2ahUKEwjEnP_f4PTiAhVXAogKHRgZAh8Q9RcwEnoECAsQDg">
                Get Directions
                </a>
              </p>
            </v-flex>
            <v-flex xs12 class="mb-4">
              <h2 style="font-size: 20px; color: #D8DADE;">
                E-Mail
              </h2>
              <p style="font-size: 14px; color: #B9BCC1;">
                <a href="mailto:leo@asiato.asia">leo@asiato.asia</a>
              </p>
            </v-flex>
            <v-flex xs12>
              <h2 style="font-size: 20px; color: #D8DADE;">
                Phone Number
              </h2>
              <p style="font-size: 14px; color: #B9BCC1;">
                <a href="tel:+85578777348">+(855) 78 777 348</a>
              </p>
            </v-flex>
          </v-card-text>
        </v-card>
      </v-flex>
      <v-flex xs12>
        <v-card 
          width="100%" 
          color="#191C21" 
          dark
          class="hidden-md-and-up mb-4 mt-4 pa-1"
          style="border: 1px solid #E1E7ED; box-sizing: border-box; border-radius: 3px;">
          <v-card-text>
            <!-- <v-flex xs12>
              <h1 style="font-size: 28px; color: #D8DADE;">
                Contact
              </h1>
              <p style="font-size: 14px; color: #B9BCC1;" class="ma-1">Kirirom Institute of Technology
              </p>
            </v-flex> -->
            <v-flex xs12 class="mb-4">
              <h2 style="font-size: 20px; color: #D8DADE;">
                Address
              </h2>
              <p style="font-size: 14px; color: #B9BCC1;">#253, 255 E0, Borey BipupThmey-Boeung Chhouk Road 2011 (Ouknhar Tri Heng Road), Street E; Khan Sen Sok, Phnom Penh, Cambodia
              <br>
              <a href="https://www.google.com/maps/dir//kirirom+institute+of+technology+maps/data=!4m6!4m5!1m1!4e2!1m2!1m1!1s0x3108e8f0cdf32b35:0xadc8d363bd3d1c6c?sa=X&ved=2ahUKEwjEnP_f4PTiAhVXAogKHRgZAh8Q9RcwEnoECAsQDg">
              Get Directions
              </a>
              </p>
            </v-flex>
            <v-flex xs12 class="mb-4">
              <h2 style="font-size: 20px; color: #D8DADE;">
                E-Mail
              </h2>
              <p style="font-size: 14px; color: #B9BCC1;">
                <a href="mailto:leo@asiato.asia">leo@asiato.asia</a>
              </p>
            </v-flex>
            <v-flex xs12>
              <h2 style="font-size: 20px; color: #D8DADE;">
                Phone Number
              </h2>
              <p style="font-size: 14px; color: #B9BCC1;">
                <a href="tel:+(855)78777348">+(855) 78 777 348</a>
              </p>
            </v-flex>
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data(){
    return{
      valid: false,
      name: '',
      email: '',
      phone: '',
      message: '',
      nameRules: [
        v => !!v || 'Name is required',
      ],
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+/.test(v) || 'E-mail must be valid'
      ],
      phoneRules: [
        v => !!v || 'Phone no. is required',
      ],
    }
  }
}
</script>

<style>
  input:focus, textarea:focus { 
    border-color: 1px solid #3D424E !important;
  }
  input:focus, textarea:focus{
  outline-offset: 0px !important;
  outline: none !important;
  }
  @-webkit-keyframes autofill {
      to {
          color: #B9BCC1;
          background: transparent;
      }
  }

  input:-webkit-autofill {
      -webkit-animation-name: autofill;
      -webkit-animation-fill-mode: both;
  }
  @media only screen and (max-width: 600px) {
  .container{
    max-width: 292px;
  }
  }
  @media only screen and (min-width: 768px) {
    .container{
      max-width: 600px;
    }
  }
  @media only screen and (min-width: 1024px) {
    .container{
      max-width: 900px;
    }
  }
</style>
