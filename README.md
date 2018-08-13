# Node.js UUID Benchmark 🐢🚀

The following benchmark results are generated on a MacBook (Early 2016)
with a 1,3 GHz Intel Core m7 processor using Node.js 10.8.0.

To run them your self, run:

```
npm run bench
```

_See raw results in [`results.csv`](results.csv)_

## 128 bit UUID

<!-- AUTOGENERATED - DO NOT EDIT -->
| Method                   | Leaky | Re-use | Sync | Cache | Format |   Ops/sec | RME    | Samples |
| :----------------------- | :---: | :----: | :--: | ----: | :----- | --------: | :----- | ------: |
| [uuid/v1]                |   💦  |        |  ⬇️  |   n/a | uuid   | 1,031,296 | ±1.33% |      93 |
| [uuid/v1]                |   💦  |        |  ⬇️  |   n/a | hex    |   383,579 | ±2.26% |      84 |
| [uuid/v1]                |   💦  |   ♻️   |  ⬇️  |   n/a | hex    |   539,425 | ±1.18% |      92 |
| [uuid/v1]                |   💦  |        |  ⬇️  |   n/a | buffer |   459,584 | ±2.50% |      81 |
| [uuid/v1]                |   💦  |   ♻️   |  ⬇️  |   n/a | buffer |   663,802 | ±1.11% |      91 |
| [uuid/v4]                |       |        |  ⬇️  |   n/a | uuid   |   245,452 | ±2.05% |      84 |
| [uuid/v4]                |       |        |  ⬇️  |   n/a | hex    |   231,759 | ±3.63% |      83 |
| [uuid/v4]                |       |   ♻️   |  ⬇️  |   n/a | hex    |   264,598 | ±3.07% |      89 |
| [uuid/v4]                |       |        |  ⬇️  |   n/a | buffer |   247,127 | ±4.29% |      81 |
| [uuid/v4]                |       |   ♻️   |  ⬇️  |   n/a | buffer |   296,526 | ±3.45% |      87 |
| [fast-uuid]              |   💦  |        |  ⬇️  |   n/a | uuid   |   695,418 | ±0.63% |      91 |
| [uuid-random]            |       |        |  ⬇️  |   512 | uuid   | 1,311,139 | ±0.94% |      90 |
| [uuid-random]            |       |        |  ⬇️  |   512 | hex    | 1,201,270 | ±1.28% |      91 |
| [uuid-random]            |       |        |  ⬇️  |   512 | buffer | 1,754,359 | ±1.64% |      89 |
| [sodium-uuid]            |       |        |  ⬇️  |   n/a | hex    |   229,119 | ±0.82% |      88 |
| [sodium-uuid]            |       |   ♻️   |  ⬇️  |   n/a | hex    |   241,810 | ±0.74% |      94 |
| [sodium-uuid]            |       |        |  ⬇️  |   n/a | buffer |   285,480 | ±0.75% |      95 |
| [sodium-uuid]            |       |   ♻️   |  ⬇️  |   n/a | buffer |   289,556 | ±0.77% |      90 |
| [crypto.randomBytes]     |       |        |      |   n/a | hex    |    35,109 | ±1.73% |      76 |
| [crypto.randomBytes]     |       |        |  ⬇️  |   n/a | hex    |   278,611 | ±2.88% |      85 |
| [crypto.randomBytes]     |       |        |      |   n/a | buffer |    36,940 | ±1.40% |      75 |
| [crypto.randomBytes]     |       |        |  ⬇️  |   n/a | buffer |   314,279 | ±2.89% |      87 |
| [crypto.randomBytes]     |       |        |  ⬇️  |   256 | hex    | 1,041,264 | ±1.31% |      89 |
| [crypto.randomBytes]     |       |   ♻️   |  ⬇️  |   256 | hex    |   940,684 | ±1.83% |      91 |
| [crypto.randomBytes]     |       |        |      |   256 | hex    |   349,677 | ±1.40% |      73 |
| [crypto.randomBytes]     |       |   ♻️   |      |   256 | hex    |   326,977 | ±1.85% |      74 |
| [crypto.randomBytes]     |       |        |  ⬇️  |   256 | buffer | 1,428,595 | ±1.66% |      88 |
| [crypto.randomBytes]     |       |   ♻️   |  ⬇️  |   256 | buffer | 1,304,654 | ±2.53% |      87 |
| [crypto.randomBytes]     |       |        |      |   256 | buffer |   394,225 | ±1.83% |      75 |
| [crypto.randomBytes]     |       |   ♻️   |      |   256 | buffer |   427,429 | ±1.56% |      73 |
| [crypto.randomBytes]     |       |        |  ⬇️  |  4096 | hex    | 1,301,817 | ±0.77% |      90 |
| [crypto.randomBytes]     |       |   ♻️   |  ⬇️  |  4096 | hex    | 1,144,096 | ±0.79% |      90 |
| [crypto.randomBytes]     |       |        |      |  4096 | hex    |   851,989 | ±1.31% |      78 |
| [crypto.randomBytes]     |       |   ♻️   |      |  4096 | hex    |   763,647 | ±2.01% |      68 |
| [crypto.randomBytes]     |       |        |  ⬇️  |  4096 | buffer | 1,752,367 | ±1.98% |      86 |
| [crypto.randomBytes]     |       |   ♻️   |  ⬇️  |  4096 | buffer | 1,723,617 | ±0.95% |      92 |
| [crypto.randomBytes]     |       |        |      |  4096 | buffer | 1,235,274 | ±1.13% |      76 |
| [crypto.randomBytes]     |       |   ♻️   |      |  4096 | buffer | 1,120,800 | ±2.08% |      76 |
| [crypto.randomBytes]     |       |        |  ⬇️  | 65536 | hex    | 1,257,906 | ±0.46% |      89 |
| [crypto.randomBytes]     |       |   ♻️   |  ⬇️  | 65536 | hex    | 1,167,418 | ±1.45% |      81 |
| [crypto.randomBytes]     |       |        |      | 65536 | hex    |   981,184 | ±0.85% |      77 |
| [crypto.randomBytes]     |       |   ♻️   |      | 65536 | hex    |   911,565 | ±1.00% |      78 |
| [crypto.randomBytes]     |       |        |  ⬇️  | 65536 | buffer | 1,896,843 | ±0.77% |      91 |
| [crypto.randomBytes]     |       |   ♻️   |  ⬇️  | 65536 | buffer | 1,799,147 | ±0.56% |      90 |
| [crypto.randomBytes]     |       |        |      | 65536 | buffer | 1,436,612 | ±1.63% |      77 |
| [crypto.randomBytes]     |       |   ♻️   |      | 65536 | buffer | 1,404,341 | ±1.13% |      78 |
| [crypto.randomFillSync]  |       |   ♻️   |  ⬇️  |   n/a | hex    |   318,268 | ±0.81% |      91 |
| [crypto.randomFillSync]  |       |   ♻️   |  ⬇️  |   n/a | buffer |   346,923 | ±1.03% |      93 |
| [crypto.randomFillSync]  |       |        |  ⬇️  |   256 | hex    | 1,062,179 | ±0.40% |      90 |
| [crypto.randomFillSync]  |       |   ♻️   |  ⬇️  |   256 | hex    | 1,029,554 | ±0.86% |      95 |
| [crypto.randomFillSync]  |       |        |  ⬇️  |   256 | buffer | 1,531,608 | ±1.07% |      91 |
| [crypto.randomFillSync]  |       |   ♻️   |  ⬇️  |   256 | buffer | 1,499,337 | ±0.99% |      88 |
| [crypto.randomFillSync]  |       |        |  ⬇️  |  4096 | hex    | 1,315,217 | ±0.90% |      93 |
| [crypto.randomFillSync]  |       |   ♻️   |  ⬇️  |  4096 | hex    | 1,280,109 | ±0.74% |      94 |
| [crypto.randomFillSync]  |       |        |  ⬇️  |  4096 | buffer | 2,052,726 | ±3.75% |      89 |
| [crypto.randomFillSync]  |       |   ♻️   |  ⬇️  |  4096 | buffer | 2,017,966 | ±1.33% |      94 |
| [crypto.randomFillSync]  |       |        |  ⬇️  | 65536 | hex    | 1,419,989 | ±0.49% |      62 |
| [crypto.randomFillSync]  |       |   ♻️   |  ⬇️  | 65536 | hex    | 1,347,480 | ±0.70% |      64 |
| [crypto.randomFillSync]  |       |        |  ⬇️  | 65536 | buffer | 2,222,222 | ±0.85% |      90 |
| [crypto.randomFillSync]  |       |   ♻️   |  ⬇️  | 65536 | buffer | 2,104,368 | ±0.34% |      90 |
| [crypto.randomFill]      |       |   ♻️   |      |   n/a | hex    |    39,516 | ±1.36% |      75 |
| [crypto.randomFill]      |       |   ♻️   |      |   n/a | buffer |    40,831 | ±1.58% |      74 |
| [crypto.randomFill]      |       |        |      |   256 | hex    |   340,626 | ±1.33% |      75 |
| [crypto.randomFill]      |       |   ♻️   |      |   256 | hex    |   321,855 | ±1.24% |      77 |
| [crypto.randomFill]      |       |        |      |   256 | buffer |   408,898 | ±1.31% |      71 |
| [crypto.randomFill]      |       |   ♻️   |      |   256 | buffer |   387,464 | ±1.53% |      73 |
| [crypto.randomFill]      |       |        |      |  4096 | hex    |   867,676 | ±1.33% |      75 |
| [crypto.randomFill]      |       |   ♻️   |      |  4096 | hex    |   850,430 | ±1.07% |      73 |
| [crypto.randomFill]      |       |        |      |  4096 | buffer | 1,246,467 | ±1.42% |      75 |
| [crypto.randomFill]      |       |   ♻️   |      |  4096 | buffer | 1,172,963 | ±1.01% |      78 |
| [crypto.randomFill]      |       |        |      | 65536 | hex    |   974,525 | ±1.20% |      75 |
| [crypto.randomFill]      |       |   ♻️   |      | 65536 | hex    |   917,491 | ±0.90% |      81 |
| [crypto.randomFill]      |       |        |      | 65536 | buffer | 1,465,306 | ±0.89% |      75 |
| [crypto.randomFill]      |       |   ♻️   |      | 65536 | buffer | 1,323,350 | ±1.35% |      77 |
| [/dev/random]            |       |   ♻️   |      |   n/a | hex    |    41,563 | ±1.62% |      75 |
| [/dev/random]            |       |   ♻️   |  ⬇️  |   n/a | hex    |   233,827 | ±1.11% |      88 |
| [/dev/random]            |       |   ♻️   |      |   n/a | buffer |    43,349 | ±2.14% |      68 |
| [/dev/random]            |       |   ♻️   |  ⬇️  |   n/a | buffer |   282,235 | ±1.66% |      86 |
| [/dev/random]            |       |        |      |   256 | hex    |   251,217 | ±1.31% |      76 |
| [/dev/random]            |       |   ♻️   |      |   256 | hex    |   265,264 | ±1.49% |      71 |
| [/dev/random]            |       |   ♻️   |  ⬇️  |   256 | hex    |   482,202 | ±1.13% |      89 |
| [/dev/random]            |       |        |      |   256 | buffer |   280,323 | ±1.27% |      74 |
| [/dev/random]            |       |   ♻️   |      |   256 | buffer |   269,864 | ±1.66% |      64 |
| [/dev/random]            |       |   ♻️   |  ⬇️  |   256 | buffer |   566,258 | ±1.62% |      88 |
| [/dev/random]            |       |        |      |  4096 | hex    |   403,573 | ±1.98% |      72 |
| [/dev/random]            |       |   ♻️   |      |  4096 | hex    |   418,885 | ±1.59% |      70 |
| [/dev/random]            |       |   ♻️   |  ⬇️  |  4096 | hex    |   505,192 | ±1.79% |      84 |
| [/dev/random]            |       |        |      |  4096 | buffer |   476,947 | ±0.98% |      76 |
| [/dev/random]            |       |   ♻️   |      |  4096 | buffer |   470,936 | ±1.29% |      73 |
| [/dev/random]            |       |   ♻️   |  ⬇️  |  4096 | buffer |   634,133 | ±0.95% |      88 |
| [/dev/random]            |       |        |      | 65536 | hex    |   434,931 | ±1.39% |      75 |
| [/dev/random]            |       |   ♻️   |      | 65536 | hex    |   456,504 | ±1.96% |      73 |
| [/dev/random]            |       |   ♻️   |  ⬇️  | 65536 | hex    |   579,672 | ±1.37% |      33 |
| [/dev/random]            |       |        |      | 65536 | buffer |   512,601 | ±1.22% |      73 |
| [/dev/random]            |       |   ♻️   |      | 65536 | buffer |   555,446 | ±1.64% |      53 |
| [/dev/random]            |       |   ♻️   |  ⬇️  | 65536 | buffer |   632,153 | ±1.13% |      86 |
| [/dev/urandom]           |   💦  |   ♻️   |      |   n/a | hex    |    42,691 | ±2.08% |      72 |
| [/dev/urandom]           |   💦  |   ♻️   |  ⬇️  |   n/a | hex    |   240,259 | ±1.19% |      91 |
| [/dev/urandom]           |   💦  |   ♻️   |      |   n/a | buffer |    44,807 | ±1.63% |      75 |
| [/dev/urandom]           |   💦  |   ♻️   |  ⬇️  |   n/a | buffer |   288,069 | ±0.45% |      94 |
| [/dev/urandom]           |   💦  |        |      |   256 | hex    |   260,989 | ±1.81% |      72 |
| [/dev/urandom]           |   💦  |   ♻️   |      |   256 | hex    |   254,373 | ±2.54% |      74 |
| [/dev/urandom]           |   💦  |   ♻️   |  ⬇️  |   256 | hex    |   482,135 | ±1.10% |      91 |
| [/dev/urandom]           |   💦  |        |      |   256 | buffer |   284,213 | ±1.25% |      78 |
| [/dev/urandom]           |   💦  |   ♻️   |      |   256 | buffer |   285,990 | ±1.72% |      74 |
| [/dev/urandom]           |   💦  |   ♻️   |  ⬇️  |   256 | buffer |   548,637 | ±0.59% |      90 |
| [/dev/urandom]           |   💦  |        |      |  4096 | hex    |   403,408 | ±1.91% |      76 |
| [/dev/urandom]           |   💦  |   ♻️   |      |  4096 | hex    |   468,630 | ±1.10% |      52 |
| [/dev/urandom]           |   💦  |   ♻️   |  ⬇️  |  4096 | hex    |   519,458 | ±0.69% |      91 |
| [/dev/urandom]           |   💦  |        |      |  4096 | buffer |   522,863 | ±1.27% |      53 |
| [/dev/urandom]           |   💦  |   ♻️   |      |  4096 | buffer |   464,222 | ±1.47% |      77 |
| [/dev/urandom]           |   💦  |   ♻️   |  ⬇️  |  4096 | buffer |   620,019 | ±3.20% |      88 |
| [/dev/urandom]           |   💦  |        |      | 65536 | hex    |   452,933 | ±1.78% |      75 |
| [/dev/urandom]           |   💦  |   ♻️   |      | 65536 | hex    |   458,316 | ±1.48% |      72 |
| [/dev/urandom]           |   💦  |   ♻️   |  ⬇️  | 65536 | hex    |   618,625 | ±1.38% |      35 |
| [/dev/urandom]           |   💦  |        |      | 65536 | buffer |   527,979 | ±1.60% |      75 |
| [/dev/urandom]           |   💦  |   ♻️   |      | 65536 | buffer |   529,828 | ±2.04% |      71 |
| [/dev/urandom]           |   💦  |   ♻️   |  ⬇️  | 65536 | buffer |   679,038 | ±0.82% |      91 |
<!-- AUTOGENERATED - DO NOT EDIT -->

