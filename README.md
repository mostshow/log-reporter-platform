# log-reporter-platform

A Monitor platform with React, Redux and ES6. Use sourceMap to Debug errorJs.

Including:

* React-Router
* Redux-Thunk
* Mongodb
* Webpack
* Express
* pm2

## Quick start

Clone the repository
```bash
git clone git@github.com:mostshow/log-reporter-platform.git
```

Install 
[Mongodb](https://docs.mongodb.com/manual/installation/)

dependencies 
```bash
cd log-reporter-platform
npm install
sudo npm i babel-node -g
sudo npm i pm2 -g
```


Development
```bash
npm run server
```

Production
```bash
pm2 start release.config.json
```

Auto clear log
```
mongo:
db.settings.insert({
    "id": 1,
    "expiredTime": 604800,
    "createAt" : new Date()
 })
pm2 start removeLog.config.json

(but you can find all log in log dir)
```
## front-end

- [log-reporter](https://github.com/mostshow/log-reporter)

