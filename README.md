Creating helm chart repo


Steps:
How It Works
I set up GitHub Pages to point to the docs folder. From there, I can create and publish docs like this:

$ helm create samplechart
$ helm package samplechart
$ mv samplechart-0.1.0.tgz docs
$ helm repo index docs --url https://github.com/anupammehtaSF/helmcharts
$ git add .
$ git commit -m "Charts repo"
$ git push origin master

From there, I can do:
 helm repo add helmcharts https://github.com/anupammehtaSF/helmcharts
