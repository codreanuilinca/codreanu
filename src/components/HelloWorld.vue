<!-- <template>
  <div>
    <h1>Hello, World!</h1>

    <h2>{{ counter }}</h2>

    <button @click="increase">+1</button>
    <button @click="decrease">-1</button>
  </div>
</template>

<script setup>
import { onMounted, ref, onUpdated, computed ,watch} from 'vue'

const counter = ref(0);

const increase = () => {
    const result = computed ( ) => {
        return 'Counter New value : >>>' + counter,value
    }
    watch (counter ,() =>{
     consule 'Counter New value : >>>", COUNTE)
    }
  counter.value += 1
}

const decrease = () => {
  counter.value -= 1
}

onMounted(() => {
  console.log('Componentul a fost montat')
})

onUpdated(() => {
  console.log('Re rerender')
})
</script>

<style scoped></style> -->
