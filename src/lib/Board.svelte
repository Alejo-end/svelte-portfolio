<script lang="ts">
	import Welcome from './Welcome.svelte';

</script>

<div class="board">
    <!-- <img class="logo" src={logoADL} alt="Logo" /> -->
    <Welcome/>
</div>

<style lang="scss">
.board{
    position: relative;
    background-color: #f7f7f7;
    border: 4px solid #333333;
    padding: 40px;
    transition: 1s;
    transition-delay: 0.1s;
    box-shadow: 7px 7px #333333;
    width: 60%;
    &:hover {
        transform: skew(-3deg);
    }
}


</style>
