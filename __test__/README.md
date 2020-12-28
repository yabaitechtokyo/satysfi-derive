# Notes on regression tests

## How to run them

You need to install [SATySFi](https://github.com/gfngfn/SATySFi), [Yarn](https://yarnpkg.com/lang/en/docs/install), and [diff-pdf](https://github.com/vslavik/diff-pdf).

```shell
$ yarn install  # install dependencies
$ yarn test     # run test
```

## How to keep them updated

The existing tests stores current expected output as `__pdf_snapshots__`.
If you changed some feature and pdf output get different from snapshots, diffs between new output and snapshots would be put into `__tests__/__pdf_snapshots__/__diff_output__`.

Check them out and see if they are acceptable. If you think they are okay, you can just run `yarn test --updateSnapshot` to update snapshots.
