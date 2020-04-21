# CodePipeline Radiator

Has your CodePipeline builds ever been broken for multiple days because the status of those pipes weren't visible somewhere all the time? 😢

With CodePipeline Radiator you can see the status of all project pipes you wan't to track. Everything at a glance! 🔥👀

## How to configure

__Note!__ Configration is subject to change as the radiator is currently being switched to Lambda, which in turn uses IAM roles

1. Create `.env` file with `cp .env.example .env`
2. Set the `AWS_REGION` with the desired region in `.env` file or environment variable
3. Auth either using `aws-cli` or create IAM user with access to CodePipeline and set `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` to `.env` file or environment variables

Example `.env` file

```bash
HTTP_PORT=80
AWS_REGION=eu-west-1
AWS_ACCESS_KEY_ID=someRandomStringHereGeneratedByAWS
AWS_SECRET_ACCESS_KEY=someRandomStringHereGeneratedByAWS
```

## Usage

1. Run `npm run build` to create production build of the radiator
2. Run `npm start` to start the server
3. Open `http://localhost` and set the CodePipeline name to the `q` url param (fe. `http://localhost?q=my-fantastic-codepipeline`)
4. Enjoy your new visibility to AWS CodePipeline 📺!
