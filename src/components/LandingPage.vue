<script setup>

</script>

<template>
    <v-container max-width="100%">
        <v-row>
            <v-carousel>
                <v-carousel-item src="/alexandra-tran-fS3tGOkp0xY-unsplash (1).jpg" cover></v-carousel-item>
                <v-carousel-item src="/victor-freitas-vqDAUejnwKw-unsplash.jpg" cover></v-carousel-item>
                <v-carousel-item src="/rahul-singh-R_cN3dJLcK8-unsplash.jpg" cover></v-carousel-item>
            </v-carousel>
        </v-row>
    </v-container>

    <!-- About Us -->
    <v-container style="background-color:#FFFAF0" max-width="100%">
         <v-row>
            <v-col md="8" class="text-centre">
                <div class="text-display-medium mb-12">Welcome to MacFit Gym, where fitness meets determination</div>
                <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Our facility is designed to help you achieve your fitness goals in a supportive and motivating environment. Whether you are just starting your fitness journey or pushing to reach new limits, this is the right place for you.</div>
                <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Our gym provides the equipment, space, and motivation you need to build strength, improve your health, and become the best version of yourself.</div>
                <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Your fitness journey starts here. Step into a space built for progress, energy, and transformation.We are committed to helping you reach your goals and push beyond your limits.</div>
                <v-btn color="#FFDDAA">LEARN MORE</v-btn>
            </v-col>
            <v-col md="4" class="d-flex align-centre justify-centre fill-height">
                <v-img src="madison-lavern-D2uK7elFBU4-unsplash.jpg" cover></v-img>
            </v-col>
         </v-row>
    </v-container>
    <v-container>
        <v-row>
            <v-col md="4">
                <v-card>
                    <v-img src="boxed-water-is-better-JpWcneSvhDY-unsplash.jpg" cover></v-img>
                    <v-card-title></v-card-title>
                    <v-card-text>Yoga is a pracice that combines physical posture, breathing and relaxation to improve health and well-being...</v-card-text>
                    <v-btn color="#FFDDAA">READ MORE</v-btn>
                </v-card>
            </v-col>
             <v-col md="4">
                <v-card>
                    <v-img src="quokkabottles-NN68U4SwSIs-unsplash.jpg" cover></v-img>
                    <v-card-title></v-card-title>
                    <v-card-text>Do you stay hydrated at all times? Staying hydrated improves concentration and physical performance...</v-card-text>
                    <v-btn color="#FFDDAA">READ MORE</v-btn>
                </v-card>
            </v-col>
             <v-col md="4">
                <v-card>
                    <v-img src="nexa-black-gu4bdVTq0CU-unsplash.jpg" cover></v-img>
                    <v-card-title></v-card-title>
                    <v-card-text>Proper use of gym equipments reduces risk of injury while exercising...</v-card-text>
                    <v-btn color="#FFDDAA">READ MORE</v-btn>
                </v-card>
            </v-col>
        </v-row>
    </v-container>

    <!-- Reviews -->
     <v-container>
        <v-row>
            <v-col md="3">
                <v-card color="#FFFAF0">
                    <v-card-text>No other place where i feel comfortable to exercise  like here</v-card-text>
                    <v-rating :length="5" :size="32" :model-value="4" active-color="primary"></v-rating>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card color="#FFFAF0">
                    <v-card-text>My whole family comes here, It is the best Gym in Nairobi, maybe even the world</v-card-text>
                    <v-rating :length="5" :size="32" :model-value="5" active-color="primary"></v-rating>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card color="#FFFAF0">
                    <v-card-text>No other place like MacFit, it has guided me well through my workout journey</v-card-text>
                    <v-rating :length="5" :size="32" :model-value="3" active-color="primary"></v-rating>
                </v-card>
            </v-col>
            <v-col md="3">
                <v-card color="#FFFAF0">
                    <v-card-text>This is the best work out place ever, it has helped me soo muchh!!</v-card-text>
                    <v-rating :length="5" :size="32" :model-value="4" active-color="primary"></v-rating>
                </v-card>
            </v-col>
        </v-row>
     </v-container>

     <!-- Contact Us -->
     <v-container style="background-color:#FFFAF0" max-width="100%">
        <v-row class="text-centre">
            <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Opening Hours</div>
            <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Mon-Fri: 6am-8pm  |  Sat: 7am-5pm  |  Sun: 7am-2pm</div>
            <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Contact Us</div>
            <div class="text-title-large font-weight-light text-medium-emphasis mb-8">0796534016  |  macfitgym@gmail.com  |  IG: @MacFitGymm </div>
            <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Locate Us at</div>
             <div class="text-title-large font-weight-light text-medium-emphasis mb-8">Imara Mall - 2nd Floor, Garden City Mall - 3rd Floor</div>
        </v-row>
     </v-container>

</template>