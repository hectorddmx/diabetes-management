# GET - Submit blood glucose value
You can submit multiple tipes of values with the `add.json` request.

Before we start, to use this calls you'll need to be logged in and generated a token. See [[GET - Login]] for more info.

To submit blood glucose values we'll have to send to log_type value as 1: 
`log_type=1`

If you're familiar how blood glucose levels are measured, you'll know there are two common measures, `mmol/L` common in the US and `mg/dL` common in Mexico.
An example of a high value for a non-diabetic person, 90 mg/dL, is about 5 mmol/L
![[Pasted image 20210810040827.png]]

To record a blood glucose value we can do it like this
```shell
# BLOOD_GLUCOSE_VALUE must be in range 1 to 59 mmol, 'Lo' or 'Hi' (not 90)
# 5 mmol is equivalent to 90 mg/dl
BLOOD_GLUCOSE_VALUE='5'
curl "https://api.jadediabetes.com/api/1.0/add.json?token=${API_TOKEN}&value=${BLOOD_GLUCOSE_VALUE}&time=&other=&notes=none&guid=&log_type=1"
```

By default the time is sent as NOW if you leave it empty.
Otherwise the format is `Y-m-d H:i:s` in `UTC/GMT`

```shell
BLOOD_GLUCOSE_VALUE='4.1'
RECORD_TIME='2021-08-09%2000:00:00'
curl "https://api.jadediabetes.com/api/1.0/add.json?token=${API_TOKEN}&value=${BLOOD_GLUCOSE_VALUE}&time=${RECORD_TIME}&other=&notes=none&guid=&log_type=1"
```

- - -

## Invalid input

### Out of bounds value

If you send an out of bounds value
```shell
BLOOD_GLUCOSE_VALUE='220'
curl "https://api.jadediabetes.com/api/1.0/add.json?token=${API_TOKEN}&value=${BLOOD_GLUCOSE_VALUE}&time=&other=mmld&notes=none&guid=&log_type=1"
```
You'll get the following JSON response:
```json
{
  "result": false,
  "message": "BGL must be in range 1 to 59 mmol, 'Lo' or 'Hi' (not 220)",
  "created": ""
}
```

### Invalid token

If you send an incorrect token, you may receive a message like this:
```json
{
  "result": false,
  "message": "Bad token [17787b50939175f0ff3957313ec55dd1$] - login to JadeDiabetes.com and check Settings:Sharing:Third Party"
}
```