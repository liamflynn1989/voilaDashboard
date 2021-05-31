# Voila apps on Heroku

This repo is used to create and deploy a voila [Voila](https://github.com/QuantStack/voila) app or dashboard to the web using the [heroku](https://www.heroku.com) platform. [Voila](https://github.com/QuantStack/voila) runs a jupyter notebook on a small jupyter server that by default displays only interactive widgets (such as sliders or buttons via [ipywidgets](https://ipywidgets.readthedocs.io/en/latest/index.html)) and the generated output , while hiding the code. The result is a live browser 'app' or dashboard with which the user can interact.  This is similar in concep to [R's Shiny](https://www.rstudio.com/products/shiny/shiny-server/) apps.

If one then deploys this app to the cloud via a platform such as Heroku (or Google cloud, AWS, etc) then the web app or dashboard becomes accessible to multiple users by simply browsing to a URL.

This repo contains the files to create a heroku app and my loose non-specialist instructions and explanations of how I think things work.  This repo is based on Martin Renou's own instructive [voila_heroku](https://github.com/martinRenou/voila_heroku) repo (visit there to see screencasts of sample apps).

### Heroku

Heroku is a 'platform as service' where one can deploys 'containers' (called 'dynos') that include the necessary unix OS and installed packages (specified in `requirements.txt` to run your voila/jupyter notebook server in the cloud.  One first creates the heroku app on one's local machine and then pushes the repo to heroku via `git`.  This then makes the dyno available online and it's deployment is triggered when a user visits the Heroku-created URL for the app. Heroku puts the container in place to execute everything and serve results via the web while the user(s) interact with the app.  The dyno will stay awake on the ready to serve results to the same or app instances or, after some set amount of time with no use , it will go to 'sleep' (closing down the dyno) until another user visits to re-trigger the cycle. 


Deploy Voila apps using Heroku, based on Martin Renou's [martinRenou/voila_heroku](https://github.com/martinRenou/voila_heroku)

I've written up observations and more detailed instructions in the [voila_notes.md](voila_notes.md) file.


