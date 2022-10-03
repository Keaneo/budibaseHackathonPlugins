<script language="typescript">
  import { getContext, onMount } from "svelte"
  import {renderGif} from '@giphy/js-components'
  import {GiphyFetch} from '@giphy/js-fetch-api'

  const gf = new GiphyFetch('yYwIq1b7rUl53tHKIS7eECJ4BXnfVGkB')
  const { styleable } = getContext("sdk")
  const component = getContext("component")

  export let searchGif = "fpXxIjftmkk9y"

  let main
  const vanillaJSGif = async (mountNode) => {
    // render a single gif
    const { data: gif1 } = await gf.gif(searchGif)
    renderGif({ gif: gif1, width: 300 }, mountNode)
}
onMount(() => {
  vanillaJSGif(main);
})

$: searchGif,vanillaJSGif(main)
</script>

<div use:styleable={$component.styles}>
  <div bind:this={main}>
    
  </div>
</div>
