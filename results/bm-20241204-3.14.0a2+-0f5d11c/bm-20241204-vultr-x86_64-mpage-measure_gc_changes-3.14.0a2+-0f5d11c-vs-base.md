# Results vs. base

- fork: mpage
- ref: measure_gc_changes
- machine: linux-x86_64
- commit hash: 0f5d11c
- commit date: 2024-12-04
- overall geometric mean: 1.019x slower
- HPT reliability: 74.19%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 258 ms: 1.01x faster                                                |
| docutils       | 2.58 sec                                                               | 2.61 sec: 1.01x slower                                              |
| sphinx         | 997 ms                                                                 | 1.03 sec: 1.03x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| coroutines                 | 22.5 ms                                                                | 22.3 ms: 1.01x faster                                               |
| async_generators           | 366 ms                                                                 | 370 ms: 1.01x slower                                                |
| async_tree_cpu_io_mixed    | 503 ms                                                                 | 570 ms: 1.13x slower                                                |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 564 ms: 1.16x slower                                                |
| async_tree_none            | 278 ms                                                                 | 331 ms: 1.19x slower                                                |
| async_tree_memoization     | 341 ms                                                                 | 408 ms: 1.20x slower                                                |
| async_tree_memoization_tg  | 314 ms                                                                 | 388 ms: 1.24x slower                                                |
| async_tree_none_tg         | 264 ms                                                                 | 345 ms: 1.30x slower                                                |
| async_tree_io              | 629 ms                                                                 | 850 ms: 1.35x slower                                                |
| async_tree_io_tg           | 629 ms                                                                 | 882 ms: 1.40x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.17x slower                                                        |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 79.2 ms                                                                | 80.7 ms: 1.02x slower                                               |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                        |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 131 ms                                                                 | 129 ms: 1.01x faster                                                |
| regex_effbot   | 2.79 ms                                                                | 2.82 ms: 1.01x slower                                               |
| regex_dna      | 171 ms                                                                 | 176 ms: 1.03x slower                                                |
| regex_v8       | 23.7 ms                                                                | 24.7 ms: 1.04x slower                                               |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_loads           | 25.4 us                                                                | 24.8 us: 1.03x faster                                               |
| unpickle_pure_python | 222 us                                                                 | 218 us: 1.02x faster                                                |
| pickle_pure_python   | 322 us                                                                 | 320 us: 1.01x faster                                                |
| json_dumps           | 11.4 ms                                                                | 11.4 ms: 1.00x faster                                               |
| xml_etree_generate   | 85.8 ms                                                                | 86.3 ms: 1.01x slower                                               |
| xml_etree_parse      | 130 ms                                                                 | 137 ms: 1.05x slower                                                |
| xml_etree_iterparse  | 92.3 ms                                                                | 98.9 ms: 1.07x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                        |

