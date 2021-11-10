## rust-web-server-mustache
Template for generating rust web base on Mustache.

## How to use
Use [rust-web-server-cli](https://github.com/SimonOsaka/rust-web-server-cli) to generate code.

## Template Variable
### package_name
- `{{#repository}}{{package_name}}{{/repository}}`: repository package name
- `{{#domain}}{{package_name}}{{/domain}}`: domain package name
- `{{#auth}}{{package_name}}{{/auth}}`: auth package name
- `{{#types}}{{package_name}}{{/types}}`: types package name

... other variables see [mustache.config.toml](https://github.com/SimonOsaka/rust-web-server-cli/blob/main/mustache.config.toml)

for example:
```toml
[domain]
package_name = "jdomain"
member_name = "just_domain"
```
represent
```
{{#domain}}{{package_name}}{{/domain}} // value is `jdomain`
{{#domain}}{{member_name}}{{/domain}}  // value is `just_domain`
```