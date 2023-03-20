<template>
<!-- Post -->
<div class="post">

  <!-- Post Details -->
  <div class="post_inf">

    <span>{{ date }}</span><br />

    <NuxtLink
      class="posc" 
      :to="getHref(id)">

      3 Comments
      
    </NuxtLink>

  </div>

  <!-- Post Title - Permalink -->
  <h1>
    <NuxtLink
      :to="getHref(id)"
    >
      {{ title }}
    </NuxtLink>
  </h1>

  <!-- Post Content -->
  <NuxtLink 
    class="pic_lnk"
    :to="getHref(id)"
  >
    <img 
      src="@/assets/images/post_pic3.jpg" 
      alt="post_pic1" 
    />
  </NuxtLink>

  <p>{{ text }}</p>

</div>
</template>
<script setup>
const props = defineProps({
  id: String,
  date: String,
  title: String,
  text: String,
  title: String,
  imgSrc: String,
})

function getHref(id) {
  return '/post/' + id
}

function getImgSrc(imgSrc) {
  return '/assets/images/' + imgSrc
}

</script>