# Results vs. 3.12.6

- fork: kumaraditya303
- ref: asyncio_tsafe
- machine: linux-x86_64
- commit hash: 41a86a6
- commit date: 2025-01-01
- overall geometric mean: 1.173x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 352 ms: 1.33x slower                                                    |
| docutils       | 2.64 sec                                               | 3.02 sec: 1.14x slower                                                  |
| html5lib       | 63.6 ms                                                | 93.2 ms: 1.47x slower                                                   |
| Geometric mean | (ref)                                                  | 1.31x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 740 ms: 1.50x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 314 ms: 1.42x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 764 ms: 1.42x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 400 ms: 1.40x faster                                                    |
| async_tree_none            | 464 ms                                                 | 351 ms: 1.32x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 429 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 567 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 599 ms: 1.19x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                    |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                   |
| async_generators           | 384 ms                                                 | 453 ms: 1.18x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 182 ms: 1.01x faster                                                    |
| float          | 80.8 ms                                                | 108 ms: 1.34x slower                                                    |
| nbody          | 89.3 ms                                                | 130 ms: 1.45x slower                                                    |
| Geometric mean | (ref)                                                  | 1.24x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                   |
| regex_dna      | 168 ms                                                 | 187 ms: 1.11x slower                                                    |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.19x slower                                                   |
| regex_compile  | 142 ms                                                 | 171 ms: 1.20x slower                                                    |
| Geometric mean | (ref)                                                  | 1.10x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                    |
| xml_etree_iterparse  | 96.7 ms                                                | 90.6 ms: 1.07x faster                                                   |
| json_loads           | 26.5 us                                                | 27.7 us: 1.04x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 97.4 ms: 1.14x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 2.57 sec: 1.22x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 74.4 ms: 1.26x slower                                                   |
| json_dumps           | 10.4 ms                                                | 13.9 ms: 1.34x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 331 us: 1.50x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 510 us: 1.66x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.20x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.76 ms: 1.36x slower                                                   |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.58x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 64.9 ms: 1.29x slower                                                   |
| genshi_text     | 22.8 ms                                                | 31.3 ms: 1.37x slower                                                   |
| django_template | 34.7 ms                                                | 50.1 ms: 1.44x slower                                                   |
| mako            | 11.0 ms                                                | 17.2 ms: 1.56x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.41x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 740 ms: 1.50x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 314 ms: 1.42x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 764 ms: 1.42x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 400 ms: 1.40x faster                                                    |
| async_tree_none            | 464 ms                                                 | 351 ms: 1.32x faster                                                    |
| async_tree_memoization     | 555 ms                                                 | 429 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 567 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 599 ms: 1.19x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                                   |
| deepcopy                   | 352 us                                                 | 324 us: 1.08x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 90.6 ms: 1.07x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 3.30 ms: 1.05x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 2.15 us: 1.02x faster                                                   |
| pidigits                   | 184 ms                                                 | 182 ms: 1.01x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 520 ms: 1.01x slower                                                    |
| deepcopy_memo              | 40.3 us                                                | 40.5 us: 1.01x slower                                                   |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                    |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                   |
| json_loads                 | 26.5 us                                                | 27.7 us: 1.04x slower                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 5.06 sec: 1.07x slower                                                  |
| pylint                     | 319 ms                                                 | 349 ms: 1.10x slower                                                    |
| regex_dna                  | 168 ms                                                 | 187 ms: 1.11x slower                                                    |
| deepcopy_reduce            | 3.08 us                                                | 3.44 us: 1.12x slower                                                   |
| scimark_fft                | 342 ms                                                 | 385 ms: 1.13x slower                                                    |
| dulwich_log                | 78.9 ms                                                | 89.9 ms: 1.14x slower                                                   |
| xml_etree_generate         | 85.2 ms                                                | 97.4 ms: 1.14x slower                                                   |
| docutils                   | 2.64 sec                                               | 3.02 sec: 1.14x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.81 sec: 1.16x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 195 ms: 1.17x slower                                                    |
| async_generators           | 384 ms                                                 | 453 ms: 1.18x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 90.8 ms: 1.18x slower                                                   |
| pycparser                  | 1.17 sec                                               | 1.39 sec: 1.19x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 24.6 ms: 1.19x slower                                                   |
| regex_compile              | 142 ms                                                 | 171 ms: 1.20x slower                                                    |
| generators                 | 32.2 ms                                                | 38.7 ms: 1.20x slower                                                   |
| tomli_loads                | 2.11 sec                                               | 2.57 sec: 1.22x slower                                                  |
| sympy_str                  | 292 ms                                                 | 357 ms: 1.22x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 25.3 ms: 1.23x slower                                                   |
| nqueens                    | 80.1 ms                                                | 100 ms: 1.25x slower                                                    |
| sqlglot_normalize          | 107 ms                                                 | 134 ms: 1.26x slower                                                    |
| sqlglot_optimize           | 53.3 ms                                                | 67.0 ms: 1.26x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 74.4 ms: 1.26x slower                                                   |
| sympy_expand               | 468 ms                                                 | 594 ms: 1.27x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 208 us: 1.27x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 946 ms: 1.27x slower                                                    |
| thrift                     | 791 us                                                 | 1.01 ms: 1.28x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 182 ms: 1.28x slower                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 27.9 ms: 1.28x slower                                                   |
| meteor_contest             | 104 ms                                                 | 133 ms: 1.29x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 64.9 ms: 1.29x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.71 ms: 1.30x slower                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.98 sec: 1.30x slower                                                  |
| 2to3                       | 264 ms                                                 | 352 ms: 1.33x slower                                                    |
| fannkuch                   | 372 ms                                                 | 497 ms: 1.34x slower                                                    |
| float                      | 80.8 ms                                                | 108 ms: 1.34x slower                                                    |
| telco                      | 6.53 ms                                                | 8.74 ms: 1.34x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 13.9 ms: 1.34x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.76 ms: 1.36x slower                                                   |
| genshi_text                | 22.8 ms                                                | 31.3 ms: 1.37x slower                                                   |
| logging_simple             | 6.63 us                                                | 9.18 us: 1.38x slower                                                   |
| comprehensions             | 19.8 us                                                | 27.6 us: 1.39x slower                                                   |
| coverage                   | 71.4 ms                                                | 99.7 ms: 1.40x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 159 ms: 1.40x slower                                                    |
| logging_format             | 7.35 us                                                | 10.4 us: 1.41x slower                                                   |
| django_template            | 34.7 ms                                                | 50.1 ms: 1.44x slower                                                   |
| pyflate                    | 448 ms                                                 | 649 ms: 1.45x slower                                                    |
| nbody                      | 89.3 ms                                                | 130 ms: 1.45x slower                                                    |
| html5lib                   | 63.6 ms                                                | 93.2 ms: 1.47x slower                                                   |
| richards_super             | 51.9 ms                                                | 76.8 ms: 1.48x slower                                                   |
| richards                   | 45.9 ms                                                | 68.6 ms: 1.49x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 331 us: 1.50x slower                                                    |
| chaos                      | 62.8 ms                                                | 95.4 ms: 1.52x slower                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 106 ms: 1.56x slower                                                    |
| mako                       | 11.0 ms                                                | 17.2 ms: 1.56x slower                                                   |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.58x slower                                                   |
| hexiom                     | 6.17 ms                                                | 9.79 ms: 1.59x slower                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 2.70 ms: 1.62x slower                                                   |
| raytrace                   | 299 ms                                                 | 491 ms: 1.64x slower                                                    |
| scimark_sor                | 130 ms                                                 | 215 ms: 1.65x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 510 us: 1.66x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.81 ms: 1.66x slower                                                   |
| logging_silent             | 109 ns                                                 | 182 ns: 1.67x slower                                                    |
| sqlglot_parse              | 1.36 ms                                                | 2.33 ms: 1.72x slower                                                   |
| go                         | 139 ms                                                 | 241 ms: 1.73x slower                                                    |
| deltablue                  | 3.45 ms                                                | 7.43 ms: 2.16x slower                                                   |
| bench_thread_pool          | 941 us                                                 | 3.38 ms: 3.59x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 100 ms: 9.30x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.26x slower                                                            |

Benchmark hidden because not significant (1): json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250101-3.14.0a3+-41a86a6-NOGIL/bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3+-41a86a6.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.173x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.33x