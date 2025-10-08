# Results vs. base

- fork: python
- ref: 85ec35d2ab8b764aefd6
- machine: linux-x86_64
- commit hash: 85ec35d
- commit date: 2025-10-08
- overall geometric mean: 1.091x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json | results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                                                                          | 279 ms: 1.13x slower                                                                                                  |
| docutils       | 2.55 sec                                                                                                        | 2.67 sec: 1.05x slower                                                                                                |
| html5lib       | 62.7 ms                                                                                                         | 66.5 ms: 1.06x slower                                                                                                 |
| sphinx         | 974 ms                                                                                                          | 1.07 sec: 1.10x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json | results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 624 ms                                                                                                          | 518 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 252 ms                                                                                                          | 225 ms: 1.12x faster                                                                                                  |
| async_tree_memoization_tg  | 316 ms                                                                                                          | 283 ms: 1.11x faster                                                                                                  |
| async_tree_io              | 605 ms                                                                                                          | 544 ms: 1.11x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                                                          | 468 ms: 1.06x faster                                                                                                  |
| async_tree_none            | 263 ms                                                                                                          | 256 ms: 1.03x faster                                                                                                  |
| coroutines                 | 24.5 ms                                                                                                         | 24.1 ms: 1.02x faster                                                                                                 |
| async_tree_memoization     | 313 ms                                                                                                          | 310 ms: 1.01x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 491 ms                                                                                                          | 495 ms: 1.01x slower                                                                                                  |
| async_generators           | 341 ms                                                                                                          | 370 ms: 1.09x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x faster                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json | results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 72.3 ms                                                                                                         | 69.2 ms: 1.04x faster                                                                                                 |
| pidigits       | 213 ms                                                                                                          | 207 ms: 1.03x faster                                                                                                  |
| nbody          | 92.1 ms                                                                                                         | 126 ms: 1.37x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json | results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 179 ms                                                                                                          | 170 ms: 1.05x faster                                                                                                  |
| regex_v8       | 21.4 ms                                                                                                         | 20.8 ms: 1.03x faster                                                                                                 |
| regex_effbot   | 2.69 ms                                                                                                         | 2.75 ms: 1.02x slower                                                                                                 |
| regex_compile  | 123 ms                                                                                                          | 143 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.02x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json | results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.8 ms                                                                                                         | 88.0 ms: 1.07x faster                                                                                                 |
| xml_etree_parse      | 134 ms                                                                                                          | 130 ms: 1.03x faster                                                                                                  |
| tomli_loads          | 1.91 sec                                                                                                        | 2.03 sec: 1.06x slower                                                                                                |
| pickle_pure_python   | 306 us                                                                                                          | 339 us: 1.11x slower                                                                                                  |
| unpickle_pure_python | 206 us                                                                                                          | 232 us: 1.13x slower                                                                                                  |
| json_loads           | 27.8 us                                                                                                         | 31.6 us: 1.14x slower                                                                                                 |
| json_dumps           | 9.61 ms                                                                                                         | 11.0 ms: 1.14x slower                                                                                                 |
| xml_etree_generate   | 83.1 ms                                                                                                         | 96.0 ms: 1.16x slower                                                                                                 |
| xml_etree_process    | 57.7 ms                                                                                                         | 69.3 ms: 1.20x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json | results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                                                         | 15.8 ms: 1.26x slower                                                                                                 |
| python_startup_no_site | 7.24 ms                                                                                                         | 9.59 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json | results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.5 ms                                                                                                         | 40.8 ms: 1.18x slower                                                                                                 |
| genshi_xml      | 48.1 ms                                                                                                         | 57.7 ms: 1.20x slower                                                                                                 |
| genshi_text     | 20.4 ms                                                                                                         | 26.5 ms: 1.30x slower                                                                                                 |
| mako            | 11.6 ms                                                                                                         | 15.5 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.25x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json | results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.66 ms                                                                                                         | 1.95 ms: 2.39x faster                                                                                                 |
| create_gc_cycles           | 1.92 ms                                                                                                         | 1.53 ms: 1.26x faster                                                                                                 |
| async_tree_io_tg           | 624 ms                                                                                                          | 518 ms: 1.20x faster                                                                                                  |
| sqlite_synth               | 2.30 us                                                                                                         | 2.05 us: 1.12x faster                                                                                                 |
| async_tree_none_tg         | 252 ms                                                                                                          | 225 ms: 1.12x faster                                                                                                  |
| async_tree_memoization_tg  | 316 ms                                                                                                          | 283 ms: 1.11x faster                                                                                                  |
| async_tree_io              | 605 ms                                                                                                          | 544 ms: 1.11x faster                                                                                                  |
| xml_etree_iterparse        | 93.8 ms                                                                                                         | 88.0 ms: 1.07x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                                                          | 468 ms: 1.06x faster                                                                                                  |
| regex_dna                  | 179 ms                                                                                                          | 170 ms: 1.05x faster                                                                                                  |
| float                      | 72.3 ms                                                                                                         | 69.2 ms: 1.04x faster                                                                                                 |
| regex_v8                   | 21.4 ms                                                                                                         | 20.8 ms: 1.03x faster                                                                                                 |
| pidigits                   | 213 ms                                                                                                          | 207 ms: 1.03x faster                                                                                                  |
| async_tree_none            | 263 ms                                                                                                          | 256 ms: 1.03x faster                                                                                                  |
| xml_etree_parse            | 134 ms                                                                                                          | 130 ms: 1.03x faster                                                                                                  |
| coroutines                 | 24.5 ms                                                                                                         | 24.1 ms: 1.02x faster                                                                                                 |
| async_tree_memoization     | 313 ms                                                                                                          | 310 ms: 1.01x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 491 ms                                                                                                          | 495 ms: 1.01x slower                                                                                                  |
| regex_effbot               | 2.69 ms                                                                                                         | 2.75 ms: 1.02x slower                                                                                                 |
| pathlib                    | 17.6 ms                                                                                                         | 18.1 ms: 1.03x slower                                                                                                 |
| bpe_tokeniser              | 4.19 sec                                                                                                        | 4.37 sec: 1.04x slower                                                                                                |
| docutils                   | 2.55 sec                                                                                                        | 2.67 sec: 1.05x slower                                                                                                |
| html5lib                   | 62.7 ms                                                                                                         | 66.5 ms: 1.06x slower                                                                                                 |
| tomli_loads                | 1.91 sec                                                                                                        | 2.03 sec: 1.06x slower                                                                                                |
| pycparser                  | 1.07 sec                                                                                                        | 1.14 sec: 1.07x slower                                                                                                |
| scimark_fft                | 320 ms                                                                                                          | 341 ms: 1.07x slower                                                                                                  |
| dulwich_log                | 66.8 ms                                                                                                         | 71.8 ms: 1.07x slower                                                                                                 |
| async_generators           | 341 ms                                                                                                          | 370 ms: 1.09x slower                                                                                                  |
| json                       | 4.95 ms                                                                                                         | 5.40 ms: 1.09x slower                                                                                                 |
| pylint                     | 278 ms                                                                                                          | 306 ms: 1.10x slower                                                                                                  |
| k_core                     | 2.03 sec                                                                                                        | 2.23 sec: 1.10x slower                                                                                                |
| sphinx                     | 974 ms                                                                                                          | 1.07 sec: 1.10x slower                                                                                                |
| sympy_expand               | 467 ms                                                                                                          | 517 ms: 1.11x slower                                                                                                  |
| pickle_pure_python         | 306 us                                                                                                          | 339 us: 1.11x slower                                                                                                  |
| deepcopy_reduce            | 2.63 us                                                                                                         | 2.93 us: 1.11x slower                                                                                                 |
| logging_silent             | 95.5 ns                                                                                                         | 106 ns: 1.11x slower                                                                                                  |
| telco                      | 156 ms                                                                                                          | 175 ms: 1.12x slower                                                                                                  |
| many_optionals             | 1.23 ms                                                                                                         | 1.38 ms: 1.12x slower                                                                                                 |
| pprint_safe_repr           | 690 ms                                                                                                          | 776 ms: 1.12x slower                                                                                                  |
| unpickle_pure_python       | 206 us                                                                                                          | 232 us: 1.13x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.64 ms                                                                                                         | 5.25 ms: 1.13x slower                                                                                                 |
| 2to3                       | 246 ms                                                                                                          | 279 ms: 1.13x slower                                                                                                  |
| spectral_norm              | 97.8 ms                                                                                                         | 111 ms: 1.13x slower                                                                                                  |
| deepcopy                   | 245 us                                                                                                          | 278 us: 1.14x slower                                                                                                  |
| chaos                      | 56.3 ms                                                                                                         | 63.9 ms: 1.14x slower                                                                                                 |
| json_loads                 | 27.8 us                                                                                                         | 31.6 us: 1.14x slower                                                                                                 |
| pprint_pformat             | 1.41 sec                                                                                                        | 1.60 sec: 1.14x slower                                                                                                |
| json_dumps                 | 9.61 ms                                                                                                         | 11.0 ms: 1.14x slower                                                                                                 |
| sympy_str                  | 271 ms                                                                                                          | 309 ms: 1.14x slower                                                                                                  |
| hexiom                     | 5.60 ms                                                                                                         | 6.41 ms: 1.14x slower                                                                                                 |
| deltablue                  | 3.07 ms                                                                                                         | 3.54 ms: 1.15x slower                                                                                                 |
| xml_etree_generate         | 83.1 ms                                                                                                         | 96.0 ms: 1.16x slower                                                                                                 |
| mdp                        | 1.14 sec                                                                                                        | 1.32 sec: 1.16x slower                                                                                                |
| comprehensions             | 15.6 us                                                                                                         | 18.1 us: 1.16x slower                                                                                                 |
| scimark_sor                | 107 ms                                                                                                          | 124 ms: 1.16x slower                                                                                                  |
| regex_compile              | 123 ms                                                                                                          | 143 ms: 1.16x slower                                                                                                  |
| nqueens                    | 76.9 ms                                                                                                         | 89.4 ms: 1.16x slower                                                                                                 |
| sympy_integrate            | 18.8 ms                                                                                                         | 21.9 ms: 1.16x slower                                                                                                 |
| sympy_sum                  | 153 ms                                                                                                          | 178 ms: 1.16x slower                                                                                                  |
| sqlglot_v2_optimize        | 50.0 ms                                                                                                         | 58.3 ms: 1.17x slower                                                                                                 |
| subparsers                 | 44.5 ms                                                                                                         | 52.0 ms: 1.17x slower                                                                                                 |
| pyflate                    | 396 ms                                                                                                          | 463 ms: 1.17x slower                                                                                                  |
| sqlglot_v2_normalize       | 98.8 ms                                                                                                         | 116 ms: 1.17x slower                                                                                                  |
| deepcopy_memo              | 26.5 us                                                                                                         | 31.1 us: 1.17x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.77 ms: 1.18x slower                                                                                                 |
| thrift                     | 741 us                                                                                                          | 872 us: 1.18x slower                                                                                                  |
| go                         | 104 ms                                                                                                          | 123 ms: 1.18x slower                                                                                                  |
| django_template            | 34.5 ms                                                                                                         | 40.8 ms: 1.18x slower                                                                                                 |
| generators                 | 27.6 ms                                                                                                         | 32.7 ms: 1.18x slower                                                                                                 |
| raytrace                   | 252 ms                                                                                                          | 299 ms: 1.19x slower                                                                                                  |
| meteor_contest             | 98.8 ms                                                                                                         | 118 ms: 1.19x slower                                                                                                  |
| scimark_lu                 | 111 ms                                                                                                          | 132 ms: 1.20x slower                                                                                                  |
| genshi_xml                 | 48.1 ms                                                                                                         | 57.7 ms: 1.20x slower                                                                                                 |
| fannkuch                   | 377 ms                                                                                                          | 453 ms: 1.20x slower                                                                                                  |
| xml_etree_process          | 57.7 ms                                                                                                         | 69.3 ms: 1.20x slower                                                                                                 |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.46 ms: 1.20x slower                                                                                                 |
| shortest_path              | 446 ms                                                                                                          | 539 ms: 1.21x slower                                                                                                  |
| logging_simple             | 5.67 us                                                                                                         | 6.87 us: 1.21x slower                                                                                                 |
| connected_components       | 404 ms                                                                                                          | 494 ms: 1.22x slower                                                                                                  |
| logging_format             | 6.41 us                                                                                                         | 7.87 us: 1.23x slower                                                                                                 |
| crypto_pyaes               | 69.2 ms                                                                                                         | 84.9 ms: 1.23x slower                                                                                                 |
| bench_mp_pool              | 12.3 ms                                                                                                         | 15.2 ms: 1.23x slower                                                                                                 |
| typing_runtime_protocols   | 152 us                                                                                                          | 189 us: 1.25x slower                                                                                                  |
| python_startup             | 12.5 ms                                                                                                         | 15.8 ms: 1.26x slower                                                                                                 |
| scimark_monte_carlo        | 61.7 ms                                                                                                         | 78.0 ms: 1.26x slower                                                                                                 |
| richards                   | 40.7 ms                                                                                                         | 51.6 ms: 1.27x slower                                                                                                 |
| richards_super             | 46.6 ms                                                                                                         | 59.4 ms: 1.27x slower                                                                                                 |
| genshi_text                | 20.4 ms                                                                                                         | 26.5 ms: 1.30x slower                                                                                                 |
| python_startup_no_site     | 7.24 ms                                                                                                         | 9.59 ms: 1.32x slower                                                                                                 |
| mako                       | 11.6 ms                                                                                                         | 15.5 ms: 1.34x slower                                                                                                 |
| coverage                   | 81.3 ms                                                                                                         | 111 ms: 1.36x slower                                                                                                  |
| nbody                      | 92.1 ms                                                                                                         | 126 ms: 1.37x slower                                                                                                  |
| bench_thread_pool          | 996 us                                                                                                          | 3.06 ms: 3.07x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.091x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.21x