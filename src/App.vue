<template>
  <div class="container">
    <h3>Ma fiche perso</h3>
    <div class="row">
      <div class="col-6">
        <div class="mb-3">
          <label class="form-label" for="lastname">Nom</label>
          <input v-model="lastname" class="form-control" type="text">
        </div>
      </div>
      <div class="col-6">
        <div class="mb-3">
          <label class="form-label" for="firstname">Prénom</label>
          <input class="form-control" type="text">
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-6">
        <div class="mb-3">
          <label class="form-label" for="age">Âge</label>
          <input class="form-control" type="number">
        </div>
      </div>
      <div class="col-6">
        <div class="mb-3">
          <label class="form-label" for="gender">Genre</label>
          <select class="form-control">
            <option selected disabled>Selectionner une valeur</option>
            <option value="male">Homme</option>
            <option value="female">Femme</option>
            <option value="other">Autre</option>
          </select>
        </div>
      </div>
    </div>
    <hr>
    {{ lastnameDisplay }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      lastname: '',
      lastnameDisplay: '',
    };
  },
  methods: {},
  computed: {}
}
</script>