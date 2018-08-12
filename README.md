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
| Method | Leaky | Format | Re-use | Cache | Sync | Ops/sec | RME | Samples |
|--------|-------|--------|--------|-------|------|---------|-----|---------|
| [uuid/v1]  | 💦 | uuid |  | n/a | ✅ | 1,010,728 | ±1.21% | 90 |
| [uuid/v1]  | 💦 | hex |  | n/a | ✅ | 361,508 | ±1.16% | 86 |
| [uuid/v1]  | 💦 | hex | ✅ | n/a | ✅ | 454,132 | ±1.06% | 90 |
| [uuid/v1]  | 💦 | buffer |  | n/a | ✅ | 399,189 | ±2.58% | 84 |
| [uuid/v1]  | 💦 | buffer | ✅ | n/a | ✅ | 584,416 | ±0.67% | 90 |
| [uuid/v4]  |  | uuid |  | n/a | ✅ | 217,428 | ±2.16% | 85 |
| [uuid/v4]  |  | hex |  | n/a | ✅ | 208,469 | ±4.21% | 83 |
| [uuid/v4]  |  | hex | ✅ | n/a | ✅ | 245,745 | ±3.01% | 90 |
| [uuid/v4]  |  | buffer |  | n/a | ✅ | 232,072 | ±4.59% | 84 |
| [uuid/v4]  |  | buffer | ✅ | n/a | ✅ | 278,945 | ±3.37% | 86 |
| [fast-uuid]  | 💦 | uuid |  | n/a | ✅ | 628,870 | ±0.64% | 94 |
| [uuid-random]  |  | uuid |  | 512 | ✅ | 1,203,369 | ±0.51% | 94 |
| [uuid-random]  |  | hex |  | 512 | ✅ | 1,163,045 | ±0.54% | 92 |
| [uuid-random]  |  | buffer |  | 512 | ✅ | 1,706,416 | ±0.95% | 92 |
| [sodium-uuid]  |  | hex |  | n/a | ✅ | 218,952 | ±0.49% | 94 |
| [sodium-uuid]  |  | hex | ✅ | n/a | ✅ | 221,198 | ±0.66% | 95 |
| [sodium-uuid]  |  | buffer |  | n/a | ✅ | 258,064 | ±0.45% | 94 |
| [sodium-uuid]  |  | buffer | ✅ | n/a | ✅ | 258,461 | ±0.50% | 95 |
| [crypto.randomBytes]  |  | hex |  | n/a |  | 37,157 | ±1.32% | 74 |
| [crypto.randomBytes]  |  | hex |  | n/a | ✅ | 247,885 | ±2.97% | 85 |
| [crypto.randomBytes]  |  | buffer |  | n/a |  | 38,669 | ±1.18% | 78 |
| [crypto.randomBytes]  |  | buffer |  | n/a | ✅ | 280,483 | ±3.26% | 84 |
| [crypto.randomBytes]  |  | hex |  | 256 | ✅ | 925,363 | ±1.47% | 87 |
| [crypto.randomBytes]  |  | hex | ✅ | 256 | ✅ | 881,535 | ±1.18% | 89 |
| [crypto.randomBytes]  |  | hex |  | 256 |  | 322,356 | ±1.30% | 75 |
| [crypto.randomBytes]  |  | hex | ✅ | 256 |  | 329,935 | ±1.14% | 73 |
| [crypto.randomBytes]  |  | buffer |  | 256 | ✅ | 1,280,254 | ±0.81% | 93 |
| [crypto.randomBytes]  |  | buffer | ✅ | 256 | ✅ | 1,251,967 | ±1.59% | 92 |
| [crypto.randomBytes]  |  | buffer |  | 256 |  | 368,950 | ±0.82% | 77 |
| [crypto.randomBytes]  |  | buffer | ✅ | 256 |  | 358,403 | ±1.54% | 76 |
| [crypto.randomBytes]  |  | hex |  | 4096 | ✅ | 1,226,660 | ±0.21% | 95 |
| [crypto.randomBytes]  |  | hex | ✅ | 4096 | ✅ | 1,134,007 | ±0.82% | 90 |
| [crypto.randomBytes]  |  | hex |  | 4096 |  | 784,679 | ±1.82% | 77 |
| [crypto.randomBytes]  |  | hex | ✅ | 4096 |  | 796,862 | ±1.34% | 77 |
| [crypto.randomBytes]  |  | buffer |  | 4096 | ✅ | 1,832,142 | ±0.46% | 91 |
| [crypto.randomBytes]  |  | buffer | ✅ | 4096 | ✅ | 1,694,581 | ±1.26% | 92 |
| [crypto.randomBytes]  |  | buffer |  | 4096 |  | 1,190,011 | ±1.25% | 72 |
| [crypto.randomBytes]  |  | buffer | ✅ | 4096 |  | 1,079,299 | ±1.88% | 78 |
| [crypto.randomBytes]  |  | hex |  | 65536 | ✅ | 1,231,223 | ±1.17% | 82 |
| [crypto.randomBytes]  |  | hex | ✅ | 65536 | ✅ | 1,093,792 | ±2.31% | 81 |
| [crypto.randomBytes]  |  | hex |  | 65536 |  | 915,463 | ±1.18% | 79 |
| [crypto.randomBytes]  |  | hex | ✅ | 65536 |  | 899,184 | ±1.41% | 76 |
| [crypto.randomBytes]  |  | buffer |  | 65536 | ✅ | 1,717,668 | ±6.39% | 84 |
| [crypto.randomBytes]  |  | buffer | ✅ | 65536 | ✅ | 1,730,798 | ±1.47% | 79 |
| [crypto.randomBytes]  |  | buffer |  | 65536 |  | 1,374,223 | ±1.18% | 79 |
| [crypto.randomBytes]  |  | buffer | ✅ | 65536 |  | 1,297,745 | ±1.10% | 79 |
| [crypto.randomFillSync]  |  | hex | ✅ | n/a | ✅ | 295,257 | ±1.47% | 90 |
| [crypto.randomFillSync]  |  | buffer | ✅ | n/a | ✅ | 334,193 | ±1.70% | 90 |
| [crypto.randomFillSync]  |  | hex |  | 256 | ✅ | 920,767 | ±6.47% | 81 |
| [crypto.randomFillSync]  |  | hex | ✅ | 256 | ✅ | 994,415 | ±1.32% | 89 |
| [crypto.randomFillSync]  |  | buffer |  | 256 | ✅ | 1,487,325 | ±1.61% | 87 |
| [crypto.randomFillSync]  |  | buffer | ✅ | 256 | ✅ | 1,472,371 | ±1.36% | 90 |
| [crypto.randomFillSync]  |  | hex |  | 4096 | ✅ | 1,283,295 | ±1.37% | 92 |
| [crypto.randomFillSync]  |  | hex | ✅ | 4096 | ✅ | 1,227,543 | ±1.73% | 91 |
| [crypto.randomFillSync]  |  | buffer |  | 4096 | ✅ | 2,075,880 | ±1.58% | 87 |
| [crypto.randomFillSync]  |  | buffer | ✅ | 4096 | ✅ | 1,971,822 | ±1.33% | 94 |
| [crypto.randomFillSync]  |  | hex |  | 65536 | ✅ | 1,296,499 | ±1.42% | 91 |
| [crypto.randomFillSync]  |  | hex | ✅ | 65536 | ✅ | 1,318,609 | ±1.40% | 63 |
| [crypto.randomFillSync]  |  | buffer |  | 65536 | ✅ | 2,050,087 | ±1.53% | 88 |
| [crypto.randomFillSync]  |  | buffer | ✅ | 65536 | ✅ | 1,830,577 | ±1.18% | 89 |
| [crypto.randomFill]  |  | hex | ✅ | n/a |  | 37,195 | ±1.23% | 76 |
| [crypto.randomFill]  |  | buffer | ✅ | n/a |  | 39,665 | ±1.37% | 75 |
| [crypto.randomFill]  |  | hex |  | 256 |  | 323,895 | ±1.33% | 77 |
| [crypto.randomFill]  |  | hex | ✅ | 256 |  | 324,126 | ±1.33% | 76 |
| [crypto.randomFill]  |  | buffer |  | 256 |  | 370,563 | ±1.65% | 76 |
| [crypto.randomFill]  |  | buffer | ✅ | 256 |  | 370,313 | ±1.23% | 77 |
| [crypto.randomFill]  |  | hex |  | 4096 |  | 794,552 | ±1.45% | 74 |
| [crypto.randomFill]  |  | hex | ✅ | 4096 |  | 800,702 | ±1.30% | 75 |
| [crypto.randomFill]  |  | buffer |  | 4096 |  | 1,137,689 | ±1.44% | 78 |
| [crypto.randomFill]  |  | buffer | ✅ | 4096 |  | 1,080,769 | ±1.35% | 73 |
| [crypto.randomFill]  |  | hex |  | 65536 |  | 905,386 | ±0.95% | 77 |
| [crypto.randomFill]  |  | hex | ✅ | 65536 |  | 881,036 | ±1.26% | 78 |
| [crypto.randomFill]  |  | buffer |  | 65536 |  | 1,418,688 | ±1.02% | 73 |
| [crypto.randomFill]  |  | buffer | ✅ | 65536 |  | 1,303,381 | ±1.44% | 77 |
| [/dev/random]  |  | hex | ✅ | n/a |  | 39,425 | ±1.59% | 75 |
| [/dev/random]  |  | hex | ✅ | n/a | ✅ | 224,243 | ±1.56% | 91 |
| [/dev/random]  |  | buffer | ✅ | n/a |  | 42,582 | ±0.87% | 77 |
| [/dev/random]  |  | buffer | ✅ | n/a | ✅ | 260,796 | ±1.44% | 92 |
| [/dev/random]  |  | hex |  | 256 |  | 234,600 | ±0.82% | 77 |
| [/dev/random]  |  | hex | ✅ | 256 |  | 235,844 | ±1.39% | 77 |
| [/dev/random]  |  | hex | ✅ | 256 | ✅ | 433,351 | ±1.46% | 94 |
| [/dev/random]  |  | buffer |  | 256 |  | 255,461 | ±0.81% | 77 |
| [/dev/random]  |  | buffer | ✅ | 256 |  | 248,054 | ±1.30% | 76 |
| [/dev/random]  |  | buffer | ✅ | 256 | ✅ | 515,650 | ±1.29% | 91 |
| [/dev/random]  |  | hex |  | 4096 |  | 383,202 | ±1.38% | 76 |
| [/dev/random]  |  | hex | ✅ | 4096 |  | 374,830 | ±1.30% | 79 |
| [/dev/random]  |  | hex | ✅ | 4096 | ✅ | 475,687 | ±1.24% | 94 |
| [/dev/random]  |  | buffer |  | 4096 |  | 459,233 | ±1.22% | 69 |
| [/dev/random]  |  | buffer | ✅ | 4096 |  | 445,995 | ±1.33% | 74 |
| [/dev/random]  |  | buffer | ✅ | 4096 | ✅ | 565,852 | ±1.24% | 92 |
| [/dev/random]  |  | hex |  | 65536 |  | 410,640 | ±1.25% | 75 |
| [/dev/random]  |  | hex | ✅ | 65536 |  | 403,011 | ±1.46% | 77 |
| [/dev/random]  |  | hex | ✅ | 65536 | ✅ | 522,898 | ±1.89% | 30 |
| [/dev/random]  |  | buffer |  | 65536 |  | 469,559 | ±1.70% | 77 |
| [/dev/random]  |  | buffer | ✅ | 65536 |  | 511,500 | ±1.62% | 49 |
| [/dev/random]  |  | buffer | ✅ | 65536 | ✅ | 571,189 | ±1.06% | 81 |
| [/dev/urandom]  | 💦 | hex | ✅ | n/a |  | 40,497 | ±1.02% | 75 |
| [/dev/urandom]  | 💦 | hex | ✅ | n/a | ✅ | 223,469 | ±1.30% | 93 |
| [/dev/urandom]  | 💦 | buffer | ✅ | n/a |  | 42,288 | ±1.00% | 75 |
| [/dev/urandom]  | 💦 | buffer | ✅ | n/a | ✅ | 260,256 | ±1.28% | 91 |
| [/dev/urandom]  | 💦 | hex |  | 256 |  | 236,374 | ±1.11% | 75 |
| [/dev/urandom]  | 💦 | hex | ✅ | 256 |  | 225,028 | ±1.41% | 77 |
| [/dev/urandom]  | 💦 | hex | ✅ | 256 | ✅ | 436,857 | ±1.47% | 89 |
| [/dev/urandom]  | 💦 | buffer |  | 256 |  | 256,362 | ±1.73% | 75 |
| [/dev/urandom]  | 💦 | buffer | ✅ | 256 |  | 260,655 | ±1.48% | 77 |
| [/dev/urandom]  | 💦 | buffer | ✅ | 256 | ✅ | 461,768 | ±8.84% | 83 |
| [/dev/urandom]  | 💦 | hex |  | 4096 |  | 391,269 | ±1.29% | 65 |
| [/dev/urandom]  | 💦 | hex | ✅ | 4096 |  | 378,844 | ±1.23% | 77 |
| [/dev/urandom]  | 💦 | hex | ✅ | 4096 | ✅ | 468,003 | ±1.54% | 89 |
| [/dev/urandom]  | 💦 | buffer |  | 4096 |  | 488,849 | ±1.25% | 51 |
| [/dev/urandom]  | 💦 | buffer | ✅ | 4096 |  | 435,512 | ±1.43% | 75 |
| [/dev/urandom]  | 💦 | buffer | ✅ | 4096 | ✅ | 529,692 | ±1.34% | 89 |
| [/dev/urandom]  | 💦 | hex |  | 65536 |  | 386,841 | ±1.44% | 77 |
| [/dev/urandom]  | 💦 | hex | ✅ | 65536 |  | 402,166 | ±1.44% | 73 |
| [/dev/urandom]  | 💦 | hex | ✅ | 65536 | ✅ | 514,504 | ±1.35% | 30 |
| [/dev/urandom]  | 💦 | buffer |  | 65536 |  | 460,235 | ±1.65% | 74 |
| [/dev/urandom]  | 💦 | buffer | ✅ | 65536 |  | 479,469 | ±1.46% | 70 |
| [/dev/urandom]  | 💦 | buffer | ✅ | 65536 | ✅ | 608,736 | ±2.01% | 18 |
<!-- AUTOGENERATED - DO NOT EDIT -->

