# Results vs. base

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 93646c2
- commit date: 2025-04-08
- overall geometric mean: 1.041x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 245 ms: 1.04x faster                                                  |
| docutils       | 2.60 sec                                                               | 2.52 sec: 1.03x faster                                                |
| sphinx         | 1.00 sec                                                               | 973 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 24.6 ms                                                                | 23.3 ms: 1.06x faster                                                 |
| async_generators           | 336 ms                                                                 | 323 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 325 ms                                                                 | 315 ms: 1.03x faster                                                  |
| async_tree_io_tg           | 626 ms                                                                 | 608 ms: 1.03x faster                                                  |
| async_tree_memoization     | 318 ms                                                                 | 309 ms: 1.03x faster                                                  |
| async_tree_none            | 278 ms                                                                 | 271 ms: 1.03x faster                                                  |
| async_tree_none_tg         | 263 ms                                                                 | 256 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed    | 506 ms                                                                 | 494 ms: 1.03x faster                                                  |
| async_tree_io              | 628 ms                                                                 | 613 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed_tg | 503 ms                                                                 | 491 ms: 1.02x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 94.9 ms                                                                | 82.0 ms: 1.16x faster                                                 |
| float          | 72.3 ms                                                                | 68.3 ms: 1.06x faster                                                 |
| pidigits       | 192 ms                                                                 | 199 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 130 ms                                                                 | 123 ms: 1.06x faster                                                  |
| regex_v8       | 21.8 ms                                                                | 21.4 ms: 1.02x faster                                                 |
| regex_dna      | 171 ms                                                                 | 174 ms: 1.02x slower                                                  |
| regex_effbot   | 2.70 ms                                                                | 2.80 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.86 sec: 1.08x faster                                                |
| unpickle_pure_python | 222 us                                                                 | 209 us: 1.06x faster                                                  |
| pickle_pure_python   | 318 us                                                                 | 301 us: 1.06x faster                                                  |
| xml_etree_process    | 61.4 ms                                                                | 58.7 ms: 1.05x faster                                                 |
| xml_etree_generate   | 85.7 ms                                                                | 83.3 ms: 1.03x faster                                                 |
| json_loads           | 28.8 us                                                                | 28.4 us: 1.02x faster                                                 |
| json_dumps           | 11.3 ms                                                                | 11.2 ms: 1.01x faster                                                 |
| xml_etree_iterparse  | 93.0 ms                                                                | 91.9 ms: 1.01x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                                  |
| Geometric mean       | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                                | 15.0 ms: 1.01x faster                                                 |
| python_startup_no_site | 8.68 ms                                                                | 8.62 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.0 ms                                                                | 20.6 ms: 1.07x faster                                                 |
| genshi_xml      | 50.6 ms                                                                | 47.7 ms: 1.06x faster                                                 |
| mako            | 12.3 ms                                                                | 11.8 ms: 1.05x faster                                                 |
| django_template | 36.7 ms                                                                | 35.9 ms: 1.02x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.05x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody                      | 94.9 ms                                                                | 82.0 ms: 1.16x faster                                                 |
| logging_silent             | 103 ns                                                                 | 92.8 ns: 1.10x faster                                                 |
| richards                   | 44.4 ms                                                                | 40.3 ms: 1.10x faster                                                 |
| richards_super             | 50.6 ms                                                                | 46.2 ms: 1.10x faster                                                 |
| go                         | 115 ms                                                                 | 105 ms: 1.10x faster                                                  |
| hexiom                     | 6.12 ms                                                                | 5.60 ms: 1.09x faster                                                 |
| deltablue                  | 3.42 ms                                                                | 3.16 ms: 1.08x faster                                                 |
| tomli_loads                | 2.01 sec                                                               | 1.86 sec: 1.08x faster                                                |
| spectral_norm              | 99.1 ms                                                                | 91.9 ms: 1.08x faster                                                 |
| generators                 | 29.1 ms                                                                | 27.1 ms: 1.07x faster                                                 |
| chaos                      | 56.3 ms                                                                | 52.5 ms: 1.07x faster                                                 |
| genshi_text                | 22.0 ms                                                                | 20.6 ms: 1.07x faster                                                 |
| scimark_sor                | 115 ms                                                                 | 108 ms: 1.07x faster                                                  |
| logging_format             | 6.98 us                                                                | 6.54 us: 1.07x faster                                                 |
| unpickle_pure_python       | 222 us                                                                 | 209 us: 1.06x faster                                                  |
| regex_compile              | 130 ms                                                                 | 123 ms: 1.06x faster                                                  |
| nqueens                    | 80.2 ms                                                                | 75.5 ms: 1.06x faster                                                 |
| genshi_xml                 | 50.6 ms                                                                | 47.7 ms: 1.06x faster                                                 |
| sqlglot_v2_parse           | 1.29 ms                                                                | 1.21 ms: 1.06x faster                                                 |
| sqlglot_v2_normalize       | 106 ms                                                                 | 99.9 ms: 1.06x faster                                                 |
| sqlglot_v2_transpile       | 1.60 ms                                                                | 1.51 ms: 1.06x faster                                                 |
| deepcopy_reduce            | 2.75 us                                                                | 2.60 us: 1.06x faster                                                 |
| pycparser                  | 1.15 sec                                                               | 1.09 sec: 1.06x faster                                                |
| deepcopy                   | 263 us                                                                 | 248 us: 1.06x faster                                                  |
| raytrace                   | 258 ms                                                                 | 243 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.51 sec                                                               | 1.43 sec: 1.06x faster                                                |
| float                      | 72.3 ms                                                                | 68.3 ms: 1.06x faster                                                 |
| logging_simple             | 6.22 us                                                                | 5.88 us: 1.06x faster                                                 |
| pickle_pure_python         | 318 us                                                                 | 301 us: 1.06x faster                                                  |
| coroutines                 | 24.6 ms                                                                | 23.3 ms: 1.06x faster                                                 |
| crypto_pyaes               | 70.5 ms                                                                | 66.7 ms: 1.06x faster                                                 |
| comprehensions             | 17.3 us                                                                | 16.3 us: 1.06x faster                                                 |
| scimark_monte_carlo        | 63.3 ms                                                                | 59.9 ms: 1.06x faster                                                 |
| scimark_lu                 | 118 ms                                                                 | 112 ms: 1.05x faster                                                  |
| pyflate                    | 421 ms                                                                 | 400 ms: 1.05x faster                                                  |
| mdp                        | 1.18 sec                                                               | 1.13 sec: 1.05x faster                                                |
| pprint_safe_repr           | 739 ms                                                                 | 705 ms: 1.05x faster                                                  |
| sqlglot_v2_optimize        | 52.7 ms                                                                | 50.3 ms: 1.05x faster                                                 |
| mako                       | 12.3 ms                                                                | 11.8 ms: 1.05x faster                                                 |
| xml_etree_process          | 61.4 ms                                                                | 58.7 ms: 1.05x faster                                                 |
| fannkuch                   | 389 ms                                                                 | 373 ms: 1.04x faster                                                  |
| many_optionals             | 1.04 ms                                                                | 1.00 ms: 1.04x faster                                                 |
| 2to3                       | 255 ms                                                                 | 245 ms: 1.04x faster                                                  |
| sympy_integrate            | 19.7 ms                                                                | 18.9 ms: 1.04x faster                                                 |
| deepcopy_memo              | 30.1 us                                                                | 29.0 us: 1.04x faster                                                 |
| sqlalchemy_declarative     | 133 ms                                                                 | 128 ms: 1.04x faster                                                  |
| sympy_str                  | 282 ms                                                                 | 271 ms: 1.04x faster                                                  |
| async_generators           | 336 ms                                                                 | 323 ms: 1.04x faster                                                  |
| sqlalchemy_imperative      | 20.6 ms                                                                | 19.8 ms: 1.04x faster                                                 |
| typing_runtime_protocols   | 160 us                                                                 | 154 us: 1.04x faster                                                  |
| subparsers                 | 22.3 ms                                                                | 21.6 ms: 1.04x faster                                                 |
| dulwich_log                | 69.1 ms                                                                | 66.8 ms: 1.03x faster                                                 |
| async_tree_memoization_tg  | 325 ms                                                                 | 315 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 4.35 sec                                                               | 4.21 sec: 1.03x faster                                                |
| sphinx                     | 1.00 sec                                                               | 973 ms: 1.03x faster                                                  |
| docutils                   | 2.60 sec                                                               | 2.52 sec: 1.03x faster                                                |
| scimark_fft                | 324 ms                                                                 | 314 ms: 1.03x faster                                                  |
| pylint                     | 287 ms                                                                 | 278 ms: 1.03x faster                                                  |
| sympy_sum                  | 160 ms                                                                 | 155 ms: 1.03x faster                                                  |
| sqlite_synth               | 2.23 us                                                                | 2.16 us: 1.03x faster                                                 |
| async_tree_io_tg           | 626 ms                                                                 | 608 ms: 1.03x faster                                                  |
| xml_etree_generate         | 85.7 ms                                                                | 83.3 ms: 1.03x faster                                                 |
| sympy_expand               | 473 ms                                                                 | 460 ms: 1.03x faster                                                  |
| async_tree_memoization     | 318 ms                                                                 | 309 ms: 1.03x faster                                                  |
| connected_components       | 400 ms                                                                 | 389 ms: 1.03x faster                                                  |
| meteor_contest             | 101 ms                                                                 | 98.3 ms: 1.03x faster                                                 |
| async_tree_none            | 278 ms                                                                 | 271 ms: 1.03x faster                                                  |
| async_tree_none_tg         | 263 ms                                                                 | 256 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed    | 506 ms                                                                 | 494 ms: 1.03x faster                                                  |
| async_tree_io              | 628 ms                                                                 | 613 ms: 1.03x faster                                                  |
| telco                      | 7.31 ms                                                                | 7.13 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed_tg | 503 ms                                                                 | 491 ms: 1.02x faster                                                  |
| django_template            | 36.7 ms                                                                | 35.9 ms: 1.02x faster                                                 |
| gc_traversal               | 4.34 ms                                                                | 4.24 ms: 1.02x faster                                                 |
| shortest_path              | 442 ms                                                                 | 433 ms: 1.02x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 19.0 ms: 1.02x faster                                                 |
| json                       | 5.19 ms                                                                | 5.10 ms: 1.02x faster                                                 |
| bench_thread_pool          | 1.07 ms                                                                | 1.05 ms: 1.02x faster                                                 |
| regex_v8                   | 21.8 ms                                                                | 21.4 ms: 1.02x faster                                                 |
| json_loads                 | 28.8 us                                                                | 28.4 us: 1.02x faster                                                 |
| json_dumps                 | 11.3 ms                                                                | 11.2 ms: 1.01x faster                                                 |
| scimark_sparse_mat_mult    | 4.59 ms                                                                | 4.53 ms: 1.01x faster                                                 |
| k_core                     | 2.06 sec                                                               | 2.03 sec: 1.01x faster                                                |
| xml_etree_iterparse        | 93.0 ms                                                                | 91.9 ms: 1.01x faster                                                 |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                                  |
| bench_mp_pool              | 89.1 ms                                                                | 88.4 ms: 1.01x faster                                                 |
| python_startup             | 15.2 ms                                                                | 15.0 ms: 1.01x faster                                                 |
| python_startup_no_site     | 8.68 ms                                                                | 8.62 ms: 1.01x faster                                                 |
| regex_dna                  | 171 ms                                                                 | 174 ms: 1.02x slower                                                  |
| pidigits                   | 192 ms                                                                 | 199 ms: 1.03x slower                                                  |
| regex_effbot               | 2.70 ms                                                                | 2.80 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (3): asyncio_websockets, create_gc_cycles, coverage

- Geometric mean (including insignificant results): 1.041x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.01x