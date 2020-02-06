1) What does using the key attribute with the v-for directive bring us? Positive or negative results?

> <!-- BAD -->
> <div v-for='product in products'>  </div>
>
> <!-- GOOD! -->
> <div v-for='product in products' :key='product.id'>

<h2>ANSWER</h2>

<p> Using the key attribute with the v-for directive helps your application be constant and predictable whenever you want to manipulate the data.
This is necessary so Vue can track your component state as well as have a constant reference to your different elements. An example where keys are extremely useful is when using animations or Vue transitions.
Without keys, Vue will just try to make the DOM as efficient as possible. This may mean elements in the v-for may appear out of order, or their behavior will be less predictable. If we have a unique key reference to each element, then we can better predict how exactly our Vue application will handle DOM manipulation. </p>

2) How should we format the custom events? Kebab-case or CamelCase? How does VUE handle that?

> this.$emit('close-window')
> // then in the parent
> <popup-window @close-window='handleEvent()' />

<h2>ANSWER</h2>
<p>
When it comes to emitting custom events, it’s always best to use kebab case. This is because in the parent component, that’s the same syntax we use to listen to that event.
So for consistency across our components, and to make your code more readable, stick to using kebab case in both places.
</p>

