<div class="header">
    <input type="text" class="main" placeholder="Search">
    <div class="menu"><img src="/menu.png" alt="menu" /></div>
 </div>
 
 <style lang="scss">
     .header {
         display: flex;
         align-items: center;
         width: calc(100% - 24px);
         margin: 12px;
     }
     
     .header > .main {
         background-color: #94d2bd;
         color: #ffffff;
         height: 48px;
         flex-grow: 1; 
         margin-right: 8px; 
         border-radius: 0.25rem;
         border: none;
         padding: 0 12px;
         outline: none;
     }
 
     .header > .menu {
         display: flex;
         align-items: center;
         justify-content: center;
         background-color: #94d2bd;
         height: 48px;
         width: 48px;
         border-radius: 0.25rem;
         font-size: 32px;
         cursor: pointer;
     }

     .header > .menu > img {
        width: 32px;
        height: 32px;
     }
 </style>
 