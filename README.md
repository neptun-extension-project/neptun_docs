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

