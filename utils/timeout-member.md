# Timeout member

## Timeout for 10 seconds

```javascript
<member>.edit({
    communication_disabled_until: 10000 //in millisecond
})
// OR after 1.3.0
<member>.setTimeout(10000, "reason")
```

## Remove timeout

```javascript
<member>.edit({
    communication_disabled_until: null
})
// OR after 1.3.0
<member>.setTimeout(null, "reason")
```

{% hint style="info" %}
You can add the propertie`reason`to specify a reason in the guild logs
{% endhint %}
