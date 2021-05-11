<template>
  <b-container>
    <b-row>
      <b-col cols="6" class="mx-auto">
        <b-card title="Private Dashboard">
          Welcome {{ $auth.user.name }}
        </b-card>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
   
};
</script>
