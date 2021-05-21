ESTA API NO FUNCIONA ASÍ QUE NO INTENTES UTILIZARLA

Ejemplo python sin errores de sintaxis:
```
import requests

headers = {
    'accept': 'application/json',
    'content-type': 'application/json',
    'Authorization': 'Bearer APP_USR-.........'
}

data = """{
            "file_name_prefix": "settlement-report-USER_ID",
            "show_fee_prevision": false,
            "show_chargeback_cancel": true,
            "detailed": true,
            "coupon_detailed": true,
            "shipping_detail": true,
            "refund_detailed": true,
            "extended": false,
            "frequency": {
                "hour": 0,
                "type": "monthly",
                "value": 1
            }
        }"""

response = requests.post('https://api.mercadopago.com/v1/account/settlement_report/config', headers=headers, data=data)
print(response)
print(response.text
```
Da como resultado:
```
<Response [400]>
{"message":"Invalid include_withdraw,","error":"invalid_include_withdraw","cause":[]}
```

Sin el endpoint GET a `https://api.mercadopago.com/v1/account/settlement_report/config` toda esta API NO PUEDE USARSE, con lo cual recomendamos que no inviertas tiempo leyendo esta documentación.
