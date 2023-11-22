# OWASP Juice Shop - CTF Tutorial

## Prerequisites

1. [Install OWASP Juice Shop](https://github.com/juice-shop/juice-shop#setup) locally.
2. [Install Juice Shop CTF CLI](https://github.com/juice-shop/juice-shop-ctf#setup----) locally.
3. [Install CTFd](https://github.com/CTFd/CTFd#install) locally or as a Docker container.
4. Open [OWASP Juice Shop - Tutorial Series - CTF.pdf](OWASP%20Juice%20Shop%20-%20Tutorial%20Series%20-%20CTF.pdf) for context and general instructions.

## Tutorial Steps

### 0. Launch OWASP Juice Shop
```
npm start
```
launches Juice Shop in standard configuration. When solving any hacking challenge, you do not get a flag code for the CTF.

### 1. Launch OWASP Juice Shop in CTF mode
```
set NODE_ENV=ctf     # on Windows
export NODE_ENV=ctf  # on Linux

npm start
```
or shorthand (on Linux only)
```
NODE_ENV=ctf npm start
```
Solving any hacking challenge will now yield a flag code! Now we need a place to trade those flag codes for valuable CTF points! In CTF mode you can also re-trigger the notifications by clicking the flag-button on the Score Board. This can be handy in case you missed a flag code.

### 2. Set up an empty CTF event in CTFd

Install CTFd locally on your machine according to <https://github.com/CTFd/CTFd#install>. The simplest possible installation is their singular Docker image that can be started with

```
docker run -p 8000:8000 -it ctfd/ctfd
```

### 3. Run Juice Shop CTF CLI interactively
```
juice-shop-ctf
```

1. `CTF framework to generate data for?`: Select `CTFd` with the up/down arrow keys and hit Enter
2. `Juice Shop URL to retrieve challenges?`: Type `localhost:3000` (or the URL where your Juice Shop server is available at) and hit Enter
3. `Secret key <or> URL to ctf.key file?`: Type `1234567890` and hit Enter
4. `Insert a text hint along with each challenge?`: Select `Free text hints` and hit Enter
5. `Insert a hint URL along with each challenge?`: Keep `No hint URLs` and just hit Enter
6. `Insert a code snippet as hint each challenge?`: Keep `No hint snippets` and just hit Enter 

### 4. Import generated CSV backup into CTFd
1. Go to the section _Admin Panel_ > _Config_ > _Backup_ and choose _Import CSV_
2. Select _Challenges_ from the _CSV Type_ dropdown
3. Select the generated `.csv` file as _CSV File_ and press _Import_.

### 5. Launch Juice Shop in CTF mode
```
NODE_ENV=ctf npm start
```

Solve a challenge in your Juice Shop (started with `NODE_ENV=ctf`) and paste the flag code into your CTFd instance. You will notice, that the flag is _not accepted_? Why is that? We did not tell Juice Shop the matching `ctf.key` during startup!

### 6. Launch Juice Shop in CTF mode with custom `ctf.key`
Start Juice Shop again with an additional environment variable `CTF_KEY` set to `1234567890`, e.g. in Linux via this one-line command:
```
NODE_ENV=ctf CTF_KEY=1234567890 npm start
```

Replay the notification of the previously solved challenge. You will notice that the flag code changed. Pasting it into CTFd should solve the matching challenge there!
