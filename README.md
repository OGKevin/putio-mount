# PutioMount
Mount put.io as a drive using python

## Retrieving a token
1) Go to https://put.io/oauth/apps/new , create an app (fill something in all fields, it does not matter)  
2) Go to https://put.io/oauth/apps , and click on the "key" icon, next to your app name  
3) Last field contains your token. Paste it in the /home/YOUR-USERNAME/.putio-token, instead of "YOUR_TOKEN_HERER"

## Installation
```bash
$ python setup.py install
```

## Usage
```bash
$ python ./putiomount.py /destination/folder
```

## Advanced usage
You can use PutioMount as a library:
```python
import PutioMount

# Set a custom temporary path
PutioMount.set_tmp_path('/tmp')

# Set a custom credentials path
PutioMount.set_credentials_path('/path/to/.credentials')

# Mount to specific path
PutioMount.mount('/my/mount/point')
```

## Issues
Upgrade requests and urllib3:
```bash
$ pip install -U urllib3
$ pip install -U requests
```

Check if fuse is installed:
```bash
$ apt-get install fuse
```
