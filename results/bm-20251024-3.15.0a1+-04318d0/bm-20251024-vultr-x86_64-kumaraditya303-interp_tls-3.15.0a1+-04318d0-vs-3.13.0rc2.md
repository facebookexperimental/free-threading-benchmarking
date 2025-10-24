# Results vs. 3.13.0rc2

- fork: kumaraditya303
- ref: interp_tls
- machine: linux-x86_64
- commit hash: 04318d0
- commit date: 2025-10-24
- overall geometric mean: 1.047x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 247 ms: 1.05x faster                                                 |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                               |
| html5lib       | 67.0 ms                                                      | 62.5 ms: 1.07x faster                                                |
| Geometric mean | (ref)                                                        | 1.05x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 558 ms: 1.57x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 594 ms: 1.54x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 309 ms: 1.49x faster                                                 |
| async_tree_none            | 354 ms                                                       | 246 ms: 1.44x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 482 ms: 1.38x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                 |
| async_generators           | 377 ms                                                       | 346 ms: 1.09x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 69.4 ms: 1.12x faster                                                |
| pidigits       | 217 ms                                                       | 201 ms: 1.08x faster                                                 |
| nbody          | 85.1 ms                                                      | 87.7 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                        | 1.05x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.69 ms: 1.15x faster                                                |
| regex_v8       | 22.7 ms                                                      | 21.2 ms: 1.07x faster                                                |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                 |
| regex_dna      | 180 ms                                                       | 169 ms: 1.07x faster                                                 |
| Geometric mean | (ref)                                                        | 1.09x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.2 ms: 1.13x faster                                                |
| json_dumps           | 10.5 ms                                                      | 9.49 ms: 1.11x faster                                                |
| tomli_loads          | 2.01 sec                                                     | 1.91 sec: 1.05x faster                                               |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 82.5 ms: 1.04x faster                                                |
| xml_etree_process    | 59.3 ms                                                      | 58.4 ms: 1.02x faster                                                |
| unpickle_pure_python | 210 us                                                       | 208 us: 1.01x faster                                                 |
| json_loads           | 27.0 us                                                      | 27.8 us: 1.03x slower                                                |
| pickle_pure_python   | 294 us                                                       | 304 us: 1.03x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.04x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.20 ms: 1.03x faster                                                |
| python_startup         | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text    | 21.5 ms                                                      | 20.4 ms: 1.05x faster                                                |
| genshi_xml     | 48.8 ms                                                      | 48.3 ms: 1.01x faster                                                |
| mako           | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                        | 1.01x faster                                                         |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.06x faster                                               |
| async_tree_io              | 876 ms                                                       | 558 ms: 1.57x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 594 ms: 1.54x faster                                                 |
| deepcopy_memo              | 39.1 us                                                      | 25.9 us: 1.51x faster                                                |
| async_tree_memoization     | 461 ms                                                       | 309 ms: 1.49x faster                                                 |
| deepcopy                   | 355 us                                                       | 241 us: 1.47x faster                                                 |
| async_tree_none            | 354 ms                                                       | 246 ms: 1.44x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 482 ms: 1.38x faster                                                 |
| go                         | 141 ms                                                       | 103 ms: 1.37x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 247 ms: 1.36x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 310 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                 |
| scimark_sor                | 134 ms                                                       | 105 ms: 1.28x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.58 us: 1.21x faster                                                |
| spectral_norm              | 111 ms                                                       | 92.6 ms: 1.20x faster                                                |
| regex_effbot               | 3.08 ms                                                      | 2.69 ms: 1.15x faster                                                |
| scimark_fft                | 349 ms                                                       | 308 ms: 1.13x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.2 ms: 1.13x faster                                                |
| float                      | 77.5 ms                                                      | 69.4 ms: 1.12x faster                                                |
| richards_super             | 51.6 ms                                                      | 46.4 ms: 1.11x faster                                                |
| richards                   | 45.2 ms                                                      | 40.7 ms: 1.11x faster                                                |
| json_dumps                 | 10.5 ms                                                      | 9.49 ms: 1.11x faster                                                |
| pyflate                    | 449 ms                                                       | 407 ms: 1.10x faster                                                 |
| pylint                     | 317 ms                                                       | 289 ms: 1.10x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 68.2 ms: 1.10x faster                                                |
| async_generators           | 377 ms                                                       | 346 ms: 1.09x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.54 ms: 1.08x faster                                                |
| pprint_safe_repr           | 738 ms                                                       | 683 ms: 1.08x faster                                                 |
| pidigits                   | 217 ms                                                       | 201 ms: 1.08x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.39 sec: 1.07x faster                                               |
| html5lib                   | 67.0 ms                                                      | 62.5 ms: 1.07x faster                                                |
| logging_simple             | 6.16 us                                                      | 5.75 us: 1.07x faster                                                |
| logging_silent             | 103 ns                                                       | 95.9 ns: 1.07x faster                                                |
| regex_v8                   | 22.7 ms                                                      | 21.2 ms: 1.07x faster                                                |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                 |
| regex_dna                  | 180 ms                                                       | 169 ms: 1.07x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.17 sec: 1.07x faster                                               |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.3 ms: 1.07x faster                                                |
| logging_format             | 6.84 us                                                      | 6.46 us: 1.06x faster                                                |
| comprehensions             | 16.5 us                                                      | 15.6 us: 1.05x faster                                                |
| genshi_text                | 21.5 ms                                                      | 20.4 ms: 1.05x faster                                                |
| tomli_loads                | 2.01 sec                                                     | 1.91 sec: 1.05x faster                                               |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                 |
| 2to3                       | 260 ms                                                       | 247 ms: 1.05x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.07 sec: 1.05x faster                                               |
| sympy_integrate            | 19.8 ms                                                      | 19.0 ms: 1.05x faster                                                |
| generators                 | 28.8 ms                                                      | 27.6 ms: 1.04x faster                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.51 ms: 1.04x faster                                                |
| chaos                      | 57.3 ms                                                      | 55.3 ms: 1.04x faster                                                |
| xml_etree_generate         | 85.4 ms                                                      | 82.5 ms: 1.04x faster                                                |
| thrift                     | 778 us                                                       | 754 us: 1.03x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.20 ms: 1.03x faster                                                |
| meteor_contest             | 102 ms                                                       | 99.2 ms: 1.02x faster                                                |
| raytrace                   | 253 ms                                                       | 247 ms: 1.02x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                               |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 58.4 ms: 1.02x faster                                                |
| typing_runtime_protocols   | 155 us                                                       | 153 us: 1.01x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 208 us: 1.01x faster                                                 |
| genshi_xml                 | 48.8 ms                                                      | 48.3 ms: 1.01x faster                                                |
| coverage                   | 83.0 ms                                                      | 82.5 ms: 1.01x faster                                                |
| crypto_pyaes               | 67.9 ms                                                      | 68.5 ms: 1.01x slower                                                |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                |
| deltablue                  | 3.12 ms                                                      | 3.20 ms: 1.02x slower                                                |
| sqlite_synth               | 2.21 us                                                      | 2.27 us: 1.03x slower                                                |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                |
| nbody                      | 85.1 ms                                                      | 87.7 ms: 1.03x slower                                                |
| json_loads                 | 27.0 us                                                      | 27.8 us: 1.03x slower                                                |
| pickle_pure_python         | 294 us                                                       | 304 us: 1.03x slower                                                 |
| sympy_expand               | 457 ms                                                       | 477 ms: 1.04x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                 |
| fannkuch                   | 370 ms                                                       | 388 ms: 1.05x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 995 us: 1.08x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                |
| bench_mp_pool              | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                |
| create_gc_cycles           | 1.34 ms                                                      | 1.94 ms: 1.45x slower                                                |
| gc_traversal               | 3.14 ms                                                      | 4.79 ms: 1.52x slower                                                |
| telco                      | 7.82 ms                                                      | 155 ms: 19.85x slower                                                |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                         |

Benchmark hidden because not significant (5): sympy_str, sympy_sum, nqueens, django_template, json
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251024-3.15.0a1+-04318d0/bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1+-04318d0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.047x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x