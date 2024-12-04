# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: measure_gc_changes
- machine: linux-x86_64
- commit hash: 0f5d11c
- commit date: 2024-12-04
- overall geometric mean: 1.291x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.31x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 376 ms: 1.45x slower                                                |
| docutils       | 2.58 sec                                                               | 3.19 sec: 1.24x slower                                              |
| sphinx         | 997 ms                                                                 | 1.23 sec: 1.23x slower                                              |
| Geometric mean | (ref)                                                                  | 1.30x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                |
| coroutines                 | 22.5 ms                                                                | 28.4 ms: 1.26x slower                                               |
| async_generators           | 366 ms                                                                 | 467 ms: 1.28x slower                                                |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 624 ms: 1.28x slower                                                |
| async_tree_cpu_io_mixed    | 503 ms                                                                 | 659 ms: 1.31x slower                                                |
| async_tree_io_tg           | 629 ms                                                                 | 865 ms: 1.38x slower                                                |
| async_tree_none_tg         | 264 ms                                                                 | 366 ms: 1.38x slower                                                |
| async_tree_io              | 629 ms                                                                 | 891 ms: 1.42x slower                                                |
| async_tree_none            | 278 ms                                                                 | 400 ms: 1.44x slower                                                |
| async_tree_memoization     | 341 ms                                                                 | 493 ms: 1.45x slower                                                |
| async_tree_memoization_tg  | 314 ms                                                                 | 461 ms: 1.47x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.33x slower                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 184 ms: 1.00x faster                                                |
| nbody          | 95.5 ms                                                                | 128 ms: 1.34x slower                                                |
| float          | 79.2 ms                                                                | 143 ms: 1.81x slower                                                |
| Geometric mean | (ref)                                                                  | 1.34x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 2.79 ms                                                                | 2.67 ms: 1.04x faster                                               |
| regex_dna      | 171 ms                                                                 | 175 ms: 1.02x slower                                                |
| regex_compile  | 131 ms                                                                 | 191 ms: 1.46x slower                                                |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                        |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.3 ms                                                                | 94.9 ms: 1.03x slower                                               |
| json_loads           | 25.4 us                                                                | 28.1 us: 1.11x slower                                               |
| xml_etree_generate   | 85.8 ms                                                                | 103 ms: 1.20x slower                                                |
| json_dumps           | 11.4 ms                                                                | 14.5 ms: 1.27x slower                                               |
| tomli_loads          | 2.10 sec                                                               | 2.81 sec: 1.34x slower                                              |
| xml_etree_process    | 60.1 ms                                                                | 82.3 ms: 1.37x slower                                               |
| unpickle_pure_python | 222 us                                                                 | 379 us: 1.71x slower                                                |
| pickle_pure_python   | 322 us                                                                 | 556 us: 1.72x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.28x slower                                                        |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 17.4 ms: 1.19x slower                                               |
| python_startup_no_site | 7.50 ms                                                                | 10.2 ms: 1.36x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.27x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 50.5 ms                                                                | 66.7 ms: 1.32x slower                                               |
| genshi_text     | 22.1 ms                                                                | 33.5 ms: 1.52x slower                                               |
| django_template | 36.3 ms                                                                | 55.2 ms: 1.52x slower                                               |
| mako            | 11.6 ms                                                                | 19.6 ms: 1.68x slower                                               |
| Geometric mean  | (ref)                                                                  | 1.51x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20241203-vultr-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal               | 4.28 ms                                                                | 3.30 ms: 1.30x faster                                               |
| regex_effbot               | 2.79 ms                                                                | 2.67 ms: 1.04x faster                                               |
| asyncio_websockets         | 523 ms                                                                 | 520 ms: 1.01x faster                                                |
| pidigits                   | 185 ms                                                                 | 184 ms: 1.00x faster                                                |
| regex_dna                  | 171 ms                                                                 | 175 ms: 1.02x slower                                                |
| xml_etree_iterparse        | 92.3 ms                                                                | 94.9 ms: 1.03x slower                                               |
| sqlite_synth               | 2.22 us                                                                | 2.30 us: 1.04x slower                                               |
| json_loads                 | 25.4 us                                                                | 28.1 us: 1.11x slower                                               |
| json                       | 4.56 ms                                                                | 5.06 ms: 1.11x slower                                               |
| pathlib                    | 18.2 ms                                                                | 20.7 ms: 1.14x slower                                               |
| k_core                     | 2.08 sec                                                               | 2.45 sec: 1.17x slower                                              |
| spectral_norm              | 113 ms                                                                 | 134 ms: 1.18x slower                                                |
| scimark_fft                | 338 ms                                                                 | 401 ms: 1.19x slower                                                |
| python_startup             | 14.7 ms                                                                | 17.4 ms: 1.19x slower                                               |
| telco                      | 7.37 ms                                                                | 8.79 ms: 1.19x slower                                               |
| xml_etree_generate         | 85.8 ms                                                                | 103 ms: 1.20x slower                                                |
| bench_mp_pool              | 89.6 ms                                                                | 110 ms: 1.22x slower                                                |
| sphinx                     | 997 ms                                                                 | 1.23 sec: 1.23x slower                                              |
| docutils                   | 2.58 sec                                                               | 3.19 sec: 1.24x slower                                              |
| bpe_tokeniser              | 4.34 sec                                                               | 5.47 sec: 1.26x slower                                              |
| coroutines                 | 22.5 ms                                                                | 28.4 ms: 1.26x slower                                               |
| coverage                   | 78.9 ms                                                                | 99.7 ms: 1.26x slower                                               |
| json_dumps                 | 11.4 ms                                                                | 14.5 ms: 1.27x slower                                               |
| connected_components       | 402 ms                                                                 | 513 ms: 1.28x slower                                                |
| async_generators           | 366 ms                                                                 | 467 ms: 1.28x slower                                                |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 624 ms: 1.28x slower                                                |
| shortest_path              | 442 ms                                                                 | 569 ms: 1.29x slower                                                |
| mdp                        | 2.34 sec                                                               | 3.03 sec: 1.29x slower                                              |
| nqueens                    | 79.8 ms                                                                | 103 ms: 1.29x slower                                                |
| dulwich_log                | 76.2 ms                                                                | 98.9 ms: 1.30x slower                                               |
| scimark_sparse_mat_mult    | 4.47 ms                                                                | 5.82 ms: 1.30x slower                                               |
| async_tree_cpu_io_mixed    | 503 ms                                                                 | 659 ms: 1.31x slower                                                |
| genshi_xml                 | 50.5 ms                                                                | 66.7 ms: 1.32x slower                                               |
| generators                 | 29.1 ms                                                                | 38.4 ms: 1.32x slower                                               |
| many_optionals             | 1.03 ms                                                                | 1.37 ms: 1.33x slower                                               |
| deepcopy                   | 266 us                                                                 | 353 us: 1.33x slower                                                |
| tomli_loads                | 2.10 sec                                                               | 2.81 sec: 1.34x slower                                              |
| nbody                      | 95.5 ms                                                                | 128 ms: 1.34x slower                                                |
| typing_runtime_protocols   | 157 us                                                                 | 212 us: 1.35x slower                                                |
| meteor_contest             | 100 ms                                                                 | 135 ms: 1.35x slower                                                |
| fannkuch                   | 378 ms                                                                 | 511 ms: 1.35x slower                                                |
| python_startup_no_site     | 7.50 ms                                                                | 10.2 ms: 1.36x slower                                               |
| xml_etree_process          | 60.1 ms                                                                | 82.3 ms: 1.37x slower                                               |
| async_tree_io_tg           | 629 ms                                                                 | 865 ms: 1.38x slower                                                |
| pylint                     | 285 ms                                                                 | 393 ms: 1.38x slower                                                |
| async_tree_none_tg         | 264 ms                                                                 | 366 ms: 1.38x slower                                                |
| sqlglot_optimize           | 54.1 ms                                                                | 75.4 ms: 1.39x slower                                               |
| deepcopy_reduce            | 2.68 us                                                                | 3.74 us: 1.40x slower                                               |
| sqlglot_normalize          | 107 ms                                                                 | 151 ms: 1.41x slower                                                |
| crypto_pyaes               | 67.6 ms                                                                | 95.4 ms: 1.41x slower                                               |
| async_tree_io              | 629 ms                                                                 | 891 ms: 1.42x slower                                                |
| pycparser                  | 1.13 sec                                                               | 1.61 sec: 1.42x slower                                              |
| async_tree_none            | 278 ms                                                                 | 400 ms: 1.44x slower                                                |
| deepcopy_memo              | 31.1 us                                                                | 44.9 us: 1.45x slower                                               |
| async_tree_memoization     | 341 ms                                                                 | 493 ms: 1.45x slower                                                |
| 2to3                       | 259 ms                                                                 | 376 ms: 1.45x slower                                                |
| regex_compile              | 131 ms                                                                 | 191 ms: 1.46x slower                                                |
| pprint_safe_repr           | 729 ms                                                                 | 1.07 sec: 1.47x slower                                              |
| async_tree_memoization_tg  | 314 ms                                                                 | 461 ms: 1.47x slower                                                |
| subparsers                 | 22.5 ms                                                                | 33.7 ms: 1.50x slower                                               |
| pprint_pformat             | 1.48 sec                                                               | 2.24 sec: 1.51x slower                                              |
| genshi_text                | 22.1 ms                                                                | 33.5 ms: 1.52x slower                                               |
| django_template            | 36.3 ms                                                                | 55.2 ms: 1.52x slower                                               |
| sympy_integrate            | 20.2 ms                                                                | 30.8 ms: 1.53x slower                                               |
| sqlalchemy_imperative      | 19.2 ms                                                                | 30.2 ms: 1.57x slower                                               |
| pyflate                    | 457 ms                                                                 | 726 ms: 1.59x slower                                                |
| sqlalchemy_declarative     | 128 ms                                                                 | 207 ms: 1.62x slower                                                |
| comprehensions             | 17.8 us                                                                | 28.9 us: 1.63x slower                                               |
| thrift                     | 744 us                                                                 | 1.22 ms: 1.64x slower                                               |
| mako                       | 11.6 ms                                                                | 19.6 ms: 1.68x slower                                               |
| scimark_lu                 | 114 ms                                                                 | 194 ms: 1.70x slower                                                |
| unpickle_pure_python       | 222 us                                                                 | 379 us: 1.71x slower                                                |
| pickle_pure_python         | 322 us                                                                 | 556 us: 1.72x slower                                                |
| richards                   | 47.9 ms                                                                | 82.6 ms: 1.73x slower                                               |
| logging_silent             | 112 ns                                                                 | 197 ns: 1.76x slower                                                |
| logging_format             | 7.12 us                                                                | 12.6 us: 1.76x slower                                               |
| hexiom                     | 6.10 ms                                                                | 10.8 ms: 1.77x slower                                               |
| logging_simple             | 6.36 us                                                                | 11.3 us: 1.78x slower                                               |
| scimark_sor                | 137 ms                                                                 | 245 ms: 1.79x slower                                                |
| sympy_str                  | 277 ms                                                                 | 495 ms: 1.79x slower                                                |
| float                      | 79.2 ms                                                                | 143 ms: 1.81x slower                                                |
| richards_super             | 54.0 ms                                                                | 99.1 ms: 1.84x slower                                               |
| scimark_monte_carlo        | 66.4 ms                                                                | 122 ms: 1.84x slower                                                |
| chaos                      | 60.0 ms                                                                | 112 ms: 1.86x slower                                                |
| sqlglot_transpile          | 1.64 ms                                                                | 3.08 ms: 1.88x slower                                               |
| sqlglot_parse              | 1.32 ms                                                                | 2.66 ms: 2.02x slower                                               |
| sympy_expand               | 466 ms                                                                 | 987 ms: 2.12x slower                                                |
| raytrace                   | 272 ms                                                                 | 602 ms: 2.21x slower                                                |
| go                         | 124 ms                                                                 | 281 ms: 2.27x slower                                                |
| sympy_sum                  | 154 ms                                                                 | 359 ms: 2.32x slower                                                |
| deltablue                  | 3.36 ms                                                                | 8.76 ms: 2.61x slower                                               |
| bench_thread_pool          | 1.02 ms                                                                | 3.38 ms: 3.31x slower                                               |
| Geometric mean             | (ref)                                                                  | 1.42x slower                                                        |

Benchmark hidden because not significant (3): xml_etree_parse, create_gc_cycles, regex_v8
Ignored benchmarks (1) of results/bm-20241204-3.14.0a2+-0f5d11c-NOGIL/bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c.json: html5lib

- Geometric mean (including insignificant results): 1.291x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.33x
- 99% likely to have a slowdown of 1.31x

# Memory
- memory change: 1.19x