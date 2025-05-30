# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: 26bfc21
- commit date: 2024-11-22
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                 | 381 ms: 1.48x slower                                                  |
| docutils       | 2.63 sec                                                               | 3.21 sec: 1.22x slower                                                |
| html5lib       | 67.3 ms                                                                | 99.7 ms: 1.48x slower                                                 |
| sphinx         | 1.03 sec                                                               | 1.24 sec: 1.20x slower                                                |
| Geometric mean | (ref)                                                                  | 1.34x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                  |
| async_tree_io              | 841 ms                                                                 | 912 ms: 1.08x slower                                                  |
| async_tree_none_tg         | 345 ms                                                                 | 377 ms: 1.09x slower                                                  |
| async_tree_cpu_io_mixed_tg | 572 ms                                                                 | 642 ms: 1.12x slower                                                  |
| async_tree_cpu_io_mixed    | 573 ms                                                                 | 667 ms: 1.16x slower                                                  |
| async_tree_memoization_tg  | 391 ms                                                                 | 472 ms: 1.21x slower                                                  |
| async_tree_memoization     | 405 ms                                                                 | 500 ms: 1.23x slower                                                  |
| coroutines                 | 22.2 ms                                                                | 27.5 ms: 1.24x slower                                                 |
| async_tree_none            | 329 ms                                                                 | 412 ms: 1.25x slower                                                  |
| async_generators           | 376 ms                                                                 | 473 ms: 1.26x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.15x slower                                                          |