Benchmark hidden because not significant (2): xml_etree_process, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.50 ms                                                                | 7.38 ms: 1.02x faster                                               |
| python_startup         | 14.7 ms                                                                | 14.5 ms: 1.01x faster                                               |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| django_template | 36.3 ms                                                                | 35.6 ms: 1.02x faster                                               |
| genshi_text     | 22.1 ms                                                                | 22.2 ms: 1.01x slower                                               |
| mako            | 11.6 ms                                                                | 11.7 ms: 1.01x slower                                               |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal               | 4.28 ms                                                                | 4.02 ms: 1.07x faster                                               |
| pylint                     | 285 ms                                                                 | 270 ms: 1.05x faster                                                |
| bench_mp_pool              | 89.6 ms                                                                | 85.9 ms: 1.04x faster                                               |
| deepcopy_memo              | 31.1 us                                                                | 30.0 us: 1.04x faster                                               |
| scimark_sor                | 137 ms                                                                 | 133 ms: 1.03x faster                                                |
| scimark_lu                 | 114 ms                                                                 | 111 ms: 1.03x faster                                                |
| deepcopy                   | 266 us                                                                 | 259 us: 1.03x faster                                                |
| json_loads                 | 25.4 us                                                                | 24.8 us: 1.03x faster                                               |
| richards                   | 47.9 ms                                                                | 46.7 ms: 1.03x faster                                               |
| sqlglot_transpile          | 1.64 ms                                                                | 1.60 ms: 1.03x faster                                               |
| raytrace                   | 272 ms                                                                 | 266 ms: 1.02x faster                                                |
| deepcopy_reduce            | 2.68 us                                                                | 2.61 us: 1.02x faster                                               |
| logging_silent             | 112 ns                                                                 | 110 ns: 1.02x faster                                                |
| chaos                      | 60.0 ms                                                                | 58.8 ms: 1.02x faster                                               |
| django_template            | 36.3 ms                                                                | 35.6 ms: 1.02x faster                                               |
| deltablue                  | 3.36 ms                                                                | 3.30 ms: 1.02x faster                                               |
| unpickle_pure_python       | 222 us                                                                 | 218 us: 1.02x faster                                                |
| nqueens                    | 79.8 ms                                                                | 78.5 ms: 1.02x faster                                               |
| python_startup_no_site     | 7.50 ms                                                                | 7.38 ms: 1.02x faster                                               |
| scimark_monte_carlo        | 66.4 ms                                                                | 65.5 ms: 1.01x faster                                               |
| richards_super             | 54.0 ms                                                                | 53.2 ms: 1.01x faster                                               |
| sqlglot_parse              | 1.32 ms                                                                | 1.30 ms: 1.01x faster                                               |
| subparsers                 | 22.5 ms                                                                | 22.2 ms: 1.01x faster                                               |
| pprint_pformat             | 1.48 sec                                                               | 1.46 sec: 1.01x faster                                              |
| pyflate                    | 457 ms                                                                 | 451 ms: 1.01x faster                                                |
| coroutines                 | 22.5 ms                                                                | 22.3 ms: 1.01x faster                                               |
| hexiom                     | 6.10 ms                                                                | 6.03 ms: 1.01x faster                                               |
| pprint_safe_repr           | 729 ms                                                                 | 721 ms: 1.01x faster                                                |
| many_optionals             | 1.03 ms                                                                | 1.02 ms: 1.01x faster                                               |
| regex_compile              | 131 ms                                                                 | 129 ms: 1.01x faster                                                |
| sympy_str                  | 277 ms                                                                 | 275 ms: 1.01x faster                                                |
| python_startup             | 14.7 ms                                                                | 14.5 ms: 1.01x faster                                               |
| go                         | 124 ms                                                                 | 123 ms: 1.01x faster                                                |
| sqlalchemy_declarative     | 128 ms                                                                 | 127 ms: 1.01x faster                                                |
| pickle_pure_python         | 322 us                                                                 | 320 us: 1.01x faster                                                |
| 2to3                       | 259 ms                                                                 | 258 ms: 1.01x faster                                                |
| fannkuch                   | 378 ms                                                                 | 375 ms: 1.01x faster                                                |
| scimark_sparse_mat_mult    | 4.47 ms                                                                | 4.45 ms: 1.01x faster                                               |
| sqlglot_optimize           | 54.1 ms                                                                | 53.9 ms: 1.00x faster                                               |
| sympy_sum                  | 154 ms                                                                 | 154 ms: 1.00x faster                                                |
| sympy_integrate            | 20.2 ms                                                                | 20.1 ms: 1.00x faster                                               |
| scimark_fft                | 338 ms                                                                 | 337 ms: 1.00x faster                                                |
| json_dumps                 | 11.4 ms                                                                | 11.4 ms: 1.00x faster                                               |
| sqlglot_normalize          | 107 ms                                                                 | 108 ms: 1.00x slower                                                |
| bench_thread_pool          | 1.02 ms                                                                | 1.03 ms: 1.01x slower                                               |
| xml_etree_generate         | 85.8 ms                                                                | 86.3 ms: 1.01x slower                                               |
| crypto_pyaes               | 67.6 ms                                                                | 68.0 ms: 1.01x slower                                               |
| generators                 | 29.1 ms                                                                | 29.3 ms: 1.01x slower                                               |
| genshi_text                | 22.1 ms                                                                | 22.2 ms: 1.01x slower                                               |
| mako                       | 11.6 ms                                                                | 11.7 ms: 1.01x slower                                               |
| sqlite_synth               | 2.22 us                                                                | 2.24 us: 1.01x slower                                               |
| docutils                   | 2.58 sec                                                               | 2.61 sec: 1.01x slower                                              |
| regex_effbot               | 2.79 ms                                                                | 2.82 ms: 1.01x slower                                               |
| async_generators           | 366 ms                                                                 | 370 ms: 1.01x slower                                                |
| spectral_norm              | 113 ms                                                                 | 114 ms: 1.01x slower                                                |
| coverage                   | 78.9 ms                                                                | 80.0 ms: 1.01x slower                                               |
| float                      | 79.2 ms                                                                | 80.7 ms: 1.02x slower                                               |
| bpe_tokeniser              | 4.34 sec                                                               | 4.44 sec: 1.02x slower                                              |
| sqlalchemy_imperative      | 19.2 ms                                                                | 19.6 ms: 1.03x slower                                               |
| regex_dna                  | 171 ms                                                                 | 176 ms: 1.03x slower                                                |
| sphinx                     | 997 ms                                                                 | 1.03 sec: 1.03x slower                                              |
| regex_v8                   | 23.7 ms                                                                | 24.7 ms: 1.04x slower                                               |
| xml_etree_parse            | 130 ms                                                                 | 137 ms: 1.05x slower                                                |
| mdp                        | 2.34 sec                                                               | 2.51 sec: 1.07x slower                                              |
| xml_etree_iterparse        | 92.3 ms                                                                | 98.9 ms: 1.07x slower                                               |
| create_gc_cycles           | 1.82 ms                                                                | 1.96 ms: 1.07x slower                                               |
| async_tree_cpu_io_mixed    | 503 ms                                                                 | 570 ms: 1.13x slower                                                |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 564 ms: 1.16x slower                                                |
| async_tree_none            | 278 ms                                                                 | 331 ms: 1.19x slower                                                |
| async_tree_memoization     | 341 ms                                                                 | 408 ms: 1.20x slower                                                |
| k_core                     | 2.08 sec                                                               | 2.50 sec: 1.20x slower                                              |
| async_tree_memoization_tg  | 314 ms                                                                 | 388 ms: 1.24x slower                                                |
| async_tree_none_tg         | 264 ms                                                                 | 345 ms: 1.30x slower                                                |
| async_tree_io              | 629 ms                                                                 | 850 ms: 1.35x slower                                                |
| async_tree_io_tg           | 629 ms                                                                 | 882 ms: 1.40x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                        |

Benchmark hidden because not significant (20): comprehensions, telco, logging_format, sympy_expand, logging_simple, json, nbody, genshi_xml, asyncio_websockets, pycparser, thrift, pidigits, shortest_path, meteor_contest, xml_etree_process, pathlib, connected_components, dulwich_log, typing_runtime_protocols, tomli_loads

- Geometric mean (including insignificant results): 1.019x slower

# HPT report

- Reliability score: 74.19% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x