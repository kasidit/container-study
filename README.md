<h1>Tutorial: docker แบบง่ายๆ</h1>
<p><p>
<h2>1. ติดตั้ง docker บน ubuntu 16.04 </h2>
<p><p>
เรา assume ว่า host ใช้ ubuntu 16.04 ที่มี FS แบบ ext4
<p><p>
<pre>
$ sudo sed -i "s/us.arch/th.arch/g" /etc/apt/sources.list
$ sudo apt-get update
$ sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
</pre>
<pre>
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
</pre>
ตรวจสอบ key
<pre>
$ sudo apt-key fingerprint 0EBFCD88
pub   4096R/0EBFCD88 2017-02-22
      Key fingerprint = 9DC8 5822 9FC7 DD38 854A  E2D8 8D81 803C 0EBF CD88
uid                  Docker Release (CE deb) <docker@docker.com>
sub   4096R/F273FCD8 2017-02-22
$
</pre>
<pre>
$ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
$
$ sudo apt-get update
$ sudo apt-get install docker-ce
$
</pre>
ตรวจสอบว่า ติดตั้งถูกต้องด้วยการรัน hello world
<pre>
$ sudo docker run hello-world
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
ca4f61b1923c: Pull complete
Digest: sha256:be0cd392e45be79ffeffa6b05338b98ebb16c87b255f48e297ec7f98e123905c
Status: Downloaded newer image for hello-world:latest
Hello from Docker!
This message shows that your installation appears to be working correctly.
To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.
To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash
Share images, automate workflows, and more with a free Docker ID:
 https://cloud.docker.com/
For more examples and ideas, visit:
 https://docs.docker.com/engine/userguide/
$
</pre>
ในกรณีที่ นศ จะ uninstall docker ให้ใช้คำสั่ง
<pre>
$ sudo apt-get purge docker-ce
$ sudo rm -rf /var/lib/docker
</pre>
<p><p>
<h2>2. การโหลดและรัน image จาก repository</h2>
<p><p>
<p><p>
<h2>3. คำสั่ง docker CLI</h2>
<p><p>
<p><p>
<h2>4. docker hub</h2>
<p><p>
<p><p>
<h2>5. การ publish image ใหม่</h2>
<p><p>  
