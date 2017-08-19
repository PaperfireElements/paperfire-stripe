# \<paperfire-stripe\>
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/paperfireElements/paperfire-stripe)

A stripe payment element

## Demo
<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="paperfire-stripe.html">
    <link rel="import" href="../paper-button/paper-button.html">
    <paper-button id="checkoutBtn" raised>Checkout</paper-button>
    <next-code-block></next-code-block>
  </template>
  <script>
    document.getElementById('checkoutBtn').addEventListener('click', function () {
          this.dispatchEvent(new CustomEvent('paperfire-stripe-checkout', {
            bubbles: true,
            composed: true
          }));
        });
    </script>
</custom-element-demo>
```
-->
```html
<paperfire-stripe amount="100000000" name="paperfire-stripe demo" description="Something really cool"></paperfire-stripe>
```

## Usage
To open Stripe Checkout you need to fire a custom event `paperfire-stripe-checkout`
```
    this.dispatchEvent(
        new CustomEvent('paperfire-stripe-checkout', {
          bubbles: true,
          composed: true
        })
    );
```


## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your element locally.

## Viewing Your Element

```
$ polymer serve
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.
