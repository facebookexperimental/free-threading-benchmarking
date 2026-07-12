# Results vs. base

- fork: python
- ref: c22e9c9daef4d97a3fdf
- machine: linux-x86_64
- commit hash: c22e9c9
- commit date: 2026-07-10
- overall geometric mean: 1.104x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260710-3.16.0a0-c22e9c9/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json | results/bm-20260710-3.16.0a0-c22e9c9-NOGIL/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                                                          | 296 ms: 1.15x slower                                                                                                  |
| docutils       | 2.41 sec                                                                                                        | 2.96 sec: 1.23x slower                                                                                                |
| html5lib       | 60.2 ms                                                                                                         | 68.1 ms: 1.13x slower                                                                                                 |
| sphinx         | 992 ms                                                                                                          | 1.11 sec: 1.12x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260710-3.16.0a0-c22e9c9/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json | results/bm-20260710-3.16.0a0-c22e9c9-NOGIL/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 754 ms                                                                                                          | 686 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 514 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 714 ms                                                                                                          | 702 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 557 ms                                                                                                          | 581 ms: 1.04x slower                                                                                                  |
| async_tree_memoization_tg  | 364 ms                                                                                                          | 396 ms: 1.09x slower                                                                                                  |
| async_tree_none_tg         | 297 ms                                                                                                          | 323 ms: 1.09x slower                                                                                                  |
| coroutines                 | 23.3 ms                                                                                                         | 25.8 ms: 1.10x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 541 ms                                                                                                          | 601 ms: 1.11x slower                                                                                                  |
| async_tree_memoization     | 374 ms                                                                                                          | 418 ms: 1.12x slower                                                                                                  |
| async_generators           | 344 ms                                                                                                          | 390 ms: 1.13x slower                                                                                                  |
| async_tree_none            | 289 ms                                                                                                          | 338 ms: 1.17x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260710-3.16.0a0-c22e9c9/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json | results/bm-20260710-3.16.0a0-c22e9c9-NOGIL/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 195 ms                                                                                                          | 180 ms: 1.08x faster                                                                                                  |
| float          | 74.1 ms                                                                                                         | 84.9 ms: 1.15x slower                                                                                                 |
| nbody          | 91.6 ms                                                                                                         | 125 ms: 1.37x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.13x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260710-3.16.0a0-c22e9c9/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json | results/bm-20260710-3.16.0a0-c22e9c9-NOGIL/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.6 ms                                                                                                         | 20.9 ms: 1.03x faster                                                                                                 |
| regex_dna      | 188 ms                                                                                                          | 187 ms: 1.01x faster                                                                                                  |
| regex_effbot   | 2.83 ms                                                                                                         | 3.06 ms: 1.08x slower                                                                                                 |
| regex_compile  | 148 ms                                                                                                          | 168 ms: 1.14x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.04x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260710-3.16.0a0-c22e9c9/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json | results/bm-20260710-3.16.0a0-c22e9c9-NOGIL/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| xml_etree_iterparse  | 89.3 ms                                                                                                         | 95.3 ms: 1.07x slower                                                                                                 |
| json_dumps           | 9.81 ms                                                                                                         | 10.7 ms: 1.09x slower                                                                                                 |
| json_loads           | 27.4 us                                                                                                         | 29.9 us: 1.09x slower                                                                                                 |
| pickle_pure_python   | 309 us                                                                                                          | 338 us: 1.09x slower                                                                                                  |
| tomli_loads          | 1.79 sec                                                                                                        | 1.97 sec: 1.10x slower                                                                                                |
| unpickle_pure_python | 213 us                                                                                                          | 240 us: 1.12x slower                                                                                                  |
| xml_etree_generate   | 86.3 ms                                                                                                         | 101 ms: 1.16x slower                                                                                                  |
| xml_etree_process    | 60.6 ms                                                                                                         | 74.5 ms: 1.23x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260710-3.16.0a0-c22e9c9/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json | results/bm-20260710-3.16.0a0-c22e9c9-NOGIL/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                         | 15.6 ms: 1.26x slower                                                                                                 |
| python_startup_no_site | 7.03 ms                                                                                                         | 9.28 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260710-3.16.0a0-c22e9c9/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json | results/bm-20260710-3.16.0a0-c22e9c9-NOGIL/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.7 ms                                                                                                         | 40.3 ms: 1.13x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 15.8 ms: 1.33x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260710-3.16.0a0-c22e9c9/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json | results/bm-20260710-3.16.0a0-c22e9c9-NOGIL/bm-20260710-vultr-x86_64-python-c22e9c9daef4d97a3fdf-3.16.0a0-c22e9c9.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 261 ms                                                                                                          | 6.93 ms: 37.61x faster                                                                                                |
| gc_traversal               | 3.86 ms                                                                                                         | 1.77 ms: 2.18x faster                                                                                                 |
| create_gc_cycles           | 1.69 ms                                                                                                         | 1.36 ms: 1.24x faster                                                                                                 |
| sqlite_synth               | 2.24 us                                                                                                         | 1.97 us: 1.14x faster                                                                                                 |
| async_tree_io_tg           | 754 ms                                                                                                          | 686 ms: 1.10x faster                                                                                                  |
| pidigits                   | 195 ms                                                                                                          | 180 ms: 1.08x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 514 ms: 1.06x faster                                                                                                  |
| regex_v8                   | 21.6 ms                                                                                                         | 20.9 ms: 1.03x faster                                                                                                 |
| xml_etree_parse            | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| async_tree_io              | 714 ms                                                                                                          | 702 ms: 1.02x faster                                                                                                  |
| regex_dna                  | 188 ms                                                                                                          | 187 ms: 1.01x faster                                                                                                  |
| pathlib                    | 17.8 ms                                                                                                         | 17.9 ms: 1.00x slower                                                                                                 |
| dulwich_log                | 68.9 ms                                                                                                         | 70.9 ms: 1.03x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 557 ms                                                                                                          | 581 ms: 1.04x slower                                                                                                  |
| bpe_tokeniser              | 4.20 sec                                                                                                        | 4.38 sec: 1.04x slower                                                                                                |
| pycparser                  | 1.11 sec                                                                                                        | 1.16 sec: 1.04x slower                                                                                                |
| json                       | 5.03 ms                                                                                                         | 5.26 ms: 1.04x slower                                                                                                 |
| xml_etree_iterparse        | 89.3 ms                                                                                                         | 95.3 ms: 1.07x slower                                                                                                 |
| k_core                     | 2.10 sec                                                                                                        | 2.25 sec: 1.07x slower                                                                                                |
| regex_effbot               | 2.83 ms                                                                                                         | 3.06 ms: 1.08x slower                                                                                                 |
| many_optionals             | 929 us                                                                                                          | 1.01 ms: 1.09x slower                                                                                                 |
| async_tree_memoization_tg  | 364 ms                                                                                                          | 396 ms: 1.09x slower                                                                                                  |
| async_tree_none_tg         | 297 ms                                                                                                          | 323 ms: 1.09x slower                                                                                                  |
| telco                      | 160 ms                                                                                                          | 175 ms: 1.09x slower                                                                                                  |
| json_dumps                 | 9.81 ms                                                                                                         | 10.7 ms: 1.09x slower                                                                                                 |
| json_loads                 | 27.4 us                                                                                                         | 29.9 us: 1.09x slower                                                                                                 |
| pickle_pure_python         | 309 us                                                                                                          | 338 us: 1.09x slower                                                                                                  |
| deltablue                  | 3.34 ms                                                                                                         | 3.68 ms: 1.10x slower                                                                                                 |
| tomli_loads                | 1.79 sec                                                                                                        | 1.97 sec: 1.10x slower                                                                                                |
| coroutines                 | 23.3 ms                                                                                                         | 25.8 ms: 1.10x slower                                                                                                 |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.49 ms: 1.11x slower                                                                                                 |
| scimark_fft                | 318 ms                                                                                                          | 353 ms: 1.11x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 541 ms                                                                                                          | 601 ms: 1.11x slower                                                                                                  |
| sphinx                     | 992 ms                                                                                                          | 1.11 sec: 1.12x slower                                                                                                |
| async_tree_memoization     | 374 ms                                                                                                          | 418 ms: 1.12x slower                                                                                                  |
| comprehensions             | 15.9 us                                                                                                         | 17.8 us: 1.12x slower                                                                                                 |
| logging_silent             | 96.0 ns                                                                                                         | 108 ns: 1.12x slower                                                                                                  |
| unpickle_pure_python       | 213 us                                                                                                          | 240 us: 1.12x slower                                                                                                  |
| pprint_safe_repr           | 710 ms                                                                                                          | 799 ms: 1.12x slower                                                                                                  |
| logging_simple             | 6.10 us                                                                                                         | 6.86 us: 1.13x slower                                                                                                 |
| sqlglot_v2_optimize        | 51.2 ms                                                                                                         | 57.7 ms: 1.13x slower                                                                                                 |
| logging_format             | 6.85 us                                                                                                         | 7.72 us: 1.13x slower                                                                                                 |
| django_template            | 35.7 ms                                                                                                         | 40.3 ms: 1.13x slower                                                                                                 |
| scimark_sor                | 109 ms                                                                                                          | 123 ms: 1.13x slower                                                                                                  |
| html5lib                   | 60.2 ms                                                                                                         | 68.1 ms: 1.13x slower                                                                                                 |
| sympy_expand               | 458 ms                                                                                                          | 520 ms: 1.13x slower                                                                                                  |
| subparsers                 | 9.31 ms                                                                                                         | 10.6 ms: 1.13x slower                                                                                                 |
| async_generators           | 344 ms                                                                                                          | 390 ms: 1.13x slower                                                                                                  |
| sympy_integrate            | 19.2 ms                                                                                                         | 21.9 ms: 1.14x slower                                                                                                 |
| go                         | 106 ms                                                                                                          | 121 ms: 1.14x slower                                                                                                  |
| deepcopy_reduce            | 2.57 us                                                                                                         | 2.93 us: 1.14x slower                                                                                                 |
| sympy_str                  | 274 ms                                                                                                          | 312 ms: 1.14x slower                                                                                                  |
| sympy_sum                  | 157 ms                                                                                                          | 179 ms: 1.14x slower                                                                                                  |
| sqlglot_v2_normalize       | 101 ms                                                                                                          | 115 ms: 1.14x slower                                                                                                  |
| regex_compile              | 148 ms                                                                                                          | 168 ms: 1.14x slower                                                                                                  |
| pylint                     | 115 ms                                                                                                          | 131 ms: 1.14x slower                                                                                                  |
| deepcopy_memo              | 27.0 us                                                                                                         | 31.0 us: 1.15x slower                                                                                                 |
| mdp                        | 1.14 sec                                                                                                        | 1.30 sec: 1.15x slower                                                                                                |
| scimark_lu                 | 112 ms                                                                                                          | 129 ms: 1.15x slower                                                                                                  |
| float                      | 74.1 ms                                                                                                         | 84.9 ms: 1.15x slower                                                                                                 |
| 2to3                       | 258 ms                                                                                                          | 296 ms: 1.15x slower                                                                                                  |
| pprint_pformat             | 1.45 sec                                                                                                        | 1.67 sec: 1.15x slower                                                                                                |
| deepcopy                   | 233 us                                                                                                          | 270 us: 1.16x slower                                                                                                  |
| chaos                      | 54.2 ms                                                                                                         | 62.8 ms: 1.16x slower                                                                                                 |
| hexiom                     | 5.63 ms                                                                                                         | 6.54 ms: 1.16x slower                                                                                                 |
| thrift                     | 786 us                                                                                                          | 913 us: 1.16x slower                                                                                                  |
| xml_etree_generate         | 86.3 ms                                                                                                         | 101 ms: 1.16x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.50 ms                                                                                                         | 1.75 ms: 1.17x slower                                                                                                 |
| async_tree_none            | 289 ms                                                                                                          | 338 ms: 1.17x slower                                                                                                  |
| nqueens                    | 74.2 ms                                                                                                         | 87.3 ms: 1.18x slower                                                                                                 |
| generators                 | 28.2 ms                                                                                                         | 33.3 ms: 1.18x slower                                                                                                 |
| pyflate                    | 394 ms                                                                                                          | 468 ms: 1.19x slower                                                                                                  |
| shortest_path              | 445 ms                                                                                                          | 535 ms: 1.20x slower                                                                                                  |
| raytrace                   | 254 ms                                                                                                          | 306 ms: 1.21x slower                                                                                                  |
| sqlglot_v2_parse           | 1.16 ms                                                                                                         | 1.40 ms: 1.21x slower                                                                                                 |
| meteor_contest             | 102 ms                                                                                                          | 124 ms: 1.21x slower                                                                                                  |
| connected_components       | 401 ms                                                                                                          | 489 ms: 1.22x slower                                                                                                  |
| richards_super             | 49.2 ms                                                                                                         | 60.2 ms: 1.22x slower                                                                                                 |
| fannkuch                   | 378 ms                                                                                                          | 464 ms: 1.23x slower                                                                                                  |
| xml_etree_process          | 60.6 ms                                                                                                         | 74.5 ms: 1.23x slower                                                                                                 |
| docutils                   | 2.41 sec                                                                                                        | 2.96 sec: 1.23x slower                                                                                                |
| scimark_sparse_mat_mult    | 4.52 ms                                                                                                         | 5.57 ms: 1.23x slower                                                                                                 |
| typing_runtime_protocols   | 117 us                                                                                                          | 146 us: 1.24x slower                                                                                                  |
| scimark_monte_carlo        | 63.4 ms                                                                                                         | 79.4 ms: 1.25x slower                                                                                                 |
| python_startup             | 12.4 ms                                                                                                         | 15.6 ms: 1.26x slower                                                                                                 |
| spectral_norm              | 90.2 ms                                                                                                         | 113 ms: 1.26x slower                                                                                                  |
| richards                   | 42.9 ms                                                                                                         | 54.3 ms: 1.26x slower                                                                                                 |
| crypto_pyaes               | 69.1 ms                                                                                                         | 89.7 ms: 1.30x slower                                                                                                 |
| python_startup_no_site     | 7.03 ms                                                                                                         | 9.28 ms: 1.32x slower                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 15.8 ms: 1.33x slower                                                                                                 |
| nbody                      | 91.6 ms                                                                                                         | 125 ms: 1.37x slower                                                                                                  |
| coverage                   | 82.8 ms                                                                                                         | 115 ms: 1.39x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.104x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.18x