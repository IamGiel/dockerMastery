<h1><b>Learning Docker in Depth</b></h1>
<h2>Deep-dive into docker</h2>

<hr>
<h2><u>Image Vs Container</u></h2>
<ul>
    <li>
        <h3>Image is the application we want to run</h3>
    </li>
    <li>
        <h3>Container is the running instance of that image.</h3>
    </li>
</ul>

<br>
<hr>
<h2><u>Docker Commands</u></h2>

<div>docker container run --publish 80:80 nginx</div>
<div>docker container run --publish 80:80 --detach nginx (keeps container running in the background, provides unique id printed in the console)</div>
<div>docker container ls (lists all containers)</div>
<div>docker container stop 3432... (first few numbers of the id, stops the container from running)</div>
