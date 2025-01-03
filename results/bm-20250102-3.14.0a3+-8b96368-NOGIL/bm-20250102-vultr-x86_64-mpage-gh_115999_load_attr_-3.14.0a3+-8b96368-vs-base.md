# Results vs. base

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 8b96368
- commit date: 2025-01-02
- overall geometric mean: 1.123x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 351 ms                                                                 | 312 ms: 1.12x faster                                                  |
| docutils       | 3.00 sec                                                               | 2.84 sec: 1.06x faster                                                |
| html5lib       | 93.4 ms                                                                | 73.6 ms: 1.27x faster                                                 |
| sphinx         | 1.16 sec                                                               | 1.13 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                                  | 1.12x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 309 ms                                                                 | 233 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 391 ms                                                                 | 303 ms: 1.29x faster                                                  |
| async_tree_io              | 749 ms                                                                 | 594 ms: 1.26x faster                                                  |
| async_tree_none            | 348 ms                                                                 | 276 ms: 1.26x faster                                                  |
| async_tree_io_tg           | 719 ms                                                                 | 577 ms: 1.25x faster                                                  |
| async_tree_memoization     | 422 ms                                                                 | 343 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 563 ms                                                                 | 471 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 592 ms                                                                 | 506 ms: 1.17x faster                                                  |
| async_generators           | 451 ms                                                                 | 416 ms: 1.09x faster                                                  |
| coroutines                 | 24.4 ms                                                                | 25.1 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.18x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 108 ms                                                                 | 77.7 ms: 1.39x faster                                                 |
| pidigits       | 193 ms                                                                 | 190 ms: 1.02x faster                                                  |
| nbody          | 129 ms                                                                 | 127 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.13x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 170 ms                                                                 | 150 ms: 1.13x faster                                                  |
| regex_dna      | 178 ms                                                                 | 171 ms: 1.04x faster                                                  |
| regex_v8       | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| regex_effbot   | 2.71 ms                                                                | 2.88 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 499 us                                                                 | 375 us: 1.33x faster                                                  |
| unpickle_pure_python | 327 us                                                                 | 248 us: 1.32x faster                                                  |
| xml_etree_process    | 74.0 ms                                                                | 68.9 ms: 1.08x faster                                                 |
| json_dumps           | 13.9 ms                                                                | 12.9 ms: 1.07x faster                                                 |
| xml_etree_iterparse  | 89.5 ms                                                                | 87.6 ms: 1.02x faster                                                 |
| tomli_loads          | 2.55 sec                                                               | 2.51 sec: 1.02x faster                                                |
| json_loads           | 28.1 us                                                                | 27.7 us: 1.01x faster                                                 |
| xml_etree_generate   | 97.7 ms                                                                | 96.5 ms: 1.01x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 129 ms: 1.01x faster                                                  |
| Geometric mean       | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.6 ms                                                                | 15.4 ms: 1.01x faster                                                 |
| python_startup_no_site | 9.76 ms                                                                | 9.71 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 49.6 ms                                                                | 42.8 ms: 1.16x faster                                                 |
| mako            | 17.2 ms                                                                | 15.5 ms: 1.11x faster                                                 |
| genshi_text     | 31.0 ms                                                                | 28.1 ms: 1.10x faster                                                 |
| genshi_xml      | 63.9 ms                                                                | 59.5 ms: 1.07x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.11x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| go                         | 238 ms                                                                 | 144 ms: 1.66x faster                                                  |
| logging_silent             | 181 ns                                                                 | 115 ns: 1.58x faster                                                  |
| deltablue                  | 7.39 ms                                                                | 4.81 ms: 1.53x faster                                                 |
| raytrace                   | 489 ms                                                                 | 322 ms: 1.52x faster                                                  |
| sqlglot_parse              | 2.32 ms                                                                | 1.59 ms: 1.46x faster                                                 |
| sqlglot_transpile          | 2.69 ms                                                                | 1.93 ms: 1.39x faster                                                 |
| float                      | 108 ms                                                                 | 77.7 ms: 1.39x faster                                                 |
| chaos                      | 96.0 ms                                                                | 71.3 ms: 1.35x faster                                                 |
| scimark_sor                | 216 ms                                                                 | 161 ms: 1.34x faster                                                  |
| pickle_pure_python         | 499 us                                                                 | 375 us: 1.33x faster                                                  |
| async_tree_none_tg         | 309 ms                                                                 | 233 ms: 1.33x faster                                                  |
| unpickle_pure_python       | 327 us                                                                 | 248 us: 1.32x faster                                                  |
| async_tree_memoization_tg  | 391 ms                                                                 | 303 ms: 1.29x faster                                                  |
| comprehensions             | 27.2 us                                                                | 21.1 us: 1.29x faster                                                 |
| pyflate                    | 665 ms                                                                 | 518 ms: 1.28x faster                                                  |
| html5lib                   | 93.4 ms                                                                | 73.6 ms: 1.27x faster                                                 |
| hexiom                     | 9.62 ms                                                                | 7.59 ms: 1.27x faster                                                 |
| async_tree_io              | 749 ms                                                                 | 594 ms: 1.26x faster                                                  |
| async_tree_none            | 348 ms                                                                 | 276 ms: 1.26x faster                                                  |
| generators                 | 38.3 ms                                                                | 30.6 ms: 1.25x faster                                                 |
| logging_simple             | 9.10 us                                                                | 7.29 us: 1.25x faster                                                 |
| logging_format             | 10.3 us                                                                | 8.30 us: 1.25x faster                                                 |
| scimark_monte_carlo        | 106 ms                                                                 | 85.0 ms: 1.25x faster                                                 |
| async_tree_io_tg           | 719 ms                                                                 | 577 ms: 1.25x faster                                                  |
| richards                   | 67.6 ms                                                                | 54.9 ms: 1.23x faster                                                 |
| async_tree_memoization     | 422 ms                                                                 | 343 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 563 ms                                                                 | 471 ms: 1.19x faster                                                  |
| richards_super             | 76.5 ms                                                                | 64.1 ms: 1.19x faster                                                 |
| async_tree_cpu_io_mixed    | 592 ms                                                                 | 506 ms: 1.17x faster                                                  |
| django_template            | 49.6 ms                                                                | 42.8 ms: 1.16x faster                                                 |
| pprint_pformat             | 1.97 sec                                                               | 1.71 sec: 1.15x faster                                                |
| pprint_safe_repr           | 943 ms                                                                 | 827 ms: 1.14x faster                                                  |
| pycparser                  | 1.37 sec                                                               | 1.20 sec: 1.14x faster                                                |
| regex_compile              | 170 ms                                                                 | 150 ms: 1.13x faster                                                  |
| sqlalchemy_imperative      | 27.3 ms                                                                | 24.1 ms: 1.13x faster                                                 |
| sqlalchemy_declarative     | 182 ms                                                                 | 162 ms: 1.13x faster                                                  |
| 2to3                       | 351 ms                                                                 | 312 ms: 1.12x faster                                                  |
| subparsers                 | 28.4 ms                                                                | 25.3 ms: 1.12x faster                                                 |
| scimark_lu                 | 155 ms                                                                 | 138 ms: 1.12x faster                                                  |
| mako                       | 17.2 ms                                                                | 15.5 ms: 1.11x faster                                                 |
| genshi_text                | 31.0 ms                                                                | 28.1 ms: 1.10x faster                                                 |
| sqlglot_normalize          | 133 ms                                                                 | 121 ms: 1.10x faster                                                  |
| dulwich_log                | 90.0 ms                                                                | 82.6 ms: 1.09x faster                                                 |
| async_generators           | 451 ms                                                                 | 416 ms: 1.09x faster                                                  |
| sqlglot_optimize           | 66.6 ms                                                                | 62.0 ms: 1.08x faster                                                 |
| xml_etree_process          | 74.0 ms                                                                | 68.9 ms: 1.08x faster                                                 |
| genshi_xml                 | 63.9 ms                                                                | 59.5 ms: 1.07x faster                                                 |
| json_dumps                 | 13.9 ms                                                                | 12.9 ms: 1.07x faster                                                 |
| thrift                     | 1.01 ms                                                                | 940 us: 1.07x faster                                                  |
| gc_traversal               | 3.52 ms                                                                | 3.30 ms: 1.07x faster                                                 |
| pylint                     | 347 ms                                                                 | 327 ms: 1.06x faster                                                  |
| docutils                   | 3.00 sec                                                               | 2.84 sec: 1.06x faster                                                |
| sympy_expand               | 584 ms                                                                 | 553 ms: 1.06x faster                                                  |
| deepcopy_memo              | 40.8 us                                                                | 38.7 us: 1.06x faster                                                 |
| bpe_tokeniser              | 5.04 sec                                                               | 4.79 sec: 1.05x faster                                                |
| sympy_sum                  | 195 ms                                                                 | 186 ms: 1.05x faster                                                  |
| many_optionals             | 1.24 ms                                                                | 1.18 ms: 1.05x faster                                                 |
| deepcopy_reduce            | 3.40 us                                                                | 3.25 us: 1.05x faster                                                 |
| regex_dna                  | 178 ms                                                                 | 171 ms: 1.04x faster                                                  |
| sympy_integrate            | 25.2 ms                                                                | 24.2 ms: 1.04x faster                                                 |
| sympy_str                  | 355 ms                                                                 | 340 ms: 1.04x faster                                                  |
| deepcopy                   | 324 us                                                                 | 311 us: 1.04x faster                                                  |
| crypto_pyaes               | 90.1 ms                                                                | 86.6 ms: 1.04x faster                                                 |
| scimark_sparse_mat_mult    | 5.58 ms                                                                | 5.41 ms: 1.03x faster                                                 |
| typing_runtime_protocols   | 207 us                                                                 | 200 us: 1.03x faster                                                  |
| json                       | 5.00 ms                                                                | 4.85 ms: 1.03x faster                                                 |
| telco                      | 8.66 ms                                                                | 8.40 ms: 1.03x faster                                                 |
| sphinx                     | 1.16 sec                                                               | 1.13 sec: 1.03x faster                                                |
| mdp                        | 2.69 sec                                                               | 2.61 sec: 1.03x faster                                                |
| create_gc_cycles           | 1.85 ms                                                                | 1.80 ms: 1.03x faster                                                 |
| bench_mp_pool              | 100 ms                                                                 | 97.7 ms: 1.02x faster                                                 |
| meteor_contest             | 132 ms                                                                 | 129 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 89.5 ms                                                                | 87.6 ms: 1.02x faster                                                 |
| pidigits                   | 193 ms                                                                 | 190 ms: 1.02x faster                                                  |
| tomli_loads                | 2.55 sec                                                               | 2.51 sec: 1.02x faster                                                |
| connected_components       | 499 ms                                                                 | 490 ms: 1.02x faster                                                  |
| spectral_norm              | 113 ms                                                                 | 111 ms: 1.02x faster                                                  |
| nbody                      | 129 ms                                                                 | 127 ms: 1.02x faster                                                  |
| scimark_fft                | 377 ms                                                                 | 371 ms: 1.02x faster                                                  |
| shortest_path              | 550 ms                                                                 | 542 ms: 1.01x faster                                                  |
| k_core                     | 2.35 sec                                                               | 2.32 sec: 1.01x faster                                                |
| sqlite_synth               | 2.11 us                                                                | 2.08 us: 1.01x faster                                                 |
| json_loads                 | 28.1 us                                                                | 27.7 us: 1.01x faster                                                 |
| xml_etree_generate         | 97.7 ms                                                                | 96.5 ms: 1.01x faster                                                 |
| python_startup             | 15.6 ms                                                                | 15.4 ms: 1.01x faster                                                 |
| pathlib                    | 19.3 ms                                                                | 19.1 ms: 1.01x faster                                                 |
| bench_thread_pool          | 3.37 ms                                                                | 3.35 ms: 1.01x faster                                                 |
| xml_etree_parse            | 129 ms                                                                 | 129 ms: 1.01x faster                                                  |
| fannkuch                   | 495 ms                                                                 | 492 ms: 1.01x faster                                                  |
| python_startup_no_site     | 9.76 ms                                                                | 9.71 ms: 1.00x faster                                                 |
| nqueens                    | 97.9 ms                                                                | 99.4 ms: 1.02x slower                                                 |
| coverage                   | 98.7 ms                                                                | 101 ms: 1.02x slower                                                  |
| regex_v8                   | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| coroutines                 | 24.4 ms                                                                | 25.1 ms: 1.03x slower                                                 |
| regex_effbot               | 2.71 ms                                                                | 2.88 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.12x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

- Geometric mean (including insignificant results): 1.123x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.02x