# Results vs. 3.13.0rc2

- fork: python
- ref: e66f87ca73516efb4aec
- machine: linux-x86_64
- commit hash: e66f87c
- commit date: 2025-11-02
- overall geometric mean: 1.043x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 247 ms: 1.05x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                 |
| html5lib       | 67.0 ms                                                      | 60.8 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 557 ms: 1.57x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 593 ms: 1.54x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 308 ms: 1.50x faster                                                   |
| async_tree_none            | 354 ms                                                       | 246 ms: 1.44x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 510 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 509 ms: 1.25x faster                                                   |
| async_generators           | 377 ms                                                       | 337 ms: 1.12x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 69.2 ms: 1.12x faster                                                  |
| pidigits       | 217 ms                                                       | 214 ms: 1.01x faster                                                   |
| nbody          | 85.1 ms                                                      | 86.9 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.64 ms: 1.17x faster                                                  |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| regex_dna      | 180 ms                                                       | 173 ms: 1.04x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.2 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.4 ms: 1.12x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 9.49 ms: 1.11x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.90 sec: 1.05x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 82.4 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.4 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 211 us: 1.01x slower                                                   |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 306 us: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.20 ms: 1.03x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 20.6 ms: 1.05x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 47.8 ms: 1.02x faster                                                  |
| django_template | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                  |
| mako            | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.06x faster                                                 |
| async_tree_io              | 876 ms                                                       | 557 ms: 1.57x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 593 ms: 1.54x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 308 ms: 1.50x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.5 us: 1.48x faster                                                  |
| deepcopy                   | 355 us                                                       | 245 us: 1.45x faster                                                   |
| async_tree_none            | 354 ms                                                       | 246 ms: 1.44x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 246 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                   |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 510 ms: 1.31x faster                                                   |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 509 ms: 1.25x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.58 us: 1.20x faster                                                  |
| spectral_norm              | 111 ms                                                       | 95.0 ms: 1.17x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.64 ms: 1.17x faster                                                  |
| scimark_fft                | 349 ms                                                       | 305 ms: 1.14x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.4 ms: 1.12x faster                                                  |
| float                      | 77.5 ms                                                      | 69.2 ms: 1.12x faster                                                  |
| async_generators           | 377 ms                                                       | 337 ms: 1.12x faster                                                   |
| json_dumps                 | 10.5 ms                                                      | 9.49 ms: 1.11x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.24 ms: 1.11x faster                                                  |
| pyflate                    | 449 ms                                                       | 406 ms: 1.10x faster                                                   |
| pylint                     | 317 ms                                                       | 287 ms: 1.10x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 60.8 ms: 1.10x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 68.4 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.09x faster                                                  |
| richards_super             | 51.6 ms                                                      | 47.8 ms: 1.08x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.57 ms: 1.08x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.2 ms: 1.07x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 61.0 ms: 1.07x faster                                                  |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| logging_simple             | 6.16 us                                                      | 5.79 us: 1.06x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 696 ms: 1.06x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.20 sec: 1.06x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.42 sec: 1.06x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.90 sec: 1.05x faster                                                 |
| 2to3                       | 260 ms                                                       | 247 ms: 1.05x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 20.6 ms: 1.05x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 108 ms: 1.04x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 19.0 ms: 1.04x faster                                                  |
| regex_dna                  | 180 ms                                                       | 173 ms: 1.04x faster                                                   |
| pycparser                  | 1.12 sec                                                     | 1.07 sec: 1.04x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.58 us: 1.04x faster                                                  |
| comprehensions             | 16.5 us                                                      | 15.9 us: 1.04x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 82.4 ms: 1.04x faster                                                  |
| thrift                     | 778 us                                                       | 754 us: 1.03x faster                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.20 ms: 1.03x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.2 ms: 1.02x faster                                                  |
| chaos                      | 57.3 ms                                                      | 56.0 ms: 1.02x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.1 ms: 1.02x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.2 ms: 1.02x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 47.8 ms: 1.02x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 77.2 ms: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.57 sec: 1.02x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 58.4 ms: 1.02x faster                                                  |
| raytrace                   | 253 ms                                                       | 249 ms: 1.01x faster                                                   |
| logging_silent             | 103 ns                                                       | 101 ns: 1.01x faster                                                   |
| pidigits                   | 217 ms                                                       | 214 ms: 1.01x faster                                                   |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 155 ms: 1.00x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 211 us: 1.01x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 69.3 ms: 1.02x slower                                                  |
| nbody                      | 85.1 ms                                                      | 86.9 ms: 1.02x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.26 us: 1.02x slower                                                  |
| json                       | 4.93 ms                                                      | 5.04 ms: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.9 us: 1.03x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 306 us: 1.04x slower                                                   |
| sympy_expand               | 457 ms                                                       | 475 ms: 1.04x slower                                                   |
| fannkuch                   | 370 ms                                                       | 387 ms: 1.05x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.31 ms: 1.06x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.00 ms: 1.09x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.09 ms: 1.30x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.92 ms: 1.44x slower                                                  |
| telco                      | 7.82 ms                                                      | 157 ms: 20.13x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (2): sympy_str, typing_runtime_protocols
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251102-3.15.0a1+-e66f87c/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.043x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x