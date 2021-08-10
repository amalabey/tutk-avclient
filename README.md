# Overview

CLI program that can tap into video cameras that use TUTK IOT platform.

# Compile

Ensure below are installed in Linux environment so that C program can be compiled.

```
 sudo apt update
 sudo apt isntall build-essential
 sudo apt install gcc-multilib
```

Compile AVClient program. 

```
cd src
make
```

# Run

Follow below steps to run the AVClient against a known UUID.

```
source .env
./AVAPIs_Client -g "UUID" -u "userid" -p "password"
```

# Generate playable output

Use ffmpeg to generate a mp4 file from the binary (H264) files produced by AVClient.

```
ffmpeg -i I_000.bin -c:v copy -f mp4 "mytestoutput.mp4"
```

**You can install ffmpeg using below**
```
sudo apt install ffmpeg
```