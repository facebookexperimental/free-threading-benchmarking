# Results vs. 3.13.0rc2

- fork: python
- ref: e2118b0ac21191bfeecd
- machine: linux-x86_64
- commit hash: e2118b0
- commit date: 2026-08-25
- overall geometric mean: 1.030x faster
- HPT reliability: 99.77%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.62 sec                                                     | 2.36 sec: 1.11x faster                                                |
| html5lib       | 67.0 ms                                                      | 58.1 ms: 1.15x faster                                                 |
| Geometric mean | (ref)                                                        | 1.08x faster                                                          |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 539 ms: 1.24x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 378 ms: 1.22x faster                                                  |
| async_tree_io              | 876 ms                                                       | 720 ms: 1.22x faster                                                  |
| async_tree_none            | 354 ms                                                       | 291 ms: 1.22x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 761 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 558 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 296 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 366 ms: 1.13x faster                                                  |
| async_generators           | 377 ms                                                       | 347 ms: 1.09x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.14x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 187 ms: 1.16x faster                                                  |
| float          | 77.5 ms                                                      | 72.8 ms: 1.06x faster                                                 |
| nbody          | 85.1 ms                                                      | 91.5 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.58 ms: 1.19x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 21.8 ms: 1.04x faster                                                 |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                  |
| regex_compile  | 132 ms                                                       | 148 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.38 ms: 1.12x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.1 ms: 1.04x faster                                                 |
| json_loads           | 27.0 us                                                      | 27.4 us: 1.01x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 214 us: 1.02x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 304 us: 1.03x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 88.3 ms: 1.03x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 142 ms: 1.04x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 62.8 ms: 1.06x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.70 ms: 1.04x slower                                                 |
| python_startup         | 11.0 ms                                                      | 12.9 ms: 1.17x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| django_template | 34.1 ms                                                      | 37.0 ms: 1.09x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 114 ms: 2.78x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.13 sec: 2.08x faster                                                |
| deepcopy                   | 355 us                                                       | 236 us: 1.51x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 27.0 us: 1.45x faster                                                 |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 120 us: 1.29x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 539 ms: 1.24x faster                                                  |
| scimark_sor                | 134 ms                                                       | 109 ms: 1.23x faster                                                  |
| spectral_norm              | 111 ms                                                       | 90.1 ms: 1.23x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 378 ms: 1.22x faster                                                  |
| async_tree_io              | 876 ms                                                       | 720 ms: 1.22x faster                                                  |
| async_tree_none            | 354 ms                                                       | 291 ms: 1.22x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 761 ms: 1.20x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.58 ms: 1.19x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.62 us: 1.19x faster                                                 |
| pidigits                   | 217 ms                                                       | 187 ms: 1.16x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 58.1 ms: 1.15x faster                                                 |
| scimark_fft                | 349 ms                                                       | 304 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 558 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 296 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 366 ms: 1.13x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.38 ms: 1.12x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.79 sec: 1.12x faster                                                |
| pyflate                    | 449 ms                                                       | 401 ms: 1.12x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.36 sec: 1.11x faster                                                |
| dulwich_log                | 74.8 ms                                                      | 68.5 ms: 1.09x faster                                                 |
| async_generators           | 377 ms                                                       | 347 ms: 1.09x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 73.0 ms: 1.08x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.9 ms: 1.07x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.39 ms: 1.07x faster                                                 |
| chaos                      | 57.3 ms                                                      | 53.8 ms: 1.07x faster                                                 |
| float                      | 77.5 ms                                                      | 72.8 ms: 1.06x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.67 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.23 sec: 1.05x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.1 ms: 1.04x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.8 ms: 1.04x faster                                                 |
| logging_silent             | 103 ns                                                       | 99.1 ns: 1.04x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.2 ms: 1.03x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.9 us: 1.03x faster                                                 |
| logging_simple             | 6.16 us                                                      | 6.00 us: 1.03x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.3 ms: 1.02x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 724 ms: 1.02x faster                                                  |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                                  |
| richards                   | 45.2 ms                                                      | 44.4 ms: 1.02x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                |
| richards_super             | 51.6 ms                                                      | 50.9 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 67.4 ms: 1.01x faster                                                 |
| json                       | 4.93 ms                                                      | 4.90 ms: 1.01x faster                                                 |
| fannkuch                   | 370 ms                                                       | 373 ms: 1.01x slower                                                  |
| raytrace                   | 253 ms                                                       | 255 ms: 1.01x slower                                                  |
| generators                 | 28.8 ms                                                      | 29.2 ms: 1.01x slower                                                 |
| json_loads                 | 27.0 us                                                      | 27.4 us: 1.01x slower                                                 |
| meteor_contest             | 102 ms                                                       | 103 ms: 1.02x slower                                                  |
| thrift                     | 778 us                                                       | 790 us: 1.02x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.02x slower                                                |
| unpickle_pure_python       | 210 us                                                       | 214 us: 1.02x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.25 us: 1.02x slower                                                 |
| sympy_str                  | 275 ms                                                       | 280 ms: 1.02x slower                                                  |
| coverage                   | 83.0 ms                                                      | 85.4 ms: 1.03x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 160 ms: 1.03x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 304 us: 1.03x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 88.3 ms: 1.03x slower                                                 |
| sympy_expand               | 457 ms                                                       | 476 ms: 1.04x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 117 ms: 1.04x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.70 ms: 1.04x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 142 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 62.8 ms: 1.06x slower                                                 |
| nbody                      | 85.1 ms                                                      | 91.5 ms: 1.07x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.39 ms: 1.08x slower                                                 |
| django_template            | 34.1 ms                                                      | 37.0 ms: 1.09x slower                                                 |
| regex_compile              | 132 ms                                                       | 148 ms: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.9 ms: 1.17x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.76 ms: 1.20x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.64 ms: 1.23x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.35 ms: 1.47x slower                                                 |
| telco                      | 7.82 ms                                                      | 161 ms: 20.52x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 229 ms: 20.82x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (3): logging_format, coroutines, 2to3
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260825-3.16.0a0-e2118b0/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.030x faster

# HPT report

- Reliability score: 99.77% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x