<script lang="ts">
    import classNames from 'classnames';
    import { afterUpdate, getContext } from 'svelte';
  
    export let href: string = '';
    export let active: boolean = false;
    export let data: string = '';
  
 

    afterUpdate(() => {
        console.log(`${data} updated, active: ${active}`);
    });


  </script>


  
  <li>
    <svelte:element
      this={href ? 'a' : 'div'}
      {href}
   
      >
      <slot />
    </svelte:element>
  </li>