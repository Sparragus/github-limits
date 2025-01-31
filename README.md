# GitHub limits

A collection of various string/numeric limits with GitHub. Not all of these are publicly documented, but I'd like to change that.

*Note: these do **not** include things like [GraphQL resource limits](https://developer.github.com/v4/guides/resource-limitations/), [REST rate limits](https://developer.github.com/v3/rate_limit/) and [disk quotas](https://help.github.com/articles/what-is-my-disk-quota/), things that are about resource usage, rather than simple strings or numbers.*

## List of limits

Each limit carries the full set of relevant restrictions, as well as where I gained the information from.

#### Usernames

- Max length: 39 characters
- All characters must be either a hyphen (`-`) or alphanumeric
- Cannot start with a hyphen
- Cannot include consecutive hyphens
- Cannot be [a reserved name](https://github.com/Mottie/github-reserved-names)
- Must be globally unique

*This was verified through checking validation messages when attempting to create an account.*

#### Organization names

- Max length: 39 characters
- All characters must be either a hyphen (`-`) or alphanumeric
- Cannot start with a hyphen
- Cannot include consecutive hyphens
- Cannot be [a reserved name](https://github.com/Mottie/github-reserved-names)
- Must be globally unique

*This was verified through checking validation messages when attempting to create an organization.*

#### Team names

- Max length: 255 characters
- All characters must be either a hyphen (`-`) or alphanumeric
- Must be unique per-organization

Note: longer team names will still validate, they will just be truncated.

*This was verified through a support email.*

#### Repository names

- Max length: 100 characters
- All characters must be either a hyphen (`-`), a period (`.`), or alphanumeric
- Must be unique per-user and/or per-organization

*This was verified through checking automatically-generated aliases with repository names.*

#### Issue/pull request numbers

- Max value: 1073741824 (max 4-byte Ruby integer)
- Min value: 1

*The first was verified through a support email. The second was verified by creating an issue in an empty repo.*

## Contributing

If you find limits to something not listed here, please feel free to [file an issue](https://github.com/isiahmeadows/github-limits/issues/new) with details about the limits. Alternatively, you could [edit this file](https://github.com/isiahmeadows/github-limits/edit/master/README.md) and file a pull request. I do need three things for each entry, though:

- The entry itself.
- Any relevant constraints, including max length, permitted characters, etc.
- How you figured out the relevant constraints.

Also, these are only confirmed with the public GitHub site. If there's a different set of limits for private data and/or enterprise setups, I'd love to have those.

## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
