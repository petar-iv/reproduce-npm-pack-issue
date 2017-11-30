# reproduce-npm-pack-issue

The issue can be reproduced with npm v5.5.1.
Execute `npm install` and then `npm pack`.
For convenience, the archive resulting from `npm pack` is part of the repository.

According to the [npm docu](https://docs.npmjs.com/files/package-lock.json): _"One key detail about package-lock.json is that it cannot be published ..."_.
One would expect that, even if _package-lock.json_ is present in the _"files"_ property in _package.json_, this file would not be present in the archieve produced with `npm pack` (as it is with _node_modules_).
