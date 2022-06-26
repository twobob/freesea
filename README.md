# Purpose It is relatively slow to access video websites such as YouTube over the wall, and it is also a method to track the download regularly.
## Can download video sites
* youtube
* p站 不解释
# Instructions
## file local storage
* Apply for a droplet of digital ocean
* python3.6 and above
* Install related system packages `apt-get update && apt-get install -y libmemcached-dev zlib1g-dev openssl build-essential libssl-dev xvfb`
* Create freesea `user useradd freesea`
* `mkdir /opt/freesea`
* `git clone https://github.com/daomanlet/freesea.git /opt/freesea`
* `cd /opt/freesea`
* Create virtual environment `python3 -m venv /opt/freesea/py3`
* Activate virtual environment `source /opt/freesea/bin/active`
* Install dependencies `python -m pip install -r requirements.txt`
* app/config.py modify mail, webdav configuration
* `uwsgi freesea.ini -H /opt/freesea/py3`
## Use seafile network disk
* Originally wanted to provide a public network disk, which can be registered and used, but there is not much space. Content that should not be placed will be cleared by the administrator
* But considering that this is beyond the scope of the development program, you can install it yourself, you can configure synchronization to the network disk
## uBuntu needs to install special parts to use imgkit
* Refer to imgkit[https://pypi.org/project/imgkit/]
* Which static library [https://github.com/jarrekk/imgkit/blob/master/travis/init.sh] also needs
* Specially add this `sudo apt-get install libssl1.0-dev`
## docker
* https://hub.docker.com/repository/docker/rouynxia/freesea
