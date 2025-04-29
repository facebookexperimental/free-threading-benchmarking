# Results

- fork: sergey-miryanov/gh_132042_precalc_mr
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [39f987b](https://github.com/sergey%2dmiryanov/cpython/commit/39f987b)
- commit date: 2025-04-29T14:34:32+05:00
- commit merge base: [208d06fd515119af49f844c7781e1eb2be8a8add](https://github.com/python/cpython/commit/208d06fd515119af49f844c7781e1eb2be8a8add)
- ref: gh_132042_precalc_mr

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14732101454)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250429-linux-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 71.43%, 1.00x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250429-linux-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.12.6.md)
- [📈time plot](bm-20250429-linux-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 50.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250429-linux-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250429-linux-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 90.14%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250429-linux-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base-mem.svg)
- [📄table](bm-20250429-linux-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base.md)
- [📈time plot](bm-20250429-linux-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- [📄table](bm-20250429-linux-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250429-linux-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-default_base_vs_NOGIL.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14732101454)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b.json)

### vs. 3.12.6

- Geometric mean: 1.031x faster (HPT: reliability of 62.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.12.6.md)
- [📈time plot](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x slower (HPT: reliability of 85.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x slower (HPT: reliability of 97.70%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base-mem.svg)
- [📄table](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base.md)
- [📈time plot](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.081x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250429-vultr-x86_64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-default_base_vs_NOGIL.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14732101454)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 90.68%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.12.6.md)
- [📈time plot](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.008x faster (HPT: reliability of 82.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x faster (HPT: reliability of 90.82%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base-mem.svg)
- [📄table](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base.md)
- [📈time plot](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.008x slower (HPT: reliability of 98.87%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- [📄table](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250429-macm4pro-arm64-sergey%252dmiryanov-gh_132042_precalc_mr-3.14.0a7%2B-39f987b-vs-default_base_vs_NOGIL.svg)

