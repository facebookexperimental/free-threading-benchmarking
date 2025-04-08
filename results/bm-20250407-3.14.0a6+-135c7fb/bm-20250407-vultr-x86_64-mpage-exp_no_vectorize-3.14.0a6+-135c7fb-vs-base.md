# Results vs. base

- fork: mpage
- ref: exp_no_vectorize
- machine: linux-x86_64
- commit hash: 135c7fb
- commit date: 2025-04-07
- overall geometric mean: 1.045x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 245 ms: 1.03x faster                                              |
| docutils       | 2.58 sec                                                               | 2.49 sec: 1.04x faster                                            |
| sphinx         | 1.00 sec                                                               | 967 ms: 1.04x faster                                              |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| coroutines                 | 24.8 ms                                                                | 23.4 ms: 1.06x faster                                             |
| async_generators           | 334 ms                                                                 | 322 ms: 1.04x faster                                              |
| async_tree_memoization     | 321 ms                                                                 | 311 ms: 1.03x faster                                              |
| async_tree_none            | 279 ms                                                                 | 271 ms: 1.03x faster                                              |
| async_tree_memoization_tg  | 323 ms                                                                 | 315 ms: 1.02x faster                                              |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 493 ms: 1.02x faster                                              |
| async_tree_io              | 627 ms                                                                 | 613 ms: 1.02x faster                                              |
| async_tree_io_tg           | 625 ms                                                                 | 612 ms: 1.02x faster                                              |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 494 ms: 1.01x faster                                              |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                      |

