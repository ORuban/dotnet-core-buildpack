# dotnet-core-buildpack
Experimental Heroku Buildpack for .NET Core project

----
## Examples
Use below button to install [fork](https://github.com/ORuban/aspnetcore-angular2-universal)
of [ASP.NET Core & Angular 2+ Universal starter](https://github.com/MarkPieszak/aspnetcore-angular2-universal)

<a href="https://dashboard.heroku.com/new?template=https://github.com/ORuban/aspnetcore-angular2-universal.git">
  <img src="https://www.herokucdn.com/deploy/button.svg" alt="Deploy">
</a>

Life link: https://aspnetcore-angular2-universal.herokuapp.com


It uses the following `app.json` to set up app on Heroku:

```json
{
  "name": "aspnetcore-angular2-universal",
  "description": "Deploy Angular 2+ Universal & ASP.NET Core SPA Advanced Starter on Heroku",
  "logo": "https://raw.githubusercontent.com/herokumx/herokumxnet/master/NETChatterGroup.png",
  "keywords": ["heroku", "asp.net-core", "angular2", "spa"],
  "env": {
    "NPM_CONFIG_PRODUCTION": {
      "description": "False as we need to install devDependencies on heroku instance (webpack, ...)",
      "value" : "false"
    }
  },
  "buildpacks": [
    {
      "url": "heroku/nodejs"
    },
    {
      "url": "https://github.com/ORuban/dotnet-core-buildpack.git"
    }
  ]
}
```

## Useful links
- [HEROKU app.json Schema](https://devcenter.heroku.com/articles/app-json-schema)
- [Creating a 'Deploy to Heroku' Button](https://devcenter.heroku.com/articles/heroku-button)
