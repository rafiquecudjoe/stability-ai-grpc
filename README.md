
## API

```ts
import { generate } from 'stability-client'

const api = generate({
  prompt: 'A Stunning House',
  apiKey: process.env.DREAMSTUDIO_API_KEY,
})

api.on('image', ({ buffer, filePath }) => {
  console.log('Image', buffer, filePath)
})

api.on('end', (data) => {
  console.log('Generating Complete', data)
})
```

Async/Promise API

```ts
import { generateAsync } from 'stability-client'

try {
  const { res, images } = await generateAsync({
    prompt: 'A Stunning House',
    apiKey: process.env.DREAMSTUDIO_API_KEY,
  })
  console.log(images)
} catch (e) {
  // ...
}
```



## Developing

```
npm i
npm run build
npm run start
