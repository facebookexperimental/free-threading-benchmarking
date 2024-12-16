# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_for_iter_i
- machine: linux-x86_64
- commit hash: 3c144b3
- commit date: 2024-12-15
- overall geometric mean: 1.140x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 432 ms                                                                 | 526 ms: 1.22x slower                                                  |
| docutils       | 3.61 sec                                                               | 4.13 sec: 1.14x slower                                                |
| html5lib       | 89.3 ms                                                                | 104 ms: 1.17x slower                                                  |
| sphinx         | 1.44 sec                                                               | 1.59 sec: 1.11x slower                                                |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 849 ms                                                                 | 742 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 363 ms                                                                 | 321 ms: 1.13x faster                                                  |
| async_tree_cpu_io_mixed_tg | 682 ms                                                                 | 635 ms: 1.07x faster                                                  |
| async_tree_io              | 889 ms                                                                 | 837 ms: 1.06x faster                                                  |
| async_tree_none            | 378 ms                                                                 | 393 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed    | 686 ms                                                                 | 724 ms: 1.06x slower                                                  |
| coroutines                 | 30.1 ms                                                                | 32.4 ms: 1.08x slower                                                 |
| async_generators           | 535 ms                                                                 | 624 ms: 1.17x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (3): async_tree_memoization_tg, async_tree_memoization, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 120 ms                                                                 | 177 ms: 1.47x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                          |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 276 ms                                                                 | 285 ms: 1.03x slower                                                  |
| regex_v8       | 32.5 ms                                                                | 33.9 ms: 1.04x slower                                                 |
| regex_effbot   | 4.12 ms                                                                | 4.36 ms: 1.06x slower                                                 |
| regex_compile  | 171 ms                                                                 | 198 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 143 ms                                                                 | 131 ms: 1.09x faster                                                  |
| xml_etree_parse      | 192 ms                                                                 | 198 ms: 1.03x slower                                                  |
| json_loads           | 32.7 us                                                                | 34.6 us: 1.06x slower                                                 |
| pickle_pure_python   | 434 us                                                                 | 482 us: 1.11x slower                                                  |
| json_dumps           | 15.6 ms                                                                | 17.4 ms: 1.11x slower                                                 |
| xml_etree_process    | 82.1 ms                                                                | 92.1 ms: 1.12x slower                                                 |
| xml_etree_generate   | 113 ms                                                                 | 132 ms: 1.16x slower                                                  |
| unpickle_pure_python | 282 us                                                                 | 340 us: 1.21x slower                                                  |
| tomli_loads          | 2.50 sec                                                               | 3.04 sec: 1.21x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 25.0 ms                                                                | 31.8 ms: 1.27x slower                                                 |
| python_startup_no_site | 14.3 ms                                                                | 19.6 ms: 1.37x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.32x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 69.5 ms                                                                | 77.4 ms: 1.11x slower                                                 |
| django_template | 44.3 ms                                                                | 51.9 ms: 1.17x slower                                                 |
| genshi_text     | 29.7 ms                                                                | 36.6 ms: 1.23x slower                                                 |
| mako            | 17.3 ms                                                                | 24.5 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.23x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2+-2de048c | bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2+-3c144b3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 7.70 ms                                                                | 6.53 ms: 1.18x faster                                                 |
| async_tree_io_tg           | 849 ms                                                                 | 742 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 363 ms                                                                 | 321 ms: 1.13x faster                                                  |
| xml_etree_iterparse        | 143 ms                                                                 | 131 ms: 1.09x faster                                                  |
| sqlite_synth               | 3.88 us                                                                | 3.61 us: 1.08x faster                                                 |
| async_tree_cpu_io_mixed_tg | 682 ms                                                                 | 635 ms: 1.07x faster                                                  |
| async_tree_io              | 889 ms                                                                 | 837 ms: 1.06x faster                                                  |
| xml_etree_parse            | 192 ms                                                                 | 198 ms: 1.03x slower                                                  |
| regex_dna                  | 276 ms                                                                 | 285 ms: 1.03x slower                                                  |
| async_tree_none            | 378 ms                                                                 | 393 ms: 1.04x slower                                                  |
| regex_v8                   | 32.5 ms                                                                | 33.9 ms: 1.04x slower                                                 |
| async_tree_cpu_io_mixed    | 686 ms                                                                 | 724 ms: 1.06x slower                                                  |
| k_core                     | 4.03 sec                                                               | 4.26 sec: 1.06x slower                                                |
| json_loads                 | 32.7 us                                                                | 34.6 us: 1.06x slower                                                 |
| regex_effbot               | 4.12 ms                                                                | 4.36 ms: 1.06x slower                                                 |
| generators                 | 39.5 ms                                                                | 42.4 ms: 1.07x slower                                                 |
| logging_silent             | 136 ns                                                                 | 146 ns: 1.08x slower                                                  |
| coroutines                 | 30.1 ms                                                                | 32.4 ms: 1.08x slower                                                 |
| dulwich_log                | 93.5 ms                                                                | 101 ms: 1.08x slower                                                  |
| json                       | 6.03 ms                                                                | 6.67 ms: 1.11x slower                                                 |
| sphinx                     | 1.44 sec                                                               | 1.59 sec: 1.11x slower                                                |
| pickle_pure_python         | 434 us                                                                 | 482 us: 1.11x slower                                                  |
| json_dumps                 | 15.6 ms                                                                | 17.4 ms: 1.11x slower                                                 |
| genshi_xml                 | 69.5 ms                                                                | 77.4 ms: 1.11x slower                                                 |
| xml_etree_process          | 82.1 ms                                                                | 92.1 ms: 1.12x slower                                                 |
| telco                      | 10.2 ms                                                                | 11.5 ms: 1.13x slower                                                 |
| sqlglot_normalize          | 135 ms                                                                 | 153 ms: 1.14x slower                                                  |
| sqlglot_optimize           | 72.8 ms                                                                | 83.2 ms: 1.14x slower                                                 |
| docutils                   | 3.61 sec                                                               | 4.13 sec: 1.14x slower                                                |
| shortest_path              | 880 ms                                                                 | 1.01 sec: 1.15x slower                                                |
| pyflate                    | 633 ms                                                                 | 726 ms: 1.15x slower                                                  |
| meteor_contest             | 144 ms                                                                 | 166 ms: 1.15x slower                                                  |
| pprint_pformat             | 1.99 sec                                                               | 2.30 sec: 1.15x slower                                                |
| regex_compile              | 171 ms                                                                 | 198 ms: 1.16x slower                                                  |
| connected_components       | 798 ms                                                                 | 925 ms: 1.16x slower                                                  |
| xml_etree_generate         | 113 ms                                                                 | 132 ms: 1.16x slower                                                  |
| mdp                        | 3.77 sec                                                               | 4.39 sec: 1.16x slower                                                |
| html5lib                   | 89.3 ms                                                                | 104 ms: 1.17x slower                                                  |
| async_generators           | 535 ms                                                                 | 624 ms: 1.17x slower                                                  |
| pprint_safe_repr           | 944 ms                                                                 | 1.10 sec: 1.17x slower                                                |
| django_template            | 44.3 ms                                                                | 51.9 ms: 1.17x slower                                                 |
| hexiom                     | 8.16 ms                                                                | 9.62 ms: 1.18x slower                                                 |
| comprehensions             | 21.2 us                                                                | 25.1 us: 1.18x slower                                                 |
| logging_simple             | 8.00 us                                                                | 9.47 us: 1.18x slower                                                 |
| nqueens                    | 105 ms                                                                 | 125 ms: 1.19x slower                                                  |
| scimark_fft                | 436 ms                                                                 | 520 ms: 1.19x slower                                                  |
| go                         | 149 ms                                                                 | 178 ms: 1.19x slower                                                  |
| logging_format             | 8.97 us                                                                | 10.7 us: 1.20x slower                                                 |
| many_optionals             | 1.14 ms                                                                | 1.37 ms: 1.20x slower                                                 |
| bench_thread_pool          | 2.91 ms                                                                | 3.50 ms: 1.20x slower                                                 |
| unpickle_pure_python       | 282 us                                                                 | 340 us: 1.21x slower                                                  |
| subparsers                 | 30.2 ms                                                                | 36.6 ms: 1.21x slower                                                 |
| deepcopy                   | 348 us                                                                 | 422 us: 1.21x slower                                                  |
| richards_super             | 69.8 ms                                                                | 84.6 ms: 1.21x slower                                                 |
| spectral_norm              | 134 ms                                                                 | 163 ms: 1.21x slower                                                  |
| tomli_loads                | 2.50 sec                                                               | 3.04 sec: 1.21x slower                                                |
| pylint                     | 393 ms                                                                 | 478 ms: 1.21x slower                                                  |
| 2to3                       | 432 ms                                                                 | 526 ms: 1.22x slower                                                  |
| richards                   | 61.9 ms                                                                | 75.5 ms: 1.22x slower                                                 |
| deepcopy_memo              | 39.6 us                                                                | 48.5 us: 1.23x slower                                                 |
| bpe_tokeniser              | 5.80 sec                                                               | 7.11 sec: 1.23x slower                                                |
| genshi_text                | 29.7 ms                                                                | 36.6 ms: 1.23x slower                                                 |
| deepcopy_reduce            | 3.45 us                                                                | 4.28 us: 1.24x slower                                                 |
| thrift                     | 1.00 ms                                                                | 1.25 ms: 1.25x slower                                                 |
| scimark_sor                | 157 ms                                                                 | 196 ms: 1.25x slower                                                  |
| typing_runtime_protocols   | 208 us                                                                 | 263 us: 1.26x slower                                                  |
| python_startup             | 25.0 ms                                                                | 31.8 ms: 1.27x slower                                                 |
| scimark_monte_carlo        | 88.2 ms                                                                | 112 ms: 1.27x slower                                                  |
| crypto_pyaes               | 97.2 ms                                                                | 124 ms: 1.28x slower                                                  |
| chaos                      | 80.6 ms                                                                | 104 ms: 1.29x slower                                                  |
| raytrace                   | 336 ms                                                                 | 437 ms: 1.30x slower                                                  |
| scimark_lu                 | 154 ms                                                                 | 201 ms: 1.30x slower                                                  |
| sqlglot_transpile          | 2.12 ms                                                                | 2.78 ms: 1.31x slower                                                 |
| fannkuch                   | 504 ms                                                                 | 663 ms: 1.31x slower                                                  |
| sympy_integrate            | 28.4 ms                                                                | 37.4 ms: 1.31x slower                                                 |
| coverage                   | 103 ms                                                                 | 136 ms: 1.32x slower                                                  |
| sqlglot_parse              | 1.62 ms                                                                | 2.15 ms: 1.33x slower                                                 |
| scimark_sparse_mat_mult    | 6.29 ms                                                                | 8.58 ms: 1.36x slower                                                 |
| python_startup_no_site     | 14.3 ms                                                                | 19.6 ms: 1.37x slower                                                 |
| sqlalchemy_declarative     | 174 ms                                                                 | 238 ms: 1.37x slower                                                  |
| deltablue                  | 4.17 ms                                                                | 5.91 ms: 1.42x slower                                                 |
| mako                       | 17.3 ms                                                                | 24.5 ms: 1.42x slower                                                 |
| sqlalchemy_imperative      | 21.7 ms                                                                | 31.6 ms: 1.46x slower                                                 |
| nbody                      | 120 ms                                                                 | 177 ms: 1.47x slower                                                  |
| sympy_str                  | 345 ms                                                                 | 548 ms: 1.59x slower                                                  |
| sympy_expand               | 575 ms                                                                 | 1.10 sec: 1.91x slower                                                |
| sympy_sum                  | 197 ms                                                                 | 392 ms: 1.98x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.17x slower                                                          |

Benchmark hidden because not significant (9): create_gc_cycles, pidigits, async_tree_memoization_tg, float, pycparser, async_tree_memoization, asyncio_websockets, bench_mp_pool, pathlib

- Geometric mean (including insignificant results): 1.140x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.19x