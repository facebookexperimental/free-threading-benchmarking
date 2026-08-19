# Results vs. 3.13.0rc2

- fork: python
- ref: af49df919dafc3767ae9
- machine: linux-x86_64
- commit hash: af49df9
- commit date: 2026-08-18
- overall geometric mean: 1.037x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.62 sec                                                     | 2.37 sec: 1.10x faster                                                |
| html5lib       | 67.0 ms                                                      | 59.5 ms: 1.13x faster                                                 |
| Geometric mean | (ref)                                                        | 1.08x faster                                                          |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 539 ms: 1.24x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 375 ms: 1.23x faster                                                  |
| async_tree_io              | 876 ms                                                       | 720 ms: 1.22x faster                                                  |
| async_tree_none            | 354 ms                                                       | 292 ms: 1.21x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 758 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 555 ms: 1.15x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 363 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 297 ms: 1.13x faster                                                  |
| async_generators           | 377 ms                                                       | 343 ms: 1.10x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.14x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 187 ms: 1.16x faster                                                  |
| float          | 77.5 ms                                                      | 72.1 ms: 1.07x faster                                                 |
| nbody          | 85.1 ms                                                      | 89.1 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.54 ms: 1.21x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 21.8 ms: 1.04x faster                                                 |
| regex_dna      | 180 ms                                                       | 181 ms: 1.00x slower                                                  |
| regex_compile  | 132 ms                                                       | 149 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|---------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps          | 10.5 ms                                                      | 9.33 ms: 1.13x faster                                                 |
| tomli_loads         | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                |
| xml_etree_iterparse | 94.9 ms                                                      | 91.1 ms: 1.04x faster                                                 |
| json_loads          | 27.0 us                                                      | 27.4 us: 1.01x slower                                                 |
| pickle_pure_python  | 294 us                                                       | 300 us: 1.02x slower                                                  |
| xml_etree_generate  | 85.4 ms                                                      | 88.3 ms: 1.03x slower                                                 |
| xml_etree_parse     | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| xml_etree_process   | 59.3 ms                                                      | 62.6 ms: 1.05x slower                                                 |
| Geometric mean      | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.09 ms: 1.04x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                 |
| django_template | 34.1 ms                                                      | 36.6 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 114 ms: 2.78x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.13 sec: 2.09x faster                                                |
| deepcopy                   | 355 us                                                       | 232 us: 1.53x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 26.5 us: 1.47x faster                                                 |
| go                         | 141 ms                                                       | 103 ms: 1.37x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 118 us: 1.31x faster                                                  |
| scimark_sor                | 134 ms                                                       | 104 ms: 1.29x faster                                                  |
| spectral_norm              | 111 ms                                                       | 89.1 ms: 1.25x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 539 ms: 1.24x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 375 ms: 1.23x faster                                                  |
| async_tree_io              | 876 ms                                                       | 720 ms: 1.22x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.54 ms: 1.21x faster                                                 |
| async_tree_none            | 354 ms                                                       | 292 ms: 1.21x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.58 us: 1.21x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 758 ms: 1.21x faster                                                  |
| scimark_fft                | 349 ms                                                       | 301 ms: 1.16x faster                                                  |
| pidigits                   | 217 ms                                                       | 187 ms: 1.16x faster                                                  |
| pyflate                    | 449 ms                                                       | 389 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 555 ms: 1.15x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 363 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 297 ms: 1.13x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.33 ms: 1.13x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 59.5 ms: 1.13x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 67.4 ms: 1.11x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.37 sec: 1.10x faster                                                |
| async_generators           | 377 ms                                                       | 343 ms: 1.10x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                |
| logging_silent             | 103 ns                                                       | 94.7 ns: 1.08x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.08x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.36 ms: 1.08x faster                                                 |
| chaos                      | 57.3 ms                                                      | 53.3 ms: 1.08x faster                                                 |
| float                      | 77.5 ms                                                      | 72.1 ms: 1.07x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.62 ms: 1.07x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 74.5 ms: 1.06x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.6 us: 1.05x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.22 sec: 1.05x faster                                                |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.2 ms: 1.05x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.09 ms: 1.04x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.1 ms: 1.04x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.8 ms: 1.04x faster                                                 |
| generators                 | 28.8 ms                                                      | 28.0 ms: 1.03x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.3 ms: 1.03x faster                                                 |
| raytrace                   | 253 ms                                                       | 247 ms: 1.02x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 66.9 ms: 1.01x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.19 us: 1.01x faster                                                 |
| json                       | 4.93 ms                                                      | 4.89 ms: 1.01x faster                                                 |
| richards_super             | 51.6 ms                                                      | 51.3 ms: 1.01x faster                                                 |
| richards                   | 45.2 ms                                                      | 45.0 ms: 1.01x faster                                                 |
| coverage                   | 83.0 ms                                                      | 82.6 ms: 1.00x faster                                                 |
| regex_dna                  | 180 ms                                                       | 181 ms: 1.00x slower                                                  |
| meteor_contest             | 102 ms                                                       | 102 ms: 1.00x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                 |
| json_loads                 | 27.0 us                                                      | 27.4 us: 1.01x slower                                                 |
| logging_format             | 6.84 us                                                      | 6.95 us: 1.02x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 300 us: 1.02x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 159 ms: 1.02x slower                                                  |
| sympy_str                  | 275 ms                                                       | 282 ms: 1.03x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 116 ms: 1.03x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 88.3 ms: 1.03x slower                                                 |
| sympy_expand               | 457 ms                                                       | 476 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| nbody                      | 85.1 ms                                                      | 89.1 ms: 1.05x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 62.6 ms: 1.05x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.31 ms: 1.06x slower                                                 |
| django_template            | 34.1 ms                                                      | 36.6 ms: 1.07x slower                                                 |
| regex_compile              | 132 ms                                                       | 149 ms: 1.13x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.84 ms: 1.22x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.66 ms: 1.24x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.35 ms: 1.46x slower                                                 |
| telco                      | 7.82 ms                                                      | 159 ms: 20.34x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 242 ms: 22.02x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (8): pprint_safe_repr, 2to3, unpickle_pure_python, fannkuch, pycparser, pprint_pformat, thrift, logging_simple
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260818-3.16.0a0-af49df9/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.037x faster

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x