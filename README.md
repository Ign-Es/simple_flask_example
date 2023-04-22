# Simple Flask API Example
This example includes the API code in api.py and uses a pipenv inside a docker container for ease of use.

To pull the ready to use docker image:
```bash
docker pull ignesmir/ml-flask1
```
Then run the container with mapped port 5000 :
```bash
docker run --rm --name test-api -p 5000:5000 ignesmir/ml-flask1
```
Now you may issue a request to the API using curl:
```bash
curl http://localhost:5000/score \
    --request POST \
    --header "Content-Type: application/json" \
    --data '{"X": [1, 2]}'
```
It is also possible to simply clone the repository and activate the virtual environment