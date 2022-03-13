<template>
    <div @click="addCard" class="rounded-sm p-2 text-gray-600 cursor-pointer hover:bg-gray-400 hover:text-gray-800 text-sm">Add a New Card</div>
</template>
<script>
import CardAdd from "./../graphql/CardAdd.gql";
export default {
    methods: {
        addCard() {
            this.$apollo.mutate({
                mutation: CardAdd,
                variables: { title: "aaafff", listId: 1, order: 1 }
            });
        }
    }
}
</script>