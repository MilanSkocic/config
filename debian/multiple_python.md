# Dependencies

```
$ sudo apt-get install build-essential checkinstall
$ sudo apt-get install libreadline-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev libffi-dev zlib1g-dev
```

```
$ cd /opt
$ sudo wget https://www.python.org/ftp/python/3.13.0/Python-3.13.0.tgz
$ sudo tar -xvf Python-3.13.0.tgz
```

```
$ cd Python-3.13.0
$ sudo ./configure --enable-optimizations
$ sudo make altinstall
```

```
$ update-alternatives --install /usr/bin/python3 python /usr/local/bin/python3.13 2 --slave /usr/bin/pip3 pip /usr/local/bin/pip3.13
$ update-alternatives --install /usr/bin/python3 python /usr/local/bin/python3.12 1 --slave /usr/bin/pip3 pip /usr/local/bin/pip3.12
```

```
$ update-alternatives --list python
/usr/bin/python3.12
/usr/local/bin/python3.13
```


```
$ update-alternatives --config python
```
There are 2 choices for the alternative python (providing /usr/bin/python).

```
  Selection    Path                      Priority   Status
------------------------------------------------------------
* 0            /usr/local/bin/python3.13   2         auto mode
  1            /usr/bin/python3.12         1         manual mode
  2            /usr/local/bin/python3.13   2         manual mode

Press <enter> to keep the current choice[*], or type selection number:
```

# create link for pip if not present
ln -s /usr/bin/pip3 /usr/bin/pip
