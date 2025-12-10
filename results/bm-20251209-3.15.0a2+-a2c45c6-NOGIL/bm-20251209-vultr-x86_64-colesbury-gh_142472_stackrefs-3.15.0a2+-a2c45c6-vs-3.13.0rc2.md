# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_142472_stackrefs
- machine: linux-x86_64
- commit hash: a2c45c6
- commit date: 2025-12-09
- overall geometric mean: 1.060x slower
- HPT reliability: 97.06%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 277 ms: 1.07x slower                                                     |
| docutils       | 2.62 sec                                                     | 2.70 sec: 1.03x slower                                                   |
| html5lib       | 67.0 ms                                                      | 65.9 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                        | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 611 ms: 1.50x faster                                                     |
| async_tree_io              | 876 ms                                                       | 623 ms: 1.41x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 355 ms: 1.30x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 329 ms: 1.26x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 269 ms: 1.25x faster                                                     |
| async_tree_none            | 354 ms                                                       | 287 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 560 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 540 ms: 1.18x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                     |
| async_generators           | 377 ms                                                       | 380 ms: 1.01x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 72.3 ms: 1.07x faster                                                    |
| pidigits       | 217 ms                                                       | 215 ms: 1.01x faster                                                     |
| nbody          | 85.1 ms                                                      | 121 ms: 1.43x slower                                                     |
| Geometric mean | (ref)                                                        | 1.10x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.87 ms: 1.07x faster                                                    |
| regex_v8       | 22.7 ms                                                      | 22.1 ms: 1.03x faster                                                    |
| regex_compile  | 132 ms                                                       | 141 ms: 1.07x slower                                                     |
| Geometric mean | (ref)                                                        | 1.01x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.02x faster                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 93.5 ms: 1.02x faster                                                    |
| json_dumps           | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 233 us: 1.11x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 95.3 ms: 1.12x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 330 us: 1.12x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.29 sec: 1.14x slower                                                   |
| xml_etree_process    | 59.3 ms                                                      | 68.1 ms: 1.15x slower                                                    |
| json_loads           | 27.0 us                                                      | 31.9 us: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.70 ms: 1.31x slower                                                    |
| python_startup         | 11.0 ms                                                      | 15.8 ms: 1.44x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 56.9 ms: 1.17x slower                                                    |
| django_template | 34.1 ms                                                      | 40.4 ms: 1.18x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 26.3 ms: 1.22x slower                                                    |
| mako            | 11.3 ms                                                      | 15.5 ms: 1.36x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.23x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.30 sec: 1.81x faster                                                   |
| gc_traversal               | 3.14 ms                                                      | 1.90 ms: 1.65x faster                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 7.30 ms: 1.51x faster                                                    |
| async_tree_io_tg           | 913 ms                                                       | 611 ms: 1.50x faster                                                     |
| async_tree_io              | 876 ms                                                       | 623 ms: 1.41x faster                                                     |
| deepcopy                   | 355 us                                                       | 272 us: 1.31x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 355 ms: 1.30x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 30.3 us: 1.29x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 329 ms: 1.26x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 269 ms: 1.25x faster                                                     |
| async_tree_none            | 354 ms                                                       | 287 ms: 1.23x faster                                                     |
| go                         | 141 ms                                                       | 118 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 560 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 540 ms: 1.18x faster                                                     |
| scimark_sor                | 134 ms                                                       | 120 ms: 1.12x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.09x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.87 ms: 1.07x faster                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 2.90 us: 1.07x faster                                                    |
| float                      | 77.5 ms                                                      | 72.3 ms: 1.07x faster                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.09 us: 1.06x faster                                                    |
| dulwich_log                | 74.8 ms                                                      | 71.9 ms: 1.04x faster                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.30 sec: 1.03x faster                                                   |
| spectral_norm              | 111 ms                                                       | 108 ms: 1.03x faster                                                     |
| regex_v8                   | 22.7 ms                                                      | 22.1 ms: 1.03x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 133 ms: 1.02x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                     |
| html5lib                   | 67.0 ms                                                      | 65.9 ms: 1.02x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 93.5 ms: 1.02x faster                                                    |
| scimark_fft                | 349 ms                                                       | 344 ms: 1.01x faster                                                     |
| pidigits                   | 217 ms                                                       | 215 ms: 1.01x faster                                                     |
| pyflate                    | 449 ms                                                       | 451 ms: 1.00x slower                                                     |
| logging_silent             | 103 ns                                                       | 103 ns: 1.01x slower                                                     |
| async_generators           | 377 ms                                                       | 380 ms: 1.01x slower                                                     |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                    |
| json_dumps                 | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                    |
| docutils                   | 2.62 sec                                                     | 2.70 sec: 1.03x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 6.23 ms: 1.04x slower                                                    |
| pprint_safe_repr           | 738 ms                                                       | 767 ms: 1.04x slower                                                     |
| generators                 | 28.8 ms                                                      | 30.3 ms: 1.05x slower                                                    |
| comprehensions             | 16.5 us                                                      | 17.4 us: 1.06x slower                                                    |
| pprint_pformat             | 1.50 sec                                                     | 1.59 sec: 1.06x slower                                                   |
| 2to3                       | 260 ms                                                       | 277 ms: 1.07x slower                                                     |
| regex_compile              | 132 ms                                                       | 141 ms: 1.07x slower                                                     |
| chaos                      | 57.3 ms                                                      | 61.7 ms: 1.08x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 21.6 ms: 1.09x slower                                                    |
| logging_simple             | 6.16 us                                                      | 6.77 us: 1.10x slower                                                    |
| json                       | 4.93 ms                                                      | 5.45 ms: 1.11x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.48 ms: 1.11x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 233 us: 1.11x slower                                                     |
| thrift                     | 778 us                                                       | 865 us: 1.11x slower                                                     |
| nqueens                    | 78.6 ms                                                      | 87.5 ms: 1.11x slower                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.25 ms: 1.11x slower                                                    |
| sympy_str                  | 275 ms                                                       | 306 ms: 1.12x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 95.3 ms: 1.12x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 330 us: 1.12x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 176 ms: 1.13x slower                                                     |
| richards                   | 45.2 ms                                                      | 51.1 ms: 1.13x slower                                                    |
| richards_super             | 51.6 ms                                                      | 58.6 ms: 1.13x slower                                                    |
| logging_format             | 6.84 us                                                      | 7.76 us: 1.13x slower                                                    |
| sympy_expand               | 457 ms                                                       | 520 ms: 1.14x slower                                                     |
| tomli_loads                | 2.01 sec                                                     | 2.29 sec: 1.14x slower                                                   |
| scimark_lu                 | 113 ms                                                       | 128 ms: 1.14x slower                                                     |
| xml_etree_process          | 59.3 ms                                                      | 68.1 ms: 1.15x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 56.9 ms: 1.17x slower                                                    |
| meteor_contest             | 102 ms                                                       | 119 ms: 1.17x slower                                                     |
| raytrace                   | 253 ms                                                       | 296 ms: 1.17x slower                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 76.7 ms: 1.17x slower                                                    |
| json_loads                 | 27.0 us                                                      | 31.9 us: 1.18x slower                                                    |
| django_template            | 34.1 ms                                                      | 40.4 ms: 1.18x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 3.77 ms: 1.21x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 26.3 ms: 1.22x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 190 us: 1.23x slower                                                     |
| fannkuch                   | 370 ms                                                       | 456 ms: 1.23x slower                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 85.3 ms: 1.26x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 9.70 ms: 1.31x slower                                                    |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.34x slower                                                     |
| mako                       | 11.3 ms                                                      | 15.5 ms: 1.36x slower                                                    |
| nbody                      | 85.1 ms                                                      | 121 ms: 1.43x slower                                                     |
| python_startup             | 11.0 ms                                                      | 15.8 ms: 1.44x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 1.47 ms: 1.60x slower                                                    |
| telco                      | 7.82 ms                                                      | 175 ms: 22.34x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.06x slower                                                             |

Benchmark hidden because not significant (2): pylint, regex_dna
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251209-3.15.0a2+-a2c45c6-NOGIL/bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.060x slower

# HPT report

- Reliability score: 97.06% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x