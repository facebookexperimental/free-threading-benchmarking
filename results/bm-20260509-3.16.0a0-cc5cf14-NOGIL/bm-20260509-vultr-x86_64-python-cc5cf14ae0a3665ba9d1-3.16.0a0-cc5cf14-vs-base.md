# Results vs. base

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: linux-x86_64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.099x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-NOGIL/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| docutils       | 2.41 sec                                                                                                        | 2.96 sec: 1.23x slower                                                                                                |
| html5lib       | 61.1 ms                                                                                                         | 70.0 ms: 1.15x slower                                                                                                 |
| sphinx         | 996 ms                                                                                                          | 1.11 sec: 1.12x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-NOGIL/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 754 ms                                                                                                          | 691 ms: 1.09x faster                                                                                                  |
| asyncio_websockets         | 543 ms                                                                                                          | 509 ms: 1.07x faster                                                                                                  |
| async_tree_io              | 716 ms                                                                                                          | 709 ms: 1.01x faster                                                                                                  |
| coroutines                 | 24.9 ms                                                                                                         | 25.0 ms: 1.01x slower                                                                                                 |
| asyncio_tcp                | 450 ms                                                                                                          | 463 ms: 1.03x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 552 ms                                                                                                          | 573 ms: 1.04x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 543 ms                                                                                                          | 584 ms: 1.08x slower                                                                                                  |
| async_tree_memoization_tg  | 364 ms                                                                                                          | 393 ms: 1.08x slower                                                                                                  |
| async_tree_none_tg         | 297 ms                                                                                                          | 325 ms: 1.09x slower                                                                                                  |
| async_tree_memoization     | 379 ms                                                                                                          | 419 ms: 1.11x slower                                                                                                  |
| async_generators           | 341 ms                                                                                                          | 387 ms: 1.13x slower                                                                                                  |
| async_tree_none            | 295 ms                                                                                                          | 340 ms: 1.15x slower                                                                                                  |
| asyncio_tcp_ssl            | 1.46 sec                                                                                                        | 1.68 sec: 1.15x slower                                                                                                |
| Geometric mean             | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-NOGIL/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                                                          | 194 ms: 1.06x slower                                                                                                  |
| float          | 75.2 ms                                                                                                         | 88.6 ms: 1.18x slower                                                                                                 |
| nbody          | 90.1 ms                                                                                                         | 124 ms: 1.37x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.20x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-NOGIL/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.7 ms                                                                                                         | 20.2 ms: 1.08x faster                                                                                                 |
| regex_dna      | 184 ms                                                                                                          | 172 ms: 1.07x faster                                                                                                  |
| regex_compile  | 125 ms                                                                                                          | 145 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.00x slower                                                                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-NOGIL/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pickle_list          | 5.18 us                                                                                                         | 4.84 us: 1.07x faster                                                                                                 |
| pickle_dict          | 34.3 us                                                                                                         | 32.4 us: 1.06x faster                                                                                                 |
| pickle               | 13.1 us                                                                                                         | 12.6 us: 1.04x faster                                                                                                 |
| xml_etree_parse      | 142 ms                                                                                                          | 140 ms: 1.01x faster                                                                                                  |
| xml_etree_iterparse  | 90.9 ms                                                                                                         | 95.4 ms: 1.05x slower                                                                                                 |
| tomli_loads          | 1.84 sec                                                                                                        | 1.97 sec: 1.07x slower                                                                                                |
| pickle_pure_python   | 319 us                                                                                                          | 347 us: 1.09x slower                                                                                                  |
| unpickle             | 15.2 us                                                                                                         | 17.0 us: 1.12x slower                                                                                                 |
| json_dumps           | 9.75 ms                                                                                                         | 10.9 ms: 1.12x slower                                                                                                 |
| json_loads           | 27.4 us                                                                                                         | 30.8 us: 1.12x slower                                                                                                 |
| unpickle_pure_python | 216 us                                                                                                          | 247 us: 1.14x slower                                                                                                  |
| xml_etree_generate   | 86.9 ms                                                                                                         | 101 ms: 1.16x slower                                                                                                  |
| unpickle_list        | 5.06 us                                                                                                         | 5.89 us: 1.16x slower                                                                                                 |
| xml_etree_process    | 61.2 ms                                                                                                         | 74.9 ms: 1.22x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-NOGIL/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.2 ms                                                                                                         | 39.6 ms: 1.09x slower                                                                                                 |
| mako            | 12.0 ms                                                                                                         | 15.9 ms: 1.32x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.20x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json | results/bm-20260509-3.16.0a0-cc5cf14-NOGIL/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 299 ms                                                                                                          | 13.9 ms: 21.50x faster                                                                                                |
| gc_traversal               | 4.19 ms                                                                                                         | 1.89 ms: 2.22x faster                                                                                                 |
| create_gc_cycles           | 1.82 ms                                                                                                         | 1.49 ms: 1.23x faster                                                                                                 |
| sqlite_synth               | 2.19 us                                                                                                         | 1.96 us: 1.12x faster                                                                                                 |
| async_tree_io_tg           | 754 ms                                                                                                          | 691 ms: 1.09x faster                                                                                                  |
| regex_v8                   | 21.7 ms                                                                                                         | 20.2 ms: 1.08x faster                                                                                                 |
| regex_dna                  | 184 ms                                                                                                          | 172 ms: 1.07x faster                                                                                                  |
| pickle_list                | 5.18 us                                                                                                         | 4.84 us: 1.07x faster                                                                                                 |
| asyncio_websockets         | 543 ms                                                                                                          | 509 ms: 1.07x faster                                                                                                  |
| pickle_dict                | 34.3 us                                                                                                         | 32.4 us: 1.06x faster                                                                                                 |
| pickle                     | 13.1 us                                                                                                         | 12.6 us: 1.04x faster                                                                                                 |
| xml_etree_parse            | 142 ms                                                                                                          | 140 ms: 1.01x faster                                                                                                  |
| async_tree_io              | 716 ms                                                                                                          | 709 ms: 1.01x faster                                                                                                  |
| pycparser                  | 1.18 sec                                                                                                        | 1.18 sec: 1.00x slower                                                                                                |
| coroutines                 | 24.9 ms                                                                                                         | 25.0 ms: 1.01x slower                                                                                                 |
| asyncio_tcp                | 450 ms                                                                                                          | 463 ms: 1.03x slower                                                                                                  |
| dulwich_log                | 68.7 ms                                                                                                         | 71.1 ms: 1.04x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 552 ms                                                                                                          | 573 ms: 1.04x slower                                                                                                  |
| pathlib                    | 17.6 ms                                                                                                         | 18.3 ms: 1.04x slower                                                                                                 |
| xml_etree_iterparse        | 90.9 ms                                                                                                         | 95.4 ms: 1.05x slower                                                                                                 |
| bpe_tokeniser              | 4.18 sec                                                                                                        | 4.40 sec: 1.05x slower                                                                                                |
| pidigits                   | 184 ms                                                                                                          | 194 ms: 1.06x slower                                                                                                  |
| json                       | 5.03 ms                                                                                                         | 5.36 ms: 1.06x slower                                                                                                 |
| logging_silent             | 101 ns                                                                                                          | 108 ns: 1.07x slower                                                                                                  |
| tomli_loads                | 1.84 sec                                                                                                        | 1.97 sec: 1.07x slower                                                                                                |
| async_tree_cpu_io_mixed    | 543 ms                                                                                                          | 584 ms: 1.08x slower                                                                                                  |
| async_tree_memoization_tg  | 364 ms                                                                                                          | 393 ms: 1.08x slower                                                                                                  |
| k_core                     | 2.09 sec                                                                                                        | 2.26 sec: 1.08x slower                                                                                                |
| pickle_pure_python         | 319 us                                                                                                          | 347 us: 1.09x slower                                                                                                  |
| telco                      | 162 ms                                                                                                          | 177 ms: 1.09x slower                                                                                                  |
| async_tree_none_tg         | 297 ms                                                                                                          | 325 ms: 1.09x slower                                                                                                  |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.47 ms: 1.09x slower                                                                                                 |
| comprehensions             | 16.0 us                                                                                                         | 17.5 us: 1.09x slower                                                                                                 |
| django_template            | 36.2 ms                                                                                                         | 39.6 ms: 1.09x slower                                                                                                 |
| scimark_fft                | 316 ms                                                                                                          | 347 ms: 1.10x slower                                                                                                  |
| async_tree_memoization     | 379 ms                                                                                                          | 419 ms: 1.11x slower                                                                                                  |
| many_optionals             | 911 us                                                                                                          | 1.01 ms: 1.11x slower                                                                                                 |
| deltablue                  | 3.39 ms                                                                                                         | 3.77 ms: 1.11x slower                                                                                                 |
| hexiom                     | 5.89 ms                                                                                                         | 6.55 ms: 1.11x slower                                                                                                 |
| pprint_safe_repr           | 734 ms                                                                                                          | 818 ms: 1.11x slower                                                                                                  |
| unpickle                   | 15.2 us                                                                                                         | 17.0 us: 1.12x slower                                                                                                 |
| sphinx                     | 996 ms                                                                                                          | 1.11 sec: 1.12x slower                                                                                                |
| scimark_sor                | 110 ms                                                                                                          | 123 ms: 1.12x slower                                                                                                  |
| sqlglot_v2_normalize       | 103 ms                                                                                                          | 115 ms: 1.12x slower                                                                                                  |
| json_dumps                 | 9.75 ms                                                                                                         | 10.9 ms: 1.12x slower                                                                                                 |
| json_loads                 | 27.4 us                                                                                                         | 30.8 us: 1.12x slower                                                                                                 |
| sqlglot_v2_optimize        | 51.4 ms                                                                                                         | 57.8 ms: 1.12x slower                                                                                                 |
| subparsers                 | 9.37 ms                                                                                                         | 10.6 ms: 1.13x slower                                                                                                 |
| chaos                      | 55.6 ms                                                                                                         | 62.9 ms: 1.13x slower                                                                                                 |
| deepcopy_memo              | 27.7 us                                                                                                         | 31.4 us: 1.13x slower                                                                                                 |
| async_generators           | 341 ms                                                                                                          | 387 ms: 1.13x slower                                                                                                  |
| go                         | 108 ms                                                                                                          | 123 ms: 1.14x slower                                                                                                  |
| sympy_expand               | 472 ms                                                                                                          | 536 ms: 1.14x slower                                                                                                  |
| pprint_pformat             | 1.49 sec                                                                                                        | 1.70 sec: 1.14x slower                                                                                                |
| sympy_str                  | 276 ms                                                                                                          | 316 ms: 1.14x slower                                                                                                  |
| unpickle_pure_python       | 216 us                                                                                                          | 247 us: 1.14x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.68 ms                                                                                                         | 5.36 ms: 1.15x slower                                                                                                 |
| html5lib                   | 61.1 ms                                                                                                         | 70.0 ms: 1.15x slower                                                                                                 |
| deepcopy                   | 237 us                                                                                                          | 272 us: 1.15x slower                                                                                                  |
| async_tree_none            | 295 ms                                                                                                          | 340 ms: 1.15x slower                                                                                                  |
| sympy_integrate            | 19.2 ms                                                                                                         | 22.2 ms: 1.15x slower                                                                                                 |
| asyncio_tcp_ssl            | 1.46 sec                                                                                                        | 1.68 sec: 1.15x slower                                                                                                |
| scimark_lu                 | 113 ms                                                                                                          | 130 ms: 1.15x slower                                                                                                  |
| sympy_sum                  | 157 ms                                                                                                          | 181 ms: 1.16x slower                                                                                                  |
| regex_compile              | 125 ms                                                                                                          | 145 ms: 1.16x slower                                                                                                  |
| spectral_norm              | 94.6 ms                                                                                                         | 109 ms: 1.16x slower                                                                                                  |
| pylint                     | 114 ms                                                                                                          | 132 ms: 1.16x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.33 sec: 1.16x slower                                                                                                |
| xml_etree_generate         | 86.9 ms                                                                                                         | 101 ms: 1.16x slower                                                                                                  |
| generators                 | 27.5 ms                                                                                                         | 32.1 ms: 1.16x slower                                                                                                 |
| unpickle_list              | 5.06 us                                                                                                         | 5.89 us: 1.16x slower                                                                                                 |
| pyflate                    | 399 ms                                                                                                          | 466 ms: 1.17x slower                                                                                                  |
| deepcopy_reduce            | 2.57 us                                                                                                         | 3.01 us: 1.17x slower                                                                                                 |
| float                      | 75.2 ms                                                                                                         | 88.6 ms: 1.18x slower                                                                                                 |
| nqueens                    | 74.9 ms                                                                                                         | 88.3 ms: 1.18x slower                                                                                                 |
| raytrace                   | 259 ms                                                                                                          | 306 ms: 1.18x slower                                                                                                  |
| logging_format             | 6.67 us                                                                                                         | 7.92 us: 1.19x slower                                                                                                 |
| unpack_sequence            | 43.2 ns                                                                                                         | 51.5 ns: 1.19x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                         | 1.76 ms: 1.20x slower                                                                                                 |
| richards                   | 43.7 ms                                                                                                         | 52.4 ms: 1.20x slower                                                                                                 |
| thrift                     | 782 us                                                                                                          | 939 us: 1.20x slower                                                                                                  |
| richards_super             | 49.4 ms                                                                                                         | 59.6 ms: 1.21x slower                                                                                                 |
| logging_simple             | 5.84 us                                                                                                         | 7.07 us: 1.21x slower                                                                                                 |
| shortest_path              | 443 ms                                                                                                          | 540 ms: 1.22x slower                                                                                                  |
| sqlglot_v2_parse           | 1.16 ms                                                                                                         | 1.42 ms: 1.22x slower                                                                                                 |
| xml_etree_process          | 61.2 ms                                                                                                         | 74.9 ms: 1.22x slower                                                                                                 |
| scimark_monte_carlo        | 64.8 ms                                                                                                         | 79.5 ms: 1.23x slower                                                                                                 |
| docutils                   | 2.41 sec                                                                                                        | 2.96 sec: 1.23x slower                                                                                                |
| fannkuch                   | 381 ms                                                                                                          | 469 ms: 1.23x slower                                                                                                  |
| typing_runtime_protocols   | 163 us                                                                                                          | 201 us: 1.23x slower                                                                                                  |
| connected_components       | 396 ms                                                                                                          | 495 ms: 1.25x slower                                                                                                  |
| meteor_contest             | 100 ms                                                                                                          | 129 ms: 1.28x slower                                                                                                  |
| crypto_pyaes               | 69.6 ms                                                                                                         | 89.8 ms: 1.29x slower                                                                                                 |
| mako                       | 12.0 ms                                                                                                         | 15.9 ms: 1.32x slower                                                                                                 |
| nbody                      | 90.1 ms                                                                                                         | 124 ms: 1.37x slower                                                                                                  |
| coverage                   | 82.8 ms                                                                                                         | 115 ms: 1.39x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmark hidden because not significant (1): regex_effbot

- Geometric mean (including insignificant results): 1.099x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.18x