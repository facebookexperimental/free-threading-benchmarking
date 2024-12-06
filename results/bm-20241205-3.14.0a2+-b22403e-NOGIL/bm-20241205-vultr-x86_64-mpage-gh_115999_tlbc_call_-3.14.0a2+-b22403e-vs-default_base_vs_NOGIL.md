# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: b22403e
- commit date: 2024-12-05
- overall geometric mean: 1.262x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                 | 366 ms: 1.42x slower                                                  |
| docutils       | 2.57 sec                                                               | 3.11 sec: 1.21x slower                                                |
| sphinx         | 994 ms                                                                 | 1.19 sec: 1.20x slower                                                |
| Geometric mean | (ref)                                                                  | 1.27x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 521 ms: 1.00x faster                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                                 | 621 ms: 1.06x slower                                                  |
| async_tree_cpu_io_mixed    | 607 ms                                                                 | 644 ms: 1.06x slower                                                  |
| coroutines                 | 21.9 ms                                                                | 24.0 ms: 1.10x slower                                                 |
| async_generators           | 370 ms                                                                 | 451 ms: 1.22x slower                                                  |
| async_tree_io_tg           | 624 ms                                                                 | 827 ms: 1.32x slower                                                  |
| async_tree_io              | 626 ms                                                                 | 848 ms: 1.35x slower                                                  |
| async_tree_none_tg         | 262 ms                                                                 | 358 ms: 1.37x slower                                                  |
| async_tree_memoization     | 339 ms                                                                 | 469 ms: 1.39x slower                                                  |
| async_tree_none            | 276 ms                                                                 | 386 ms: 1.40x slower                                                  |
| async_tree_memoization_tg  | 314 ms                                                                 | 452 ms: 1.44x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.24x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 222 ms                                                                 | 184 ms: 1.21x faster                                                  |
| nbody          | 95.2 ms                                                                | 131 ms: 1.38x slower                                                  |
| float          | 78.6 ms                                                                | 140 ms: 1.78x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.27x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.74 ms                                                                | 2.90 ms: 1.06x slower                                                 |
| regex_v8       | 23.3 ms                                                                | 24.9 ms: 1.07x slower                                                 |
| regex_dna      | 169 ms                                                                 | 189 ms: 1.12x slower                                                  |
| regex_compile  | 130 ms                                                                 | 180 ms: 1.38x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.1 ms                                                                | 91.6 ms: 1.01x faster                                                 |
| json_loads           | 25.1 us                                                                | 28.7 us: 1.14x slower                                                 |
| xml_etree_generate   | 85.1 ms                                                                | 97.5 ms: 1.15x slower                                                 |
| json_dumps           | 11.5 ms                                                                | 14.3 ms: 1.24x slower                                                 |
| tomli_loads          | 2.11 sec                                                               | 2.66 sec: 1.26x slower                                                |
| xml_etree_process    | 59.6 ms                                                                | 78.3 ms: 1.32x slower                                                 |
| unpickle_pure_python | 216 us                                                                 | 334 us: 1.54x slower                                                  |
| pickle_pure_python   | 316 us                                                                 | 504 us: 1.59x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.23x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

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
| genshi_xml      | 51.2 ms                                                                | 63.2 ms: 1.24x slower                                                 |
| genshi_text     | 22.3 ms                                                                | 31.6 ms: 1.42x slower                                                 |
| django_template | 35.6 ms                                                                | 50.7 ms: 1.43x slower                                                 |
| mako            | 11.5 ms                                                                | 17.8 ms: 1.55x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.40x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241206-vultr-x86_64-python-e991ac8f2037d78140e4-3.14.0a2+-e991ac8 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.58 ms                                                                | 3.29 ms: 1.39x faster                                                 |
| pidigits                   | 222 ms                                                                 | 184 ms: 1.21x faster                                                  |
| create_gc_cycles           | 1.83 ms                                                                | 1.81 ms: 1.01x faster                                                 |
| xml_etree_iterparse        | 92.1 ms                                                                | 91.6 ms: 1.01x faster                                                 |
| asyncio_websockets         | 523 ms                                                                 | 521 ms: 1.00x faster                                                  |
| sqlite_synth               | 2.28 us                                                                | 2.30 us: 1.01x slower                                                 |
| async_tree_cpu_io_mixed_tg | 587 ms                                                                 | 621 ms: 1.06x slower                                                  |
| regex_effbot               | 2.74 ms                                                                | 2.90 ms: 1.06x slower                                                 |
| async_tree_cpu_io_mixed    | 607 ms                                                                 | 644 ms: 1.06x slower                                                  |
| regex_v8                   | 23.3 ms                                                                | 24.9 ms: 1.07x slower                                                 |
| coroutines                 | 21.9 ms                                                                | 24.0 ms: 1.10x slower                                                 |
| spectral_norm              | 107 ms                                                                 | 119 ms: 1.11x slower                                                  |
| regex_dna                  | 169 ms                                                                 | 189 ms: 1.12x slower                                                  |
| pathlib                    | 18.2 ms                                                                | 20.3 ms: 1.12x slower                                                 |
| json_loads                 | 25.1 us                                                                | 28.7 us: 1.14x slower                                                 |
| json                       | 4.53 ms                                                                | 5.18 ms: 1.14x slower                                                 |
| xml_etree_generate         | 85.1 ms                                                                | 97.5 ms: 1.15x slower                                                 |
| bpe_tokeniser              | 4.32 sec                                                               | 5.01 sec: 1.16x slower                                                |
| scimark_fft                | 340 ms                                                                 | 395 ms: 1.16x slower                                                  |
| k_core                     | 2.08 sec                                                               | 2.42 sec: 1.17x slower                                                |
| python_startup             | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                 |
| sphinx                     | 994 ms                                                                 | 1.19 sec: 1.20x slower                                                |
| telco                      | 7.19 ms                                                                | 8.63 ms: 1.20x slower                                                 |
| docutils                   | 2.57 sec                                                               | 3.11 sec: 1.21x slower                                                |
| nqueens                    | 79.5 ms                                                                | 96.9 ms: 1.22x slower                                                 |
| async_generators           | 370 ms                                                                 | 451 ms: 1.22x slower                                                  |
| mdp                        | 2.35 sec                                                               | 2.89 sec: 1.23x slower                                                |
| bench_mp_pool              | 88.5 ms                                                                | 109 ms: 1.23x slower                                                  |
| genshi_xml                 | 51.2 ms                                                                | 63.2 ms: 1.24x slower                                                 |
| json_dumps                 | 11.5 ms                                                                | 14.3 ms: 1.24x slower                                                 |
| shortest_path              | 444 ms                                                                 | 552 ms: 1.24x slower                                                  |
| connected_components       | 400 ms                                                                 | 501 ms: 1.25x slower                                                  |
| many_optionals             | 1.03 ms                                                                | 1.29 ms: 1.25x slower                                                 |
| deepcopy                   | 262 us                                                                 | 328 us: 1.25x slower                                                  |
| tomli_loads                | 2.11 sec                                                               | 2.66 sec: 1.26x slower                                                |
| typing_runtime_protocols   | 161 us                                                                 | 203 us: 1.26x slower                                                  |
| coverage                   | 79.8 ms                                                                | 101 ms: 1.26x slower                                                  |
| dulwich_log                | 76.1 ms                                                                | 96.5 ms: 1.27x slower                                                 |
| sqlglot_normalize          | 107 ms                                                                 | 136 ms: 1.27x slower                                                  |
| sqlglot_optimize           | 53.6 ms                                                                | 69.0 ms: 1.29x slower                                                 |
| deepcopy_memo              | 30.7 us                                                                | 39.7 us: 1.30x slower                                                 |
| scimark_sparse_mat_mult    | 4.57 ms                                                                | 5.97 ms: 1.31x slower                                                 |
| meteor_contest             | 99.1 ms                                                                | 130 ms: 1.31x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 494 ms: 1.31x slower                                                  |
| xml_etree_process          | 59.6 ms                                                                | 78.3 ms: 1.32x slower                                                 |
| async_tree_io_tg           | 624 ms                                                                 | 827 ms: 1.32x slower                                                  |
| generators                 | 29.0 ms                                                                | 38.4 ms: 1.33x slower                                                 |
| pylint                     | 285 ms                                                                 | 383 ms: 1.34x slower                                                  |
| pprint_safe_repr           | 715 ms                                                                 | 965 ms: 1.35x slower                                                  |
| crypto_pyaes               | 68.1 ms                                                                | 92.0 ms: 1.35x slower                                                 |
| pycparser                  | 1.13 sec                                                               | 1.52 sec: 1.35x slower                                                |
| deepcopy_reduce            | 2.60 us                                                                | 3.51 us: 1.35x slower                                                 |
| async_tree_io              | 626 ms                                                                 | 848 ms: 1.35x slower                                                  |
| pprint_pformat             | 1.45 sec                                                               | 1.99 sec: 1.37x slower                                                |
| async_tree_none_tg         | 262 ms                                                                 | 358 ms: 1.37x slower                                                  |
| nbody                      | 95.2 ms                                                                | 131 ms: 1.38x slower                                                  |
| regex_compile              | 130 ms                                                                 | 180 ms: 1.38x slower                                                  |
| python_startup_no_site     | 7.43 ms                                                                | 10.3 ms: 1.38x slower                                                 |
| async_tree_memoization     | 339 ms                                                                 | 469 ms: 1.39x slower                                                  |
| async_tree_none            | 276 ms                                                                 | 386 ms: 1.40x slower                                                  |
| genshi_text                | 22.3 ms                                                                | 31.6 ms: 1.42x slower                                                 |
| 2to3                       | 257 ms                                                                 | 366 ms: 1.42x slower                                                  |
| django_template            | 35.6 ms                                                                | 50.7 ms: 1.43x slower                                                 |
| async_tree_memoization_tg  | 314 ms                                                                 | 452 ms: 1.44x slower                                                  |
| subparsers                 | 22.1 ms                                                                | 32.3 ms: 1.46x slower                                                 |
| sympy_integrate            | 20.1 ms                                                                | 29.5 ms: 1.47x slower                                                 |
| sqlalchemy_imperative      | 19.4 ms                                                                | 29.1 ms: 1.51x slower                                                 |
| unpickle_pure_python       | 216 us                                                                 | 334 us: 1.54x slower                                                  |
| mako                       | 11.5 ms                                                                | 17.8 ms: 1.55x slower                                                 |
| pyflate                    | 448 ms                                                                 | 697 ms: 1.55x slower                                                  |
| comprehensions             | 17.3 us                                                                | 27.2 us: 1.57x slower                                                 |
| thrift                     | 736 us                                                                 | 1.16 ms: 1.57x slower                                                 |
| pickle_pure_python         | 316 us                                                                 | 504 us: 1.59x slower                                                  |
| sqlalchemy_declarative     | 127 ms                                                                 | 204 ms: 1.61x slower                                                  |
| richards_super             | 52.7 ms                                                                | 85.2 ms: 1.62x slower                                                 |
| richards                   | 46.7 ms                                                                | 76.0 ms: 1.63x slower                                                 |
| hexiom                     | 5.99 ms                                                                | 9.88 ms: 1.65x slower                                                 |
| scimark_lu                 | 109 ms                                                                 | 182 ms: 1.67x slower                                                  |
| sympy_str                  | 277 ms                                                                 | 476 ms: 1.72x slower                                                  |
| logging_format             | 7.04 us                                                                | 12.2 us: 1.73x slower                                                 |
| chaos                      | 60.1 ms                                                                | 104 ms: 1.73x slower                                                  |
| logging_simple             | 6.27 us                                                                | 10.9 us: 1.74x slower                                                 |
| scimark_sor                | 133 ms                                                                 | 235 ms: 1.77x slower                                                  |
| logging_silent             | 105 ns                                                                 | 186 ns: 1.77x slower                                                  |
| float                      | 78.6 ms                                                                | 140 ms: 1.78x slower                                                  |
| scimark_monte_carlo        | 65.6 ms                                                                | 119 ms: 1.81x slower                                                  |
| sqlglot_transpile          | 1.61 ms                                                                | 3.00 ms: 1.87x slower                                                 |
| sqlglot_parse              | 1.30 ms                                                                | 2.60 ms: 2.00x slower                                                 |
| sympy_expand               | 460 ms                                                                 | 953 ms: 2.07x slower                                                  |
| raytrace                   | 265 ms                                                                 | 551 ms: 2.08x slower                                                  |
| go                         | 120 ms                                                                 | 266 ms: 2.22x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 350 ms: 2.27x slower                                                  |
| deltablue                  | 3.25 ms                                                                | 7.94 ms: 2.44x slower                                                 |
| bench_thread_pool          | 1.02 ms                                                                | 3.35 ms: 3.29x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.37x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse
Ignored benchmarks (1) of results/bm-20241205-3.14.0a2+-b22403e-NOGIL/bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e.json: html5lib

- Geometric mean (including insignificant results): 1.262x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.19x