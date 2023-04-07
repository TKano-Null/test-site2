<template>
  <v-app>
    <v-main class="bg-black">
      <v-btn href="#" v-scroll-to="'#test'" :active="false">
        Scrolle Button
      </v-btn>
      <v-container>
        <!-- justify contentsを中央揃えに -->
        <v-row>
          <v-sheet style="width: 800px">
            <v-card>
              <v-card-text>
                <div style="text-align: center; height: 1000px">
                  <h1>test</h1>
                </div>
              </v-card-text>
            </v-card>
            <v-divider thickness="5"></v-divider>
            <v-card>
              <v-card-text>
                <div id="test" style="text-align: center; height: 1000px">
                  <h1>scroll here</h1>
                </div>
              </v-card-text>
            </v-card>
          </v-sheet>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>
