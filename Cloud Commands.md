# heroku Publish
--cmd--
npm uninstall -g heroku-cli
npm i -g heroku
git init 
git add .
git commit -m "heroku"
heroku login
heroku create dtweetapi
heroku git:remote dtweetapi
heroku buildpacks:set jincod/dotnetcore
git push heroku main

# Github Push
--gitbash--
gitclone url
cd folder Name
git init
git add .
git commit -m "first commit"
git push origin master

settings -> add build Package
https://github.com/hkarthikraj01/dotnetcore-buildpack.git

# Docker Image to DockerHub
--cmd--
docker login
docker images
docker tag tweetapi:dev hkarthikraj01/tweetapi
docker push hkarthikraj01/tweetapi
