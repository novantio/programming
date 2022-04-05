# content
[soap](##soap)


# soap
```
url = "http://novantio.com:80/sap/xi/engine?type=entry&version=3.0&Sender.Service=PM_DEV&Interface=urn:laksa:getpmdata^si_osGetEqui"
maxrow=10000
payload="<soapenv:Envelope xmlns:soapenv=\"http://schemas.xmlsoap.org/soap/envelope/\" xmlns:urn=\"urn:laksa:getpmdata\">\r\n   <soapenv:Header/>\r\n   <soapenv:Body>\r\n      <urn:mt_GetEqui_Req>\r\n         <Client>350</Client>\r\n         <CoCode>2021</CoCode>\r\n         <Plan_Plant></Plan_Plant>\r\n         <MaxRow>"+str(maxrow)+"</MaxRow>\r\n         <Characteristic></Characteristic>\r\n         <!--1 or more repetitions:-->\r\n         <Equipment>\r\n            <Equipment></Equipment>\r\n         </Equipment>\r\n         <CrtdDate>\r\n            <CrtdDateFr></CrtdDateFr>\r\n            <CrtdDateTo></CrtdDateTo>\r\n         </CrtdDate>\r\n         <ChangeDate>\r\n            <ChangeDateFr></ChangeDateFr>\r\n            <ChangeDateTo></ChangeDateTo>\r\n         </ChangeDate>\r\n      </urn:mt_GetEqui_Req>\r\n   </soapenv:Body>\r\n</soapenv:Envelope>"
headers = {
  'Content-Type': 'text/xml',
  'SOAPAction': 'http://sap.com/xi/WebService/soap1.1',
  'Authorization': 'Basic dF9oWRheWF0dWxtOnBlcnRbWluYSE=',
  'Cookie': 'sap-usercontext=sap-client=300'
}

response = requests.request("POST", url, headers=headers, data=payload)

dom = response.text
```
