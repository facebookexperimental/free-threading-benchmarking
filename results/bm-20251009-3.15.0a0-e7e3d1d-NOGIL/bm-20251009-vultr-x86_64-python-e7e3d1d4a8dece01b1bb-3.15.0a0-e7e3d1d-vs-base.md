# Results vs. base

- fork: python
- ref: e7e3d1d4a8dece01b1bb
- machine: linux-x86_64
- commit hash: e7e3d1d
- commit date: 2025-10-09
- overall geometric mean: 1.089x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20251009-3.15.0a0-e7e3d1d/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json | results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 247 ms                                                                                                          | 280 ms: 1.13x slower                                                                                                  |
| docutils       | 2.55 sec                                                                                                        | 2.67 sec: 1.05x slower                                                                                                |
| html5lib       | 61.5 ms                                                                                                         | 68.4 ms: 1.11x slower                                                                                                 |
| sphinx         | 976 ms                                                                                                          | 1.07 sec: 1.09x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20251009-3.15.0a0-e7e3d1d/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json | results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 620 ms                                                                                                          | 515 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 252 ms                                                                                                          | 223 ms: 1.13x faster                                                                                                  |
| async_tree_memoization_tg  | 316 ms                                                                                                          | 280 ms: 1.13x faster                                                                                                  |
| async_tree_io              | 608 ms                                                                                                          | 546 ms: 1.11x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                                                          | 466 ms: 1.06x faster                                                                                                  |
| async_tree_none            | 266 ms                                                                                                          | 258 ms: 1.03x faster                                                                                                  |
| async_tree_memoization     | 315 ms                                                                                                          | 309 ms: 1.02x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 491 ms                                                                                                          | 496 ms: 1.01x slower                                                                                                  |
| coroutines                 | 23.8 ms                                                                                                         | 24.5 ms: 1.03x slower                                                                                                 |
| async_generators           | 342 ms                                                                                                          | 366 ms: 1.07x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x faster                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20251009-3.15.0a0-e7e3d1d/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json | results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 71.6 ms                                                                                                         | 69.2 ms: 1.03x faster                                                                                                 |
| pidigits       | 193 ms                                                                                                          | 198 ms: 1.02x slower                                                                                                  |
| nbody          | 90.5 ms                                                                                                         | 119 ms: 1.32x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20251009-3.15.0a0-e7e3d1d/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json | results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 23.1 ms                                                                                                         | 20.3 ms: 1.14x faster                                                                                                 |
| regex_dna      | 179 ms                                                                                                          | 177 ms: 1.01x faster                                                                                                  |
| regex_effbot   | 2.76 ms                                                                                                         | 2.74 ms: 1.01x faster                                                                                                 |
| regex_compile  | 124 ms                                                                                                          | 144 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.00x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20251009-3.15.0a0-e7e3d1d/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json | results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.8 ms                                                                                                         | 86.7 ms: 1.07x faster                                                                                                 |
| tomli_loads          | 1.89 sec                                                                                                        | 2.03 sec: 1.07x slower                                                                                                |
| pickle_pure_python   | 308 us                                                                                                          | 342 us: 1.11x slower                                                                                                  |
| json_loads           | 28.3 us                                                                                                         | 31.5 us: 1.11x slower                                                                                                 |
| unpickle_pure_python | 209 us                                                                                                          | 234 us: 1.12x slower                                                                                                  |
| json_dumps           | 9.60 ms                                                                                                         | 11.0 ms: 1.15x slower                                                                                                 |
| xml_etree_generate   | 82.7 ms                                                                                                         | 96.1 ms: 1.16x slower                                                                                                 |
| xml_etree_process    | 58.0 ms                                                                                                         | 69.5 ms: 1.20x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20251009-3.15.0a0-e7e3d1d/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json | results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                                                         | 15.7 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 7.25 ms                                                                                                         | 9.57 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20251009-3.15.0a0-e7e3d1d/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json | results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 48.6 ms                                                                                                         | 56.4 ms: 1.16x slower                                                                                                 |
| django_template | 34.5 ms                                                                                                         | 41.4 ms: 1.20x slower                                                                                                 |
| genshi_text     | 20.5 ms                                                                                                         | 26.6 ms: 1.29x slower                                                                                                 |
| mako            | 11.7 ms                                                                                                         | 15.5 ms: 1.32x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.24x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20251009-3.15.0a0-e7e3d1d/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json | results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.41 ms                                                                                                         | 1.95 ms: 2.27x faster                                                                                                 |
| create_gc_cycles           | 1.93 ms                                                                                                         | 1.53 ms: 1.26x faster                                                                                                 |
| async_tree_io_tg           | 620 ms                                                                                                          | 515 ms: 1.20x faster                                                                                                  |
| regex_v8                   | 23.1 ms                                                                                                         | 20.3 ms: 1.14x faster                                                                                                 |
| async_tree_none_tg         | 252 ms                                                                                                          | 223 ms: 1.13x faster                                                                                                  |
| async_tree_memoization_tg  | 316 ms                                                                                                          | 280 ms: 1.13x faster                                                                                                  |
| async_tree_io              | 608 ms                                                                                                          | 546 ms: 1.11x faster                                                                                                  |
| sqlite_synth               | 2.29 us                                                                                                         | 2.08 us: 1.10x faster                                                                                                 |
| xml_etree_iterparse        | 92.8 ms                                                                                                         | 86.7 ms: 1.07x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                                                          | 466 ms: 1.06x faster                                                                                                  |
| float                      | 71.6 ms                                                                                                         | 69.2 ms: 1.03x faster                                                                                                 |
| async_tree_none            | 266 ms                                                                                                          | 258 ms: 1.03x faster                                                                                                  |
| async_tree_memoization     | 315 ms                                                                                                          | 309 ms: 1.02x faster                                                                                                  |
| regex_dna                  | 179 ms                                                                                                          | 177 ms: 1.01x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| regex_effbot               | 2.76 ms                                                                                                         | 2.74 ms: 1.01x faster                                                                                                 |
| pathlib                    | 17.7 ms                                                                                                         | 17.9 ms: 1.01x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 491 ms                                                                                                          | 496 ms: 1.01x slower                                                                                                  |
| pidigits                   | 193 ms                                                                                                          | 198 ms: 1.02x slower                                                                                                  |
| coroutines                 | 23.8 ms                                                                                                         | 24.5 ms: 1.03x slower                                                                                                 |
| bpe_tokeniser              | 4.21 sec                                                                                                        | 4.39 sec: 1.04x slower                                                                                                |
| logging_silent             | 98.3 ns                                                                                                         | 103 ns: 1.04x slower                                                                                                  |
| docutils                   | 2.55 sec                                                                                                        | 2.67 sec: 1.05x slower                                                                                                |
| json                       | 5.09 ms                                                                                                         | 5.37 ms: 1.05x slower                                                                                                 |
| pycparser                  | 1.08 sec                                                                                                        | 1.15 sec: 1.06x slower                                                                                                |
| tomli_loads                | 1.89 sec                                                                                                        | 2.03 sec: 1.07x slower                                                                                                |
| async_generators           | 342 ms                                                                                                          | 366 ms: 1.07x slower                                                                                                  |
| dulwich_log                | 67.6 ms                                                                                                         | 72.3 ms: 1.07x slower                                                                                                 |
| generators                 | 27.9 ms                                                                                                         | 30.1 ms: 1.08x slower                                                                                                 |
| sphinx                     | 976 ms                                                                                                          | 1.07 sec: 1.09x slower                                                                                                |
| pylint                     | 279 ms                                                                                                          | 306 ms: 1.10x slower                                                                                                  |
| scimark_fft                | 314 ms                                                                                                          | 347 ms: 1.10x slower                                                                                                  |
| k_core                     | 2.02 sec                                                                                                        | 2.24 sec: 1.11x slower                                                                                                |
| sympy_expand               | 469 ms                                                                                                          | 519 ms: 1.11x slower                                                                                                  |
| telco                      | 160 ms                                                                                                          | 177 ms: 1.11x slower                                                                                                  |
| pickle_pure_python         | 308 us                                                                                                          | 342 us: 1.11x slower                                                                                                  |
| html5lib                   | 61.5 ms                                                                                                         | 68.4 ms: 1.11x slower                                                                                                 |
| json_loads                 | 28.3 us                                                                                                         | 31.5 us: 1.11x slower                                                                                                 |
| spectral_norm              | 97.5 ms                                                                                                         | 109 ms: 1.12x slower                                                                                                  |
| many_optionals             | 1.24 ms                                                                                                         | 1.38 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python       | 209 us                                                                                                          | 234 us: 1.12x slower                                                                                                  |
| pprint_safe_repr           | 703 ms                                                                                                          | 787 ms: 1.12x slower                                                                                                  |
| scimark_sor                | 110 ms                                                                                                          | 123 ms: 1.13x slower                                                                                                  |
| chaos                      | 56.3 ms                                                                                                         | 63.4 ms: 1.13x slower                                                                                                 |
| pprint_pformat             | 1.43 sec                                                                                                        | 1.62 sec: 1.13x slower                                                                                                |
| 2to3                       | 247 ms                                                                                                          | 280 ms: 1.13x slower                                                                                                  |
| mdp                        | 1.16 sec                                                                                                        | 1.31 sec: 1.13x slower                                                                                                |
| sympy_str                  | 271 ms                                                                                                          | 308 ms: 1.14x slower                                                                                                  |
| deepcopy_reduce            | 2.60 us                                                                                                         | 2.96 us: 1.14x slower                                                                                                 |
| hexiom                     | 5.65 ms                                                                                                         | 6.45 ms: 1.14x slower                                                                                                 |
| nqueens                    | 76.9 ms                                                                                                         | 88.1 ms: 1.15x slower                                                                                                 |
| json_dumps                 | 9.60 ms                                                                                                         | 11.0 ms: 1.15x slower                                                                                                 |
| comprehensions             | 15.6 us                                                                                                         | 18.0 us: 1.15x slower                                                                                                 |
| deepcopy_memo              | 26.6 us                                                                                                         | 30.8 us: 1.16x slower                                                                                                 |
| sympy_sum                  | 153 ms                                                                                                          | 177 ms: 1.16x slower                                                                                                  |
| sqlglot_v2_normalize       | 99.3 ms                                                                                                         | 115 ms: 1.16x slower                                                                                                  |
| sympy_integrate            | 19.0 ms                                                                                                         | 21.9 ms: 1.16x slower                                                                                                 |
| sqlglot_v2_optimize        | 50.2 ms                                                                                                         | 58.1 ms: 1.16x slower                                                                                                 |
| genshi_xml                 | 48.6 ms                                                                                                         | 56.4 ms: 1.16x slower                                                                                                 |
| xml_etree_generate         | 82.7 ms                                                                                                         | 96.1 ms: 1.16x slower                                                                                                 |
| deepcopy                   | 242 us                                                                                                          | 281 us: 1.16x slower                                                                                                  |
| regex_compile              | 124 ms                                                                                                          | 144 ms: 1.16x slower                                                                                                  |
| go                         | 105 ms                                                                                                          | 122 ms: 1.17x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.56 ms                                                                                                         | 5.31 ms: 1.17x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.78 ms: 1.18x slower                                                                                                 |
| subparsers                 | 44.1 ms                                                                                                         | 51.8 ms: 1.18x slower                                                                                                 |
| raytrace                   | 252 ms                                                                                                          | 297 ms: 1.18x slower                                                                                                  |
| scimark_lu                 | 111 ms                                                                                                          | 132 ms: 1.18x slower                                                                                                  |
| pyflate                    | 397 ms                                                                                                          | 471 ms: 1.19x slower                                                                                                  |
| logging_format             | 6.52 us                                                                                                         | 7.75 us: 1.19x slower                                                                                                 |
| xml_etree_process          | 58.0 ms                                                                                                         | 69.5 ms: 1.20x slower                                                                                                 |
| logging_simple             | 5.68 us                                                                                                         | 6.80 us: 1.20x slower                                                                                                 |
| django_template            | 34.5 ms                                                                                                         | 41.4 ms: 1.20x slower                                                                                                 |
| fannkuch                   | 379 ms                                                                                                          | 456 ms: 1.20x slower                                                                                                  |
| thrift                     | 739 us                                                                                                          | 887 us: 1.20x slower                                                                                                  |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.46 ms: 1.21x slower                                                                                                 |
| shortest_path              | 444 ms                                                                                                          | 537 ms: 1.21x slower                                                                                                  |
| meteor_contest             | 98.8 ms                                                                                                         | 120 ms: 1.21x slower                                                                                                  |
| bench_mp_pool              | 12.4 ms                                                                                                         | 15.0 ms: 1.21x slower                                                                                                 |
| deltablue                  | 3.08 ms                                                                                                         | 3.76 ms: 1.22x slower                                                                                                 |
| connected_components       | 401 ms                                                                                                          | 494 ms: 1.23x slower                                                                                                  |
| crypto_pyaes               | 69.3 ms                                                                                                         | 86.1 ms: 1.24x slower                                                                                                 |
| richards                   | 41.4 ms                                                                                                         | 51.7 ms: 1.25x slower                                                                                                 |
| python_startup             | 12.5 ms                                                                                                         | 15.7 ms: 1.25x slower                                                                                                 |
| typing_runtime_protocols   | 151 us                                                                                                          | 189 us: 1.26x slower                                                                                                  |
| scimark_monte_carlo        | 61.9 ms                                                                                                         | 78.3 ms: 1.27x slower                                                                                                 |
| richards_super             | 47.1 ms                                                                                                         | 59.6 ms: 1.27x slower                                                                                                 |
| genshi_text                | 20.5 ms                                                                                                         | 26.6 ms: 1.29x slower                                                                                                 |
| python_startup_no_site     | 7.25 ms                                                                                                         | 9.57 ms: 1.32x slower                                                                                                 |
| nbody                      | 90.5 ms                                                                                                         | 119 ms: 1.32x slower                                                                                                  |
| mako                       | 11.7 ms                                                                                                         | 15.5 ms: 1.32x slower                                                                                                 |
| coverage                   | 83.2 ms                                                                                                         | 111 ms: 1.34x slower                                                                                                  |
| bench_thread_pool          | 998 us                                                                                                          | 3.05 ms: 3.05x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

- Geometric mean (including insignificant results): 1.089x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x