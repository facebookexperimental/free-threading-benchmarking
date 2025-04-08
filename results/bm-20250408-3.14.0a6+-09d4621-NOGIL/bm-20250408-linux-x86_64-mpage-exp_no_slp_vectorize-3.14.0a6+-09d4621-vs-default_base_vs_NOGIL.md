# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 09d4621
- commit date: 2025-04-08
- overall geometric mean: 1.097x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 441 ms                                                                 | 511 ms: 1.16x slower                                                  |
| docutils       | 3.66 sec                                                               | 4.09 sec: 1.12x slower                                                |
| sphinx         | 1.41 sec                                                               | 1.62 sec: 1.15x slower                                                |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 883 ms                                                                 | 703 ms: 1.26x faster                                                  |
| async_tree_none_tg         | 360 ms                                                                 | 316 ms: 1.14x faster                                                  |
| async_tree_io              | 870 ms                                                                 | 793 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 673 ms                                                                 | 617 ms: 1.09x faster                                                  |
| async_tree_memoization_tg  | 474 ms                                                                 | 451 ms: 1.05x faster                                                  |
| asyncio_websockets         | 722 ms                                                                 | 754 ms: 1.04x slower                                                  |
| async_tree_memoization     | 457 ms                                                                 | 495 ms: 1.08x slower                                                  |
| async_generators           | 515 ms                                                                 | 559 ms: 1.09x slower                                                  |
| coroutines                 | 32.0 ms                                                                | 36.6 ms: 1.15x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 247 ms                                                                 | 231 ms: 1.07x faster                                                  |
| nbody          | 115 ms                                                                 | 150 ms: 1.30x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.53 ms                                                                | 4.24 ms: 1.07x faster                                                 |
| regex_v8       | 30.1 ms                                                                | 31.8 ms: 1.06x slower                                                 |
| regex_compile  | 157 ms                                                                 | 192 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 16.1 ms                                                                | 17.0 ms: 1.06x slower                                                 |
| xml_etree_parse      | 202 ms                                                                 | 216 ms: 1.07x slower                                                  |
| unpickle_pure_python | 289 us                                                                 | 312 us: 1.08x slower                                                  |
| json_loads           | 38.2 us                                                                | 41.7 us: 1.09x slower                                                 |
| xml_etree_process    | 81.8 ms                                                                | 91.5 ms: 1.12x slower                                                 |
| xml_etree_generate   | 111 ms                                                                 | 129 ms: 1.16x slower                                                  |
| pickle_pure_python   | 419 us                                                                 | 497 us: 1.19x slower                                                  |
| tomli_loads          | 2.41 sec                                                               | 2.88 sec: 1.19x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 27.6 ms                                                                | 29.8 ms: 1.08x slower                                                 |
| python_startup_no_site | 17.4 ms                                                                | 21.8 ms: 1.25x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 45.3 ms                                                                | 53.0 ms: 1.17x slower                                                 |
| genshi_xml      | 64.6 ms                                                                | 79.3 ms: 1.23x slower                                                 |
| genshi_text     | 29.0 ms                                                                | 37.0 ms: 1.28x slower                                                 |
| mako            | 16.6 ms                                                                | 21.4 ms: 1.29x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.24x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250408-linux-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6+-e2b35ee | bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 7.09 ms                                                                | 4.14 ms: 1.71x faster                                                 |
| create_gc_cycles           | 3.52 ms                                                                | 2.50 ms: 1.41x faster                                                 |
| async_tree_io_tg           | 883 ms                                                                 | 703 ms: 1.26x faster                                                  |
| async_tree_none_tg         | 360 ms                                                                 | 316 ms: 1.14x faster                                                  |
| async_tree_io              | 870 ms                                                                 | 793 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 673 ms                                                                 | 617 ms: 1.09x faster                                                  |
| pidigits                   | 247 ms                                                                 | 231 ms: 1.07x faster                                                  |
| regex_effbot               | 4.53 ms                                                                | 4.24 ms: 1.07x faster                                                 |
| async_tree_memoization_tg  | 474 ms                                                                 | 451 ms: 1.05x faster                                                  |
| asyncio_websockets         | 722 ms                                                                 | 754 ms: 1.04x slower                                                  |
| regex_v8                   | 30.1 ms                                                                | 31.8 ms: 1.06x slower                                                 |
| k_core                     | 4.11 sec                                                               | 4.35 sec: 1.06x slower                                                |
| json_dumps                 | 16.1 ms                                                                | 17.0 ms: 1.06x slower                                                 |
| xml_etree_parse            | 202 ms                                                                 | 216 ms: 1.07x slower                                                  |
| pathlib                    | 29.1 ms                                                                | 31.1 ms: 1.07x slower                                                 |
| richards_super             | 70.5 ms                                                                | 76.1 ms: 1.08x slower                                                 |
| python_startup             | 27.6 ms                                                                | 29.8 ms: 1.08x slower                                                 |
| deltablue                  | 4.54 ms                                                                | 4.91 ms: 1.08x slower                                                 |
| unpickle_pure_python       | 289 us                                                                 | 312 us: 1.08x slower                                                  |
| async_tree_memoization     | 457 ms                                                                 | 495 ms: 1.08x slower                                                  |
| logging_silent             | 127 ns                                                                 | 138 ns: 1.09x slower                                                  |
| async_generators           | 515 ms                                                                 | 559 ms: 1.09x slower                                                  |
| generators                 | 42.9 ms                                                                | 46.6 ms: 1.09x slower                                                 |
| scimark_fft                | 449 ms                                                                 | 488 ms: 1.09x slower                                                  |
| bench_thread_pool          | 3.22 ms                                                                | 3.51 ms: 1.09x slower                                                 |
| json_loads                 | 38.2 us                                                                | 41.7 us: 1.09x slower                                                 |
| sympy_integrate            | 28.1 ms                                                                | 30.8 ms: 1.09x slower                                                 |
| comprehensions             | 22.8 us                                                                | 25.3 us: 1.11x slower                                                 |
| pylint                     | 388 ms                                                                 | 433 ms: 1.12x slower                                                  |
| docutils                   | 3.66 sec                                                               | 4.09 sec: 1.12x slower                                                |
| nqueens                    | 102 ms                                                                 | 114 ms: 1.12x slower                                                  |
| sqlglot_v2_parse           | 1.75 ms                                                                | 1.96 ms: 1.12x slower                                                 |
| xml_etree_process          | 81.8 ms                                                                | 91.5 ms: 1.12x slower                                                 |
| sympy_expand               | 607 ms                                                                 | 680 ms: 1.12x slower                                                  |
| sqlglot_v2_normalize       | 129 ms                                                                 | 146 ms: 1.13x slower                                                  |
| pprint_safe_repr           | 901 ms                                                                 | 1.03 sec: 1.14x slower                                                |
| spectral_norm              | 128 ms                                                                 | 147 ms: 1.14x slower                                                  |
| coroutines                 | 32.0 ms                                                                | 36.6 ms: 1.15x slower                                                 |
| scimark_sor                | 147 ms                                                                 | 168 ms: 1.15x slower                                                  |
| sqlalchemy_declarative     | 184 ms                                                                 | 211 ms: 1.15x slower                                                  |
| sphinx                     | 1.41 sec                                                               | 1.62 sec: 1.15x slower                                                |
| crypto_pyaes               | 97.7 ms                                                                | 113 ms: 1.15x slower                                                  |
| sqlglot_v2_optimize        | 71.5 ms                                                                | 82.8 ms: 1.16x slower                                                 |
| fannkuch                   | 521 ms                                                                 | 604 ms: 1.16x slower                                                  |
| xml_etree_generate         | 111 ms                                                                 | 129 ms: 1.16x slower                                                  |
| 2to3                       | 441 ms                                                                 | 511 ms: 1.16x slower                                                  |
| sympy_str                  | 366 ms                                                                 | 426 ms: 1.17x slower                                                  |
| subparsers                 | 31.2 ms                                                                | 36.4 ms: 1.17x slower                                                 |
| shortest_path              | 872 ms                                                                 | 1.02 sec: 1.17x slower                                                |
| django_template            | 45.3 ms                                                                | 53.0 ms: 1.17x slower                                                 |
| deepcopy_reduce            | 3.29 us                                                                | 3.86 us: 1.17x slower                                                 |
| scimark_sparse_mat_mult    | 6.19 ms                                                                | 7.27 ms: 1.17x slower                                                 |
| connected_components       | 796 ms                                                                 | 935 ms: 1.17x slower                                                  |
| pickle_pure_python         | 419 us                                                                 | 497 us: 1.19x slower                                                  |
| bpe_tokeniser              | 5.81 sec                                                               | 6.90 sec: 1.19x slower                                                |
| pyflate                    | 597 ms                                                                 | 711 ms: 1.19x slower                                                  |
| deepcopy_memo              | 38.5 us                                                                | 45.8 us: 1.19x slower                                                 |
| tomli_loads                | 2.41 sec                                                               | 2.88 sec: 1.19x slower                                                |
| pprint_pformat             | 1.78 sec                                                               | 2.15 sec: 1.21x slower                                                |
| logging_format             | 8.78 us                                                                | 10.7 us: 1.22x slower                                                 |
| sympy_sum                  | 204 ms                                                                 | 249 ms: 1.22x slower                                                  |
| scimark_lu                 | 150 ms                                                                 | 183 ms: 1.22x slower                                                  |
| regex_compile              | 157 ms                                                                 | 192 ms: 1.22x slower                                                  |
| genshi_xml                 | 64.6 ms                                                                | 79.3 ms: 1.23x slower                                                 |
| hexiom                     | 8.62 ms                                                                | 10.6 ms: 1.23x slower                                                 |
| telco                      | 9.79 ms                                                                | 12.1 ms: 1.23x slower                                                 |
| raytrace                   | 322 ms                                                                 | 398 ms: 1.24x slower                                                  |
| logging_simple             | 7.45 us                                                                | 9.27 us: 1.24x slower                                                 |
| many_optionals             | 1.25 ms                                                                | 1.56 ms: 1.24x slower                                                 |
| go                         | 143 ms                                                                 | 179 ms: 1.25x slower                                                  |
| mdp                        | 1.88 sec                                                               | 2.35 sec: 1.25x slower                                                |
| chaos                      | 69.6 ms                                                                | 87.0 ms: 1.25x slower                                                 |
| python_startup_no_site     | 17.4 ms                                                                | 21.8 ms: 1.25x slower                                                 |
| meteor_contest             | 143 ms                                                                 | 181 ms: 1.26x slower                                                  |
| genshi_text                | 29.0 ms                                                                | 37.0 ms: 1.28x slower                                                 |
| mako                       | 16.6 ms                                                                | 21.4 ms: 1.29x slower                                                 |
| richards                   | 54.4 ms                                                                | 70.2 ms: 1.29x slower                                                 |
| scimark_monte_carlo        | 81.9 ms                                                                | 106 ms: 1.30x slower                                                  |
| nbody                      | 115 ms                                                                 | 150 ms: 1.30x slower                                                  |
| deepcopy                   | 308 us                                                                 | 405 us: 1.31x slower                                                  |
| sqlglot_v2_transpile       | 2.06 ms                                                                | 2.76 ms: 1.34x slower                                                 |
| coverage                   | 115 ms                                                                 | 158 ms: 1.37x slower                                                  |
| sqlalchemy_imperative      | 21.2 ms                                                                | 29.3 ms: 1.38x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.11x slower                                                          |

Benchmark hidden because not significant (11): bench_mp_pool, xml_etree_iterparse, async_tree_cpu_io_mixed, async_tree_none, sqlite_synth, regex_dna, pycparser, float, json, dulwich_log, typing_runtime_protocols
Ignored benchmarks (1) of results/bm-20250408-3.14.0a6+-09d4621-NOGIL/bm-20250408-linux-x86_64-mpage-exp_no_slp_vectorize-3.14.0a6+-09d4621.json: html5lib

- Geometric mean (including insignificant results): 1.097x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x