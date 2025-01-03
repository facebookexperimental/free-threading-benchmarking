# Results vs. base

- fork: mpage
- ref: measure_non_deferred
- machine: linux-x86_64
- commit hash: b4b58dd
- commit date: 2025-01-03
- overall geometric mean: 1.124x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 351 ms                                                                 | 312 ms: 1.12x faster                                                  |
| docutils       | 3.00 sec                                                               | 2.80 sec: 1.07x faster                                                |
| html5lib       | 93.4 ms                                                                | 72.1 ms: 1.29x faster                                                 |
| sphinx         | 1.16 sec                                                               | 1.11 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                                  | 1.13x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 309 ms                                                                 | 232 ms: 1.33x faster                                                  |
| async_tree_memoization_tg  | 391 ms                                                                 | 303 ms: 1.29x faster                                                  |
| async_tree_none            | 348 ms                                                                 | 277 ms: 1.26x faster                                                  |
| async_tree_io_tg           | 719 ms                                                                 | 574 ms: 1.25x faster                                                  |
| async_tree_io              | 749 ms                                                                 | 600 ms: 1.25x faster                                                  |
| async_tree_memoization     | 422 ms                                                                 | 341 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed_tg | 563 ms                                                                 | 478 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 592 ms                                                                 | 514 ms: 1.15x faster                                                  |
| async_generators           | 451 ms                                                                 | 419 ms: 1.08x faster                                                  |
| coroutines                 | 24.4 ms                                                                | 25.2 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.18x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 108 ms                                                                 | 79.9 ms: 1.35x faster                                                 |
| pidigits       | 193 ms                                                                 | 183 ms: 1.05x faster                                                  |
| nbody          | 129 ms                                                                 | 132 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.12x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 170 ms                                                                 | 151 ms: 1.13x faster                                                  |
| regex_effbot   | 2.71 ms                                                                | 2.80 ms: 1.03x slower                                                 |
| regex_dna      | 178 ms                                                                 | 186 ms: 1.04x slower                                                  |
| regex_v8       | 23.3 ms                                                                | 24.4 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 499 us                                                                 | 363 us: 1.38x faster                                                  |
| unpickle_pure_python | 327 us                                                                 | 254 us: 1.29x faster                                                  |
| xml_etree_process    | 74.0 ms                                                                | 68.7 ms: 1.08x faster                                                 |
| json_dumps           | 13.9 ms                                                                | 12.9 ms: 1.08x faster                                                 |
| xml_etree_generate   | 97.7 ms                                                                | 95.9 ms: 1.02x faster                                                 |
| tomli_loads          | 2.55 sec                                                               | 2.52 sec: 1.02x faster                                                |
| xml_etree_iterparse  | 89.5 ms                                                                | 88.2 ms: 1.01x faster                                                 |
| json_loads           | 28.1 us                                                                | 27.7 us: 1.01x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.00x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.09x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.6 ms                                                                | 15.5 ms: 1.01x faster                                                 |
| python_startup_no_site | 9.76 ms                                                                | 9.70 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 49.6 ms                                                                | 43.2 ms: 1.15x faster                                                 |
| mako            | 17.2 ms                                                                | 15.7 ms: 1.10x faster                                                 |
| genshi_text     | 31.0 ms                                                                | 28.4 ms: 1.09x faster                                                 |
| genshi_xml      | 63.9 ms                                                                | 60.0 ms: 1.06x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.10x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250102-vultr-x86_64-python-8eebe4e6d02bb4ad3f1c-3.14.0a3+-8eebe4e | bm-20250103-vultr-x86_64-mpage-measure_non_deferred-3.14.0a3+-b4b58dd |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| deltablue                  | 7.39 ms                                                                | 4.41 ms: 1.68x faster                                                 |
| go                         | 238 ms                                                                 | 144 ms: 1.65x faster                                                  |
| logging_silent             | 181 ns                                                                 | 114 ns: 1.59x faster                                                  |
| raytrace                   | 489 ms                                                                 | 324 ms: 1.51x faster                                                  |
| sqlglot_parse              | 2.32 ms                                                                | 1.57 ms: 1.48x faster                                                 |
| sqlglot_transpile          | 2.69 ms                                                                | 1.90 ms: 1.41x faster                                                 |
| pickle_pure_python         | 499 us                                                                 | 363 us: 1.38x faster                                                  |
| float                      | 108 ms                                                                 | 79.9 ms: 1.35x faster                                                 |
| chaos                      | 96.0 ms                                                                | 71.4 ms: 1.34x faster                                                 |
| async_tree_none_tg         | 309 ms                                                                 | 232 ms: 1.33x faster                                                  |
| scimark_monte_carlo        | 106 ms                                                                 | 79.8 ms: 1.33x faster                                                 |
| scimark_sor                | 216 ms                                                                 | 164 ms: 1.32x faster                                                  |
| html5lib                   | 93.4 ms                                                                | 72.1 ms: 1.29x faster                                                 |
| async_tree_memoization_tg  | 391 ms                                                                 | 303 ms: 1.29x faster                                                  |
| comprehensions             | 27.2 us                                                                | 21.0 us: 1.29x faster                                                 |
| pyflate                    | 665 ms                                                                 | 515 ms: 1.29x faster                                                  |
| unpickle_pure_python       | 327 us                                                                 | 254 us: 1.29x faster                                                  |
| async_tree_none            | 348 ms                                                                 | 277 ms: 1.26x faster                                                  |
| hexiom                     | 9.62 ms                                                                | 7.67 ms: 1.25x faster                                                 |
| async_tree_io_tg           | 719 ms                                                                 | 574 ms: 1.25x faster                                                  |
| async_tree_io              | 749 ms                                                                 | 600 ms: 1.25x faster                                                  |
| logging_simple             | 9.10 us                                                                | 7.29 us: 1.25x faster                                                 |
| logging_format             | 10.3 us                                                                | 8.34 us: 1.24x faster                                                 |
| async_tree_memoization     | 422 ms                                                                 | 341 ms: 1.24x faster                                                  |
| generators                 | 38.3 ms                                                                | 31.0 ms: 1.24x faster                                                 |
| richards                   | 67.6 ms                                                                | 55.0 ms: 1.23x faster                                                 |
| richards_super             | 76.5 ms                                                                | 64.7 ms: 1.18x faster                                                 |
| async_tree_cpu_io_mixed_tg | 563 ms                                                                 | 478 ms: 1.18x faster                                                  |
| pprint_pformat             | 1.97 sec                                                               | 1.70 sec: 1.16x faster                                                |
| async_tree_cpu_io_mixed    | 592 ms                                                                 | 514 ms: 1.15x faster                                                  |
| django_template            | 49.6 ms                                                                | 43.2 ms: 1.15x faster                                                 |
| pprint_safe_repr           | 943 ms                                                                 | 822 ms: 1.15x faster                                                  |
| sqlalchemy_imperative      | 27.3 ms                                                                | 23.8 ms: 1.14x faster                                                 |
| thrift                     | 1.01 ms                                                                | 885 us: 1.14x faster                                                  |
| sqlalchemy_declarative     | 182 ms                                                                 | 161 ms: 1.13x faster                                                  |
| pycparser                  | 1.37 sec                                                               | 1.21 sec: 1.13x faster                                                |
| regex_compile              | 170 ms                                                                 | 151 ms: 1.13x faster                                                  |
| crypto_pyaes               | 90.1 ms                                                                | 80.2 ms: 1.12x faster                                                 |
| 2to3                       | 351 ms                                                                 | 312 ms: 1.12x faster                                                  |
| subparsers                 | 28.4 ms                                                                | 25.4 ms: 1.12x faster                                                 |
| sqlglot_normalize          | 133 ms                                                                 | 119 ms: 1.11x faster                                                  |
| scimark_lu                 | 155 ms                                                                 | 140 ms: 1.10x faster                                                  |
| mako                       | 17.2 ms                                                                | 15.7 ms: 1.10x faster                                                 |
| dulwich_log                | 90.0 ms                                                                | 82.1 ms: 1.10x faster                                                 |
| genshi_text                | 31.0 ms                                                                | 28.4 ms: 1.09x faster                                                 |
| sqlglot_optimize           | 66.6 ms                                                                | 61.7 ms: 1.08x faster                                                 |
| xml_etree_process          | 74.0 ms                                                                | 68.7 ms: 1.08x faster                                                 |
| json_dumps                 | 13.9 ms                                                                | 12.9 ms: 1.08x faster                                                 |
| async_generators           | 451 ms                                                                 | 419 ms: 1.08x faster                                                  |
| docutils                   | 3.00 sec                                                               | 2.80 sec: 1.07x faster                                                |
| sympy_expand               | 584 ms                                                                 | 546 ms: 1.07x faster                                                  |
| sympy_str                  | 355 ms                                                                 | 332 ms: 1.07x faster                                                  |
| gc_traversal               | 3.52 ms                                                                | 3.30 ms: 1.07x faster                                                 |
| pylint                     | 347 ms                                                                 | 326 ms: 1.07x faster                                                  |
| genshi_xml                 | 63.9 ms                                                                | 60.0 ms: 1.06x faster                                                 |
| sympy_sum                  | 195 ms                                                                 | 185 ms: 1.06x faster                                                  |
| deepcopy_reduce            | 3.40 us                                                                | 3.21 us: 1.06x faster                                                 |
| pidigits                   | 193 ms                                                                 | 183 ms: 1.05x faster                                                  |
| deepcopy_memo              | 40.8 us                                                                | 38.9 us: 1.05x faster                                                 |
| bpe_tokeniser              | 5.04 sec                                                               | 4.80 sec: 1.05x faster                                                |
| sympy_integrate            | 25.2 ms                                                                | 24.1 ms: 1.05x faster                                                 |
| many_optionals             | 1.24 ms                                                                | 1.18 ms: 1.05x faster                                                 |
| sphinx                     | 1.16 sec                                                               | 1.11 sec: 1.04x faster                                                |
| deepcopy                   | 324 us                                                                 | 311 us: 1.04x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 18.6 ms: 1.04x faster                                                 |
| typing_runtime_protocols   | 207 us                                                                 | 200 us: 1.03x faster                                                  |
| mdp                        | 2.69 sec                                                               | 2.61 sec: 1.03x faster                                                |
| telco                      | 8.66 ms                                                                | 8.43 ms: 1.03x faster                                                 |
| scimark_sparse_mat_mult    | 5.58 ms                                                                | 5.44 ms: 1.03x faster                                                 |
| create_gc_cycles           | 1.85 ms                                                                | 1.80 ms: 1.02x faster                                                 |
| bench_mp_pool              | 100 ms                                                                 | 97.8 ms: 1.02x faster                                                 |
| json                       | 5.00 ms                                                                | 4.89 ms: 1.02x faster                                                 |
| connected_components       | 499 ms                                                                 | 490 ms: 1.02x faster                                                  |
| xml_etree_generate         | 97.7 ms                                                                | 95.9 ms: 1.02x faster                                                 |
| k_core                     | 2.35 sec                                                               | 2.31 sec: 1.02x faster                                                |
| sqlite_synth               | 2.11 us                                                                | 2.08 us: 1.02x faster                                                 |
| shortest_path              | 550 ms                                                                 | 541 ms: 1.02x faster                                                  |
| bench_thread_pool          | 3.37 ms                                                                | 3.32 ms: 1.02x faster                                                 |
| tomli_loads                | 2.55 sec                                                               | 2.52 sec: 1.02x faster                                                |
| xml_etree_iterparse        | 89.5 ms                                                                | 88.2 ms: 1.01x faster                                                 |
| json_loads                 | 28.1 us                                                                | 27.7 us: 1.01x faster                                                 |
| python_startup             | 15.6 ms                                                                | 15.5 ms: 1.01x faster                                                 |
| python_startup_no_site     | 9.76 ms                                                                | 9.70 ms: 1.01x faster                                                 |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.00x slower                                                  |
| coverage                   | 98.7 ms                                                                | 99.2 ms: 1.01x slower                                                 |
| fannkuch                   | 495 ms                                                                 | 499 ms: 1.01x slower                                                  |
| scimark_fft                | 377 ms                                                                 | 382 ms: 1.01x slower                                                  |
| spectral_norm              | 113 ms                                                                 | 115 ms: 1.01x slower                                                  |
| nbody                      | 129 ms                                                                 | 132 ms: 1.02x slower                                                  |
| regex_effbot               | 2.71 ms                                                                | 2.80 ms: 1.03x slower                                                 |
| coroutines                 | 24.4 ms                                                                | 25.2 ms: 1.03x slower                                                 |
| regex_dna                  | 178 ms                                                                 | 186 ms: 1.04x slower                                                  |
| regex_v8                   | 23.3 ms                                                                | 24.4 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.12x faster                                                          |

Benchmark hidden because not significant (3): meteor_contest, nqueens, asyncio_websockets

- Geometric mean (including insignificant results): 1.124x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.02x