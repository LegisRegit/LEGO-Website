<template>
  <!-- CV Grid -->
  <section class="bg-light page-section" id="cv">
    <div class="container">
      <div class="row">
        <div class="col-lg-12 text-center">
          <h2 class="section-heading text-uppercase">Harald's CV</h2>
          <h3 class="section-subheading text-muted">Harald's Educational and Employment Credentials.</h3>
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
          name: "University Education",
          description: `<p>
              Bachelor's Degree in Software Engineering from the University of Southern Denmark.
              <br>During my education I have had courses in:
              <br>- Programming, Java, C#, SQL, and more.
              <br>- Organizational Theory.
              <br>- Project Management.
              <br>- Design of Software Systems.
            </p>`,
          active: false
        },
        {
          name: "Discord Moderator",
          description: `<p>
              Moderating an online community.
              <br>- Ensure good communication and behaviour.
              <br>- Conflict solving between members.
              <br>- Event management.
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
