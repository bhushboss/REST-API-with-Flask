# REST-API-with-Flask
Build a REST API with Flask Objective: Create a REST API that manages user data. Tools :Python, Flask, Postman or Curl Deliverables: Flask app with GET/POST/PUT/DELETE routes

1.How to Run the API:
install flask , open terminal/ command prompt and run 
bash 
pip install Flask
2.Save the code in a file 
app.py
3.Run application in your terminal 
python app.py
4. Observe output 
* Running on http://127.0.0.1:5000
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: ...
which means your API server is running
So API is live and listening for your requests
Test Your API (Using cURL)

GET fetches all users
Bash 
curl http://127.0.0.1:5000/users

Expected output
Json:
[
  {
    "email": "bhushan@example.com", 
    "id": 1, 
    "username": "bhushan"
  }, 
  {
    "email": "baby@example.com", 
    "id": 2, 
    "username": "baby"
  }
]
POST (Create User)
Creates a new user named "bharath".
bash :
curl -X POST -H "Content-Type: application/json" \
-d '{"username": "bharath_dev", "email": "bharath@example.com"}' \
http://127.0.0.1:5000/users
output: Json:{
  "email": "bharath@example.com", 
  "id": 3, 
  "username": "bharath_dev"
}
PUT:
curl -X PUT -H "Content-Type: application/json" \
-d '{"username": "bharath_developer"}' \
http://127.0.0.1:5000/users/3
output :
{
  "email": "bharath@example.com", 
  "id": 3, 
  "username": "bharath_developer"
}
DELETE 
Deletes user id 3.
bash :curl -X DELETE http://127.0.0.1:5000/users/3
Output:
{
  "message": "User with id 3 deleted successfully"
}.
Final Check : GET
output : 
[
  {
    "email": "bhushan@example.com", 
    "id": 1, 
    "username": "bhushan"
  }, 
  {
    "email": "baby@example.com", 
    "id": 2, 
    "username": "baby"
  }
]
