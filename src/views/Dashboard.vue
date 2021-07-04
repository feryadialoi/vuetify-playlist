<template>
  <div class="dashboard pa-3">
    <h1>Homepage</h1>
    <p
      class="red white--text"
    >Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate ipsum, officiis totam alias culpa delectus aut natus debitis. Laborum consectetur error illum eaque ratione quas, non doloribus nulla dicta maxime.</p>
    <p
      class="pink lighten-4 red--text text--darken-4"
    >Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo necessitatibus doloribus perspiciatis. Nam aperiam illo vitae eligendi reprehenderit exercitationem blanditiis perferendis fuga assumenda tenetur, laudantium laborum ullam ipsa, eveniet itaque!</p>
    <h1 class="display-4">Massive Display</h1>
    <h1 class="display-1">Smaller Display</h1>
    <p class="headline">This is a headline</p>
    <p class="subheading font-weight-bold">This is a subheading</p>
    <p class="caption">This is a caption</p>
    <v-btn class="pink white--text">click me</v-btn>
    <v-btn depressed dark color="pink">click me</v-btn>
    <v-btn text color="pink">click me!</v-btn>
    <v-btn depressed class="pink white--text">
      <v-icon>mdi-email</v-icon>
    </v-btn>
    <v-btn small>
      <v-icon small>mdi-email</v-icon>
      <span>email me</span>
    </v-btn>
    <v-btn large>
      <v-icon large>mdi-email</v-icon>
      <span>email me</span>
    </v-btn>
    <v-btn depressed fab small dark color="pink">
      <v-icon>mdi-heart</v-icon>
    </v-btn>
    <!-- breakpoint and visibility -->

    <div>
      <v-btn class="hidden-md-and-down">click me</v-btn>
      <v-btn class="hidden-md-and-up">click me</v-btn>
      <v-btn class="hidden-sm-only">click me</v-btn>
    </div>

    <!-- breakpoint and visibility end -->
  </div>
</template>
<script>
export default {};
</script>