# Results vs. 3.13.0rc2

- fork: python
- ref: e2118b0ac21191bfeecd
- machine: linux-x86_64
- commit hash: e2118b0
- commit date: 2026-08-25
- overall geometric mean: 1.068x slower
- HPT reliability: 97.59%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 295 ms: 1.14x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.91 sec: 1.11x slower                                                |
| Geometric mean | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 694 ms: 1.32x faster                                                  |
| async_tree_io              | 876 ms                                                       | 704 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 597 ms: 1.12x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 418 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 584 ms: 1.09x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 399 ms: 1.04x faster                                                  |
| async_tree_none            | 354 ms                                                       | 341 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                 |
| async_generators           | 377 ms                                                       | 414 ms: 1.10x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                          |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| float          | 77.5 ms                                                      | 83.9 ms: 1.08x slower                                                 |
| nbody          | 85.1 ms                                                      | 119 ms: 1.40x slower                                                  |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 2.98 ms: 1.03x faster                                                 |
| regex_dna      | 180 ms                                                       | 181 ms: 1.01x slower                                                  |
| regex_compile  | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                |
| json_dumps           | 10.5 ms                                                      | 10.1 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 95.3 ms: 1.00x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 333 us: 1.13x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 238 us: 1.13x slower                                                  |
| json_loads           | 27.0 us                                                      | 30.7 us: 1.14x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.19x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 75.6 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.87 ms: 1.34x slower                                                 |
| python_startup         | 11.0 ms                                                      | 16.1 ms: 1.46x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.40x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 41.1 ms: 1.20x slower                                                 |
| mako            | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 130 ms: 2.43x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.30 sec: 1.81x faster                                                |
| gc_traversal               | 3.14 ms                                                      | 1.76 ms: 1.79x faster                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 6.71 ms: 1.64x faster                                                 |
| deepcopy                   | 355 us                                                       | 265 us: 1.34x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 694 ms: 1.32x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 31.1 us: 1.25x faster                                                 |
| async_tree_io              | 876 ms                                                       | 704 ms: 1.24x faster                                                  |
| go                         | 141 ms                                                       | 119 ms: 1.18x faster                                                  |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| scimark_sor                | 134 ms                                                       | 118 ms: 1.14x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 1.95 us: 1.13x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 597 ms: 1.12x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 418 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 584 ms: 1.09x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.0 ms: 1.08x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 69.7 ms: 1.07x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.9 ms: 1.07x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 144 us: 1.07x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                |
| json_dumps                 | 10.5 ms                                                      | 10.1 ms: 1.04x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 399 ms: 1.04x faster                                                  |
| async_tree_none            | 354 ms                                                       | 341 ms: 1.04x faster                                                  |
| spectral_norm              | 111 ms                                                       | 107 ms: 1.04x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.98 ms: 1.03x faster                                                 |
| scimark_fft                | 349 ms                                                       | 339 ms: 1.03x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.03 us: 1.03x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.38 sec: 1.01x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 95.3 ms: 1.00x slower                                                 |
| regex_dna                  | 180 ms                                                       | 181 ms: 1.01x slower                                                  |
| logging_silent             | 103 ns                                                       | 103 ns: 1.01x slower                                                  |
| pyflate                    | 449 ms                                                       | 454 ms: 1.01x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.36 ms: 1.01x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.05x slower                                                |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                 |
| chaos                      | 57.3 ms                                                      | 60.5 ms: 1.06x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.8 us: 1.08x slower                                                 |
| float                      | 77.5 ms                                                      | 83.9 ms: 1.08x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.51 ms: 1.09x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 807 ms: 1.09x slower                                                  |
| json                       | 4.93 ms                                                      | 5.39 ms: 1.09x slower                                                 |
| async_generators           | 377 ms                                                       | 414 ms: 1.10x slower                                                  |
| generators                 | 28.8 ms                                                      | 31.8 ms: 1.10x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 22.0 ms: 1.11x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.22 ms: 1.11x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 87.2 ms: 1.11x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.91 sec: 1.11x slower                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.68 sec: 1.12x slower                                                |
| scimark_lu                 | 113 ms                                                       | 127 ms: 1.13x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 333 us: 1.13x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 238 us: 1.13x slower                                                  |
| 2to3                       | 260 ms                                                       | 295 ms: 1.14x slower                                                  |
| json_loads                 | 27.0 us                                                      | 30.7 us: 1.14x slower                                                 |
| logging_simple             | 6.16 us                                                      | 7.10 us: 1.15x slower                                                 |
| raytrace                   | 253 ms                                                       | 291 ms: 1.15x slower                                                  |
| richards                   | 45.2 ms                                                      | 52.2 ms: 1.15x slower                                                 |
| sympy_str                  | 275 ms                                                       | 320 ms: 1.16x slower                                                  |
| richards_super             | 51.6 ms                                                      | 60.1 ms: 1.16x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 76.6 ms: 1.17x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.67 ms: 1.17x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 183 ms: 1.18x slower                                                  |
| sympy_expand               | 457 ms                                                       | 538 ms: 1.18x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.08 us: 1.18x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 102 ms: 1.19x slower                                                  |
| thrift                     | 778 us                                                       | 928 us: 1.19x slower                                                  |
| django_template            | 34.1 ms                                                      | 41.1 ms: 1.20x slower                                                 |
| fannkuch                   | 370 ms                                                       | 464 ms: 1.25x slower                                                  |
| meteor_contest             | 102 ms                                                       | 128 ms: 1.26x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 75.6 ms: 1.27x slower                                                 |
| regex_compile              | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 88.9 ms: 1.31x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.87 ms: 1.34x slower                                                 |
| coverage                   | 83.0 ms                                                      | 115 ms: 1.39x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                 |
| nbody                      | 85.1 ms                                                      | 119 ms: 1.40x slower                                                  |
| python_startup             | 11.0 ms                                                      | 16.1 ms: 1.46x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.47 ms: 1.60x slower                                                 |
| telco                      | 7.82 ms                                                      | 175 ms: 22.36x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                          |

Benchmark hidden because not significant (2): async_tree_none_tg, html5lib
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260825-3.16.0a0-e2118b0-NOGIL/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.068x slower

# HPT report

- Reliability score: 97.59% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x