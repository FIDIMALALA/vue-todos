<template>
  <authentication-form />
</template>

<script lang="ts">
import AuthenticationForm from '@/components/authentication/AuthenticationForm.vue';
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: { AuthenticationForm }
})
export default class Authentication extends Vue {}
</script>
