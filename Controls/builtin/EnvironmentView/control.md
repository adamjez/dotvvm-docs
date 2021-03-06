Allows to render content when an application is running on a specific environment (eg. Development, Production). We use an `IEnvironmentNameProvider`
service to get the name of the current environment. The default implementation behaves differently on OWIN and on ASP.NET Core.

- **On ASP.NET Core:** We simply use the [IHostingEnvironment.EnvironmentName](https://docs.asp.net/projects/api/en/latest/autoapi/Microsoft/AspNetCore/Hosting/IHostingEnvironment/index.html?highlight=EnvironmentName#prop-Microsoft.AspNetCore.Hosting.IHostingEnvironment.EnvironmentName)
property to get the name.
- **On OWIN:** We use a value stored in the environment dictionary under the `host.AppMode` key. If you host your application on `System.Web` 
the value is automatically set to `Development` when debugging is enabled in Web.config.

In both cases the default environment name is `Production`. You may override this behavior by implementing your own `IEnvironmentNameProvider`.