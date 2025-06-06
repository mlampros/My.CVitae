
[![](https://img.shields.io/docker/automated/mlampros/mycvitae.svg)](https://hub.docker.com/r/mlampros/mycvitae)


## My.CVitae

<br>

**2025-05-05**: Added the Github Token in the [(gh) .yml file](https://github.com/mlampros/My.CVitae/blob/master/.github/workflows/docker_action.yml) file because I had to install the latest version of the [scholar R package]() from Github due to an [error](https://github.com/jkeirstead/scholar/issues/108). It seems that the `get_publication() function: 404 error` is random because I can render the [cv.Rmd](https://github.com/mlampros/My.CVitae/blob/master/docs/cv.Rmd) file error-free in my PC.

<br>

A workflow to programmatically generate my Curriculum Vitae from [templated .csv files](https://github.com/mlampros/My.CVitae/tree/master/data) in the R language both 

* when I push changes to the repository and 
* on weekly basis using a Github Actions (gh) cron-job (for instance to automatically receive updates from web sources such as [Google Scholar](https://scholar.google.com/citations?user=JXg3b58AAAAJ&hl=en) - if any). 

The [(gh) .yml file](https://github.com/mlampros/My.CVitae/blob/master/.github/workflows/docker_action.yml) relies on my [docker image](https://hub.docker.com/r/mlampros/mycvitae) that includes all R dependencies for the generation of my Curriculum Vitae (it is advised to use a docker image due to the [tinytex](https://yihui.org/tinytex/) and [fontawesome](https://github.com/rstudio/fontawesome) dependencies which can cause headaches sometimes). The [cv.Rmd file](https://github.com/mlampros/My.CVitae/blob/master/docs/cv.Rmd) takes as parameter also the docker working directory (which corresponds to the Github repository) from inside the [.yml file](https://github.com/mlampros/My.CVitae/blob/master/.github/workflows/docker_action.yml) so that minimal adjustments are required.

In a final step - if an R user intends to replicate the whole process - the 

* [Github Url](https://raw.githubusercontent.com/mlampros/My.CVitae/master/docs/cv.pdf) has to be modified in the following way `https://raw.githubusercontent.com/{PATH TO THE CV.pdf FILE}` and 
* [Google Docs Url](https://docs.google.com/viewer?url=https://raw.githubusercontent.com/mlampros/My.CVitae/master/docs/cv.pdf) has to be modified in the following way `https://docs.google.com/viewer?url={PATH TO THE CV.pdf FILE}`

to display the **My.CVitae/docs/cv.pdf** output file in a web format.

<br>

**References:**

* https://github.com/mitchelloharawild/vitae
* https://github.com/seabbs/cv
* https://github.com/loreabad6/R-CV
* https://dirask.com/posts/Github-how-to-display-raw-PDF-from-github-repository-in-web-browser-instead-of-download-PpqXnD

<br>
