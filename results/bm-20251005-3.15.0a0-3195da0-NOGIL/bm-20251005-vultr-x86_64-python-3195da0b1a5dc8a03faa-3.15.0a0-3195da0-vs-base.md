# Results vs. base

- fork: python
- ref: 3195da0b1a5dc8a03faa
- machine: linux-x86_64
- commit hash: 3195da0
- commit date: 2025-10-05
- overall geometric mean: 1.091x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20251005-3.15.0a0-3195da0/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json | results/bm-20251005-3.15.0a0-3195da0-NOGIL/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                                                                          | 279 ms: 1.13x slower                                                                                                  |
| docutils       | 2.57 sec                                                                                                        | 2.67 sec: 1.04x slower                                                                                                |
| html5lib       | 61.2 ms                                                                                                         | 66.7 ms: 1.09x slower                                                                                                 |
| sphinx         | 973 ms                                                                                                          | 1.06 sec: 1.09x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20251005-3.15.0a0-3195da0/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json | results/bm-20251005-3.15.0a0-3195da0-NOGIL/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 616 ms                                                                                                          | 514 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 251 ms                                                                                                          | 222 ms: 1.13x faster                                                                                                  |
| async_tree_memoization_tg  | 313 ms                                                                                                          | 279 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 604 ms                                                                                                          | 539 ms: 1.12x faster                                                                                                  |
| async_tree_none            | 265 ms                                                                                                          | 255 ms: 1.04x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 493 ms                                                                                                          | 482 ms: 1.02x faster                                                                                                  |
| async_tree_memoization     | 311 ms                                                                                                          | 309 ms: 1.01x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| coroutines                 | 24.4 ms                                                                                                         | 24.6 ms: 1.01x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 490 ms                                                                                                          | 511 ms: 1.04x slower                                                                                                  |
| async_generators           | 347 ms                                                                                                          | 373 ms: 1.08x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x faster                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20251005-3.15.0a0-3195da0/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json | results/bm-20251005-3.15.0a0-3195da0-NOGIL/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 72.0 ms                                                                                                         | 69.4 ms: 1.04x faster                                                                                                 |
| pidigits       | 193 ms                                                                                                          | 197 ms: 1.02x slower                                                                                                  |
| nbody          | 91.1 ms                                                                                                         | 126 ms: 1.38x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20251005-3.15.0a0-3195da0/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json | results/bm-20251005-3.15.0a0-3195da0-NOGIL/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.4 ms                                                                                                         | 20.6 ms: 1.04x faster                                                                                                 |
| regex_effbot   | 2.61 ms                                                                                                         | 2.56 ms: 1.02x faster                                                                                                 |
| regex_compile  | 124 ms                                                                                                          | 143 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.02x slower                                                                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20251005-3.15.0a0-3195da0/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json | results/bm-20251005-3.15.0a0-3195da0-NOGIL/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.1 ms                                                                                                         | 87.8 ms: 1.06x faster                                                                                                 |
| tomli_loads          | 1.89 sec                                                                                                        | 2.04 sec: 1.08x slower                                                                                                |
| unpickle_pure_python | 206 us                                                                                                          | 230 us: 1.12x slower                                                                                                  |
| pickle_pure_python   | 302 us                                                                                                          | 340 us: 1.13x slower                                                                                                  |
| json_dumps           | 9.62 ms                                                                                                         | 10.9 ms: 1.14x slower                                                                                                 |
| json_loads           | 27.8 us                                                                                                         | 31.6 us: 1.14x slower                                                                                                 |
| xml_etree_generate   | 83.6 ms                                                                                                         | 95.7 ms: 1.14x slower                                                                                                 |
| xml_etree_process    | 58.2 ms                                                                                                         | 68.8 ms: 1.18x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20251005-3.15.0a0-3195da0/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json | results/bm-20251005-3.15.0a0-3195da0-NOGIL/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                                                         | 15.8 ms: 1.26x slower                                                                                                 |
| python_startup_no_site | 7.24 ms                                                                                                         | 9.59 ms: 1.33x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20251005-3.15.0a0-3195da0/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json | results/bm-20251005-3.15.0a0-3195da0-NOGIL/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 33.9 ms                                                                                                         | 40.2 ms: 1.19x slower                                                                                                 |
| genshi_xml      | 48.2 ms                                                                                                         | 57.8 ms: 1.20x slower                                                                                                 |
| genshi_text     | 20.3 ms                                                                                                         | 26.3 ms: 1.30x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 15.5 ms: 1.31x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.25x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20251005-3.15.0a0-3195da0/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json | results/bm-20251005-3.15.0a0-3195da0-NOGIL/bm-20251005-vultr-x86_64-python-3195da0b1a5dc8a03faa-3.15.0a0-3195da0.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.40 ms                                                                                                         | 1.95 ms: 2.26x faster                                                                                                 |
| create_gc_cycles           | 1.92 ms                                                                                                         | 1.52 ms: 1.27x faster                                                                                                 |
| async_tree_io_tg           | 616 ms                                                                                                          | 514 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 251 ms                                                                                                          | 222 ms: 1.13x faster                                                                                                  |
| async_tree_memoization_tg  | 313 ms                                                                                                          | 279 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 604 ms                                                                                                          | 539 ms: 1.12x faster                                                                                                  |
| sqlite_synth               | 2.25 us                                                                                                         | 2.08 us: 1.08x faster                                                                                                 |
| xml_etree_iterparse        | 93.1 ms                                                                                                         | 87.8 ms: 1.06x faster                                                                                                 |
| regex_v8                   | 21.4 ms                                                                                                         | 20.6 ms: 1.04x faster                                                                                                 |
| float                      | 72.0 ms                                                                                                         | 69.4 ms: 1.04x faster                                                                                                 |
| async_tree_none            | 265 ms                                                                                                          | 255 ms: 1.04x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 493 ms                                                                                                          | 482 ms: 1.02x faster                                                                                                  |
| regex_effbot               | 2.61 ms                                                                                                         | 2.56 ms: 1.02x faster                                                                                                 |
| async_tree_memoization     | 311 ms                                                                                                          | 309 ms: 1.01x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 512 ms: 1.01x faster                                                                                                  |
| coroutines                 | 24.4 ms                                                                                                         | 24.6 ms: 1.01x slower                                                                                                 |
| pidigits                   | 193 ms                                                                                                          | 197 ms: 1.02x slower                                                                                                  |
| pathlib                    | 17.4 ms                                                                                                         | 18.0 ms: 1.03x slower                                                                                                 |
| logging_silent             | 97.9 ns                                                                                                         | 101 ns: 1.03x slower                                                                                                  |
| docutils                   | 2.57 sec                                                                                                        | 2.67 sec: 1.04x slower                                                                                                |
| async_tree_cpu_io_mixed    | 490 ms                                                                                                          | 511 ms: 1.04x slower                                                                                                  |
| bpe_tokeniser              | 4.20 sec                                                                                                        | 4.40 sec: 1.05x slower                                                                                                |
| deltablue                  | 3.29 ms                                                                                                         | 3.50 ms: 1.06x slower                                                                                                 |
| async_generators           | 347 ms                                                                                                          | 373 ms: 1.08x slower                                                                                                  |
| tomli_loads                | 1.89 sec                                                                                                        | 2.04 sec: 1.08x slower                                                                                                |
| dulwich_log                | 66.5 ms                                                                                                         | 71.7 ms: 1.08x slower                                                                                                 |
| json                       | 5.01 ms                                                                                                         | 5.42 ms: 1.08x slower                                                                                                 |
| html5lib                   | 61.2 ms                                                                                                         | 66.7 ms: 1.09x slower                                                                                                 |
| sphinx                     | 973 ms                                                                                                          | 1.06 sec: 1.09x slower                                                                                                |
| pycparser                  | 1.07 sec                                                                                                        | 1.17 sec: 1.09x slower                                                                                                |
| scimark_sparse_mat_mult    | 4.85 ms                                                                                                         | 5.32 ms: 1.10x slower                                                                                                 |
| scimark_fft                | 312 ms                                                                                                          | 344 ms: 1.10x slower                                                                                                  |
| pylint                     | 278 ms                                                                                                          | 307 ms: 1.10x slower                                                                                                  |
| generators                 | 27.3 ms                                                                                                         | 30.2 ms: 1.10x slower                                                                                                 |
| k_core                     | 2.03 sec                                                                                                        | 2.24 sec: 1.10x slower                                                                                                |
| telco                      | 158 ms                                                                                                          | 175 ms: 1.11x slower                                                                                                  |
| chaos                      | 56.4 ms                                                                                                         | 63.1 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python       | 206 us                                                                                                          | 230 us: 1.12x slower                                                                                                  |
| many_optionals             | 1.23 ms                                                                                                         | 1.38 ms: 1.12x slower                                                                                                 |
| pickle_pure_python         | 302 us                                                                                                          | 340 us: 1.13x slower                                                                                                  |
| 2to3                       | 246 ms                                                                                                          | 279 ms: 1.13x slower                                                                                                  |
| json_dumps                 | 9.62 ms                                                                                                         | 10.9 ms: 1.14x slower                                                                                                 |
| json_loads                 | 27.8 us                                                                                                         | 31.6 us: 1.14x slower                                                                                                 |
| sympy_expand               | 459 ms                                                                                                          | 523 ms: 1.14x slower                                                                                                  |
| nqueens                    | 77.6 ms                                                                                                         | 88.4 ms: 1.14x slower                                                                                                 |
| comprehensions             | 15.7 us                                                                                                         | 18.0 us: 1.14x slower                                                                                                 |
| hexiom                     | 5.65 ms                                                                                                         | 6.46 ms: 1.14x slower                                                                                                 |
| mdp                        | 1.15 sec                                                                                                        | 1.32 sec: 1.14x slower                                                                                                |
| xml_etree_generate         | 83.6 ms                                                                                                         | 95.7 ms: 1.14x slower                                                                                                 |
| scimark_sor                | 107 ms                                                                                                          | 123 ms: 1.15x slower                                                                                                  |
| sympy_str                  | 271 ms                                                                                                          | 311 ms: 1.15x slower                                                                                                  |
| pprint_safe_repr           | 688 ms                                                                                                          | 791 ms: 1.15x slower                                                                                                  |
| thrift                     | 766 us                                                                                                          | 881 us: 1.15x slower                                                                                                  |
| go                         | 105 ms                                                                                                          | 121 ms: 1.15x slower                                                                                                  |
| sqlglot_v2_optimize        | 50.2 ms                                                                                                         | 58.0 ms: 1.16x slower                                                                                                 |
| sqlglot_v2_normalize       | 98.8 ms                                                                                                         | 114 ms: 1.16x slower                                                                                                  |
| sympy_sum                  | 154 ms                                                                                                          | 178 ms: 1.16x slower                                                                                                  |
| regex_compile              | 124 ms                                                                                                          | 143 ms: 1.16x slower                                                                                                  |
| deepcopy_reduce            | 2.57 us                                                                                                         | 2.98 us: 1.16x slower                                                                                                 |
| sympy_integrate            | 18.9 ms                                                                                                         | 21.9 ms: 1.16x slower                                                                                                 |
| pyflate                    | 398 ms                                                                                                          | 462 ms: 1.16x slower                                                                                                  |
| spectral_norm              | 95.6 ms                                                                                                         | 111 ms: 1.16x slower                                                                                                  |
| pprint_pformat             | 1.40 sec                                                                                                        | 1.63 sec: 1.17x slower                                                                                                |
| deepcopy                   | 241 us                                                                                                          | 281 us: 1.17x slower                                                                                                  |
| subparsers                 | 44.0 ms                                                                                                         | 51.5 ms: 1.17x slower                                                                                                 |
| scimark_lu                 | 113 ms                                                                                                          | 132 ms: 1.17x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.50 ms                                                                                                         | 1.77 ms: 1.18x slower                                                                                                 |
| raytrace                   | 253 ms                                                                                                          | 297 ms: 1.18x slower                                                                                                  |
| xml_etree_process          | 58.2 ms                                                                                                         | 68.8 ms: 1.18x slower                                                                                                 |
| meteor_contest             | 99.8 ms                                                                                                         | 118 ms: 1.18x slower                                                                                                  |
| logging_format             | 6.51 us                                                                                                         | 7.71 us: 1.18x slower                                                                                                 |
| django_template            | 33.9 ms                                                                                                         | 40.2 ms: 1.19x slower                                                                                                 |
| deepcopy_memo              | 26.1 us                                                                                                         | 30.9 us: 1.19x slower                                                                                                 |
| logging_simple             | 5.74 us                                                                                                         | 6.82 us: 1.19x slower                                                                                                 |
| fannkuch                   | 382 ms                                                                                                          | 455 ms: 1.19x slower                                                                                                  |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.44 ms: 1.19x slower                                                                                                 |
| genshi_xml                 | 48.2 ms                                                                                                         | 57.8 ms: 1.20x slower                                                                                                 |
| shortest_path              | 444 ms                                                                                                          | 538 ms: 1.21x slower                                                                                                  |
| connected_components       | 404 ms                                                                                                          | 494 ms: 1.22x slower                                                                                                  |
| bench_mp_pool              | 12.3 ms                                                                                                         | 15.2 ms: 1.23x slower                                                                                                 |
| richards                   | 40.8 ms                                                                                                         | 50.6 ms: 1.24x slower                                                                                                 |
| crypto_pyaes               | 69.2 ms                                                                                                         | 85.8 ms: 1.24x slower                                                                                                 |
| typing_runtime_protocols   | 150 us                                                                                                          | 189 us: 1.26x slower                                                                                                  |
| scimark_monte_carlo        | 61.8 ms                                                                                                         | 77.9 ms: 1.26x slower                                                                                                 |
| python_startup             | 12.5 ms                                                                                                         | 15.8 ms: 1.26x slower                                                                                                 |
| richards_super             | 46.5 ms                                                                                                         | 58.7 ms: 1.26x slower                                                                                                 |
| genshi_text                | 20.3 ms                                                                                                         | 26.3 ms: 1.30x slower                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 15.5 ms: 1.31x slower                                                                                                 |
| python_startup_no_site     | 7.24 ms                                                                                                         | 9.59 ms: 1.33x slower                                                                                                 |
| coverage                   | 81.3 ms                                                                                                         | 110 ms: 1.35x slower                                                                                                  |
| nbody                      | 91.1 ms                                                                                                         | 126 ms: 1.38x slower                                                                                                  |
| bench_thread_pool          | 996 us                                                                                                          | 3.06 ms: 3.07x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmark hidden because not significant (2): xml_etree_parse, regex_dna

- Geometric mean (including insignificant results): 1.091x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x