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
<div><u>docker ps</u> ( same as above - lists all containers)</div>
<div><u>docker top nameOfContainer</u> (pid)</div>
<div><u>docker container stop 3432...</u> (first few numbers of the id, stops the container from running)</div>
<div><u>docker container run --publish 80:80 --detach --name alphagiel nginx</u> (name your container)</div>
<div><u>docker container logs alphagiel</u> (logs)</div>
<div><u>docker container rm 123... </u> (delete/remove a container, but will not delete a running container)</div>
<div><u>docker container rm -f 268... </u> (-forces delete/remove a container)</div>
<div><u>ps aux | grep nameOfwhatYouWantTofilter </u> (filters a name)</div>

<br>
<hr>
<h2><u>What Happens when a docker container runs?</u></h2>

<ul>
    <li>
        <h3>It looks for the image that we want to run locally in image cache, doesnt find anything...</h3>
    </li>
    <li>
        <h3>Then looks at remote page repository ( by default: docker hub )</h3>
    </li>
    <li>
        <h3>downloads latest version</h3>
    </li>
    <li>
        <h3>Creates new container base on that image and prepares to start</h3>
    </li>
    <li>
        <h3>Gives it a virtual IP on a private network inside docker engine</h3>
    </li>
    <li>
        <h3>Runs on a port that we specify (port 80 on localhost and port 80 on container)</h3>
    </li>
    <li>
        <h3>Starts container by using the CMD in the image Dockerfile</h3>
        <u>docker container run --publish 80:80 --name alphagiel -d nginx</u>
    </li>
</ul>

<br>
<hr>
<h2><u>Activity Commands running images with multiple containers</u></h2>

<ul>
    <li>
        <h3>running mysql</h3>
        <h3><u>docker run --name alpha-giel -e MYSQL_ROOT_PASSWORD=yourPassword -d mysql</u></h3>
    </li>
</ul>
<ul>
    <li>
        <h3>running nginx</h3>
        <h3><u>docker container run --publish 80:80 --detach --name alphagiel nginx</u></h3>
    </li>
</ul>
