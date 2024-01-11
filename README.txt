10/29/23 2:24 PM
This is a simple JSON/HTTP commit log service which accepts and responds with JSON while storing records in an in-memory log. This service is built in go.

curl -X POST localhost:8080 -d \ '{"record": {"value": "TGV0J3MgR28gIzEK"}}'

curl -X POST localhost:8080 -d \ '{"record": {"value": "TGV0J3MgR28gIzIK"}}'

curl -X POST localhost:8080 -d \ '{"record": {"value": "TGV0J3MgR28gIzMK"}}'

curl -X GET localhost:8080 -d '{"offset": 0}'

curl -X GET localhost:8080 -d '{"offset": 1}'

curl -X GET localhost:8080 -d '{"offset": 2}'
