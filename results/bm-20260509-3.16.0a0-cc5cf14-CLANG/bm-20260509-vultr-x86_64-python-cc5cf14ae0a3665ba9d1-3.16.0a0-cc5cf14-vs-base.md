# Results vs. base

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: linux-x86_64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.027x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-CLANG/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| docutils       | 2.41 sec                                                                                                        | 2.34 sec: 1.03x faster                                                                                                |
| html5lib       | 61.1 ms                                                                                                         | 58.6 ms: 1.04x faster                                                                                                 |
| sphinx         | 996 ms                                                                                                          | 972 ms: 1.02x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.03x faster                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-CLANG/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_none            | 295 ms                                                                                                          | 283 ms: 1.04x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 543 ms                                                                                                          | 524 ms: 1.04x faster                                                                                                  |
| coroutines                 | 24.9 ms                                                                                                         | 24.1 ms: 1.03x faster                                                                                                 |
| async_tree_memoization     | 379 ms                                                                                                          | 367 ms: 1.03x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 552 ms                                                                                                          | 540 ms: 1.02x faster                                                                                                  |
| async_generators           | 341 ms                                                                                                          | 335 ms: 1.02x faster                                                                                                  |
| asyncio_tcp_ssl            | 1.46 sec                                                                                                        | 1.48 sec: 1.01x slower                                                                                                |
| Geometric mean             | (ref)                                                                                                           | 1.01x faster                                                                                                          |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_none_tg, async_tree_io, asyncio_websockets, asyncio_tcp, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-CLANG/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| nbody          | 90.1 ms                                                                                                         | 83.6 ms: 1.08x faster                                                                                                 |
| float          | 75.2 ms                                                                                                         | 73.9 ms: 1.02x faster                                                                                                 |
| pidigits       | 184 ms                                                                                                          | 191 ms: 1.04x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.02x faster                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-CLANG/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 125 ms                                                                                                          | 122 ms: 1.03x faster                                                                                                  |
| regex_v8       | 21.7 ms                                                                                                         | 22.2 ms: 1.02x slower                                                                                                 |
| regex_dna      | 184 ms                                                                                                          | 193 ms: 1.04x slower                                                                                                  |
| regex_effbot   | 2.95 ms                                                                                                         | 3.11 ms: 1.06x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.02x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-CLANG/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| unpickle_list        | 5.06 us                                                                                                         | 4.67 us: 1.08x faster                                                                                                 |
| pickle_dict          | 34.3 us                                                                                                         | 31.9 us: 1.07x faster                                                                                                 |
| xml_etree_process    | 61.2 ms                                                                                                         | 57.6 ms: 1.06x faster                                                                                                 |
| pickle_list          | 5.18 us                                                                                                         | 4.88 us: 1.06x faster                                                                                                 |
| json_dumps           | 9.75 ms                                                                                                         | 9.36 ms: 1.04x faster                                                                                                 |
| xml_etree_generate   | 86.9 ms                                                                                                         | 83.7 ms: 1.04x faster                                                                                                 |
| json_loads           | 27.4 us                                                                                                         | 26.6 us: 1.03x faster                                                                                                 |
| pickle_pure_python   | 319 us                                                                                                          | 312 us: 1.02x faster                                                                                                  |
| unpickle_pure_python | 216 us                                                                                                          | 213 us: 1.01x faster                                                                                                  |
| tomli_loads          | 1.84 sec                                                                                                        | 1.83 sec: 1.00x faster                                                                                                |
| pickle               | 13.1 us                                                                                                         | 13.2 us: 1.01x slower                                                                                                 |
| unpickle             | 15.2 us                                                                                                         | 15.5 us: 1.02x slower                                                                                                 |
| xml_etree_iterparse  | 90.9 ms                                                                                                         | 93.7 ms: 1.03x slower                                                                                                 |
| xml_etree_parse      | 142 ms                                                                                                          | 160 ms: 1.12x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                           | 1.02x faster                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-CLANG/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.2 ms                                                                                                         | 33.3 ms: 1.09x faster                                                                                                 |
| mako            | 12.0 ms                                                                                                         | 12.9 ms: 1.07x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.01x faster                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-CLANG/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| logging_silent             | 101 ns                                                                                                          | 83.0 ns: 1.22x faster                                                                                                 |
| deltablue                  | 3.39 ms                                                                                                         | 3.00 ms: 1.13x faster                                                                                                 |
| typing_runtime_protocols   | 163 us                                                                                                          | 146 us: 1.12x faster                                                                                                  |
| richards                   | 43.7 ms                                                                                                         | 39.3 ms: 1.11x faster                                                                                                 |
| richards_super             | 49.4 ms                                                                                                         | 44.8 ms: 1.10x faster                                                                                                 |
| spectral_norm              | 94.6 ms                                                                                                         | 86.0 ms: 1.10x faster                                                                                                 |
| scimark_sparse_mat_mult    | 4.68 ms                                                                                                         | 4.28 ms: 1.09x faster                                                                                                 |
| comprehensions             | 16.0 us                                                                                                         | 14.7 us: 1.09x faster                                                                                                 |
| scimark_monte_carlo        | 64.8 ms                                                                                                         | 59.4 ms: 1.09x faster                                                                                                 |
| scimark_fft                | 316 ms                                                                                                          | 291 ms: 1.09x faster                                                                                                  |
| django_template            | 36.2 ms                                                                                                         | 33.3 ms: 1.09x faster                                                                                                 |
| unpickle_list              | 5.06 us                                                                                                         | 4.67 us: 1.08x faster                                                                                                 |
| nbody                      | 90.1 ms                                                                                                         | 83.6 ms: 1.08x faster                                                                                                 |
| pickle_dict                | 34.3 us                                                                                                         | 31.9 us: 1.07x faster                                                                                                 |
| logging_format             | 6.67 us                                                                                                         | 6.23 us: 1.07x faster                                                                                                 |
| pycparser                  | 1.18 sec                                                                                                        | 1.10 sec: 1.07x faster                                                                                                |
| deepcopy                   | 237 us                                                                                                          | 222 us: 1.07x faster                                                                                                  |
| chaos                      | 55.6 ms                                                                                                         | 52.3 ms: 1.06x faster                                                                                                 |
| xml_etree_process          | 61.2 ms                                                                                                         | 57.6 ms: 1.06x faster                                                                                                 |
| pickle_list                | 5.18 us                                                                                                         | 4.88 us: 1.06x faster                                                                                                 |
| sympy_expand               | 472 ms                                                                                                          | 444 ms: 1.06x faster                                                                                                  |
| deepcopy_reduce            | 2.57 us                                                                                                         | 2.42 us: 1.06x faster                                                                                                 |
| deepcopy_memo              | 27.7 us                                                                                                         | 26.2 us: 1.06x faster                                                                                                 |
| gc_traversal               | 4.19 ms                                                                                                         | 3.97 ms: 1.05x faster                                                                                                 |
| raytrace                   | 259 ms                                                                                                          | 245 ms: 1.05x faster                                                                                                  |
| logging_simple             | 5.84 us                                                                                                         | 5.54 us: 1.05x faster                                                                                                 |
| scimark_lu                 | 113 ms                                                                                                          | 107 ms: 1.05x faster                                                                                                  |
| sympy_integrate            | 19.2 ms                                                                                                         | 18.3 ms: 1.05x faster                                                                                                 |
| sympy_sum                  | 157 ms                                                                                                          | 149 ms: 1.05x faster                                                                                                  |
| sqlglot_v2_optimize        | 51.4 ms                                                                                                         | 49.0 ms: 1.05x faster                                                                                                 |
| sqlglot_v2_normalize       | 103 ms                                                                                                          | 98.1 ms: 1.05x faster                                                                                                 |
| sympy_str                  | 276 ms                                                                                                          | 264 ms: 1.05x faster                                                                                                  |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                         | 1.41 ms: 1.04x faster                                                                                                 |
| go                         | 108 ms                                                                                                          | 104 ms: 1.04x faster                                                                                                  |
| async_tree_none            | 295 ms                                                                                                          | 283 ms: 1.04x faster                                                                                                  |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.29 ms: 1.04x faster                                                                                                 |
| html5lib                   | 61.1 ms                                                                                                         | 58.6 ms: 1.04x faster                                                                                                 |
| json_dumps                 | 9.75 ms                                                                                                         | 9.36 ms: 1.04x faster                                                                                                 |
| coverage                   | 82.8 ms                                                                                                         | 79.6 ms: 1.04x faster                                                                                                 |
| mdp                        | 1.14 sec                                                                                                        | 1.10 sec: 1.04x faster                                                                                                |
| xml_etree_generate         | 86.9 ms                                                                                                         | 83.7 ms: 1.04x faster                                                                                                 |
| sqlglot_v2_parse           | 1.16 ms                                                                                                         | 1.12 ms: 1.04x faster                                                                                                 |
| scimark_sor                | 110 ms                                                                                                          | 106 ms: 1.04x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 543 ms                                                                                                          | 524 ms: 1.04x faster                                                                                                  |
| thrift                     | 782 us                                                                                                          | 754 us: 1.04x faster                                                                                                  |
| telco                      | 162 ms                                                                                                          | 157 ms: 1.04x faster                                                                                                  |
| nqueens                    | 74.9 ms                                                                                                         | 72.3 ms: 1.04x faster                                                                                                 |
| coroutines                 | 24.9 ms                                                                                                         | 24.1 ms: 1.03x faster                                                                                                 |
| json_loads                 | 27.4 us                                                                                                         | 26.6 us: 1.03x faster                                                                                                 |
| async_tree_memoization     | 379 ms                                                                                                          | 367 ms: 1.03x faster                                                                                                  |
| docutils                   | 2.41 sec                                                                                                        | 2.34 sec: 1.03x faster                                                                                                |
| regex_compile              | 125 ms                                                                                                          | 122 ms: 1.03x faster                                                                                                  |
| hexiom                     | 5.89 ms                                                                                                         | 5.74 ms: 1.03x faster                                                                                                 |
| sphinx                     | 996 ms                                                                                                          | 972 ms: 1.02x faster                                                                                                  |
| pickle_pure_python         | 319 us                                                                                                          | 312 us: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 552 ms                                                                                                          | 540 ms: 1.02x faster                                                                                                  |
| fannkuch                   | 381 ms                                                                                                          | 372 ms: 1.02x faster                                                                                                  |
| shortest_path              | 443 ms                                                                                                          | 435 ms: 1.02x faster                                                                                                  |
| async_generators           | 341 ms                                                                                                          | 335 ms: 1.02x faster                                                                                                  |
| subparsers                 | 9.37 ms                                                                                                         | 9.21 ms: 1.02x faster                                                                                                 |
| float                      | 75.2 ms                                                                                                         | 73.9 ms: 1.02x faster                                                                                                 |
| unpickle_pure_python       | 216 us                                                                                                          | 213 us: 1.01x faster                                                                                                  |
| bpe_tokeniser              | 4.18 sec                                                                                                        | 4.13 sec: 1.01x faster                                                                                                |
| pprint_pformat             | 1.49 sec                                                                                                        | 1.48 sec: 1.01x faster                                                                                                |
| pathlib                    | 17.6 ms                                                                                                         | 17.4 ms: 1.01x faster                                                                                                 |
| dulwich_log                | 68.7 ms                                                                                                         | 68.1 ms: 1.01x faster                                                                                                 |
| pprint_safe_repr           | 734 ms                                                                                                          | 729 ms: 1.01x faster                                                                                                  |
| tomli_loads                | 1.84 sec                                                                                                        | 1.83 sec: 1.00x faster                                                                                                |
| connected_components       | 396 ms                                                                                                          | 398 ms: 1.00x slower                                                                                                  |
| asyncio_tcp_ssl            | 1.46 sec                                                                                                        | 1.48 sec: 1.01x slower                                                                                                |
| pickle                     | 13.1 us                                                                                                         | 13.2 us: 1.01x slower                                                                                                 |
| crypto_pyaes               | 69.6 ms                                                                                                         | 70.9 ms: 1.02x slower                                                                                                 |
| regex_v8                   | 21.7 ms                                                                                                         | 22.2 ms: 1.02x slower                                                                                                 |
| pyflate                    | 399 ms                                                                                                          | 407 ms: 1.02x slower                                                                                                  |
| unpickle                   | 15.2 us                                                                                                         | 15.5 us: 1.02x slower                                                                                                 |
| xml_etree_iterparse        | 90.9 ms                                                                                                         | 93.7 ms: 1.03x slower                                                                                                 |
| pidigits                   | 184 ms                                                                                                          | 191 ms: 1.04x slower                                                                                                  |
| regex_dna                  | 184 ms                                                                                                          | 193 ms: 1.04x slower                                                                                                  |
| generators                 | 27.5 ms                                                                                                         | 28.8 ms: 1.04x slower                                                                                                 |
| regex_effbot               | 2.95 ms                                                                                                         | 3.11 ms: 1.06x slower                                                                                                 |
| create_gc_cycles           | 1.82 ms                                                                                                         | 1.95 ms: 1.07x slower                                                                                                 |
| meteor_contest             | 100 ms                                                                                                          | 107 ms: 1.07x slower                                                                                                  |
| mako                       | 12.0 ms                                                                                                         | 12.9 ms: 1.07x slower                                                                                                 |
| xml_etree_parse            | 142 ms                                                                                                          | 160 ms: 1.12x slower                                                                                                  |
| unpack_sequence            | 43.2 ns                                                                                                         | 52.5 ns: 1.22x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (12): async_tree_memoization_tg, async_tree_none_tg, sqlite_synth, pylint, many_optionals, json, async_tree_io, asyncio_websockets, asyncio_tcp, k_core, async_tree_io_tg, bench_mp_pool

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.02x