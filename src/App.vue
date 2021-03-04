<template>
  <div class="info-header">
    <Info
        :Header="Header"
        :Text="Text"
        :Style="Style"
        :ButonAciklama="ButonAciklama"
        :Icon="Icon"
        :Border="Border"
        :FontType="FontType"

    />
  </div>
</template>

<script>
import Info from './components/Info.vue';

export default {
  name: 'app',
  components: {
    Info,
  },
  data() {
    return {
      Header: "Dikkat!",
      Text: "Güncel sözleşmenizi Sözleşme Onaylama menüsünden onayladıktan sonra işleminize devam edebilirsiniz. ",
      Style: "yellow-info",
      Icon: "logo",
      ButonAciklama:"Sözleşme Onaylama",
      Border: true
    }
  }
}

</script>


