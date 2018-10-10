# jsinteractive2018-notes
notes from jsinteractive 2018

## About this repo
This is a collection of notes from jsinteractive 2018 using a tool called
hackerslides. 

* More info: https://github.com/msoedov/hacker-slides
* hacker-slides info: https://hackmd.io/s/slide-example#First-slide
* github markdown doc:
* https://help.github.com/articles/basic-writing-and-formatting-syntax/#quoting-text
* reveal.js docs: https://github.com/hakimel/reveal.js/
* useful markdwon snippets:
https://raw.githubusercontent.com/jeffcole/well-designed-phoenix-apps-talk/master/PITCHME.md

## run slides locally
```
docker run -it -p 8081:8080 -v $(pwd)/slides:/app/slides msoedov/hacker-slides
```

## run docs locally
building
```
 docker build -t jsinteractive2018-notes:latest .
```

run local
```
docker run -it --rm -p 4000:4000 --name jsinteractive2018-notes -v "$PWD":/usr/src/app -w /usr/src/app jsinteractive2018-notes:latest
```
or background
```
docker run -t -d --rm -p 4000:4000 -h localhost --name jsinteractive2018-notes -v "$PWD":/usr/src/app -w /usr/src/app jsinteractive2018-notes:latest
```

run locally without building (slower starts)
```
docker run -it --rm -p 4000:4000 --name jsinteractive2018-notes -v "$PWD":/usr/src/jsinteractive2018-notes -w /usr/src/jsinteractive2018-notes ruby:2.5 bundle install && bundle exec jekyll serve
```

