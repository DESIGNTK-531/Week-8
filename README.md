
## 1. Turn on the Raspberry Pi

## 2. Turn on SSH

go to the Raspberry Pi configuration menu

```
sudo raspi-config
```

then reboot

```
sudo reboot
```

## 3. Get the Raspberry Pi's IP address

```
hostname -I
```

## 4. SSH into the Raspberry Pi
```
ssh pi@<raspberry-pi-ip>
```

## 5. On the Raspberry Pi, run the subscriber

go to the repo  

```
cd <path-to-repo>
```

install the paho-mqtt library

```
sudo apt install python3-paho-mqtt
```

run the subscriber

```
python sub.py
```

## 6. On your local machine, run the publisher

go to the repo

```
cd <path-to-repo>
```

run the publisher

```
python pub.py
```

## 7. Check the messages

```
cat mqtt_messages.txt
```