# Results vs. base

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: linux-x86_64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.078x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-JIT/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| docutils       | 2.41 sec                                                                                                        | 2.51 sec: 1.04x slower                                                                                              |
| html5lib       | 61.1 ms                                                                                                         | 65.9 ms: 1.08x slower                                                                                               |
| sphinx         | 996 ms                                                                                                          | 1.02 sec: 1.03x slower                                                                                              |
| Geometric mean | (ref)                                                                                                           | 1.05x slower                                                                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-JIT/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| async_tree_memoization     | 379 ms                                                                                                          | 354 ms: 1.07x faster                                                                                                |
| async_tree_none            | 295 ms                                                                                                          | 278 ms: 1.06x faster                                                                                                |
| async_tree_memoization_tg  | 364 ms                                                                                                          | 343 ms: 1.06x faster                                                                                                |
| async_tree_cpu_io_mixed    | 543 ms                                                                                                          | 520 ms: 1.05x faster                                                                                                |
| async_tree_io              | 716 ms                                                                                                          | 689 ms: 1.04x faster                                                                                                |
| async_tree_cpu_io_mixed_tg | 552 ms                                                                                                          | 533 ms: 1.04x faster                                                                                                |
| async_tree_io_tg           | 754 ms                                                                                                          | 728 ms: 1.04x faster                                                                                                |
| async_tree_none_tg         | 297 ms                                                                                                          | 288 ms: 1.03x faster                                                                                                |
| asyncio_tcp                | 450 ms                                                                                                          | 441 ms: 1.02x faster                                                                                                |
| coroutines                 | 24.9 ms                                                                                                         | 24.6 ms: 1.01x faster                                                                                               |
| asyncio_tcp_ssl            | 1.46 sec                                                                                                        | 1.45 sec: 1.01x faster                                                                                              |
| async_generators           | 341 ms                                                                                                          | 354 ms: 1.04x slower                                                                                                |
| Geometric mean             | (ref)                                                                                                           | 1.03x faster                                                                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-JIT/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| nbody          | 90.1 ms                                                                                                         | 64.3 ms: 1.40x faster                                                                                               |
| float          | 75.2 ms                                                                                                         | 57.2 ms: 1.31x faster                                                                                               |
| pidigits       | 184 ms                                                                                                          | 184 ms: 1.00x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.22x faster                                                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-JIT/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.7 ms                                                                                                         | 21.4 ms: 1.02x faster                                                                                               |
| regex_dna      | 184 ms                                                                                                          | 183 ms: 1.01x faster                                                                                                |
| regex_effbot   | 2.95 ms                                                                                                         | 2.93 ms: 1.00x faster                                                                                               |
| Geometric mean | (ref)                                                                                                           | 1.01x faster                                                                                                        |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-JIT/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| unpickle_pure_python | 216 us                                                                                                          | 189 us: 1.14x faster                                                                                                |
| pickle_pure_python   | 319 us                                                                                                          | 279 us: 1.14x faster                                                                                                |
| xml_etree_process    | 61.2 ms                                                                                                         | 57.1 ms: 1.07x faster                                                                                               |
| json_dumps           | 9.75 ms                                                                                                         | 9.25 ms: 1.05x faster                                                                                               |
| xml_etree_iterparse  | 90.9 ms                                                                                                         | 87.3 ms: 1.04x faster                                                                                               |
| xml_etree_generate   | 86.9 ms                                                                                                         | 83.5 ms: 1.04x faster                                                                                               |
| pickle_list          | 5.18 us                                                                                                         | 5.03 us: 1.03x faster                                                                                               |
| tomli_loads          | 1.84 sec                                                                                                        | 1.80 sec: 1.02x faster                                                                                              |
| pickle               | 13.1 us                                                                                                         | 12.9 us: 1.01x faster                                                                                               |
| unpickle_list        | 5.06 us                                                                                                         | 5.22 us: 1.03x slower                                                                                               |
| Geometric mean       | (ref)                                                                                                           | 1.04x faster                                                                                                        |

Benchmark hidden because not significant (4): unpickle, pickle_dict, json_loads, xml_etree_parse

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-JIT/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| mako            | 12.0 ms                                                                                                         | 10.5 ms: 1.15x faster                                                                                               |
| django_template | 36.2 ms                                                                                                         | 41.3 ms: 1.14x slower                                                                                               |
| Geometric mean  | (ref)                                                                                                           | 1.00x faster                                                                                                        |

All benchmarks:
===============

