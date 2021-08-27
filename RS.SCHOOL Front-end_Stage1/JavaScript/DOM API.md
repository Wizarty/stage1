#js #dom
 
The DOM is not part of the JavaScript language, but is instead a Web API used to build websites. JavaScript can also be used in other contexts. For example, Node.js runs JavaScript programs on a computer, but provides a different set of APIs, and the DOM API is not a core part of the Node.js runtime.

# The HTML DOM API

The **HTML DOM API** is made up of the interfaces that define the functionality of each of the [elements](https://developer.mozilla.org/en-US/docs/Glossary/Element) in [HTML](https://developer.mozilla.org/en-US/docs/Glossary/HTML), as well as any supporting types and interfaces they rely upon.

The functional areas included in the HTML DOM API include:

-   Access to and control of HTML elements via the [DOM](https://developer.mozilla.org/en-US/docs/Glossary/DOM).
-   Access to and manipulation of form data.
-   Interacting with the contents of 2D images and the context of an HTML [`<canvas>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas), for example to draw on top of them.
-   Management of media connected to the HTML media elements ([`<audio>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio) and [`<video>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video)).
-   Dragging and dropping of content on webpages.
-   Access to the browser navigation history
-   Supporting and connective interfaces for other APIs such as [Web Components](https://developer.mozilla.org/en-US/docs/Web/Web_Components), [Web Storage](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API "Web Storage"), [Web Workers](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API "Web Workers"), [WebSocket](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API "WebSocket"), and [Server-sent events](https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events "Server-sent events").

## HTML DOM concepts and usage

In this article, we'll focus on the parts of the HTML DOM that involve engaging with HTML elements. Discussion of other areas, such as [Drag and Drop](https://developer.mozilla.org/en-US/docs/Web/API/HTML_Drag_and_Drop_API "Drag and Drop"), [WebSockets](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API "WebSockets"), [Web Storage](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API "Web Storage"), etc. can be found in the documentation for those APIs.

## HTML DOM target audience

The features exposed by the HTML DOM are among the most commonly-used APIs in the web developer's arsenal. All but the most simple web applications will use some features of the HTML DOM.

## HTML DOM API interfaces

The majority of the interfaces that comprise the HTML DOM API map almost one-to-one to individual HTML elements, or to a small group of elements with similar functionality. In addition, the HTML DOM API includes a few interfaces and types to support the HTML element interfaces.