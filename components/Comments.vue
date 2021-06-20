<template>
  <div class="card m-3">
      <div class="card-body ">
          <h5>{{comment.name.title}} {{comment.name.first}} {{comment.name.last}}</h5>
      <p>{{comment.email}}</p>
      </div>
  </div>
</template>

<script>
export default {
    props:['comment']
}
</script>

<style>

</style>