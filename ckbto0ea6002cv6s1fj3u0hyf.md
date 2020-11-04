## Copy text to clipboard with Javascript

One thing that I find myself searching for from time to time, is how to copy a specific text on my app to the clipboard, when the user just clicks on a button or some action occured. My most recent example, was to copy the current IP of the machine, without having to select the text and hit Control + C or Command + C. Basically copying the text, just by pressing a single button.

There are some ways to achieve this, but what I found to be the easiest is to follow this steps:

-   Create and append a `<textarea>` element to the DOM;
-   Set the `value` of the `<textarea>` , to the desired content that we want our user to copy;
-   Use this function, `HTMLInputElement.select()`  to select the content;
-   Use another function to copy the selected text, `Document.execCommand('copy')` ;
-   In the, just delete that `<textarea>` .

This can be achieved with this:

```
const copyToClipboard = text => {
  // Create textarea  
  const ta = document.createElement('textarea');
  // Add your value to it
  ta.value = text;
  // Append it to the DOM
  document.body.appendChild(el);
  // Select its contents
  ta.select();
  // Copy the selected content
  document.execCommand('copy');
  // Removed it when the content is copied
  document.body.removeChild(ta);
};
```

For those out there who are not familiar with this Javascript syntax, I'll give you something else that you might be more familiar with.

```
var copyToClipboard = function(text) {
  // Create textarea  
  var ta = document.createElement('textarea');
  // Add your value to it
  ta.value = text;
  // Append it to the DOM
  document.body.appendChild(el);
  // Select its contents
  ta.select();
  // Copy the selected content
  document.execCommand('copy');
  // Removed it when the content is copied
  document.body.removeChild(ta);
};
```

Either way, to make this work, you just need to call this newly created function, and pass a parameter to it, with the text you desire your user to copy to the clipboard.

```
copyToClipboard("192.1.1.168");
// If the user pastes now, it will return: 192.1.1.168
```