## Non UUID

The following ID generators does not generate 128 bit id's. Beware that
not all of them are globally unique.

<!-- AUTOGENERATED - DO NOT EDIT -->
| Method               | GUID | Leaky | Re-use | Sync | Cache |   Ops/sec | RME    | Samples | Example                                         |
| :------------------- | :--: | :---: | :----: | :--: | ----: | --------: | :----- | ------: | :---------------------------------------------- |
| [hyperid] cold start |      |   💦  |        |  ⬇️  |   n/a |   101,063 | ±1.53% |      87 | <sub><sub>IBlfHWEYSoSPKWIsvtWjFQ/0</sub></sub>  |
| [hyperid] normal     |      |   💦  |        |  ⬇️  |   n/a | 8,617,328 | ±1.79% |      83 | <sub><sub>IBlfHWEYSoSPKWIsvtWjFQ/0</sub></sub>  |
| [cuid]               |      |   💦  |        |  ⬇️  |   n/a |   436,592 | ±1.02% |      90 | <sub><sub>cjks1ispr0000zqhgbj2pjyqu</sub></sub> |
| [shortid]            |      |   💦  |        |  ⬇️  |   n/a |    22,376 | ±3.16% |      83 | <sub><sub>7iuRccbK6</sub></sub>                 |
| [nanoid]             |      |       |        |  ⬇️  |   n/a |   229,452 | ±1.71% |      87 | <sub><sub>A9WqtIdF0ELW_MiGIJ35O</sub></sub>     |
<!-- AUTOGENERATED - DO NOT EDIT -->

