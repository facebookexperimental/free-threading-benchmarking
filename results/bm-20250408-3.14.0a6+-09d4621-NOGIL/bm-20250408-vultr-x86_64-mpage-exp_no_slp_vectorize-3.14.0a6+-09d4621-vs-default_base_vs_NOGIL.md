# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 09d4621
- commit date: 2025-04-08
- overall geometric mean: 1.090x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 293 ms: 1.16x slower                                                  |
| docutils       | 2.58 sec                                                               | 2.80 sec: 1.09x slower                                                |
| sphinx         | 1.00 sec                                                               | 1.10 sec: 1.09x slower                                                |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 625 ms                                                                 | 537 ms: 1.17x faster                                                  |
| async_tree_none_tg         | 261 ms                                                                 | 233 ms: 1.12x faster                                                  |
| async_tree_io              | 627 ms                                                                 | 567 ms: 1.11x faster                                                  |
| async_tree_memoization_tg  | 323 ms                                                                 | 295 ms: 1.09x faster                                                  |
| async_tree_none            | 279 ms                                                                 | 267 ms: 1.04x faster                                                  |
| coroutines                 | 24.8 ms                                                                | 24.1 ms: 1.03x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                  |
| async_tree_memoization     | 321 ms                                                                 | 325 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 532 ms: 1.07x slower                                                  |
| async_generators           | 334 ms                                                                 | 367 ms: 1.10x slower                                                  |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 560 ms: 1.11x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 196 ms                                                                 | 218 ms: 1.11x slower                                                  |
| nbody          | 97.0 ms                                                                | 123 ms: 1.26x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 21.7 ms                                                                | 21.1 ms: 1.03x faster                                                 |
| regex_effbot   | 2.82 ms                                                                | 2.86 ms: 1.01x slower                                                 |
| regex_dna      | 178 ms                                                                 | 183 ms: 1.03x slower                                                  |
| regex_compile  | 129 ms                                                                 | 153 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.8 ms                                                                | 86.7 ms: 1.08x faster                                                 |
| xml_etree_parse      | 130 ms                                                                 | 127 ms: 1.02x faster                                                  |
| json_loads           | 27.2 us                                                                | 29.2 us: 1.08x slower                                                 |
| pickle_pure_python   | 320 us                                                                 | 349 us: 1.09x slower                                                  |
| unpickle_pure_python | 221 us                                                                 | 245 us: 1.11x slower                                                  |
| json_dumps           | 11.3 ms                                                                | 12.7 ms: 1.12x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.26 sec: 1.12x slower                                                |
| xml_etree_generate   | 85.1 ms                                                                | 95.8 ms: 1.13x slower                                                 |
| xml_etree_process    | 60.4 ms                                                                | 70.1 ms: 1.16x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.1 ms                                                                | 15.9 ms: 1.05x slower                                                 |
| python_startup_no_site | 8.65 ms                                                                | 11.2 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 36.3 ms                                                                | 41.7 ms: 1.15x slower                                                 |
| genshi_xml      | 50.3 ms                                                                | 59.5 ms: 1.18x slower                                                 |
| mako            | 12.2 ms                                                                | 15.6 ms: 1.29x slower                                                 |
| genshi_text     | 21.6 ms                                                                | 27.8 ms: 1.29x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.34 ms                                                                | 1.79 ms: 2.43x faster                                                 |
| create_gc_cycles           | 1.85 ms                                                                | 1.35 ms: 1.37x faster                                                 |
| async_tree_io_tg           | 625 ms                                                                 | 537 ms: 1.17x faster                                                  |
| async_tree_none_tg         | 261 ms                                                                 | 233 ms: 1.12x faster                                                  |
| async_tree_io              | 627 ms                                                                 | 567 ms: 1.11x faster                                                  |
| async_tree_memoization_tg  | 323 ms                                                                 | 295 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.21 us                                                                | 2.03 us: 1.09x faster                                                 |
| xml_etree_iterparse        | 93.8 ms                                                                | 86.7 ms: 1.08x faster                                                 |
| async_tree_none            | 279 ms                                                                 | 267 ms: 1.04x faster                                                  |
| regex_v8                   | 21.7 ms                                                                | 21.1 ms: 1.03x faster                                                 |
| coroutines                 | 24.8 ms                                                                | 24.1 ms: 1.03x faster                                                 |
| xml_etree_parse            | 130 ms                                                                 | 127 ms: 1.02x faster                                                  |
| pathlib                    | 19.7 ms                                                                | 19.4 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                  |
| regex_effbot               | 2.82 ms                                                                | 2.86 ms: 1.01x slower                                                 |
| pycparser                  | 1.16 sec                                                               | 1.17 sec: 1.01x slower                                                |
| async_tree_memoization     | 321 ms                                                                 | 325 ms: 1.01x slower                                                  |
| regex_dna                  | 178 ms                                                                 | 183 ms: 1.03x slower                                                  |
| json                       | 4.94 ms                                                                | 5.11 ms: 1.03x slower                                                 |
| python_startup             | 15.1 ms                                                                | 15.9 ms: 1.05x slower                                                 |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 532 ms: 1.07x slower                                                  |
| dulwich_log                | 68.3 ms                                                                | 73.2 ms: 1.07x slower                                                 |
| logging_silent             | 103 ns                                                                 | 110 ns: 1.07x slower                                                  |
| json_loads                 | 27.2 us                                                                | 29.2 us: 1.08x slower                                                 |
| bench_mp_pool              | 89.2 ms                                                                | 96.3 ms: 1.08x slower                                                 |
| bpe_tokeniser              | 4.33 sec                                                               | 4.68 sec: 1.08x slower                                                |
| docutils                   | 2.58 sec                                                               | 2.80 sec: 1.09x slower                                                |
| spectral_norm              | 100 ms                                                                 | 109 ms: 1.09x slower                                                  |
| scimark_fft                | 327 ms                                                                 | 356 ms: 1.09x slower                                                  |
| pickle_pure_python         | 320 us                                                                 | 349 us: 1.09x slower                                                  |
| sphinx                     | 1.00 sec                                                               | 1.10 sec: 1.09x slower                                                |
| k_core                     | 2.06 sec                                                               | 2.26 sec: 1.10x slower                                                |
| async_generators           | 334 ms                                                                 | 367 ms: 1.10x slower                                                  |
| pprint_safe_repr           | 734 ms                                                                 | 811 ms: 1.11x slower                                                  |
| pylint                     | 286 ms                                                                 | 317 ms: 1.11x slower                                                  |
| unpickle_pure_python       | 221 us                                                                 | 245 us: 1.11x slower                                                  |
| async_tree_cpu_io_mixed    | 505 ms                                                                 | 560 ms: 1.11x slower                                                  |
| many_optionals             | 1.03 ms                                                                | 1.15 ms: 1.11x slower                                                 |
| pidigits                   | 196 ms                                                                 | 218 ms: 1.11x slower                                                  |
| sqlglot_v2_normalize       | 106 ms                                                                 | 118 ms: 1.12x slower                                                  |
| json_dumps                 | 11.3 ms                                                                | 12.7 ms: 1.12x slower                                                 |
| scimark_sor                | 115 ms                                                                 | 129 ms: 1.12x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.26 sec: 1.12x slower                                                |
| nqueens                    | 80.8 ms                                                                | 90.7 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.1 ms                                                                | 95.8 ms: 1.13x slower                                                 |
| pprint_pformat             | 1.50 sec                                                               | 1.69 sec: 1.13x slower                                                |
| scimark_lu                 | 119 ms                                                                 | 135 ms: 1.13x slower                                                  |
| subparsers                 | 22.3 ms                                                                | 25.2 ms: 1.13x slower                                                 |
| deepcopy_reduce            | 2.70 us                                                                | 3.05 us: 1.13x slower                                                 |
| sqlglot_v2_optimize        | 52.8 ms                                                                | 59.8 ms: 1.13x slower                                                 |
| telco                      | 7.33 ms                                                                | 8.41 ms: 1.15x slower                                                 |
| django_template            | 36.3 ms                                                                | 41.7 ms: 1.15x slower                                                 |
| scimark_sparse_mat_mult    | 4.54 ms                                                                | 5.22 ms: 1.15x slower                                                 |
| deepcopy                   | 261 us                                                                 | 300 us: 1.15x slower                                                  |
| generators                 | 29.1 ms                                                                | 33.5 ms: 1.15x slower                                                 |
| deltablue                  | 3.36 ms                                                                | 3.88 ms: 1.16x slower                                                 |
| 2to3                       | 253 ms                                                                 | 293 ms: 1.16x slower                                                  |
| xml_etree_process          | 60.4 ms                                                                | 70.1 ms: 1.16x slower                                                 |
| sympy_expand               | 469 ms                                                                 | 545 ms: 1.16x slower                                                  |
| sympy_sum                  | 159 ms                                                                 | 185 ms: 1.16x slower                                                  |
| pyflate                    | 424 ms                                                                 | 494 ms: 1.17x slower                                                  |
| mdp                        | 1.17 sec                                                               | 1.37 sec: 1.17x slower                                                |
| chaos                      | 55.8 ms                                                                | 65.4 ms: 1.17x slower                                                 |
| sympy_str                  | 280 ms                                                                 | 330 ms: 1.18x slower                                                  |
| sqlglot_v2_transpile       | 1.60 ms                                                                | 1.88 ms: 1.18x slower                                                 |
| fannkuch                   | 399 ms                                                                 | 470 ms: 1.18x slower                                                  |
| go                         | 116 ms                                                                 | 137 ms: 1.18x slower                                                  |
| regex_compile              | 129 ms                                                                 | 153 ms: 1.18x slower                                                  |
| comprehensions             | 17.2 us                                                                | 20.3 us: 1.18x slower                                                 |
| logging_simple             | 6.27 us                                                                | 7.40 us: 1.18x slower                                                 |
| hexiom                     | 6.14 ms                                                                | 7.27 ms: 1.18x slower                                                 |
| sqlalchemy_imperative      | 20.5 ms                                                                | 24.2 ms: 1.18x slower                                                 |
| genshi_xml                 | 50.3 ms                                                                | 59.5 ms: 1.18x slower                                                 |
| sympy_integrate            | 19.6 ms                                                                | 23.3 ms: 1.19x slower                                                 |
| raytrace                   | 259 ms                                                                 | 309 ms: 1.19x slower                                                  |
| logging_format             | 7.00 us                                                                | 8.37 us: 1.20x slower                                                 |
| sqlalchemy_declarative     | 133 ms                                                                 | 159 ms: 1.20x slower                                                  |
| scimark_monte_carlo        | 64.1 ms                                                                | 77.3 ms: 1.21x slower                                                 |
| shortest_path              | 443 ms                                                                 | 535 ms: 1.21x slower                                                  |
| sqlglot_v2_parse           | 1.28 ms                                                                | 1.56 ms: 1.21x slower                                                 |
| typing_runtime_protocols   | 163 us                                                                 | 198 us: 1.22x slower                                                  |
| connected_components       | 397 ms                                                                 | 490 ms: 1.23x slower                                                  |
| richards                   | 44.5 ms                                                                | 55.1 ms: 1.24x slower                                                 |
| crypto_pyaes               | 69.9 ms                                                                | 87.1 ms: 1.25x slower                                                 |
| richards_super             | 50.9 ms                                                                | 63.4 ms: 1.25x slower                                                 |
| deepcopy_memo              | 29.6 us                                                                | 36.9 us: 1.25x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 127 ms: 1.25x slower                                                  |
| nbody                      | 97.0 ms                                                                | 123 ms: 1.26x slower                                                  |
| mako                       | 12.2 ms                                                                | 15.6 ms: 1.29x slower                                                 |
| genshi_text                | 21.6 ms                                                                | 27.8 ms: 1.29x slower                                                 |
| python_startup_no_site     | 8.65 ms                                                                | 11.2 ms: 1.29x slower                                                 |
| coverage                   | 81.9 ms                                                                | 107 ms: 1.31x slower                                                  |
| bench_thread_pool          | 1.06 ms                                                                | 3.15 ms: 2.97x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.11x slower                                                          |

Benchmark hidden because not significant (1): float
Ignored benchmarks (1) of results/bm-20250408-3.14.0a6+-09d4621-NOGIL/bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621.json: html5lib

- Geometric mean (including insignificant results): 1.090x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.21x