Benchmark hidden because not significant (1): async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 184 ms: 1.01x faster                                                  |
| nbody          | 93.7 ms                                                                | 158 ms: 1.69x slower                                                  |
| float          | 82.1 ms                                                                | 146 ms: 1.77x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.44x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.85 ms                                                                | 2.80 ms: 1.02x faster                                                 |
| regex_dna      | 177 ms                                                                 | 181 ms: 1.03x slower                                                  |
| regex_v8       | 23.9 ms                                                                | 25.3 ms: 1.06x slower                                                 |
| regex_compile  | 130 ms                                                                 | 196 ms: 1.50x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                                 | 131 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 99.0 ms                                                                | 95.6 ms: 1.04x faster                                                 |
| json_loads           | 25.0 us                                                                | 27.9 us: 1.11x slower                                                 |
| xml_etree_generate   | 87.2 ms                                                                | 103 ms: 1.18x slower                                                  |
| json_dumps           | 11.5 ms                                                                | 14.5 ms: 1.27x slower                                                 |
| xml_etree_process    | 61.3 ms                                                                | 82.6 ms: 1.35x slower                                                 |
| tomli_loads          | 2.11 sec                                                               | 2.88 sec: 1.37x slower                                                |
| pickle_pure_python   | 321 us                                                                 | 545 us: 1.70x slower                                                  |
| unpickle_pure_python | 218 us                                                                 | 371 us: 1.70x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                                | 17.5 ms: 1.33x slower                                                 |
| python_startup_no_site | 7.41 ms                                                                | 10.3 ms: 1.39x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.9 ms                                                                | 68.1 ms: 1.34x slower                                                 |
| genshi_text     | 22.7 ms                                                                | 34.2 ms: 1.50x slower                                                 |
| django_template | 36.2 ms                                                                | 55.5 ms: 1.54x slower                                                 |
| mako            | 11.9 ms                                                                | 19.7 ms: 1.65x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.50x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e | bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-26bfc21 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 3.79 ms                                                                | 3.51 ms: 1.08x faster                                                 |
| xml_etree_parse            | 139 ms                                                                 | 131 ms: 1.06x faster                                                  |
| create_gc_cycles           | 1.93 ms                                                                | 1.85 ms: 1.04x faster                                                 |
| xml_etree_iterparse        | 99.0 ms                                                                | 95.6 ms: 1.04x faster                                                 |
| regex_effbot               | 2.85 ms                                                                | 2.80 ms: 1.02x faster                                                 |
| pidigits                   | 185 ms                                                                 | 184 ms: 1.01x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                  |
| regex_dna                  | 177 ms                                                                 | 181 ms: 1.03x slower                                                  |
| sqlite_synth               | 2.23 us                                                                | 2.31 us: 1.04x slower                                                 |
| regex_v8                   | 23.9 ms                                                                | 25.3 ms: 1.06x slower                                                 |
| async_tree_io              | 841 ms                                                                 | 912 ms: 1.08x slower                                                  |
| async_tree_none_tg         | 345 ms                                                                 | 377 ms: 1.09x slower                                                  |
| json_loads                 | 25.0 us                                                                | 27.9 us: 1.11x slower                                                 |
| json                       | 4.53 ms                                                                | 5.05 ms: 1.11x slower                                                 |
| pathlib                    | 18.6 ms                                                                | 20.7 ms: 1.12x slower                                                 |
| async_tree_cpu_io_mixed_tg | 572 ms                                                                 | 642 ms: 1.12x slower                                                  |
| spectral_norm              | 113 ms                                                                 | 127 ms: 1.13x slower                                                  |
| async_tree_cpu_io_mixed    | 573 ms                                                                 | 667 ms: 1.16x slower                                                  |
| scimark_fft                | 343 ms                                                                 | 401 ms: 1.17x slower                                                  |
| xml_etree_generate         | 87.2 ms                                                                | 103 ms: 1.18x slower                                                  |
| sphinx                     | 1.03 sec                                                               | 1.24 sec: 1.20x slower                                                |
| async_tree_memoization_tg  | 391 ms                                                                 | 472 ms: 1.21x slower                                                  |
| mdp                        | 2.49 sec                                                               | 3.02 sec: 1.21x slower                                                |
| docutils                   | 2.63 sec                                                               | 3.21 sec: 1.22x slower                                                |
| async_tree_memoization     | 405 ms                                                                 | 500 ms: 1.23x slower                                                  |
| coroutines                 | 22.2 ms                                                                | 27.5 ms: 1.24x slower                                                 |
| coverage                   | 80.9 ms                                                                | 101 ms: 1.25x slower                                                  |
| telco                      | 7.31 ms                                                                | 9.12 ms: 1.25x slower                                                 |
| async_tree_none            | 329 ms                                                                 | 412 ms: 1.25x slower                                                  |
| shortest_path              | 444 ms                                                                 | 558 ms: 1.26x slower                                                  |
| async_generators           | 376 ms                                                                 | 473 ms: 1.26x slower                                                  |
| connected_components       | 404 ms                                                                 | 509 ms: 1.26x slower                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 5.64 sec: 1.26x slower                                                |
| json_dumps                 | 11.5 ms                                                                | 14.5 ms: 1.27x slower                                                 |
| scimark_sparse_mat_mult    | 4.53 ms                                                                | 5.80 ms: 1.28x slower                                                 |
| bench_mp_pool              | 86.0 ms                                                                | 110 ms: 1.28x slower                                                  |
| dulwich_log                | 76.1 ms                                                                | 98.7 ms: 1.30x slower                                                 |
| generators                 | 29.4 ms                                                                | 39.0 ms: 1.32x slower                                                 |
| python_startup             | 13.2 ms                                                                | 17.5 ms: 1.33x slower                                                 |
| typing_runtime_protocols   | 158 us                                                                 | 211 us: 1.33x slower                                                  |
| many_optionals             | 1.03 ms                                                                | 1.38 ms: 1.34x slower                                                 |
| genshi_xml                 | 50.9 ms                                                                | 68.1 ms: 1.34x slower                                                 |
| xml_etree_process          | 61.3 ms                                                                | 82.6 ms: 1.35x slower                                                 |
| nqueens                    | 79.5 ms                                                                | 108 ms: 1.35x slower                                                  |
| deepcopy                   | 263 us                                                                 | 356 us: 1.35x slower                                                  |
| tomli_loads                | 2.11 sec                                                               | 2.88 sec: 1.37x slower                                                |
| meteor_contest             | 99.2 ms                                                                | 136 ms: 1.37x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 10.3 ms: 1.39x slower                                                 |
| sqlglot_normalize          | 107 ms                                                                 | 149 ms: 1.39x slower                                                  |
| sqlglot_optimize           | 53.7 ms                                                                | 75.5 ms: 1.41x slower                                                 |
| deepcopy_reduce            | 2.69 us                                                                | 3.79 us: 1.41x slower                                                 |
| pycparser                  | 1.14 sec                                                               | 1.61 sec: 1.41x slower                                                |
| fannkuch                   | 386 ms                                                                 | 550 ms: 1.42x slower                                                  |
| pylint                     | 270 ms                                                                 | 396 ms: 1.46x slower                                                  |
| pprint_safe_repr           | 725 ms                                                                 | 1.07 sec: 1.48x slower                                                |
| 2to3                       | 257 ms                                                                 | 381 ms: 1.48x slower                                                  |
| html5lib                   | 67.3 ms                                                                | 99.7 ms: 1.48x slower                                                 |
| deepcopy_memo              | 30.4 us                                                                | 45.2 us: 1.49x slower                                                 |
| regex_compile              | 130 ms                                                                 | 196 ms: 1.50x slower                                                  |
| genshi_text                | 22.7 ms                                                                | 34.2 ms: 1.50x slower                                                 |
| pprint_pformat             | 1.48 sec                                                               | 2.23 sec: 1.51x slower                                                |
| crypto_pyaes               | 68.4 ms                                                                | 103 ms: 1.51x slower                                                  |
| subparsers                 | 22.1 ms                                                                | 33.5 ms: 1.52x slower                                                 |
| django_template            | 36.2 ms                                                                | 55.5 ms: 1.54x slower                                                 |
| sympy_integrate            | 20.0 ms                                                                | 31.3 ms: 1.57x slower                                                 |
| thrift                     | 744 us                                                                 | 1.21 ms: 1.62x slower                                                 |
| pyflate                    | 455 ms                                                                 | 738 ms: 1.62x slower                                                  |
| mako                       | 11.9 ms                                                                | 19.7 ms: 1.65x slower                                                 |
| comprehensions             | 17.3 us                                                                | 28.9 us: 1.67x slower                                                 |
| nbody                      | 93.7 ms                                                                | 158 ms: 1.69x slower                                                  |
| pickle_pure_python         | 321 us                                                                 | 545 us: 1.70x slower                                                  |
| unpickle_pure_python       | 218 us                                                                 | 371 us: 1.70x slower                                                  |
| logging_format             | 7.03 us                                                                | 12.3 us: 1.76x slower                                                 |
| richards                   | 47.2 ms                                                                | 83.6 ms: 1.77x slower                                                 |
| logging_simple             | 6.26 us                                                                | 11.1 us: 1.77x slower                                                 |
| float                      | 82.1 ms                                                                | 146 ms: 1.77x slower                                                  |
| logging_silent             | 109 ns                                                                 | 195 ns: 1.79x slower                                                  |
| scimark_sor                | 135 ms                                                                 | 243 ms: 1.80x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 497 ms: 1.82x slower                                                  |
| scimark_lu                 | 113 ms                                                                 | 205 ms: 1.82x slower                                                  |
| scimark_monte_carlo        | 66.5 ms                                                                | 121 ms: 1.82x slower                                                  |
| richards_super             | 53.8 ms                                                                | 99.7 ms: 1.85x slower                                                 |
| hexiom                     | 6.09 ms                                                                | 11.4 ms: 1.86x slower                                                 |
| sqlglot_transpile          | 1.62 ms                                                                | 3.09 ms: 1.91x slower                                                 |
| chaos                      | 59.2 ms                                                                | 115 ms: 1.95x slower                                                  |
| sqlglot_parse              | 1.32 ms                                                                | 2.68 ms: 2.03x slower                                                 |
| sympy_expand               | 460 ms                                                                 | 991 ms: 2.15x slower                                                  |
| raytrace                   | 266 ms                                                                 | 601 ms: 2.26x slower                                                  |
| go                         | 123 ms                                                                 | 284 ms: 2.32x slower                                                  |
| sympy_sum                  | 153 ms                                                                 | 358 ms: 2.34x slower                                                  |
| deltablue                  | 3.29 ms                                                                | 8.65 ms: 2.63x slower                                                 |
| bench_thread_pool          | 1.03 ms                                                                | 3.42 ms: 3.32x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.41x slower                                                          |

Benchmark hidden because not significant (2): k_core, async_tree_io_tg
Ignored benchmarks (2) of results/bm-20241122-3.14.0a2+-d24a22e/bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2+-d24a22e.json: sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.19x