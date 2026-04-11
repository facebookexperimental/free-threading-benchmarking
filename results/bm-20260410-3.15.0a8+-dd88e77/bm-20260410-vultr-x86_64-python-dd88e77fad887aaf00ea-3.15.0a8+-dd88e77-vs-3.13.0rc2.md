# Results vs. 3.13.0rc2

- fork: python
- ref: dd88e77fad887aaf00ea
- machine: linux-x86_64
- commit hash: dd88e77
- commit date: 2026-04-10
- overall geometric mean: 1.028x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 257 ms: 1.01x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.45 sec: 1.07x faster                                                 |
| html5lib       | 67.0 ms                                                      | 59.9 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 597 ms: 1.53x faster                                                   |
| async_tree_io              | 876 ms                                                       | 590 ms: 1.49x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 321 ms: 1.43x faster                                                   |
| async_tree_none            | 354 ms                                                       | 249 ms: 1.42x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 501 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 254 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 495 ms: 1.29x faster                                                   |
| async_generators           | 377 ms                                                       | 344 ms: 1.10x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                   |
| float          | 77.5 ms                                                      | 70.8 ms: 1.09x faster                                                  |
| nbody          | 85.1 ms                                                      | 96.9 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| regex_effbot   | 3.08 ms                                                      | 2.92 ms: 1.06x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.9 ms: 1.03x faster                                                  |
| regex_dna      | 180 ms                                                       | 189 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.7 ms: 1.12x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.83 sec: 1.09x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 9.66 ms: 1.09x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 84.5 ms: 1.01x faster                                                  |
| json_loads           | 27.0 us                                                      | 27.2 us: 1.01x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 59.8 ms: 1.01x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 215 us: 1.03x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 317 us: 1.08x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.46 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                      | 12.7 ms: 1.15x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.08x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 49.9 ms: 1.02x slower                                                  |
| django_template | 34.1 ms                                                      | 36.0 ms: 1.06x slower                                                  |
| mako            | 11.3 ms                                                      | 12.2 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.05x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 597 ms: 1.53x faster                                                   |
| deepcopy                   | 355 us                                                       | 238 us: 1.49x faster                                                   |
| async_tree_io              | 876 ms                                                       | 590 ms: 1.49x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 321 ms: 1.43x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 27.5 us: 1.42x faster                                                  |
| async_tree_none            | 354 ms                                                       | 249 ms: 1.42x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                   |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 501 ms: 1.33x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 254 ms: 1.32x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 495 ms: 1.29x faster                                                   |
| scimark_sor                | 134 ms                                                       | 111 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.61 us: 1.19x faster                                                  |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                   |
| spectral_norm              | 111 ms                                                       | 94.6 ms: 1.17x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.7 ms: 1.12x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 59.9 ms: 1.12x faster                                                  |
| pylint                     | 317 ms                                                       | 284 ms: 1.12x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 17.3 ms: 1.11x faster                                                  |
| scimark_fft                | 349 ms                                                       | 317 ms: 1.10x faster                                                   |
| async_generators           | 377 ms                                                       | 344 ms: 1.10x faster                                                   |
| float                      | 77.5 ms                                                      | 70.8 ms: 1.09x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.83 sec: 1.09x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.66 ms: 1.09x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 68.8 ms: 1.09x faster                                                  |
| pyflate                    | 449 ms                                                       | 414 ms: 1.08x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.15 sec: 1.07x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.45 sec: 1.07x faster                                                 |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.92 ms: 1.06x faster                                                  |
| chaos                      | 57.3 ms                                                      | 54.4 ms: 1.05x faster                                                  |
| richards                   | 45.2 ms                                                      | 43.0 ms: 1.05x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.87 us: 1.05x faster                                                  |
| richards_super             | 51.6 ms                                                      | 49.4 ms: 1.05x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 75.4 ms: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| logging_format             | 6.84 us                                                      | 6.57 us: 1.04x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.78 ms: 1.04x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.9 ms: 1.03x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.55 ms: 1.03x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.4 ms: 1.03x faster                                                  |
| logging_silent             | 103 ns                                                       | 99.7 ns: 1.03x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 724 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                 |
| genshi_text                | 21.5 ms                                                      | 21.3 ms: 1.01x faster                                                  |
| 2to3                       | 260 ms                                                       | 257 ms: 1.01x faster                                                   |
| coverage                   | 83.0 ms                                                      | 82.1 ms: 1.01x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 84.5 ms: 1.01x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.3 us: 1.01x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 112 ms: 1.01x faster                                                   |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                   |
| thrift                     | 778 us                                                       | 773 us: 1.01x faster                                                   |
| json_loads                 | 27.0 us                                                      | 27.2 us: 1.01x slower                                                  |
| raytrace                   | 253 ms                                                       | 254 ms: 1.01x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 59.8 ms: 1.01x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.46 ms: 1.01x slower                                                  |
| sympy_str                  | 275 ms                                                       | 278 ms: 1.01x slower                                                   |
| json                       | 4.93 ms                                                      | 4.99 ms: 1.01x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 158 ms: 1.02x slower                                                   |
| generators                 | 28.8 ms                                                      | 29.3 ms: 1.02x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 49.9 ms: 1.02x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 215 us: 1.03x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 159 us: 1.03x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 70.4 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                   |
| regex_dna                  | 180 ms                                                       | 189 ms: 1.05x slower                                                   |
| django_template            | 34.1 ms                                                      | 36.0 ms: 1.06x slower                                                  |
| fannkuch                   | 370 ms                                                       | 391 ms: 1.06x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.30 ms: 1.06x slower                                                  |
| sympy_expand               | 457 ms                                                       | 485 ms: 1.06x slower                                                   |
| mako                       | 11.3 ms                                                      | 12.2 ms: 1.08x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 317 us: 1.08x slower                                                   |
| nbody                      | 85.1 ms                                                      | 96.9 ms: 1.14x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.7 ms: 1.15x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.36 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.92 ms: 1.44x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.33 ms: 1.45x slower                                                  |
| telco                      | 7.82 ms                                                      | 158 ms: 20.24x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 303 ms: 27.56x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (2): pycparser, sqlite_synth
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260410-3.15.0a8+-dd88e77/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8+-dd88e77.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.028x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.17x