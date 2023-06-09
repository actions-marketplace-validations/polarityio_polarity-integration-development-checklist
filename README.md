# Polarity Integration Development Checklist action

Checks a list of requirements found in the Polarity Integration Development Checklist.  This currently includes:
- LICENSE File Checks 
  - Verifying the LICENSE file exists
- .prettierrc File Checks 
  - Verifying the .prettierrc file exists
- .gitignore File Checks 
  - Verifying the .gitignore file exists
- README.md File Checks 
  - Verifying the README.md file exists
- config.js File Checks 
  - Verifying Logging Level is set to `info`
  - Verifying `defaultColor` property has a value set
  - Verifying Request Options are set correctly including
    - `cert`, `key`, `passphrase`, `ca`, and `proxy` all having the value `''`
  - Verifying all Integration Options have a description containing content
- package.json File Checks 
  - Verifying the package.json file exists
  - Verifying the `private` flag is set to true
  - Verifying the `version` property matches standard semantic versioning format
  - Checks to see if the current `version` property already exists as a release on Github.
- package-lock.json File Checks 
  - Verifying the package-lock.json file exists
  - Verifying the package-lock.json file `version` property matches the `version` property found in the package.json file
  

## Inputs

### `GITHUB_TOKEN`

**Required** Your secrets github token `${{ secrets.GITHUB_TOKEN }}`.


## Example Step

```yaml
- uses: actions/checkout@v2
- name: Polarity Integration Development Checklist
  id: int-dev-checklist
  uses: polarityio/polarity-integration-development-checklist@v1.0.0
  with:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
