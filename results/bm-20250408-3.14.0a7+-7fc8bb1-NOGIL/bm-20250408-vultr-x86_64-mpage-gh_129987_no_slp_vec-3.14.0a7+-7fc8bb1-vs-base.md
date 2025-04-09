# Results vs. base

- fork: mpage
- ref: gh_129987_no_slp_vec
- machine: linux-x86_64
- commit hash: 7fc8bb1
- commit date: 2025-04-08
- overall geometric mean: 1.072x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 311 ms                                                                 | 291 ms: 1.07x faster                                                  |
| docutils       | 2.91 sec                                                               | 2.77 sec: 1.05x faster                                                |
| html5lib       | 76.5 ms                                                                | 70.5 ms: 1.09x faster                                                 |
| sphinx         | 1.15 sec                                                               | 1.09 sec: 1.05x faster                                                |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 26.9 ms                                                                | 23.8 ms: 1.13x faster                                                 |
| async_tree_memoization     | 342 ms                                                                 | 322 ms: 1.06x faster                                                  |
| async_tree_io              | 599 ms                                                                 | 564 ms: 1.06x faster                                                  |
| async_tree_none            | 285 ms                                                                 | 269 ms: 1.06x faster                                                  |
| async_tree_io_tg           | 566 ms                                                                 | 536 ms: 1.06x faster                                                  |
| async_generators           | 386 ms                                                                 | 367 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 244 ms                                                                 | 233 ms: 1.05x faster                                                  |
| async_tree_memoization_tg  | 309 ms                                                                 | 296 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed    | 548 ms                                                                 | 528 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed_tg | 514 ms                                                                 | 498 ms: 1.03x faster                                                  |
| asyncio_websockets         | 515 ms                                                                 | 516 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 134 ms                                                                 | 117 ms: 1.14x faster                                                  |
| float          | 77.6 ms                                                                | 70.1 ms: 1.11x faster                                                 |
| pidigits       | 211 ms                                                                 | 217 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 170 ms                                                                 | 152 ms: 1.11x faster                                                  |
| regex_effbot   | 2.87 ms                                                                | 2.71 ms: 1.06x faster                                                 |
| regex_v8       | 21.3 ms                                                                | 21.0 ms: 1.01x faster                                                 |
| regex_dna      | 178 ms                                                                 | 183 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.53 sec                                                               | 2.27 sec: 1.11x faster                                                |
| unpickle_pure_python | 268 us                                                                 | 243 us: 1.10x faster                                                  |
| pickle_pure_python   | 382 us                                                                 | 350 us: 1.09x faster                                                  |
| xml_etree_process    | 74.4 ms                                                                | 70.2 ms: 1.06x faster                                                 |
| xml_etree_generate   | 102 ms                                                                 | 96.0 ms: 1.06x faster                                                 |
| xml_etree_iterparse  | 91.9 ms                                                                | 87.9 ms: 1.05x faster                                                 |
| json_dumps           | 13.2 ms                                                                | 13.0 ms: 1.01x faster                                                 |
| json_loads           | 31.1 us                                                                | 30.7 us: 1.01x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.05x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 16.0 ms                                                                | 15.9 ms: 1.01x faster                                                 |
| python_startup_no_site | 11.2 ms                                                                | 11.2 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.9 ms                                                                | 58.6 ms: 1.16x faster                                                 |
| genshi_text     | 31.3 ms                                                                | 27.7 ms: 1.13x faster                                                 |
| mako            | 16.5 ms                                                                | 15.5 ms: 1.06x faster                                                 |
| django_template | 45.0 ms                                                                | 42.5 ms: 1.06x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.10x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-7fc8bb1 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| generators                 | 44.6 ms                                                                | 33.5 ms: 1.33x faster                                                 |
| scimark_sor                | 161 ms                                                                 | 129 ms: 1.25x faster                                                  |
| logging_format             | 9.79 us                                                                | 8.21 us: 1.19x faster                                                 |
| logging_simple             | 8.67 us                                                                | 7.32 us: 1.18x faster                                                 |
| deltablue                  | 4.44 ms                                                                | 3.80 ms: 1.17x faster                                                 |
| genshi_xml                 | 67.9 ms                                                                | 58.6 ms: 1.16x faster                                                 |
| spectral_norm              | 121 ms                                                                 | 105 ms: 1.15x faster                                                  |
| nbody                      | 134 ms                                                                 | 117 ms: 1.14x faster                                                  |
| scimark_monte_carlo        | 87.4 ms                                                                | 76.8 ms: 1.14x faster                                                 |
| logging_silent             | 125 ns                                                                 | 110 ns: 1.14x faster                                                  |
| genshi_text                | 31.3 ms                                                                | 27.7 ms: 1.13x faster                                                 |
| coroutines                 | 26.9 ms                                                                | 23.8 ms: 1.13x faster                                                 |
| nqueens                    | 102 ms                                                                 | 90.0 ms: 1.13x faster                                                 |
| go                         | 152 ms                                                                 | 136 ms: 1.12x faster                                                  |
| chaos                      | 72.5 ms                                                                | 64.7 ms: 1.12x faster                                                 |
| hexiom                     | 8.08 ms                                                                | 7.23 ms: 1.12x faster                                                 |
| tomli_loads                | 2.53 sec                                                               | 2.27 sec: 1.11x faster                                                |
| regex_compile              | 170 ms                                                                 | 152 ms: 1.11x faster                                                  |
| richards                   | 60.7 ms                                                                | 54.6 ms: 1.11x faster                                                 |
| float                      | 77.6 ms                                                                | 70.1 ms: 1.11x faster                                                 |
| raytrace                   | 339 ms                                                                 | 307 ms: 1.11x faster                                                  |
| richards_super             | 68.9 ms                                                                | 62.4 ms: 1.10x faster                                                 |
| unpickle_pure_python       | 268 us                                                                 | 243 us: 1.10x faster                                                  |
| deepcopy                   | 326 us                                                                 | 298 us: 1.10x faster                                                  |
| fannkuch                   | 515 ms                                                                 | 471 ms: 1.09x faster                                                  |
| pprint_pformat             | 1.80 sec                                                               | 1.65 sec: 1.09x faster                                                |
| pickle_pure_python         | 382 us                                                                 | 350 us: 1.09x faster                                                  |
| scimark_sparse_mat_mult    | 5.55 ms                                                                | 5.10 ms: 1.09x faster                                                 |
| pprint_safe_repr           | 867 ms                                                                 | 799 ms: 1.09x faster                                                  |
| html5lib                   | 76.5 ms                                                                | 70.5 ms: 1.09x faster                                                 |
| sqlglot_v2_normalize       | 129 ms                                                                 | 119 ms: 1.08x faster                                                  |
| sympy_expand               | 588 ms                                                                 | 542 ms: 1.08x faster                                                  |
| deepcopy_memo              | 39.9 us                                                                | 36.8 us: 1.08x faster                                                 |
| sqlglot_v2_transpile       | 2.01 ms                                                                | 1.87 ms: 1.08x faster                                                 |
| sqlglot_v2_optimize        | 64.2 ms                                                                | 59.7 ms: 1.07x faster                                                 |
| sqlglot_v2_parse           | 1.66 ms                                                                | 1.54 ms: 1.07x faster                                                 |
| comprehensions             | 22.1 us                                                                | 20.6 us: 1.07x faster                                                 |
| sympy_str                  | 353 ms                                                                 | 330 ms: 1.07x faster                                                  |
| pyflate                    | 520 ms                                                                 | 486 ms: 1.07x faster                                                  |
| subparsers                 | 27.1 ms                                                                | 25.3 ms: 1.07x faster                                                 |
| typing_runtime_protocols   | 208 us                                                                 | 195 us: 1.07x faster                                                  |
| scimark_lu                 | 143 ms                                                                 | 134 ms: 1.07x faster                                                  |
| 2to3                       | 311 ms                                                                 | 291 ms: 1.07x faster                                                  |
| dulwich_log                | 78.1 ms                                                                | 73.3 ms: 1.07x faster                                                 |
| mdp                        | 1.46 sec                                                               | 1.37 sec: 1.07x faster                                                |
| many_optionals             | 1.22 ms                                                                | 1.15 ms: 1.07x faster                                                 |
| pycparser                  | 1.25 sec                                                               | 1.17 sec: 1.07x faster                                                |
| deepcopy_reduce            | 3.26 us                                                                | 3.07 us: 1.06x faster                                                 |
| mako                       | 16.5 ms                                                                | 15.5 ms: 1.06x faster                                                 |
| async_tree_memoization     | 342 ms                                                                 | 322 ms: 1.06x faster                                                  |
| async_tree_io              | 599 ms                                                                 | 564 ms: 1.06x faster                                                  |
| crypto_pyaes               | 91.3 ms                                                                | 86.0 ms: 1.06x faster                                                 |
| async_tree_none            | 285 ms                                                                 | 269 ms: 1.06x faster                                                  |
| xml_etree_process          | 74.4 ms                                                                | 70.2 ms: 1.06x faster                                                 |
| regex_effbot               | 2.87 ms                                                                | 2.71 ms: 1.06x faster                                                 |
| django_template            | 45.0 ms                                                                | 42.5 ms: 1.06x faster                                                 |
| xml_etree_generate         | 102 ms                                                                 | 96.0 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.95 sec                                                               | 4.68 sec: 1.06x faster                                                |
| scimark_fft                | 379 ms                                                                 | 358 ms: 1.06x faster                                                  |
| async_tree_io_tg           | 566 ms                                                                 | 536 ms: 1.06x faster                                                  |
| sqlalchemy_imperative      | 25.4 ms                                                                | 24.1 ms: 1.06x faster                                                 |
| sphinx                     | 1.15 sec                                                               | 1.09 sec: 1.05x faster                                                |
| async_generators           | 386 ms                                                                 | 367 ms: 1.05x faster                                                  |
| pylint                     | 333 ms                                                                 | 317 ms: 1.05x faster                                                  |
| docutils                   | 2.91 sec                                                               | 2.77 sec: 1.05x faster                                                |
| sympy_sum                  | 195 ms                                                                 | 186 ms: 1.05x faster                                                  |
| connected_components       | 511 ms                                                                 | 487 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 244 ms                                                                 | 233 ms: 1.05x faster                                                  |
| sympy_integrate            | 24.3 ms                                                                | 23.2 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 91.9 ms                                                                | 87.9 ms: 1.05x faster                                                 |
| meteor_contest             | 134 ms                                                                 | 129 ms: 1.04x faster                                                  |
| sqlite_synth               | 2.08 us                                                                | 2.00 us: 1.04x faster                                                 |
| async_tree_memoization_tg  | 309 ms                                                                 | 296 ms: 1.04x faster                                                  |
| sqlalchemy_declarative     | 165 ms                                                                 | 159 ms: 1.04x faster                                                  |
| shortest_path              | 553 ms                                                                 | 533 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed    | 548 ms                                                                 | 528 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed_tg | 514 ms                                                                 | 498 ms: 1.03x faster                                                  |
| pathlib                    | 19.9 ms                                                                | 19.5 ms: 1.02x faster                                                 |
| telco                      | 8.57 ms                                                                | 8.41 ms: 1.02x faster                                                 |
| k_core                     | 2.29 sec                                                               | 2.25 sec: 1.02x faster                                                |
| bench_mp_pool              | 97.4 ms                                                                | 95.9 ms: 1.02x faster                                                 |
| coverage                   | 110 ms                                                                 | 108 ms: 1.02x faster                                                  |
| json_dumps                 | 13.2 ms                                                                | 13.0 ms: 1.01x faster                                                 |
| bench_thread_pool          | 3.19 ms                                                                | 3.15 ms: 1.01x faster                                                 |
| regex_v8                   | 21.3 ms                                                                | 21.0 ms: 1.01x faster                                                 |
| json                       | 5.35 ms                                                                | 5.28 ms: 1.01x faster                                                 |
| json_loads                 | 31.1 us                                                                | 30.7 us: 1.01x faster                                                 |
| python_startup             | 16.0 ms                                                                | 15.9 ms: 1.01x faster                                                 |
| create_gc_cycles           | 1.34 ms                                                                | 1.33 ms: 1.01x faster                                                 |
| python_startup_no_site     | 11.2 ms                                                                | 11.2 ms: 1.01x faster                                                 |
| gc_traversal               | 1.78 ms                                                                | 1.77 ms: 1.01x faster                                                 |
| asyncio_websockets         | 515 ms                                                                 | 516 ms: 1.00x slower                                                  |
| regex_dna                  | 178 ms                                                                 | 183 ms: 1.03x slower                                                  |
| pidigits                   | 211 ms                                                                 | 217 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.01x