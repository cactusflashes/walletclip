<title>walletclip</title>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400;1,700&display=swap');
  body {
    margin: 0;
    padding: 0;
    overflow: hidden;
  }

  .container {
    display: flex;
    background-color: #f0f0f0;
    height: 100vh;
    width: 100vw;
    align-items: center;
    justify-content: center;
  }

  .card {
    perspective: 500px;
  }

  .content {
    display: flex;
    align-items: center;
    justify-content: center;

  }

  .front, 
  .back {
      display: flex;
      flex-direction: column;
      height: 20vw;
      width: 35vw;
      background-color: white;
      backface-visibility: hidden;
      border-radius: 10px;
      transition: transform 0.8s; 
      position: absolute;
      align-self: center;
      box-shadow: 0 0 15px rgba(0,0,0,.1);
      min-width: 380px;
      max-width: 380px;
      min-height: 250px;
      max-height: 250px;
  }

  .back {
    transform: rotateY(180deg);
  }

  h1 {
    font-family: Space Mono;
    font-weight: 300;
    margin: 0;
    font-size: 2rem;
  }

  h2 {
    font-family: Space Mono;
    font-weight: 500;
    margin: 0;
    font-size: 1.5rem;
  }

  h3 {
    font-family: Space Mono;
    font-weight: 100;
    margin: 0;
    font-size: 1rem;
  }

  .card:hover .front {
    transform: rotateY(180deg);
    cursor: alias;
  }

  .card:hover .back {
    transform: rotateY(0);
    cursor: alias;

  }

  .front-align {
    margin-top: 10%;
    margin-left: 10%;
  }

  .profile {
    display: flex;
    max-width: 40%; 
    align-self: center;
    margin-top: 10%;
  }

</style>

<script>
  import profile from '$lib/pro.png'
</script>

<body>

  <div class="container">

    <div class="card">
      <div class="content">


        <div class="front">
          <div class="front-align">
            <h1>Joseph Salmón</h1>  
            <h2>Front-End Engineer</h2>
            <h3>airefrescodesign@gmail.com</h3>
            <h3>928.821.9183</h3>
          </div>
        </div>

        <div class="back">
            <!-- svelte-ignore a11y-missing-attribute -->
            <img src={profile} class="profile"/>
        </div>
        
      </div>
    </div>

  </div>

</body>
