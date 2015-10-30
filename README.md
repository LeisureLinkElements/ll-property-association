# ll-property-association

### Summary
UI for adding and removing property relations, configurable for any source, such as taxes.
### Usage
1. Add tag to html:

        <ll-property-association
            id="myPropAssoc"
            pmc-id="iwiks932"
            relation-source="taxes"
            relation-source-singular="tax"
            relation-source-id="98ksh982">
        </ll-property-association>
        
1. Optional: Set properties with javascript instead:

        var propAssoc = document.getElementById("myPropAssoc");
        propAssoc.pmcId = "iwiks932";
        propAssoc.relationSource = "taxes";
        propAssoc.relationSourceSingular = "tax";
        propAssoc.relationSourceId = "98ksh982";
        
1. Optional: Add event listeners for messages and errors:

        var propAssoc = document.getElementById("myPropAssoc");
        propAssoc.addEventListener('display-message', function (evt) {
          alert('message: '+evt.detail);
        });
        propAssoc.addEventListener('display-error', function (evt) {
          alert('error: '+evt.detail);
        });
        
1. Optional debugging attributes: Set attribute fire-log and optional fire-log-name="Property Association UI" to output debugging messages to console.
1. Display associated properties:

        propAssoc.load();

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install


## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    polyserve

Once running, you can preview your element at
`http://localhost:8080/components/seed-element/`, where `seed-element` is the name of the directory containing it.


## Testing Your Element

Simply navigate to the `/test` directory of your element to run its tests. If
you are using Polyserve: `http://localhost:8080/components/seed-element/test/`

### web-component-tester

The tests are compatible with [web-component-tester](https://github.com/Polymer/web-component-tester).
Install it via:

    npm install -g web-component-tester

Then, you can run your tests on _all_ of your local browsers via:

    wct

#### WCT Tips

`wct -l chrome` will only run tests in chrome.

`wct -p` will keep the browsers alive after test runs (refresh to re-run).

`wct test/some-file.html` will test only the files you specify.
