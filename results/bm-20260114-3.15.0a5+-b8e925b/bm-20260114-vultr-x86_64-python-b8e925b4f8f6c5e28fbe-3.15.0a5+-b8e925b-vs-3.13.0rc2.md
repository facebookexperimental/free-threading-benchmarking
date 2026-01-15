# Results vs. 3.13.0rc2

- fork: python
- ref: b8e925b4f8f6c5e28fbe
- machine: linux-x86_64
- commit hash: b8e925b
- commit date: 2026-01-14
- overall geometric mean: 1.039x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| html5lib       | 67.0 ms                                                      | 59.6 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 547 ms: 1.60x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 587 ms: 1.56x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 305 ms: 1.51x faster                                                   |
| async_tree_none            | 354 ms                                                       | 241 ms: 1.47x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 242 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 485 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                   |
| async_generators           | 377 ms                                                       | 353 ms: 1.07x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                   |
| float          | 77.5 ms                                                      | 70.3 ms: 1.10x faster                                                  |
| nbody          | 85.1 ms                                                      | 91.2 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.87 ms: 1.08x faster                                                  |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.1 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 85.3 ms: 1.11x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.83 sec: 1.10x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 9.69 ms: 1.09x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 82.6 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 57.8 ms: 1.03x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.02x slower                                                   |
| json_loads           | 27.0 us                                                      | 27.6 us: 1.02x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 311 us: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.29 ms: 1.01x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 49.2 ms: 1.01x slower                                                  |
| django_template | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.16 sec: 2.04x faster                                                 |
| async_tree_io              | 876 ms                                                       | 547 ms: 1.60x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 587 ms: 1.56x faster                                                   |
| deepcopy                   | 355 us                                                       | 232 us: 1.53x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 305 ms: 1.51x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 25.9 us: 1.51x faster                                                  |
| async_tree_none            | 354 ms                                                       | 241 ms: 1.47x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 242 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 485 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 304 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                   |
| go                         | 141 ms                                                       | 108 ms: 1.30x faster                                                   |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.25x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.52 us: 1.23x faster                                                  |
| spectral_norm              | 111 ms                                                       | 96.4 ms: 1.15x faster                                                  |
| scimark_fft                | 349 ms                                                       | 306 ms: 1.14x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 59.6 ms: 1.12x faster                                                  |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                   |
| pylint                     | 317 ms                                                       | 284 ms: 1.12x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 85.3 ms: 1.11x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 67.3 ms: 1.11x faster                                                  |
| float                      | 77.5 ms                                                      | 70.3 ms: 1.10x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.83 sec: 1.10x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.69 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.08x faster                                                  |
| pyflate                    | 449 ms                                                       | 414 ms: 1.08x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.36 ms: 1.08x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.87 ms: 1.08x faster                                                  |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| async_generators           | 377 ms                                                       | 353 ms: 1.07x faster                                                   |
| richards_super             | 51.6 ms                                                      | 48.3 ms: 1.07x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.6 ms: 1.06x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.84 us: 1.06x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.22 sec: 1.05x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 18.9 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 704 ms: 1.05x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.72 ms: 1.05x faster                                                  |
| logging_silent             | 103 ns                                                       | 98.1 ns: 1.05x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.05x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 108 ms: 1.05x faster                                                   |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.7 ms: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| logging_format             | 6.84 us                                                      | 6.59 us: 1.04x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 82.6 ms: 1.03x faster                                                  |
| generators                 | 28.8 ms                                                      | 27.9 ms: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.54 sec: 1.03x faster                                                 |
| thrift                     | 778 us                                                       | 757 us: 1.03x faster                                                   |
| regex_v8                   | 22.7 ms                                                      | 22.1 ms: 1.03x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 57.8 ms: 1.03x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.4 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.02x faster                                                  |
| chaos                      | 57.3 ms                                                      | 56.5 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.29 ms: 1.01x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                   |
| raytrace                   | 253 ms                                                       | 253 ms: 1.00x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.12 sec: 1.01x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 49.2 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.24 us: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.02x slower                                                   |
| json_loads                 | 27.0 us                                                      | 27.6 us: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 34.9 ms: 1.02x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 69.6 ms: 1.03x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 311 us: 1.06x slower                                                   |
| fannkuch                   | 370 ms                                                       | 394 ms: 1.07x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.34 ms: 1.07x slower                                                  |
| sympy_expand               | 457 ms                                                       | 489 ms: 1.07x slower                                                   |
| nbody                      | 85.1 ms                                                      | 91.2 ms: 1.07x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.30 ms: 1.37x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.91 ms: 1.43x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.43x slower                                                  |
| telco                      | 7.82 ms                                                      | 158 ms: 20.15x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 313 ms: 28.48x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (6): meteor_contest, genshi_text, sympy_str, nqueens, json, regex_dna
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260114-3.15.0a5+-b8e925b/bm-20260114-vultr-x86_64-python-b8e925b4f8f6c5e28fbe-3.15.0a5+-b8e925b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.039x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.16x