## API-only XSS
### Perform a persisted XSS attack with \<iframe src="javascript:alert(`xss`)"\> without using the frontend application at all.
### Category: XSS

Make a REST API call to `/api/Products/` and observe that it returns a list of product details in json.

`{"name":"xss", "description":"<iframe src=\"javascript:alert(`xss`)\">"}`

// ruleid:javascript-prompt
var name = prompt('what is your name');
// ruleid: javascript-alert
alert('your name is ' + name);
alert('not', 'a', 'valid', 'alert')
// ruleid: javascript-confirm
if ( confirm("pushem!") == true) {
    r = "x";
} else {
    r = "Y";
    // ruleid: javascript-debugger
    debugger;
}
