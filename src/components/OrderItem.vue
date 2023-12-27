<template>
<img src='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR2vqs61_Mp97NlD-qtZZdBLk4xV0qHbdVwDn7BvRyLfciQDR64xa7BwR5ZRqPIWj5-8NQ&usqp=CAU' alt='picture'>
<div>
<h2>{{ msg }}</h2>
<p>{{ msg }}</p>
<div>UAH {{ msg }} <span>за ночь</span></div>
</div>
</template>

<script>
export default {
  name: 'OrderItem',
  props: {
    msg: String
  }
}
</script>