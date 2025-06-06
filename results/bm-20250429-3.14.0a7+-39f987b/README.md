# Results

- fork: sergey-miryanov/gh_132042_precalc_mr
- version: 3.14.0a7+
- config: 
- commit hash: [39f987b](https://github.com/sergey%2dmiryanov/cpython/commit/39f987b)
- commit date: 2025-04-29T14:34:32+05:00
- commit merge base: [208d06fd515119af49f844c7781e1eb2be8a8add](https://github.com/python/cpython/commit/208d06fd515119af49f844c7781e1eb2be8a8add)
- ref: gh_132042_precalc_mr

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14732097395)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b.json)

### vs. 3.12.6

- Geometric mean: 1.113x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.12.6.md)
- [📈time plot](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 61.63%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base-mem.svg)
- [📄table](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base.md)
- [📈time plot](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14732097395)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b.json)

### vs. 3.12.6

- Geometric mean: 1.102x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.12.6.md)
- [📈time plot](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x faster (HPT: reliability of 53.84%, 1.00x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base-mem.svg)
- [📄table](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base.md)
- [📈time plot](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base.svg)