Benchmark hidden because not significant (2): async_tree_none_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 97.0 ms                                                                | 82.3 ms: 1.18x faster                                             |
| float          | 71.9 ms                                                                | 68.5 ms: 1.05x faster                                             |
| pidigits       | 196 ms                                                                 | 198 ms: 1.01x slower                                              |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 2.82 ms                                                                | 2.64 ms: 1.07x faster                                             |
| regex_compile  | 129 ms                                                                 | 121 ms: 1.07x faster                                              |
| regex_dna      | 178 ms                                                                 | 171 ms: 1.04x faster                                              |
| regex_v8       | 21.7 ms                                                                | 21.3 ms: 1.02x faster                                             |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.84 sec: 1.09x faster                                            |
| unpickle_pure_python | 221 us                                                                 | 207 us: 1.07x faster                                              |
| pickle_pure_python   | 320 us                                                                 | 302 us: 1.06x faster                                              |
| xml_etree_process    | 60.4 ms                                                                | 58.0 ms: 1.04x faster                                             |
| xml_etree_generate   | 85.1 ms                                                                | 82.5 ms: 1.03x faster                                             |
| xml_etree_iterparse  | 93.8 ms                                                                | 91.7 ms: 1.02x faster                                             |
| json_dumps           | 11.3 ms                                                                | 11.2 ms: 1.01x faster                                             |
| json_loads           | 27.2 us                                                                | 27.0 us: 1.01x faster                                             |
| xml_etree_parse      | 130 ms                                                                 | 130 ms: 1.01x faster                                              |
| Geometric mean       | (ref)                                                                  | 1.04x faster                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.1 ms                                                                | 15.1 ms: 1.00x faster                                             |
| python_startup_no_site | 8.65 ms                                                                | 8.66 ms: 1.00x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_text     | 21.6 ms                                                                | 19.9 ms: 1.08x faster                                             |
| genshi_xml      | 50.3 ms                                                                | 47.2 ms: 1.07x faster                                             |
| django_template | 36.3 ms                                                                | 34.4 ms: 1.06x faster                                             |
| mako            | 12.2 ms                                                                | 11.7 ms: 1.04x faster                                             |
| Geometric mean  | (ref)                                                                  | 1.06x faster                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody                      | 97.0 ms                                                                | 82.3 ms: 1.18x faster                                             |
| go                         | 116 ms                                                                 | 105 ms: 1.10x faster                                              |
| richards_super             | 50.9 ms                                                                | 46.1 ms: 1.10x faster                                             |
| richards                   | 44.5 ms                                                                | 40.5 ms: 1.10x faster                                             |
| scimark_lu                 | 119 ms                                                                 | 108 ms: 1.10x faster                                              |
| tomli_loads                | 2.01 sec                                                               | 1.84 sec: 1.09x faster                                            |
| spectral_norm              | 100 ms                                                                 | 91.9 ms: 1.09x faster                                             |
| generators                 | 29.1 ms                                                                | 26.7 ms: 1.09x faster                                             |
| hexiom                     | 6.14 ms                                                                | 5.66 ms: 1.09x faster                                             |
| genshi_text                | 21.6 ms                                                                | 19.9 ms: 1.08x faster                                             |
| logging_silent             | 103 ns                                                                 | 95.5 ns: 1.08x faster                                             |
| chaos                      | 55.8 ms                                                                | 51.7 ms: 1.08x faster                                             |
| fannkuch                   | 399 ms                                                                 | 370 ms: 1.08x faster                                              |
| scimark_sor                | 115 ms                                                                 | 107 ms: 1.08x faster                                              |
| scimark_fft                | 327 ms                                                                 | 305 ms: 1.07x faster                                              |
| sqlglot_v2_parse           | 1.28 ms                                                                | 1.20 ms: 1.07x faster                                             |
| logging_format             | 7.00 us                                                                | 6.54 us: 1.07x faster                                             |
| sqlglot_v2_transpile       | 1.60 ms                                                                | 1.49 ms: 1.07x faster                                             |
| pprint_safe_repr           | 734 ms                                                                 | 686 ms: 1.07x faster                                              |
| unpickle_pure_python       | 221 us                                                                 | 207 us: 1.07x faster                                              |
| regex_effbot               | 2.82 ms                                                                | 2.64 ms: 1.07x faster                                             |
| deltablue                  | 3.36 ms                                                                | 3.14 ms: 1.07x faster                                             |
| pprint_pformat             | 1.50 sec                                                               | 1.40 sec: 1.07x faster                                            |
| regex_compile              | 129 ms                                                                 | 121 ms: 1.07x faster                                              |
| logging_simple             | 6.27 us                                                                | 5.87 us: 1.07x faster                                             |
| nqueens                    | 80.8 ms                                                                | 75.8 ms: 1.07x faster                                             |
| genshi_xml                 | 50.3 ms                                                                | 47.2 ms: 1.07x faster                                             |
| scimark_monte_carlo        | 64.1 ms                                                                | 60.2 ms: 1.06x faster                                             |
| sqlglot_v2_normalize       | 106 ms                                                                 | 99.2 ms: 1.06x faster                                             |
| sqlglot_v2_optimize        | 52.8 ms                                                                | 49.7 ms: 1.06x faster                                             |
| pickle_pure_python         | 320 us                                                                 | 302 us: 1.06x faster                                              |
| comprehensions             | 17.2 us                                                                | 16.2 us: 1.06x faster                                             |
| coroutines                 | 24.8 ms                                                                | 23.4 ms: 1.06x faster                                             |
| pycparser                  | 1.16 sec                                                               | 1.09 sec: 1.06x faster                                            |
| pyflate                    | 424 ms                                                                 | 401 ms: 1.06x faster                                              |
| django_template            | 36.3 ms                                                                | 34.4 ms: 1.06x faster                                             |
| deepcopy                   | 261 us                                                                 | 248 us: 1.05x faster                                              |
| float                      | 71.9 ms                                                                | 68.5 ms: 1.05x faster                                             |
| raytrace                   | 259 ms                                                                 | 247 ms: 1.05x faster                                              |
| deepcopy_memo              | 29.6 us                                                                | 28.2 us: 1.05x faster                                             |
| coverage                   | 81.9 ms                                                                | 78.2 ms: 1.05x faster                                             |
| sqlalchemy_imperative      | 20.5 ms                                                                | 19.6 ms: 1.04x faster                                             |
| scimark_sparse_mat_mult    | 4.54 ms                                                                | 4.36 ms: 1.04x faster                                             |
| xml_etree_process          | 60.4 ms                                                                | 58.0 ms: 1.04x faster                                             |
| mdp                        | 1.17 sec                                                               | 1.13 sec: 1.04x faster                                            |
| mako                       | 12.2 ms                                                                | 11.7 ms: 1.04x faster                                             |
| async_generators           | 334 ms                                                                 | 322 ms: 1.04x faster                                              |
| sympy_str                  | 280 ms                                                                 | 270 ms: 1.04x faster                                              |
| regex_dna                  | 178 ms                                                                 | 171 ms: 1.04x faster                                              |
| telco                      | 7.33 ms                                                                | 7.07 ms: 1.04x faster                                             |
| bpe_tokeniser              | 4.33 sec                                                               | 4.17 sec: 1.04x faster                                            |
| sympy_expand               | 469 ms                                                                 | 453 ms: 1.04x faster                                              |
| sphinx                     | 1.00 sec                                                               | 967 ms: 1.04x faster                                              |
| typing_runtime_protocols   | 163 us                                                                 | 157 us: 1.04x faster                                              |
| sympy_sum                  | 159 ms                                                                 | 153 ms: 1.04x faster                                              |
| docutils                   | 2.58 sec                                                               | 2.49 sec: 1.04x faster                                            |
| crypto_pyaes               | 69.9 ms                                                                | 67.5 ms: 1.03x faster                                             |
| pylint                     | 286 ms                                                                 | 277 ms: 1.03x faster                                              |
| 2to3                       | 253 ms                                                                 | 245 ms: 1.03x faster                                              |
| sqlalchemy_declarative     | 133 ms                                                                 | 128 ms: 1.03x faster                                              |
| pathlib                    | 19.7 ms                                                                | 19.0 ms: 1.03x faster                                             |
| xml_etree_generate         | 85.1 ms                                                                | 82.5 ms: 1.03x faster                                             |
| async_tree_memoization     | 321 ms                                                                 | 311 ms: 1.03x faster                                              |
| sympy_integrate            | 19.6 ms                                                                | 19.0 ms: 1.03x faster                                             |
| async_tree_none            | 279 ms                                                                 | 271 ms: 1.03x faster                                              |
| dulwich_log                | 68.3 ms                                                                | 66.6 ms: 1.03x faster                                             |
| meteor_contest             | 101 ms                                                                 | 98.9 ms: 1.03x faster                                             |
| async_tree_memoization_tg  | 323 ms                                                                 | 315 ms: 1.02x faster                                              |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 493 ms: 1.02x faster                                              |
| many_optionals             | 1.03 ms                                                                | 1.01 ms: 1.02x faster                                             |
| async_tree_io              | 627 ms                                                                 | 613 ms: 1.02x faster                                              |
| shortest_path              | 443 ms                                                                 | 434 ms: 1.02x faster                                              |
| xml_etree_iterparse        | 93.8 ms                                                                | 91.7 ms: 1.02x faster                                             |
| async_tree_io_tg           | 625 ms                                                                 | 612 ms: 1.02x faster                                              |
| subparsers                 | 22.3 ms                                                                | 21.8 ms: 1.02x faster                                             |
| deepcopy_reduce            | 2.70 us                                                                | 2.64 us: 1.02x faster                                             |
| regex_v8                   | 21.7 ms                                                                | 21.3 ms: 1.02x faster                                             |
| bench_thread_pool          | 1.06 ms                                                                | 1.04 ms: 1.02x faster                                             |
| connected_components       | 397 ms                                                                 | 392 ms: 1.01x faster                                              |
| sqlite_synth               | 2.21 us                                                                | 2.18 us: 1.01x faster                                             |
| k_core                     | 2.06 sec                                                               | 2.03 sec: 1.01x faster                                            |
| bench_mp_pool              | 89.2 ms                                                                | 88.3 ms: 1.01x faster                                             |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 494 ms: 1.01x faster                                              |
| json_dumps                 | 11.3 ms                                                                | 11.2 ms: 1.01x faster                                             |
| json_loads                 | 27.2 us                                                                | 27.0 us: 1.01x faster                                             |
| xml_etree_parse            | 130 ms                                                                 | 130 ms: 1.01x faster                                              |
| python_startup             | 15.1 ms                                                                | 15.1 ms: 1.00x faster                                             |
| python_startup_no_site     | 8.65 ms                                                                | 8.66 ms: 1.00x slower                                             |
| pidigits                   | 196 ms                                                                 | 198 ms: 1.01x slower                                              |
| gc_traversal               | 4.34 ms                                                                | 4.58 ms: 1.06x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                      |

Benchmark hidden because not significant (4): json, async_tree_none_tg, create_gc_cycles, asyncio_websockets

- Geometric mean (including insignificant results): 1.045x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.01x