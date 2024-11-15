<template>
    <div class="header-container">
      <div class="logo-section">
        <a><img src="@/assets/logo_white.png" class="logo"></a>
      </div>
  
      <div class="nav-links">
        <a>Inicio</a>
        <a>Servicios</a>
        <a>Cursos</a>
        <a>Certificaciones</a>
        <a>Empresa</a>
      </div>
          
      <div class="icons-section">
        <a>
          <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 512 512">
            <path fill="#dedcd9" d="M258.9 48C141.92 46.42 46.42 141.92 48 258.9c1.56 112.19 92.91 203.54 205.1 205.1c117 1.6 212.48-93.9 210.88-210.88C462.44 140.91 371.09 49.56 258.9 48m126.42 327.25a4 4 0 0 1-6.14-.32a124.3 124.3 0 0 0-32.35-29.59C321.37 329 289.11 320 256 320s-65.37 9-90.83 25.34a124.2 124.2 0 0 0-32.35 29.58a4 4 0 0 1-6.14.32A175.32 175.32 0 0 1 80 259c-1.63-97.31 78.22-178.76 175.57-179S432 158.81 432 256a175.32 175.32 0 0 1-46.68 119.25"/>
            <path fill="#dedcd9" d="M256 144c-19.72 0-37.55 7.39-50.22 20.82s-19 32-17.57 51.93C191.11 256 221.52 288 256 288s64.83-32 67.79-71.24c1.48-19.74-4.8-38.14-17.68-51.82C293.39 151.44 275.59 144 256 144"/>
          </svg>
        </a>
        <a>
          <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 64 64">
            <path fill="#dedcd9" d="M61.063 2H58.25v.896c-3.916.876-4.479 4.511-4.7 5.9c-.105.657-.318 1.942-.582 3.516H3.988c-1.938 0-2.155 1.811-1.902 2.813l5.746 25.367c.252 1.002 1.313 1.82 2.353 1.82h42.944c1.034 0 1.877.841 1.877 1.875s-.843 1.875-1.877 1.875H6.255a1.874 1.874 0 1 0 0 3.75h2.43a7.5 7.5 0 0 0-3.872 6.563h1.875c0 3.105 2.52 5.625 5.625 5.625s5.625-2.52 5.625-5.625h1.875a7.5 7.5 0 0 0-3.873-6.563h26.494a7.5 7.5 0 0 0-3.873 6.563h1.875a5.627 5.627 0 0 0 11.252 0h1.875a7.5 7.5 0 0 0-3.872-6.563h3.44a5.63 5.63 0 0 0 5.625-5.625a5.626 5.626 0 0 0-5.627-5.625h-.697l2.398-14.91c.668-3.938 2.108-12.445 2.446-14.561c.17-1.069.335-1.82.974-2.241v.774h2.813A.94.94 0 0 0 62 6.688v-3.75A.94.94 0 0 0 61.063 2"/>
          </svg>
        </a>
      </div>
    </div>
</template>
  
<script>
export default {
  name: "NavbarComponent",
};
</script>

  
<style>
    body, html {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
  
    .header-container {
      width: 100vw;
      height: 130px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: #332f66;
    }
  
    .logo-section {
      width: 30%;
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: flex-start;
      padding-left: 80px;
    }
  
    .logo {
      width: 50%;
    }
  
    .nav-links {
      width: 50%;
      display: flex;
      justify-content: space-between;
      gap: 4px;
      color: beige;
    }
  
    .nav-links a {
      color: beige;
      font-size: 20px;
      text-decoration: none;
    }
  
    .icons-section {
      width: 20%;
      display: flex;
      justify-content: flex-end;
      gap: 20px;
      color: beige;
      padding-right: 90px;
    }
</style>