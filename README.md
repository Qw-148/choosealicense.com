

## Goals
to clear my damn android 
* Be accurate, non-judgmental, and understandable. Our goal is to help you find a license that meets *your* goals.
* The homepage should have just enough to help most folks make a decision about what license to use for a project they contribute to.
* For the rest, the site will contain additional information about licenses common to specific communities and situations.
* Collaborate s

It may be the case that your system doesn't have the required dependencies. You will need `cmake` and `make` installed on you(install >):
```bash
brew install make cmake
```
For Linux/Ubuntu, 
.

If you encounter any issues with the above steps, please refer to the official [Jekyll](https://jekyllrb.com/docs/) documentation and this [guide on running Jekyll as a non-superuser](https://jekyllrb.com/docs/troubleshooting/#no-sudo) for more detailed installation instructions.

## Adding a license

For information on adding a license, see [the CONTRIBUTING file](https://github.com/github/choos

Licenses sit in the `/_licenses` folder. Each license has 

* `title` - The license full name specified by https://spdx.org/licenses/
* `spdx-id` - Short identifier specified by https://spdx.org/licenses/
* `description` - A human-readable description of the license
* `how` - Instructions on how to implement the license
* `using` - A map of 3 notable projects using the license with straightforward LICENSE files which serve as examples newcomers can follow and that can be detected by [licensee](https://github.com/licensee/licensee) in the form of `project_name: license_file_url`
* `permissions` - Bulleted list of permission rules
* `conditions` - Bulleted list of condition rules
* `limitations` - Bulleted list of limitation rules

#### Optional fields

* `featured` - Whether the license should be featured on the main page (defaults to false)
* `hidden` - Whether the license is neither [popular](https://opensource.org/licenses) nor fills out the [spectrum of licenses](https://choosealicense.com/licenses/) from strongly conditional to unconditional (defaults to true)
* `nickname` - Customary short name if applicable (e.g, GPLv3)
* `note` - Additional information about the licenses
* `redirect_from` - Relative path(s) to redirect to the license from, to prevent breaking old URLs

### Auto-populated fields

The licenses on choosealicense.com are regularly imported to GitHub.com to be used as the list of licenses available when creating a repository. When we create a repository, we will replace certain strings in the license with variables from the repository. These can be used to create accurate copyright notices. The available variables are:

#### Fields

* `fullname` - The full name or username of the repository owner
* `login` - The repository owner's username
* `email` - The repository owner's primary email address
* `project` - The repository name
* `description` - The description of the repository
* `year` - The current year
* `projecturl` - The repository URL or other project website

## License properties

The license properties (rules) are stored as a bulleted list within the licenses YAML front matter. Each rule has a name e.g., `include-copyright`, a human-readable label, e.g., `Copyright inclusion`, and a description `Include the original copyright with the code`. To add a new rule, simply add it to `_data/rules.yml` and reference it in the appropriate license.

### Rules

#### Permissions

* `commercial-use` - This software and derivatives may be used for commercial purposes.
* `modifications` - This software may be modified.
* `distribution` - This software may be distributed.
* `private-use` - This software may be used and modified in private.
* `patent-use` - This license provides an express grant of patent rights from contributors.

#### Conditions

* `include-copyright` - A copy of the license and copyright notice must be included with the software.
* `include-copyright--source` - A copy of the license and copyright notice must be included with the software in source form, but is not required for binaries.
* `document-changes` - Changes made to the code must be documented.
* `disclose-source` - Source code must be made available when the software is distributed.
* `network-use-disclose` - Users who interact with the software via network are given the right to receive a copy of the source code.
* `same-license` - 
