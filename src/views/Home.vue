<template>
  <div>
    <HeaderComponent/>
    <div>
    </div>
    <FooterComponent/>
  </div>
</template>

<script>
// @ is an alias to /src
import HeaderComponent from '@/components/HeaderComponent.vue';
import FooterComponent from '@/components/FooterComponent.vue';

export default {
  name: 'home',
  components: {
    HeaderComponent,
    FooterComponent,
  },
};
</script>
