# Results

- fork: nascheme/gh_158197_split_dict
- version: 3.16.0a1+dev
- config: CLANG,NOGIL
- commit hash: [703df80](https://github.com/nascheme/cpython/commit/703df80)
- commit date: 2026-10-16T20:57:42-07:00
- commit merge base: [010bebbf9fd12bba1e3f40bdbddacd51a9c2bf20](https://github.com/python/cpython/commit/010bebbf9fd12bba1e3f40bdbddacd51a9c2bf20)
- ref: gh_158197_split_dict

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39328141965)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1%2Bdev-703df80.json)

### vs. 3.12.6

- Geometric mean: 1.133x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1%2Bdev-703df80-vs-3.12.6.md)
- [📈time plot](bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1%2Bdev-703df80-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x faster (HPT: reliability of 79.98%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1%2Bdev-703df80-vs-3.13.0rc2.md)
- [📈time plot](bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1%2Bdev-703df80-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1%2Bdev-703df80-vs-base-mem.svg)
- [📄table](bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1%2Bdev-703df80-vs-base.md)
- [📈time plot](bm-20261016-macm4pro-arm64-nascheme-gh_158197_split_dict-3.16.0a1%2Bdev-703df80-vs-base.svg)

