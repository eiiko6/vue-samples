<template>
    <div class="navbar">
    <nav>
      <ul>
        <li class="pfp"><a href="#"><img src="./assets/Customer.png" alt="Pfp"></a></li>
        <div class="separator"></div>
        <li><router-link class="lk" to="/LyphDraw-portfolio/"><img src="./assets/icons8_home_1.ico" alt="Home"></router-link></li>
        <li class="b"><router-link class="lk" to=""><img src="./assets/icons8_large_icons.ico" alt="Artworks"></router-link></li>
        <li class="b"><router-link class="lk" to=""><img src="./assets/icons8_linking_1.ico" alt="Links"></router-link></li>
        <li class="b"><router-link class="lk" to=""><img src="./assets/icons8_categorize_5.ico" alt="Misc"></router-link></li>
      </ul>
    </nav>
</div>
</template>

<style scoped>
  .navbar {
    z-index: 2;
    user-select: none;
    position: fixed;
    top: 0;
    left: 0;
    height: 100%;
    width: 100px;
    background-color: #00000023;
    color: #fff;
    padding: 10px;
    display: flex;
    flex-direction: column;
    border-right: 2px solid #ffffff80;
    /*justify-content: center;*/
  }

  .lk.router-link-active img {
    opacity: .6;
    transform: scale(1.3);
  }

  .navbar::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    backdrop-filter: blur(15px);
    opacity: 0.8;
    z-index: -1;
    background-color: #00000023;
  }

  .navbar nav ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100%;
    left: 0;
  }

  .navbar nav ul li {
    margin-top: 25px;
    margin-bottom: 25px;
  }

  .navbar nav a {
    color: #fff;
    text-decoration: none;
    padding: 10px 10px;
    border-radius: 2px;
    margin: 5px;
    transform: translateZ(0);
    -webkit-tap-highlight-color: transparent;
    left: 0;
  }

  .navbar img {
    width: 45px;
    transition: 0.1s ease-out;
    left: 0;
  }

  .navbar a:hover img {
    color: #333;
    transform: scale(1.3) translateZ(0);
  }

  .navbar a:active img {
    transform: scale(1.15) translateZ(0);
  }

  .separator {
    background-color: #ffffffab;
    width: 30px;
    height: 3px;
    border-radius: 2px;
    margin: 20px;
  }

  @media screen and (max-width: 730px) {
    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 70px;
      flex-direction: row;
      justify-content: space-around;
      padding: 10px 0;
      border-right: none;
      border-bottom: 2px solid #ffffff80;
    }
    
    .navbar nav ul {
      flex-direction: row;
    }
    
    .navbar nav li {
      margin: 15px;
    }
    
    .separator {
      width: 3px;
      height: 30px;
      border-radius: 2px;
      margin-left: 5px;
      margin-right: 20px;
    }
  }

  @media screen and (max-width: 400px) {
    .pfp {
      display: none;
    }

    .separator {
      display: none;
    }
  }

  .navbar * {
    transition: .1s ease-out;
  }
</style>
