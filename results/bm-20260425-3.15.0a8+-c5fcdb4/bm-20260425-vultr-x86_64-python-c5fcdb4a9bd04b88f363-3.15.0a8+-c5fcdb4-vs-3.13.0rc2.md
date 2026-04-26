# Results vs. 3.13.0rc2

- fork: python
- ref: c5fcdb4a9bd04b88f363
- machine: linux-x86_64
- commit hash: c5fcdb4
- commit date: 2026-04-25
- overall geometric mean: 1.051x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 256 ms: 1.02x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.46 sec: 1.06x faster                                                 |
| html5lib       | 67.0 ms                                                      | 59.5 ms: 1.13x faster                                                  |
| Geometric mean | (ref)                                                        | 1.07x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 594 ms: 1.54x faster                                                   |
| async_tree_io              | 876 ms                                                       | 584 ms: 1.50x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                                   |
| async_tree_none            | 354 ms                                                       | 246 ms: 1.44x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 303 ms: 1.37x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 490 ms: 1.30x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 446 ms: 1.13x faster                                                   |
| async_generators           | 377 ms                                                       | 346 ms: 1.09x faster                                                   |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.46 sec: 1.03x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| float          | 77.5 ms                                                      | 70.1 ms: 1.10x faster                                                  |
| nbody          | 85.1 ms                                                      | 93.2 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                  |
| regex_compile  | 132 ms                                                       | 125 ms: 1.06x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 21.9 ms: 1.04x faster                                                  |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.4 ms: 1.12x faster                                                  |
| json_dumps           | 10.5 ms                                                      | 9.61 ms: 1.10x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                 |
| pickle_dict          | 32.5 us                                                      | 30.4 us: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.01x slower                                                   |
| pickle_list          | 4.93 us                                                      | 4.99 us: 1.01x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 87.1 ms: 1.02x slower                                                  |
| json_loads           | 27.0 us                                                      | 27.7 us: 1.03x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 61.5 ms: 1.04x slower                                                  |
| unpickle             | 14.3 us                                                      | 14.9 us: 1.04x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 308 us: 1.05x slower                                                   |
| unpickle_list        | 4.71 us                                                      | 5.17 us: 1.10x slower                                                  |
| pickle               | 11.3 us                                                      | 12.6 us: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 6.82 ms: 1.08x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.02x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.0 ms: 1.02x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.2 ms: 1.03x slower                                                  |
| django_template | 34.1 ms                                                      | 35.8 ms: 1.05x slower                                                  |
| mako            | 11.3 ms                                                      | 12.2 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 116 ms: 2.73x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.16 sec: 2.04x faster                                                 |
| deepcopy                   | 355 us                                                       | 231 us: 1.54x faster                                                   |
| async_tree_io_tg           | 913 ms                                                       | 594 ms: 1.54x faster                                                   |
| async_tree_io              | 876 ms                                                       | 584 ms: 1.50x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 313 ms: 1.47x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.9 us: 1.46x faster                                                  |
| async_tree_none            | 354 ms                                                       | 246 ms: 1.44x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 303 ms: 1.37x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 248 ms: 1.35x faster                                                   |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 490 ms: 1.30x faster                                                   |
| scimark_sor                | 134 ms                                                       | 109 ms: 1.23x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.58 us: 1.21x faster                                                  |
| spectral_norm              | 111 ms                                                       | 93.6 ms: 1.19x faster                                                  |
| pidigits                   | 217 ms                                                       | 185 ms: 1.17x faster                                                   |
| asyncio_tcp                | 505 ms                                                       | 446 ms: 1.13x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 59.5 ms: 1.13x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.4 ms: 1.12x faster                                                  |
| scimark_fft                | 349 ms                                                       | 314 ms: 1.11x faster                                                   |
| dulwich_log                | 74.8 ms                                                      | 67.7 ms: 1.11x faster                                                  |
| float                      | 77.5 ms                                                      | 70.1 ms: 1.10x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.61 ms: 1.10x faster                                                  |
| async_generators           | 377 ms                                                       | 346 ms: 1.09x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 17.6 ms: 1.09x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 6.82 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.11 sec: 1.08x faster                                                 |
| pyflate                    | 449 ms                                                       | 415 ms: 1.08x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 1.86 sec: 1.08x faster                                                 |
| richards_super             | 51.6 ms                                                      | 48.2 ms: 1.07x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.39 ms: 1.07x faster                                                  |
| richards                   | 45.2 ms                                                      | 42.2 ms: 1.07x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.75 us: 1.07x faster                                                  |
| pickle_dict                | 32.5 us                                                      | 30.4 us: 1.07x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.63 ms: 1.06x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.46 sec: 1.06x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.45 us: 1.06x faster                                                  |
| regex_compile              | 132 ms                                                       | 125 ms: 1.06x faster                                                   |
| chaos                      | 57.3 ms                                                      | 54.2 ms: 1.06x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 74.6 ms: 1.05x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.0 ms: 1.04x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.9 ms: 1.04x faster                                                  |
| comprehensions             | 16.5 us                                                      | 15.9 us: 1.04x faster                                                  |
| logging_silent             | 103 ns                                                       | 99.3 ns: 1.03x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.46 sec: 1.03x faster                                                 |
| pycparser                  | 1.12 sec                                                     | 1.08 sec: 1.03x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.03x faster                                                   |
| genshi_text                | 21.5 ms                                                      | 21.0 ms: 1.02x faster                                                  |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                                   |
| pprint_safe_repr           | 738 ms                                                       | 725 ms: 1.02x faster                                                   |
| 2to3                       | 260 ms                                                       | 256 ms: 1.02x faster                                                   |
| generators                 | 28.8 ms                                                      | 28.4 ms: 1.02x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 64.4 ms: 1.02x faster                                                  |
| thrift                     | 778 us                                                       | 767 us: 1.01x faster                                                   |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.01x faster                                                   |
| coverage                   | 83.0 ms                                                      | 82.1 ms: 1.01x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.4 ms: 1.01x faster                                                  |
| raytrace                   | 253 ms                                                       | 252 ms: 1.00x faster                                                   |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.01x slower                                                   |
| pickle_list                | 4.93 us                                                      | 4.99 us: 1.01x slower                                                  |
| unpack_sequence            | 44.8 ns                                                      | 45.5 ns: 1.02x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 87.1 ms: 1.02x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.7 us: 1.03x slower                                                  |
| json                       | 4.93 ms                                                      | 5.06 ms: 1.03x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 69.8 ms: 1.03x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 50.2 ms: 1.03x slower                                                  |
| sympy_expand               | 457 ms                                                       | 472 ms: 1.03x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 61.5 ms: 1.04x slower                                                  |
| fannkuch                   | 370 ms                                                       | 383 ms: 1.04x slower                                                   |
| unpickle                   | 14.3 us                                                      | 14.9 us: 1.04x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 161 us: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.27 ms: 1.05x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 308 us: 1.05x slower                                                   |
| django_template            | 34.1 ms                                                      | 35.8 ms: 1.05x slower                                                  |
| mako                       | 11.3 ms                                                      | 12.2 ms: 1.08x slower                                                  |
| nbody                      | 85.1 ms                                                      | 93.2 ms: 1.10x slower                                                  |
| unpickle_list              | 4.71 us                                                      | 5.17 us: 1.10x slower                                                  |
| pickle                     | 11.3 us                                                      | 12.6 us: 1.11x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.36 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.94 ms: 1.45x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.33 ms: 1.45x slower                                                  |
| telco                      | 7.82 ms                                                      | 158 ms: 20.20x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 273 ms: 24.82x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (3): sympy_str, sympy_sum, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260425-3.15.0a8+-c5fcdb4/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.051x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.17x