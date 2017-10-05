# \<paperfire-stripe\>
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/paperfireElements/paperfire-stripe)

A stripe payment element

## This element is in early development

This is a pretty simple wrapper for the Stripe Checkout flow, so it should be ready to use. But I haven't done any rigorous testing yet so please handle with care. Thanks :)

## Demo
<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="paperfire-stripe.html">
    <link rel="import" href="../paper-button/paper-button.html">
    <next-code-block></next-code-block>
  </template>
  
</custom-element-demo>
```
-->
```html
<div style="height: 400px;"></div>
<span>cost: $1,000,000</span>
<paper-button id="checkoutBtn" raised>Checkout</paper-button>
<paperfire-stripe id="stripe" amount="100000000" name="paperfire-stripe demo" description="Something really cool"></paperfire-stripe>
<script>
    document.getElementById('checkoutBtn').addEventListener('click', function () {
        this.dispatchEvent(
            new CustomEvent('paperfire-stripe-checkout', {
                bubbles: true,
                composed: true
            })
        );
    });
</script>
```

## Usage

To open Stripe Checkout you can fire a custom event `paperfire-stripe-checkout`
```
    this.dispatchEvent(
        new CustomEvent('paperfire-stripe-checkout', {
          bubbles: true,
          composed: true
          // the stripe checkout config can be passed in
          detail: {
              email: evasmith@smith.com,
              amount: 10000
          }
        })
    );
```

Or use the `open` method

```
 this.$.stripe.open();

 // the stripe checkout config can be passed in
 this.$.stripe.open({
     email: johnsmith@smith.com
     amount: 10000
 });

```


# Editing the element

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
