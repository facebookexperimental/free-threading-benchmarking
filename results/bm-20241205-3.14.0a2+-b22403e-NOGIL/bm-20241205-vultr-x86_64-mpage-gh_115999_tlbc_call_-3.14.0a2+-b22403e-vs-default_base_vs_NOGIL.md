# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: b22403e
- commit date: 2024-12-05
- overall geometric mean: 1.260x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                 | 366 ms: 1.42x slower                                                  |
| docutils       | 2.57 sec                                                               | 3.08 sec: 1.20x slower                                                |
| sphinx         | 994 ms                                                                 | 1.18 sec: 1.19x slower                                                |
| Geometric mean | (ref)                                                                  | 1.27x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 587 ms                                                                 | 611 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed    | 607 ms                                                                 | 632 ms: 1.04x slower                                                  |
| coroutines                 | 21.9 ms                                                                | 24.3 ms: 1.11x slower                                                 |
| async_generators           | 370 ms                                                                 | 451 ms: 1.22x slower                                                  |
| async_tree_io_tg           | 624 ms                                                                 | 817 ms: 1.31x slower                                                  |
| async_tree_none_tg         | 262 ms                                                                 | 352 ms: 1.34x slower                                                  |
| async_tree_io              | 626 ms                                                                 | 842 ms: 1.35x slower                                                  |
| async_tree_memoization     | 339 ms                                                                 | 468 ms: 1.38x slower                                                  |
| async_tree_none            | 276 ms                                                                 | 383 ms: 1.39x slower                                                  |
| async_tree_memoization_tg  | 314 ms                                                                 | 444 ms: 1.42x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.23x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 222 ms                                                                 | 181 ms: 1.23x faster                                                  |
| nbody          | 95.2 ms                                                                | 131 ms: 1.37x slower                                                  |
| float          | 78.6 ms                                                                | 139 ms: 1.77x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.74 ms                                                                | 2.84 ms: 1.04x slower                                                 |
| regex_dna      | 169 ms                                                                 | 181 ms: 1.07x slower                                                  |
| regex_v8       | 23.3 ms                                                                | 25.0 ms: 1.07x slower                                                 |
| regex_compile  | 130 ms                                                                 | 181 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.1 ms                                                                | 91.3 ms: 1.01x faster                                                 |
| xml_etree_parse      | 130 ms                                                                 | 131 ms: 1.01x slower                                                  |
| json_loads           | 25.1 us                                                                | 28.5 us: 1.13x slower                                                 |
| xml_etree_generate   | 85.1 ms                                                                | 97.9 ms: 1.15x slower                                                 |
| json_dumps           | 11.5 ms                                                                | 14.4 ms: 1.25x slower                                                 |
| tomli_loads          | 2.11 sec                                                               | 2.67 sec: 1.27x slower                                                |
| xml_etree_process    | 59.6 ms                                                                | 78.0 ms: 1.31x slower                                                 |
| unpickle_pure_python | 216 us                                                                 | 331 us: 1.53x slower                                                  |
| pickle_pure_python   | 316 us                                                                 | 504 us: 1.59x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.23x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                 |
| python_startup_no_site | 7.43 ms                                                                | 10.3 ms: 1.38x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.29x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 51.2 ms                                                                | 63.4 ms: 1.24x slower                                                 |
| genshi_text     | 22.3 ms                                                                | 31.5 ms: 1.41x slower                                                 |
| django_template | 35.6 ms                                                                | 50.3 ms: 1.41x slower                                                 |
| mako            | 11.5 ms                                                                | 17.7 ms: 1.54x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.40x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.58 ms                                                                | 3.51 ms: 1.31x faster                                                 |
| pidigits                   | 222 ms                                                                 | 181 ms: 1.23x faster                                                  |
| xml_etree_iterparse        | 92.1 ms                                                                | 91.3 ms: 1.01x faster                                                 |
| xml_etree_parse            | 130 ms                                                                 | 131 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.28 us                                                                | 2.29 us: 1.01x slower                                                 |
| regex_effbot               | 2.74 ms                                                                | 2.84 ms: 1.04x slower                                                 |
| async_tree_cpu_io_mixed_tg | 587 ms                                                                 | 611 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed    | 607 ms                                                                 | 632 ms: 1.04x slower                                                  |
| regex_dna                  | 169 ms                                                                 | 181 ms: 1.07x slower                                                  |
| regex_v8                   | 23.3 ms                                                                | 25.0 ms: 1.07x slower                                                 |
| coroutines                 | 21.9 ms                                                                | 24.3 ms: 1.11x slower                                                 |
| json                       | 4.53 ms                                                                | 5.12 ms: 1.13x slower                                                 |
| pathlib                    | 18.2 ms                                                                | 20.5 ms: 1.13x slower                                                 |
| spectral_norm              | 107 ms                                                                 | 122 ms: 1.13x slower                                                  |
| json_loads                 | 25.1 us                                                                | 28.5 us: 1.13x slower                                                 |
| bpe_tokeniser              | 4.32 sec                                                               | 4.97 sec: 1.15x slower                                                |
| xml_etree_generate         | 85.1 ms                                                                | 97.9 ms: 1.15x slower                                                 |
| k_core                     | 2.08 sec                                                               | 2.42 sec: 1.16x slower                                                |
| mdp                        | 2.35 sec                                                               | 2.77 sec: 1.18x slower                                                |
| sphinx                     | 994 ms                                                                 | 1.18 sec: 1.19x slower                                                |
| scimark_fft                | 340 ms                                                                 | 405 ms: 1.19x slower                                                  |
| docutils                   | 2.57 sec                                                               | 3.08 sec: 1.20x slower                                                |
| python_startup             | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                 |
| telco                      | 7.19 ms                                                                | 8.64 ms: 1.20x slower                                                 |
| nqueens                    | 79.5 ms                                                                | 96.7 ms: 1.22x slower                                                 |
| async_generators           | 370 ms                                                                 | 451 ms: 1.22x slower                                                  |
| bench_mp_pool              | 88.5 ms                                                                | 109 ms: 1.23x slower                                                  |
| shortest_path              | 444 ms                                                                 | 548 ms: 1.23x slower                                                  |
| genshi_xml                 | 51.2 ms                                                                | 63.4 ms: 1.24x slower                                                 |
| connected_components       | 400 ms                                                                 | 498 ms: 1.24x slower                                                  |
| json_dumps                 | 11.5 ms                                                                | 14.4 ms: 1.25x slower                                                 |
| deepcopy                   | 262 us                                                                 | 327 us: 1.25x slower                                                  |
| many_optionals             | 1.03 ms                                                                | 1.29 ms: 1.25x slower                                                 |
| dulwich_log                | 76.1 ms                                                                | 95.4 ms: 1.25x slower                                                 |
| typing_runtime_protocols   | 161 us                                                                 | 202 us: 1.26x slower                                                  |
| coverage                   | 79.8 ms                                                                | 101 ms: 1.26x slower                                                  |
| tomli_loads                | 2.11 sec                                                               | 2.67 sec: 1.27x slower                                                |
| sqlglot_normalize          | 107 ms                                                                 | 136 ms: 1.27x slower                                                  |
| sqlglot_optimize           | 53.6 ms                                                                | 68.8 ms: 1.28x slower                                                 |
| scimark_sparse_mat_mult    | 4.57 ms                                                                | 5.96 ms: 1.30x slower                                                 |
| generators                 | 29.0 ms                                                                | 37.9 ms: 1.31x slower                                                 |
| async_tree_io_tg           | 624 ms                                                                 | 817 ms: 1.31x slower                                                  |
| xml_etree_process          | 59.6 ms                                                                | 78.0 ms: 1.31x slower                                                 |
| meteor_contest             | 99.1 ms                                                                | 130 ms: 1.31x slower                                                  |
| deepcopy_memo              | 30.7 us                                                                | 40.5 us: 1.32x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 497 ms: 1.32x slower                                                  |
| crypto_pyaes               | 68.1 ms                                                                | 90.7 ms: 1.33x slower                                                 |
| pylint                     | 285 ms                                                                 | 380 ms: 1.33x slower                                                  |
| async_tree_none_tg         | 262 ms                                                                 | 352 ms: 1.34x slower                                                  |
| async_tree_io              | 626 ms                                                                 | 842 ms: 1.35x slower                                                  |
| pycparser                  | 1.13 sec                                                               | 1.53 sec: 1.35x slower                                                |
| pprint_safe_repr           | 715 ms                                                                 | 971 ms: 1.36x slower                                                  |
| deepcopy_reduce            | 2.60 us                                                                | 3.54 us: 1.36x slower                                                 |
| nbody                      | 95.2 ms                                                                | 131 ms: 1.37x slower                                                  |
| pprint_pformat             | 1.45 sec                                                               | 2.01 sec: 1.38x slower                                                |
| async_tree_memoization     | 339 ms                                                                 | 468 ms: 1.38x slower                                                  |
| python_startup_no_site     | 7.43 ms                                                                | 10.3 ms: 1.38x slower                                                 |
| async_tree_none            | 276 ms                                                                 | 383 ms: 1.39x slower                                                  |
| regex_compile              | 130 ms                                                                 | 181 ms: 1.39x slower                                                  |
| genshi_text                | 22.3 ms                                                                | 31.5 ms: 1.41x slower                                                 |
| django_template            | 35.6 ms                                                                | 50.3 ms: 1.41x slower                                                 |
| async_tree_memoization_tg  | 314 ms                                                                 | 444 ms: 1.42x slower                                                  |
| 2to3                       | 257 ms                                                                 | 366 ms: 1.42x slower                                                  |
| subparsers                 | 22.1 ms                                                                | 31.8 ms: 1.44x slower                                                 |
| sympy_integrate            | 20.1 ms                                                                | 29.4 ms: 1.47x slower                                                 |
| sqlalchemy_imperative      | 19.4 ms                                                                | 29.4 ms: 1.52x slower                                                 |
| unpickle_pure_python       | 216 us                                                                 | 331 us: 1.53x slower                                                  |
| mako                       | 11.5 ms                                                                | 17.7 ms: 1.54x slower                                                 |
| pyflate                    | 448 ms                                                                 | 695 ms: 1.55x slower                                                  |
| comprehensions             | 17.3 us                                                                | 26.9 us: 1.55x slower                                                 |
| thrift                     | 736 us                                                                 | 1.16 ms: 1.58x slower                                                 |
| pickle_pure_python         | 316 us                                                                 | 504 us: 1.59x slower                                                  |
| sqlalchemy_declarative     | 127 ms                                                                 | 203 ms: 1.61x slower                                                  |
| richards_super             | 52.7 ms                                                                | 85.9 ms: 1.63x slower                                                 |
| hexiom                     | 5.99 ms                                                                | 9.83 ms: 1.64x slower                                                 |
| richards                   | 46.7 ms                                                                | 76.6 ms: 1.64x slower                                                 |
| logging_format             | 7.04 us                                                                | 11.7 us: 1.67x slower                                                 |
| logging_simple             | 6.27 us                                                                | 10.5 us: 1.67x slower                                                 |
| scimark_lu                 | 109 ms                                                                 | 184 ms: 1.68x slower                                                  |
| sympy_str                  | 277 ms                                                                 | 475 ms: 1.71x slower                                                  |
| logging_silent             | 105 ns                                                                 | 181 ns: 1.72x slower                                                  |
| chaos                      | 60.1 ms                                                                | 104 ms: 1.73x slower                                                  |
| scimark_sor                | 133 ms                                                                 | 234 ms: 1.76x slower                                                  |
| float                      | 78.6 ms                                                                | 139 ms: 1.77x slower                                                  |
| scimark_monte_carlo        | 65.6 ms                                                                | 119 ms: 1.81x slower                                                  |
| sqlglot_transpile          | 1.61 ms                                                                | 2.99 ms: 1.86x slower                                                 |
| sqlglot_parse              | 1.30 ms                                                                | 2.58 ms: 1.98x slower                                                 |
| sympy_expand               | 460 ms                                                                 | 949 ms: 2.06x slower                                                  |
| raytrace                   | 265 ms                                                                 | 549 ms: 2.07x slower                                                  |
| go                         | 120 ms                                                                 | 264 ms: 2.20x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 348 ms: 2.26x slower                                                  |
| deltablue                  | 3.25 ms                                                                | 7.86 ms: 2.42x slower                                                 |
| bench_thread_pool          | 1.02 ms                                                                | 3.36 ms: 3.30x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.37x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, create_gc_cycles
Ignored benchmarks (1) of results/bm-20241205-3.14.0a2+-b22403e-NOGIL/bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e.json: html5lib

- Geometric mean (including insignificant results): 1.260x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.19x