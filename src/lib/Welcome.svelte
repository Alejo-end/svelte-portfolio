
<div class="text">
    <h2>Alejandro De León</h2>
    <h3>Welcome to my Portfolio.</h3>
    <p>
        I am a Web Designer, Software Engineer and Open Data Enthusiast.
    </p>
    <div><a href="/projects" class="link-a">View Projects</a></div>
</div>

<style lang="scss">
.text{
  position: relative;
  padding: 0.8em;


  & > h2 {
    font-size: 4.5em;
    font-weight: 300;
    color: #333333;
    line-height: 1em;
    text-transform: uppercase;
    transition: 0.5s;
    margin: 0.25em auto;
    &:hover{
        transform: skew(-15deg); 
    }
}



    & > h3 {
        font-size: 2.5em;
        font-weight: 500;
        color: #333333;
        line-height: 1em;
        text-transform: uppercase;
        margin-top: 20px;
    }
    & > p {
        font-size: 1.5em;
        color: #333333;
        margin: 20px 0;
        font-weight: 400;
        max-width: 700px;
    }
    & > div {
        display: inline-block;
        font-size: 1em;
        background: #333333;
        padding: 10px 20px;
        text-transform: uppercase;
        text-decoration: none;
        font-weight: 500;
        margin-top: 10px;
        color: #f7f7f7;
        letter-spacing: 2px;
        transition: 0.2s;
        cursor: pointer;
    }
    & > div:hover {
        letter-spacing: 5px;
        animation: colorRotate 2s linear 0s infinite;
        box-shadow: 5px 5px #333333;
    }
}
.link-a{
        text-decoration: none;
        color: white;
}
@media (max-width: 480px) {
    .text{ 
        margin-top: 1.25em;
        & > h2{
        font-size: 3em;
        }
        & > h3{
        font-size: 1.8em;
        }
        & > p{
        font-size: 1.25em;
        }

    }
}
</style>
