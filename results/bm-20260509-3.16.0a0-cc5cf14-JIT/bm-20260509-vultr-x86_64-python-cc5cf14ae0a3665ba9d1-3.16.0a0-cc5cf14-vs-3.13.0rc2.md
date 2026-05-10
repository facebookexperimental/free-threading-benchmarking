# Results vs. 3.13.0rc2

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: linux-x86_64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.113x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.62 sec                                                     | 2.51 sec: 1.04x faster                                                |
| html5lib       | 67.0 ms                                                      | 65.9 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 461 ms                                                       | 354 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 520 ms: 1.28x faster                                                  |
| async_tree_none            | 354 ms                                                       | 278 ms: 1.27x faster                                                  |
| async_tree_io              | 876 ms                                                       | 689 ms: 1.27x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 728 ms: 1.25x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 343 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 533 ms: 1.20x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 288 ms: 1.17x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 441 ms: 1.15x faster                                                  |
| async_generators           | 377 ms                                                       | 354 ms: 1.06x faster                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.45 sec: 1.04x faster                                                |
| coroutines                 | 23.6 ms                                                      | 24.6 ms: 1.04x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.16x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 57.2 ms: 1.35x faster                                                 |
| nbody          | 85.1 ms                                                      | 64.3 ms: 1.32x faster                                                 |
| pidigits       | 217 ms                                                       | 184 ms: 1.17x faster                                                  |
| Geometric mean | (ref)                                                        | 1.28x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                 |
| regex_compile  | 132 ms                                                       | 125 ms: 1.06x faster                                                  |
| regex_effbot   | 3.08 ms                                                      | 2.93 ms: 1.05x faster                                                 |
| regex_dna      | 180 ms                                                       | 183 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.25 ms: 1.14x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.80 sec: 1.11x faster                                                |
| unpickle_pure_python | 210 us                                                       | 189 us: 1.11x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 87.3 ms: 1.09x faster                                                 |
| pickle_pure_python   | 294 us                                                       | 279 us: 1.05x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 57.1 ms: 1.04x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.5 ms: 1.02x faster                                                 |
| json_loads           | 27.0 us                                                      | 27.4 us: 1.02x slower                                                 |
| pickle_list          | 4.93 us                                                      | 5.03 us: 1.02x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| unpickle             | 14.3 us                                                      | 15.1 us: 1.05x slower                                                 |
| pickle_dict          | 32.5 us                                                      | 34.3 us: 1.05x slower                                                 |
| unpickle_list        | 4.71 us                                                      | 5.22 us: 1.11x slower                                                 |
| pickle               | 11.3 us                                                      | 12.9 us: 1.14x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                 |
| django_template | 34.1 ms                                                      | 41.3 ms: 1.21x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 115 ms: 2.76x faster                                                  |
| richards_super             | 51.6 ms                                                      | 21.4 ms: 2.41x faster                                                 |
| richards                   | 45.2 ms                                                      | 19.0 ms: 2.38x faster                                                 |
| mdp                        | 2.36 sec                                                     | 1.24 sec: 1.90x faster                                                |
| scimark_sor                | 134 ms                                                       | 78.9 ms: 1.70x faster                                                 |
| deepcopy_memo              | 39.1 us                                                      | 23.2 us: 1.69x faster                                                 |
| spectral_norm              | 111 ms                                                       | 71.0 ms: 1.56x faster                                                 |
| deepcopy                   | 355 us                                                       | 244 us: 1.45x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 81.5 ms: 1.38x faster                                                 |
| go                         | 141 ms                                                       | 102 ms: 1.38x faster                                                  |
| float                      | 77.5 ms                                                      | 57.2 ms: 1.35x faster                                                 |
| scimark_fft                | 349 ms                                                       | 261 ms: 1.34x faster                                                  |
| nbody                      | 85.1 ms                                                      | 64.3 ms: 1.32x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 354 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 520 ms: 1.28x faster                                                  |
| pyflate                    | 449 ms                                                       | 352 ms: 1.27x faster                                                  |
| async_tree_none            | 354 ms                                                       | 278 ms: 1.27x faster                                                  |
| async_tree_io              | 876 ms                                                       | 689 ms: 1.27x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 728 ms: 1.25x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 52.2 ms: 1.25x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 343 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 533 ms: 1.20x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 65.7 ms: 1.20x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.63 us: 1.18x faster                                                 |
| pidigits                   | 217 ms                                                       | 184 ms: 1.17x faster                                                  |
| chaos                      | 57.3 ms                                                      | 49.0 ms: 1.17x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 288 ms: 1.17x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 633 ms: 1.17x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.06 ms: 1.16x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.29 sec: 1.16x faster                                                |
| deltablue                  | 3.12 ms                                                      | 2.72 ms: 1.15x faster                                                 |
| asyncio_tcp                | 505 ms                                                       | 441 ms: 1.15x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.25 ms: 1.14x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.42 us: 1.14x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 3.97 sec: 1.12x faster                                                |
| pathlib                    | 19.2 ms                                                      | 17.1 ms: 1.12x faster                                                 |
| fannkuch                   | 370 ms                                                       | 331 ms: 1.12x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.80 sec: 1.11x faster                                                |
| unpickle_pure_python       | 210 us                                                       | 189 us: 1.11x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.22 us: 1.10x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.0 us: 1.10x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.3 ms: 1.09x faster                                                 |
| mako                       | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                 |
| async_generators           | 377 ms                                                       | 354 ms: 1.06x faster                                                  |
| meteor_contest             | 102 ms                                                       | 95.7 ms: 1.06x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.4 ms: 1.06x faster                                                 |
| regex_compile              | 132 ms                                                       | 125 ms: 1.06x faster                                                  |
| pickle_pure_python         | 294 us                                                       | 279 us: 1.05x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.69 ms: 1.05x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.93 ms: 1.05x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 71.3 ms: 1.05x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.45 sec: 1.04x faster                                                |
| docutils                   | 2.62 sec                                                     | 2.51 sec: 1.04x faster                                                |
| sqlite_synth               | 2.21 us                                                      | 2.12 us: 1.04x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 57.1 ms: 1.04x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 65.4 ms: 1.04x faster                                                 |
| logging_silent             | 103 ns                                                       | 100 ns: 1.02x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 83.5 ms: 1.02x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 152 us: 1.02x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 65.9 ms: 1.02x faster                                                 |
| coverage                   | 83.0 ms                                                      | 82.7 ms: 1.00x faster                                                 |
| raytrace                   | 253 ms                                                       | 255 ms: 1.01x slower                                                  |
| generators                 | 28.8 ms                                                      | 29.2 ms: 1.01x slower                                                 |
| sympy_expand               | 457 ms                                                       | 464 ms: 1.01x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.4 us: 1.02x slower                                                 |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.02x slower                                                  |
| pickle_list                | 4.93 us                                                      | 5.03 us: 1.02x slower                                                 |
| thrift                     | 778 us                                                       | 809 us: 1.04x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.6 ms: 1.04x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| sympy_str                  | 275 ms                                                       | 289 ms: 1.05x slower                                                  |
| unpickle                   | 14.3 us                                                      | 15.1 us: 1.05x slower                                                 |
| pickle_dict                | 32.5 us                                                      | 34.3 us: 1.05x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 165 ms: 1.06x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.22 sec: 1.09x slower                                                |
| unpickle_list              | 4.71 us                                                      | 5.22 us: 1.11x slower                                                 |
| pickle                     | 11.3 us                                                      | 12.9 us: 1.14x slower                                                 |
| django_template            | 34.1 ms                                                      | 41.3 ms: 1.21x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.87 ms: 1.23x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.36x slower                                                 |
| unpack_sequence            | 44.8 ns                                                      | 64.8 ns: 1.45x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.33 ms: 1.45x slower                                                 |
| telco                      | 7.82 ms                                                      | 137 ms: 17.45x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 203 ms: 18.42x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                          |

Benchmark hidden because not significant (2): json, sympy_integrate
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260509-3.16.0a0-cc5cf14-JIT/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.113x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.21x