# ui-binary
Consentua's default binary consent interface. Fork this to create custom interactions!

## Creating custom interactions
A custom interaction is a new user interface for collecting consent. By implementing a custom interaction you can customise how
your consent collection looks and behaves. 

Consentua interactions are built using HTML, CSS and Javascript. 

1. Get the WebSDK integrated into your app or website and get it working with one of our default interactions! This step is important, it's much easier to build a custom interaction if the rest of the WebSDK is working correctly!

2. Clone this repository, and make it available via a web server. For testing purposes, it can be a local server accessed at http://localhost/

3. In the embedding page, you need to tell Consentua to use your custom interaction. You can do so by passing in some additional 
options.

`
var cwrap = new ConsentuaEmbed({
iframe: iframe,
clientid: cid,
uid: uid,
templateid: tid,
serviceid: sid,
lang: 'en',
opts: {ix: "http://localhost/my-custom-interaction/"}
});
`

4. You can now change the HTML/CSS/Javascript on your local server to customise how the interaction looks and behaves. 

5. To deploy a custom interaction in a live environment, you can continue to pass an {ix: } option, but it's best to contact us
so that we can deploy your interaction via our own web server. By serving an interaction through our web server, we can provide
more detailed audit and versioning of your consent records. 
