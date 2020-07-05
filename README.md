# jelly-docker-post
jelly-docker-post

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

