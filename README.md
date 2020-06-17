Creating helm chart repo



### How It Works
I set up GitHub Pages to point to the docs folder. From there, I can create and publish docs like this:

```console
$ helm create samplechart
$ helm package samplechart
$ mv samplechart-0.1.0.tgz docs
$ helm repo index docs --url https://github.com/anupammehtaSF/helmcharts
$ cat docs/index.yaml
$ helm repo list
$ git add .
$ git commit -m "Charts repo"
$ git push origin master
```

From there, I can do:
```
helm repo add myrepo https://anupammehtasf.github.io/helmcharts/docs
```
