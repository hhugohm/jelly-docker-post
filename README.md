# jelly-docker-post
jelly-docker-post
------------------------------
running-jekyll-in-docker
-----------------------------
- JEKYLL_VERSION=3.8
- https://ddewaele.github.io/running-jekyll-in-docker/
- https://github.com/envygeeks/jekyll-docker/blob/master/README.md
- https://hub.docker.com/r/jekyll/jekyll

1 $ mkdir /jelly/site

2 $ cd /jelly/site

3 $ docker run --rm --volume="$PWD:/srv/jekyll" -it jekyll/jekyll:3.8 jekyll new .

4 $ docker run --rm --volume="$PWD:/srv/jekyll" -it jekyll/jekyll:3.8 jekyll build

5 $ docker run --name myjellyblog --volume="$PWD:/srv/jekyll" -p 3000:4000 -it jekyll/jekyll:3.8 jekyll serve --watch --drafts

6 $ touch 2020-07-05-my-first-post.md
---
layout: post
title:  "Bienvenidos a Jekyll!"
---

# Bienvenido

**Hola Mundo**, Este es el primer blog post usando Jekyll!!!.

Espero que te guste!!!!

7 - Execute http://localhost:3000/

- $ docker commit  fc2cf38e8561 myjellyblog
- $ docker image tag myjellyblog hhugohm/jelly-blog:1.0.0
- $ docker push hhugohm/jelly-blog:1.0.0
- download https://github.com/hhugohm/jelly-docker-post

- $ docker run --name myjellyblog --volume="$PWD:/srv/jekyll" -p 3000:4000 -it  hhugohm/jelly-blog:1.0.0  jekyll serve --watch --drafts

