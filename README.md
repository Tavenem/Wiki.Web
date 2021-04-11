![build](https://img.shields.io/github/workflow/status/Tavenem/Wiki.Web/publish/main) [![NuGet downloads](https://img.shields.io/nuget/dt/Tavenem.Wiki.Web)](https://www.nuget.org/packages/Tavenem.Wiki.Web/)

Tavenem.Wiki.Web
==

Tavenem.Wiki.Web provides common logic for all web-based implementations of
[Tavenem.Wiki](https://github.com/Tavenem/Wiki). It is used by the
[Tavenem.Wiki.Mvc](https://github.com/Tavenem/Wiki.Mvc) project: the "reference implementation" of
Tavenem.Wiki.

## Installation

Tavenem.Wiki.Web is available as a [NuGet package](https://www.nuget.org/packages/Tavenem.Wiki.Web/).

## Configuration
The `WikiWebOptions` static class includes a number of settable properties which control the
behavior of the wiki.
- `AboutPageTitle`*: The title of the main about page. Default is "About".
- `AdminGroupName`: The name of the admin user group. Default is "Wiki Admins".
- `AdminNamespaces`: An optional collection of namespaces which may not be assigned to pages by
  non-admin users. The namespace assigned to `SystemNamespace` is included automatically.

  Read-only. items can be added with the `AddAdminNamespace` method.
- `ContactPageTitle`*: The title of the main contact page. Default is "Contact".
- `ContentsPageTitle`*: The title of the main contents page. Default is "Contents".
- `CopyrightPageTitle`*: The title of the main copyright page. Default is "Copyright".
- `GroupNamespace`: The name of the user group namespace. Default is "Group".
- `HelpPageTitle`*: The title of the main help page. Default is "Help".
- `MaxFileSize`: The maximum size (in bytes) of uploaded files. Default is 5,000,000 (5 MB).

  Setting this to a value less than or equal to zero effectively prevents file uploads.
- `MaxFileSizeString`: Read-only. Gets a string representing the `MaxFileSize` in a reasonable unit
  (GB for large sizes, down to bytes for small ones).
- `PolicyPageTitle`*: The title of the main policy page. Default is "Policies".
- `SystemNamespace`: The name of the system namespace. Default is "System".
- `UserNamespace`: The name of the user namespace. Default is "User".

**This property may be set to `null` or an empty `string` to disable the associated wiki page.*

## Roadmap

Tavenem.Wiki.Web is currently in a **prerelease** state. Development is ongoing, and breaking
changes are possible before the first production release.

No release date is currently set for v1.0 of Tavenem.Wiki.Web. The project is currently in a "wait
and see" phase while [Tavenem.DataStore](https://github.com/Tavenem/DataStore) (a dependency of
Tavenem.Wiki.Web) is in prerelease. When that project has a stable release, a production release of
Tavenem.Wiki.Web will follow.

## Contributing

Contributions are always welcome. Please carefully read the [contributing](docs/CONTRIBUTING.md) document to learn more before submitting issues or pull requests.

## Code of conduct

Please read the [code of conduct](docs/CODE_OF_CONDUCT.md) before engaging with our community, including but not limited to submitting or replying to an issue or pull request.