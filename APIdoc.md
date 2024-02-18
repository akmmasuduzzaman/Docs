Running the model via API(NodeJS):

Install Replicate’s Node.js client library:
```
npm install replicate
```

Set the REPLICATE_API_TOKEN environment variable: (API Token can be found here: https://replicate.com/account/api-tokens)
```
export REPLICATE_API_TOKEN=r8_2q5*************************
```

Import and set up the client:
```
const output = await replicate.run(
  "akmmasuduzzaman/face-expression:2c47d8eabb86507111d1eb9acb793213753f3ae294f787280277c4614ae20a24",
  {
    input: {
      intensity: "normal",#<slight,normal,extreme>
      scheduler: "DPMSolverMultistep",
      expression: "Happy",
      guidance_scale: 7.5,
      num_inference_steps: 30,#<Can reduce to reduce the time>
      init_image_path: #<URI/URL of image>,
    }
  }
);
console.log(output);
```


For more information visit:

https://replicate.com/docs/get-started/nodejs

https://replicate.com/akmmasuduzzaman/face-expression?input=nodejs

