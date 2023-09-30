
<script>
    import { onMount, onDestroy } from 'svelte';
  
    let typed;
  
    onMount(() => {
      const Typed = require('typed.js');
      typed = new Typed('.typing', {
        strings: [
          'I like <b>Html</b>',
          'I love <b>JavaScript</b>',
          'I am <b>Web Developer</b>',
        ],
        typeSpeed: 50,
        backSpeed: 50,
        loop: true,
      });
    });
  
    onDestroy(() => {
      // Clean up and destroy the Typed instance when the component is unmounted
      typed.destroy();
    });
  </script>
  
  <style>
    .typing {
      font-size: 1.25rem;
      color: #fff;
    }
  </style>
  
  <div class="typing"></div>