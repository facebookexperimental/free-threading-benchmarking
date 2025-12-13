# Results vs. 3.13.0rc2

- fork: python
- ref: c90863ac3dcbc5b0b8f9
- machine: linux-x86_64
- commit hash: c90863a
- commit date: 2025-12-12
- overall geometric mean: 1.066x slower
- HPT reliability: 95.48%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 279 ms: 1.07x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.76 sec: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 621 ms: 1.47x faster                                                   |
| async_tree_io              | 876 ms                                                       | 628 ms: 1.40x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 355 ms: 1.30x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 264 ms: 1.27x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 328 ms: 1.26x faster                                                   |
| async_tree_none            | 354 ms                                                       | 287 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 521 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 547 ms: 1.22x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 511 ms: 1.02x faster                                                   |
| async_generators           | 377 ms                                                       | 375 ms: 1.00x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 190 ms: 1.14x faster                                                   |
| float          | 77.5 ms                                                      | 72.0 ms: 1.08x faster                                                  |
| nbody          | 85.1 ms                                                      | 122 ms: 1.43x slower                                                   |
| Geometric mean | (ref)                                                        | 1.05x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.87 ms: 1.07x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                  |
| regex_dna      | 180 ms                                                       | 178 ms: 1.01x faster                                                   |
| regex_compile  | 132 ms                                                       | 142 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.3 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 134 ms: 1.02x faster                                                   |
| json_dumps           | 10.5 ms                                                      | 11.2 ms: 1.06x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 237 us: 1.13x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.29 sec: 1.14x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 337 us: 1.14x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 98.8 ms: 1.16x slower                                                  |
| json_loads           | 27.0 us                                                      | 31.2 us: 1.16x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 70.6 ms: 1.19x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.10x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.70 ms: 1.31x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.8 ms: 1.44x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 40.8 ms: 1.19x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 58.9 ms: 1.21x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 26.5 ms: 1.23x slower                                                  |
| mako            | 11.3 ms                                                      | 15.4 ms: 1.36x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.25x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.32 sec: 1.78x faster                                                 |
| gc_traversal               | 3.14 ms                                                      | 1.93 ms: 1.63x faster                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 7.14 ms: 1.54x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 621 ms: 1.47x faster                                                   |
| async_tree_io              | 876 ms                                                       | 628 ms: 1.40x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 355 ms: 1.30x faster                                                   |
| deepcopy                   | 355 us                                                       | 278 us: 1.28x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.6 us: 1.28x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 264 ms: 1.27x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 328 ms: 1.26x faster                                                   |
| async_tree_none            | 354 ms                                                       | 287 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 521 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 547 ms: 1.22x faster                                                   |
| go                         | 141 ms                                                       | 121 ms: 1.16x faster                                                   |
| pidigits                   | 217 ms                                                       | 190 ms: 1.14x faster                                                   |
| scimark_sor                | 134 ms                                                       | 123 ms: 1.10x faster                                                   |
| float                      | 77.5 ms                                                      | 72.0 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.07x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.3 ms: 1.07x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.87 ms: 1.07x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.98 us: 1.04x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 72.1 ms: 1.04x faster                                                  |
| scimark_fft                | 349 ms                                                       | 341 ms: 1.02x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 134 ms: 1.02x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 511 ms: 1.02x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.38 sec: 1.01x faster                                                 |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                   |
| regex_dna                  | 180 ms                                                       | 178 ms: 1.01x faster                                                   |
| async_generators           | 377 ms                                                       | 375 ms: 1.00x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                  |
| pyflate                    | 449 ms                                                       | 455 ms: 1.01x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.76 sec: 1.05x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 11.2 ms: 1.06x slower                                                  |
| generators                 | 28.8 ms                                                      | 30.8 ms: 1.07x slower                                                  |
| 2to3                       | 260 ms                                                       | 279 ms: 1.07x slower                                                   |
| regex_compile              | 132 ms                                                       | 142 ms: 1.07x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 6.44 ms: 1.08x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 795 ms: 1.08x slower                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.08 ms: 1.08x slower                                                  |
| json                       | 4.93 ms                                                      | 5.37 ms: 1.09x slower                                                  |
| comprehensions             | 16.5 us                                                      | 18.0 us: 1.09x slower                                                  |
| chaos                      | 57.3 ms                                                      | 62.7 ms: 1.09x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.65 sec: 1.10x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 21.8 ms: 1.10x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 86.6 ms: 1.10x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.51 ms: 1.13x slower                                                  |
| logging_simple             | 6.16 us                                                      | 6.96 us: 1.13x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 237 us: 1.13x slower                                                   |
| sympy_str                  | 275 ms                                                       | 313 ms: 1.14x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.29 sec: 1.14x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 337 us: 1.14x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 178 ms: 1.14x slower                                                   |
| richards                   | 45.2 ms                                                      | 52.1 ms: 1.15x slower                                                  |
| thrift                     | 778 us                                                       | 897 us: 1.15x slower                                                   |
| logging_format             | 6.84 us                                                      | 7.91 us: 1.16x slower                                                  |
| richards_super             | 51.6 ms                                                      | 59.7 ms: 1.16x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 98.8 ms: 1.16x slower                                                  |
| sympy_expand               | 457 ms                                                       | 529 ms: 1.16x slower                                                   |
| json_loads                 | 27.0 us                                                      | 31.2 us: 1.16x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 131 ms: 1.16x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.65 ms: 1.17x slower                                                  |
| raytrace                   | 253 ms                                                       | 296 ms: 1.17x slower                                                   |
| meteor_contest             | 102 ms                                                       | 121 ms: 1.19x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 70.6 ms: 1.19x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.9 ms: 1.19x slower                                                  |
| django_template            | 34.1 ms                                                      | 40.8 ms: 1.19x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 58.9 ms: 1.21x slower                                                  |
| fannkuch                   | 370 ms                                                       | 454 ms: 1.23x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 26.5 ms: 1.23x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 85.5 ms: 1.26x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 196 us: 1.27x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 9.70 ms: 1.31x slower                                                  |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.34x slower                                                   |
| mako                       | 11.3 ms                                                      | 15.4 ms: 1.36x slower                                                  |
| nbody                      | 85.1 ms                                                      | 122 ms: 1.43x slower                                                   |
| python_startup             | 11.0 ms                                                      | 15.8 ms: 1.44x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.48 ms: 1.61x slower                                                  |
| telco                      | 7.82 ms                                                      | 178 ms: 22.78x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                           |

Benchmark hidden because not significant (3): pylint, logging_silent, html5lib
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251212-3.15.0a2+-c90863a-NOGIL/bm-20251212-vultr-x86_64-python-c90863ac3dcbc5b0b8f9-3.15.0a2+-c90863a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.066x slower

# HPT report

- Reliability score: 95.48% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x