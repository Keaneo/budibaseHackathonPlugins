<script>
  import { getContext } from "svelte"
  import { slide } from "svelte/types/runtime/transition";

  export let sliderVal = 0
  export let min
  export let max
  export let step
  //let sliderVal = 0

  const { styleable } = getContext("sdk")
  const component = getContext("component")
</script>

<div use:styleable={$component.styles}>
  The slider is set to: {sliderVal}.
  <input type="range"
  value={sliderVal}   
  min={min}
  max={max} 
  step={step}
  on:input={(value) => sliderVal}
  />
</div>
