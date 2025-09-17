<template>
  <NewFriend @newFriend="addFriend" />

  <div v-for="Amis in lesAmis" :key="Amis.id">
    <List
      :id="Amis.id"
      :name="Amis.name"
      :phone="Amis.phone"
      :email="Amis.email"
      :premium="Amis.premium"
      @delete="deleteFriend"
      @change="changePremium"
    />
  </div>
</template>

<script setup>
import List from "~/components/exercices/List.vue";
import NewFriend from "~/components/exercices/NewFriend.vue";

const lesAmis = ref([
  {
    id: "lasticot",
    name: "COCO L ASTICOT",
    phone: "01234 5678 991",
    email: "coco@lasticot.com",
    premium: true,
  },
  {
    id: "lasticot2",
    name: "COCO L ASTICOT",
    phone: "01234 5678 991",
    email: "coco@lasticot.com",
    premium: true,
  },
  {
    id: "kimonoSurUnFrigo",
    name: "Steven Seagal",
    phone: "+338765477",
    email: "steven@seagal.com",
    premium: true,
  },
  {
    id: "yoyoyo",
    name: "JAROD",
    phone: "+338765477",
    email: "jAROD@seagal.com",
    premium: true,
  },
]);

function deleteFriend(id) {
  lesAmis.value = lesAmis.value.filter((a) => a.id !== id);
}

function changePremium(id) {
  const ami = lesAmis.value.find((a) => a.id === id);
  if (ami) ami.premium = !ami.premium;
}

function addFriend(ami) {
  lesAmis.value.push(ami);
}
</script>
