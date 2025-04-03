to reproduce the unstable hashes issue:

```
pnpm i
```

```
pnpm build.client
```

Observe the hash name of the last file. Repeat the build a few times. It will change.

Then uncomment the `maxParallelFileOps: 1` line in `vite.config.ts`, and the hash will no longer change.
