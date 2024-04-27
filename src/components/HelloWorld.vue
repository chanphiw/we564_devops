<template>
  <v-container class="fill-height">
    <v-responsive
      class="align-centerfill-height mx-auto"
      max-width="900"
    >
      <v-img
        class="mb-4"
        height="150"
        src="@/assets/logo.png"
      />

      <div class="text-center">
        <h1 class="text-h2 font-weight-bold">Create by Power team</h1>
      </div>

      <div class="py-4" />

      <v-row>
        <v-col cols="12">
          <v-card
            class="py-4"
            color="surface-variant"
            image="https://cdn.vuetifyjs.com/docs/images/one/create/feature.png"
            prepend-icon="mdi-rocket-launch-outline"
            rounded="lg"
            variant="outlined"
          >
            <template #image>
              <v-img position="top right" />
            </template>

            <template #title>
              <h2 class="text-h5 font-weight-bold">This Power team</h2>
            </template>

            <template #subtitle>
              <div class="text-subtitle-1">
                <!-- Replace this page by removing <v-kbd>{{ `<HelloWorld />` }}</v-kbd> in <v-kbd>pages/index.vue</v-kbd>. -->
                project devOp
              </div>
            </template>

            <v-overlay
              opacity=".12"
              scrim="primary"
              contained
              model-value
              persistent
            />
          </v-card>
        </v-col>

        <v-col cols="6" v-for="_m in memberTeams" :key="_m">
          <v-card
            append-icon="mdi-account"
            class="py-4"
            :color="_m.color"
            href="https://vuetifyjs.com/"
            prepend-icon="mdi-text-box-outline"
            rel="noopener noreferrer"
            rounded="lg"
            :subtitle="_m.name"
            target="_blank"
            :title="_m.code"
            variant="text"
          >
            <v-overlay
              opacity=".06"
              scrim="primary"
              contained
              model-value
              persistent
            />
          </v-card>
        </v-col>


      </v-row>
    </v-responsive>
  </v-container>
</template>

<script setup>
  let memberTeams = [
    {
      code : 66130045,
      name : "ปฐมพงษ์  จันทร์ผิว",
      color : "red"
    },
    {
      code : 66130099,
      name : "ณฐรัช เกตอุบล",
      color : "green"

    },
    {
      code : 66130216,
      name : "สถาพร คาบแก้ว",
      color : "blue"
    },
    {
      code : 66130294,
      name : "ทศพร ชวชัยกร",
      color : "yellow"
    }
  ]
  //
</script>
