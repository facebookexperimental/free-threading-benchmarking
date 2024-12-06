# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: eb8ce39
- commit date: 2024-12-05
- overall geometric mean: 1.251x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                 | 361 ms: 1.40x slower                                                  |
| docutils       | 2.57 sec                                                               | 3.07 sec: 1.20x slower                                                |
| sphinx         | 994 ms                                                                 | 1.17 sec: 1.17x slower                                                |
| Geometric mean | (ref)                                                                  | 1.25x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed    | 607 ms                                                                 | 626 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                                 | 610 ms: 1.04x slower                                                  |
| coroutines                 | 21.9 ms                                                                | 25.1 ms: 1.14x slower                                                 |
| async_generators           | 370 ms                                                                 | 453 ms: 1.23x slower                                                  |
| async_tree_io_tg           | 624 ms                                                                 | 786 ms: 1.26x slower                                                  |
| async_tree_io              | 626 ms                                                                 | 811 ms: 1.30x slower                                                  |
| async_tree_none_tg         | 262 ms                                                                 | 345 ms: 1.32x slower                                                  |
| async_tree_memoization     | 339 ms                                                                 | 453 ms: 1.34x slower                                                  |
| async_tree_none            | 276 ms                                                                 | 374 ms: 1.36x slower                                                  |
| async_tree_memoization_tg  | 314 ms                                                                 | 432 ms: 1.38x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.21x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 222 ms                                                                 | 184 ms: 1.20x faster                                                  |
| nbody          | 95.2 ms                                                                | 125 ms: 1.31x slower                                                  |
| float          | 78.6 ms                                                                | 137 ms: 1.75x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.24x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.74 ms                                                                | 2.81 ms: 1.02x slower                                                 |
| regex_v8       | 23.3 ms                                                                | 24.2 ms: 1.04x slower                                                 |
| regex_dna      | 169 ms                                                                 | 184 ms: 1.09x slower                                                  |
| regex_compile  | 130 ms                                                                 | 179 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.1 ms                                                                | 91.5 ms: 1.01x faster                                                 |
| xml_etree_parse      | 130 ms                                                                 | 131 ms: 1.01x slower                                                  |
| xml_etree_generate   | 85.1 ms                                                                | 97.4 ms: 1.14x slower                                                 |
| json_loads           | 25.1 us                                                                | 28.8 us: 1.15x slower                                                 |
| json_dumps           | 11.5 ms                                                                | 14.3 ms: 1.24x slower                                                 |
| tomli_loads          | 2.11 sec                                                               | 2.64 sec: 1.26x slower                                                |
| xml_etree_process    | 59.6 ms                                                                | 78.5 ms: 1.32x slower                                                 |
| unpickle_pure_python | 216 us                                                                 | 331 us: 1.53x slower                                                  |
| pickle_pure_python   | 316 us                                                                 | 518 us: 1.64x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.24x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.1 ms: 1.18x slower                                                 |
| python_startup_no_site | 7.43 ms                                                                | 10.2 ms: 1.38x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.27x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 51.2 ms                                                                | 62.7 ms: 1.23x slower                                                 |
| genshi_text     | 22.3 ms                                                                | 30.4 ms: 1.37x slower                                                 |
| django_template | 35.6 ms                                                                | 50.2 ms: 1.41x slower                                                 |
| mako            | 11.5 ms                                                                | 16.8 ms: 1.46x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.36x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.58 ms                                                                | 3.29 ms: 1.39x faster                                                 |
| pidigits                   | 222 ms                                                                 | 184 ms: 1.20x faster                                                  |
| sqlite_synth               | 2.28 us                                                                | 2.22 us: 1.03x faster                                                 |
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.83 ms                                                                | 1.81 ms: 1.01x faster                                                 |
| xml_etree_iterparse        | 92.1 ms                                                                | 91.5 ms: 1.01x faster                                                 |
| xml_etree_parse            | 130 ms                                                                 | 131 ms: 1.01x slower                                                  |
| regex_effbot               | 2.74 ms                                                                | 2.81 ms: 1.02x slower                                                 |
| async_tree_cpu_io_mixed    | 607 ms                                                                 | 626 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                                 | 610 ms: 1.04x slower                                                  |
| regex_v8                   | 23.3 ms                                                                | 24.2 ms: 1.04x slower                                                 |
| regex_dna                  | 169 ms                                                                 | 184 ms: 1.09x slower                                                  |
| spectral_norm              | 107 ms                                                                 | 119 ms: 1.11x slower                                                  |
| pathlib                    | 18.2 ms                                                                | 20.1 ms: 1.11x slower                                                 |
| json                       | 4.53 ms                                                                | 5.06 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.1 ms                                                                | 97.4 ms: 1.14x slower                                                 |
| coroutines                 | 21.9 ms                                                                | 25.1 ms: 1.14x slower                                                 |
| json_loads                 | 25.1 us                                                                | 28.8 us: 1.15x slower                                                 |
| scimark_fft                | 340 ms                                                                 | 391 ms: 1.15x slower                                                  |
| bpe_tokeniser              | 4.32 sec                                                               | 5.00 sec: 1.16x slower                                                |
| k_core                     | 2.08 sec                                                               | 2.42 sec: 1.16x slower                                                |
| mdp                        | 2.35 sec                                                               | 2.74 sec: 1.17x slower                                                |
| sphinx                     | 994 ms                                                                 | 1.17 sec: 1.17x slower                                                |
| python_startup             | 14.6 ms                                                                | 17.1 ms: 1.18x slower                                                 |
| telco                      | 7.19 ms                                                                | 8.59 ms: 1.20x slower                                                 |
| docutils                   | 2.57 sec                                                               | 3.07 sec: 1.20x slower                                                |
| nqueens                    | 79.5 ms                                                                | 96.5 ms: 1.21x slower                                                 |
| many_optionals             | 1.03 ms                                                                | 1.26 ms: 1.22x slower                                                 |
| bench_mp_pool              | 88.5 ms                                                                | 108 ms: 1.22x slower                                                  |
| scimark_sparse_mat_mult    | 4.57 ms                                                                | 5.57 ms: 1.22x slower                                                 |
| deepcopy                   | 262 us                                                                 | 320 us: 1.22x slower                                                  |
| async_generators           | 370 ms                                                                 | 453 ms: 1.23x slower                                                  |
| genshi_xml                 | 51.2 ms                                                                | 62.7 ms: 1.23x slower                                                 |
| shortest_path              | 444 ms                                                                 | 546 ms: 1.23x slower                                                  |
| json_dumps                 | 11.5 ms                                                                | 14.3 ms: 1.24x slower                                                 |
| connected_components       | 400 ms                                                                 | 497 ms: 1.24x slower                                                  |
| sqlglot_optimize           | 53.6 ms                                                                | 66.8 ms: 1.25x slower                                                 |
| dulwich_log                | 76.1 ms                                                                | 95.0 ms: 1.25x slower                                                 |
| tomli_loads                | 2.11 sec                                                               | 2.64 sec: 1.26x slower                                                |
| async_tree_io_tg           | 624 ms                                                                 | 786 ms: 1.26x slower                                                  |
| sqlglot_normalize          | 107 ms                                                                 | 136 ms: 1.26x slower                                                  |
| coverage                   | 79.8 ms                                                                | 101 ms: 1.27x slower                                                  |
| typing_runtime_protocols   | 161 us                                                                 | 204 us: 1.27x slower                                                  |
| deepcopy_memo              | 30.7 us                                                                | 39.5 us: 1.29x slower                                                 |
| async_tree_io              | 626 ms                                                                 | 811 ms: 1.30x slower                                                  |
| pylint                     | 285 ms                                                                 | 370 ms: 1.30x slower                                                  |
| meteor_contest             | 99.1 ms                                                                | 129 ms: 1.30x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 491 ms: 1.31x slower                                                  |
| nbody                      | 95.2 ms                                                                | 125 ms: 1.31x slower                                                  |
| generators                 | 29.0 ms                                                                | 38.1 ms: 1.31x slower                                                 |
| xml_etree_process          | 59.6 ms                                                                | 78.5 ms: 1.32x slower                                                 |
| async_tree_none_tg         | 262 ms                                                                 | 345 ms: 1.32x slower                                                  |
| deepcopy_reduce            | 2.60 us                                                                | 3.44 us: 1.32x slower                                                 |
| async_tree_memoization     | 339 ms                                                                 | 453 ms: 1.34x slower                                                  |
| pprint_safe_repr           | 715 ms                                                                 | 959 ms: 1.34x slower                                                  |
| crypto_pyaes               | 68.1 ms                                                                | 91.6 ms: 1.34x slower                                                 |
| pycparser                  | 1.13 sec                                                               | 1.53 sec: 1.35x slower                                                |
| async_tree_none            | 276 ms                                                                 | 374 ms: 1.36x slower                                                  |
| pprint_pformat             | 1.45 sec                                                               | 1.99 sec: 1.37x slower                                                |
| genshi_text                | 22.3 ms                                                                | 30.4 ms: 1.37x slower                                                 |
| python_startup_no_site     | 7.43 ms                                                                | 10.2 ms: 1.38x slower                                                 |
| regex_compile              | 130 ms                                                                 | 179 ms: 1.38x slower                                                  |
| async_tree_memoization_tg  | 314 ms                                                                 | 432 ms: 1.38x slower                                                  |
| subparsers                 | 22.1 ms                                                                | 30.9 ms: 1.40x slower                                                 |
| 2to3                       | 257 ms                                                                 | 361 ms: 1.40x slower                                                  |
| django_template            | 35.6 ms                                                                | 50.2 ms: 1.41x slower                                                 |
| sympy_integrate            | 20.1 ms                                                                | 29.3 ms: 1.46x slower                                                 |
| mako                       | 11.5 ms                                                                | 16.8 ms: 1.46x slower                                                 |
| sqlalchemy_imperative      | 19.4 ms                                                                | 28.8 ms: 1.49x slower                                                 |
| thrift                     | 736 us                                                                 | 1.11 ms: 1.51x slower                                                 |
| unpickle_pure_python       | 216 us                                                                 | 331 us: 1.53x slower                                                  |
| pyflate                    | 448 ms                                                                 | 690 ms: 1.54x slower                                                  |
| logging_format             | 7.04 us                                                                | 10.9 us: 1.55x slower                                                 |
| logging_simple             | 6.27 us                                                                | 9.82 us: 1.57x slower                                                 |
| comprehensions             | 17.3 us                                                                | 27.5 us: 1.59x slower                                                 |
| sqlalchemy_declarative     | 127 ms                                                                 | 201 ms: 1.59x slower                                                  |
| richards_super             | 52.7 ms                                                                | 85.5 ms: 1.62x slower                                                 |
| richards                   | 46.7 ms                                                                | 76.1 ms: 1.63x slower                                                 |
| hexiom                     | 5.99 ms                                                                | 9.78 ms: 1.63x slower                                                 |
| pickle_pure_python         | 316 us                                                                 | 518 us: 1.64x slower                                                  |
| scimark_lu                 | 109 ms                                                                 | 182 ms: 1.67x slower                                                  |
| chaos                      | 60.1 ms                                                                | 103 ms: 1.71x slower                                                  |
| sympy_str                  | 277 ms                                                                 | 474 ms: 1.71x slower                                                  |
| logging_silent             | 105 ns                                                                 | 184 ns: 1.75x slower                                                  |
| float                      | 78.6 ms                                                                | 137 ms: 1.75x slower                                                  |
| scimark_sor                | 133 ms                                                                 | 233 ms: 1.75x slower                                                  |
| scimark_monte_carlo        | 65.6 ms                                                                | 119 ms: 1.81x slower                                                  |
| sqlglot_transpile          | 1.61 ms                                                                | 2.93 ms: 1.82x slower                                                 |
| sqlglot_parse              | 1.30 ms                                                                | 2.54 ms: 1.95x slower                                                 |
| sympy_expand               | 460 ms                                                                 | 952 ms: 2.07x slower                                                  |
| raytrace                   | 265 ms                                                                 | 551 ms: 2.08x slower                                                  |
| go                         | 120 ms                                                                 | 266 ms: 2.22x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 348 ms: 2.26x slower                                                  |
| deltablue                  | 3.25 ms                                                                | 8.08 ms: 2.49x slower                                                 |
| bench_thread_pool          | 1.02 ms                                                                | 3.32 ms: 3.26x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.35x slower                                                          |
Ignored benchmarks (1) of results/bm-20241205-3.14.0a2+-eb8ce39-NOGIL/bm-20241205-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-eb8ce39.json: html5lib

- Geometric mean (including insignificant results): 1.251x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.19x