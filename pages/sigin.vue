<template>
    <section class="BG">
        <div>
            <div class="d-flex align-center justify-center" style=" height:100vh;">
                <v-card width="600">

                    <v-toolbar color="#161A30" dark style="display: flex;align-items: center; flex-direction: column; background: linear-gradient(90deg, rgba(121,120,136,1) 0%, rgba(22,26,48,1) 57%);">

                        <v-toobar-tittle style="font-weight: bold;">
                            SIGN-IN
                        </v-toobar-tittle>

                    </v-toolbar>


                    <v-card-text>
                        <v-form>
                            <v-text-field outlined label="Email" prepend-inner-icon="mdi-account"> </v-text-field>
                            <v-text-field outlined label="Password" prepend-inner-icon="mdi-lock"
                                :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'" @click:append="show1 = !show1"
                                :type="show1 ? 'text' : 'password'"> </v-text-field>
                            <div class="text-align: left my-5">
                                <v-btn text color="#161A30">Forgot Password</v-btn>
                            </div>
                            <v-btn color="#161A30" dark elevation="5" rounded block style="font-weight: bold;background: linear-gradient(90deg, rgba(121,120,136,1) 0%, rgba(22,26,48,1) 57%);">Signin</v-btn>

                        </v-form>
                    </v-card-text>
                </v-card>

            </div>

        </div>
    </section>
</template>

<script>
export default {
    layout: 'auth',
    data() {
        return {
            show1: false,
        }

    }

}
</script>
<style>
.BG {
    background-image: url(~/assets/bg2.jpg);
    background-position: center center;
    background-size: cover;

}

.Signin {
    background-image: url(~/assets/V.jpg);
    background-position: center center;
    background-repeat: no-repeat;


}
</style>