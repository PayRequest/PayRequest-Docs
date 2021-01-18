---
description: Send payment data to a webhook URL
---

# Webhooks

## Setup Webhooks

Just navigate to Settings -&gt; API and fill in your Webhook URL:

![Webhook URL](../.gitbook/assets/schermafbeelding-2021-01-18-om-13.12.32.png)

{% hint style="info" %}
 Super-powers are granted randomly so please submit an issue if you're not happy with yours.
{% endhint %}

Once you're link: personallink &lt;-- indien personal payment of link id als het een paymentlink is amount: amount &lt;-- spreekt voor zich?

indien recurring: count: X &lt;-- aantal keer betaald

indien paymentlink: status: eigenlijk altijd PAID

indien personallink: user, email, note &lt;-- spreekt voor zich? enough, save the world:

{% code title="hello.sh" %}
```bash
# Ain't no code for that yet, sorry
echo 'You got to trust me on this, I saved the world'
```
{% endcode %}

{% api-method method="get" host="link:" path="personallink or linkid" %}
{% api-method-summary %}
Link ID
{% endapi-method-summary %}

{% api-method-description %}
If it is a 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="link:" type="string" required=false %}
personallink or linked
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="" type="string" required=false %}
S
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
Sample output
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



