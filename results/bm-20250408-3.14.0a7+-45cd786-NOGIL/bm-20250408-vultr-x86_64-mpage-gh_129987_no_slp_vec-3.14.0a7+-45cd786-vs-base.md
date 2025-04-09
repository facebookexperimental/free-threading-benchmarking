# Results vs. base

- fork: mpage
- ref: gh_129987_no_slp_vec
- machine: linux-x86_64
- commit hash: 45cd786
- commit date: 2025-04-08
- overall geometric mean: 1.084x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 311 ms                                                                 | 287 ms: 1.08x faster                                                  |
| docutils       | 2.91 sec                                                               | 2.75 sec: 1.06x faster                                                |
| html5lib       | 76.5 ms                                                                | 69.2 ms: 1.10x faster                                                 |
| sphinx         | 1.15 sec                                                               | 1.09 sec: 1.06x faster                                                |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 26.9 ms                                                                | 23.2 ms: 1.16x faster                                                 |
| async_tree_cpu_io_mixed    | 548 ms                                                                 | 504 ms: 1.09x faster                                                  |
| async_tree_io              | 599 ms                                                                 | 556 ms: 1.08x faster                                                  |
| async_tree_none            | 285 ms                                                                 | 265 ms: 1.08x faster                                                  |
| async_tree_cpu_io_mixed_tg | 514 ms                                                                 | 479 ms: 1.07x faster                                                  |
| async_tree_memoization     | 342 ms                                                                 | 321 ms: 1.07x faster                                                  |
| async_tree_io_tg           | 566 ms                                                                 | 535 ms: 1.06x faster                                                  |
| async_tree_memoization_tg  | 309 ms                                                                 | 292 ms: 1.06x faster                                                  |
| async_generators           | 386 ms                                                                 | 367 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 244 ms                                                                 | 232 ms: 1.05x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 134 ms                                                                 | 118 ms: 1.13x faster                                                  |
| float          | 77.6 ms                                                                | 70.5 ms: 1.10x faster                                                 |
| pidigits       | 211 ms                                                                 | 200 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 170 ms                                                                 | 151 ms: 1.13x faster                                                  |
| regex_dna      | 178 ms                                                                 | 179 ms: 1.01x slower                                                  |
| regex_v8       | 21.3 ms                                                                | 21.4 ms: 1.01x slower                                                 |
| regex_effbot   | 2.87 ms                                                                | 2.93 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.53 sec                                                               | 2.21 sec: 1.15x faster                                                |
| unpickle_pure_python | 268 us                                                                 | 238 us: 1.13x faster                                                  |
| pickle_pure_python   | 382 us                                                                 | 344 us: 1.11x faster                                                  |
| xml_etree_process    | 74.4 ms                                                                | 68.3 ms: 1.09x faster                                                 |
| xml_etree_generate   | 102 ms                                                                 | 94.8 ms: 1.07x faster                                                 |
| xml_etree_iterparse  | 91.9 ms                                                                | 86.3 ms: 1.06x faster                                                 |
| json_dumps           | 13.2 ms                                                                | 12.6 ms: 1.04x faster                                                 |
| json_loads           | 31.1 us                                                                | 30.5 us: 1.02x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                                  |
| Geometric mean       | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 16.0 ms                                                                | 15.9 ms: 1.01x faster                                                 |
| python_startup_no_site | 11.2 ms                                                                | 11.2 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.9 ms                                                                | 57.9 ms: 1.17x faster                                                 |
| genshi_text     | 31.3 ms                                                                | 27.0 ms: 1.16x faster                                                 |
| django_template | 45.0 ms                                                                | 40.8 ms: 1.10x faster                                                 |
| mako            | 16.5 ms                                                                | 15.4 ms: 1.07x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.13x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| generators                 | 44.6 ms                                                                | 31.7 ms: 1.41x faster                                                 |
| scimark_sor                | 161 ms                                                                 | 128 ms: 1.26x faster                                                  |
| logging_simple             | 8.67 us                                                                | 7.25 us: 1.19x faster                                                 |
| deltablue                  | 4.44 ms                                                                | 3.72 ms: 1.19x faster                                                 |
| logging_format             | 9.79 us                                                                | 8.20 us: 1.19x faster                                                 |
| genshi_xml                 | 67.9 ms                                                                | 57.9 ms: 1.17x faster                                                 |
| genshi_text                | 31.3 ms                                                                | 27.0 ms: 1.16x faster                                                 |
| coroutines                 | 26.9 ms                                                                | 23.2 ms: 1.16x faster                                                 |
| spectral_norm              | 121 ms                                                                 | 105 ms: 1.16x faster                                                  |
| logging_silent             | 125 ns                                                                 | 108 ns: 1.16x faster                                                  |
| nqueens                    | 102 ms                                                                 | 88.2 ms: 1.15x faster                                                 |
| go                         | 152 ms                                                                 | 133 ms: 1.15x faster                                                  |
| tomli_loads                | 2.53 sec                                                               | 2.21 sec: 1.15x faster                                                |
| scimark_monte_carlo        | 87.4 ms                                                                | 76.5 ms: 1.14x faster                                                 |
| hexiom                     | 8.08 ms                                                                | 7.07 ms: 1.14x faster                                                 |
| nbody                      | 134 ms                                                                 | 118 ms: 1.13x faster                                                  |
| chaos                      | 72.5 ms                                                                | 63.9 ms: 1.13x faster                                                 |
| richards                   | 60.7 ms                                                                | 53.8 ms: 1.13x faster                                                 |
| richards_super             | 68.9 ms                                                                | 61.0 ms: 1.13x faster                                                 |
| unpickle_pure_python       | 268 us                                                                 | 238 us: 1.13x faster                                                  |
| regex_compile              | 170 ms                                                                 | 151 ms: 1.13x faster                                                  |
| raytrace                   | 339 ms                                                                 | 303 ms: 1.12x faster                                                  |
| fannkuch                   | 515 ms                                                                 | 462 ms: 1.12x faster                                                  |
| pickle_pure_python         | 382 us                                                                 | 344 us: 1.11x faster                                                  |
| html5lib                   | 76.5 ms                                                                | 69.2 ms: 1.10x faster                                                 |
| django_template            | 45.0 ms                                                                | 40.8 ms: 1.10x faster                                                 |
| sqlglot_v2_normalize       | 129 ms                                                                 | 117 ms: 1.10x faster                                                  |
| deepcopy                   | 326 us                                                                 | 297 us: 1.10x faster                                                  |
| float                      | 77.6 ms                                                                | 70.5 ms: 1.10x faster                                                 |
| pyflate                    | 520 ms                                                                 | 474 ms: 1.10x faster                                                  |
| pprint_safe_repr           | 867 ms                                                                 | 790 ms: 1.10x faster                                                  |
| subparsers                 | 27.1 ms                                                                | 24.7 ms: 1.10x faster                                                 |
| deepcopy_reduce            | 3.26 us                                                                | 2.98 us: 1.10x faster                                                 |
| pprint_pformat             | 1.80 sec                                                               | 1.65 sec: 1.10x faster                                                |
| sqlglot_v2_transpile       | 2.01 ms                                                                | 1.84 ms: 1.09x faster                                                 |
| comprehensions             | 22.1 us                                                                | 20.2 us: 1.09x faster                                                 |
| sqlglot_v2_optimize        | 64.2 ms                                                                | 58.9 ms: 1.09x faster                                                 |
| sqlglot_v2_parse           | 1.66 ms                                                                | 1.52 ms: 1.09x faster                                                 |
| xml_etree_process          | 74.4 ms                                                                | 68.3 ms: 1.09x faster                                                 |
| scimark_sparse_mat_mult    | 5.55 ms                                                                | 5.09 ms: 1.09x faster                                                 |
| deepcopy_memo              | 39.9 us                                                                | 36.6 us: 1.09x faster                                                 |
| async_tree_cpu_io_mixed    | 548 ms                                                                 | 504 ms: 1.09x faster                                                  |
| sympy_expand               | 588 ms                                                                 | 542 ms: 1.08x faster                                                  |
| 2to3                       | 311 ms                                                                 | 287 ms: 1.08x faster                                                  |
| scimark_fft                | 379 ms                                                                 | 351 ms: 1.08x faster                                                  |
| pycparser                  | 1.25 sec                                                               | 1.16 sec: 1.08x faster                                                |
| mdp                        | 1.46 sec                                                               | 1.35 sec: 1.08x faster                                                |
| sympy_str                  | 353 ms                                                                 | 327 ms: 1.08x faster                                                  |
| async_tree_io              | 599 ms                                                                 | 556 ms: 1.08x faster                                                  |
| many_optionals             | 1.22 ms                                                                | 1.14 ms: 1.08x faster                                                 |
| async_tree_none            | 285 ms                                                                 | 265 ms: 1.08x faster                                                  |
| async_tree_cpu_io_mixed_tg | 514 ms                                                                 | 479 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 4.95 sec                                                               | 4.61 sec: 1.07x faster                                                |
| typing_runtime_protocols   | 208 us                                                                 | 194 us: 1.07x faster                                                  |
| crypto_pyaes               | 91.3 ms                                                                | 85.2 ms: 1.07x faster                                                 |
| xml_etree_generate         | 102 ms                                                                 | 94.8 ms: 1.07x faster                                                 |
| dulwich_log                | 78.1 ms                                                                | 73.1 ms: 1.07x faster                                                 |
| mako                       | 16.5 ms                                                                | 15.4 ms: 1.07x faster                                                 |
| scimark_lu                 | 143 ms                                                                 | 134 ms: 1.07x faster                                                  |
| async_tree_memoization     | 342 ms                                                                 | 321 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 91.9 ms                                                                | 86.3 ms: 1.06x faster                                                 |
| sqlalchemy_imperative      | 25.4 ms                                                                | 23.9 ms: 1.06x faster                                                 |
| meteor_contest             | 134 ms                                                                 | 126 ms: 1.06x faster                                                  |
| sphinx                     | 1.15 sec                                                               | 1.09 sec: 1.06x faster                                                |
| sympy_integrate            | 24.3 ms                                                                | 22.9 ms: 1.06x faster                                                 |
| pylint                     | 333 ms                                                                 | 314 ms: 1.06x faster                                                  |
| async_tree_io_tg           | 566 ms                                                                 | 535 ms: 1.06x faster                                                  |
| docutils                   | 2.91 sec                                                               | 2.75 sec: 1.06x faster                                                |
| async_tree_memoization_tg  | 309 ms                                                                 | 292 ms: 1.06x faster                                                  |
| pidigits                   | 211 ms                                                                 | 200 ms: 1.05x faster                                                  |
| sympy_sum                  | 195 ms                                                                 | 185 ms: 1.05x faster                                                  |
| async_generators           | 386 ms                                                                 | 367 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 244 ms                                                                 | 232 ms: 1.05x faster                                                  |
| sqlalchemy_declarative     | 165 ms                                                                 | 157 ms: 1.05x faster                                                  |
| connected_components       | 511 ms                                                                 | 488 ms: 1.05x faster                                                  |
| json_dumps                 | 13.2 ms                                                                | 12.6 ms: 1.04x faster                                                 |
| shortest_path              | 553 ms                                                                 | 533 ms: 1.04x faster                                                  |
| sqlite_synth               | 2.08 us                                                                | 2.01 us: 1.04x faster                                                 |
| pathlib                    | 19.9 ms                                                                | 19.4 ms: 1.03x faster                                                 |
| json                       | 5.35 ms                                                                | 5.22 ms: 1.03x faster                                                 |
| coverage                   | 110 ms                                                                 | 107 ms: 1.02x faster                                                  |
| json_loads                 | 31.1 us                                                                | 30.5 us: 1.02x faster                                                 |
| telco                      | 8.57 ms                                                                | 8.41 ms: 1.02x faster                                                 |
| k_core                     | 2.29 sec                                                               | 2.25 sec: 1.02x faster                                                |
| bench_mp_pool              | 97.4 ms                                                                | 96.0 ms: 1.01x faster                                                 |
| bench_thread_pool          | 3.19 ms                                                                | 3.15 ms: 1.01x faster                                                 |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.34 ms                                                                | 1.33 ms: 1.01x faster                                                 |
| python_startup             | 16.0 ms                                                                | 15.9 ms: 1.01x faster                                                 |
| python_startup_no_site     | 11.2 ms                                                                | 11.2 ms: 1.01x faster                                                 |
| gc_traversal               | 1.78 ms                                                                | 1.77 ms: 1.00x faster                                                 |
| regex_dna                  | 178 ms                                                                 | 179 ms: 1.01x slower                                                  |
| regex_v8                   | 21.3 ms                                                                | 21.4 ms: 1.01x slower                                                 |
| regex_effbot               | 2.87 ms                                                                | 2.93 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

- Geometric mean (including insignificant results): 1.084x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.01x