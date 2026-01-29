# Results vs. base

- fork: DinoV
- ref: lazy_review_updates2
- machine: linux-x86_64
- commit hash: 8fd3f20
- commit date: 2026-01-27
- overall geometric mean: 1.105x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 281 ms: 1.13x slower                                                  |
| docutils       | 2.57 sec                                                               | 2.74 sec: 1.07x slower                                                |
| html5lib       | 59.2 ms                                                                | 63.5 ms: 1.07x slower                                                 |
| sphinx         | 964 ms                                                                 | 1.07 sec: 1.11x slower                                                |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets         | 544 ms                                                                 | 546 ms: 1.00x slower                                                  |
| coroutines                 | 24.4 ms                                                                | 25.5 ms: 1.04x slower                                                 |
| async_tree_memoization     | 306 ms                                                                 | 323 ms: 1.06x slower                                                  |
| async_tree_memoization_tg  | 305 ms                                                                 | 322 ms: 1.06x slower                                                  |
| async_tree_io_tg           | 587 ms                                                                 | 627 ms: 1.07x slower                                                  |
| async_tree_none            | 243 ms                                                                 | 266 ms: 1.09x slower                                                  |
| async_generators           | 338 ms                                                                 | 378 ms: 1.12x slower                                                  |
| async_tree_none_tg         | 243 ms                                                                 | 272 ms: 1.12x slower                                                  |
| async_tree_io              | 554 ms                                                                 | 642 ms: 1.16x slower                                                  |
| async_tree_cpu_io_mixed    | 477 ms                                                                 | 560 ms: 1.17x slower                                                  |
| async_tree_cpu_io_mixed_tg | 478 ms                                                                 | 563 ms: 1.18x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 197 ms                                                                 | 190 ms: 1.03x faster                                                  |
| float          | 71.1 ms                                                                | 76.5 ms: 1.08x slower                                                 |
| nbody          | 91.4 ms                                                                | 105 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.91 ms                                                                | 2.70 ms: 1.08x faster                                                 |
| regex_dna      | 180 ms                                                                 | 177 ms: 1.02x faster                                                  |
| regex_compile  | 124 ms                                                                 | 140 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_loads           | 28.2 us                                                                | 29.8 us: 1.06x slower                                                 |
| tomli_loads          | 1.86 sec                                                               | 2.05 sec: 1.10x slower                                                |
| xml_etree_parse      | 131 ms                                                                 | 146 ms: 1.12x slower                                                  |
| xml_etree_iterparse  | 84.9 ms                                                                | 94.9 ms: 1.12x slower                                                 |
| pickle_pure_python   | 310 us                                                                 | 348 us: 1.12x slower                                                  |
| unpickle_pure_python | 213 us                                                                 | 240 us: 1.13x slower                                                  |
| json_dumps           | 9.58 ms                                                                | 11.3 ms: 1.18x slower                                                 |
| xml_etree_generate   | 82.6 ms                                                                | 101 ms: 1.23x slower                                                  |
| xml_etree_process    | 58.2 ms                                                                | 71.4 ms: 1.23x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.28 ms                                                                | 7.81 ms: 1.07x slower                                                 |
| python_startup         | 12.4 ms                                                                | 13.5 ms: 1.09x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 12.1 ms                                                                | 13.5 ms: 1.12x slower                                                 |
| genshi_xml      | 49.7 ms                                                                | 56.9 ms: 1.15x slower                                                 |
| genshi_text     | 21.6 ms                                                                | 25.1 ms: 1.16x slower                                                 |
| django_template | 35.6 ms                                                                | 42.2 ms: 1.19x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.15x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5+-c461aa9 | bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5+-8fd3f20 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| bench_mp_pool              | 283 ms                                                                 | 194 ms: 1.46x faster                                                  |
| regex_effbot               | 2.91 ms                                                                | 2.70 ms: 1.08x faster                                                 |
| pidigits                   | 197 ms                                                                 | 190 ms: 1.03x faster                                                  |
| regex_dna                  | 180 ms                                                                 | 177 ms: 1.02x faster                                                  |
| asyncio_websockets         | 544 ms                                                                 | 546 ms: 1.00x slower                                                  |
| shortest_path              | 436 ms                                                                 | 441 ms: 1.01x slower                                                  |
| connected_components       | 389 ms                                                                 | 399 ms: 1.03x slower                                                  |
| k_core                     | 1.89 sec                                                               | 1.95 sec: 1.03x slower                                                |
| coroutines                 | 24.4 ms                                                                | 25.5 ms: 1.04x slower                                                 |
| deepcopy_memo              | 26.9 us                                                                | 28.2 us: 1.05x slower                                                 |
| go                         | 105 ms                                                                 | 111 ms: 1.05x slower                                                  |
| async_tree_memoization     | 306 ms                                                                 | 323 ms: 1.06x slower                                                  |
| async_tree_memoization_tg  | 305 ms                                                                 | 322 ms: 1.06x slower                                                  |
| json_loads                 | 28.2 us                                                                | 29.8 us: 1.06x slower                                                 |
| async_tree_io_tg           | 587 ms                                                                 | 627 ms: 1.07x slower                                                  |
| docutils                   | 2.57 sec                                                               | 2.74 sec: 1.07x slower                                                |
| python_startup_no_site     | 7.28 ms                                                                | 7.81 ms: 1.07x slower                                                 |
| html5lib                   | 59.2 ms                                                                | 63.5 ms: 1.07x slower                                                 |
| generators                 | 28.0 ms                                                                | 30.1 ms: 1.08x slower                                                 |
| float                      | 71.1 ms                                                                | 76.5 ms: 1.08x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 109 ms: 1.08x slower                                                  |
| pyflate                    | 409 ms                                                                 | 442 ms: 1.08x slower                                                  |
| json                       | 5.04 ms                                                                | 5.46 ms: 1.08x slower                                                 |
| python_startup             | 12.4 ms                                                                | 13.5 ms: 1.09x slower                                                 |
| bench_thread_pool          | 1.31 ms                                                                | 1.42 ms: 1.09x slower                                                 |
| pylint                     | 285 ms                                                                 | 310 ms: 1.09x slower                                                  |
| logging_silent             | 101 ns                                                                 | 110 ns: 1.09x slower                                                  |
| gc_traversal               | 4.00 ms                                                                | 4.36 ms: 1.09x slower                                                 |
| sympy_expand               | 491 ms                                                                 | 536 ms: 1.09x slower                                                  |
| sympy_integrate            | 19.2 ms                                                                | 21.0 ms: 1.09x slower                                                 |
| async_tree_none            | 243 ms                                                                 | 266 ms: 1.09x slower                                                  |
| dulwich_log                | 67.6 ms                                                                | 74.0 ms: 1.09x slower                                                 |
| create_gc_cycles           | 1.86 ms                                                                | 2.04 ms: 1.10x slower                                                 |
| sympy_sum                  | 156 ms                                                                 | 172 ms: 1.10x slower                                                  |
| comprehensions             | 16.0 us                                                                | 17.6 us: 1.10x slower                                                 |
| many_optionals             | 949 us                                                                 | 1.04 ms: 1.10x slower                                                 |
| tomli_loads                | 1.86 sec                                                               | 2.05 sec: 1.10x slower                                                |
| deltablue                  | 3.32 ms                                                                | 3.67 ms: 1.11x slower                                                 |
| sphinx                     | 964 ms                                                                 | 1.07 sec: 1.11x slower                                                |
| pycparser                  | 1.09 sec                                                               | 1.22 sec: 1.11x slower                                                |
| hexiom                     | 5.65 ms                                                                | 6.28 ms: 1.11x slower                                                 |
| sqlglot_v2_transpile       | 1.53 ms                                                                | 1.70 ms: 1.11x slower                                                 |
| sqlglot_v2_parse           | 1.22 ms                                                                | 1.36 ms: 1.12x slower                                                 |
| async_generators           | 338 ms                                                                 | 378 ms: 1.12x slower                                                  |
| xml_etree_parse            | 131 ms                                                                 | 146 ms: 1.12x slower                                                  |
| async_tree_none_tg         | 243 ms                                                                 | 272 ms: 1.12x slower                                                  |
| xml_etree_iterparse        | 84.9 ms                                                                | 94.9 ms: 1.12x slower                                                 |
| sympy_str                  | 280 ms                                                                 | 314 ms: 1.12x slower                                                  |
| pathlib                    | 17.6 ms                                                                | 19.8 ms: 1.12x slower                                                 |
| pickle_pure_python         | 310 us                                                                 | 348 us: 1.12x slower                                                  |
| mako                       | 12.1 ms                                                                | 13.5 ms: 1.12x slower                                                 |
| unpickle_pure_python       | 213 us                                                                 | 240 us: 1.13x slower                                                  |
| spectral_norm              | 96.0 ms                                                                | 108 ms: 1.13x slower                                                  |
| scimark_lu                 | 109 ms                                                                 | 123 ms: 1.13x slower                                                  |
| 2to3                       | 249 ms                                                                 | 281 ms: 1.13x slower                                                  |
| regex_compile              | 124 ms                                                                 | 140 ms: 1.13x slower                                                  |
| deepcopy                   | 238 us                                                                 | 270 us: 1.14x slower                                                  |
| crypto_pyaes               | 69.7 ms                                                                | 79.3 ms: 1.14x slower                                                 |
| scimark_monte_carlo        | 62.2 ms                                                                | 70.9 ms: 1.14x slower                                                 |
| genshi_xml                 | 49.7 ms                                                                | 56.9 ms: 1.15x slower                                                 |
| sqlglot_v2_optimize        | 51.7 ms                                                                | 59.4 ms: 1.15x slower                                                 |
| subparsers                 | 9.28 ms                                                                | 10.7 ms: 1.15x slower                                                 |
| nbody                      | 91.4 ms                                                                | 105 ms: 1.15x slower                                                  |
| coverage                   | 81.5 ms                                                                | 94.0 ms: 1.15x slower                                                 |
| async_tree_io              | 554 ms                                                                 | 642 ms: 1.16x slower                                                  |
| genshi_text                | 21.6 ms                                                                | 25.1 ms: 1.16x slower                                                 |
| nqueens                    | 79.2 ms                                                                | 92.3 ms: 1.16x slower                                                 |
| mdp                        | 1.16 sec                                                               | 1.36 sec: 1.16x slower                                                |
| richards_super             | 48.8 ms                                                                | 56.8 ms: 1.17x slower                                                 |
| chaos                      | 55.9 ms                                                                | 65.2 ms: 1.17x slower                                                 |
| scimark_sparse_mat_mult    | 4.37 ms                                                                | 5.12 ms: 1.17x slower                                                 |
| scimark_sor                | 106 ms                                                                 | 124 ms: 1.17x slower                                                  |
| async_tree_cpu_io_mixed    | 477 ms                                                                 | 560 ms: 1.17x slower                                                  |
| logging_simple             | 5.92 us                                                                | 6.96 us: 1.17x slower                                                 |
| raytrace                   | 253 ms                                                                 | 298 ms: 1.18x slower                                                  |
| async_tree_cpu_io_mixed_tg | 478 ms                                                                 | 563 ms: 1.18x slower                                                  |
| json_dumps                 | 9.58 ms                                                                | 11.3 ms: 1.18x slower                                                 |
| deepcopy_reduce            | 2.59 us                                                                | 3.05 us: 1.18x slower                                                 |
| fannkuch                   | 388 ms                                                                 | 458 ms: 1.18x slower                                                  |
| sqlglot_v2_normalize       | 102 ms                                                                 | 120 ms: 1.18x slower                                                  |
| bpe_tokeniser              | 4.21 sec                                                               | 4.97 sec: 1.18x slower                                                |
| pprint_pformat             | 1.43 sec                                                               | 1.69 sec: 1.18x slower                                                |
| typing_runtime_protocols   | 158 us                                                                 | 187 us: 1.18x slower                                                  |
| richards                   | 42.8 ms                                                                | 50.7 ms: 1.18x slower                                                 |
| django_template            | 35.6 ms                                                                | 42.2 ms: 1.19x slower                                                 |
| pprint_safe_repr           | 702 ms                                                                 | 836 ms: 1.19x slower                                                  |
| telco                      | 160 ms                                                                 | 190 ms: 1.19x slower                                                  |
| thrift                     | 768 us                                                                 | 921 us: 1.20x slower                                                  |
| xml_etree_generate         | 82.6 ms                                                                | 101 ms: 1.23x slower                                                  |
| scimark_fft                | 305 ms                                                                 | 374 ms: 1.23x slower                                                  |
| xml_etree_process          | 58.2 ms                                                                | 71.4 ms: 1.23x slower                                                 |
| sqlite_synth               | 2.28 us                                                                | 2.81 us: 1.23x slower                                                 |
| logging_format             | 6.59 us                                                                | 8.23 us: 1.25x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.11x slower                                                          |

Benchmark hidden because not significant (1): regex_v8

- Geometric mean (including insignificant results): 1.105x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.02x