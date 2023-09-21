<div class="header">
    <div class="main">
        <img src="/logo.png" alt="Logo" class="logo">
        <input type="text" class="main" placeholder="Search">
    </div> 
    <div class="menu">
        <img src="/menu.png" alt="menu" />
    </div>
</div>
 
 <style lang="scss">
    .header {
        display: flex;
        align-items: center;
        justify-content: center;
        width: calc(100% - 24px);
        margin: 12px auto;
        gap: 2px; 
    }

    .header > .main {
        display: flex;
        align-items: center;
        background-color: #94d2bd;
        height: 48px;
        padding: 0 12px;
        border-radius: 0.25rem;
        flex-grow: 1; 
    }

    .logo {
        height: 40px;
        margin-right: 10px;
    }

    .header > .main > input {
        flex-grow: 1; 
        height: 32px;
        border: none; 
        border-radius: 0.25rem;
        padding-left: 8px; 
        background-color: #94d2bd;
        outline: none; 
        color: #333
    }

    .header > .main > input::placeholder {
        color: rgba(255, 255, 255, 0.8); 
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
    }

    .header > .menu > img {
        width: 32px;
        height: 32px;
    }
 </style>
 