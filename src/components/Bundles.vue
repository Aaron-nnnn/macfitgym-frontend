<script setup>
import {ref} from 'vue'
import {useRouter} from "vue-router";

const router = useRouter();

const showBundleDialog = ref(false)
const isLoggedIn = localStorage.getItem("isLoggedIn")
const selectedBundle = ref(null)
const selectedPrice = ref(null)

function showBundle(name, price){
    if(isLoggedIn){
        selectedBundle.value = name
        selectedPrice.value = price
        showBundleDialog.value = true
    }else{
        router.push('/login')
    }
}
function subscribe(){
    const userDetails = JSON.parse(localStorage.getItem('userDetails'))
    userDetails.subscription ={
        name: selectedBundle.value,
        price: selectedPrice.value
    }

    localStorage.setItem('userDetails', JSON.stringify(userDetails))
    showBundleDialog.value = false
}
</script>

<template>
    <v-container  style="background-color:#FFFAF0" class="mt-12">
        <v-row>
            <div class="text-display-medium mb-12">Gym Packages</div>
        </v-row>
         <v-row>
            <div class="text-label-medium font-italic">Click on a bundle to subscribe</div>
        </v-row>
        <v-row>
            <v-col md="3">
                <v-card class="text-center" @click="showBundle('Daily Pass', 800)">
                    <v-icon color="#FFDDAA" icon="mdi-calendar-clock-outline" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#FFDDAA">Daily Pass</v-card-title>
                    <v-card-text>Ksh 800</v-card-text>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card class="text-center"  @click="showBundle('1 Month', 5500)">
                    <v-icon color="#FFDDAA" icon="mdi-calendar-clock-outline" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#FFDDAA">1 Month</v-card-title>
                    <v-card-text>Ksh 5,500</v-card-text>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card class="text-center" @click="showBundle('3 Months', 15000)">
                    <v-icon color="#FFDDAA" icon="mdi-calendar-clock-outline" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#FFDDAA">3 Months</v-card-title>
                    <v-card-text>Ksh 15,000</v-card-text>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card class="text-center" @click="showBundle('6 Months', 29000)">
                    <v-icon color="#FFDDAA" icon="mdi-calendar-clock-outline" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#FFDDAA">6 Months</v-card-title>
                    <v-card-text>Ksh 29000</v-card-text>
                </v-card>
            </v-col>
        </v-row>
        <v-row>
            <v-col md="12">
                <v-card class="text-center" @click="showBundle('Annual', 55000)">
                    <v-icon color="#FFDDAA" icon="mdi-calendar-clock-outline" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#FFDDAA">Annual</v-card-title>
                    <v-card-text>Ksh 55,000</v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>

    <!-- Bundles Previleges -->
    <v-container style="background-color:#FFFAF0" class="mt-12">
         <v-row>
            <v-col>
                <div class="text-display-medium mb-12">Membership Privilleges</div>
            </v-col>
        </v-row>
        <v-row>
            <v-col md="3">
                <v-card class="text-center">
                     <v-icon color="#FFDDAA" icon="mdi-shower-head" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#FFDDAA">Hot Showers</v-card-title>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card class="text-center">
                     <v-icon color="#FFDDAA" icon="mdi-cup-water" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#FFDDAA">Free drinks</v-card-title>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card class="text-center">
                     <v-icon color="#FFDDAA" icon="mdi-hours-24" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#FFDDAA">24hr access</v-card-title>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card class="text-center">
                     <v-icon color="#FFDDAA" icon="mdi-weight-lifter" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#FFDDAA">Gym assistant</v-card-title>
                </v-card>
            </v-col>
        </v-row>
        <v-row>
            <v-col md="12">
                <v-card class="text-center">
                     <v-icon color="#FFDDAA" icon="mdi-parking" size="large" class="mt-8"></v-icon>
                    <v-card-title color="#FFDDAA">Free parking & locker</v-card-title>
                </v-card>
            </v-col>
        </v-row>
    </v-container>

    <!-- How to join -->
     <v-container style="background-color:#FFFAF0" class="mt-12">
        <v-row>
            <v-col>
                <div class="text-display-medium mb-12">How to become a member</div>
            </v-col>
        </v-row>
         <v-row>
            <v-col>
               <v-list>
                <v-list-item>1.Find a bundle in our page that well suites you.</v-list-item>
                <v-list-item>2.Make payments via the details provided either partially or fully.</v-list-item>
                <v-list-item>3.Fill in your details through the online form.</v-list-item>
                <v-list-item>4.Visit the gym to activate your account.</v-list-item>
               </v-list> 
            </v-col>
        </v-row>
         <v-row>
            <v-col>
                
            </v-col>
        </v-row>
     </v-container>
     <!-- Dialog -->
      <v-dialog v-model="showBundleDialog" max-width="600" >

      <v-card prepend-icon="mdi-account" title="Subscribe to Bundle" >
        <v-card-text>
          You are about to subscribe to {{ selectedBundle }} at {{ selectedPrice }}. Click on the button below to complete payment
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
         <v-spacer></v-spacer>
          <v-btn text="Close" variant="plain" @click="showBundleDialog = false" ></v-btn>
          <v-btn color="primary" variant="tonal" @click="subscribe()" >Subscribe</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
</template>