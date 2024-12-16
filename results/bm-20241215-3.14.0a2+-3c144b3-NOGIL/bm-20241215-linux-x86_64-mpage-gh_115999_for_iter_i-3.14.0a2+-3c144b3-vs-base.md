# Results vs. base

- fork: mpage
- ref: gh_115999_for_iter_i
- machine: linux-x86_64
- commit hash: 3c144b3
- commit date: 2024-12-15
- overall geometric mean: 1.132x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 590 ms                                                                 | 526 ms: 1.12x faster                                                  |
| docutils       | 4.38 sec                                                               | 4.13 sec: 1.06x faster                                                |
| html5lib       | 126 ms                                                                 | 104 ms: 1.21x faster                                                  |
| sphinx         | 1.68 sec                                                               | 1.59 sec: 1.06x faster                                                |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 452 ms                                                                 | 321 ms: 1.41x faster                                                  |
| async_tree_io_tg           | 1.03 sec                                                               | 742 ms: 1.39x faster                                                  |
| async_tree_none            | 513 ms                                                                 | 393 ms: 1.31x faster                                                  |
| async_tree_memoization_tg  | 580 ms                                                                 | 447 ms: 1.30x faster                                                  |
| async_tree_io              | 1.05 sec                                                               | 837 ms: 1.26x faster                                                  |
| async_tree_memoization     | 645 ms                                                                 | 514 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 762 ms                                                                 | 635 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 857 ms                                                                 | 724 ms: 1.18x faster                                                  |
| coroutines                 | 34.3 ms                                                                | 32.4 ms: 1.06x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.21x faster                                                          |

Benchmark hidden because not significant (2): async_generators, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 163 ms                                                                 | 111 ms: 1.47x faster                                                  |
| pidigits       | 241 ms                                                                 | 233 ms: 1.03x faster                                                  |
| nbody          | 168 ms                                                                 | 177 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.13x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 218 ms                                                                 | 198 ms: 1.10x faster                                                  |
| regex_dna      | 293 ms                                                                 | 285 ms: 1.03x faster                                                  |
| regex_v8       | 32.6 ms                                                                | 33.9 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 614 us                                                                 | 482 us: 1.27x faster                                                  |
| xml_etree_process    | 107 ms                                                                 | 92.1 ms: 1.16x faster                                                 |
| unpickle_pure_python | 392 us                                                                 | 340 us: 1.16x faster                                                  |
| tomli_loads          | 3.38 sec                                                               | 3.04 sec: 1.11x faster                                                |
| json_loads           | 38.2 us                                                                | 34.6 us: 1.10x faster                                                 |
| xml_etree_parse      | 212 ms                                                                 | 198 ms: 1.07x faster                                                  |
| Geometric mean       | (ref)                                                                  | 1.10x faster                                                          |

