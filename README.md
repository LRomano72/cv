# cv

My resumé in LaTeX.

## Compiling

### 1. Using `soleo/latex`

1. LaTeX compiling is done via the [`soleo/latex`](https://github.com/soleo/docker-latex) Docker image (~ 4GB). Pull it first: `docker pull soleo/latex`
2. Define helper function `docker-latex`: `docker-latex() { docker run -v $PWD:/mnt/src --rm  soleo/latex:latest ​$@; return $?; }`
3. `docker-latex example.tex`. This will create `example.pdf`

### 2. Using Visual Studio Code

1. Install [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) extension
2. In Settings, set `latex-workshop.docker.enabled` to `true`
3. LaTeX Workshop uses the [`tianon/latex`](https://github.com/tianon/dockerfiles/blob/master/latex/Dockerfile) Docker image (~ 3GB) by default. Pull it first: `docker pull tianon/latex`
4. Open an editor for `example.tex`, make a change and Save. The LaTeX will be compiled to `example.pdf`. Select "View LaTeX PDF file" on the top-right to have a live PDF view of changes saved.

