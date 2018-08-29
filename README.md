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

<div><u>docker container run --publish 80:80 nginx</u></div>
<div><u>docker container run --publish 80:80 --detach nginx</u> (keeps container running in the background, provides unique id printed in the console)</div>
<div><u>docker container ls</u> (lists all containers)</div>
<div><u>docker container stop 3432...</u> (first few numbers of the id, stops the container from running)</div>
<div><u>docker container run --publish 80:80 --detach --name alphagiel nginx</u> (name your container)</div>
<div><u>docker container logs alphagiel</u> (logs)</div>
<div><u>docker container rm 123... </u> (delete/remove a container, but will not delete a running container)</div>
<div><u>docker container rm -f 268... </u> (-forces delete/remove a container)</div>
