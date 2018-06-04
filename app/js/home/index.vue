<template lang="html">
    <div>
        <Heador/>
        <Hslilder/>
        <Borrow/> 
        <Novice/> 
        <Money/>
        <Porduct/>
    </div>
</template>

<script>
import Heador from '../public/header.vue'
import Hslilder from './hslilder'
import Novice from './novice'
import Borrow from './borrow'
import Money from './money'
import Porduct from './product'
export default {
  components: {
    Heador,
    Hslilder,
    Novice,
    Borrow,
    Money,
    Porduct
  }
}
</script>