| Benchmark                  | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-JIT/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------:|
| richards_super             | 49.4 ms                                                                                                         | 21.4 ms: 2.31x faster                                                                                               |
| richards                   | 43.7 ms                                                                                                         | 19.0 ms: 2.30x faster                                                                                               |
| bench_mp_pool              | 299 ms                                                                                                          | 203 ms: 1.47x faster                                                                                                |
| nbody                      | 90.1 ms                                                                                                         | 64.3 ms: 1.40x faster                                                                                               |
| scimark_sor                | 110 ms                                                                                                          | 78.9 ms: 1.40x faster                                                                                               |
| scimark_lu                 | 113 ms                                                                                                          | 81.5 ms: 1.38x faster                                                                                               |
| spectral_norm              | 94.6 ms                                                                                                         | 71.0 ms: 1.33x faster                                                                                               |
| float                      | 75.2 ms                                                                                                         | 57.2 ms: 1.31x faster                                                                                               |
| deltablue                  | 3.39 ms                                                                                                         | 2.72 ms: 1.25x faster                                                                                               |
| scimark_monte_carlo        | 64.8 ms                                                                                                         | 52.2 ms: 1.24x faster                                                                                               |
| scimark_fft                | 316 ms                                                                                                          | 261 ms: 1.21x faster                                                                                                |
| deepcopy_memo              | 27.7 us                                                                                                         | 23.2 us: 1.20x faster                                                                                               |
| telco                      | 162 ms                                                                                                          | 137 ms: 1.19x faster                                                                                                |
| pprint_safe_repr           | 734 ms                                                                                                          | 633 ms: 1.16x faster                                                                                                |
| pprint_pformat             | 1.49 sec                                                                                                        | 1.29 sec: 1.16x faster                                                                                              |
| scimark_sparse_mat_mult    | 4.68 ms                                                                                                         | 4.06 ms: 1.15x faster                                                                                               |
| mako                       | 12.0 ms                                                                                                         | 10.5 ms: 1.15x faster                                                                                               |
| fannkuch                   | 381 ms                                                                                                          | 331 ms: 1.15x faster                                                                                                |
| unpickle_pure_python       | 216 us                                                                                                          | 189 us: 1.14x faster                                                                                                |
| pickle_pure_python         | 319 us                                                                                                          | 279 us: 1.14x faster                                                                                                |
| nqueens                    | 74.9 ms                                                                                                         | 65.7 ms: 1.14x faster                                                                                               |
| chaos                      | 55.6 ms                                                                                                         | 49.0 ms: 1.13x faster                                                                                               |
| pyflate                    | 399 ms                                                                                                          | 352 ms: 1.13x faster                                                                                                |
| gc_traversal               | 4.19 ms                                                                                                         | 3.87 ms: 1.08x faster                                                                                               |
| logging_simple             | 5.84 us                                                                                                         | 5.42 us: 1.08x faster                                                                                               |
| typing_runtime_protocols   | 163 us                                                                                                          | 152 us: 1.07x faster                                                                                                |
| logging_format             | 6.67 us                                                                                                         | 6.22 us: 1.07x faster                                                                                               |
| xml_etree_process          | 61.2 ms                                                                                                         | 57.1 ms: 1.07x faster                                                                                               |
| async_tree_memoization     | 379 ms                                                                                                          | 354 ms: 1.07x faster                                                                                                |
| comprehensions             | 16.0 us                                                                                                         | 15.0 us: 1.07x faster                                                                                               |
| sqlglot_v2_normalize       | 103 ms                                                                                                          | 96.4 ms: 1.07x faster                                                                                               |
| crypto_pyaes               | 69.6 ms                                                                                                         | 65.4 ms: 1.06x faster                                                                                               |
| async_tree_none            | 295 ms                                                                                                          | 278 ms: 1.06x faster                                                                                                |
| async_tree_memoization_tg  | 364 ms                                                                                                          | 343 ms: 1.06x faster                                                                                                |
| go                         | 108 ms                                                                                                          | 102 ms: 1.06x faster                                                                                                |
| shortest_path              | 443 ms                                                                                                          | 420 ms: 1.05x faster                                                                                                |
| json_dumps                 | 9.75 ms                                                                                                         | 9.25 ms: 1.05x faster                                                                                               |
| bpe_tokeniser              | 4.18 sec                                                                                                        | 3.97 sec: 1.05x faster                                                                                              |
| connected_components       | 396 ms                                                                                                          | 377 ms: 1.05x faster                                                                                                |
| meteor_contest             | 100 ms                                                                                                          | 95.7 ms: 1.05x faster                                                                                               |
| async_tree_cpu_io_mixed    | 543 ms                                                                                                          | 520 ms: 1.05x faster                                                                                                |
| xml_etree_iterparse        | 90.9 ms                                                                                                         | 87.3 ms: 1.04x faster                                                                                               |
| xml_etree_generate         | 86.9 ms                                                                                                         | 83.5 ms: 1.04x faster                                                                                               |
| async_tree_io              | 716 ms                                                                                                          | 689 ms: 1.04x faster                                                                                                |
| async_tree_cpu_io_mixed_tg | 552 ms                                                                                                          | 533 ms: 1.04x faster                                                                                                |
| async_tree_io_tg           | 754 ms                                                                                                          | 728 ms: 1.04x faster                                                                                                |
| hexiom                     | 5.89 ms                                                                                                         | 5.69 ms: 1.03x faster                                                                                               |
| sqlglot_v2_parse           | 1.16 ms                                                                                                         | 1.12 ms: 1.03x faster                                                                                               |
| sqlglot_v2_optimize        | 51.4 ms                                                                                                         | 49.8 ms: 1.03x faster                                                                                               |
| sqlite_synth               | 2.19 us                                                                                                         | 2.12 us: 1.03x faster                                                                                               |
| async_tree_none_tg         | 297 ms                                                                                                          | 288 ms: 1.03x faster                                                                                                |
| pickle_list                | 5.18 us                                                                                                         | 5.03 us: 1.03x faster                                                                                               |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                         | 1.43 ms: 1.03x faster                                                                                               |
| subparsers                 | 9.37 ms                                                                                                         | 9.12 ms: 1.03x faster                                                                                               |
| json                       | 5.03 ms                                                                                                         | 4.91 ms: 1.03x faster                                                                                               |
| pathlib                    | 17.6 ms                                                                                                         | 17.1 ms: 1.02x faster                                                                                               |
| tomli_loads                | 1.84 sec                                                                                                        | 1.80 sec: 1.02x faster                                                                                              |
| asyncio_tcp                | 450 ms                                                                                                          | 441 ms: 1.02x faster                                                                                                |
| regex_v8                   | 21.7 ms                                                                                                         | 21.4 ms: 1.02x faster                                                                                               |
| sympy_expand               | 472 ms                                                                                                          | 464 ms: 1.02x faster                                                                                                |
| raytrace                   | 259 ms                                                                                                          | 255 ms: 1.02x faster                                                                                                |
| pickle                     | 13.1 us                                                                                                         | 12.9 us: 1.01x faster                                                                                               |
| coroutines                 | 24.9 ms                                                                                                         | 24.6 ms: 1.01x faster                                                                                               |
| asyncio_tcp_ssl            | 1.46 sec                                                                                                        | 1.45 sec: 1.01x faster                                                                                              |
| regex_dna                  | 184 ms                                                                                                          | 183 ms: 1.01x faster                                                                                                |
| regex_effbot               | 2.95 ms                                                                                                         | 2.93 ms: 1.00x faster                                                                                               |
| pidigits                   | 184 ms                                                                                                          | 184 ms: 1.00x slower                                                                                                |
| pylint                     | 114 ms                                                                                                          | 115 ms: 1.01x slower                                                                                                |
| deepcopy_reduce            | 2.57 us                                                                                                         | 2.63 us: 1.02x slower                                                                                               |
| sphinx                     | 996 ms                                                                                                          | 1.02 sec: 1.03x slower                                                                                              |
| sympy_integrate            | 19.2 ms                                                                                                         | 19.8 ms: 1.03x slower                                                                                               |
| deepcopy                   | 237 us                                                                                                          | 244 us: 1.03x slower                                                                                                |
| unpickle_list              | 5.06 us                                                                                                         | 5.22 us: 1.03x slower                                                                                               |
| thrift                     | 782 us                                                                                                          | 809 us: 1.04x slower                                                                                                |
| pycparser                  | 1.18 sec                                                                                                        | 1.22 sec: 1.04x slower                                                                                              |
| async_generators           | 341 ms                                                                                                          | 354 ms: 1.04x slower                                                                                                |
| dulwich_log                | 68.7 ms                                                                                                         | 71.3 ms: 1.04x slower                                                                                               |
| docutils                   | 2.41 sec                                                                                                        | 2.51 sec: 1.04x slower                                                                                              |
| many_optionals             | 911 us                                                                                                          | 953 us: 1.05x slower                                                                                                |
| sympy_str                  | 276 ms                                                                                                          | 289 ms: 1.05x slower                                                                                                |
| sympy_sum                  | 157 ms                                                                                                          | 165 ms: 1.05x slower                                                                                                |
| generators                 | 27.5 ms                                                                                                         | 29.2 ms: 1.06x slower                                                                                               |
| html5lib                   | 61.1 ms                                                                                                         | 65.9 ms: 1.08x slower                                                                                               |
| mdp                        | 1.14 sec                                                                                                        | 1.24 sec: 1.09x slower                                                                                              |
| k_core                     | 2.09 sec                                                                                                        | 2.32 sec: 1.11x slower                                                                                              |
| django_template            | 36.2 ms                                                                                                         | 41.3 ms: 1.14x slower                                                                                               |
| unpack_sequence            | 43.2 ns                                                                                                         | 64.8 ns: 1.50x slower                                                                                               |
| Geometric mean             | (ref)                                                                                                           | 1.07x faster                                                                                                        |

Benchmark hidden because not significant (10): bench_thread_pool, logging_silent, unpickle, coverage, regex_compile, pickle_dict, json_loads, asyncio_websockets, create_gc_cycles, xml_etree_parse

- Geometric mean (including insignificant results): 1.078x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.05x