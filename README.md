# Discord.OAuth2
[![NuGet](https://img.shields.io/nuget/vpre/Discord.OAuth2.svg?maxAge=2592000?style=plastic)](https://www.nuget.org/packages/Discord.OAuth2)
[![MyGet](https://img.shields.io/myget/rogueexception/vpre/Discord.OAuth2.svg)](https://www.myget.org/feed/rogueexception/package/nuget/Discord.OAuth2) 
[![Build status](https://ci.appveyor.com/api/projects/status/axedfea3b7j1l2ua?svg=true)](https://ci.appveyor.com/project/RogueException/discord-oauth2)

ASP.Net Core middleware that enables an application to support Discord's OAuth 2.0 authentication workflow.

Based on the [ASP.Net Core Facebook OAuth](https://github.com/aspnet/Security/tree/dev/src/Microsoft.AspNetCore.Authentication.Facebook)

### Usage
```cs
app.UseDiscordAuthentication(new DiscordOptions
{
    AppId = Configuration["Discord:AppId"],
    AppSecret = Configuration["Discord:AppSecret"],
    Scope = { "identify", "guilds" }
});
```
