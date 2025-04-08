# Results vs. base

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 09d4621
- commit date: 2025-04-08
- overall geometric mean: 1.057x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 310 ms                                                                 | 293 ms: 1.06x faster                                                  |
| docutils       | 2.90 sec                                                               | 2.80 sec: 1.03x faster                                                |
| html5lib       | 75.4 ms                                                                | 70.7 ms: 1.07x faster                                                 |
| sphinx         | 1.15 sec                                                               | 1.10 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 26.7 ms                                                                | 24.1 ms: 1.11x faster                                                 |
| async_tree_none_tg         | 246 ms                                                                 | 233 ms: 1.06x faster                                                  |
| async_generators           | 387 ms                                                                 | 367 ms: 1.05x faster                                                  |
| async_tree_memoization_tg  | 310 ms                                                                 | 295 ms: 1.05x faster                                                  |
| async_tree_memoization     | 341 ms                                                                 | 325 ms: 1.05x faster                                                  |
| async_tree_io_tg           | 563 ms                                                                 | 537 ms: 1.05x faster                                                  |
| async_tree_none            | 280 ms                                                                 | 267 ms: 1.05x faster                                                  |
| async_tree_io              | 592 ms                                                                 | 567 ms: 1.04x faster                                                  |
| asyncio_websockets         | 516 ms                                                                 | 515 ms: 1.00x faster                                                  |
| async_tree_cpu_io_mixed    | 525 ms                                                                 | 560 ms: 1.07x slower                                                  |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                 | 532 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 136 ms                                                                 | 123 ms: 1.11x faster                                                  |
| float          | 76.6 ms                                                                | 71.6 ms: 1.07x faster                                                 |
| pidigits       | 192 ms                                                                 | 218 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 168 ms                                                                 | 153 ms: 1.10x faster                                                  |
| regex_dna      | 177 ms                                                                 | 183 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.53 sec                                                               | 2.26 sec: 1.12x faster                                                |
| unpickle_pure_python | 269 us                                                                 | 245 us: 1.10x faster                                                  |
| pickle_pure_python   | 377 us                                                                 | 349 us: 1.08x faster                                                  |
| xml_etree_iterparse  | 92.2 ms                                                                | 86.7 ms: 1.06x faster                                                 |
| xml_etree_generate   | 102 ms                                                                 | 95.8 ms: 1.06x faster                                                 |
| xml_etree_process    | 74.0 ms                                                                | 70.1 ms: 1.05x faster                                                 |
| json_dumps           | 13.2 ms                                                                | 12.7 ms: 1.04x faster                                                 |
| json_loads           | 29.7 us                                                                | 29.2 us: 1.02x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.02x faster                                                  |
| Geometric mean       | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.9 ms                                                                | 15.9 ms: 1.00x faster                                                 |
| python_startup_no_site | 11.2 ms                                                                | 11.2 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                                | 27.8 ms: 1.14x faster                                                 |
| genshi_xml      | 67.3 ms                                                                | 59.5 ms: 1.13x faster                                                 |
| django_template | 44.5 ms                                                                | 41.7 ms: 1.07x faster                                                 |
| mako            | 16.5 ms                                                                | 15.6 ms: 1.06x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.10x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| generators                 | 44.8 ms                                                                | 33.5 ms: 1.34x faster                                                 |
| scimark_sor                | 152 ms                                                                 | 129 ms: 1.18x faster                                                  |
| deltablue                  | 4.47 ms                                                                | 3.88 ms: 1.15x faster                                                 |
| logging_silent             | 126 ns                                                                 | 110 ns: 1.14x faster                                                  |
| genshi_text                | 31.7 ms                                                                | 27.8 ms: 1.14x faster                                                 |
| genshi_xml                 | 67.3 ms                                                                | 59.5 ms: 1.13x faster                                                 |
| logging_simple             | 8.36 us                                                                | 7.40 us: 1.13x faster                                                 |
| logging_format             | 9.41 us                                                                | 8.37 us: 1.12x faster                                                 |
| tomli_loads                | 2.53 sec                                                               | 2.26 sec: 1.12x faster                                                |
| go                         | 153 ms                                                                 | 137 ms: 1.12x faster                                                  |
| hexiom                     | 8.07 ms                                                                | 7.27 ms: 1.11x faster                                                 |
| nbody                      | 136 ms                                                                 | 123 ms: 1.11x faster                                                  |
| coroutines                 | 26.7 ms                                                                | 24.1 ms: 1.11x faster                                                 |
| nqueens                    | 100 ms                                                                 | 90.7 ms: 1.10x faster                                                 |
| regex_compile              | 168 ms                                                                 | 153 ms: 1.10x faster                                                  |
| unpickle_pure_python       | 269 us                                                                 | 245 us: 1.10x faster                                                  |
| chaos                      | 71.8 ms                                                                | 65.4 ms: 1.10x faster                                                 |
| comprehensions             | 22.1 us                                                                | 20.3 us: 1.09x faster                                                 |
| richards                   | 60.1 ms                                                                | 55.1 ms: 1.09x faster                                                 |
| deepcopy_memo              | 40.3 us                                                                | 36.9 us: 1.09x faster                                                 |
| raytrace                   | 336 ms                                                                 | 309 ms: 1.09x faster                                                  |
| fannkuch                   | 511 ms                                                                 | 470 ms: 1.09x faster                                                  |
| pickle_pure_python         | 377 us                                                                 | 349 us: 1.08x faster                                                  |
| sqlglot_v2_normalize       | 127 ms                                                                 | 118 ms: 1.08x faster                                                  |
| deepcopy_reduce            | 3.29 us                                                                | 3.05 us: 1.08x faster                                                 |
| pprint_safe_repr           | 875 ms                                                                 | 811 ms: 1.08x faster                                                  |
| spectral_norm              | 118 ms                                                                 | 109 ms: 1.08x faster                                                  |
| richards_super             | 68.3 ms                                                                | 63.4 ms: 1.08x faster                                                 |
| scimark_monte_carlo        | 83.2 ms                                                                | 77.3 ms: 1.08x faster                                                 |
| scimark_lu                 | 145 ms                                                                 | 135 ms: 1.08x faster                                                  |
| pprint_pformat             | 1.82 sec                                                               | 1.69 sec: 1.07x faster                                                |
| deepcopy                   | 322 us                                                                 | 300 us: 1.07x faster                                                  |
| float                      | 76.6 ms                                                                | 71.6 ms: 1.07x faster                                                 |
| django_template            | 44.5 ms                                                                | 41.7 ms: 1.07x faster                                                 |
| sqlglot_v2_optimize        | 63.9 ms                                                                | 59.8 ms: 1.07x faster                                                 |
| html5lib                   | 75.4 ms                                                                | 70.7 ms: 1.07x faster                                                 |
| pyflate                    | 527 ms                                                                 | 494 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 92.2 ms                                                                | 86.7 ms: 1.06x faster                                                 |
| sympy_expand               | 579 ms                                                                 | 545 ms: 1.06x faster                                                  |
| xml_etree_generate         | 102 ms                                                                 | 95.8 ms: 1.06x faster                                                 |
| scimark_fft                | 378 ms                                                                 | 356 ms: 1.06x faster                                                  |
| sqlglot_v2_transpile       | 2.00 ms                                                                | 1.88 ms: 1.06x faster                                                 |
| subparsers                 | 26.8 ms                                                                | 25.2 ms: 1.06x faster                                                 |
| mdp                        | 1.46 sec                                                               | 1.37 sec: 1.06x faster                                                |
| pycparser                  | 1.24 sec                                                               | 1.17 sec: 1.06x faster                                                |
| sympy_str                  | 350 ms                                                                 | 330 ms: 1.06x faster                                                  |
| async_tree_none_tg         | 246 ms                                                                 | 233 ms: 1.06x faster                                                  |
| dulwich_log                | 77.4 ms                                                                | 73.2 ms: 1.06x faster                                                 |
| sqlglot_v2_parse           | 1.64 ms                                                                | 1.56 ms: 1.06x faster                                                 |
| mako                       | 16.5 ms                                                                | 15.6 ms: 1.06x faster                                                 |
| 2to3                       | 310 ms                                                                 | 293 ms: 1.06x faster                                                  |
| many_optionals             | 1.21 ms                                                                | 1.15 ms: 1.06x faster                                                 |
| xml_etree_process          | 74.0 ms                                                                | 70.1 ms: 1.05x faster                                                 |
| async_generators           | 387 ms                                                                 | 367 ms: 1.05x faster                                                  |
| async_tree_memoization_tg  | 310 ms                                                                 | 295 ms: 1.05x faster                                                  |
| async_tree_memoization     | 341 ms                                                                 | 325 ms: 1.05x faster                                                  |
| typing_runtime_protocols   | 208 us                                                                 | 198 us: 1.05x faster                                                  |
| async_tree_io_tg           | 563 ms                                                                 | 537 ms: 1.05x faster                                                  |
| bpe_tokeniser              | 4.91 sec                                                               | 4.68 sec: 1.05x faster                                                |
| async_tree_none            | 280 ms                                                                 | 267 ms: 1.05x faster                                                  |
| async_tree_io              | 592 ms                                                                 | 567 ms: 1.04x faster                                                  |
| sphinx                     | 1.15 sec                                                               | 1.10 sec: 1.04x faster                                                |
| json_dumps                 | 13.2 ms                                                                | 12.7 ms: 1.04x faster                                                 |
| scimark_sparse_mat_mult    | 5.44 ms                                                                | 5.22 ms: 1.04x faster                                                 |
| crypto_pyaes               | 90.7 ms                                                                | 87.1 ms: 1.04x faster                                                 |
| sympy_sum                  | 192 ms                                                                 | 185 ms: 1.04x faster                                                  |
| connected_components       | 510 ms                                                                 | 490 ms: 1.04x faster                                                  |
| pylint                     | 330 ms                                                                 | 317 ms: 1.04x faster                                                  |
| meteor_contest             | 132 ms                                                                 | 127 ms: 1.04x faster                                                  |
| shortest_path              | 554 ms                                                                 | 535 ms: 1.04x faster                                                  |
| sympy_integrate            | 24.1 ms                                                                | 23.3 ms: 1.04x faster                                                 |
| sqlalchemy_declarative     | 164 ms                                                                 | 159 ms: 1.03x faster                                                  |
| docutils                   | 2.90 sec                                                               | 2.80 sec: 1.03x faster                                                |
| sqlalchemy_imperative      | 24.9 ms                                                                | 24.2 ms: 1.03x faster                                                 |
| pathlib                    | 19.9 ms                                                                | 19.4 ms: 1.02x faster                                                 |
| json_loads                 | 29.7 us                                                                | 29.2 us: 1.02x faster                                                 |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.02x faster                                                  |
| coverage                   | 109 ms                                                                 | 107 ms: 1.02x faster                                                  |
| k_core                     | 2.29 sec                                                               | 2.26 sec: 1.01x faster                                                |
| bench_thread_pool          | 3.18 ms                                                                | 3.15 ms: 1.01x faster                                                 |
| telco                      | 8.47 ms                                                                | 8.41 ms: 1.01x faster                                                 |
| bench_mp_pool              | 96.9 ms                                                                | 96.3 ms: 1.01x faster                                                 |
| asyncio_websockets         | 516 ms                                                                 | 515 ms: 1.00x faster                                                  |
| python_startup             | 15.9 ms                                                                | 15.9 ms: 1.00x faster                                                 |
| python_startup_no_site     | 11.2 ms                                                                | 11.2 ms: 1.00x faster                                                 |
| regex_dna                  | 177 ms                                                                 | 183 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed    | 525 ms                                                                 | 560 ms: 1.07x slower                                                  |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                 | 532 ms: 1.08x slower                                                  |
| pidigits                   | 192 ms                                                                 | 218 ms: 1.14x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (6): regex_v8, sqlite_synth, json, gc_traversal, create_gc_cycles, regex_effbot

- Geometric mean (including insignificant results): 1.057x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.02x