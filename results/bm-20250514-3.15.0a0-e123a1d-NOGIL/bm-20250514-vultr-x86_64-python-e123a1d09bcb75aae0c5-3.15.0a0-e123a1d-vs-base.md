# Results vs. base

- fork: python
- ref: e123a1d09bcb75aae0c5
- machine: linux-x86_64
- commit hash: e123a1d
- commit date: 2025-05-14
- overall geometric mean: 1.090x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                          | 285 ms: 1.14x slower                                                                                                  |
| docutils       | 2.52 sec                                                                                                        | 2.70 sec: 1.07x slower                                                                                                |
| html5lib       | 61.2 ms                                                                                                         | 65.8 ms: 1.08x slower                                                                                                 |
| sphinx         | 975 ms                                                                                                          | 1.07 sec: 1.10x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 627 ms                                                                                                          | 521 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 255 ms                                                                                                          | 227 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 601 ms                                                                                                          | 550 ms: 1.09x faster                                                                                                  |
| async_tree_memoization_tg  | 310 ms                                                                                                          | 284 ms: 1.09x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 506 ms                                                                                                          | 480 ms: 1.05x faster                                                                                                  |
| async_tree_none            | 272 ms                                                                                                          | 261 ms: 1.04x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 515 ms                                                                                                          | 510 ms: 1.01x faster                                                                                                  |
| coroutines                 | 23.1 ms                                                                                                         | 23.0 ms: 1.00x faster                                                                                                 |
| async_generators           | 335 ms                                                                                                          | 371 ms: 1.11x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 205 ms                                                                                                          | 199 ms: 1.03x faster                                                                                                  |
| float          | 71.7 ms                                                                                                         | 70.0 ms: 1.02x faster                                                                                                 |
| nbody          | 91.1 ms                                                                                                         | 120 ms: 1.32x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.8 ms                                                                                                         | 21.0 ms: 1.04x faster                                                                                                 |
| regex_effbot   | 2.84 ms                                                                                                         | 2.77 ms: 1.02x faster                                                                                                 |
| regex_dna      | 181 ms                                                                                                          | 177 ms: 1.02x faster                                                                                                  |
| regex_compile  | 124 ms                                                                                                          | 145 ms: 1.17x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.02x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.6 ms                                                                                                         | 88.3 ms: 1.04x faster                                                                                                 |
| json_loads           | 28.7 us                                                                                                         | 30.6 us: 1.07x slower                                                                                                 |
| json_dumps           | 10.7 ms                                                                                                         | 11.6 ms: 1.08x slower                                                                                                 |
| pickle_pure_python   | 305 us                                                                                                          | 334 us: 1.10x slower                                                                                                  |
| unpickle_pure_python | 208 us                                                                                                          | 229 us: 1.10x slower                                                                                                  |
| xml_etree_generate   | 82.9 ms                                                                                                         | 95.4 ms: 1.15x slower                                                                                                 |
| tomli_loads          | 1.86 sec                                                                                                        | 2.15 sec: 1.16x slower                                                                                                |
| xml_etree_process    | 58.0 ms                                                                                                         | 68.6 ms: 1.18x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 16.0 ms: 1.27x slower                                                                                                 |
| python_startup_no_site | 7.31 ms                                                                                                         | 9.57 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 47.6 ms                                                                                                         | 55.8 ms: 1.17x slower                                                                                                 |
| django_template | 33.8 ms                                                                                                         | 40.5 ms: 1.20x slower                                                                                                 |
| genshi_text     | 20.0 ms                                                                                                         | 26.2 ms: 1.31x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 15.6 ms: 1.32x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.25x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250514-3.15.0a0-e123a1d/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json | results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.57 ms                                                                                                         | 1.89 ms: 2.42x faster                                                                                                 |
| create_gc_cycles           | 1.94 ms                                                                                                         | 1.46 ms: 1.33x faster                                                                                                 |
| async_tree_io_tg           | 627 ms                                                                                                          | 521 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 255 ms                                                                                                          | 227 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 601 ms                                                                                                          | 550 ms: 1.09x faster                                                                                                  |
| async_tree_memoization_tg  | 310 ms                                                                                                          | 284 ms: 1.09x faster                                                                                                  |
| sqlite_synth               | 2.24 us                                                                                                         | 2.07 us: 1.08x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 506 ms                                                                                                          | 480 ms: 1.05x faster                                                                                                  |
| async_tree_none            | 272 ms                                                                                                          | 261 ms: 1.04x faster                                                                                                  |
| regex_v8                   | 21.8 ms                                                                                                         | 21.0 ms: 1.04x faster                                                                                                 |
| xml_etree_iterparse        | 91.6 ms                                                                                                         | 88.3 ms: 1.04x faster                                                                                                 |
| pidigits                   | 205 ms                                                                                                          | 199 ms: 1.03x faster                                                                                                  |
| regex_effbot               | 2.84 ms                                                                                                         | 2.77 ms: 1.02x faster                                                                                                 |
| float                      | 71.7 ms                                                                                                         | 70.0 ms: 1.02x faster                                                                                                 |
| regex_dna                  | 181 ms                                                                                                          | 177 ms: 1.02x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 515 ms                                                                                                          | 510 ms: 1.01x faster                                                                                                  |
| coroutines                 | 23.1 ms                                                                                                         | 23.0 ms: 1.00x faster                                                                                                 |
| pycparser                  | 1.10 sec                                                                                                        | 1.13 sec: 1.03x slower                                                                                                |
| generators                 | 27.8 ms                                                                                                         | 28.9 ms: 1.04x slower                                                                                                 |
| dulwich_log                | 67.7 ms                                                                                                         | 71.0 ms: 1.05x slower                                                                                                 |
| bench_mp_pool              | 98.4 ms                                                                                                         | 103 ms: 1.05x slower                                                                                                  |
| json_loads                 | 28.7 us                                                                                                         | 30.6 us: 1.07x slower                                                                                                 |
| docutils                   | 2.52 sec                                                                                                        | 2.70 sec: 1.07x slower                                                                                                |
| html5lib                   | 61.2 ms                                                                                                         | 65.8 ms: 1.08x slower                                                                                                 |
| bpe_tokeniser              | 4.11 sec                                                                                                        | 4.43 sec: 1.08x slower                                                                                                |
| json_dumps                 | 10.7 ms                                                                                                         | 11.6 ms: 1.08x slower                                                                                                 |
| many_optionals             | 1.05 ms                                                                                                         | 1.15 ms: 1.09x slower                                                                                                 |
| pylint                     | 279 ms                                                                                                          | 304 ms: 1.09x slower                                                                                                  |
| pickle_pure_python         | 305 us                                                                                                          | 334 us: 1.10x slower                                                                                                  |
| deltablue                  | 3.21 ms                                                                                                         | 3.53 ms: 1.10x slower                                                                                                 |
| unpickle_pure_python       | 208 us                                                                                                          | 229 us: 1.10x slower                                                                                                  |
| scimark_sor                | 110 ms                                                                                                          | 122 ms: 1.10x slower                                                                                                  |
| sphinx                     | 975 ms                                                                                                          | 1.07 sec: 1.10x slower                                                                                                |
| k_core                     | 2.03 sec                                                                                                        | 2.25 sec: 1.10x slower                                                                                                |
| async_generators           | 335 ms                                                                                                          | 371 ms: 1.11x slower                                                                                                  |
| pprint_safe_repr           | 698 ms                                                                                                          | 776 ms: 1.11x slower                                                                                                  |
| scimark_fft                | 328 ms                                                                                                          | 365 ms: 1.11x slower                                                                                                  |
| subparsers                 | 25.4 ms                                                                                                         | 28.4 ms: 1.12x slower                                                                                                 |
| chaos                      | 55.2 ms                                                                                                         | 62.1 ms: 1.13x slower                                                                                                 |
| spectral_norm              | 95.9 ms                                                                                                         | 109 ms: 1.13x slower                                                                                                  |
| thrift                     | 755 us                                                                                                          | 858 us: 1.14x slower                                                                                                  |
| pprint_pformat             | 1.42 sec                                                                                                        | 1.61 sec: 1.14x slower                                                                                                |
| deepcopy_reduce            | 2.61 us                                                                                                         | 2.99 us: 1.14x slower                                                                                                 |
| 2to3                       | 249 ms                                                                                                          | 285 ms: 1.14x slower                                                                                                  |
| nqueens                    | 76.5 ms                                                                                                         | 87.6 ms: 1.14x slower                                                                                                 |
| xml_etree_generate         | 82.9 ms                                                                                                         | 95.4 ms: 1.15x slower                                                                                                 |
| scimark_lu                 | 110 ms                                                                                                          | 126 ms: 1.15x slower                                                                                                  |
| tomli_loads                | 1.86 sec                                                                                                        | 2.15 sec: 1.16x slower                                                                                                |
| sqlglot_v2_optimize        | 49.3 ms                                                                                                         | 57.1 ms: 1.16x slower                                                                                                 |
| go                         | 106 ms                                                                                                          | 123 ms: 1.16x slower                                                                                                  |
| logging_silent             | 463 ns                                                                                                          | 539 ns: 1.16x slower                                                                                                  |
| hexiom                     | 5.65 ms                                                                                                         | 6.58 ms: 1.17x slower                                                                                                 |
| mdp                        | 1.14 sec                                                                                                        | 1.33 sec: 1.17x slower                                                                                                |
| sympy_sum                  | 153 ms                                                                                                          | 178 ms: 1.17x slower                                                                                                  |
| raytrace                   | 251 ms                                                                                                          | 294 ms: 1.17x slower                                                                                                  |
| logging_format             | 7.49 us                                                                                                         | 8.77 us: 1.17x slower                                                                                                 |
| regex_compile              | 124 ms                                                                                                          | 145 ms: 1.17x slower                                                                                                  |
| logging_simple             | 6.56 us                                                                                                         | 7.69 us: 1.17x slower                                                                                                 |
| sqlglot_v2_normalize       | 97.6 ms                                                                                                         | 114 ms: 1.17x slower                                                                                                  |
| genshi_xml                 | 47.6 ms                                                                                                         | 55.8 ms: 1.17x slower                                                                                                 |
| comprehensions             | 16.3 us                                                                                                         | 19.3 us: 1.18x slower                                                                                                 |
| sympy_integrate            | 18.8 ms                                                                                                         | 22.2 ms: 1.18x slower                                                                                                 |
| deepcopy                   | 247 us                                                                                                          | 292 us: 1.18x slower                                                                                                  |
| xml_etree_process          | 58.0 ms                                                                                                         | 68.6 ms: 1.18x slower                                                                                                 |
| sympy_expand               | 449 ms                                                                                                          | 532 ms: 1.18x slower                                                                                                  |
| sympy_str                  | 266 ms                                                                                                          | 317 ms: 1.19x slower                                                                                                  |
| django_template            | 33.8 ms                                                                                                         | 40.5 ms: 1.20x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.50 ms                                                                                                         | 1.80 ms: 1.20x slower                                                                                                 |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.45 ms: 1.20x slower                                                                                                 |
| telco                      | 7.33 ms                                                                                                         | 8.80 ms: 1.20x slower                                                                                                 |
| pyflate                    | 398 ms                                                                                                          | 486 ms: 1.22x slower                                                                                                  |
| shortest_path              | 434 ms                                                                                                          | 530 ms: 1.22x slower                                                                                                  |
| connected_components       | 393 ms                                                                                                          | 480 ms: 1.22x slower                                                                                                  |
| scimark_monte_carlo        | 62.5 ms                                                                                                         | 76.7 ms: 1.23x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.40 ms                                                                                                         | 5.42 ms: 1.23x slower                                                                                                 |
| fannkuch                   | 386 ms                                                                                                          | 475 ms: 1.23x slower                                                                                                  |
| crypto_pyaes               | 69.2 ms                                                                                                         | 85.4 ms: 1.23x slower                                                                                                 |
| deepcopy_memo              | 28.4 us                                                                                                         | 35.5 us: 1.25x slower                                                                                                 |
| richards_super             | 46.1 ms                                                                                                         | 57.7 ms: 1.25x slower                                                                                                 |
| meteor_contest             | 101 ms                                                                                                          | 127 ms: 1.26x slower                                                                                                  |
| typing_runtime_protocols   | 157 us                                                                                                          | 197 us: 1.26x slower                                                                                                  |
| richards                   | 40.2 ms                                                                                                         | 50.5 ms: 1.26x slower                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 16.0 ms: 1.27x slower                                                                                                 |
| python_startup_no_site     | 7.31 ms                                                                                                         | 9.57 ms: 1.31x slower                                                                                                 |
| genshi_text                | 20.0 ms                                                                                                         | 26.2 ms: 1.31x slower                                                                                                 |
| nbody                      | 91.1 ms                                                                                                         | 120 ms: 1.32x slower                                                                                                  |
| mako                       | 11.8 ms                                                                                                         | 15.6 ms: 1.32x slower                                                                                                 |
| coverage                   | 81.0 ms                                                                                                         | 109 ms: 1.34x slower                                                                                                  |
| bench_thread_pool          | 1.05 ms                                                                                                         | 3.13 ms: 2.99x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmark hidden because not significant (5): pathlib, xml_etree_parse, asyncio_websockets, json, async_tree_memoization

- Geometric mean (including insignificant results): 1.090x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.22x