## Legend

- **Method:** Name of npm module, Node.js core function, or OS based random generator used
- **GUID:** Indicates that the ID is globally unique
- **Leaky:** Indicates that the method used to generate the 128 bit number leak metadata
- **Format:**
  - `uuid` - ID is a UUID formatted string representing a 128 bit number, e.g. `3a017fc5-4f50-4db9-b0ce-4547ba0a1bfd`
  - `hex` - ID is a hex formatted string representing a 128 bit number, e.g. `3a017fc54f504db9b0ce4547ba0a1bfd`
  - `buffer` - ID is a raw 128 bit binary Buffer object
  - `other` - ID is **not** a UUID or 128 bit number, and might not be globally unique
- **Re-use:** Indicates an output buffer was re-used between each test to potentially reduce the number of objects that needed to be created
- **Cache:**
  - `n/a` - Only the amount of bytes required to generate a 128 bit number was read into memory
  - &lt;Number> - Number of bytes read into memory the first time a 128 bit number was requested. Subsequent runs would use the leftover bytes in the cache until it had been depleted, at which time another chunk of bytes would be read into memory
- **Sync:** Indicates that the UUID generation was performed synchronously
- **Ops/sec:** Number of UUID's generated per second
- **RME:** The relative margin of error (expressed as a percentage of the mean)
- **Samples:** Number of runs sampled
- **Example:** Example of a generated ID

## License

[MIT](LICENSE)

[uuid/v1]: https://www.npmjs.com/package/uuid
[uuid/v4]: https://www.npmjs.com/package/uuid
[fast-uuid]: https://www.npmjs.com/package/fast-uuid
[uuid-random]: https://www.npmjs.com/package/uuid-random
[sodium-uuid]: https://www.npmjs.com/package/sodium-uuid
[crypto.randomBytes]: https://nodejs.org/api/crypto.html#crypto_crypto_randombytes_size_callback
[crypto.randomFillSync]: https://nodejs.org/api/crypto.html#crypto_crypto_randomfillsync_buffer_offset_size
[crypto.randomFill]: https://nodejs.org/api/crypto.html#crypto_crypto_randomfill_buffer_offset_size_callback
[/dev/random]: https://en.wikipedia.org/wiki//dev/random
[/dev/urandom]: https://en.wikipedia.org/wiki//dev/random
[hyperid]: https://www.npmjs.com/package/hyperid
[cuid]: https://www.npmjs.com/package/cuid
[shortid]: https://www.npmjs.com/package/shortid
[nanoid]: https://www.npmjs.com/package/nanoid
