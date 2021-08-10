# GET - Login
They have a very bare bones and somewhat insecure login URL but let's ignore that for now.

If we just created a new user with the following data:
Email: `sampleuser@gmail.com`
Password: `823ywriy23iasdasd`

We can login buy using the `login.json` request.
```shell
USER_EMAIL="sampleuser@gmail.com"
USER_PASS="823ywriy23iasdasd"
curl "https://api.jadediabetes.com/api/1.0/login.json?email=${USER_EMAIL}&password=${USER_PASS}&debug="
```

We'll receive the following JSON response.
```json
{
  "result": true,
  "token": "32973-89012830918230192830",
  "user_id": 32973,
  "message": "Ok"
}
```

The token is what's important for us.
We can save this token for later for testing with curl
```shell
export API_TOKEN='32973-89012830918230192830'
```

To test that your login was successful, you can try creating a new record:
- [[GET - Submit blood glucose value]]