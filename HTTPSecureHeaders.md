## HTTP Secure Headers

### Content-Security-Policy (CSP)
- Only allow resources from trusted sources. (Resources include scripts, styles, images, etc.)
- Prevents XSS attacks by restricting where content can be loaded from.
- Loads everything from the same origin by default.

### HSTS (HTTP Strict Transport Security)
- Enforces secure connections (HTTPS) to the server.
- Prevents downgrade attacks by ensuring that browsers only connect via HTTPS.
- Can be set using the `Strict-Transport-Security` header.

### X-Content-Type-Options
- Prevents browsers from MIME-sniffing a response away from the declared content type.
- Helps to prevent attacks based on content type confusion.
- Set using the `X-Content-Type-Options` header with the value `nosniff`.
- What is MIME-sniffing?
  - MIME-sniffing is a technique used by browsers to determine the type of content being served, which can lead to security vulnerabilities if the content type is not properly declared.
- With this header malicious content cannot be executed as a different type than what it is declared as.

### Referrer-Policy
- Controls how much referrer information is passed when navigating from one page to another.
- Helps to protect user privacy by limiting the information shared with other sites.
- If not set then the default behavior is to send the full URL with query parameters which can expose sensitive information.

### Cross-Origin Resource Sharing (CORS)
- A security feature that allows or restricts resources to be requested from another domain outside the domain from which the resource originated.

### Permissions-Policy
- Controls which features and APIs can be used in the browser.
- Allows or restricts access to features like geolocation, camera, microphone, etc.

