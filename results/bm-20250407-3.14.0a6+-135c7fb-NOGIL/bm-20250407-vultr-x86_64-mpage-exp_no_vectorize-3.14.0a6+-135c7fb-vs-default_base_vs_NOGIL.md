# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: exp_no_vectorize
- machine: linux-x86_64
- commit hash: 135c7fb
- commit date: 2025-04-07
- overall geometric mean: 1.086x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 291 ms: 1.15x slower                                              |
| docutils       | 2.58 sec                                                               | 2.79 sec: 1.08x slower                                            |
| sphinx         | 1.00 sec                                                               | 1.10 sec: 1.09x slower                                            |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 625 ms                                                                 | 534 ms: 1.17x faster                                              |
| async_tree_none_tg         | 261 ms                                                                 | 234 ms: 1.11x faster                                              |
| async_tree_io              | 627 ms                                                                 | 567 ms: 1.11x faster                                              |
| async_tree_memoization_tg  | 323 ms                                                                 | 295 ms: 1.09x faster                                              |
| coroutines                 | 24.8 ms                                                                | 23.2 ms: 1.07x faster                                             |
| async_tree_none            | 279 ms                                                                 | 268 ms: 1.04x faster                                              |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 486 ms: 1.03x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                              |
| async_tree_memoization     | 321 ms                                                                 | 325 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 514 ms: 1.02x slower                                              |
| async_generators           | 334 ms                                                                 | 367 ms: 1.10x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 196 ms                                                                 | 198 ms: 1.01x slower                                              |
| float          | 71.9 ms                                                                | 73.1 ms: 1.02x slower                                             |
| nbody          | 97.0 ms                                                                | 120 ms: 1.24x slower                                              |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 2.82 ms                                                                | 2.69 ms: 1.05x faster                                             |
| regex_v8       | 21.7 ms                                                                | 20.7 ms: 1.05x faster                                             |
| regex_dna      | 178 ms                                                                 | 175 ms: 1.01x faster                                              |
| regex_compile  | 129 ms                                                                 | 152 ms: 1.18x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 93.8 ms                                                                | 87.8 ms: 1.07x faster                                             |
| xml_etree_parse      | 130 ms                                                                 | 128 ms: 1.02x faster                                              |
| json_loads           | 27.2 us                                                                | 29.5 us: 1.08x slower                                             |
| pickle_pure_python   | 320 us                                                                 | 348 us: 1.09x slower                                              |
| unpickle_pure_python | 221 us                                                                 | 245 us: 1.11x slower                                              |
| json_dumps           | 11.3 ms                                                                | 12.7 ms: 1.13x slower                                             |
| tomli_loads          | 2.01 sec                                                               | 2.28 sec: 1.13x slower                                            |
| xml_etree_generate   | 85.1 ms                                                                | 96.8 ms: 1.14x slower                                             |
| xml_etree_process    | 60.4 ms                                                                | 70.4 ms: 1.17x slower                                             |
| Geometric mean       | (ref)                                                                  | 1.08x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 15.1 ms                                                                | 15.9 ms: 1.05x slower                                             |
| python_startup_no_site | 8.65 ms                                                                | 11.2 ms: 1.30x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| django_template | 36.3 ms                                                                | 42.0 ms: 1.16x slower                                             |
| genshi_xml      | 50.3 ms                                                                | 59.3 ms: 1.18x slower                                             |
| mako            | 12.2 ms                                                                | 15.7 ms: 1.29x slower                                             |
| genshi_text     | 21.6 ms                                                                | 28.0 ms: 1.30x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.23x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 4.34 ms                                                                | 1.78 ms: 2.43x faster                                             |
| create_gc_cycles           | 1.85 ms                                                                | 1.36 ms: 1.36x faster                                             |
| async_tree_io_tg           | 625 ms                                                                 | 534 ms: 1.17x faster                                              |
| async_tree_none_tg         | 261 ms                                                                 | 234 ms: 1.11x faster                                              |
| async_tree_io              | 627 ms                                                                 | 567 ms: 1.11x faster                                              |
| async_tree_memoization_tg  | 323 ms                                                                 | 295 ms: 1.09x faster                                              |
| sqlite_synth               | 2.21 us                                                                | 2.03 us: 1.09x faster                                             |
| xml_etree_iterparse        | 93.8 ms                                                                | 87.8 ms: 1.07x faster                                             |
| coroutines                 | 24.8 ms                                                                | 23.2 ms: 1.07x faster                                             |
| regex_effbot               | 2.82 ms                                                                | 2.69 ms: 1.05x faster                                             |
| regex_v8                   | 21.7 ms                                                                | 20.7 ms: 1.05x faster                                             |
| async_tree_none            | 279 ms                                                                 | 268 ms: 1.04x faster                                              |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 486 ms: 1.03x faster                                              |
| xml_etree_parse            | 130 ms                                                                 | 128 ms: 1.02x faster                                              |
| regex_dna                  | 178 ms                                                                 | 175 ms: 1.01x faster                                              |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                              |
| pidigits                   | 196 ms                                                                 | 198 ms: 1.01x slower                                              |
| async_tree_memoization     | 321 ms                                                                 | 325 ms: 1.01x slower                                              |
| float                      | 71.9 ms                                                                | 73.1 ms: 1.02x slower                                             |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 514 ms: 1.02x slower                                              |
| json                       | 4.94 ms                                                                | 5.04 ms: 1.02x slower                                             |
| pycparser                  | 1.16 sec                                                               | 1.18 sec: 1.02x slower                                            |
| python_startup             | 15.1 ms                                                                | 15.9 ms: 1.05x slower                                             |
| dulwich_log                | 68.3 ms                                                                | 72.7 ms: 1.06x slower                                             |
| bench_mp_pool              | 89.2 ms                                                                | 96.2 ms: 1.08x slower                                             |
| docutils                   | 2.58 sec                                                               | 2.79 sec: 1.08x slower                                            |
| spectral_norm              | 100 ms                                                                 | 109 ms: 1.08x slower                                              |
| bpe_tokeniser              | 4.33 sec                                                               | 4.70 sec: 1.08x slower                                            |
| json_loads                 | 27.2 us                                                                | 29.5 us: 1.08x slower                                             |
| pickle_pure_python         | 320 us                                                                 | 348 us: 1.09x slower                                              |
| sphinx                     | 1.00 sec                                                               | 1.10 sec: 1.09x slower                                            |
| logging_silent             | 103 ns                                                                 | 113 ns: 1.09x slower                                              |
| pprint_safe_repr           | 734 ms                                                                 | 803 ms: 1.09x slower                                              |
| k_core                     | 2.06 sec                                                               | 2.26 sec: 1.10x slower                                            |
| async_generators           | 334 ms                                                                 | 367 ms: 1.10x slower                                              |
| scimark_fft                | 327 ms                                                                 | 360 ms: 1.10x slower                                              |
| nqueens                    | 80.8 ms                                                                | 89.3 ms: 1.10x slower                                             |
| pylint                     | 286 ms                                                                 | 317 ms: 1.11x slower                                              |
| many_optionals             | 1.03 ms                                                                | 1.15 ms: 1.11x slower                                             |
| unpickle_pure_python       | 221 us                                                                 | 245 us: 1.11x slower                                              |
| deepcopy_reduce            | 2.70 us                                                                | 3.02 us: 1.12x slower                                             |
| pprint_pformat             | 1.50 sec                                                               | 1.68 sec: 1.12x slower                                            |
| scimark_lu                 | 119 ms                                                                 | 134 ms: 1.13x slower                                              |
| sqlglot_v2_normalize       | 106 ms                                                                 | 119 ms: 1.13x slower                                              |
| json_dumps                 | 11.3 ms                                                                | 12.7 ms: 1.13x slower                                             |
| subparsers                 | 22.3 ms                                                                | 25.2 ms: 1.13x slower                                             |
| tomli_loads                | 2.01 sec                                                               | 2.28 sec: 1.13x slower                                            |
| deltablue                  | 3.36 ms                                                                | 3.80 ms: 1.13x slower                                             |
| xml_etree_generate         | 85.1 ms                                                                | 96.8 ms: 1.14x slower                                             |
| telco                      | 7.33 ms                                                                | 8.35 ms: 1.14x slower                                             |
| sqlglot_v2_optimize        | 52.8 ms                                                                | 60.2 ms: 1.14x slower                                             |
| scimark_sor                | 115 ms                                                                 | 132 ms: 1.14x slower                                              |
| scimark_sparse_mat_mult    | 4.54 ms                                                                | 5.20 ms: 1.14x slower                                             |
| generators                 | 29.1 ms                                                                | 33.3 ms: 1.14x slower                                             |
| 2to3                       | 253 ms                                                                 | 291 ms: 1.15x slower                                              |
| pyflate                    | 424 ms                                                                 | 490 ms: 1.16x slower                                              |
| sympy_expand               | 469 ms                                                                 | 543 ms: 1.16x slower                                              |
| django_template            | 36.3 ms                                                                | 42.0 ms: 1.16x slower                                             |
| mdp                        | 1.17 sec                                                               | 1.36 sec: 1.16x slower                                            |
| logging_simple             | 6.27 us                                                                | 7.26 us: 1.16x slower                                             |
| deepcopy                   | 261 us                                                                 | 302 us: 1.16x slower                                              |
| xml_etree_process          | 60.4 ms                                                                | 70.4 ms: 1.17x slower                                             |
| sympy_sum                  | 159 ms                                                                 | 186 ms: 1.17x slower                                              |
| fannkuch                   | 399 ms                                                                 | 467 ms: 1.17x slower                                              |
| sympy_str                  | 280 ms                                                                 | 328 ms: 1.17x slower                                              |
| logging_format             | 7.00 us                                                                | 8.20 us: 1.17x slower                                             |
| sqlglot_v2_transpile       | 1.60 ms                                                                | 1.87 ms: 1.17x slower                                             |
| chaos                      | 55.8 ms                                                                | 65.4 ms: 1.17x slower                                             |
| go                         | 116 ms                                                                 | 136 ms: 1.17x slower                                              |
| regex_compile              | 129 ms                                                                 | 152 ms: 1.18x slower                                              |
| genshi_xml                 | 50.3 ms                                                                | 59.3 ms: 1.18x slower                                             |
| sqlalchemy_imperative      | 20.5 ms                                                                | 24.2 ms: 1.18x slower                                             |
| hexiom                     | 6.14 ms                                                                | 7.26 ms: 1.18x slower                                             |
| sympy_integrate            | 19.6 ms                                                                | 23.2 ms: 1.18x slower                                             |
| raytrace                   | 259 ms                                                                 | 309 ms: 1.19x slower                                              |
| sqlalchemy_declarative     | 133 ms                                                                 | 159 ms: 1.20x slower                                              |
| comprehensions             | 17.2 us                                                                | 20.6 us: 1.20x slower                                             |
| scimark_monte_carlo        | 64.1 ms                                                                | 77.3 ms: 1.21x slower                                             |
| sqlglot_v2_parse           | 1.28 ms                                                                | 1.55 ms: 1.21x slower                                             |
| shortest_path              | 443 ms                                                                 | 536 ms: 1.21x slower                                              |
| typing_runtime_protocols   | 163 us                                                                 | 200 us: 1.23x slower                                              |
| richards                   | 44.5 ms                                                                | 55.0 ms: 1.23x slower                                             |
| crypto_pyaes               | 69.9 ms                                                                | 86.3 ms: 1.24x slower                                             |
| connected_components       | 397 ms                                                                 | 491 ms: 1.24x slower                                              |
| nbody                      | 97.0 ms                                                                | 120 ms: 1.24x slower                                              |
| richards_super             | 50.9 ms                                                                | 63.2 ms: 1.24x slower                                             |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.26x slower                                              |
| deepcopy_memo              | 29.6 us                                                                | 37.5 us: 1.27x slower                                             |
| mako                       | 12.2 ms                                                                | 15.7 ms: 1.29x slower                                             |
| genshi_text                | 21.6 ms                                                                | 28.0 ms: 1.30x slower                                             |
| python_startup_no_site     | 8.65 ms                                                                | 11.2 ms: 1.30x slower                                             |
| coverage                   | 81.9 ms                                                                | 108 ms: 1.32x slower                                              |
| bench_thread_pool          | 1.06 ms                                                                | 3.16 ms: 2.97x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.11x slower                                                      |

Benchmark hidden because not significant (1): pathlib
Ignored benchmarks (1) of results/bm-20250407-3.14.0a6+-135c7fb-NOGIL/bm-20250407-vultr-x86_64-mpage-exp_no_vectorize-3.14.0a6+-135c7fb.json: html5lib

- Geometric mean (including insignificant results): 1.086x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x