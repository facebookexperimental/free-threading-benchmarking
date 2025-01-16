# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 3cedaed
- commit date: 2025-01-15
- overall geometric mean: 1.127x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 304 ms: 1.20x slower                                                  |
| docutils       | 2.58 sec                                                               | 2.82 sec: 1.09x slower                                                |
| sphinx         | 989 ms                                                                 | 1.12 sec: 1.13x slower                                                |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 500 ms: 1.10x faster                                                  |
| async_tree_none_tg         | 256 ms                                                                 | 239 ms: 1.07x faster                                                  |
| async_tree_io_tg           | 612 ms                                                                 | 576 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed    | 569 ms                                                                 | 539 ms: 1.06x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 517 ms: 1.01x faster                                                  |
| async_tree_memoization_tg  | 303 ms                                                                 | 309 ms: 1.02x slower                                                  |
| async_tree_none            | 268 ms                                                                 | 285 ms: 1.06x slower                                                  |
| async_tree_memoization     | 325 ms                                                                 | 348 ms: 1.07x slower                                                  |
| coroutines                 | 21.9 ms                                                                | 23.8 ms: 1.09x slower                                                 |
| async_generators           | 322 ms                                                                 | 369 ms: 1.15x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 229 ms                                                                 | 193 ms: 1.18x faster                                                  |
| float          | 74.9 ms                                                                | 77.2 ms: 1.03x slower                                                 |
| nbody          | 96.1 ms                                                                | 132 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.80 ms                                                                | 2.92 ms: 1.04x slower                                                 |
| regex_v8       | 22.8 ms                                                                | 24.4 ms: 1.07x slower                                                 |
| regex_dna      | 172 ms                                                                 | 185 ms: 1.08x slower                                                  |
| regex_compile  | 127 ms                                                                 | 149 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.5 ms                                                                | 86.1 ms: 1.06x faster                                                 |
| xml_etree_parse      | 128 ms                                                                 | 127 ms: 1.01x faster                                                  |
| json_loads           | 27.8 us                                                                | 30.8 us: 1.11x slower                                                 |
| json_dumps           | 11.7 ms                                                                | 13.0 ms: 1.11x slower                                                 |
| unpickle_pure_python | 214 us                                                                 | 243 us: 1.14x slower                                                  |
| xml_etree_generate   | 83.7 ms                                                                | 96.7 ms: 1.15x slower                                                 |
| xml_etree_process    | 59.0 ms                                                                | 68.8 ms: 1.17x slower                                                 |
| pickle_pure_python   | 314 us                                                                 | 370 us: 1.18x slower                                                  |
| tomli_loads          | 1.92 sec                                                               | 2.31 sec: 1.20x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.2 ms: 1.04x slower                                                 |
| python_startup_no_site | 7.46 ms                                                                | 9.55 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.15x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.1 ms                                                                | 59.9 ms: 1.25x slower                                                 |
| django_template | 34.8 ms                                                                | 43.6 ms: 1.25x slower                                                 |
| mako            | 11.7 ms                                                                | 15.5 ms: 1.32x slower                                                 |
| genshi_text     | 20.8 ms                                                                | 28.0 ms: 1.34x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4+-d05140f | bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| create_gc_cycles           | 1.82 ms                                                                | 1.33 ms: 1.37x faster                                                 |
| gc_traversal               | 4.29 ms                                                                | 3.30 ms: 1.30x faster                                                 |
| pidigits                   | 229 ms                                                                 | 193 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 500 ms: 1.10x faster                                                  |
| sqlite_synth               | 2.22 us                                                                | 2.03 us: 1.09x faster                                                 |
| async_tree_none_tg         | 256 ms                                                                 | 239 ms: 1.07x faster                                                  |
| async_tree_io_tg           | 612 ms                                                                 | 576 ms: 1.06x faster                                                  |
| xml_etree_iterparse        | 91.5 ms                                                                | 86.1 ms: 1.06x faster                                                 |
| async_tree_cpu_io_mixed    | 569 ms                                                                 | 539 ms: 1.06x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 517 ms: 1.01x faster                                                  |
| xml_etree_parse            | 128 ms                                                                 | 127 ms: 1.01x faster                                                  |
| async_tree_memoization_tg  | 303 ms                                                                 | 309 ms: 1.02x slower                                                  |
| pathlib                    | 18.2 ms                                                                | 18.8 ms: 1.03x slower                                                 |
| float                      | 74.9 ms                                                                | 77.2 ms: 1.03x slower                                                 |
| python_startup             | 14.7 ms                                                                | 15.2 ms: 1.04x slower                                                 |
| regex_effbot               | 2.80 ms                                                                | 2.92 ms: 1.04x slower                                                 |
| logging_silent             | 105 ns                                                                 | 110 ns: 1.06x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                                |
| bench_mp_pool              | 88.8 ms                                                                | 94.3 ms: 1.06x slower                                                 |
| async_tree_none            | 268 ms                                                                 | 285 ms: 1.06x slower                                                  |
| async_tree_memoization     | 325 ms                                                                 | 348 ms: 1.07x slower                                                  |
| regex_v8                   | 22.8 ms                                                                | 24.4 ms: 1.07x slower                                                 |
| json                       | 4.98 ms                                                                | 5.35 ms: 1.07x slower                                                 |
| regex_dna                  | 172 ms                                                                 | 185 ms: 1.08x slower                                                  |
| dulwich_log                | 75.5 ms                                                                | 82.1 ms: 1.09x slower                                                 |
| coroutines                 | 21.9 ms                                                                | 23.8 ms: 1.09x slower                                                 |
| docutils                   | 2.58 sec                                                               | 2.82 sec: 1.09x slower                                                |
| bpe_tokeniser              | 4.25 sec                                                               | 4.68 sec: 1.10x slower                                                |
| generators                 | 28.1 ms                                                                | 31.0 ms: 1.11x slower                                                 |
| json_loads                 | 27.8 us                                                                | 30.8 us: 1.11x slower                                                 |
| json_dumps                 | 11.7 ms                                                                | 13.0 ms: 1.11x slower                                                 |
| mdp                        | 2.32 sec                                                               | 2.60 sec: 1.12x slower                                                |
| k_core                     | 2.06 sec                                                               | 2.32 sec: 1.13x slower                                                |
| pylint                     | 281 ms                                                                 | 318 ms: 1.13x slower                                                  |
| scimark_sor                | 116 ms                                                                 | 131 ms: 1.13x slower                                                  |
| sphinx                     | 989 ms                                                                 | 1.12 sec: 1.13x slower                                                |
| unpickle_pure_python       | 214 us                                                                 | 243 us: 1.14x slower                                                  |
| go                         | 119 ms                                                                 | 136 ms: 1.14x slower                                                  |
| async_generators           | 322 ms                                                                 | 369 ms: 1.15x slower                                                  |
| pyflate                    | 420 ms                                                                 | 483 ms: 1.15x slower                                                  |
| many_optionals             | 1.03 ms                                                                | 1.18 ms: 1.15x slower                                                 |
| xml_etree_generate         | 83.7 ms                                                                | 96.7 ms: 1.15x slower                                                 |
| xml_etree_process          | 59.0 ms                                                                | 68.8 ms: 1.17x slower                                                 |
| sqlglot_normalize          | 104 ms                                                                 | 121 ms: 1.17x slower                                                  |
| spectral_norm              | 97.6 ms                                                                | 114 ms: 1.17x slower                                                  |
| subparsers                 | 21.8 ms                                                                | 25.6 ms: 1.17x slower                                                 |
| sqlglot_optimize           | 52.6 ms                                                                | 61.8 ms: 1.18x slower                                                 |
| telco                      | 7.25 ms                                                                | 8.53 ms: 1.18x slower                                                 |
| regex_compile              | 127 ms                                                                 | 149 ms: 1.18x slower                                                  |
| pickle_pure_python         | 314 us                                                                 | 370 us: 1.18x slower                                                  |
| tomli_loads                | 1.92 sec                                                               | 2.31 sec: 1.20x slower                                                |
| 2to3                       | 253 ms                                                                 | 304 ms: 1.20x slower                                                  |
| sqlglot_transpile          | 1.58 ms                                                                | 1.90 ms: 1.20x slower                                                 |
| pprint_safe_repr           | 689 ms                                                                 | 829 ms: 1.20x slower                                                  |
| chaos                      | 58.6 ms                                                                | 70.6 ms: 1.20x slower                                                 |
| raytrace                   | 268 ms                                                                 | 323 ms: 1.21x slower                                                  |
| scimark_lu                 | 113 ms                                                                 | 136 ms: 1.21x slower                                                  |
| sympy_expand               | 452 ms                                                                 | 548 ms: 1.21x slower                                                  |
| scimark_fft                | 314 ms                                                                 | 381 ms: 1.21x slower                                                  |
| coverage                   | 80.0 ms                                                                | 96.9 ms: 1.21x slower                                                 |
| pprint_pformat             | 1.40 sec                                                               | 1.70 sec: 1.22x slower                                                |
| sympy_integrate            | 19.7 ms                                                                | 24.2 ms: 1.23x slower                                                 |
| sqlglot_parse              | 1.28 ms                                                                | 1.57 ms: 1.23x slower                                                 |
| sympy_sum                  | 152 ms                                                                 | 187 ms: 1.23x slower                                                  |
| thrift                     | 747 us                                                                 | 920 us: 1.23x slower                                                  |
| deepcopy                   | 255 us                                                                 | 314 us: 1.23x slower                                                  |
| comprehensions             | 16.9 us                                                                | 20.9 us: 1.24x slower                                                 |
| sympy_str                  | 271 ms                                                                 | 336 ms: 1.24x slower                                                  |
| connected_components       | 390 ms                                                                 | 484 ms: 1.24x slower                                                  |
| logging_simple             | 5.95 us                                                                | 7.40 us: 1.24x slower                                                 |
| shortest_path              | 433 ms                                                                 | 538 ms: 1.24x slower                                                  |
| genshi_xml                 | 48.1 ms                                                                | 59.9 ms: 1.25x slower                                                 |
| logging_format             | 6.75 us                                                                | 8.43 us: 1.25x slower                                                 |
| django_template            | 34.8 ms                                                                | 43.6 ms: 1.25x slower                                                 |
| nqueens                    | 77.2 ms                                                                | 96.8 ms: 1.25x slower                                                 |
| sqlalchemy_declarative     | 130 ms                                                                 | 163 ms: 1.26x slower                                                  |
| sqlalchemy_imperative      | 19.2 ms                                                                | 24.2 ms: 1.26x slower                                                 |
| hexiom                     | 5.77 ms                                                                | 7.26 ms: 1.26x slower                                                 |
| richards                   | 43.5 ms                                                                | 55.3 ms: 1.27x slower                                                 |
| python_startup_no_site     | 7.46 ms                                                                | 9.55 ms: 1.28x slower                                                 |
| deepcopy_memo              | 30.0 us                                                                | 38.4 us: 1.28x slower                                                 |
| scimark_monte_carlo        | 64.0 ms                                                                | 82.2 ms: 1.28x slower                                                 |
| deepcopy_reduce            | 2.55 us                                                                | 3.27 us: 1.28x slower                                                 |
| richards_super             | 49.6 ms                                                                | 64.2 ms: 1.29x slower                                                 |
| fannkuch                   | 366 ms                                                                 | 475 ms: 1.30x slower                                                  |
| meteor_contest             | 99.5 ms                                                                | 129 ms: 1.30x slower                                                  |
| crypto_pyaes               | 66.5 ms                                                                | 86.9 ms: 1.31x slower                                                 |
| typing_runtime_protocols   | 154 us                                                                 | 202 us: 1.31x slower                                                  |
| mako                       | 11.7 ms                                                                | 15.5 ms: 1.32x slower                                                 |
| genshi_text                | 20.8 ms                                                                | 28.0 ms: 1.34x slower                                                 |
| nbody                      | 96.1 ms                                                                | 132 ms: 1.38x slower                                                  |
| scimark_sparse_mat_mult    | 4.18 ms                                                                | 5.84 ms: 1.40x slower                                                 |
| deltablue                  | 3.21 ms                                                                | 4.57 ms: 1.42x slower                                                 |
| bench_thread_pool          | 1.04 ms                                                                | 3.31 ms: 3.19x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.16x slower                                                          |

Benchmark hidden because not significant (1): async_tree_io
Ignored benchmarks (1) of results/bm-20250115-3.14.0a4+-3cedaed-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-3cedaed.json: html5lib

- Geometric mean (including insignificant results): 1.127x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x