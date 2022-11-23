# How to build 

I use texlive/texlive:latest image from docker hub to build the resume. 

If you don't have the container on your machine run 

``` bash
docker run -it --mount type=bind,source="$(PWD)",target=/home texlive/texlive:latest
```

If you have a texlive container: 

Run the start command to start the container. 
``` bash 
docker start <container name> 
```

Run exec to get into the shell 

``` bash
docker exec -it texresume bin/bash
```

Once in the shell run: 

``` bash
cd home 
xelatex resume_cv.tex 
```

