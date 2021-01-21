<template>
<v-container class="grey lighten-5">
    <v-row class="sss" no-gutters>
         <v-col
        cols="12"
        sm="4"
      >
        <chatbox />
      </v-col>
      <v-col align-self-baseline no-warp
        cols="12"
        sm="4"
      >
       <v-responsive :aspect-ratio="16/9">
        <v-card-text>
          This card will always be 16:9 (unless you put more stuff in it)
        </v-card-text>
      </v-responsive>
       <div class="reversinputbox">
         

         
         <v-textarea
          class="mx-4"
          label="send"
          rows="1"
          prepend-icon="mdi-send"
        >
        </v-textarea>
       </div>
      
        
      </v-col>
       <v-col
        cols="12"
        sm="4"
      >
        <v-card
          class="pa-2"
          outlined
          tile
        >
          One of three columns
        </v-card>
      </v-col>
      
    </v-row>
    
 </v-container>
</template>
<style>
.container {
    max-width: 100%;
}
</style>
<script>
import chatbox from '../components/chatroom/chatbox.vue'
  export default {
    data () {
      
      return {
        items: [
          {
            header: 'Today',
          },
          { divider: true },
          {
            avatar: 'https://picsum.photos/250/300?image=660',
            title: 'Meeting @ Noon',
            subtitle:
              `<span class="font-weight-bold">Spike Lee</span> &mdash; I'll be in your neighborhood`,
          },
          {
            avatar: 'https://picsum.photos/250/300?image=821',
            title: 'Summer BBQ <span class="grey--text text--lighten-1"></span>',
            subtitle:
              '<span class="font-weight-bold">to Operations support</span> &mdash; Wish I could come.',
          },
          {
            avatar: 'https://picsum.photos/250/300?image=783',
            title: 'Yes yes',
            subtitle:
              '<span class="font-weight-bold">Bella</span> &mdash; Do you have Paris recommendations',
          },
          {
            header: 'Yesterday',
          },
          { divider: true },
          {
            avatar: 'https://picsum.photos/250/300?image=1006',
            title: 'Dinner tonight?',
            subtitle:
              '<span class="font-weight-bold">LaToya</span> &mdash; Do you want to hang out?',
          },
          {
            avatar: 'https://picsum.photos/250/300?image=146',
            title: 'So long',
            subtitle:
              '<span class="font-weight-bold">Nancy</span> &mdash; Do you see what time it is?',
          },
          {
            header: 'Last Week',
          },
          { divider: true },
          {
            avatar: 'https://picsum.photos/250/300?image=1008',
            title: 'Breakfast?',
            subtitle:
              '<span class="font-weight-bold">LaToya</span> &mdash; Do you want to hang out?',
          },
          {
            avatar: 'https://picsum.photos/250/300?image=839',
            title:
              'Winter Porridge <span class="grey--text text--lighten-1"></span>',
            subtitle:
              '<span class="font-weight-bold">cc: Daniel</span> &mdash; Tell me more...',
          },
          {
            avatar: 'https://picsum.photos/250/300?image=145',
            title: 'Oui oui',
            subtitle:
              '<span class="font-weight-bold">Nancy</span> &mdash; Do you see what time it is?',
          },
        ],
        scrollInvoked: 0,
      }
    },
    components: {
        chatbox
  },
  

    methods: {
      onScroll () {
        this.scrollInvoked++
      },
    },
  }
  
</script>