# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: ccaa69a
- commit date: 2025-04-02
- overall geometric mean: 1.110x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 443 ms                                                                 | 516 ms: 1.16x slower                                                  |
| docutils       | 3.57 sec                                                               | 4.30 sec: 1.21x slower                                                |
| sphinx         | 1.42 sec                                                               | 1.61 sec: 1.14x slower                                                |
| Geometric mean | (ref)                                                                  | 1.17x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 880 ms                                                                 | 746 ms: 1.18x faster                                                  |
| async_tree_io              | 873 ms                                                                 | 776 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 351 ms                                                                 | 320 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 664 ms                                                                 | 643 ms: 1.03x faster                                                  |
| async_generators           | 529 ms                                                                 | 579 ms: 1.09x slower                                                  |
| async_tree_none            | 365 ms                                                                 | 404 ms: 1.11x slower                                                  |
| async_tree_memoization     | 449 ms                                                                 | 513 ms: 1.14x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (4): async_tree_memoization_tg, asyncio_websockets, async_tree_cpu_io_mixed, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 92.9 ms                                                                | 89.0 ms: 1.04x faster                                                 |
| pidigits       | 242 ms                                                                 | 273 ms: 1.13x slower                                                  |
| nbody          | 118 ms                                                                 | 158 ms: 1.34x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 162 ms                                                                 | 222 ms: 1.37x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (3): regex_effbot, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 164 ms                                                                 | 139 ms: 1.18x faster                                                  |
| xml_etree_parse      | 238 ms                                                                 | 210 ms: 1.13x faster                                                  |
| json_loads           | 41.7 us                                                                | 45.4 us: 1.09x slower                                                 |
| pickle_pure_python   | 421 us                                                                 | 483 us: 1.15x slower                                                  |
| xml_etree_process    | 81.8 ms                                                                | 94.4 ms: 1.15x slower                                                 |
| tomli_loads          | 2.49 sec                                                               | 2.92 sec: 1.17x slower                                                |
| unpickle_pure_python | 272 us                                                                 | 322 us: 1.18x slower                                                  |
| json_dumps           | 15.1 ms                                                                | 18.1 ms: 1.20x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 29.4 ms                                                                | 33.4 ms: 1.14x slower                                                 |
| python_startup_no_site | 16.7 ms                                                                | 24.8 ms: 1.48x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.30x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 29.1 ms                                                                | 34.6 ms: 1.19x slower                                                 |
| django_template | 45.4 ms                                                                | 59.6 ms: 1.31x slower                                                 |
| mako            | 17.3 ms                                                                | 23.4 ms: 1.35x slower                                                 |
| genshi_xml      | 61.9 ms                                                                | 84.5 ms: 1.36x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250402-linux-x86_64-python-6bd96894269be4754a81-3.14.0a6+-6bd9689 | bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 7.84 ms                                                                | 4.07 ms: 1.93x faster                                                 |
| create_gc_cycles           | 3.34 ms                                                                | 2.70 ms: 1.23x faster                                                 |
| async_tree_io_tg           | 880 ms                                                                 | 746 ms: 1.18x faster                                                  |
| xml_etree_iterparse        | 164 ms                                                                 | 139 ms: 1.18x faster                                                  |
| xml_etree_parse            | 238 ms                                                                 | 210 ms: 1.13x faster                                                  |
| async_tree_io              | 873 ms                                                                 | 776 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 351 ms                                                                 | 320 ms: 1.10x faster                                                  |
| sqlite_synth               | 3.72 us                                                                | 3.56 us: 1.05x faster                                                 |
| float                      | 92.9 ms                                                                | 89.0 ms: 1.04x faster                                                 |
| async_tree_cpu_io_mixed_tg | 664 ms                                                                 | 643 ms: 1.03x faster                                                  |
| pycparser                  | 1.52 sec                                                               | 1.63 sec: 1.07x slower                                                |
| richards                   | 61.5 ms                                                                | 66.3 ms: 1.08x slower                                                 |
| typing_runtime_protocols   | 249 us                                                                 | 270 us: 1.08x slower                                                  |
| json_loads                 | 41.7 us                                                                | 45.4 us: 1.09x slower                                                 |
| logging_silent             | 129 ns                                                                 | 141 ns: 1.09x slower                                                  |
| async_generators           | 529 ms                                                                 | 579 ms: 1.09x slower                                                  |
| nqueens                    | 111 ms                                                                 | 122 ms: 1.10x slower                                                  |
| async_tree_none            | 365 ms                                                                 | 404 ms: 1.11x slower                                                  |
| scimark_fft                | 454 ms                                                                 | 504 ms: 1.11x slower                                                  |
| sqlglot_v2_optimize        | 72.1 ms                                                                | 80.4 ms: 1.11x slower                                                 |
| bench_mp_pool              | 88.1 ms                                                                | 98.5 ms: 1.12x slower                                                 |
| spectral_norm              | 134 ms                                                                 | 151 ms: 1.13x slower                                                  |
| pidigits                   | 242 ms                                                                 | 273 ms: 1.13x slower                                                  |
| pprint_safe_repr           | 924 ms                                                                 | 1.04 sec: 1.13x slower                                                |
| k_core                     | 3.95 sec                                                               | 4.47 sec: 1.13x slower                                                |
| scimark_sor                | 151 ms                                                                 | 172 ms: 1.13x slower                                                  |
| python_startup             | 29.4 ms                                                                | 33.4 ms: 1.14x slower                                                 |
| sphinx                     | 1.42 sec                                                               | 1.61 sec: 1.14x slower                                                |
| async_tree_memoization     | 449 ms                                                                 | 513 ms: 1.14x slower                                                  |
| sympy_str                  | 378 ms                                                                 | 433 ms: 1.14x slower                                                  |
| scimark_lu                 | 160 ms                                                                 | 183 ms: 1.14x slower                                                  |
| pickle_pure_python         | 421 us                                                                 | 483 us: 1.15x slower                                                  |
| generators                 | 41.6 ms                                                                | 47.7 ms: 1.15x slower                                                 |
| hexiom                     | 8.32 ms                                                                | 9.53 ms: 1.15x slower                                                 |
| xml_etree_process          | 81.8 ms                                                                | 94.4 ms: 1.15x slower                                                 |
| many_optionals             | 1.27 ms                                                                | 1.47 ms: 1.16x slower                                                 |
| 2to3                       | 443 ms                                                                 | 516 ms: 1.16x slower                                                  |
| sympy_sum                  | 217 ms                                                                 | 253 ms: 1.17x slower                                                  |
| sqlalchemy_imperative      | 26.4 ms                                                                | 30.9 ms: 1.17x slower                                                 |
| dulwich_log                | 84.2 ms                                                                | 98.7 ms: 1.17x slower                                                 |
| tomli_loads                | 2.49 sec                                                               | 2.92 sec: 1.17x slower                                                |
| sympy_expand               | 601 ms                                                                 | 709 ms: 1.18x slower                                                  |
| unpickle_pure_python       | 272 us                                                                 | 322 us: 1.18x slower                                                  |
| sqlglot_v2_parse           | 1.66 ms                                                                | 1.97 ms: 1.19x slower                                                 |
| pyflate                    | 595 ms                                                                 | 706 ms: 1.19x slower                                                  |
| pylint                     | 393 ms                                                                 | 467 ms: 1.19x slower                                                  |
| sympy_integrate            | 29.0 ms                                                                | 34.5 ms: 1.19x slower                                                 |
| genshi_text                | 29.1 ms                                                                | 34.6 ms: 1.19x slower                                                 |
| sqlglot_v2_transpile       | 2.14 ms                                                                | 2.55 ms: 1.19x slower                                                 |
| richards_super             | 65.7 ms                                                                | 78.7 ms: 1.20x slower                                                 |
| pprint_pformat             | 1.84 sec                                                               | 2.21 sec: 1.20x slower                                                |
| fannkuch                   | 528 ms                                                                 | 634 ms: 1.20x slower                                                  |
| json_dumps                 | 15.1 ms                                                                | 18.1 ms: 1.20x slower                                                 |
| docutils                   | 3.57 sec                                                               | 4.30 sec: 1.21x slower                                                |
| json                       | 6.71 ms                                                                | 8.12 ms: 1.21x slower                                                 |
| scimark_monte_carlo        | 88.9 ms                                                                | 108 ms: 1.21x slower                                                  |
| shortest_path              | 861 ms                                                                 | 1.05 sec: 1.22x slower                                                |
| logging_format             | 8.76 us                                                                | 10.7 us: 1.22x slower                                                 |
| raytrace                   | 348 ms                                                                 | 425 ms: 1.22x slower                                                  |
| subparsers                 | 28.6 ms                                                                | 35.2 ms: 1.23x slower                                                 |
| connected_components       | 769 ms                                                                 | 959 ms: 1.25x slower                                                  |
| deepcopy_memo              | 37.3 us                                                                | 46.8 us: 1.26x slower                                                 |
| go                         | 151 ms                                                                 | 190 ms: 1.26x slower                                                  |
| crypto_pyaes               | 92.4 ms                                                                | 117 ms: 1.27x slower                                                  |
| logging_simple             | 7.73 us                                                                | 9.83 us: 1.27x slower                                                 |
| deepcopy                   | 315 us                                                                 | 401 us: 1.27x slower                                                  |
| meteor_contest             | 131 ms                                                                 | 168 ms: 1.28x slower                                                  |
| comprehensions             | 21.6 us                                                                | 27.7 us: 1.29x slower                                                 |
| mdp                        | 1.79 sec                                                               | 2.31 sec: 1.29x slower                                                |
| scimark_sparse_mat_mult    | 5.88 ms                                                                | 7.65 ms: 1.30x slower                                                 |
| django_template            | 45.4 ms                                                                | 59.6 ms: 1.31x slower                                                 |
| bpe_tokeniser              | 5.78 sec                                                               | 7.69 sec: 1.33x slower                                                |
| deltablue                  | 4.34 ms                                                                | 5.81 ms: 1.34x slower                                                 |
| nbody                      | 118 ms                                                                 | 158 ms: 1.34x slower                                                  |
| mako                       | 17.3 ms                                                                | 23.4 ms: 1.35x slower                                                 |
| deepcopy_reduce            | 3.27 us                                                                | 4.43 us: 1.35x slower                                                 |
| genshi_xml                 | 61.9 ms                                                                | 84.5 ms: 1.36x slower                                                 |
| chaos                      | 74.1 ms                                                                | 101 ms: 1.37x slower                                                  |
| regex_compile              | 162 ms                                                                 | 222 ms: 1.37x slower                                                  |
| sqlalchemy_declarative     | 169 ms                                                                 | 233 ms: 1.38x slower                                                  |
| python_startup_no_site     | 16.7 ms                                                                | 24.8 ms: 1.48x slower                                                 |
| coverage                   | 105 ms                                                                 | 164 ms: 1.55x slower                                                  |
| bench_thread_pool          | 2.96 ms                                                                | 5.16 ms: 1.74x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.14x slower                                                          |

Benchmark hidden because not significant (11): async_tree_memoization_tg, regex_effbot, asyncio_websockets, sqlglot_v2_normalize, xml_etree_generate, pathlib, regex_dna, async_tree_cpu_io_mixed, regex_v8, coroutines, telco
Ignored benchmarks (1) of results/bm-20250402-3.14.0a6+-ccaa69a-NOGIL/bm-20250402-linux-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a.json: html5lib

- Geometric mean (including insignificant results): 1.110x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x