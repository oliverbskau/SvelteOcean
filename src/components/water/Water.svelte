<script>
import Shark from "../../pages/shark/Shark.svelte";
import Boat from "../../pages/boat/Boat.svelte"
</script>



<div id="waterDiv">
    <Shark/>
    <Boat/>
</div>


<style>
    #waterDiv{
        background-color: aqua;
        width: max-width;
        height: 300px;
        margin: 0px;
        padding: 2px;
        position: relative;
        bottom: 300px;
        
    }
</style>