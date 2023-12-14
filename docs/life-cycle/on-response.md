---
title: On Response - ElysiaJS
head:
    - - meta
      - property: 'og:title'
        content: On Response - ElysiaJS

    - - meta
      - name: 'description'
        content: Executed after the response sent to client. It's recommended to use **On Response** in the following situations. Clean up response. Loggic and analytic.

    - - meta
      - property: 'og:description'
        content: Executed after the response sent to client. It's recommended to use **On Response** in the following situations. Clean up response. Loggic and analytic.
---

# Response
Executed after the response sent to client.

It's recommended to use **On Response** in the following situations:
- Clean up response
- Loggic and analytic

## Example
Below is an example of using the before handle to check for user sign-in.

```typescript
import { Elysia } from '../src'

new Elysia()
	.onResponse(() => {
		console.log('Response', performance.now())
	})
	.listen(3000)
```

Console should log as the following:

```bash
Response 0.0000
Response 0.0001
Response 0.0002
```