# Api rest with spring demo
**This project is a simple api rest for manage employees and order**
## Employees
Get employees  
```
curl -v {{ host }}/employees/ | json_pp
```

Get single employee  
```
curl -v {{ host }}/employees/{{id}} | json_pp
```

Add a new employee  
```
curl -v -X POST {{host}}/employees -H 'Content-Type:application/json' -d '{"name": "Samwise Gamgee", "role": "gardener"}'
```

Delete employee  
```
curl -v -X DELETE {{host}}/employees/{{id}}
```

## Order
Get Orders  
```
curl -v {{host}}/orders
```

Get single order  
```
curl -v {{host}}/orders/{{id}}
```

Add new order  
```
curl -v -X POST {{host}}/orders -H 'Content-Type:application/json' -d '{"description":"all about order"}'
```

Cancel order  
```
curl -v -X DELETE {{host}}/orders/{{id}}/cancel
```

Complete order  
```
curl -v -X PUT {{host}}/orders/{{id}}/complete
```
