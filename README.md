# DEPRECATED ❗

❗ THIS REPO IS NO LONGER KEPT UP TO DATE. Use https://github.com/recallfuture/furaffinity-api instead! ❗


# fa-node

> The orginal repository is made by insert and can be found [here.](https://gitlab.insrt.uk/insert/furaffinity)
> This is simply a fix to still get images after some website changes (ex. shinies) and is only here to be used in a discord bot.

> FurAffinity wrapper for Node.js

## Usage

To get the most recent content:

```javascript
import { Recent, Type, Login } from 'furaffinity';
// or
let { Recent, Type, Login } = require('furaffinity');

// to allow all results to be accessible, add your cookies
Login("cookie_a", "cookie_b");

Recent(Type.Artwork).then(res => {
  // res is an array of Result(s)
  res[0].getSubmission().then(submission => {
    // submission is a Submission
  });
});
```

Searching for content:

```javascript
import { Search, Type } from 'furaffinity';

Search('search query', { /** SearchOptions */ type?, rating? }).then(res => {
  // res is an array of Result(s)
  res[0].getSubmission().then(submission => {
    // submission is a Submission
  });
});
```

Looking up a specific submission:

```javascript
import { Submission } from 'furaffinity';

Submission('1234567890').then(res => {
  // res is a Submission
});
```
