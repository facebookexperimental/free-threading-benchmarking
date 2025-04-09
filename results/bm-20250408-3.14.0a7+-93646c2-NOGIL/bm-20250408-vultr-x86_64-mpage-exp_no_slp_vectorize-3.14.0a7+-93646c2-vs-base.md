# Results vs. base

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 93646c2
- commit date: 2025-04-08
- overall geometric mean: 1.116x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 311 ms                                                                 | 280 ms: 1.11x faster                                                  |
| docutils       | 2.91 sec                                                               | 2.71 sec: 1.08x faster                                                |
| html5lib       | 76.5 ms                                                                | 64.8 ms: 1.18x faster                                                 |
| sphinx         | 1.15 sec                                                               | 1.06 sec: 1.08x faster                                                |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 26.9 ms                                                                | 22.3 ms: 1.21x faster                                                 |
| async_tree_none            | 285 ms                                                                 | 252 ms: 1.13x faster                                                  |
| async_tree_memoization     | 342 ms                                                                 | 309 ms: 1.11x faster                                                  |
| async_tree_io              | 599 ms                                                                 | 541 ms: 1.11x faster                                                  |
| async_tree_io_tg           | 566 ms                                                                 | 512 ms: 1.11x faster                                                  |
| async_tree_memoization_tg  | 309 ms                                                                 | 280 ms: 1.10x faster                                                  |
| async_tree_none_tg         | 244 ms                                                                 | 222 ms: 1.10x faster                                                  |
| async_generators           | 386 ms                                                                 | 354 ms: 1.09x faster                                                  |
| asyncio_websockets         | 515 ms                                                                 | 516 ms: 1.00x slower                                                  |
| async_tree_cpu_io_mixed_tg | 514 ms                                                                 | 521 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 134 ms                                                                 | 107 ms: 1.25x faster                                                  |
| float          | 77.6 ms                                                                | 67.2 ms: 1.15x faster                                                 |
| pidigits       | 211 ms                                                                 | 223 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 170 ms                                                                 | 142 ms: 1.19x faster                                                  |
| regex_dna      | 178 ms                                                                 | 176 ms: 1.01x faster                                                  |
| regex_effbot   | 2.87 ms                                                                | 2.86 ms: 1.00x faster                                                 |
| regex_v8       | 21.3 ms                                                                | 21.5 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.53 sec                                                               | 2.08 sec: 1.22x faster                                                |
| unpickle_pure_python | 268 us                                                                 | 226 us: 1.19x faster                                                  |
| pickle_pure_python   | 382 us                                                                 | 328 us: 1.16x faster                                                  |
| xml_etree_process    | 74.4 ms                                                                | 65.6 ms: 1.13x faster                                                 |
| xml_etree_generate   | 102 ms                                                                 | 92.1 ms: 1.10x faster                                                 |
| xml_etree_iterparse  | 91.9 ms                                                                | 84.1 ms: 1.09x faster                                                 |
| json_dumps           | 13.2 ms                                                                | 12.5 ms: 1.05x faster                                                 |
| json_loads           | 31.1 us                                                                | 30.2 us: 1.03x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 126 ms: 1.02x faster                                                  |
| Geometric mean       | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 16.0 ms                                                                | 15.8 ms: 1.01x faster                                                 |
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.9 ms                                                                | 54.3 ms: 1.25x faster                                                 |
| genshi_text     | 31.3 ms                                                                | 25.5 ms: 1.23x faster                                                 |
| django_template | 45.0 ms                                                                | 39.8 ms: 1.13x faster                                                 |
| mako            | 16.5 ms                                                                | 15.3 ms: 1.07x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.17x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| generators                 | 44.6 ms                                                                | 29.5 ms: 1.51x faster                                                 |
| scimark_sor                | 161 ms                                                                 | 119 ms: 1.35x faster                                                  |
| deltablue                  | 4.44 ms                                                                | 3.50 ms: 1.27x faster                                                 |
| genshi_xml                 | 67.9 ms                                                                | 54.3 ms: 1.25x faster                                                 |
| nbody                      | 134 ms                                                                 | 107 ms: 1.25x faster                                                  |
| go                         | 152 ms                                                                 | 124 ms: 1.23x faster                                                  |
| logging_simple             | 8.67 us                                                                | 7.04 us: 1.23x faster                                                 |
| logging_format             | 9.79 us                                                                | 7.96 us: 1.23x faster                                                 |
| genshi_text                | 31.3 ms                                                                | 25.5 ms: 1.23x faster                                                 |
| logging_silent             | 125 ns                                                                 | 102 ns: 1.22x faster                                                  |
| hexiom                     | 8.08 ms                                                                | 6.62 ms: 1.22x faster                                                 |
| tomli_loads                | 2.53 sec                                                               | 2.08 sec: 1.22x faster                                                |
| nqueens                    | 102 ms                                                                 | 84.2 ms: 1.21x faster                                                 |
| coroutines                 | 26.9 ms                                                                | 22.3 ms: 1.21x faster                                                 |
| chaos                      | 72.5 ms                                                                | 60.1 ms: 1.21x faster                                                 |
| richards                   | 60.7 ms                                                                | 50.4 ms: 1.20x faster                                                 |
| richards_super             | 68.9 ms                                                                | 57.7 ms: 1.19x faster                                                 |
| scimark_monte_carlo        | 87.4 ms                                                                | 73.2 ms: 1.19x faster                                                 |
| regex_compile              | 170 ms                                                                 | 142 ms: 1.19x faster                                                  |
| raytrace                   | 339 ms                                                                 | 284 ms: 1.19x faster                                                  |
| spectral_norm              | 121 ms                                                                 | 102 ms: 1.19x faster                                                  |
| unpickle_pure_python       | 268 us                                                                 | 226 us: 1.19x faster                                                  |
| html5lib                   | 76.5 ms                                                                | 64.8 ms: 1.18x faster                                                 |
| comprehensions             | 22.1 us                                                                | 19.0 us: 1.16x faster                                                 |
| pickle_pure_python         | 382 us                                                                 | 328 us: 1.16x faster                                                  |
| fannkuch                   | 515 ms                                                                 | 444 ms: 1.16x faster                                                  |
| float                      | 77.6 ms                                                                | 67.2 ms: 1.15x faster                                                 |
| scimark_sparse_mat_mult    | 5.55 ms                                                                | 4.85 ms: 1.14x faster                                                 |
| sqlglot_v2_normalize       | 129 ms                                                                 | 112 ms: 1.14x faster                                                  |
| sqlglot_v2_transpile       | 2.01 ms                                                                | 1.76 ms: 1.14x faster                                                 |
| pprint_pformat             | 1.80 sec                                                               | 1.58 sec: 1.14x faster                                                |
| pprint_safe_repr           | 867 ms                                                                 | 762 ms: 1.14x faster                                                  |
| pyflate                    | 520 ms                                                                 | 458 ms: 1.14x faster                                                  |
| deepcopy_reduce            | 3.26 us                                                                | 2.88 us: 1.13x faster                                                 |
| xml_etree_process          | 74.4 ms                                                                | 65.6 ms: 1.13x faster                                                 |
| sqlglot_v2_parse           | 1.66 ms                                                                | 1.47 ms: 1.13x faster                                                 |
| django_template            | 45.0 ms                                                                | 39.8 ms: 1.13x faster                                                 |
| deepcopy                   | 326 us                                                                 | 289 us: 1.13x faster                                                  |
| async_tree_none            | 285 ms                                                                 | 252 ms: 1.13x faster                                                  |
| scimark_lu                 | 143 ms                                                                 | 126 ms: 1.13x faster                                                  |
| deepcopy_memo              | 39.9 us                                                                | 35.4 us: 1.13x faster                                                 |
| sympy_expand               | 588 ms                                                                 | 522 ms: 1.13x faster                                                  |
| sqlglot_v2_optimize        | 64.2 ms                                                                | 57.1 ms: 1.12x faster                                                 |
| mdp                        | 1.46 sec                                                               | 1.30 sec: 1.12x faster                                                |
| sympy_str                  | 353 ms                                                                 | 318 ms: 1.11x faster                                                  |
| 2to3                       | 311 ms                                                                 | 280 ms: 1.11x faster                                                  |
| subparsers                 | 27.1 ms                                                                | 24.4 ms: 1.11x faster                                                 |
| async_tree_memoization     | 342 ms                                                                 | 309 ms: 1.11x faster                                                  |
| bpe_tokeniser              | 4.95 sec                                                               | 4.47 sec: 1.11x faster                                                |
| async_tree_io              | 599 ms                                                                 | 541 ms: 1.11x faster                                                  |
| async_tree_io_tg           | 566 ms                                                                 | 512 ms: 1.11x faster                                                  |
| pycparser                  | 1.25 sec                                                               | 1.13 sec: 1.11x faster                                                |
| scimark_fft                | 379 ms                                                                 | 343 ms: 1.11x faster                                                  |
| xml_etree_generate         | 102 ms                                                                 | 92.1 ms: 1.10x faster                                                 |
| async_tree_memoization_tg  | 309 ms                                                                 | 280 ms: 1.10x faster                                                  |
| async_tree_none_tg         | 244 ms                                                                 | 222 ms: 1.10x faster                                                  |
| typing_runtime_protocols   | 208 us                                                                 | 190 us: 1.10x faster                                                  |
| many_optionals             | 1.22 ms                                                                | 1.12 ms: 1.10x faster                                                 |
| xml_etree_iterparse        | 91.9 ms                                                                | 84.1 ms: 1.09x faster                                                 |
| async_generators           | 386 ms                                                                 | 354 ms: 1.09x faster                                                  |
| crypto_pyaes               | 91.3 ms                                                                | 83.5 ms: 1.09x faster                                                 |
| dulwich_log                | 78.1 ms                                                                | 71.5 ms: 1.09x faster                                                 |
| sympy_integrate            | 24.3 ms                                                                | 22.3 ms: 1.09x faster                                                 |
| meteor_contest             | 134 ms                                                                 | 123 ms: 1.09x faster                                                  |
| pylint                     | 333 ms                                                                 | 307 ms: 1.09x faster                                                  |
| sphinx                     | 1.15 sec                                                               | 1.06 sec: 1.08x faster                                                |
| sympy_sum                  | 195 ms                                                                 | 180 ms: 1.08x faster                                                  |
| sqlalchemy_imperative      | 25.4 ms                                                                | 23.6 ms: 1.08x faster                                                 |
| docutils                   | 2.91 sec                                                               | 2.71 sec: 1.08x faster                                                |
| mako                       | 16.5 ms                                                                | 15.3 ms: 1.07x faster                                                 |
| sqlalchemy_declarative     | 165 ms                                                                 | 154 ms: 1.07x faster                                                  |
| connected_components       | 511 ms                                                                 | 485 ms: 1.05x faster                                                  |
| json_dumps                 | 13.2 ms                                                                | 12.5 ms: 1.05x faster                                                 |
| pathlib                    | 19.9 ms                                                                | 19.0 ms: 1.05x faster                                                 |
| shortest_path              | 553 ms                                                                 | 529 ms: 1.04x faster                                                  |
| telco                      | 8.57 ms                                                                | 8.25 ms: 1.04x faster                                                 |
| sqlite_synth               | 2.08 us                                                                | 2.01 us: 1.04x faster                                                 |
| json_loads                 | 31.1 us                                                                | 30.2 us: 1.03x faster                                                 |
| k_core                     | 2.29 sec                                                               | 2.22 sec: 1.03x faster                                                |
| bench_mp_pool              | 97.4 ms                                                                | 95.0 ms: 1.02x faster                                                 |
| json                       | 5.35 ms                                                                | 5.23 ms: 1.02x faster                                                 |
| xml_etree_parse            | 129 ms                                                                 | 126 ms: 1.02x faster                                                  |
| bench_thread_pool          | 3.19 ms                                                                | 3.14 ms: 1.02x faster                                                 |
| coverage                   | 110 ms                                                                 | 109 ms: 1.01x faster                                                  |
| python_startup             | 16.0 ms                                                                | 15.8 ms: 1.01x faster                                                 |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                 |
| regex_dna                  | 178 ms                                                                 | 176 ms: 1.01x faster                                                  |
| regex_effbot               | 2.87 ms                                                                | 2.86 ms: 1.00x faster                                                 |
| asyncio_websockets         | 515 ms                                                                 | 516 ms: 1.00x slower                                                  |
| async_tree_cpu_io_mixed_tg | 514 ms                                                                 | 521 ms: 1.01x slower                                                  |
| regex_v8                   | 21.3 ms                                                                | 21.5 ms: 1.01x slower                                                 |
| pidigits                   | 211 ms                                                                 | 223 ms: 1.06x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.11x faster                                                          |

Benchmark hidden because not significant (3): gc_traversal, create_gc_cycles, async_tree_cpu_io_mixed

- Geometric mean (including insignificant results): 1.116x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.01x