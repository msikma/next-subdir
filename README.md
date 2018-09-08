This is a copy of the `with-custom-babel-config` example for Next.js. Originally installed via:

```bash
yarn create next-app --example with-custom-babel-config with-custom-babel-config-app
```

I'm trying to get a monorepo setup working. While working on this I found that running `next` with a subdir does not work like changing directory to the subdir and then running it. Specifically, it does not seem to want to enable our custom Babel config.

Examples:

```bash
yarn next  # runs Next in the current directory, which enables our custom Babel config

cd subdir
yarn next  # runs Next from inside our subdir, which also works

cd ..
yarn next subdir  # runs the Next application inside the subdir, but does not use our custom Babel config
```

