<template>

<post-detail
  v-for="post in Posts"
  :key="post.id"
  :id="post.id"
  :date="post.date"
  :text="post.text"
  :title="post.title"
  :img-src="post.imgSrc"
/>

<!-- Pagination -->	
<div class="pagination">				

  <span class="prev">&laquo;Previous</span>
  <span class="act">1</span>
  <a href="#">2</a>
  <a href="#">3</a>
  <a href="#">4</a>
  <a href="#">5</a>
  <a href="#">6</a>
  <a class="next" href="#">Next&raquo;</a>

</div>
</template>
<script setup>
import PostDetail from '@/components/global/post.vue'
import { Posts } from '@/use/moc-header'
</script>