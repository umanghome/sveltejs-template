<div
  class={allClasses}
  class:reverse
>
  <slot></slot>
</div>

<script>
  export default {
    data: () => ({
      classes: [],
      reverse: false,
    }),

    computed: {
      allClasses: ({ classes }) => {
        const defaultClasses = ['without-spread'];

        return defaultClasses.concat(classes).join(' ');
      }
    }
  }
</script>