## Non UUID

The following ID generators does not generate 128 bit id's. Beware that
not all of them are globally unique.

<!-- AUTOGENERATED - DO NOT EDIT -->
| Method | GID | Leaky | Re-use | Cache | Sync | Ops/sec | RME | Samples | Example |
|--------|-----|-------|--------|-------|------|---------|-----|---------|---------|
| [hyperid] cold start | ✅ | 💦 |  | n/a | ✅ | 103,950 | ±0.83% | 85 | <sub><sub>+9954GT6QCyWQ9IWLj1aYw/0</sub></sub> |
| [hyperid] normal | ✅ | 💦 |  | n/a | ✅ | 8,524,478 | ±1.79% | 85 | <sub><sub>+9954GT6QCyWQ9IWLj1aYw/0</sub></sub> |
| [cuid]  | ✅ | 💦 |  | n/a | ✅ | 427,411 | ±0.60% | 91 | <sub><sub>cjkrb16860000wuhgjes1dah2</sub></sub> |
| [shortid]  |  | 💦 |  | n/a | ✅ | 22,657 | ±3.84% | 81 | <sub><sub>6R4giSs0O</sub></sub> |
<!-- AUTOGENERATED - DO NOT EDIT -->

## Legend

- **Method:** Name of npm module, Node.js core function, or OS based random generator used
- **GID:** Indicates that the ID is globally unique
- **Leaky:** Indicates that the method used to generate the 128 bit number doesn't leak metadata
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
