<template>
  <v-container>
    <v-layout row wrap mb-0>
      <v-flex xs12 mt-0>
         <v-card
        width="100%"
        mt-0
        >
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="headline">Contact Us For Your Peace of Mind </v-list-item-title>
           
          </v-list-item-content>
        </v-list-item>

        <v-img
          src="https://www.callcentrehelper.com/images/stories/2010/03/outbound-contact-centre-760.jpg"
          height="194"
        ></v-img>

        <v-card-text>
          Please complete the form below and a representative will call you shortly
        </v-card-text>

    <v-card-actions>
    <v-spacer></v-spacer>
      <v-btn
        text
        style="background-color:blue"
       dark
      >
        Quote Me Today
      </v-btn>
      
    </v-card-actions>
      </v-card>
      </v-flex>
       
    </v-layout>
    <v-layout row wrap>
        <v-flex xs12 md6>
            <form>
              <v-text-field
                v-model="name"
                :error-messages="nameErrors"
                :counter="10"
                label="Name"
                required
                @input="$v.name.$touch()"
                @blur="$v.name.$touch()"
              ></v-text-field>
              <v-text-field
                v-model="email"
                :error-messages="emailErrors"
                label="E-mail"
                required
                @input="$v.email.$touch()"
                @blur="$v.email.$touch()"
              ></v-text-field>
              <v-text-field
                v-model="phonenumber"
                :error-messages="phoneNumberErrors"
                label="Phonenumber"
                required
                @input="$v.phonenumber.$touch()"
                @blur="$v.phonenumber.$touch()"
              ></v-text-field>
              <v-text-field
                v-model="phonenumber"
                :error-messages="phoneNumberErrors"
                label="Suburb"
                required
                @input="$v.phonenumber.$touch()"
                @blur="$v.phonenumber.$touch()"
              ></v-text-field>
              <v-textarea
                v-model="phonenumber"
                :error-messages="phoneNumberErrors"
                label="Message"
                required
                @input="$v.phonenumber.$touch()"
                @blur="$v.phonenumber.$touch()"
              ></v-textarea>

              <v-btn class="mr-4" @click="submit" style="background-color:blue"
       dark>I Need Your Services</v-btn>
            </form>
          </v-flex>
    </v-layout>
  </v-container>
</template>
