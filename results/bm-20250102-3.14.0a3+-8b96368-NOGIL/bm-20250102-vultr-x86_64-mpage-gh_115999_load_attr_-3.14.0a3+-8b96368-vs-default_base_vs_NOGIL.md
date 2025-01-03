# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 8b96368
- commit date: 2025-01-02
- overall geometric mean: 1.142x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                 | 312 ms: 1.23x slower                                                  |
| docutils       | 2.55 sec                                                               | 2.84 sec: 1.11x slower                                                |
| sphinx         | 981 ms                                                                 | 1.13 sec: 1.15x slower                                                |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 250 ms                                                                 | 233 ms: 1.07x faster                                                  |
| async_tree_io_tg           | 603 ms                                                                 | 577 ms: 1.04x faster                                                  |
| async_tree_io              | 609 ms                                                                 | 594 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                 | 471 ms: 1.02x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 517 ms: 1.01x faster                                                  |
| async_tree_memoization_tg  | 298 ms                                                                 | 303 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 506 ms: 1.02x slower                                                  |
| async_tree_none            | 272 ms                                                                 | 276 ms: 1.02x slower                                                  |
| async_tree_memoization     | 327 ms                                                                 | 343 ms: 1.05x slower                                                  |
| async_generators           | 355 ms                                                                 | 416 ms: 1.17x slower                                                  |
| coroutines                 | 20.8 ms                                                                | 25.1 ms: 1.21x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 192 ms                                                                 | 190 ms: 1.01x faster                                                  |
| float          | 72.2 ms                                                                | 77.7 ms: 1.08x slower                                                 |
| nbody          | 92.1 ms                                                                | 127 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 182 ms                                                                 | 171 ms: 1.07x faster                                                  |
| regex_v8       | 25.0 ms                                                                | 23.8 ms: 1.05x faster                                                 |
| regex_effbot   | 2.83 ms                                                                | 2.88 ms: 1.02x slower                                                 |
| regex_compile  | 127 ms                                                                 | 150 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.4 ms                                                                | 87.6 ms: 1.03x faster                                                 |
| xml_etree_parse      | 127 ms                                                                 | 129 ms: 1.01x slower                                                  |
| json_loads           | 25.9 us                                                                | 27.7 us: 1.07x slower                                                 |
| json_dumps           | 11.2 ms                                                                | 12.9 ms: 1.16x slower                                                 |
| xml_etree_generate   | 82.7 ms                                                                | 96.5 ms: 1.17x slower                                                 |
| unpickle_pure_python | 211 us                                                                 | 248 us: 1.17x slower                                                  |
| xml_etree_process    | 58.0 ms                                                                | 68.9 ms: 1.19x slower                                                 |
| pickle_pure_python   | 312 us                                                                 | 375 us: 1.20x slower                                                  |
| tomli_loads          | 1.88 sec                                                               | 2.51 sec: 1.33x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.4 ms: 1.05x slower                                                 |
| python_startup_no_site | 7.51 ms                                                                | 9.71 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.8 ms                                                                | 42.8 ms: 1.23x slower                                                 |
| genshi_xml      | 48.3 ms                                                                | 59.5 ms: 1.23x slower                                                 |
| genshi_text     | 21.1 ms                                                                | 28.1 ms: 1.33x slower                                                 |
| mako            | 11.7 ms                                                                | 15.5 ms: 1.33x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.29 ms                                                                | 3.30 ms: 1.30x faster                                                 |
| async_tree_none_tg         | 250 ms                                                                 | 233 ms: 1.07x faster                                                  |
| regex_dna                  | 182 ms                                                                 | 171 ms: 1.07x faster                                                  |
| sqlite_synth               | 2.21 us                                                                | 2.08 us: 1.06x faster                                                 |
| regex_v8                   | 25.0 ms                                                                | 23.8 ms: 1.05x faster                                                 |
| async_tree_io_tg           | 603 ms                                                                 | 577 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 90.4 ms                                                                | 87.6 ms: 1.03x faster                                                 |
| create_gc_cycles           | 1.84 ms                                                                | 1.80 ms: 1.03x faster                                                 |
| async_tree_io              | 609 ms                                                                 | 594 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                 | 471 ms: 1.02x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 517 ms: 1.01x faster                                                  |
| pidigits                   | 192 ms                                                                 | 190 ms: 1.01x faster                                                  |
| xml_etree_parse            | 127 ms                                                                 | 129 ms: 1.01x slower                                                  |
| async_tree_memoization_tg  | 298 ms                                                                 | 303 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 506 ms: 1.02x slower                                                  |
| async_tree_none            | 272 ms                                                                 | 276 ms: 1.02x slower                                                  |
| regex_effbot               | 2.83 ms                                                                | 2.88 ms: 1.02x slower                                                 |
| json                       | 4.72 ms                                                                | 4.85 ms: 1.03x slower                                                 |
| async_tree_memoization     | 327 ms                                                                 | 343 ms: 1.05x slower                                                  |
| python_startup             | 14.7 ms                                                                | 15.4 ms: 1.05x slower                                                 |
| pathlib                    | 18.0 ms                                                                | 19.1 ms: 1.06x slower                                                 |
| json_loads                 | 25.9 us                                                                | 27.7 us: 1.07x slower                                                 |
| mdp                        | 2.44 sec                                                               | 2.61 sec: 1.07x slower                                                |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                                |
| float                      | 72.2 ms                                                                | 77.7 ms: 1.08x slower                                                 |
| bench_mp_pool              | 89.5 ms                                                                | 97.7 ms: 1.09x slower                                                 |
| dulwich_log                | 74.6 ms                                                                | 82.6 ms: 1.11x slower                                                 |
| logging_silent             | 103 ns                                                                 | 115 ns: 1.11x slower                                                  |
| docutils                   | 2.55 sec                                                               | 2.84 sec: 1.11x slower                                                |
| generators                 | 27.3 ms                                                                | 30.6 ms: 1.12x slower                                                 |
| bpe_tokeniser              | 4.23 sec                                                               | 4.79 sec: 1.13x slower                                                |
| k_core                     | 2.04 sec                                                               | 2.32 sec: 1.14x slower                                                |
| subparsers                 | 22.0 ms                                                                | 25.3 ms: 1.15x slower                                                 |
| sphinx                     | 981 ms                                                                 | 1.13 sec: 1.15x slower                                                |
| many_optionals             | 1.03 ms                                                                | 1.18 ms: 1.15x slower                                                 |
| telco                      | 7.27 ms                                                                | 8.40 ms: 1.16x slower                                                 |
| json_dumps                 | 11.2 ms                                                                | 12.9 ms: 1.16x slower                                                 |
| xml_etree_generate         | 82.7 ms                                                                | 96.5 ms: 1.17x slower                                                 |
| async_generators           | 355 ms                                                                 | 416 ms: 1.17x slower                                                  |
| sqlglot_normalize          | 103 ms                                                                 | 121 ms: 1.17x slower                                                  |
| unpickle_pure_python       | 211 us                                                                 | 248 us: 1.17x slower                                                  |
| regex_compile              | 127 ms                                                                 | 150 ms: 1.17x slower                                                  |
| pylint                     | 278 ms                                                                 | 327 ms: 1.18x slower                                                  |
| scimark_fft                | 313 ms                                                                 | 371 ms: 1.19x slower                                                  |
| spectral_norm              | 93.8 ms                                                                | 111 ms: 1.19x slower                                                  |
| xml_etree_process          | 58.0 ms                                                                | 68.9 ms: 1.19x slower                                                 |
| sqlglot_optimize           | 52.1 ms                                                                | 62.0 ms: 1.19x slower                                                 |
| pickle_pure_python         | 312 us                                                                 | 375 us: 1.20x slower                                                  |
| coroutines                 | 20.8 ms                                                                | 25.1 ms: 1.21x slower                                                 |
| pprint_safe_repr           | 685 ms                                                                 | 827 ms: 1.21x slower                                                  |
| sympy_expand               | 458 ms                                                                 | 553 ms: 1.21x slower                                                  |
| sympy_sum                  | 153 ms                                                                 | 186 ms: 1.21x slower                                                  |
| scimark_sparse_mat_mult    | 4.43 ms                                                                | 5.41 ms: 1.22x slower                                                 |
| deepcopy                   | 255 us                                                                 | 311 us: 1.22x slower                                                  |
| pprint_pformat             | 1.40 sec                                                               | 1.71 sec: 1.22x slower                                                |
| 2to3                       | 254 ms                                                                 | 312 ms: 1.23x slower                                                  |
| logging_simple             | 5.94 us                                                                | 7.29 us: 1.23x slower                                                 |
| django_template            | 34.8 ms                                                                | 42.8 ms: 1.23x slower                                                 |
| sympy_integrate            | 19.6 ms                                                                | 24.2 ms: 1.23x slower                                                 |
| genshi_xml                 | 48.3 ms                                                                | 59.5 ms: 1.23x slower                                                 |
| logging_format             | 6.72 us                                                                | 8.30 us: 1.24x slower                                                 |
| chaos                      | 57.7 ms                                                                | 71.3 ms: 1.24x slower                                                 |
| scimark_lu                 | 111 ms                                                                 | 138 ms: 1.24x slower                                                  |
| comprehensions             | 17.0 us                                                                | 21.1 us: 1.24x slower                                                 |
| raytrace                   | 259 ms                                                                 | 322 ms: 1.25x slower                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.93 ms: 1.25x slower                                                 |
| go                         | 115 ms                                                                 | 144 ms: 1.25x slower                                                  |
| pyflate                    | 413 ms                                                                 | 518 ms: 1.25x slower                                                  |
| sympy_str                  | 270 ms                                                                 | 340 ms: 1.26x slower                                                  |
| shortest_path              | 430 ms                                                                 | 542 ms: 1.26x slower                                                  |
| coverage                   | 79.8 ms                                                                | 101 ms: 1.26x slower                                                  |
| connected_components       | 389 ms                                                                 | 490 ms: 1.26x slower                                                  |
| deepcopy_reduce            | 2.56 us                                                                | 3.25 us: 1.27x slower                                                 |
| sqlalchemy_imperative      | 19.0 ms                                                                | 24.1 ms: 1.27x slower                                                 |
| sqlalchemy_declarative     | 127 ms                                                                 | 162 ms: 1.27x slower                                                  |
| nqueens                    | 78.1 ms                                                                | 99.4 ms: 1.27x slower                                                 |
| hexiom                     | 5.93 ms                                                                | 7.59 ms: 1.28x slower                                                 |
| sqlglot_parse              | 1.24 ms                                                                | 1.59 ms: 1.29x slower                                                 |
| thrift                     | 729 us                                                                 | 940 us: 1.29x slower                                                  |
| python_startup_no_site     | 7.51 ms                                                                | 9.71 ms: 1.29x slower                                                 |
| typing_runtime_protocols   | 154 us                                                                 | 200 us: 1.30x slower                                                  |
| meteor_contest             | 99.3 ms                                                                | 129 ms: 1.30x slower                                                  |
| crypto_pyaes               | 66.5 ms                                                                | 86.6 ms: 1.30x slower                                                 |
| richards                   | 41.9 ms                                                                | 54.9 ms: 1.31x slower                                                 |
| deepcopy_memo              | 29.4 us                                                                | 38.7 us: 1.32x slower                                                 |
| tomli_loads                | 1.88 sec                                                               | 2.51 sec: 1.33x slower                                                |
| genshi_text                | 21.1 ms                                                                | 28.1 ms: 1.33x slower                                                 |
| mako                       | 11.7 ms                                                                | 15.5 ms: 1.33x slower                                                 |
| richards_super             | 48.0 ms                                                                | 64.1 ms: 1.34x slower                                                 |
| scimark_monte_carlo        | 63.0 ms                                                                | 85.0 ms: 1.35x slower                                                 |
| fannkuch                   | 364 ms                                                                 | 492 ms: 1.35x slower                                                  |
| nbody                      | 92.1 ms                                                                | 127 ms: 1.38x slower                                                  |
| scimark_sor                | 113 ms                                                                 | 161 ms: 1.42x slower                                                  |
| deltablue                  | 3.11 ms                                                                | 4.81 ms: 1.55x slower                                                 |
| bench_thread_pool          | 1.03 ms                                                                | 3.35 ms: 3.26x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.18x slower                                                          |
Ignored benchmarks (1) of results/bm-20250102-3.14.0a3+-8b96368-NOGIL/bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368.json: html5lib

- Geometric mean (including insignificant results): 1.142x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.20x