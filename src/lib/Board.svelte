<script lang="ts">
export let width;

</script>

<div class="board" style="width: {width}">
    <!-- <img class="logo" src={logoADL} alt="Logo" /> -->
    <slot>

    </slot>
</div>

<style lang="scss">
.board{
    position: relative;
    background-color: #f7f7f7;
    border: 5px solid #333333;
    padding: 20px;
    transition: 1s;
    transition-delay: 0.1s;
    &:hover {
    box-shadow: 10px 10px #333333;
  }
}
@media (max-width: 480px){
    .board{
    width: auto;
    }
}
</style>
