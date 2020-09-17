<template>
  <v-footer
    dark
    padless
  >
    <v-card
      flat
      tile
      class="indigo lighten-1 white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus eos tempore, enim debitis asperiores esse in rerum at ut perferendis temporibus! Doloribus soluta nisi doloremque deserunt sit error obcaecati aspernatur labore dolores dolorem itaque suscipit optio accusamus, quasi ratione reprehenderit eum voluptas impedit veniam, tempora, amet laboriosam? Nobis obcaecati doloremque atque excepturi dolor praesentium quibusdam dolorum. Suscipit fuga, fugiat alias explicabo placeat quaerat assumenda. Eius, tempore explicabo, quis enim vero asperiores itaque minus porro esse at voluptates aspernatur tempora excepturi atque provident, animi consequuntur similique beatae? Quasi, deleniti repellat veniam qui alias repellendus laudantium fuga unde rerum numquam ratione recusandae eum. Nihil necessitatibus magnam pariatur, alias repellat molestiae voluptate exercitationem dicta ab cupiditate a dolor! Minus, cumque ex ducimus magnam error atque repellat, perspiciatis incidunt itaque commodi autem quae alias perferendis est architecto, sequi dignissimos! Fuga asperiores labore distinctio perspiciatis dolores. Laborum distinctio optio provident obcaecati hic delectus facere quas ut accusantium harum enim porro laudantium qui ex, atque ipsa veniam quaerat aliquam repudiandae natus asperiores, recusandae minima tenetur fugit? Dolores velit cupiditate natus repellendus nihil minima recusandae. Iure, cupiditate veniam a fugiat vel blanditiis, est laudantium fuga distinctio rem laborum minima modi! Voluptatibus quae laudantium neque placeat, culpa earum.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
  export default {
    data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }),
  }
</script>