<nav>
    <div class="logo">
        <img src="static/logoADL.svg" alt="logo"/>
    </div>
    <div class="options">    
        <a href="/">Home</a>
        <a href="/about">About Me</a>
        <a href="/projects">Projects</a>
        <a href="/contact">Contact</a>
    </div>
</nav>

<style lang="scss">
    nav {
        margin-bottom: 7rem;
    }
    .logo{
        float: left;
    }
    .options {
        float: right;
    }
    a {
        text-decoration: none;
        font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif, sans-serif;
        font-size: larger;
        display: inline-block;
        border: 2px solid #333333;
        font-size: 1em;
        background: #333333;
        padding: 10px 20px;
        text-decoration: none;
        margin-left: 10px;
        color: #f7f7f7;
        letter-spacing: 1px;
        transition: 0.2s;
        cursor: pointer;
        &:hover {
            animation: colorRotate 2s linear 0s infinite;
            box-shadow: 3px 3px #333333;
        }
    }

</style>