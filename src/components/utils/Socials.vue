<template>
  <b-container class="l-0 p-0">
    <b-dropdown-item-button>
      <ShareNetwork
        network="whatsapp"
        :title="title"
        :url="url"
        :description="description"
      >
        <font-awesome-icon :icon="['fab', 'whatsapp']" class="size whatsapp-color"/>
        Enviar no Whatsapp
      </ShareNetwork>
    </b-dropdown-item-button>

    <b-dropdown-item-button>
      <ShareNetwork
        network="telegram"
        :title="title"
        :url="url"
        :description="description"
      >
        <font-awesome-icon :icon="['fab', 'telegram']" class="size telegram-color"/>
        Enviar no Telegram
      </ShareNetwork>
    </b-dropdown-item-button>

    <b-dropdown-item-button>
      <ShareNetwork
        network="twitter"
        :url="url"
        :title="title"
        hashtags="Cartera"
        quote="'Penso logo invisto'"
      >
      <font-awesome-icon :icon="['fab', 'twitter']" class="size twitter-color"/>
      Enviar no Twitter
      </ShareNetwork>
    </b-dropdown-item-button>

    <b-dropdown-item-button>
      <ShareNetwork
        network="facebook"
        :url="url"
        :title="title"
        :description="description"
      >
        <font-awesome-icon :icon="['fab', 'facebook']" class="size fb-color"/>
        Enviar no Facebook
      </ShareNetwork>
    </b-dropdown-item-button>
  </b-container>
</template>

<script>

export default {
  name: 'Socials',

  props: {
    url: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: false,
      default: 'Olha essa carteira! 🤑'
    },
    description: {
      type: String,
      required: false
    }
  }

}
</script>

<style scoped>
.size {
  width:  1.3rem;
  height: 1.3rem;
}

.fb-color {
  color: #3B5998;
}

.whatsapp-color {
  color: #25D366;
}

.twitter-color {
  color: #1DA1F2;
}

.telegram-color {
  color: #0088cc;
}
</style>
