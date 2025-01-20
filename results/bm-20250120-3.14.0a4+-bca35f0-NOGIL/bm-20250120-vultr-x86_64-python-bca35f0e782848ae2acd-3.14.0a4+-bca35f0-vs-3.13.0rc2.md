# Results vs. 3.13.0rc2

- fork: python
- ref: bca35f0e782848ae2acd
- machine: linux-x86_64
- commit hash: bca35f0
- commit date: 2025-01-20
- overall geometric mean: 1.089x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 305 ms: 1.17x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.82 sec: 1.08x slower                                                 |
| html5lib       | 67.0 ms                                                      | 71.3 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.10x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 579 ms: 1.58x faster                                                   |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.45x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 351 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 497 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 535 ms: 1.25x faster                                                   |
| async_tree_none            | 354 ms                                                       | 287 ms: 1.23x faster                                                   |
| async_generators           | 377 ms                                                       | 366 ms: 1.03x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.24x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 205 ms: 1.06x faster                                                   |
| nbody          | 85.1 ms                                                      | 128 ms: 1.50x slower                                                   |
| Geometric mean | (ref)                                                        | 1.12x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.92 ms: 1.05x faster                                                  |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                  |
| regex_compile  | 132 ms                                                       | 150 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                        | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.5 ms: 1.04x faster                                                  |
| json_loads           | 27.0 us                                                      | 30.2 us: 1.12x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 95.8 ms: 1.12x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 68.8 ms: 1.16x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.34 sec: 1.17x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 250 us: 1.19x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 13.0 ms: 1.24x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 373 us: 1.27x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.57 ms: 1.29x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 60.7 ms: 1.24x slower                                                  |
| django_template | 34.1 ms                                                      | 43.5 ms: 1.27x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 27.7 ms: 1.28x slower                                                  |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.37x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 579 ms: 1.58x faster                                                   |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.45x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.39x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 351 ms: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 497 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 535 ms: 1.25x faster                                                   |
| async_tree_none            | 354 ms                                                       | 287 ms: 1.23x faster                                                   |
| deepcopy                   | 355 us                                                       | 311 us: 1.14x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.08x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                   |
| pidigits                   | 217 ms                                                       | 205 ms: 1.06x faster                                                   |
| spectral_norm              | 111 ms                                                       | 105 ms: 1.05x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.92 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.5 ms: 1.04x faster                                                  |
| async_generators           | 377 ms                                                       | 366 ms: 1.03x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 18.6 ms: 1.03x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 38.5 us: 1.01x faster                                                  |
| scimark_sor                | 134 ms                                                       | 134 ms: 1.01x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                  |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.04x slower                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.66 sec: 1.05x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.19 sec: 1.06x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 71.3 ms: 1.06x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.32 us: 1.07x slower                                                  |
| telco                      | 7.82 ms                                                      | 8.36 ms: 1.07x slower                                                  |
| json                       | 4.93 ms                                                      | 5.29 ms: 1.07x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.82 sec: 1.08x slower                                                 |
| generators                 | 28.8 ms                                                      | 31.4 ms: 1.09x slower                                                  |
| scimark_fft                | 349 ms                                                       | 382 ms: 1.09x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 82.0 ms: 1.10x slower                                                  |
| pyflate                    | 449 ms                                                       | 492 ms: 1.10x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                  |
| json_loads                 | 27.0 us                                                      | 30.2 us: 1.12x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 95.8 ms: 1.12x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 831 ms: 1.13x slower                                                   |
| regex_compile              | 132 ms                                                       | 150 ms: 1.13x slower                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.71 sec: 1.14x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 121 ms: 1.15x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 68.8 ms: 1.16x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.47 ms: 1.16x slower                                                  |
| logging_silent             | 103 ns                                                       | 119 ns: 1.16x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.34 sec: 1.17x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 61.6 ms: 1.17x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.69 ms: 1.17x slower                                                  |
| 2to3                       | 260 ms                                                       | 305 ms: 1.17x slower                                                   |
| coverage                   | 83.0 ms                                                      | 97.5 ms: 1.17x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.78 sec: 1.18x slower                                                 |
| thrift                     | 778 us                                                       | 920 us: 1.18x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 250 us: 1.19x slower                                                   |
| logging_simple             | 6.16 us                                                      | 7.39 us: 1.20x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 187 ms: 1.20x slower                                                   |
| chaos                      | 57.3 ms                                                      | 69.0 ms: 1.20x slower                                                  |
| sympy_expand               | 457 ms                                                       | 551 ms: 1.20x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 95.0 ms: 1.21x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 137 ms: 1.21x slower                                                   |
| sympy_integrate            | 19.8 ms                                                      | 24.2 ms: 1.22x slower                                                  |
| sympy_str                  | 275 ms                                                       | 336 ms: 1.22x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 7.36 ms: 1.23x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.45 us: 1.23x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 13.0 ms: 1.24x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.94 ms: 1.24x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 60.7 ms: 1.24x slower                                                  |
| richards                   | 45.2 ms                                                      | 56.7 ms: 1.25x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 373 us: 1.27x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 82.8 ms: 1.27x slower                                                  |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                                   |
| django_template            | 34.1 ms                                                      | 43.5 ms: 1.27x slower                                                  |
| fannkuch                   | 370 ms                                                       | 472 ms: 1.28x slower                                                   |
| comprehensions             | 16.5 us                                                      | 21.0 us: 1.28x slower                                                  |
| richards_super             | 51.6 ms                                                      | 66.0 ms: 1.28x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 86.8 ms: 1.28x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 198 us: 1.28x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 27.7 ms: 1.28x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.61 ms: 1.29x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.57 ms: 1.29x slower                                                  |
| raytrace                   | 253 ms                                                       | 335 ms: 1.32x slower                                                   |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.37x slower                                                  |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                  |
| nbody                      | 85.1 ms                                                      | 128 ms: 1.50x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 4.73 ms: 1.51x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.30 ms: 3.60x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 94.7 ms: 8.62x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.14x slower                                                           |

Benchmark hidden because not significant (5): float, asyncio_websockets, create_gc_cycles, go, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-vultr-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.089x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.33x