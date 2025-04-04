# Results

- fork: tom-pytel/579bd08e9f4db18fbbe0
- version: 3.14.0a6+
- config: 
- commit hash: [579bd08](https://github.com/tom%2dpytel/cpython/commit/579bd08)
- commit date: 2025-03-30T18:13:59-04:00
- commit merge base: [96ef4c511f3ec763dbb06a1f3c23c658a09403a1](https://github.com/python/cpython/commit/96ef4c511f3ec763dbb06a1f3c23c658a09403a1)
- ref: 579bd08e9f4db18fbbe0

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14264986933)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08.json)

### vs. 3.12.6

- Geometric mean: 1.065x faster (HPT: reliability of 99.78%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-3.12.6.md)
- [📈time plot](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.012x slower (HPT: reliability of 94.06%, 1.00x slower at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-3.13.0rc2.md)
- [📈time plot](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-3.13.0rc2.svg)

