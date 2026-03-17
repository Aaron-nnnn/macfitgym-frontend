<script setup>
const userDetails = JSON.parse(localStorage.getItem('user'))
</script>

<template>
    <v-container width="50%" style="background-color:#FFFAF0" class="mt-12">
        <V-row>
            <v-col>
                <v-card class="text-center">
                    <v-img src="user-profile-icon-front-side-with-white-background.jpg" class=" mt-12 mx-auto" width="400" height="300" cover></v-img>
                    <v-card-title>{{ userDetails.name }}</v-card-title>
                    <v-card-text>{{  userDetails.email }}</v-card-text>
                    <v-card-text>{{  userDetails.phoneNumber }}</v-card-text>
                    <v-card-text>{{  userDetails.gymLocation }}</v-card-text>
                    <div v-if="userDetails.subscription">
                        <v-card-text>Your current subscription is: {{  userDetails.subscription.name }} at {{ userDetails.subscription.price }}</v-card-text>
                    </div>
                    <div v-else>
                        <v-btn color="primary" variant="outlined" to="/bundles">Select a Bundle</v-btn>
                    </div>
                </v-card>
            </v-col>
        </V-row>
    </v-container>
</template>