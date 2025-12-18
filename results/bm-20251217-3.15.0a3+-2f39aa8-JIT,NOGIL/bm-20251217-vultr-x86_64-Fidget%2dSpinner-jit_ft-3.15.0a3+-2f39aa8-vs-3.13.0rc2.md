# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: jit_ft
- machine: linux-x86_64
- commit hash: 2f39aa8
- commit date: 2025-12-17
- overall geometric mean: 1.040x slower
- HPT reliability: 75.81%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 278 ms: 1.07x slower                                               |
| docutils       | 2.62 sec                                                     | 2.94 sec: 1.12x slower                                             |
| html5lib       | 67.0 ms                                                      | 70.3 ms: 1.05x slower                                              |
| Geometric mean | (ref)                                                        | 1.08x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 607 ms: 1.51x faster                                               |
| async_tree_io              | 876 ms                                                       | 633 ms: 1.38x faster                                               |
| async_tree_memoization     | 461 ms                                                       | 352 ms: 1.31x faster                                               |
| async_tree_none_tg         | 336 ms                                                       | 264 ms: 1.27x faster                                               |
| async_tree_memoization_tg  | 414 ms                                                       | 329 ms: 1.26x faster                                               |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 556 ms: 1.20x faster                                               |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 533 ms: 1.20x faster                                               |
| asyncio_websockets         | 520 ms                                                       | 511 ms: 1.02x faster                                               |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                              |
| async_generators           | 377 ms                                                       | 391 ms: 1.04x slower                                               |
| Geometric mean             | (ref)                                                        | 1.20x faster                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 64.2 ms: 1.21x faster                                              |
| pidigits       | 217 ms                                                       | 192 ms: 1.13x faster                                               |
| nbody          | 85.1 ms                                                      | 105 ms: 1.23x slower                                               |
| Geometric mean | (ref)                                                        | 1.03x faster                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.92 ms: 1.06x faster                                              |
| regex_v8       | 22.7 ms                                                      | 21.9 ms: 1.04x faster                                              |
| regex_compile  | 132 ms                                                       | 146 ms: 1.11x slower                                               |
| Geometric mean | (ref)                                                        | 1.00x slower                                                       |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.7 ms: 1.08x faster                                              |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.05x faster                                               |
| unpickle_pure_python | 210 us                                                       | 204 us: 1.03x faster                                               |
| json_dumps           | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                              |
| pickle_pure_python   | 294 us                                                       | 312 us: 1.06x slower                                               |
| xml_etree_generate   | 85.4 ms                                                      | 91.0 ms: 1.07x slower                                              |
| xml_etree_process    | 59.3 ms                                                      | 63.6 ms: 1.07x slower                                              |
| tomli_loads          | 2.01 sec                                                     | 2.15 sec: 1.07x slower                                             |
| json_loads           | 27.0 us                                                      | 32.2 us: 1.19x slower                                              |
| Geometric mean       | (ref)                                                        | 1.03x slower                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.56 ms: 1.29x slower                                              |
| python_startup         | 11.0 ms                                                      | 15.9 ms: 1.45x slower                                              |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 41.1 ms: 1.21x slower                                              |
| genshi_text     | 21.5 ms                                                      | 28.0 ms: 1.30x slower                                              |
| mako            | 11.3 ms                                                      | 14.9 ms: 1.31x slower                                              |
| genshi_xml      | 48.8 ms                                                      | 67.7 ms: 1.39x slower                                              |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 22.7 ms: 1.99x faster                                              |
| richards_super             | 51.6 ms                                                      | 27.8 ms: 1.86x faster                                              |
| gc_traversal               | 3.14 ms                                                      | 1.89 ms: 1.66x faster                                              |
| bench_mp_pool              | 11.0 ms                                                      | 7.13 ms: 1.54x faster                                              |
| async_tree_io_tg           | 913 ms                                                       | 607 ms: 1.51x faster                                               |
| mdp                        | 2.36 sec                                                     | 1.58 sec: 1.49x faster                                             |
| async_tree_io              | 876 ms                                                       | 633 ms: 1.38x faster                                               |
| deepcopy_memo              | 39.1 us                                                      | 29.3 us: 1.33x faster                                              |
| async_tree_memoization     | 461 ms                                                       | 352 ms: 1.31x faster                                               |
| async_tree_none_tg         | 336 ms                                                       | 264 ms: 1.27x faster                                               |
| deepcopy                   | 355 us                                                       | 281 us: 1.26x faster                                               |
| async_tree_memoization_tg  | 414 ms                                                       | 329 ms: 1.26x faster                                               |
| go                         | 141 ms                                                       | 112 ms: 1.25x faster                                               |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                               |
| logging_silent             | 103 ns                                                       | 83.3 ns: 1.23x faster                                              |
| float                      | 77.5 ms                                                      | 64.2 ms: 1.21x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 556 ms: 1.20x faster                                               |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 533 ms: 1.20x faster                                               |
| scimark_fft                | 349 ms                                                       | 292 ms: 1.20x faster                                               |
| scimark_sor                | 134 ms                                                       | 114 ms: 1.18x faster                                               |
| pidigits                   | 217 ms                                                       | 192 ms: 1.13x faster                                               |
| spectral_norm              | 111 ms                                                       | 99.9 ms: 1.11x faster                                              |
| sqlite_synth               | 2.21 us                                                      | 2.02 us: 1.09x faster                                              |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.7 ms: 1.08x faster                                              |
| bpe_tokeniser              | 4.45 sec                                                     | 4.15 sec: 1.07x faster                                             |
| deepcopy_reduce            | 3.11 us                                                      | 2.92 us: 1.07x faster                                              |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.06x faster                                              |
| regex_effbot               | 3.08 ms                                                      | 2.92 ms: 1.06x faster                                              |
| pyflate                    | 449 ms                                                       | 425 ms: 1.05x faster                                               |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.05x faster                                               |
| regex_v8                   | 22.7 ms                                                      | 21.9 ms: 1.04x faster                                              |
| unpickle_pure_python       | 210 us                                                       | 204 us: 1.03x faster                                               |
| pprint_safe_repr           | 738 ms                                                       | 721 ms: 1.02x faster                                               |
| asyncio_websockets         | 520 ms                                                       | 511 ms: 1.02x faster                                               |
| deltablue                  | 3.12 ms                                                      | 3.17 ms: 1.01x slower                                              |
| json_dumps                 | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                              |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                              |
| pprint_pformat             | 1.50 sec                                                     | 1.55 sec: 1.04x slower                                             |
| async_generators           | 377 ms                                                       | 391 ms: 1.04x slower                                               |
| pycparser                  | 1.12 sec                                                     | 1.16 sec: 1.04x slower                                             |
| html5lib                   | 67.0 ms                                                      | 70.3 ms: 1.05x slower                                              |
| scimark_monte_carlo        | 65.4 ms                                                      | 68.7 ms: 1.05x slower                                              |
| pickle_pure_python         | 294 us                                                       | 312 us: 1.06x slower                                               |
| xml_etree_generate         | 85.4 ms                                                      | 91.0 ms: 1.07x slower                                              |
| chaos                      | 57.3 ms                                                      | 61.2 ms: 1.07x slower                                              |
| 2to3                       | 260 ms                                                       | 278 ms: 1.07x slower                                               |
| xml_etree_process          | 59.3 ms                                                      | 63.6 ms: 1.07x slower                                              |
| tomli_loads                | 2.01 sec                                                     | 2.15 sec: 1.07x slower                                             |
| generators                 | 28.8 ms                                                      | 31.0 ms: 1.08x slower                                              |
| create_gc_cycles           | 1.34 ms                                                      | 1.46 ms: 1.09x slower                                              |
| json                       | 4.93 ms                                                      | 5.38 ms: 1.09x slower                                              |
| regex_compile              | 132 ms                                                       | 146 ms: 1.11x slower                                               |
| scimark_lu                 | 113 ms                                                       | 126 ms: 1.12x slower                                               |
| docutils                   | 2.62 sec                                                     | 2.94 sec: 1.12x slower                                             |
| logging_simple             | 6.16 us                                                      | 6.94 us: 1.13x slower                                              |
| thrift                     | 778 us                                                       | 877 us: 1.13x slower                                               |
| logging_format             | 6.84 us                                                      | 7.79 us: 1.14x slower                                              |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.44 ms: 1.15x slower                                              |
| fannkuch                   | 370 ms                                                       | 429 ms: 1.16x slower                                               |
| sympy_integrate            | 19.8 ms                                                      | 23.2 ms: 1.17x slower                                              |
| comprehensions             | 16.5 us                                                      | 19.4 us: 1.18x slower                                              |
| meteor_contest             | 102 ms                                                       | 121 ms: 1.19x slower                                               |
| json_loads                 | 27.0 us                                                      | 32.2 us: 1.19x slower                                              |
| hexiom                     | 5.99 ms                                                      | 7.19 ms: 1.20x slower                                              |
| django_template            | 34.1 ms                                                      | 41.1 ms: 1.21x slower                                              |
| nbody                      | 85.1 ms                                                      | 105 ms: 1.23x slower                                               |
| raytrace                   | 253 ms                                                       | 311 ms: 1.23x slower                                               |
| sympy_sum                  | 156 ms                                                       | 194 ms: 1.24x slower                                               |
| crypto_pyaes               | 67.9 ms                                                      | 85.0 ms: 1.25x slower                                              |
| nqueens                    | 78.6 ms                                                      | 100 ms: 1.28x slower                                               |
| sympy_expand               | 457 ms                                                       | 585 ms: 1.28x slower                                               |
| sympy_str                  | 275 ms                                                       | 353 ms: 1.28x slower                                               |
| typing_runtime_protocols   | 155 us                                                       | 200 us: 1.29x slower                                               |
| python_startup_no_site     | 7.39 ms                                                      | 9.56 ms: 1.29x slower                                              |
| genshi_text                | 21.5 ms                                                      | 28.0 ms: 1.30x slower                                              |
| mako                       | 11.3 ms                                                      | 14.9 ms: 1.31x slower                                              |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.34x slower                                               |
| genshi_xml                 | 48.8 ms                                                      | 67.7 ms: 1.39x slower                                              |
| python_startup             | 11.0 ms                                                      | 15.9 ms: 1.45x slower                                              |
| bench_thread_pool          | 919 us                                                       | 1.48 ms: 1.61x slower                                              |
| telco                      | 7.82 ms                                                      | 176 ms: 22.47x slower                                              |
| Geometric mean             | (ref)                                                        | 1.04x slower                                                       |

Benchmark hidden because not significant (3): dulwich_log, regex_dna, pylint
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251217-3.15.0a3+-2f39aa8-JIT,NOGIL/bm-20251217-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-2f39aa8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.040x slower

# HPT report

- Reliability score: 75.81% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.43x