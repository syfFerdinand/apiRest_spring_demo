<h2>Project endpoint</h2>

<h3>Employees</h3>
Get employees <br>
<code>
curl -v {{ host }}/employees/ | json_pp
</code>

Get single employee <br>
<code>
curl -v {{ host }}/employees/{{id}} | json_pp
</code>

Add a new employee <br>
<code>
curl -v -X POST {{host}}/employees -H 'Content-Type:application/json' -d '{"name": "Samwise Gamgee", "role": "gardener"}'
</code>

Delete employee <br>
<code>
curl -v -X DELETE {{host}}/employees/{{id}}
</code>

<h3>Order</h3>
Get Orders <br>
<code>
curl -v {{host}}/orders
</code>

Get single order <br>
<code>
curl -v {{host}}/orders/{{id}}
</code>

Add new order <br>
<code>
curl -v -X POST {{host}}/orders -H 'Content-Type:application/json' -d '{"description":"all about order"}'
</code>

Cancel order <br>
<code>
curl -v -X DELETE {{host}}/orders/{{id}}/cancel
</code>

Complete order <br>
<code>
curl -v -X PUT {{host}}/orders/{{id}}/complete
</code>