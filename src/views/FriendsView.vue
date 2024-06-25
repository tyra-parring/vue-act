<template>
  <div>
    <div v-if="friends.length === 0">
      <spinner />
    </div>
    <div v-else>
      <div v-for="friend in friends" :key="friend.id">
        <div
          class="card"
          :style="{
            'border-color': friend.gender === 'male' ? 'gold' : 'green'
          }"
        >
        <Card>
          <template #cardTitle>
            <h2>{{ friend.firstName }} {{ friend.lastName }}</h2>
          </template>
          <template #cardContent>
            <h2>{{ friend.gender }}</h2>
            <p>{{ friend.profile }}</p>
            <p>{{ friend.contactDetails }}</p>
          </template>
        </Card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Card from '../components/CardComp.vue'

export default {
  components: { Card },
  data() {
    return {
      friends: [
        { id: 1, firstName: 'Kiara', lastName:  'Adams',  gender: 'female', profile:'kiara_adams', contactDetails: '0653643503' },
        { id: 2, firstName: 'Mohammad', lastName: 'Mohamad',  gender: 'male', profile: 'mo.mo_', contactDetails: '0629257295' },
        { id: 3, firstName: 'Chloe', lastName: 'Smith',  gender: 'female', profile: 'chloe.smith_', contactDetails: '0836223122' },
        { id: 4, firstName: 'Ntando', lastName: 'Mabuto',  gender: 'male', profile: 'ntando.boi', contactDetails: '0675674567' },
        { id: 5, firstName: 'Candice', lastName: 'Keet',  gender: 'female', profile: 'candice_keet', contactDetails: '0644213421' },
        { id: 6, firstName: 'Tyra', lastName: 'Parring',  gender: 'female', profile: 'tyranatalie_', contactDetails: '0660266730' },
        
      ]
    }
  }
}
</script>

<style scoped>
.card {
  background-color: #fff;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 10px;
  margin-bottom: 20px;
}
</style>