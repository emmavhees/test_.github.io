<!-- <style>
    .custom-font {
        /* font-family: Georgia, serif; */
        color: #f5d3e9;
    }
    .container {
        display: flex;
    }
    .column {
    flex: 33.33%;
    padding: 10px;
  }
</style> -->
<style>
  .container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
  .column {
    background-color: #FFFFFF;
    padding: 10px;
    margin: 5px;
    flex: 1;
    min-width: 250px; /* Minimum width to ensure columns stack on smaller screens */
  }
  .column img {
    width: 100%;
    max-width: 100%;
    height: auto;
  }
  @media (max-width: 768px) {
    .column {
      flex-basis: 100%;
    }
  }
</style>

# Personal Projects

In my spare time I love working on the following things: 
 <!-- style="text-align: center;" -->

<div class="container">
    <div class="column" style="background-color:#FFFFFF;">
        <h3> Making Sourdough Bread </h3>
        <img src="..\images\sourdough.png" alt="Emma" style="width: 100%; max-width: 100%;" />
    </div>
    <div class="column" style="background-color:#FFFFFF;">
    <h3> Crochet & Knitting </h3>
        <img src="..\images\crochet.png" alt="Emma" style="width: 100%; max-width: 100%;" />
    </div>
    <div class="column" style="background-color:#FFFFFF;">
    <h3> Improving Wintersport Abilities </h3>
        <img src="..\images\wintersport.png" alt="Emma" style="width: 100%; max-width: 100%;" />
    </div>
</div>


<!-- <a href="../index.md">Back to main page </a> -->