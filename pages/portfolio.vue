<template>
  <v-container>
    <div>
      <!-- render data of the person -->
      <h1>{{ person.fields.name }}</h1>
      <!-- render blog posts -->
      <ul>
        <li v-for="post in posts" :key="post.fields.title">
          {{ post.fields.title }}
        </li>
      </ul>
    </div>
  </v-container>
</template>

<script>
import { createClient } from '~/plugins/contentful.js'

const client = createClient()

export default {
  // `env` is available in the context object
  async asyncData({ env }) {
    try {
      const [entries, posts] = await Promise.all([
        // fetch the owner of the blog
        client.getEntries({
          'sys.id': env.CTF_PERSON_ID,
        }),
        // fetch all blog posts sorted by creation date
        client.getEntries({
          content_type: env.CTF_BLOG_POST_TYPE_ID,
          order: '-sys.createdAt',
        }),
      ])
      return {
        person: entries.items[0],
        posts: posts.items,
      }
    } catch (message) {
      return console.error(message)
    }
  },
}
</script>
