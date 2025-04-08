# Results vs. base

- fork: mpage
- ref: exp_no_vectorize
- machine: linux-x86_64
- commit hash: 135c7fb
- commit date: 2025-04-07
- overall geometric mean: 1.062x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 310 ms                                                                 | 291 ms: 1.06x faster                                              |
| docutils       | 2.90 sec                                                               | 2.79 sec: 1.04x faster                                            |
| html5lib       | 75.4 ms                                                                | 68.2 ms: 1.11x faster                                             |
| sphinx         | 1.15 sec                                                               | 1.10 sec: 1.05x faster                                            |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| coroutines                 | 26.7 ms                                                                | 23.2 ms: 1.15x faster                                             |
| async_generators           | 387 ms                                                                 | 367 ms: 1.05x faster                                              |
| async_tree_io_tg           | 563 ms                                                                 | 534 ms: 1.05x faster                                              |
| async_tree_memoization_tg  | 310 ms                                                                 | 295 ms: 1.05x faster                                              |
| async_tree_none_tg         | 246 ms                                                                 | 234 ms: 1.05x faster                                              |
| async_tree_memoization     | 341 ms                                                                 | 325 ms: 1.05x faster                                              |
| async_tree_none            | 280 ms                                                                 | 268 ms: 1.05x faster                                              |
| async_tree_io              | 592 ms                                                                 | 567 ms: 1.05x faster                                              |
| async_tree_cpu_io_mixed    | 525 ms                                                                 | 514 ms: 1.02x faster                                              |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                 | 486 ms: 1.02x faster                                              |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                      |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 136 ms                                                                 | 120 ms: 1.13x faster                                              |
| float          | 76.6 ms                                                                | 73.1 ms: 1.05x faster                                             |
| pidigits       | 192 ms                                                                 | 198 ms: 1.03x slower                                              |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 168 ms                                                                 | 152 ms: 1.10x faster                                              |
| regex_effbot   | 2.85 ms                                                                | 2.69 ms: 1.06x faster                                             |
| regex_v8       | 21.3 ms                                                                | 20.7 ms: 1.03x faster                                             |
| regex_dna      | 177 ms                                                                 | 175 ms: 1.01x faster                                              |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| tomli_loads          | 2.53 sec                                                               | 2.28 sec: 1.11x faster                                            |
| unpickle_pure_python | 269 us                                                                 | 245 us: 1.10x faster                                              |
| pickle_pure_python   | 377 us                                                                 | 348 us: 1.08x faster                                              |
| xml_etree_generate   | 102 ms                                                                 | 96.8 ms: 1.05x faster                                             |
| xml_etree_process    | 74.0 ms                                                                | 70.4 ms: 1.05x faster                                             |
| xml_etree_iterparse  | 92.2 ms                                                                | 87.8 ms: 1.05x faster                                             |
| json_dumps           | 13.2 ms                                                                | 12.7 ms: 1.04x faster                                             |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                              |
| json_loads           | 29.7 us                                                                | 29.5 us: 1.01x faster                                             |
| Geometric mean       | (ref)                                                                  | 1.05x faster                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.9 ms                                                                | 15.9 ms: 1.00x faster                                             |
| python_startup_no_site | 11.2 ms                                                                | 11.2 ms: 1.00x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 67.3 ms                                                                | 59.3 ms: 1.14x faster                                             |
| genshi_text     | 31.7 ms                                                                | 28.0 ms: 1.13x faster                                             |
| django_template | 44.5 ms                                                                | 42.0 ms: 1.06x faster                                             |
| mako            | 16.5 ms                                                                | 15.7 ms: 1.06x faster                                             |
| Geometric mean  | (ref)                                                                  | 1.10x faster                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| generators                 | 44.8 ms                                                                | 33.3 ms: 1.35x faster                                             |
| deltablue                  | 4.47 ms                                                                | 3.80 ms: 1.17x faster                                             |
| scimark_sor                | 152 ms                                                                 | 132 ms: 1.15x faster                                              |
| logging_simple             | 8.36 us                                                                | 7.26 us: 1.15x faster                                             |
| coroutines                 | 26.7 ms                                                                | 23.2 ms: 1.15x faster                                             |
| logging_format             | 9.41 us                                                                | 8.20 us: 1.15x faster                                             |
| genshi_xml                 | 67.3 ms                                                                | 59.3 ms: 1.14x faster                                             |
| genshi_text                | 31.7 ms                                                                | 28.0 ms: 1.13x faster                                             |
| nbody                      | 136 ms                                                                 | 120 ms: 1.13x faster                                              |
| go                         | 153 ms                                                                 | 136 ms: 1.12x faster                                              |
| nqueens                    | 100 ms                                                                 | 89.3 ms: 1.12x faster                                             |
| logging_silent             | 126 ns                                                                 | 113 ns: 1.12x faster                                              |
| hexiom                     | 8.07 ms                                                                | 7.26 ms: 1.11x faster                                             |
| tomli_loads                | 2.53 sec                                                               | 2.28 sec: 1.11x faster                                            |
| html5lib                   | 75.4 ms                                                                | 68.2 ms: 1.11x faster                                             |
| regex_compile              | 168 ms                                                                 | 152 ms: 1.10x faster                                              |
| chaos                      | 71.8 ms                                                                | 65.4 ms: 1.10x faster                                             |
| unpickle_pure_python       | 269 us                                                                 | 245 us: 1.10x faster                                              |
| richards                   | 60.1 ms                                                                | 55.0 ms: 1.09x faster                                             |
| fannkuch                   | 511 ms                                                                 | 467 ms: 1.09x faster                                              |
| pprint_safe_repr           | 875 ms                                                                 | 803 ms: 1.09x faster                                              |
| deepcopy_reduce            | 3.29 us                                                                | 3.02 us: 1.09x faster                                             |
| raytrace                   | 336 ms                                                                 | 309 ms: 1.09x faster                                              |
| pickle_pure_python         | 377 us                                                                 | 348 us: 1.08x faster                                              |
| spectral_norm              | 118 ms                                                                 | 109 ms: 1.08x faster                                              |
| pprint_pformat             | 1.82 sec                                                               | 1.68 sec: 1.08x faster                                            |
| scimark_lu                 | 145 ms                                                                 | 134 ms: 1.08x faster                                              |
| richards_super             | 68.3 ms                                                                | 63.2 ms: 1.08x faster                                             |
| scimark_monte_carlo        | 83.2 ms                                                                | 77.3 ms: 1.08x faster                                             |
| pyflate                    | 527 ms                                                                 | 490 ms: 1.08x faster                                              |
| comprehensions             | 22.1 us                                                                | 20.6 us: 1.07x faster                                             |
| deepcopy_memo              | 40.3 us                                                                | 37.5 us: 1.07x faster                                             |
| mdp                        | 1.46 sec                                                               | 1.36 sec: 1.07x faster                                            |
| sqlglot_v2_normalize       | 127 ms                                                                 | 119 ms: 1.07x faster                                              |
| sqlglot_v2_transpile       | 2.00 ms                                                                | 1.87 ms: 1.07x faster                                             |
| sympy_expand               | 579 ms                                                                 | 543 ms: 1.07x faster                                              |
| deepcopy                   | 322 us                                                                 | 302 us: 1.07x faster                                              |
| subparsers                 | 26.8 ms                                                                | 25.2 ms: 1.06x faster                                             |
| sympy_str                  | 350 ms                                                                 | 328 ms: 1.06x faster                                              |
| dulwich_log                | 77.4 ms                                                                | 72.7 ms: 1.06x faster                                             |
| 2to3                       | 310 ms                                                                 | 291 ms: 1.06x faster                                              |
| sqlglot_v2_parse           | 1.64 ms                                                                | 1.55 ms: 1.06x faster                                             |
| django_template            | 44.5 ms                                                                | 42.0 ms: 1.06x faster                                             |
| sqlglot_v2_optimize        | 63.9 ms                                                                | 60.2 ms: 1.06x faster                                             |
| regex_effbot               | 2.85 ms                                                                | 2.69 ms: 1.06x faster                                             |
| many_optionals             | 1.21 ms                                                                | 1.15 ms: 1.06x faster                                             |
| mako                       | 16.5 ms                                                                | 15.7 ms: 1.06x faster                                             |
| async_generators           | 387 ms                                                                 | 367 ms: 1.05x faster                                              |
| async_tree_io_tg           | 563 ms                                                                 | 534 ms: 1.05x faster                                              |
| xml_etree_generate         | 102 ms                                                                 | 96.8 ms: 1.05x faster                                             |
| crypto_pyaes               | 90.7 ms                                                                | 86.3 ms: 1.05x faster                                             |
| async_tree_memoization_tg  | 310 ms                                                                 | 295 ms: 1.05x faster                                              |
| async_tree_none_tg         | 246 ms                                                                 | 234 ms: 1.05x faster                                              |
| xml_etree_process          | 74.0 ms                                                                | 70.4 ms: 1.05x faster                                             |
| async_tree_memoization     | 341 ms                                                                 | 325 ms: 1.05x faster                                              |
| xml_etree_iterparse        | 92.2 ms                                                                | 87.8 ms: 1.05x faster                                             |
| scimark_fft                | 378 ms                                                                 | 360 ms: 1.05x faster                                              |
| float                      | 76.6 ms                                                                | 73.1 ms: 1.05x faster                                             |
| pycparser                  | 1.24 sec                                                               | 1.18 sec: 1.05x faster                                            |
| scimark_sparse_mat_mult    | 5.44 ms                                                                | 5.20 ms: 1.05x faster                                             |
| sphinx                     | 1.15 sec                                                               | 1.10 sec: 1.05x faster                                            |
| async_tree_none            | 280 ms                                                                 | 268 ms: 1.05x faster                                              |
| async_tree_io              | 592 ms                                                                 | 567 ms: 1.05x faster                                              |
| bpe_tokeniser              | 4.91 sec                                                               | 4.70 sec: 1.04x faster                                            |
| typing_runtime_protocols   | 208 us                                                                 | 200 us: 1.04x faster                                              |
| pylint                     | 330 ms                                                                 | 317 ms: 1.04x faster                                              |
| docutils                   | 2.90 sec                                                               | 2.79 sec: 1.04x faster                                            |
| sympy_integrate            | 24.1 ms                                                                | 23.2 ms: 1.04x faster                                             |
| connected_components       | 510 ms                                                                 | 491 ms: 1.04x faster                                              |
| json_dumps                 | 13.2 ms                                                                | 12.7 ms: 1.04x faster                                             |
| sympy_sum                  | 192 ms                                                                 | 186 ms: 1.04x faster                                              |
| shortest_path              | 554 ms                                                                 | 536 ms: 1.03x faster                                              |
| sqlalchemy_declarative     | 164 ms                                                                 | 159 ms: 1.03x faster                                              |
| meteor_contest             | 132 ms                                                                 | 128 ms: 1.03x faster                                              |
| sqlalchemy_imperative      | 24.9 ms                                                                | 24.2 ms: 1.03x faster                                             |
| regex_v8                   | 21.3 ms                                                                | 20.7 ms: 1.03x faster                                             |
| async_tree_cpu_io_mixed    | 525 ms                                                                 | 514 ms: 1.02x faster                                              |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                 | 486 ms: 1.02x faster                                              |
| telco                      | 8.47 ms                                                                | 8.35 ms: 1.02x faster                                             |
| pathlib                    | 19.9 ms                                                                | 19.6 ms: 1.01x faster                                             |
| json                       | 5.12 ms                                                                | 5.04 ms: 1.01x faster                                             |
| k_core                     | 2.29 sec                                                               | 2.26 sec: 1.01x faster                                            |
| regex_dna                  | 177 ms                                                                 | 175 ms: 1.01x faster                                              |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                              |
| coverage                   | 109 ms                                                                 | 108 ms: 1.01x faster                                              |
| bench_thread_pool          | 3.18 ms                                                                | 3.16 ms: 1.01x faster                                             |
| json_loads                 | 29.7 us                                                                | 29.5 us: 1.01x faster                                             |
| bench_mp_pool              | 96.9 ms                                                                | 96.2 ms: 1.01x faster                                             |
| python_startup             | 15.9 ms                                                                | 15.9 ms: 1.00x faster                                             |
| python_startup_no_site     | 11.2 ms                                                                | 11.2 ms: 1.00x slower                                             |
| create_gc_cycles           | 1.35 ms                                                                | 1.36 ms: 1.01x slower                                             |
| pidigits                   | 192 ms                                                                 | 198 ms: 1.03x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.06x faster                                                      |

Benchmark hidden because not significant (3): sqlite_synth, asyncio_websockets, gc_traversal

- Geometric mean (including insignificant results): 1.062x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.00x