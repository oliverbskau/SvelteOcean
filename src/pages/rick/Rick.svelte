


<script>
      
     function myTimer(){ 
      
        let timeleft = 8;
      const timerElement = document.getElementById('clock');
        const downloadTimer = setInterval(function () {
          document.getElementById("return").hidden = true;
          document.getElementById("clockDiv").hidden = false;
        if (timeleft <= 0) {
          clearInterval(downloadTimer);
          timerElement.innerHTML = "Finished";
          window.location.href =  "";
        } else {
          timerElement.innerHTML = timeleft + " seconds remaining";
          const randomColor = Math.floor(Math.random() * 16777215).toString(16); //found this line on google
          document.body.style.backgroundColor = "#" + randomColor;
        }
        timeleft -= 1;
      }, 1000);

    }
</script>


<img src="https://c.tenor.com/x8v1oNUOmg4AAAAd/rickroll-roll.gif" alt="rick">
<h3>You sadly got rick-rolled</h3>

<button id="return" on:click={myTimer}>Return</button>

<div id="clockDiv" hidden>
  <p id="clock"></p>
</div>


<style>
    #clock{
        margin: auto;
        width: 50%;
        height: 50%;
        text-align: center;
        font-size: 30px;
        font-family: fantasy;
    }
   
</style>