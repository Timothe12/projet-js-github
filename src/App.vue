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
          <input v-model="firstname" class="form-control" type="text">
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-6">
        <div class="mb-3">
          <label class="form-label" for="age">Âge</label>
          <input v-model="age" class="form-control" type="number">
        </div>
      </div>
      <div class="col-6">
        <div class="mb-3">
          <label class="form-label" for="gender">Genre</label>
          <select v-model="gender" class="form-control">
            <option value="default" disabled>Selectionner une valeur</option>
            <option value="male">Homme</option>
            <option value="female">Femme</option>
            <option value="other">Autre</option>
          </select>
        </div>
      </div>
    </div>
    <div class="d-flex justify-content-end">
      <div @click="displayValues()" class="btn btn-primary">Envoyer</div>
    </div>
    <hr>
    <h3>Ma fiche perso</h3>
    <div class="row">
      <div class="col-6">
        <div class="mb-3">
          Nom : {{ lastname }}
        </div>
      </div>
      <div class="col-6">
        <div class="mb-3">
          Prénom : {{ firstname }}
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-6">
        <div class="mb-3">
          Âge : {{ formatAge }}
        </div>
      </div>
      <div class="col-6">
        <div class="mb-3">
          Genre : {{ formatGender }}
        </div>
      </div>
    </div>
    <hr>
    <h3>Ma fiche perso</h3>
    <div class="row">
      <div class="col-6">
        <div class="mb-3">
          Nom : {{ lastnameDisplay }}
        </div>
      </div>
      <div class="col-6">
        <div class="mb-3">
          Prénom : {{ firstnameDisplay }}
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-6">
        <div class="mb-3">
          Âge : {{ formatAge }}
        </div>
      </div>
      <div class="col-6">
        <div class="mb-3">
          Genre : {{ formatGender }}
        </div>
      </div>
    </div>
    <hr>
  </div>
</template>

<script>
export default {
  data() {
    return {
      lastname: '',
      firstname: '',
      age: null,
      gender: 'default',
      lastnameDisplay: '',
      firstnameDisplay: '',
    };
  },
  methods: {
    displayValues() {
      this.lastnameDisplay = this.lastname;
      this.firstnameDisplay = this.firstname;
    }
  },
  computed: {
    formatAge() {
      if(this.age) {
        return this.age + ' ans';
      }
      return '';
    },
    formatGender() {
      if (this.gender === 'male') {
        return 'Homme';
      } else if (this.gender === 'female') {
        return 'Femme';
      } else if (this.gender === 'other') {
        return "Flaque d'eau";
      }
      return '';
    }
  }
}
</script>