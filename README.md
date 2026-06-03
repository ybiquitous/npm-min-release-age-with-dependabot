# npm `min-release-age` option with Dependabot

Dependabot respects `min-release-age` in [`.npmrc`](.npmrc).

See the Dependabot log:

```
updater | 2026/06/03 10:11:28 INFO <job_1395035059> Checking if which 6.0.1 needs updating
  proxy | 2026/06/03 10:11:28 [016] GET https://registry.npmjs.org:443/which
  proxy | 2026/06/03 10:11:28 [016] 200 https://registry.npmjs.org:443/which
updater | 2026/06/03 10:11:29 INFO <job_1395035059> Filtered out 1 versions due to cooldown
  proxy | 2026/06/03 10:11:29 [018] HEAD https://registry.npmjs.org:443/which/-/which-7.0.0.tgz
  proxy | 2026/06/03 10:11:29 [018] 200 https://registry.npmjs.org:443/which/-/which-7.0.0.tgz
updater | 2026/06/03 10:11:29 INFO <job_1395035059> Filtered out 1 versions due to cooldown
updater | 2026/06/03 10:11:29 INFO <job_1395035059> Filtered out 1 versions due to cooldown
  proxy | 2026/06/03 10:11:29 [020] HEAD https://registry.npmjs.org:443/which/-/which-6.0.1.tgz
  proxy | 2026/06/03 10:11:29 [020] 200 https://registry.npmjs.org:443/which/-/which-6.0.1.tgz
updater | 2026/06/03 10:11:29 INFO <job_1395035059> Latest version is 6.0.1
updater | 2026/06/03 10:11:29 INFO <job_1395035059> No update needed for which 6.0.1
```

Ref: <https://github.com/ybiquitous/npm-min-release-age-with-dependabot/actions/runs/26878093411/job/79270693139#step:3:165>

Dependabot found `which-7.0.0` but gave up updating due to `Filtered out 1 versions due to cooldown`.
