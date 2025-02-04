[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=17755789)
create a file in componentsanimal card
then use vbase then remove the csss
g to home view and add
const animas = [{name: "Walrus", image:"/walrus.webp"}
[name:"MarkFridlan", image:"/capy.jpg"],];
go back to animal card
and type definProps({
animal: Object,
});
in script setup

then in div add

<h2>{{animal.name}}</h2>
<img:src="animal.image" alt""/>
back in homeviewS
add import AnimalCard from "../components/AnimalCard..vue"
Then in template main
add <AnimalCard v-for="animal in animals" : key="animal.name" :animal= "animal/>
