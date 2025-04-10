# My First Flask Web App

## Dev Steps

docker run -it ubuntu bash
apt-get update

export DEBIAN_FRONTEND=noninteractive
apt-get update
apt-get install -y tzdata
ln -fs /usr/share/zoneinfo/Asia/Dhaka /etc/localtime
dpkg-reconfigure -f noninteractive tzdata
apt-get install -y python3 python3-setuptools python3-dev build-essential python3-pip default-libmysqlclient-dev

apt install python3-venv -y

mkdir flask_project

cd flask_project

python3 -m venv flaskenv

source flaskenv/bin/activate

pip install flask

cat > /opt/app.py

from flask import Flask
app = Flask(__name__)

@app.route("/")
def main():
    return "Welcome!"

@app.route("/how are you")
def hello():
    return "I am good, how about you?"

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=5000)

python3 /opt/app.py


docker build -t first-flask-webapp .

docker tag first-flask-webapp mimnets/first-flask-webapp:first-flask-webapp

docker image ls

docker push mimnets/first-flask-webapp:first-flask-webapp

login [If required]

now pull and check if it's working

docker run -p 5000:5000 mimnets/first-flask-webapp
