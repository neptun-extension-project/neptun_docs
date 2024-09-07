Kezdetleges api docs az angularos neptunhoz.

### Be van-e kapcsolva a 2FA egy adott felhasználónál 

method: `GET`

```
/api/Account/HasUserTokenRegistration?userLoginName={felhasználó név}
```

### Captcha lekérése

method: `GET`

```
/api/login/captchaimage?bypassSystemParameterCheck=false
```

Válasz:
```
{
  "data": {
    "identifier": "{captcha uuid}",
    "content": "{captcha kép base64}"
  },
  "notification": []
}
```

### Audio captcha lekérése

method: `GET`

```
/api/Account/CaptchaAudio?identifier={captcha uuid}&lcid=1038
```

### Login

method: `POST`

```
/api/Account/Authenticate
```
data:
```
{
  "userName": "{felhasználó név}",
  "password": "{jelszó}",
  "captcha": "{captcha megoldása}",
  "captchaIdentifier": "{captcha uuid}",
  "LCID": 1038
}
```
