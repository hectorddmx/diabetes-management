### GET - Login
They have a very bare bones and insecure login URL:
```
https://api.jadediabetes.com/api/1.0/login.json?email=<EMAIL_HERE>&password=<PASSWORD_HERE>&debug=`
```

For example: 
The following user with:
Email: `sampleuser@gmail.com`
Password: `823ywriy23iasdasd`

```shell
curl "https://api.jadediabetes.com/api/1.0/login.json?email=sampleuser%40gmail.com&password=823ywriy23iasdasd&debug="
```
```json
{
  "result": true,
  "token": "32973-89012830918230192830",
  "user_id": 32973,
  "message": "Ok"
}
# We can save this token for later for the terminal
API_TOKEN=32973-89012830918230192830
```


```shell
# BLOOD_GLUCOSE_VALUE must be in range 1 to 59 mmol, 'Lo' or 'Hi' (not 90)
BLOOD_GLUCOSE_VALUE=40
curl "https://api.jadediabetes.com/api/1.0/add.json?token=${API_TOKEN}$&value=${BLOOD_GLUCOSE_VALUE}&time=&other=mmld&notes=none&guid=&log_type=1"
```