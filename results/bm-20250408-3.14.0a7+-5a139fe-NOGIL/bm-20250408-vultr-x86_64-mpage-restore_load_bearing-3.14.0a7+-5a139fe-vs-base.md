# Results vs. base

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: 5a139fe
- commit date: 2025-04-08
- overall geometric mean: 1.076x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 311 ms                                                                 | 289 ms: 1.07x faster                                                  |
| docutils       | 2.91 sec                                                               | 2.77 sec: 1.05x faster                                                |
| html5lib       | 76.5 ms                                                                | 70.0 ms: 1.09x faster                                                 |
| sphinx         | 1.15 sec                                                               | 1.09 sec: 1.06x faster                                                |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 26.9 ms                                                                | 23.6 ms: 1.14x faster                                                 |
| async_tree_none            | 285 ms                                                                 | 267 ms: 1.07x faster                                                  |
| async_tree_memoization     | 342 ms                                                                 | 321 ms: 1.07x faster                                                  |
| async_tree_cpu_io_mixed    | 548 ms                                                                 | 516 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 514 ms                                                                 | 486 ms: 1.06x faster                                                  |
| async_tree_io              | 599 ms                                                                 | 567 ms: 1.06x faster                                                  |
| async_tree_memoization_tg  | 309 ms                                                                 | 293 ms: 1.05x faster                                                  |
| async_tree_io_tg           | 566 ms                                                                 | 538 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 244 ms                                                                 | 234 ms: 1.05x faster                                                  |
| async_generators           | 386 ms                                                                 | 372 ms: 1.04x faster                                                  |
| asyncio_websockets         | 515 ms                                                                 | 517 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 134 ms                                                                 | 116 ms: 1.15x faster                                                  |
| float          | 77.6 ms                                                                | 70.4 ms: 1.10x faster                                                 |
| pidigits       | 211 ms                                                                 | 193 ms: 1.09x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 170 ms                                                                 | 151 ms: 1.12x faster                                                  |
| regex_effbot   | 2.87 ms                                                                | 2.85 ms: 1.01x faster                                                 |
| regex_dna      | 178 ms                                                                 | 181 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.53 sec                                                               | 2.25 sec: 1.12x faster                                                |
| unpickle_pure_python | 268 us                                                                 | 240 us: 1.12x faster                                                  |
| pickle_pure_python   | 382 us                                                                 | 343 us: 1.11x faster                                                  |
| xml_etree_process    | 74.4 ms                                                                | 69.2 ms: 1.07x faster                                                 |
| xml_etree_generate   | 102 ms                                                                 | 95.6 ms: 1.06x faster                                                 |
| xml_etree_iterparse  | 91.9 ms                                                                | 87.0 ms: 1.06x faster                                                 |
| json_dumps           | 13.2 ms                                                                | 12.8 ms: 1.03x faster                                                 |
| json_loads           | 31.1 us                                                                | 30.5 us: 1.02x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 16.0 ms                                                                | 15.9 ms: 1.01x faster                                                 |
| python_startup_no_site | 11.2 ms                                                                | 11.2 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.9 ms                                                                | 58.5 ms: 1.16x faster                                                 |
| genshi_text     | 31.3 ms                                                                | 27.3 ms: 1.15x faster                                                 |
| django_template | 45.0 ms                                                                | 41.9 ms: 1.07x faster                                                 |
| mako            | 16.5 ms                                                                | 15.8 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.11x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| generators                 | 44.6 ms                                                                | 33.0 ms: 1.35x faster                                                 |
| scimark_sor                | 161 ms                                                                 | 128 ms: 1.26x faster                                                  |
| logging_format             | 9.79 us                                                                | 8.24 us: 1.19x faster                                                 |
| logging_simple             | 8.67 us                                                                | 7.32 us: 1.18x faster                                                 |
| deltablue                  | 4.44 ms                                                                | 3.75 ms: 1.18x faster                                                 |
| genshi_xml                 | 67.9 ms                                                                | 58.5 ms: 1.16x faster                                                 |
| nbody                      | 134 ms                                                                 | 116 ms: 1.15x faster                                                  |
| genshi_text                | 31.3 ms                                                                | 27.3 ms: 1.15x faster                                                 |
| go                         | 152 ms                                                                 | 133 ms: 1.15x faster                                                  |
| hexiom                     | 8.08 ms                                                                | 7.07 ms: 1.14x faster                                                 |
| coroutines                 | 26.9 ms                                                                | 23.6 ms: 1.14x faster                                                 |
| chaos                      | 72.5 ms                                                                | 63.6 ms: 1.14x faster                                                 |
| logging_silent             | 125 ns                                                                 | 110 ns: 1.13x faster                                                  |
| richards                   | 60.7 ms                                                                | 53.8 ms: 1.13x faster                                                 |
| scimark_monte_carlo        | 87.4 ms                                                                | 77.5 ms: 1.13x faster                                                 |
| nqueens                    | 102 ms                                                                 | 90.2 ms: 1.13x faster                                                 |
| richards_super             | 68.9 ms                                                                | 61.2 ms: 1.13x faster                                                 |
| tomli_loads                | 2.53 sec                                                               | 2.25 sec: 1.12x faster                                                |
| regex_compile              | 170 ms                                                                 | 151 ms: 1.12x faster                                                  |
| raytrace                   | 339 ms                                                                 | 303 ms: 1.12x faster                                                  |
| unpickle_pure_python       | 268 us                                                                 | 240 us: 1.12x faster                                                  |
| fannkuch                   | 515 ms                                                                 | 463 ms: 1.11x faster                                                  |
| pickle_pure_python         | 382 us                                                                 | 343 us: 1.11x faster                                                  |
| spectral_norm              | 121 ms                                                                 | 109 ms: 1.11x faster                                                  |
| comprehensions             | 22.1 us                                                                | 20.1 us: 1.10x faster                                                 |
| float                      | 77.6 ms                                                                | 70.4 ms: 1.10x faster                                                 |
| pyflate                    | 520 ms                                                                 | 475 ms: 1.10x faster                                                  |
| deepcopy                   | 326 us                                                                 | 298 us: 1.09x faster                                                  |
| html5lib                   | 76.5 ms                                                                | 70.0 ms: 1.09x faster                                                 |
| pidigits                   | 211 ms                                                                 | 193 ms: 1.09x faster                                                  |
| sqlglot_v2_transpile       | 2.01 ms                                                                | 1.85 ms: 1.09x faster                                                 |
| pprint_safe_repr           | 867 ms                                                                 | 798 ms: 1.09x faster                                                  |
| sqlglot_v2_normalize       | 129 ms                                                                 | 118 ms: 1.09x faster                                                  |
| deepcopy_memo              | 39.9 us                                                                | 36.7 us: 1.09x faster                                                 |
| pprint_pformat             | 1.80 sec                                                               | 1.66 sec: 1.08x faster                                                |
| deepcopy_reduce            | 3.26 us                                                                | 3.02 us: 1.08x faster                                                 |
| sqlglot_v2_optimize        | 64.2 ms                                                                | 59.3 ms: 1.08x faster                                                 |
| scimark_sparse_mat_mult    | 5.55 ms                                                                | 5.13 ms: 1.08x faster                                                 |
| sqlglot_v2_parse           | 1.66 ms                                                                | 1.54 ms: 1.08x faster                                                 |
| sympy_expand               | 588 ms                                                                 | 545 ms: 1.08x faster                                                  |
| crypto_pyaes               | 91.3 ms                                                                | 84.6 ms: 1.08x faster                                                 |
| 2to3                       | 311 ms                                                                 | 289 ms: 1.07x faster                                                  |
| xml_etree_process          | 74.4 ms                                                                | 69.2 ms: 1.07x faster                                                 |
| django_template            | 45.0 ms                                                                | 41.9 ms: 1.07x faster                                                 |
| sympy_str                  | 353 ms                                                                 | 329 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 4.95 sec                                                               | 4.62 sec: 1.07x faster                                                |
| mdp                        | 1.46 sec                                                               | 1.36 sec: 1.07x faster                                                |
| pycparser                  | 1.25 sec                                                               | 1.17 sec: 1.07x faster                                                |
| scimark_lu                 | 143 ms                                                                 | 134 ms: 1.07x faster                                                  |
| async_tree_none            | 285 ms                                                                 | 267 ms: 1.07x faster                                                  |
| async_tree_memoization     | 342 ms                                                                 | 321 ms: 1.07x faster                                                  |
| many_optionals             | 1.22 ms                                                                | 1.15 ms: 1.07x faster                                                 |
| xml_etree_generate         | 102 ms                                                                 | 95.6 ms: 1.06x faster                                                 |
| async_tree_cpu_io_mixed    | 548 ms                                                                 | 516 ms: 1.06x faster                                                  |
| dulwich_log                | 78.1 ms                                                                | 73.7 ms: 1.06x faster                                                 |
| scimark_fft                | 379 ms                                                                 | 358 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 514 ms                                                                 | 486 ms: 1.06x faster                                                  |
| sympy_integrate            | 24.3 ms                                                                | 23.0 ms: 1.06x faster                                                 |
| sphinx                     | 1.15 sec                                                               | 1.09 sec: 1.06x faster                                                |
| xml_etree_iterparse        | 91.9 ms                                                                | 87.0 ms: 1.06x faster                                                 |
| typing_runtime_protocols   | 208 us                                                                 | 197 us: 1.06x faster                                                  |
| async_tree_io              | 599 ms                                                                 | 567 ms: 1.06x faster                                                  |
| subparsers                 | 27.1 ms                                                                | 25.7 ms: 1.06x faster                                                 |
| sympy_sum                  | 195 ms                                                                 | 185 ms: 1.06x faster                                                  |
| pylint                     | 333 ms                                                                 | 316 ms: 1.05x faster                                                  |
| sqlalchemy_imperative      | 25.4 ms                                                                | 24.1 ms: 1.05x faster                                                 |
| async_tree_memoization_tg  | 309 ms                                                                 | 293 ms: 1.05x faster                                                  |
| async_tree_io_tg           | 566 ms                                                                 | 538 ms: 1.05x faster                                                  |
| meteor_contest             | 134 ms                                                                 | 128 ms: 1.05x faster                                                  |
| docutils                   | 2.91 sec                                                               | 2.77 sec: 1.05x faster                                                |
| sqlalchemy_declarative     | 165 ms                                                                 | 157 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 244 ms                                                                 | 234 ms: 1.05x faster                                                  |
| connected_components       | 511 ms                                                                 | 489 ms: 1.05x faster                                                  |
| mako                       | 16.5 ms                                                                | 15.8 ms: 1.04x faster                                                 |
| async_generators           | 386 ms                                                                 | 372 ms: 1.04x faster                                                  |
| shortest_path              | 553 ms                                                                 | 534 ms: 1.04x faster                                                  |
| sqlite_synth               | 2.08 us                                                                | 2.02 us: 1.03x faster                                                 |
| json_dumps                 | 13.2 ms                                                                | 12.8 ms: 1.03x faster                                                 |
| json                       | 5.35 ms                                                                | 5.24 ms: 1.02x faster                                                 |
| k_core                     | 2.29 sec                                                               | 2.24 sec: 1.02x faster                                                |
| json_loads                 | 31.1 us                                                                | 30.5 us: 1.02x faster                                                 |
| pathlib                    | 19.9 ms                                                                | 19.7 ms: 1.01x faster                                                 |
| coverage                   | 110 ms                                                                 | 108 ms: 1.01x faster                                                  |
| bench_mp_pool              | 97.4 ms                                                                | 96.2 ms: 1.01x faster                                                 |
| bench_thread_pool          | 3.19 ms                                                                | 3.16 ms: 1.01x faster                                                 |
| regex_effbot               | 2.87 ms                                                                | 2.85 ms: 1.01x faster                                                 |
| python_startup             | 16.0 ms                                                                | 15.9 ms: 1.01x faster                                                 |
| python_startup_no_site     | 11.2 ms                                                                | 11.2 ms: 1.00x faster                                                 |
| asyncio_websockets         | 515 ms                                                                 | 517 ms: 1.00x slower                                                  |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| regex_dna                  | 178 ms                                                                 | 181 ms: 1.02x slower                                                  |
| gc_traversal               | 1.78 ms                                                                | 1.82 ms: 1.02x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                                | 1.38 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (2): telco, regex_v8

- Geometric mean (including insignificant results): 1.076x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.01x