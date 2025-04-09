# Results vs. base

- fork: mpage
- ref: gh_129987_no_slp_vec
- machine: linux-x86_64
- commit hash: 45cd786
- commit date: 2025-04-08
- overall geometric mean: 1.042x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 245 ms: 1.04x faster                                                  |
| docutils       | 2.60 sec                                                               | 2.52 sec: 1.03x faster                                                |
| sphinx         | 1.00 sec                                                               | 975 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                | 24.6 ms                                                                | 23.2 ms: 1.06x faster                                                 |
| async_generators          | 336 ms                                                                 | 324 ms: 1.04x faster                                                  |
| async_tree_memoization_tg | 325 ms                                                                 | 316 ms: 1.03x faster                                                  |
| async_tree_io_tg          | 626 ms                                                                 | 611 ms: 1.02x faster                                                  |
| async_tree_memoization    | 318 ms                                                                 | 311 ms: 1.02x faster                                                  |
| async_tree_none           | 278 ms                                                                 | 272 ms: 1.02x faster                                                  |
| async_tree_none_tg        | 263 ms                                                                 | 258 ms: 1.02x faster                                                  |
| async_tree_io             | 628 ms                                                                 | 617 ms: 1.02x faster                                                  |
| Geometric mean            | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed, asyncio_websockets, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 94.9 ms                                                                | 83.2 ms: 1.14x faster                                                 |
| float          | 72.3 ms                                                                | 68.5 ms: 1.06x faster                                                 |
| pidigits       | 192 ms                                                                 | 202 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 130 ms                                                                 | 122 ms: 1.07x faster                                                  |
| regex_effbot   | 2.70 ms                                                                | 2.72 ms: 1.01x slower                                                 |
| regex_dna      | 171 ms                                                                 | 173 ms: 1.01x slower                                                  |
| regex_v8       | 21.8 ms                                                                | 22.0 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.81 sec: 1.11x faster                                                |
| unpickle_pure_python | 222 us                                                                 | 208 us: 1.07x faster                                                  |
| xml_etree_process    | 61.4 ms                                                                | 58.0 ms: 1.06x faster                                                 |
| pickle_pure_python   | 318 us                                                                 | 304 us: 1.05x faster                                                  |
| xml_etree_generate   | 85.7 ms                                                                | 82.4 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 93.0 ms                                                                | 91.4 ms: 1.02x faster                                                 |
| json_dumps           | 11.3 ms                                                                | 11.1 ms: 1.02x faster                                                 |
| json_loads           | 28.8 us                                                                | 28.4 us: 1.01x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                                | 15.0 ms: 1.01x faster                                                 |
| python_startup_no_site | 8.68 ms                                                                | 8.61 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.0 ms                                                                | 20.2 ms: 1.09x faster                                                 |
| genshi_xml      | 50.6 ms                                                                | 47.7 ms: 1.06x faster                                                 |
| django_template | 36.7 ms                                                                | 34.8 ms: 1.06x faster                                                 |
| mako            | 12.3 ms                                                                | 11.9 ms: 1.04x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.06x faster                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-gh_129987_no_slp_vec-3.14.0a7+-45cd786 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody                     | 94.9 ms                                                                | 83.2 ms: 1.14x faster                                                 |
| tomli_loads               | 2.01 sec                                                               | 1.81 sec: 1.11x faster                                                |
| richards                  | 44.4 ms                                                                | 40.1 ms: 1.11x faster                                                 |
| richards_super            | 50.6 ms                                                                | 45.9 ms: 1.10x faster                                                 |
| hexiom                    | 6.12 ms                                                                | 5.61 ms: 1.09x faster                                                 |
| go                        | 115 ms                                                                 | 106 ms: 1.09x faster                                                  |
| genshi_text               | 22.0 ms                                                                | 20.2 ms: 1.09x faster                                                 |
| deltablue                 | 3.42 ms                                                                | 3.18 ms: 1.08x faster                                                 |
| spectral_norm             | 99.1 ms                                                                | 92.1 ms: 1.08x faster                                                 |
| logging_silent            | 103 ns                                                                 | 95.4 ns: 1.07x faster                                                 |
| generators                | 29.1 ms                                                                | 27.2 ms: 1.07x faster                                                 |
| unpickle_pure_python      | 222 us                                                                 | 208 us: 1.07x faster                                                  |
| logging_format            | 6.98 us                                                                | 6.54 us: 1.07x faster                                                 |
| regex_compile             | 130 ms                                                                 | 122 ms: 1.07x faster                                                  |
| pprint_pformat            | 1.51 sec                                                               | 1.42 sec: 1.07x faster                                                |
| pyflate                   | 421 ms                                                                 | 395 ms: 1.06x faster                                                  |
| chaos                     | 56.3 ms                                                                | 52.9 ms: 1.06x faster                                                 |
| pprint_safe_repr          | 739 ms                                                                 | 695 ms: 1.06x faster                                                  |
| sqlglot_v2_normalize      | 106 ms                                                                 | 99.8 ms: 1.06x faster                                                 |
| genshi_xml                | 50.6 ms                                                                | 47.7 ms: 1.06x faster                                                 |
| sqlglot_v2_parse          | 1.29 ms                                                                | 1.21 ms: 1.06x faster                                                 |
| logging_simple            | 6.22 us                                                                | 5.86 us: 1.06x faster                                                 |
| comprehensions            | 17.3 us                                                                | 16.3 us: 1.06x faster                                                 |
| coroutines                | 24.6 ms                                                                | 23.2 ms: 1.06x faster                                                 |
| nqueens                   | 80.2 ms                                                                | 75.6 ms: 1.06x faster                                                 |
| crypto_pyaes              | 70.5 ms                                                                | 66.5 ms: 1.06x faster                                                 |
| sqlglot_v2_transpile      | 1.60 ms                                                                | 1.51 ms: 1.06x faster                                                 |
| xml_etree_process         | 61.4 ms                                                                | 58.0 ms: 1.06x faster                                                 |
| django_template           | 36.7 ms                                                                | 34.8 ms: 1.06x faster                                                 |
| float                     | 72.3 ms                                                                | 68.5 ms: 1.06x faster                                                 |
| scimark_sor               | 115 ms                                                                 | 109 ms: 1.06x faster                                                  |
| pycparser                 | 1.15 sec                                                               | 1.09 sec: 1.05x faster                                                |
| scimark_monte_carlo       | 63.3 ms                                                                | 60.1 ms: 1.05x faster                                                 |
| sqlglot_v2_optimize       | 52.7 ms                                                                | 50.1 ms: 1.05x faster                                                 |
| mdp                       | 1.18 sec                                                               | 1.13 sec: 1.05x faster                                                |
| fannkuch                  | 389 ms                                                                 | 371 ms: 1.05x faster                                                  |
| raytrace                  | 258 ms                                                                 | 246 ms: 1.05x faster                                                  |
| sqlalchemy_imperative     | 20.6 ms                                                                | 19.6 ms: 1.05x faster                                                 |
| deepcopy_memo             | 30.1 us                                                                | 28.8 us: 1.05x faster                                                 |
| pickle_pure_python        | 318 us                                                                 | 304 us: 1.05x faster                                                  |
| scimark_fft               | 324 ms                                                                 | 310 ms: 1.05x faster                                                  |
| deepcopy_reduce           | 2.75 us                                                                | 2.63 us: 1.05x faster                                                 |
| sympy_str                 | 282 ms                                                                 | 270 ms: 1.04x faster                                                  |
| sympy_integrate           | 19.7 ms                                                                | 18.9 ms: 1.04x faster                                                 |
| typing_runtime_protocols  | 160 us                                                                 | 153 us: 1.04x faster                                                  |
| xml_etree_generate        | 85.7 ms                                                                | 82.4 ms: 1.04x faster                                                 |
| bpe_tokeniser             | 4.35 sec                                                               | 4.18 sec: 1.04x faster                                                |
| 2to3                      | 255 ms                                                                 | 245 ms: 1.04x faster                                                  |
| deepcopy                  | 263 us                                                                 | 253 us: 1.04x faster                                                  |
| sqlalchemy_declarative    | 133 ms                                                                 | 128 ms: 1.04x faster                                                  |
| meteor_contest            | 101 ms                                                                 | 97.3 ms: 1.04x faster                                                 |
| mako                      | 12.3 ms                                                                | 11.9 ms: 1.04x faster                                                 |
| pylint                    | 287 ms                                                                 | 276 ms: 1.04x faster                                                  |
| sympy_expand              | 473 ms                                                                 | 457 ms: 1.04x faster                                                  |
| async_generators          | 336 ms                                                                 | 324 ms: 1.04x faster                                                  |
| many_optionals            | 1.04 ms                                                                | 1.01 ms: 1.04x faster                                                 |
| scimark_lu                | 118 ms                                                                 | 114 ms: 1.04x faster                                                  |
| scimark_sparse_mat_mult   | 4.59 ms                                                                | 4.44 ms: 1.03x faster                                                 |
| dulwich_log               | 69.1 ms                                                                | 67.0 ms: 1.03x faster                                                 |
| sphinx                    | 1.00 sec                                                               | 975 ms: 1.03x faster                                                  |
| sympy_sum                 | 160 ms                                                                 | 155 ms: 1.03x faster                                                  |
| docutils                  | 2.60 sec                                                               | 2.52 sec: 1.03x faster                                                |
| async_tree_memoization_tg | 325 ms                                                                 | 316 ms: 1.03x faster                                                  |
| json                      | 5.19 ms                                                                | 5.06 ms: 1.03x faster                                                 |
| telco                     | 7.31 ms                                                                | 7.14 ms: 1.02x faster                                                 |
| subparsers                | 22.3 ms                                                                | 21.8 ms: 1.02x faster                                                 |
| async_tree_io_tg          | 626 ms                                                                 | 611 ms: 1.02x faster                                                  |
| async_tree_memoization    | 318 ms                                                                 | 311 ms: 1.02x faster                                                  |
| shortest_path             | 442 ms                                                                 | 432 ms: 1.02x faster                                                  |
| async_tree_none           | 278 ms                                                                 | 272 ms: 1.02x faster                                                  |
| async_tree_none_tg        | 263 ms                                                                 | 258 ms: 1.02x faster                                                  |
| connected_components      | 400 ms                                                                 | 392 ms: 1.02x faster                                                  |
| sqlite_synth              | 2.23 us                                                                | 2.18 us: 1.02x faster                                                 |
| k_core                    | 2.06 sec                                                               | 2.02 sec: 1.02x faster                                                |
| async_tree_io             | 628 ms                                                                 | 617 ms: 1.02x faster                                                  |
| bench_thread_pool         | 1.07 ms                                                                | 1.05 ms: 1.02x faster                                                 |
| xml_etree_iterparse       | 93.0 ms                                                                | 91.4 ms: 1.02x faster                                                 |
| json_dumps                | 11.3 ms                                                                | 11.1 ms: 1.02x faster                                                 |
| coverage                  | 79.9 ms                                                                | 78.7 ms: 1.02x faster                                                 |
| json_loads                | 28.8 us                                                                | 28.4 us: 1.01x faster                                                 |
| bench_mp_pool             | 89.1 ms                                                                | 88.0 ms: 1.01x faster                                                 |
| create_gc_cycles          | 1.86 ms                                                                | 1.84 ms: 1.01x faster                                                 |
| pathlib                   | 19.3 ms                                                                | 19.1 ms: 1.01x faster                                                 |
| python_startup            | 15.2 ms                                                                | 15.0 ms: 1.01x faster                                                 |
| python_startup_no_site    | 8.68 ms                                                                | 8.61 ms: 1.01x faster                                                 |
| gc_traversal              | 4.34 ms                                                                | 4.31 ms: 1.01x faster                                                 |
| regex_effbot              | 2.70 ms                                                                | 2.72 ms: 1.01x slower                                                 |
| regex_dna                 | 171 ms                                                                 | 173 ms: 1.01x slower                                                  |
| regex_v8                  | 21.8 ms                                                                | 22.0 ms: 1.01x slower                                                 |
| pidigits                  | 192 ms                                                                 | 202 ms: 1.05x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, asyncio_websockets, async_tree_cpu_io_mixed_tg, xml_etree_parse

- Geometric mean (including insignificant results): 1.042x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.01x