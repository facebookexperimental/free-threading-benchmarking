# Results vs. 3.13.0rc2

- fork: python
- ref: a6bc60da02ea37f33d5a
- machine: linux-x86_64
- commit hash: a6bc60d
- commit date: 2026-01-12
- overall geometric mean: 1.035x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                 |
| html5lib       | 67.0 ms                                                      | 60.0 ms: 1.12x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 561 ms: 1.63x faster                                                   |
| async_tree_io              | 876 ms                                                       | 551 ms: 1.59x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 301 ms: 1.53x faster                                                   |
| async_tree_none            | 354 ms                                                       | 243 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 296 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 483 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 250 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 487 ms: 1.31x faster                                                   |
| async_generators           | 377 ms                                                       | 345 ms: 1.09x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 70.1 ms: 1.11x faster                                                  |
| pidigits       | 217 ms                                                       | 196 ms: 1.10x faster                                                   |
| nbody          | 85.1 ms                                                      | 93.3 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                                  |
| regex_compile  | 132 ms                                                       | 123 ms: 1.08x faster                                                   |
| regex_dna      | 180 ms                                                       | 178 ms: 1.01x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.8 ms: 1.12x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 9.79 ms: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 84.1 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 59.0 ms: 1.01x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 212 us: 1.01x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.1 us: 1.04x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 313 us: 1.06x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.27 ms: 1.02x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 49.9 ms: 1.02x slower                                                  |
| mako            | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                  |
| django_template | 34.1 ms                                                      | 36.3 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.17 sec: 2.02x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 561 ms: 1.63x faster                                                   |
| async_tree_io              | 876 ms                                                       | 551 ms: 1.59x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 301 ms: 1.53x faster                                                   |
| deepcopy                   | 355 us                                                       | 236 us: 1.51x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.4 us: 1.48x faster                                                  |
| async_tree_none            | 354 ms                                                       | 243 ms: 1.46x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 296 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 483 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 250 ms: 1.35x faster                                                   |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 487 ms: 1.31x faster                                                   |
| scimark_sor                | 134 ms                                                       | 106 ms: 1.27x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.62 us: 1.19x faster                                                  |
| spectral_norm              | 111 ms                                                       | 95.1 ms: 1.17x faster                                                  |
| scimark_fft                | 349 ms                                                       | 308 ms: 1.14x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.8 ms: 1.12x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 60.0 ms: 1.12x faster                                                  |
| pylint                     | 317 ms                                                       | 284 ms: 1.12x faster                                                   |
| float                      | 77.5 ms                                                      | 70.1 ms: 1.11x faster                                                  |
| pidigits                   | 217 ms                                                       | 196 ms: 1.10x faster                                                   |
| async_generators           | 377 ms                                                       | 345 ms: 1.09x faster                                                   |
| pyflate                    | 449 ms                                                       | 412 ms: 1.09x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 69.1 ms: 1.08x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.0 ms: 1.08x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.0 ms: 1.08x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.79 ms: 1.08x faster                                                  |
| regex_compile              | 132 ms                                                       | 123 ms: 1.08x faster                                                   |
| hexiom                     | 5.99 ms                                                      | 5.61 ms: 1.07x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.19 sec: 1.06x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.44 ms: 1.06x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.90 us: 1.04x faster                                                  |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.6 ms: 1.04x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 707 ms: 1.04x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.44 sec: 1.04x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.03x faster                                                   |
| sympy_integrate            | 19.8 ms                                                      | 19.3 ms: 1.03x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.0 ms: 1.03x faster                                                  |
| logging_silent             | 103 ns                                                       | 99.8 ns: 1.03x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                 |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.71 us: 1.02x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.27 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 84.1 ms: 1.02x faster                                                  |
| regex_dna                  | 180 ms                                                       | 178 ms: 1.01x faster                                                   |
| coverage                   | 83.0 ms                                                      | 82.0 ms: 1.01x faster                                                  |
| chaos                      | 57.3 ms                                                      | 56.9 ms: 1.01x faster                                                  |
| thrift                     | 778 us                                                       | 773 us: 1.01x faster                                                   |
| xml_etree_process          | 59.3 ms                                                      | 59.0 ms: 1.01x faster                                                  |
| raytrace                   | 253 ms                                                       | 253 ms: 1.00x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 212 us: 1.01x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                 |
| sympy_str                  | 275 ms                                                       | 279 ms: 1.02x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 80.2 ms: 1.02x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 69.4 ms: 1.02x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 49.9 ms: 1.02x slower                                                  |
| fannkuch                   | 370 ms                                                       | 381 ms: 1.03x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 160 us: 1.03x slower                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.29 us: 1.04x slower                                                  |
| json                       | 4.93 ms                                                      | 5.12 ms: 1.04x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.1 us: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.31 ms: 1.06x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 313 us: 1.06x slower                                                   |
| django_template            | 34.1 ms                                                      | 36.3 ms: 1.06x slower                                                  |
| sympy_expand               | 457 ms                                                       | 492 ms: 1.08x slower                                                   |
| nbody                      | 85.1 ms                                                      | 93.3 ms: 1.10x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.34 ms: 1.38x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.87 ms: 1.40x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.44x slower                                                  |
| telco                      | 7.82 ms                                                      | 160 ms: 20.42x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 319 ms: 28.97x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (3): meteor_contest, genshi_text, sympy_sum
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260112-3.15.0a3+-a6bc60d/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.035x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.15x