# Microservice Demo
This is a demonstration of steps 1 through 4 in payments flow.  Please note that the encryption function will not work if you use this on an unsecure host.

## Steps
Run and visit the `/parent.html` page.
```
npx http-server -p {Port_Number}
```

## Payments Flow
![Payments flow](/microservice-flow.png)

## What's happening here

### Parent Page (parent.html)
This page represents the payments page in the client app (web, iOS, Android).

### Iframe (card-iframe.html)
This file represents the iframe HTML that will be built into the client app, converted to base64, and displayed within the parent page

```
dynamicIframe.src = `data:text/html;base64,${baseEncodedHTML}`;
```