<template>
  <div class="card mb-3" style="width: 100%">
    <div class="row g-0">
      <div class="col-md-4">
        <img
          src="https://www.freedigitalphotos.net/images/img/homepage/87357.jpg"
          class="img-fluid rounded-start"
          alt="..."
        />
      </div>
      <div class="col-md-8">
        <div class="card-body">
          <h5 class="card-title">Card title</h5>
          <h5 class="card-title">Card title</h5>
          <p class="card-text">
            This is a wider card with supporting text below as a natural lead-in
            to additional content. This content is a little bit longer.
          </p>
          <p class="card-text">
            <small class="text-muted">Last updated 3 mins ago</small>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.card-body {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.mb-3 {
  border-radius: 8px;
}

img {
  border-radius: 8px 0px 0px 8px;
  height: 360px;
}
</style>