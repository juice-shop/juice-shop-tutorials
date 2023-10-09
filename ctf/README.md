# OWASP Juice Shop - CTF Tutorial

## Prerequisites

1. [Install OWASP Juice Shop](https://github.com/juice-shop/juice-shop#setup) locally.
2. [Install Juice Shop CTF CLI](https://github.com/juice-shop/juice-shop-ctf#setup----) locally.
3. [Install CTFd](https://github.com/CTFd/CTFd#install) locally or as a Docker container.
4. Open [OWASP Juice Shop - Tutorial Series - CTF.pdf](OWASP%20Juice%20Shop%20-%20Tutorial%20Series%20-%20CTF.pdf) for context and general instructions.

## Tutorial Steps

### 1. Launch OWASP Juice Shop
n/a

### 2. Set up an empty CTF event in CTFd
n/a

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
n/a

### 5. Launch Juice Shop in CTF mode
```
NODE_ENV=ctf npm start
```

### 6. Launch Juice Shop in CTF mode with custom `ctf.key`
```
NODE_ENV=ctf CTF_KEY=1234567890 npm start
```
