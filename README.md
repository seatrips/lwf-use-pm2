# How to use pm2 with LWF
Guide to switch from forever to pm2

### Steps to take

```
cd lwf-node
```
```
forever stopall
```
```
sudo npm install -g pm2
```
```
pm2 startup
```
You will be given a line to copy and paste in cmd-line
```
pm2 logrotate
```
You will be given a line to copy and paste in cmd-line
```
pm2 set pm2-logrotate:max_size 100M
```
```
pm2 start app.js
```

### updating node

```
cd lwf-node
```
```
pm2 stop app.js
```
```
./lwf_manager.bash rebuild

```
### When rebuilding and syncing is done

```
forever stop app.js
```
```
pm2 start app.js
```

### To check / Monitor

```
pm2 monit
```
```
pm2 monitor (see note below)
```
```
pm2 monitor app.js
```
```
pm2 status
```
### Keymetrics

When using "pm2 monitor" for the first time you will get the question to register on keymetrics
```
    __ __                          __       _
   / //_/__  __  ______ ___  ___  / /______(_)_________
  / ,< / _ \/ / / / __ `__ \/ _ \/ __/ ___/ / ___/ ___/
 / /| /  __/ /_/ / / / / / /  __/ /_/ /  / / /__(__  )
/_/ |_\___/\__, /_/ /_/ /_/\___/\__/_/  /_/\___/____/
          /____/

        Harden your Node.js application, today

Now registering to Keymetrics
Username: 
```
just register and add your node to keymetrics monitoring for free (up to 4 nodes)

you will get a link to the wui to monitor your node



