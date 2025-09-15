# Results vs. 3.13.0rc2

- fork: python
- ref: fa12c6bae47a41dd84e5
- machine: linux-x86_64
- commit hash: fa12c6b
- commit date: 2025-09-15
- overall geometric mean: 1.037x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 251 ms: 1.04x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.58 sec: 1.01x faster                                                |
| html5lib       | 67.0 ms                                                      | 63.3 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 314 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 625 ms: 1.46x faster                                                  |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 500 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 267 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 502 ms: 1.27x faster                                                  |
| async_generators           | 377 ms                                                       | 339 ms: 1.11x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.1 ms: 1.02x faster                                                 |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 71.3 ms: 1.09x faster                                                 |
| pidigits       | 217 ms                                                       | 209 ms: 1.04x faster                                                  |
| nbody          | 85.1 ms                                                      | 90.4 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.69 ms: 1.15x faster                                                 |
| regex_compile  | 132 ms                                                       | 123 ms: 1.08x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.3 ms: 1.07x faster                                                 |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.48 ms: 1.11x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.8 ms: 1.02x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.6 ms: 1.02x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 207 us: 1.01x faster                                                  |
| pickle_pure_python   | 294 us                                                       | 303 us: 1.03x slower                                                  |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 21.5 ms                                                      | 20.4 ms: 1.06x faster                                                 |
| genshi_xml     | 48.8 ms                                                      | 49.3 ms: 1.01x slower                                                 |
| mako           | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.05x faster                                                |
| deepcopy_memo              | 39.1 us                                                      | 26.3 us: 1.49x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 314 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 625 ms: 1.46x faster                                                  |
| deepcopy                   | 355 us                                                       | 243 us: 1.46x faster                                                  |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.45x faster                                                  |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 252 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 500 ms: 1.33x faster                                                  |
| async_tree_none            | 354 ms                                                       | 267 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 502 ms: 1.27x faster                                                  |
| scimark_sor                | 134 ms                                                       | 108 ms: 1.24x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.59 us: 1.20x faster                                                 |
| spectral_norm              | 111 ms                                                       | 94.1 ms: 1.18x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.69 ms: 1.15x faster                                                 |
| pylint                     | 317 ms                                                       | 279 ms: 1.14x faster                                                  |
| pyflate                    | 449 ms                                                       | 397 ms: 1.13x faster                                                  |
| async_generators           | 377 ms                                                       | 339 ms: 1.11x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 67.3 ms: 1.11x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.48 ms: 1.11x faster                                                 |
| richards                   | 45.2 ms                                                      | 41.2 ms: 1.10x faster                                                 |
| richards_super             | 51.6 ms                                                      | 47.1 ms: 1.10x faster                                                 |
| float                      | 77.5 ms                                                      | 71.3 ms: 1.09x faster                                                 |
| regex_compile              | 132 ms                                                       | 123 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.15 sec: 1.07x faster                                                |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.2 ms: 1.07x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.77 us: 1.07x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.07x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.3 ms: 1.07x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.89 sec: 1.06x faster                                                |
| hexiom                     | 5.99 ms                                                      | 5.66 ms: 1.06x faster                                                 |
| scimark_fft                | 349 ms                                                       | 330 ms: 1.06x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 63.3 ms: 1.06x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 20.4 ms: 1.06x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.6 us: 1.06x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 18.8 ms: 1.05x faster                                                 |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.52 us: 1.05x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 705 ms: 1.05x faster                                                  |
| logging_silent             | 103 ns                                                       | 98.4 ns: 1.04x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.44 sec: 1.04x faster                                                |
| pidigits                   | 217 ms                                                       | 209 ms: 1.04x faster                                                  |
| 2to3                       | 260 ms                                                       | 251 ms: 1.04x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.03x faster                                                |
| nqueens                    | 78.6 ms                                                      | 76.5 ms: 1.03x faster                                                 |
| meteor_contest             | 102 ms                                                       | 98.9 ms: 1.03x faster                                                 |
| generators                 | 28.8 ms                                                      | 28.1 ms: 1.02x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.0 ms: 1.02x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.8 ms: 1.02x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 83.6 ms: 1.02x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.24 ms: 1.02x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.1 ms: 1.02x faster                                                 |
| sympy_str                  | 275 ms                                                       | 269 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 152 us: 1.02x faster                                                  |
| unpickle_pure_python       | 210 us                                                       | 207 us: 1.01x faster                                                  |
| thrift                     | 778 us                                                       | 768 us: 1.01x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.58 sec: 1.01x faster                                                |
| sympy_sum                  | 156 ms                                                       | 154 ms: 1.01x faster                                                  |
| coverage                   | 83.0 ms                                                      | 82.3 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 68.2 ms: 1.00x slower                                                 |
| sympy_expand               | 457 ms                                                       | 460 ms: 1.01x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 49.3 ms: 1.01x slower                                                 |
| fannkuch                   | 370 ms                                                       | 374 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.78 ms: 1.02x slower                                                 |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                 |
| json                       | 4.93 ms                                                      | 5.06 ms: 1.03x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 303 us: 1.03x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.24 ms: 1.04x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.30 us: 1.04x slower                                                 |
| nbody                      | 85.1 ms                                                      | 90.4 ms: 1.06x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.01 ms: 1.10x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                 |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.13x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.91 ms: 1.43x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.53 ms: 1.44x slower                                                 |
| telco                      | 7.82 ms                                                      | 159 ms: 20.37x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (4): chaos, raytrace, django_template, asyncio_websockets
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250915-3.15.0a0-fa12c6b/bm-20250915-vultr-x86_64-python-fa12c6bae47a41dd84e5-3.15.0a0-fa12c6b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.037x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x