Benchmark hidden because not significant (3): xml_etree_iterparse, json_dumps, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup | 30.4 ms                                                                | 31.8 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 60.0 ms                                                                | 51.9 ms: 1.16x faster                                                 |
| genshi_xml      | 86.5 ms                                                                | 77.4 ms: 1.12x faster                                                 |
| genshi_text     | 40.4 ms                                                                | 36.6 ms: 1.10x faster                                                 |
| mako            | 26.2 ms                                                                | 24.5 ms: 1.07x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.11x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| deltablue                  | 11.1 ms                                                                | 5.91 ms: 1.88x faster                                                 |
| go                         | 303 ms                                                                 | 178 ms: 1.70x faster                                                  |
| logging_silent             | 225 ns                                                                 | 146 ns: 1.54x faster                                                  |
| sqlglot_parse              | 3.29 ms                                                                | 2.15 ms: 1.53x faster                                                 |
| scimark_sor                | 292 ms                                                                 | 196 ms: 1.49x faster                                                  |
| float                      | 163 ms                                                                 | 111 ms: 1.47x faster                                                  |
| raytrace                   | 625 ms                                                                 | 437 ms: 1.43x faster                                                  |
| async_tree_none_tg         | 452 ms                                                                 | 321 ms: 1.41x faster                                                  |
| async_tree_io_tg           | 1.03 sec                                                               | 742 ms: 1.39x faster                                                  |
| sqlglot_transpile          | 3.87 ms                                                                | 2.78 ms: 1.39x faster                                                 |
| logging_simple             | 12.5 us                                                                | 9.47 us: 1.32x faster                                                 |
| async_tree_none            | 513 ms                                                                 | 393 ms: 1.31x faster                                                  |
| comprehensions             | 32.7 us                                                                | 25.1 us: 1.31x faster                                                 |
| async_tree_memoization_tg  | 580 ms                                                                 | 447 ms: 1.30x faster                                                  |
| logging_format             | 13.9 us                                                                | 10.7 us: 1.29x faster                                                 |
| scimark_monte_carlo        | 144 ms                                                                 | 112 ms: 1.29x faster                                                  |
| chaos                      | 133 ms                                                                 | 104 ms: 1.28x faster                                                  |
| richards                   | 96.8 ms                                                                | 75.5 ms: 1.28x faster                                                 |
| hexiom                     | 12.3 ms                                                                | 9.62 ms: 1.28x faster                                                 |
| pickle_pure_python         | 614 us                                                                 | 482 us: 1.27x faster                                                  |
| async_tree_io              | 1.05 sec                                                               | 837 ms: 1.26x faster                                                  |
| pyflate                    | 913 ms                                                                 | 726 ms: 1.26x faster                                                  |
| generators                 | 53.3 ms                                                                | 42.4 ms: 1.26x faster                                                 |
| async_tree_memoization     | 645 ms                                                                 | 514 ms: 1.25x faster                                                  |
| richards_super             | 106 ms                                                                 | 84.6 ms: 1.25x faster                                                 |
| html5lib                   | 126 ms                                                                 | 104 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 762 ms                                                                 | 635 ms: 1.20x faster                                                  |
| pycparser                  | 1.88 sec                                                               | 1.58 sec: 1.19x faster                                                |
| async_tree_cpu_io_mixed    | 857 ms                                                                 | 724 ms: 1.18x faster                                                  |
| subparsers                 | 42.8 ms                                                                | 36.6 ms: 1.17x faster                                                 |
| xml_etree_process          | 107 ms                                                                 | 92.1 ms: 1.16x faster                                                 |
| pprint_pformat             | 2.66 sec                                                               | 2.30 sec: 1.16x faster                                                |
| django_template            | 60.0 ms                                                                | 51.9 ms: 1.16x faster                                                 |
| unpickle_pure_python       | 392 us                                                                 | 340 us: 1.16x faster                                                  |
| thrift                     | 1.44 ms                                                                | 1.25 ms: 1.15x faster                                                 |
| dulwich_log                | 116 ms                                                                 | 101 ms: 1.15x faster                                                  |
| sqlalchemy_imperative      | 36.0 ms                                                                | 31.6 ms: 1.14x faster                                                 |
| pprint_safe_repr           | 1.26 sec                                                               | 1.10 sec: 1.14x faster                                                |
| 2to3                       | 590 ms                                                                 | 526 ms: 1.12x faster                                                  |
| sqlalchemy_declarative     | 266 ms                                                                 | 238 ms: 1.12x faster                                                  |
| genshi_xml                 | 86.5 ms                                                                | 77.4 ms: 1.12x faster                                                 |
| sqlglot_normalize          | 171 ms                                                                 | 153 ms: 1.12x faster                                                  |
| tomli_loads                | 3.38 sec                                                               | 3.04 sec: 1.11x faster                                                |
| genshi_text                | 40.4 ms                                                                | 36.6 ms: 1.10x faster                                                 |
| scimark_lu                 | 222 ms                                                                 | 201 ms: 1.10x faster                                                  |
| json_loads                 | 38.2 us                                                                | 34.6 us: 1.10x faster                                                 |
| regex_compile              | 218 ms                                                                 | 198 ms: 1.10x faster                                                  |
| bench_thread_pool          | 3.83 ms                                                                | 3.50 ms: 1.09x faster                                                 |
| json                       | 7.27 ms                                                                | 6.67 ms: 1.09x faster                                                 |
| sympy_str                  | 592 ms                                                                 | 548 ms: 1.08x faster                                                  |
| many_optionals             | 1.47 ms                                                                | 1.37 ms: 1.07x faster                                                 |
| mako                       | 26.2 ms                                                                | 24.5 ms: 1.07x faster                                                 |
| sympy_integrate            | 40.0 ms                                                                | 37.4 ms: 1.07x faster                                                 |
| xml_etree_parse            | 212 ms                                                                 | 198 ms: 1.07x faster                                                  |
| sympy_sum                  | 418 ms                                                                 | 392 ms: 1.07x faster                                                  |
| meteor_contest             | 177 ms                                                                 | 166 ms: 1.06x faster                                                  |
| deepcopy_reduce            | 4.55 us                                                                | 4.28 us: 1.06x faster                                                 |
| docutils                   | 4.38 sec                                                               | 4.13 sec: 1.06x faster                                                |
| coroutines                 | 34.3 ms                                                                | 32.4 ms: 1.06x faster                                                 |
| bench_mp_pool              | 93.6 ms                                                                | 88.4 ms: 1.06x faster                                                 |
| sphinx                     | 1.68 sec                                                               | 1.59 sec: 1.06x faster                                                |
| telco                      | 12.1 ms                                                                | 11.5 ms: 1.05x faster                                                 |
| sympy_expand               | 1.16 sec                                                               | 1.10 sec: 1.05x faster                                                |
| sqlite_synth               | 3.78 us                                                                | 3.61 us: 1.05x faster                                                 |
| pylint                     | 500 ms                                                                 | 478 ms: 1.05x faster                                                  |
| deepcopy_memo              | 50.8 us                                                                | 48.5 us: 1.05x faster                                                 |
| bpe_tokeniser              | 7.42 sec                                                               | 7.11 sec: 1.04x faster                                                |
| pathlib                    | 29.8 ms                                                                | 28.6 ms: 1.04x faster                                                 |
| pidigits                   | 241 ms                                                                 | 233 ms: 1.03x faster                                                  |
| mdp                        | 4.52 sec                                                               | 4.39 sec: 1.03x faster                                                |
| regex_dna                  | 293 ms                                                                 | 285 ms: 1.03x faster                                                  |
| k_core                     | 4.35 sec                                                               | 4.26 sec: 1.02x faster                                                |
| regex_v8                   | 32.6 ms                                                                | 33.9 ms: 1.04x slower                                                 |
| python_startup             | 30.4 ms                                                                | 31.8 ms: 1.05x slower                                                 |
| nbody                      | 168 ms                                                                 | 177 ms: 1.05x slower                                                  |
| spectral_norm              | 154 ms                                                                 | 163 ms: 1.06x slower                                                  |
| gc_traversal               | 6.06 ms                                                                | 6.53 ms: 1.08x slower                                                 |
| scimark_sparse_mat_mult    | 7.93 ms                                                                | 8.58 ms: 1.08x slower                                                 |
| coverage                   | 126 ms                                                                 | 136 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.13x faster                                                          |

Benchmark hidden because not significant (17): sqlglot_optimize, xml_etree_iterparse, json_dumps, xml_etree_generate, async_generators, nqueens, scimark_fft, asyncio_websockets, shortest_path, typing_runtime_protocols, fannkuch, connected_components, python_startup_no_site, regex_effbot, crypto_pyaes, create_gc_cycles, deepcopy

- Geometric mean (including insignificant results): 1.132x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.01x