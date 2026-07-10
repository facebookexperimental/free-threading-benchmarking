# Results vs. base

- fork: python
- ref: b2d8db1ac818e74ffe66
- machine: linux-x86_64
- commit hash: b2d8db1
- commit date: 2026-07-09
- overall geometric mean: 1.105x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260709-3.16.0a0-b2d8db1/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json | results/bm-20260709-3.16.0a0-b2d8db1-NOGIL/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                                                          | 296 ms: 1.15x slower                                                                                                  |
| docutils       | 2.39 sec                                                                                                        | 2.97 sec: 1.24x slower                                                                                                |
| html5lib       | 57.5 ms                                                                                                         | 66.3 ms: 1.15x slower                                                                                                 |
| sphinx         | 989 ms                                                                                                          | 1.12 sec: 1.13x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260709-3.16.0a0-b2d8db1/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json | results/bm-20260709-3.16.0a0-b2d8db1-NOGIL/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 753 ms                                                                                                          | 687 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 543 ms                                                                                                          | 513 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 713 ms                                                                                                          | 707 ms: 1.01x faster                                                                                                  |
| coroutines                 | 23.7 ms                                                                                                         | 24.1 ms: 1.02x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 561 ms                                                                                                          | 583 ms: 1.04x slower                                                                                                  |
| async_tree_memoization_tg  | 364 ms                                                                                                          | 397 ms: 1.09x slower                                                                                                  |
| async_tree_none_tg         | 296 ms                                                                                                          | 330 ms: 1.11x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 541 ms                                                                                                          | 604 ms: 1.12x slower                                                                                                  |
| async_tree_memoization     | 375 ms                                                                                                          | 419 ms: 1.12x slower                                                                                                  |
| async_generators           | 340 ms                                                                                                          | 382 ms: 1.12x slower                                                                                                  |
| async_tree_none            | 288 ms                                                                                                          | 345 ms: 1.20x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260709-3.16.0a0-b2d8db1/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json | results/bm-20260709-3.16.0a0-b2d8db1-NOGIL/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 188 ms                                                                                                          | 180 ms: 1.04x faster                                                                                                  |
| float          | 74.3 ms                                                                                                         | 84.2 ms: 1.13x slower                                                                                                 |
| nbody          | 93.0 ms                                                                                                         | 126 ms: 1.35x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.14x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260709-3.16.0a0-b2d8db1/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json | results/bm-20260709-3.16.0a0-b2d8db1-NOGIL/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.7 ms                                                                                                         | 19.9 ms: 1.09x faster                                                                                                 |
| regex_dna      | 176 ms                                                                                                          | 177 ms: 1.00x slower                                                                                                  |
| regex_effbot   | 2.56 ms                                                                                                         | 2.89 ms: 1.13x slower                                                                                                 |
| regex_compile  | 148 ms                                                                                                          | 168 ms: 1.13x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.04x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260709-3.16.0a0-b2d8db1/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json | results/bm-20260709-3.16.0a0-b2d8db1-NOGIL/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 144 ms                                                                                                          | 141 ms: 1.02x faster                                                                                                  |
| xml_etree_iterparse  | 88.6 ms                                                                                                         | 95.1 ms: 1.07x slower                                                                                                 |
| json_dumps           | 9.85 ms                                                                                                         | 10.6 ms: 1.07x slower                                                                                                 |
| pickle_pure_python   | 308 us                                                                                                          | 335 us: 1.09x slower                                                                                                  |
| tomli_loads          | 1.81 sec                                                                                                        | 1.97 sec: 1.09x slower                                                                                                |
| json_loads           | 27.3 us                                                                                                         | 30.0 us: 1.10x slower                                                                                                 |
| unpickle_pure_python | 212 us                                                                                                          | 240 us: 1.13x slower                                                                                                  |
| xml_etree_generate   | 87.8 ms                                                                                                         | 101 ms: 1.15x slower                                                                                                  |
| xml_etree_process    | 61.7 ms                                                                                                         | 74.6 ms: 1.21x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260709-3.16.0a0-b2d8db1/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json | results/bm-20260709-3.16.0a0-b2d8db1-NOGIL/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                                                                         | 15.4 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 6.96 ms                                                                                                         | 9.18 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260709-3.16.0a0-b2d8db1/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json | results/bm-20260709-3.16.0a0-b2d8db1-NOGIL/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.2 ms                                                                                                         | 40.5 ms: 1.12x slower                                                                                                 |
| mako            | 12.0 ms                                                                                                         | 15.7 ms: 1.30x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.21x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260709-3.16.0a0-b2d8db1/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json | results/bm-20260709-3.16.0a0-b2d8db1-NOGIL/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 221 ms                                                                                                          | 6.89 ms: 32.09x faster                                                                                                |
| gc_traversal               | 3.83 ms                                                                                                         | 1.76 ms: 2.18x faster                                                                                                 |
| create_gc_cycles           | 1.66 ms                                                                                                         | 1.36 ms: 1.22x faster                                                                                                 |
| sqlite_synth               | 2.27 us                                                                                                         | 1.97 us: 1.15x faster                                                                                                 |
| async_tree_io_tg           | 753 ms                                                                                                          | 687 ms: 1.10x faster                                                                                                  |
| regex_v8                   | 21.7 ms                                                                                                         | 19.9 ms: 1.09x faster                                                                                                 |
| asyncio_websockets         | 543 ms                                                                                                          | 513 ms: 1.06x faster                                                                                                  |
| pidigits                   | 188 ms                                                                                                          | 180 ms: 1.04x faster                                                                                                  |
| xml_etree_parse            | 144 ms                                                                                                          | 141 ms: 1.02x faster                                                                                                  |
| async_tree_io              | 713 ms                                                                                                          | 707 ms: 1.01x faster                                                                                                  |
| regex_dna                  | 176 ms                                                                                                          | 177 ms: 1.00x slower                                                                                                  |
| pathlib                    | 17.5 ms                                                                                                         | 17.8 ms: 1.01x slower                                                                                                 |
| coroutines                 | 23.7 ms                                                                                                         | 24.1 ms: 1.02x slower                                                                                                 |
| pycparser                  | 1.10 sec                                                                                                        | 1.12 sec: 1.02x slower                                                                                                |
| dulwich_log                | 68.5 ms                                                                                                         | 70.9 ms: 1.03x slower                                                                                                 |
| bpe_tokeniser              | 4.22 sec                                                                                                        | 4.38 sec: 1.04x slower                                                                                                |
| async_tree_cpu_io_mixed_tg | 561 ms                                                                                                          | 583 ms: 1.04x slower                                                                                                  |
| json                       | 5.01 ms                                                                                                         | 5.30 ms: 1.06x slower                                                                                                 |
| xml_etree_iterparse        | 88.6 ms                                                                                                         | 95.1 ms: 1.07x slower                                                                                                 |
| k_core                     | 2.09 sec                                                                                                        | 2.25 sec: 1.07x slower                                                                                                |
| json_dumps                 | 9.85 ms                                                                                                         | 10.6 ms: 1.07x slower                                                                                                 |
| pickle_pure_python         | 308 us                                                                                                          | 335 us: 1.09x slower                                                                                                  |
| tomli_loads                | 1.81 sec                                                                                                        | 1.97 sec: 1.09x slower                                                                                                |
| async_tree_memoization_tg  | 364 ms                                                                                                          | 397 ms: 1.09x slower                                                                                                  |
| json_loads                 | 27.3 us                                                                                                         | 30.0 us: 1.10x slower                                                                                                 |
| scimark_fft                | 318 ms                                                                                                          | 349 ms: 1.10x slower                                                                                                  |
| many_optionals             | 918 us                                                                                                          | 1.01 ms: 1.10x slower                                                                                                 |
| logging_silent             | 94.3 ns                                                                                                         | 104 ns: 1.10x slower                                                                                                  |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.49 ms: 1.11x slower                                                                                                 |
| pprint_safe_repr           | 727 ms                                                                                                          | 807 ms: 1.11x slower                                                                                                  |
| async_tree_none_tg         | 296 ms                                                                                                          | 330 ms: 1.11x slower                                                                                                  |
| telco                      | 157 ms                                                                                                          | 175 ms: 1.12x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 541 ms                                                                                                          | 604 ms: 1.12x slower                                                                                                  |
| async_tree_memoization     | 375 ms                                                                                                          | 419 ms: 1.12x slower                                                                                                  |
| django_template            | 36.2 ms                                                                                                         | 40.5 ms: 1.12x slower                                                                                                 |
| async_generators           | 340 ms                                                                                                          | 382 ms: 1.12x slower                                                                                                  |
| sphinx                     | 989 ms                                                                                                          | 1.12 sec: 1.13x slower                                                                                                |
| sqlglot_v2_optimize        | 50.7 ms                                                                                                         | 57.3 ms: 1.13x slower                                                                                                 |
| pprint_pformat             | 1.48 sec                                                                                                        | 1.67 sec: 1.13x slower                                                                                                |
| regex_effbot               | 2.56 ms                                                                                                         | 2.89 ms: 1.13x slower                                                                                                 |
| comprehensions             | 15.9 us                                                                                                         | 18.0 us: 1.13x slower                                                                                                 |
| regex_compile              | 148 ms                                                                                                          | 168 ms: 1.13x slower                                                                                                  |
| float                      | 74.3 ms                                                                                                         | 84.2 ms: 1.13x slower                                                                                                 |
| unpickle_pure_python       | 212 us                                                                                                          | 240 us: 1.13x slower                                                                                                  |
| scimark_lu                 | 114 ms                                                                                                          | 129 ms: 1.13x slower                                                                                                  |
| generators                 | 28.7 ms                                                                                                         | 32.6 ms: 1.14x slower                                                                                                 |
| sympy_expand               | 457 ms                                                                                                          | 522 ms: 1.14x slower                                                                                                  |
| hexiom                     | 5.76 ms                                                                                                         | 6.59 ms: 1.14x slower                                                                                                 |
| sympy_str                  | 272 ms                                                                                                          | 311 ms: 1.14x slower                                                                                                  |
| deltablue                  | 3.23 ms                                                                                                         | 3.70 ms: 1.14x slower                                                                                                 |
| pylint                     | 115 ms                                                                                                          | 131 ms: 1.14x slower                                                                                                  |
| sympy_integrate            | 19.1 ms                                                                                                         | 21.8 ms: 1.14x slower                                                                                                 |
| sqlglot_v2_normalize       | 100 ms                                                                                                          | 115 ms: 1.14x slower                                                                                                  |
| scimark_sor                | 106 ms                                                                                                          | 122 ms: 1.15x slower                                                                                                  |
| chaos                      | 54.1 ms                                                                                                         | 62.0 ms: 1.15x slower                                                                                                 |
| 2to3                       | 258 ms                                                                                                          | 296 ms: 1.15x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.31 sec: 1.15x slower                                                                                                |
| xml_etree_generate         | 87.8 ms                                                                                                         | 101 ms: 1.15x slower                                                                                                  |
| spectral_norm              | 93.1 ms                                                                                                         | 107 ms: 1.15x slower                                                                                                  |
| thrift                     | 781 us                                                                                                          | 899 us: 1.15x slower                                                                                                  |
| html5lib                   | 57.5 ms                                                                                                         | 66.3 ms: 1.15x slower                                                                                                 |
| subparsers                 | 9.24 ms                                                                                                         | 10.7 ms: 1.15x slower                                                                                                 |
| sympy_sum                  | 156 ms                                                                                                          | 180 ms: 1.15x slower                                                                                                  |
| deepcopy_reduce            | 2.57 us                                                                                                         | 2.97 us: 1.15x slower                                                                                                 |
| deepcopy_memo              | 26.8 us                                                                                                         | 31.1 us: 1.16x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.59 ms                                                                                                         | 5.34 ms: 1.16x slower                                                                                                 |
| deepcopy                   | 231 us                                                                                                          | 270 us: 1.17x slower                                                                                                  |
| logging_simple             | 5.99 us                                                                                                         | 7.02 us: 1.17x slower                                                                                                 |
| go                         | 103 ms                                                                                                          | 121 ms: 1.18x slower                                                                                                  |
| logging_format             | 6.76 us                                                                                                         | 8.04 us: 1.19x slower                                                                                                 |
| async_tree_none            | 288 ms                                                                                                          | 345 ms: 1.20x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.44 ms                                                                                                         | 1.73 ms: 1.20x slower                                                                                                 |
| raytrace                   | 252 ms                                                                                                          | 304 ms: 1.20x slower                                                                                                  |
| xml_etree_process          | 61.7 ms                                                                                                         | 74.6 ms: 1.21x slower                                                                                                 |
| nqueens                    | 73.6 ms                                                                                                         | 89.2 ms: 1.21x slower                                                                                                 |
| typing_runtime_protocols   | 118 us                                                                                                          | 143 us: 1.21x slower                                                                                                  |
| pyflate                    | 382 ms                                                                                                          | 469 ms: 1.23x slower                                                                                                  |
| richards_super             | 48.4 ms                                                                                                         | 59.5 ms: 1.23x slower                                                                                                 |
| richards                   | 42.2 ms                                                                                                         | 52.0 ms: 1.23x slower                                                                                                 |
| sqlglot_v2_parse           | 1.13 ms                                                                                                         | 1.40 ms: 1.23x slower                                                                                                 |
| shortest_path              | 437 ms                                                                                                          | 540 ms: 1.24x slower                                                                                                  |
| connected_components       | 396 ms                                                                                                          | 491 ms: 1.24x slower                                                                                                  |
| docutils                   | 2.39 sec                                                                                                        | 2.97 sec: 1.24x slower                                                                                                |
| scimark_monte_carlo        | 63.4 ms                                                                                                         | 78.7 ms: 1.24x slower                                                                                                 |
| fannkuch                   | 373 ms                                                                                                          | 465 ms: 1.25x slower                                                                                                  |
| python_startup             | 12.3 ms                                                                                                         | 15.4 ms: 1.25x slower                                                                                                 |
| meteor_contest             | 100 ms                                                                                                          | 126 ms: 1.25x slower                                                                                                  |
| mako                       | 12.0 ms                                                                                                         | 15.7 ms: 1.30x slower                                                                                                 |
| crypto_pyaes               | 69.0 ms                                                                                                         | 90.3 ms: 1.31x slower                                                                                                 |
| python_startup_no_site     | 6.96 ms                                                                                                         | 9.18 ms: 1.32x slower                                                                                                 |
| nbody                      | 93.0 ms                                                                                                         | 126 ms: 1.35x slower                                                                                                  |
| coverage                   | 83.6 ms                                                                                                         | 115 ms: 1.38x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.105x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.18x