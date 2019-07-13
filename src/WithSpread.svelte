<div
  class={allClasses}
  class:reverse
  {...attributes}
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
        const defaultClasses = ['with-spread'];

        return defaultClasses.concat(classes).join(' ');
      }
    }
  }
</script>