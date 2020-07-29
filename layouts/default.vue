<template>
  <div class="flex flex-col h-screen w-screen">
    <!--
      Navigation Bar

      PARAMETERS
      :logoURL  (URL for Logo)
    -->
    <NaviWrapper
      imgURL="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcT9h0fgEyNSW5k96ujVE73Y1xs1W2wFTWy2PA&usqp=CAU"
    ></NaviWrapper>

    <div class="flex-1">
      <div class="flex">
        <Nuxt class="w-full h-screen overflow-y-auto"/>
      </div>
    </div>
    <FooterWrapper/>
  </div>
</template>
<script>
export default {};
</script>