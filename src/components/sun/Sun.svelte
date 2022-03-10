
<script>

let dayAmount = 1;

function changeToDay(){
    document.getElementById('sun').hidden = false;
    document.getElementById('moon').hidden = true;
    document.body.style.backgroundColor = "lightblue";
    document.getElementById("waterDiv").style.backgroundColor = "aqua";
    document.getElementById('boatGif').hidden = false;
    document.getElementById('sharkGif').hidden = true;
    document.getElementById("day").style.color = "black";
    dayAmount += 1;
    if(dayAmount > 2){
    document.getElementById("content").hidden = true;
    document.getElementById("rick").hidden = false;
}

}
function changeToNight(){
    document.getElementById('sun').hidden = true;
    document.getElementById('moon').hidden = false;
    document.body.style.backgroundColor = "black";
    document.getElementById("waterDiv").style.backgroundColor = "#212E52";
    document.getElementById('boatGif').hidden = true;
    document.getElementById('sharkGif').hidden = false;
    document.getElementById("day").style.color = "white";
}


</script>

<h1 id="sun">☀️</h1>
<h1 id="moon" hidden>🌑</h1>


<h2 id="day">Day {dayAmount}</h2>
<div id="changeDiv">
    <button on:click={changeToDay} id="toDay">Day</button>
    <button on:click={changeToNight} id="night">Night</button>
</div>




<style>
    h1{
        font-size: 300px;
        margin: none;
    }
    h2{
        font-size: 50px;
    }

    #changeDiv, #day{
        position: relative;
        bottom: 850px;
    }

    #sun, #moon{
        position: relative;
        bottom: 400px;
    }

    #day{
        position: relative;
        bottom: 810px;
    }

    
</style>