# Results vs. base

- fork: python
- ref: 763b6edb0ec959bdfb78
- machine: linux-x86_64
- commit hash: 763b6ed
- commit date: 2026-10-01
- overall geometric mean: 1.108x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json | results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                                                          | 296 ms: 1.14x slower                                                                                                  |
| docutils       | 2.38 sec                                                                                                        | 2.92 sec: 1.23x slower                                                                                                |
| html5lib       | 58.8 ms                                                                                                         | 66.4 ms: 1.13x slower                                                                                                 |
| sphinx         | 976 ms                                                                                                          | 1.12 sec: 1.15x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json | results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 754 ms                                                                                                          | 704 ms: 1.07x faster                                                                                                  |
| asyncio_websockets         | 543 ms                                                                                                          | 510 ms: 1.07x faster                                                                                                  |
| async_tree_io              | 771 ms                                                                                                          | 730 ms: 1.06x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 552 ms                                                                                                          | 584 ms: 1.06x slower                                                                                                  |
| coroutines                 | 24.1 ms                                                                                                         | 25.7 ms: 1.06x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 561 ms                                                                                                          | 613 ms: 1.09x slower                                                                                                  |
| async_tree_memoization_tg  | 363 ms                                                                                                          | 409 ms: 1.13x slower                                                                                                  |
| async_tree_memoization     | 400 ms                                                                                                          | 456 ms: 1.14x slower                                                                                                  |
| async_tree_none            | 328 ms                                                                                                          | 381 ms: 1.16x slower                                                                                                  |
| async_tree_none_tg         | 296 ms                                                                                                          | 343 ms: 1.16x slower                                                                                                  |
| async_generators           | 349 ms                                                                                                          | 422 ms: 1.21x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json | results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                                                          | 182 ms: 1.03x faster                                                                                                  |
| float          | 72.2 ms                                                                                                         | 83.6 ms: 1.16x slower                                                                                                 |
| nbody          | 89.1 ms                                                                                                         | 120 ms: 1.34x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.15x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json | results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.6 ms                                                                                                         | 20.0 ms: 1.08x faster                                                                                                 |
| regex_dna      | 178 ms                                                                                                          | 177 ms: 1.01x faster                                                                                                  |
| regex_effbot   | 2.64 ms                                                                                                         | 2.84 ms: 1.08x slower                                                                                                 |
| regex_compile  | 148 ms                                                                                                          | 170 ms: 1.14x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.03x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json | results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 145 ms                                                                                                          | 142 ms: 1.01x faster                                                                                                  |
| xml_etree_iterparse  | 92.6 ms                                                                                                         | 97.0 ms: 1.05x slower                                                                                                 |
| tomli_loads          | 1.84 sec                                                                                                        | 1.95 sec: 1.06x slower                                                                                                |
| json_dumps           | 9.34 ms                                                                                                         | 10.1 ms: 1.08x slower                                                                                                 |
| json_loads           | 27.5 us                                                                                                         | 30.7 us: 1.12x slower                                                                                                 |
| pickle_pure_python   | 301 us                                                                                                          | 340 us: 1.13x slower                                                                                                  |
| unpickle_pure_python | 211 us                                                                                                          | 239 us: 1.13x slower                                                                                                  |
| xml_etree_generate   | 88.1 ms                                                                                                         | 101 ms: 1.15x slower                                                                                                  |
| xml_etree_process    | 62.2 ms                                                                                                         | 75.5 ms: 1.21x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json | results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 7.74 ms                                                                                                         | 9.69 ms: 1.25x slower                                                                                                 |
| python_startup         | 12.9 ms                                                                                                         | 16.3 ms: 1.26x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.26x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json | results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.9 ms                                                                                                         | 41.6 ms: 1.13x slower                                                                                                 |
| mako            | 12.1 ms                                                                                                         | 16.2 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json | results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 253 ms                                                                                                          | 6.69 ms: 37.82x faster                                                                                                |
| gc_traversal               | 3.72 ms                                                                                                         | 1.77 ms: 2.11x faster                                                                                                 |
| create_gc_cycles           | 1.67 ms                                                                                                         | 1.38 ms: 1.21x faster                                                                                                 |
| sqlite_synth               | 2.25 us                                                                                                         | 1.97 us: 1.14x faster                                                                                                 |
| regex_v8                   | 21.6 ms                                                                                                         | 20.0 ms: 1.08x faster                                                                                                 |
| async_tree_io_tg           | 754 ms                                                                                                          | 704 ms: 1.07x faster                                                                                                  |
| asyncio_websockets         | 543 ms                                                                                                          | 510 ms: 1.07x faster                                                                                                  |
| async_tree_io              | 771 ms                                                                                                          | 730 ms: 1.06x faster                                                                                                  |
| pidigits                   | 187 ms                                                                                                          | 182 ms: 1.03x faster                                                                                                  |
| xml_etree_parse            | 145 ms                                                                                                          | 142 ms: 1.01x faster                                                                                                  |
| regex_dna                  | 178 ms                                                                                                          | 177 ms: 1.01x faster                                                                                                  |
| pathlib                    | 17.7 ms                                                                                                         | 18.0 ms: 1.02x slower                                                                                                 |
| pycparser                  | 1.11 sec                                                                                                        | 1.14 sec: 1.02x slower                                                                                                |
| bpe_tokeniser              | 4.20 sec                                                                                                        | 4.35 sec: 1.03x slower                                                                                                |
| xml_etree_iterparse        | 92.6 ms                                                                                                         | 97.0 ms: 1.05x slower                                                                                                 |
| dulwich_log                | 68.1 ms                                                                                                         | 71.8 ms: 1.05x slower                                                                                                 |
| tomli_loads                | 1.84 sec                                                                                                        | 1.95 sec: 1.06x slower                                                                                                |
| async_tree_cpu_io_mixed_tg | 552 ms                                                                                                          | 584 ms: 1.06x slower                                                                                                  |
| coroutines                 | 24.1 ms                                                                                                         | 25.7 ms: 1.06x slower                                                                                                 |
| json_dumps                 | 9.34 ms                                                                                                         | 10.1 ms: 1.08x slower                                                                                                 |
| regex_effbot               | 2.64 ms                                                                                                         | 2.84 ms: 1.08x slower                                                                                                 |
| json                       | 5.04 ms                                                                                                         | 5.43 ms: 1.08x slower                                                                                                 |
| k_core                     | 2.08 sec                                                                                                        | 2.26 sec: 1.09x slower                                                                                                |
| async_tree_cpu_io_mixed    | 561 ms                                                                                                          | 613 ms: 1.09x slower                                                                                                  |
| scimark_fft                | 308 ms                                                                                                          | 338 ms: 1.10x slower                                                                                                  |
| many_optionals             | 913 us                                                                                                          | 1.01 ms: 1.10x slower                                                                                                 |
| sqlglot_v2_normalize       | 101 ms                                                                                                          | 113 ms: 1.12x slower                                                                                                  |
| json_loads                 | 27.5 us                                                                                                         | 30.7 us: 1.12x slower                                                                                                 |
| deltablue                  | 3.31 ms                                                                                                         | 3.70 ms: 1.12x slower                                                                                                 |
| logging_silent             | 95.3 ns                                                                                                         | 107 ns: 1.12x slower                                                                                                  |
| telco                      | 160 ms                                                                                                          | 179 ms: 1.12x slower                                                                                                  |
| scimark_lu                 | 117 ms                                                                                                          | 132 ms: 1.13x slower                                                                                                  |
| django_template            | 36.9 ms                                                                                                         | 41.6 ms: 1.13x slower                                                                                                 |
| async_tree_memoization_tg  | 363 ms                                                                                                          | 409 ms: 1.13x slower                                                                                                  |
| sqlglot_v2_optimize        | 50.3 ms                                                                                                         | 56.7 ms: 1.13x slower                                                                                                 |
| html5lib                   | 58.8 ms                                                                                                         | 66.4 ms: 1.13x slower                                                                                                 |
| pickle_pure_python         | 301 us                                                                                                          | 340 us: 1.13x slower                                                                                                  |
| scimark_sor                | 107 ms                                                                                                          | 121 ms: 1.13x slower                                                                                                  |
| unpickle_pure_python       | 211 us                                                                                                          | 239 us: 1.13x slower                                                                                                  |
| pprint_safe_repr           | 729 ms                                                                                                          | 826 ms: 1.13x slower                                                                                                  |
| sympy_expand               | 467 ms                                                                                                          | 531 ms: 1.14x slower                                                                                                  |
| comprehensions             | 15.8 us                                                                                                         | 18.0 us: 1.14x slower                                                                                                 |
| async_tree_memoization     | 400 ms                                                                                                          | 456 ms: 1.14x slower                                                                                                  |
| 2to3                       | 259 ms                                                                                                          | 296 ms: 1.14x slower                                                                                                  |
| regex_compile              | 148 ms                                                                                                          | 170 ms: 1.14x slower                                                                                                  |
| pprint_pformat             | 1.50 sec                                                                                                        | 1.72 sec: 1.15x slower                                                                                                |
| sphinx                     | 976 ms                                                                                                          | 1.12 sec: 1.15x slower                                                                                                |
| xml_etree_generate         | 88.1 ms                                                                                                         | 101 ms: 1.15x slower                                                                                                  |
| sympy_str                  | 275 ms                                                                                                          | 316 ms: 1.15x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.31 sec: 1.15x slower                                                                                                |
| sympy_integrate            | 19.0 ms                                                                                                         | 21.9 ms: 1.15x slower                                                                                                 |
| spectral_norm              | 90.8 ms                                                                                                         | 105 ms: 1.15x slower                                                                                                  |
| pylint                     | 113 ms                                                                                                          | 131 ms: 1.16x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.49 ms                                                                                                         | 5.20 ms: 1.16x slower                                                                                                 |
| float                      | 72.2 ms                                                                                                         | 83.6 ms: 1.16x slower                                                                                                 |
| async_tree_none            | 328 ms                                                                                                          | 381 ms: 1.16x slower                                                                                                  |
| chaos                      | 52.7 ms                                                                                                         | 61.1 ms: 1.16x slower                                                                                                 |
| async_tree_none_tg         | 296 ms                                                                                                          | 343 ms: 1.16x slower                                                                                                  |
| hexiom                     | 5.64 ms                                                                                                         | 6.55 ms: 1.16x slower                                                                                                 |
| sympy_sum                  | 155 ms                                                                                                          | 180 ms: 1.16x slower                                                                                                  |
| go                         | 103 ms                                                                                                          | 120 ms: 1.17x slower                                                                                                  |
| deepcopy_reduce            | 2.57 us                                                                                                         | 3.00 us: 1.17x slower                                                                                                 |
| subparsers                 | 8.94 ms                                                                                                         | 10.5 ms: 1.17x slower                                                                                                 |
| deepcopy                   | 230 us                                                                                                          | 270 us: 1.17x slower                                                                                                  |
| logging_simple             | 6.04 us                                                                                                         | 7.09 us: 1.17x slower                                                                                                 |
| thrift                     | 788 us                                                                                                          | 928 us: 1.18x slower                                                                                                  |
| nqueens                    | 74.3 ms                                                                                                         | 87.8 ms: 1.18x slower                                                                                                 |
| raytrace                   | 248 ms                                                                                                          | 294 ms: 1.19x slower                                                                                                  |
| generators                 | 28.2 ms                                                                                                         | 33.7 ms: 1.20x slower                                                                                                 |
| logging_format             | 6.74 us                                                                                                         | 8.09 us: 1.20x slower                                                                                                 |
| pyflate                    | 380 ms                                                                                                          | 457 ms: 1.20x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.44 ms                                                                                                         | 1.74 ms: 1.20x slower                                                                                                 |
| richards_super             | 50.5 ms                                                                                                         | 60.9 ms: 1.21x slower                                                                                                 |
| deepcopy_memo              | 28.0 us                                                                                                         | 33.8 us: 1.21x slower                                                                                                 |
| async_generators           | 349 ms                                                                                                          | 422 ms: 1.21x slower                                                                                                  |
| richards                   | 43.8 ms                                                                                                         | 53.1 ms: 1.21x slower                                                                                                 |
| xml_etree_process          | 62.2 ms                                                                                                         | 75.5 ms: 1.21x slower                                                                                                 |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.63 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_parse           | 1.15 ms                                                                                                         | 1.40 ms: 1.22x slower                                                                                                 |
| fannkuch                   | 375 ms                                                                                                          | 458 ms: 1.22x slower                                                                                                  |
| docutils                   | 2.38 sec                                                                                                        | 2.92 sec: 1.23x slower                                                                                                |
| typing_runtime_protocols   | 118 us                                                                                                          | 146 us: 1.23x slower                                                                                                  |
| scimark_monte_carlo        | 63.1 ms                                                                                                         | 78.1 ms: 1.24x slower                                                                                                 |
| shortest_path              | 431 ms                                                                                                          | 534 ms: 1.24x slower                                                                                                  |
| python_startup_no_site     | 7.74 ms                                                                                                         | 9.69 ms: 1.25x slower                                                                                                 |
| meteor_contest             | 100.0 ms                                                                                                        | 126 ms: 1.26x slower                                                                                                  |
| python_startup             | 12.9 ms                                                                                                         | 16.3 ms: 1.26x slower                                                                                                 |
| connected_components       | 390 ms                                                                                                          | 493 ms: 1.27x slower                                                                                                  |
| crypto_pyaes               | 67.6 ms                                                                                                         | 88.3 ms: 1.31x slower                                                                                                 |
| mako                       | 12.1 ms                                                                                                         | 16.2 ms: 1.34x slower                                                                                                 |
| nbody                      | 89.1 ms                                                                                                         | 120 ms: 1.34x slower                                                                                                  |
| coverage                   | 83.2 ms                                                                                                         | 118 ms: 1.42x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.08x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.108x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.18x