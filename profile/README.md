8## Hi there 👋

<!--
**Ecoo240337/.github** is a ✨ _special_ ✨ repository because its `profile/README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
- uses: actions/setup-node@v4
  with:
    # Version Spec of the version to use in SemVer notation.
    # It also admits such aliases as lts/*, latest, nightly and canary builds
    # Examples: 12.x, 10.15.1, >=10.15.0, lts/Hydrogen, 16-nightly, latest, node
    node-version: ''

    # File containing the version Spec of the version to use.  Examples: package.json, .nvmrc, .node-version, .tool-versions.
    # If node-version and node-version-file are both provided the action will use version from node-version. 
    node-version-file: ''

    # Set this option if you want the action to check for the latest available version 
    # that satisfies the version spec.
    # It will only get affect for lts Nodejs versions (12.x, >=10.15.0, lts/Hydrogen). 
    # Default: false
    check-latest: false

    # Target architecture for Node to use. Examples: x86, x64. Will use system architecture by default.
    # Default: ''. The action use system architecture by default 
    architecture: ''

    # Used to pull node distributions from https://github.com/actions/node-versions. 
    # Since there's a default, this is typically not supplied by the user. 
    # When running this action on github.com, the default value is sufficient. 
    # When running on GHES, you can pass a personal access token for github.com if you are experiencing rate limiting.
    #
    # We recommend using a service account with the least permissions necessary. Also
    # when generating a new PAT, select the least scopes necessary.
    #
    # [Learn more about creating and using encrypted secrets](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/creating-and-using-encrypted-secrets)
    #
    # Default: ${{ github.server_url == 'https://github.com' && github.token || '' }}
    token: ''

    # Used to specify a package manager for caching in the default directory. Supported values: npm, yarn, pnpm.
    # Package manager should be pre-installed
    # Default: ''
    cache: ''

    # Used to specify the path to a dependency file: package-lock.json, yarn.lock, etc. 
    # It will generate hash from the target file for primary key. It works only If cache is specified.  
    # Supports wildcards or a list of file names for caching multiple dependencies.
    # Default: ''
    cache-dependency-path: ''

    # Optional registry to set up for auth. Will set the registry in a project level .npmrc and .yarnrc file, 
    # and set up auth to read in from env.NODE_AUTH_TOKEN.
    # Default: ''
    registry-url: ''

    # Optional scope for authenticating against scoped registries. 
    # Will fall back to the repository owner when using the GitHub Packages registry (https://npm.pkg.github.com/).
    # Default: ''
    scope: ''

    # Set always-auth option in npmrc file.
    # Default: ''
    always-auth: ''

    # Optional mirror to download binaries from.
    # Artifacts need to match the official Node.js
    # Example:
    # V8 Canaray Build: <mirror_url>/download/v8-canary
    # RC Build: <mirror_url>/download/rc
    # Official: Build <mirror_url>/dist
    # Nightly build: <mirror_url>/download/nightly
    # Default: ''
    mirror: ''

    # Optional mirror token.
    # The token will be used as a bearer token in the Authorization header
    # Default: ''
    mirror-token: ''
