# Collector

**All differents collector available with devland.js :**

```javascript
<channel>.awaitMessages(<params>)
```

{% hint style="info" %}
`awaitMessages` allows you to get all messages sended in the channel with your own filter
{% endhint %}

```javascript
<message/interaction>.createComponentsCollector(<params>)
```

{% hint style="info" %}
`createComponentsCollector`allows you to get all components response from the message with your own filter
{% endhint %}

```javascript
<modal>.createModalListener(<params>)
```

{% hint style="info" %}
`createModalListener` allows you to get the response of a specific modal
{% endhint %}

**Collector params :**

```javascript
type collectorOptions = {
        type: "message" | "component",
        count: number,
        time: number,
        componentType: ComponentsType, //check Types page
        filter: Function
}
```

**Filter exemples :**&#x20;

`filter: (m) => m.user.id === message.authorId`

`filter: (m) => m.authorId === message.authorId`

`m` can _represent a Interaction or a Message_

The `end` event will be emitted when the `time` is elapsed or when `count` is declared and `count` component/message response is received

{% hint style="danger" %}
`type` field in the params is **automatic**, you don't need to set a value
{% endhint %}

{% hint style="danger" %}
`componentType` field in the params can be set in a [components collector](components-collector.md) **only** _(at least, it's optional)_
{% endhint %}

{% hint style="info" %}
All fields in the params is optional
{% endhint %}
