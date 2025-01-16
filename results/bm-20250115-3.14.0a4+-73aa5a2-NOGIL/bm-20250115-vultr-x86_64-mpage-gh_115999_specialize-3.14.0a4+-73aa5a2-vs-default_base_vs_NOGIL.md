# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 73aa5a2
- commit date: 2025-01-15
- overall geometric mean: 1.131x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 305 ms: 1.20x slower                                                  |
| docutils       | 2.58 sec                                                               | 2.81 sec: 1.09x slower                                                |
| sphinx         | 989 ms                                                                 | 1.12 sec: 1.13x slower                                                |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 491 ms: 1.12x faster                                                  |
| async_tree_none_tg         | 256 ms                                                                 | 238 ms: 1.08x faster                                                  |
| async_tree_cpu_io_mixed    | 569 ms                                                                 | 530 ms: 1.07x faster                                                  |
| async_tree_io_tg           | 612 ms                                                                 | 580 ms: 1.06x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 516 ms: 1.01x faster                                                  |
| async_tree_memoization_tg  | 303 ms                                                                 | 309 ms: 1.02x slower                                                  |
| async_tree_none            | 268 ms                                                                 | 286 ms: 1.07x slower                                                  |
| async_tree_memoization     | 325 ms                                                                 | 350 ms: 1.08x slower                                                  |
| coroutines                 | 21.9 ms                                                                | 23.9 ms: 1.09x slower                                                 |
| async_generators           | 322 ms                                                                 | 373 ms: 1.16x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 229 ms                                                                 | 193 ms: 1.18x faster                                                  |
| float          | 74.9 ms                                                                | 76.9 ms: 1.03x slower                                                 |
| nbody          | 96.1 ms                                                                | 130 ms: 1.35x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.80 ms                                                                | 2.84 ms: 1.01x slower                                                 |
| regex_dna      | 172 ms                                                                 | 182 ms: 1.06x slower                                                  |
| regex_v8       | 22.8 ms                                                                | 24.6 ms: 1.08x slower                                                 |
| regex_compile  | 127 ms                                                                 | 150 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.5 ms                                                                | 86.7 ms: 1.06x faster                                                 |
| json_dumps           | 11.7 ms                                                                | 12.8 ms: 1.09x slower                                                 |
| json_loads           | 27.8 us                                                                | 30.7 us: 1.10x slower                                                 |
| xml_etree_generate   | 83.7 ms                                                                | 97.1 ms: 1.16x slower                                                 |
| unpickle_pure_python | 214 us                                                                 | 250 us: 1.17x slower                                                  |
| xml_etree_process    | 59.0 ms                                                                | 69.6 ms: 1.18x slower                                                 |
| pickle_pure_python   | 314 us                                                                 | 371 us: 1.18x slower                                                  |
| tomli_loads          | 1.92 sec                                                               | 2.32 sec: 1.20x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.2 ms: 1.04x slower                                                 |
| python_startup_no_site | 7.46 ms                                                                | 9.52 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.15x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.1 ms                                                                | 59.8 ms: 1.24x slower                                                 |
| django_template | 34.8 ms                                                                | 43.6 ms: 1.25x slower                                                 |
| mako            | 11.7 ms                                                                | 15.7 ms: 1.34x slower                                                 |
| genshi_text     | 20.8 ms                                                                | 28.3 ms: 1.36x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| create_gc_cycles           | 1.82 ms                                                                | 1.32 ms: 1.38x faster                                                 |
| pidigits                   | 229 ms                                                                 | 193 ms: 1.18x faster                                                  |
| gc_traversal               | 4.29 ms                                                                | 3.68 ms: 1.16x faster                                                 |
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 491 ms: 1.12x faster                                                  |
| sqlite_synth               | 2.22 us                                                                | 2.03 us: 1.10x faster                                                 |
| async_tree_none_tg         | 256 ms                                                                 | 238 ms: 1.08x faster                                                  |
| async_tree_cpu_io_mixed    | 569 ms                                                                 | 530 ms: 1.07x faster                                                  |
| async_tree_io_tg           | 612 ms                                                                 | 580 ms: 1.06x faster                                                  |
| xml_etree_iterparse        | 91.5 ms                                                                | 86.7 ms: 1.06x faster                                                 |
| asyncio_websockets         | 523 ms                                                                 | 516 ms: 1.01x faster                                                  |
| regex_effbot               | 2.80 ms                                                                | 2.84 ms: 1.01x slower                                                 |
| async_tree_memoization_tg  | 303 ms                                                                 | 309 ms: 1.02x slower                                                  |
| float                      | 74.9 ms                                                                | 76.9 ms: 1.03x slower                                                 |
| pathlib                    | 18.2 ms                                                                | 18.8 ms: 1.03x slower                                                 |
| python_startup             | 14.7 ms                                                                | 15.2 ms: 1.04x slower                                                 |
| regex_dna                  | 172 ms                                                                 | 182 ms: 1.06x slower                                                  |
| bench_mp_pool              | 88.8 ms                                                                | 94.2 ms: 1.06x slower                                                 |
| async_tree_none            | 268 ms                                                                 | 286 ms: 1.07x slower                                                  |
| json                       | 4.98 ms                                                                | 5.32 ms: 1.07x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                                |
| async_tree_memoization     | 325 ms                                                                 | 350 ms: 1.08x slower                                                  |
| regex_v8                   | 22.8 ms                                                                | 24.6 ms: 1.08x slower                                                 |
| dulwich_log                | 75.5 ms                                                                | 82.1 ms: 1.09x slower                                                 |
| docutils                   | 2.58 sec                                                               | 2.81 sec: 1.09x slower                                                |
| coroutines                 | 21.9 ms                                                                | 23.9 ms: 1.09x slower                                                 |
| json_dumps                 | 11.7 ms                                                                | 12.8 ms: 1.09x slower                                                 |
| generators                 | 28.1 ms                                                                | 30.9 ms: 1.10x slower                                                 |
| json_loads                 | 27.8 us                                                                | 30.7 us: 1.10x slower                                                 |
| logging_silent             | 105 ns                                                                 | 116 ns: 1.11x slower                                                  |
| bpe_tokeniser              | 4.25 sec                                                               | 4.73 sec: 1.11x slower                                                |
| k_core                     | 2.06 sec                                                               | 2.31 sec: 1.12x slower                                                |
| sphinx                     | 989 ms                                                                 | 1.12 sec: 1.13x slower                                                |
| pylint                     | 281 ms                                                                 | 318 ms: 1.13x slower                                                  |
| scimark_sor                | 116 ms                                                                 | 133 ms: 1.14x slower                                                  |
| go                         | 119 ms                                                                 | 138 ms: 1.16x slower                                                  |
| many_optionals             | 1.03 ms                                                                | 1.19 ms: 1.16x slower                                                 |
| pyflate                    | 420 ms                                                                 | 486 ms: 1.16x slower                                                  |
| xml_etree_generate         | 83.7 ms                                                                | 97.1 ms: 1.16x slower                                                 |
| async_generators           | 322 ms                                                                 | 373 ms: 1.16x slower                                                  |
| telco                      | 7.25 ms                                                                | 8.42 ms: 1.16x slower                                                 |
| mdp                        | 2.32 sec                                                               | 2.70 sec: 1.17x slower                                                |
| unpickle_pure_python       | 214 us                                                                 | 250 us: 1.17x slower                                                  |
| regex_compile              | 127 ms                                                                 | 150 ms: 1.18x slower                                                  |
| xml_etree_process          | 59.0 ms                                                                | 69.6 ms: 1.18x slower                                                 |
| sqlglot_normalize          | 104 ms                                                                 | 122 ms: 1.18x slower                                                  |
| pickle_pure_python         | 314 us                                                                 | 371 us: 1.18x slower                                                  |
| sqlglot_optimize           | 52.6 ms                                                                | 62.2 ms: 1.18x slower                                                 |
| subparsers                 | 21.8 ms                                                                | 25.9 ms: 1.19x slower                                                 |
| pprint_safe_repr           | 689 ms                                                                 | 822 ms: 1.19x slower                                                  |
| spectral_norm              | 97.6 ms                                                                | 117 ms: 1.20x slower                                                  |
| 2to3                       | 253 ms                                                                 | 305 ms: 1.20x slower                                                  |
| tomli_loads                | 1.92 sec                                                               | 2.32 sec: 1.20x slower                                                |
| thrift                     | 747 us                                                                 | 905 us: 1.21x slower                                                  |
| sympy_expand               | 452 ms                                                                 | 548 ms: 1.21x slower                                                  |
| chaos                      | 58.6 ms                                                                | 71.0 ms: 1.21x slower                                                 |
| sqlglot_transpile          | 1.58 ms                                                                | 1.92 ms: 1.21x slower                                                 |
| raytrace                   | 268 ms                                                                 | 325 ms: 1.21x slower                                                  |
| pprint_pformat             | 1.40 sec                                                               | 1.70 sec: 1.22x slower                                                |
| coverage                   | 80.0 ms                                                                | 97.6 ms: 1.22x slower                                                 |
| logging_simple             | 5.95 us                                                                | 7.28 us: 1.22x slower                                                 |
| logging_format             | 6.75 us                                                                | 8.28 us: 1.23x slower                                                 |
| scimark_fft                | 314 ms                                                                 | 387 ms: 1.23x slower                                                  |
| deepcopy                   | 255 us                                                                 | 314 us: 1.23x slower                                                  |
| sympy_sum                  | 152 ms                                                                 | 188 ms: 1.24x slower                                                  |
| sqlglot_parse              | 1.28 ms                                                                | 1.58 ms: 1.24x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 24.4 ms: 1.24x slower                                                 |
| genshi_xml                 | 48.1 ms                                                                | 59.8 ms: 1.24x slower                                                 |
| scimark_lu                 | 113 ms                                                                 | 140 ms: 1.24x slower                                                  |
| shortest_path              | 433 ms                                                                 | 540 ms: 1.25x slower                                                  |
| sympy_str                  | 271 ms                                                                 | 338 ms: 1.25x slower                                                  |
| connected_components       | 390 ms                                                                 | 489 ms: 1.25x slower                                                  |
| django_template            | 34.8 ms                                                                | 43.6 ms: 1.25x slower                                                 |
| comprehensions             | 16.9 us                                                                | 21.2 us: 1.25x slower                                                 |
| sqlalchemy_imperative      | 19.2 ms                                                                | 24.1 ms: 1.25x slower                                                 |
| nqueens                    | 77.2 ms                                                                | 97.3 ms: 1.26x slower                                                 |
| sqlalchemy_declarative     | 130 ms                                                                 | 163 ms: 1.26x slower                                                  |
| python_startup_no_site     | 7.46 ms                                                                | 9.52 ms: 1.28x slower                                                 |
| richards                   | 43.5 ms                                                                | 55.6 ms: 1.28x slower                                                 |
| scimark_monte_carlo        | 64.0 ms                                                                | 82.3 ms: 1.28x slower                                                 |
| deepcopy_memo              | 30.0 us                                                                | 38.7 us: 1.29x slower                                                 |
| deepcopy_reduce            | 2.55 us                                                                | 3.30 us: 1.30x slower                                                 |
| hexiom                     | 5.77 ms                                                                | 7.55 ms: 1.31x slower                                                 |
| fannkuch                   | 366 ms                                                                 | 479 ms: 1.31x slower                                                  |
| typing_runtime_protocols   | 154 us                                                                 | 203 us: 1.32x slower                                                  |
| crypto_pyaes               | 66.5 ms                                                                | 87.6 ms: 1.32x slower                                                 |
| meteor_contest             | 99.5 ms                                                                | 133 ms: 1.33x slower                                                  |
| richards_super             | 49.6 ms                                                                | 66.3 ms: 1.34x slower                                                 |
| mako                       | 11.7 ms                                                                | 15.7 ms: 1.34x slower                                                 |
| nbody                      | 96.1 ms                                                                | 130 ms: 1.35x slower                                                  |
| genshi_text                | 20.8 ms                                                                | 28.3 ms: 1.36x slower                                                 |
| scimark_sparse_mat_mult    | 4.18 ms                                                                | 5.71 ms: 1.37x slower                                                 |
| deltablue                  | 3.21 ms                                                                | 4.66 ms: 1.45x slower                                                 |
| bench_thread_pool          | 1.04 ms                                                                | 3.34 ms: 3.22x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.16x slower                                                          |

Benchmark hidden because not significant (2): async_tree_io, xml_etree_parse
Ignored benchmarks (1) of results/bm-20250115-3.14.0a4+-73aa5a2-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-73aa5a2.json: html5lib

- Geometric mean (including insignificant results): 1.131x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x