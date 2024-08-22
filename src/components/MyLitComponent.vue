<template>
  <div ref="litComponentContainer"></div>
</template>

<script lang="ts">
import { defineComponent, onMounted, ref, watch } from 'vue'
import * as COE from 'coe-comp-lib'

export default defineComponent({
  name: 'MyLitComponent',
  props: {
    componentType: {
      type: String,
      required: true
    },
    name: {
      type: String,
      default: 'World'
    },
    counter: {
      type: Number,
      default: 5
    }
  },
  setup(props) {
    const litComponentContainer = ref<HTMLElement | null>(null)

    onMounted(() => {
      const componentMap: { [key: string]: string } = {
        'coe-sidemenu': 'coe-sidemenu',
        'coe-card': 'coe-card'
      }

      const componentTag = componentMap[props.componentType]
      if (componentTag) {
        const litComponent = document.createElement(componentTag)

        if (props.componentType === 'coe-card') {
          litComponent.name = props.name
          litComponent.counter = props.counter
        }

        litComponentContainer.value?.appendChild(litComponent)
      }
    })

    // Update Lit component properties if props change
    watch(
      () => props.name,
      (newValue) => {
        const currentComponent = litComponentContainer.value?.firstChild
        if (currentComponent) {
          ;(currentComponent as HTMLElement).name = newValue
        }
      }
    )

    return {
      litComponentContainer
    }
  }
})
</script>

<style scoped>
/* Add any styles you need for your wrapper component */
</style>
