<template>
  <!-- CV Grid -->
  <section class="bg-light page-section" id="cv">
    <div class="container">
      <div class="row">
        <div class="col-lg-12 text-center">
          <h2 class="section-heading text-uppercase">Bjørg's Portfolio</h2>
          <h3 class="section-subheading text-muted">Bjørg's Past Projects.</h3>
        </div>
      </div>
      <div class="row">
        

        <div class="col-md-4 col-sm-6 portfolio-item" v-for="entry in portfolio" :key="entry.name" >
          <button @click="entry.active = !entry.active" class="collapsible">{{entry.name}}</button>
          <div class="content" :class="{active:entry.active}" v-html="entry.description">
          </div>
        </div>

        

        </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      portfolio: [
        {
          name: "Whacky Art 1",
          description: `<p>
              <img src="./assets/whack1.jpg">
              <br>- The first whacky art piece.
            </p>`,
          active: false
        },
        {
          name: "Whacky Art 2",
          description: `<p>
              <img src="./assets/whack2.jpg">
              <br>- The second whacky art piece.
            </p>`,
          active: false
        }
        
      ]
    };
  }
};
</script>




<style>
.collapsible {
  background-color: #eee;
  color: #444;
  cursor: pointer;
  padding: 18px;
  width: 100%;
  border: none;
  text-align: center;
  outline: none;
  font-size: 18px;
}
.active,
.collapsible:hover {
  background-color: #ccc;
}
.content {
  padding: 0 18px;
  text-align: left;
  display: none;
  overflow: hidden;
  background-color: #f1f1f1;
}
.active{
    display: block;
}
</style>
