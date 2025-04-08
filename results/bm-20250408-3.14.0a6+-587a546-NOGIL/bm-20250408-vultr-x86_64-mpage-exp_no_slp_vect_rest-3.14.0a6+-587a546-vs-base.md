# Results vs. base

- fork: mpage
- ref: exp_no_slp_vect_rest
- machine: linux-x86_64
- commit hash: 587a546
- commit date: 2025-04-08
- overall geometric mean: 1.058x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 310 ms                                                                 | 293 ms: 1.06x faster                                                  |
| docutils       | 2.90 sec                                                               | 2.80 sec: 1.03x faster                                                |
| html5lib       | 75.4 ms                                                                | 70.9 ms: 1.06x faster                                                 |
| sphinx         | 1.15 sec                                                               | 1.10 sec: 1.04x faster                                                |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines                 | 26.7 ms                                                                | 23.9 ms: 1.11x faster                                                 |
| async_generators           | 387 ms                                                                 | 367 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 246 ms                                                                 | 237 ms: 1.04x faster                                                  |
| async_tree_memoization     | 341 ms                                                                 | 328 ms: 1.04x faster                                                  |
| async_tree_io_tg           | 563 ms                                                                 | 545 ms: 1.03x faster                                                  |
| async_tree_io              | 592 ms                                                                 | 573 ms: 1.03x faster                                                  |
| async_tree_memoization_tg  | 310 ms                                                                 | 300 ms: 1.03x faster                                                  |
| async_tree_none            | 280 ms                                                                 | 271 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed    | 525 ms                                                                 | 517 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                 | 489 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 136 ms                                                                 | 119 ms: 1.14x faster                                                  |
| float          | 76.6 ms                                                                | 70.8 ms: 1.08x faster                                                 |
| pidigits       | 192 ms                                                                 | 189 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 168 ms                                                                 | 153 ms: 1.10x faster                                                  |
| regex_effbot   | 2.85 ms                                                                | 2.73 ms: 1.04x faster                                                 |
| regex_v8       | 21.3 ms                                                                | 21.0 ms: 1.01x faster                                                 |
| regex_dna      | 177 ms                                                                 | 180 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.53 sec                                                               | 2.29 sec: 1.10x faster                                                |
| unpickle_pure_python | 269 us                                                                 | 248 us: 1.08x faster                                                  |
| pickle_pure_python   | 377 us                                                                 | 349 us: 1.08x faster                                                  |
| xml_etree_generate   | 102 ms                                                                 | 95.6 ms: 1.07x faster                                                 |
| xml_etree_iterparse  | 92.2 ms                                                                | 87.2 ms: 1.06x faster                                                 |
| xml_etree_process    | 74.0 ms                                                                | 70.1 ms: 1.06x faster                                                 |
| json_dumps           | 13.2 ms                                                                | 12.9 ms: 1.03x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.02x faster                                                  |
| json_loads           | 29.7 us                                                                | 29.3 us: 1.01x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.9 ms                                                                | 16.0 ms: 1.00x slower                                                 |
| python_startup_no_site | 11.2 ms                                                                | 11.2 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                                | 28.5 ms: 1.11x faster                                                 |
| genshi_xml      | 67.3 ms                                                                | 60.5 ms: 1.11x faster                                                 |
| mako            | 16.5 ms                                                                | 15.6 ms: 1.06x faster                                                 |
| django_template | 44.5 ms                                                                | 42.2 ms: 1.06x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.09x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vect_rest-3.14.0a6+-587a546 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| generators                 | 44.8 ms                                                                | 33.4 ms: 1.34x faster                                                 |
| scimark_sor                | 152 ms                                                                 | 130 ms: 1.17x faster                                                  |
| deltablue                  | 4.47 ms                                                                | 3.85 ms: 1.16x faster                                                 |
| nbody                      | 136 ms                                                                 | 119 ms: 1.14x faster                                                  |
| logging_simple             | 8.36 us                                                                | 7.35 us: 1.14x faster                                                 |
| logging_format             | 9.41 us                                                                | 8.31 us: 1.13x faster                                                 |
| go                         | 153 ms                                                                 | 137 ms: 1.11x faster                                                  |
| coroutines                 | 26.7 ms                                                                | 23.9 ms: 1.11x faster                                                 |
| genshi_text                | 31.7 ms                                                                | 28.5 ms: 1.11x faster                                                 |
| genshi_xml                 | 67.3 ms                                                                | 60.5 ms: 1.11x faster                                                 |
| hexiom                     | 8.07 ms                                                                | 7.31 ms: 1.10x faster                                                 |
| tomli_loads                | 2.53 sec                                                               | 2.29 sec: 1.10x faster                                                |
| logging_silent             | 126 ns                                                                 | 115 ns: 1.10x faster                                                  |
| regex_compile              | 168 ms                                                                 | 153 ms: 1.10x faster                                                  |
| chaos                      | 71.8 ms                                                                | 65.6 ms: 1.09x faster                                                 |
| deepcopy_reduce            | 3.29 us                                                                | 3.02 us: 1.09x faster                                                 |
| richards                   | 60.1 ms                                                                | 55.1 ms: 1.09x faster                                                 |
| nqueens                    | 100 ms                                                                 | 91.8 ms: 1.09x faster                                                 |
| pyflate                    | 527 ms                                                                 | 485 ms: 1.09x faster                                                  |
| unpickle_pure_python       | 269 us                                                                 | 248 us: 1.08x faster                                                  |
| float                      | 76.6 ms                                                                | 70.8 ms: 1.08x faster                                                 |
| scimark_lu                 | 145 ms                                                                 | 134 ms: 1.08x faster                                                  |
| fannkuch                   | 511 ms                                                                 | 472 ms: 1.08x faster                                                  |
| pickle_pure_python         | 377 us                                                                 | 349 us: 1.08x faster                                                  |
| raytrace                   | 336 ms                                                                 | 311 ms: 1.08x faster                                                  |
| scimark_monte_carlo        | 83.2 ms                                                                | 77.1 ms: 1.08x faster                                                 |
| richards_super             | 68.3 ms                                                                | 63.5 ms: 1.08x faster                                                 |
| pprint_safe_repr           | 875 ms                                                                 | 814 ms: 1.07x faster                                                  |
| spectral_norm              | 118 ms                                                                 | 110 ms: 1.07x faster                                                  |
| deepcopy                   | 322 us                                                                 | 300 us: 1.07x faster                                                  |
| sqlglot_v2_normalize       | 127 ms                                                                 | 119 ms: 1.07x faster                                                  |
| xml_etree_generate         | 102 ms                                                                 | 95.6 ms: 1.07x faster                                                 |
| deepcopy_memo              | 40.3 us                                                                | 37.8 us: 1.06x faster                                                 |
| pprint_pformat             | 1.82 sec                                                               | 1.71 sec: 1.06x faster                                                |
| html5lib                   | 75.4 ms                                                                | 70.9 ms: 1.06x faster                                                 |
| sqlglot_v2_transpile       | 2.00 ms                                                                | 1.88 ms: 1.06x faster                                                 |
| mako                       | 16.5 ms                                                                | 15.6 ms: 1.06x faster                                                 |
| sqlglot_v2_optimize        | 63.9 ms                                                                | 60.2 ms: 1.06x faster                                                 |
| comprehensions             | 22.1 us                                                                | 20.9 us: 1.06x faster                                                 |
| scimark_fft                | 378 ms                                                                 | 357 ms: 1.06x faster                                                  |
| mdp                        | 1.46 sec                                                               | 1.37 sec: 1.06x faster                                                |
| sympy_expand               | 579 ms                                                                 | 547 ms: 1.06x faster                                                  |
| xml_etree_iterparse        | 92.2 ms                                                                | 87.2 ms: 1.06x faster                                                 |
| typing_runtime_protocols   | 208 us                                                                 | 197 us: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 5.44 ms                                                                | 5.15 ms: 1.06x faster                                                 |
| sqlglot_v2_parse           | 1.64 ms                                                                | 1.56 ms: 1.06x faster                                                 |
| 2to3                       | 310 ms                                                                 | 293 ms: 1.06x faster                                                  |
| xml_etree_process          | 74.0 ms                                                                | 70.1 ms: 1.06x faster                                                 |
| django_template            | 44.5 ms                                                                | 42.2 ms: 1.06x faster                                                 |
| async_generators           | 387 ms                                                                 | 367 ms: 1.05x faster                                                  |
| dulwich_log                | 77.4 ms                                                                | 73.4 ms: 1.05x faster                                                 |
| crypto_pyaes               | 90.7 ms                                                                | 86.2 ms: 1.05x faster                                                 |
| sympy_str                  | 350 ms                                                                 | 332 ms: 1.05x faster                                                  |
| bpe_tokeniser              | 4.91 sec                                                               | 4.67 sec: 1.05x faster                                                |
| pycparser                  | 1.24 sec                                                               | 1.18 sec: 1.05x faster                                                |
| many_optionals             | 1.21 ms                                                                | 1.16 ms: 1.05x faster                                                 |
| regex_effbot               | 2.85 ms                                                                | 2.73 ms: 1.04x faster                                                 |
| sphinx                     | 1.15 sec                                                               | 1.10 sec: 1.04x faster                                                |
| async_tree_none_tg         | 246 ms                                                                 | 237 ms: 1.04x faster                                                  |
| subparsers                 | 26.8 ms                                                                | 25.8 ms: 1.04x faster                                                 |
| async_tree_memoization     | 341 ms                                                                 | 328 ms: 1.04x faster                                                  |
| shortest_path              | 554 ms                                                                 | 534 ms: 1.04x faster                                                  |
| connected_components       | 510 ms                                                                 | 492 ms: 1.04x faster                                                  |
| meteor_contest             | 132 ms                                                                 | 127 ms: 1.04x faster                                                  |
| sympy_sum                  | 192 ms                                                                 | 186 ms: 1.04x faster                                                  |
| pylint                     | 330 ms                                                                 | 319 ms: 1.03x faster                                                  |
| async_tree_io_tg           | 563 ms                                                                 | 545 ms: 1.03x faster                                                  |
| async_tree_io              | 592 ms                                                                 | 573 ms: 1.03x faster                                                  |
| docutils                   | 2.90 sec                                                               | 2.80 sec: 1.03x faster                                                |
| async_tree_memoization_tg  | 310 ms                                                                 | 300 ms: 1.03x faster                                                  |
| sympy_integrate            | 24.1 ms                                                                | 23.3 ms: 1.03x faster                                                 |
| async_tree_none            | 280 ms                                                                 | 271 ms: 1.03x faster                                                  |
| sqlalchemy_declarative     | 164 ms                                                                 | 160 ms: 1.03x faster                                                  |
| json_dumps                 | 13.2 ms                                                                | 12.9 ms: 1.03x faster                                                 |
| sqlalchemy_imperative      | 24.9 ms                                                                | 24.4 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.05 us                                                                | 2.01 us: 1.02x faster                                                 |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.02x faster                                                  |
| coverage                   | 109 ms                                                                 | 107 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed    | 525 ms                                                                 | 517 ms: 1.01x faster                                                  |
| pidigits                   | 192 ms                                                                 | 189 ms: 1.01x faster                                                  |
| k_core                     | 2.29 sec                                                               | 2.26 sec: 1.01x faster                                                |
| json_loads                 | 29.7 us                                                                | 29.3 us: 1.01x faster                                                 |
| regex_v8                   | 21.3 ms                                                                | 21.0 ms: 1.01x faster                                                 |
| json                       | 5.12 ms                                                                | 5.06 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed_tg | 495 ms                                                                 | 489 ms: 1.01x faster                                                  |
| pathlib                    | 19.9 ms                                                                | 19.7 ms: 1.01x faster                                                 |
| bench_thread_pool          | 3.18 ms                                                                | 3.16 ms: 1.01x faster                                                 |
| bench_mp_pool              | 96.9 ms                                                                | 96.4 ms: 1.01x faster                                                 |
| python_startup             | 15.9 ms                                                                | 16.0 ms: 1.00x slower                                                 |
| python_startup_no_site     | 11.2 ms                                                                | 11.2 ms: 1.00x slower                                                 |
| gc_traversal               | 1.78 ms                                                                | 1.80 ms: 1.01x slower                                                 |
| regex_dna                  | 177 ms                                                                 | 180 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (3): asyncio_websockets, telco, create_gc_cycles

- Geometric mean (including insignificant results): 1.058x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.01x