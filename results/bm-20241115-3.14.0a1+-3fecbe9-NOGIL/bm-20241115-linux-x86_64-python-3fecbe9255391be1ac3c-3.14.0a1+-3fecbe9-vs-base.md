# Results vs. base

- fork: python
- ref: 3fecbe9255391be1ac3c
- machine: linux-x86_64
- commit hash: 3fecbe9
- commit date: 2024-11-15
- overall geometric mean: 1.46x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.37x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 431 ms                                                                                                            | 656 ms: 1.52x slower                                                                                                    |
| docutils       | 3.70 sec                                                                                                          | 4.56 sec: 1.23x slower                                                                                                  |
| html5lib       | 86.7 ms                                                                                                           | 135 ms: 1.56x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.43x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_tcp      | 903 ms                                                                                                            | 1.05 sec: 1.16x slower                                                                                                  |
| asyncio_tcp_ssl  | 2.75 sec                                                                                                          | 3.33 sec: 1.21x slower                                                                                                  |
| coroutines       | 33.0 ms                                                                                                           | 39.9 ms: 1.21x slower                                                                                                   |
| async_generators | 542 ms                                                                                                            | 713 ms: 1.32x slower                                                                                                    |
| Geometric mean   | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 117 ms                                                                                                            | 190 ms: 1.63x slower                                                                                                    |
| nbody          | 124 ms                                                                                                            | 250 ms: 2.02x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.49x slower                                                                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 34.4 ms                                                                                                           | 38.8 ms: 1.13x slower                                                                                                   |
| regex_compile  | 176 ms                                                                                                            | 290 ms: 1.64x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pickle_dict          | 46.6 us                                                                                                           | 43.2 us: 1.08x faster                                                                                                   |
| pickle               | 17.3 us                                                                                                           | 16.0 us: 1.08x faster                                                                                                   |
| json_loads           | 36.6 us                                                                                                           | 39.3 us: 1.07x slower                                                                                                   |
| unpickle_list        | 6.67 us                                                                                                           | 7.71 us: 1.16x slower                                                                                                   |
| unpickle             | 19.5 us                                                                                                           | 23.7 us: 1.21x slower                                                                                                   |
| json_dumps           | 15.3 ms                                                                                                           | 19.3 ms: 1.26x slower                                                                                                   |
| xml_etree_generate   | 118 ms                                                                                                            | 157 ms: 1.33x slower                                                                                                    |
| tomli_loads          | 2.68 sec                                                                                                          | 4.11 sec: 1.53x slower                                                                                                  |
| xml_etree_process    | 83.2 ms                                                                                                           | 129 ms: 1.55x slower                                                                                                    |
| pickle_pure_python   | 437 us                                                                                                            | 761 us: 1.74x slower                                                                                                    |
| unpickle_pure_python | 292 us                                                                                                            | 539 us: 1.85x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.22x slower                                                                                                            |

Benchmark hidden because not significant (3): pickle_list, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 20.5 ms                                                                                                           | 30.8 ms: 1.51x slower                                                                                                   |
| python_startup_no_site | 13.9 ms                                                                                                           | 20.9 ms: 1.51x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.51x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 68.4 ms                                                                                                           | 111 ms: 1.62x slower                                                                                                    |
| genshi_text     | 30.2 ms                                                                                                           | 53.0 ms: 1.76x slower                                                                                                   |
| django_template | 44.5 ms                                                                                                           | 81.0 ms: 1.82x slower                                                                                                   |
| mako            | 16.5 ms                                                                                                           | 30.9 ms: 1.87x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.77x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                | results/bm-20241115-3.14.0a1+-3fecbe9/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json | results/bm-20241115-3.14.0a1+-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal             | 5.44 ms                                                                                                           | 3.97 ms: 1.37x faster                                                                                                   |
| create_gc_cycles         | 2.42 ms                                                                                                           | 1.85 ms: 1.31x faster                                                                                                   |
| bench_mp_pool            | 66.7 ms                                                                                                           | 59.4 ms: 1.12x faster                                                                                                   |
| pickle_dict              | 46.6 us                                                                                                           | 43.2 us: 1.08x faster                                                                                                   |
| pickle                   | 17.3 us                                                                                                           | 16.0 us: 1.08x faster                                                                                                   |
| json                     | 6.92 ms                                                                                                           | 7.26 ms: 1.05x slower                                                                                                   |
| json_loads               | 36.6 us                                                                                                           | 39.3 us: 1.07x slower                                                                                                   |
| pathlib                  | 28.6 ms                                                                                                           | 32.1 ms: 1.12x slower                                                                                                   |
| regex_v8                 | 34.4 ms                                                                                                           | 38.8 ms: 1.13x slower                                                                                                   |
| sqlite_synth             | 3.80 us                                                                                                           | 4.37 us: 1.15x slower                                                                                                   |
| unpickle_list            | 6.67 us                                                                                                           | 7.71 us: 1.16x slower                                                                                                   |
| asyncio_tcp              | 903 ms                                                                                                            | 1.05 sec: 1.16x slower                                                                                                  |
| asyncio_tcp_ssl          | 2.75 sec                                                                                                          | 3.33 sec: 1.21x slower                                                                                                  |
| bench_thread_pool        | 2.92 ms                                                                                                           | 3.53 ms: 1.21x slower                                                                                                   |
| coroutines               | 33.0 ms                                                                                                           | 39.9 ms: 1.21x slower                                                                                                   |
| unpickle                 | 19.5 us                                                                                                           | 23.7 us: 1.21x slower                                                                                                   |
| scimark_sparse_mat_mult  | 6.39 ms                                                                                                           | 7.79 ms: 1.22x slower                                                                                                   |
| scimark_fft              | 480 ms                                                                                                            | 590 ms: 1.23x slower                                                                                                    |
| docutils                 | 3.70 sec                                                                                                          | 4.56 sec: 1.23x slower                                                                                                  |
| json_dumps               | 15.3 ms                                                                                                           | 19.3 ms: 1.26x slower                                                                                                   |
| mdp                      | 3.79 sec                                                                                                          | 4.86 sec: 1.28x slower                                                                                                  |
| async_generators         | 542 ms                                                                                                            | 713 ms: 1.32x slower                                                                                                    |
| dulwich_log              | 100 ms                                                                                                            | 133 ms: 1.32x slower                                                                                                    |
| telco                    | 10.4 ms                                                                                                           | 13.8 ms: 1.32x slower                                                                                                   |
| xml_etree_generate       | 118 ms                                                                                                            | 157 ms: 1.33x slower                                                                                                    |
| coverage                 | 113 ms                                                                                                            | 150 ms: 1.33x slower                                                                                                    |
| pylint                   | 459 ms                                                                                                            | 616 ms: 1.34x slower                                                                                                    |
| meteor_contest           | 140 ms                                                                                                            | 190 ms: 1.36x slower                                                                                                    |
| pycparser                | 1.56 sec                                                                                                          | 2.13 sec: 1.36x slower                                                                                                  |
| spectral_norm            | 158 ms                                                                                                            | 222 ms: 1.41x slower                                                                                                    |
| nqueens                  | 105 ms                                                                                                            | 149 ms: 1.42x slower                                                                                                    |
| generators               | 39.0 ms                                                                                                           | 56.7 ms: 1.45x slower                                                                                                   |
| deepcopy_reduce          | 3.76 us                                                                                                           | 5.53 us: 1.47x slower                                                                                                   |
| sqlglot_normalize        | 145 ms                                                                                                            | 214 ms: 1.48x slower                                                                                                    |
| fannkuch                 | 501 ms                                                                                                            | 748 ms: 1.49x slower                                                                                                    |
| python_startup           | 20.5 ms                                                                                                           | 30.8 ms: 1.51x slower                                                                                                   |
| python_startup_no_site   | 13.9 ms                                                                                                           | 20.9 ms: 1.51x slower                                                                                                   |
| 2to3                     | 431 ms                                                                                                            | 656 ms: 1.52x slower                                                                                                    |
| crypto_pyaes             | 97.4 ms                                                                                                           | 149 ms: 1.53x slower                                                                                                    |
| tomli_loads              | 2.68 sec                                                                                                          | 4.11 sec: 1.53x slower                                                                                                  |
| xml_etree_process        | 83.2 ms                                                                                                           | 129 ms: 1.55x slower                                                                                                    |
| html5lib                 | 86.7 ms                                                                                                           | 135 ms: 1.56x slower                                                                                                    |
| bpe_tokeniser            | 5.83 sec                                                                                                          | 9.21 sec: 1.58x slower                                                                                                  |
| genshi_xml               | 68.4 ms                                                                                                           | 111 ms: 1.62x slower                                                                                                    |
| float                    | 117 ms                                                                                                            | 190 ms: 1.63x slower                                                                                                    |
| sympy_integrate          | 27.5 ms                                                                                                           | 44.8 ms: 1.63x slower                                                                                                   |
| pyflate                  | 641 ms                                                                                                            | 1.04 sec: 1.63x slower                                                                                                  |
| thrift                   | 1.05 ms                                                                                                           | 1.72 ms: 1.64x slower                                                                                                   |
| sqlglot_optimize         | 70.2 ms                                                                                                           | 115 ms: 1.64x slower                                                                                                    |
| regex_compile            | 176 ms                                                                                                            | 290 ms: 1.64x slower                                                                                                    |
| deepcopy                 | 352 us                                                                                                            | 582 us: 1.65x slower                                                                                                    |
| typing_runtime_protocols | 211 us                                                                                                            | 351 us: 1.66x slower                                                                                                    |
| deepcopy_memo            | 39.9 us                                                                                                           | 66.7 us: 1.67x slower                                                                                                   |
| scimark_monte_carlo      | 87.7 ms                                                                                                           | 150 ms: 1.72x slower                                                                                                    |
| pickle_pure_python       | 437 us                                                                                                            | 761 us: 1.74x slower                                                                                                    |
| genshi_text              | 30.2 ms                                                                                                           | 53.0 ms: 1.76x slower                                                                                                   |
| comprehensions           | 21.9 us                                                                                                           | 38.5 us: 1.76x slower                                                                                                   |
| pprint_safe_repr         | 937 ms                                                                                                            | 1.65 sec: 1.76x slower                                                                                                  |
| logging_simple           | 8.48 us                                                                                                           | 15.0 us: 1.77x slower                                                                                                   |
| pprint_pformat           | 1.88 sec                                                                                                          | 3.34 sec: 1.78x slower                                                                                                  |
| richards_super           | 71.4 ms                                                                                                           | 127 ms: 1.78x slower                                                                                                    |
| django_template          | 44.5 ms                                                                                                           | 81.0 ms: 1.82x slower                                                                                                   |
| richards                 | 62.9 ms                                                                                                           | 115 ms: 1.83x slower                                                                                                    |
| logging_silent           | 139 ns                                                                                                            | 255 ns: 1.84x slower                                                                                                    |
| unpickle_pure_python     | 292 us                                                                                                            | 539 us: 1.85x slower                                                                                                    |
| chaos                    | 83.5 ms                                                                                                           | 156 ms: 1.87x slower                                                                                                    |
| scimark_lu               | 155 ms                                                                                                            | 290 ms: 1.87x slower                                                                                                    |
| mako                     | 16.5 ms                                                                                                           | 30.9 ms: 1.87x slower                                                                                                   |
| scimark_sor              | 172 ms                                                                                                            | 327 ms: 1.90x slower                                                                                                    |
| sympy_str                | 362 ms                                                                                                            | 688 ms: 1.90x slower                                                                                                    |
| hexiom                   | 8.22 ms                                                                                                           | 15.8 ms: 1.93x slower                                                                                                   |
| logging_format           | 9.47 us                                                                                                           | 18.3 us: 1.93x slower                                                                                                   |
| nbody                    | 124 ms                                                                                                            | 250 ms: 2.02x slower                                                                                                    |
| sympy_expand             | 601 ms                                                                                                            | 1.26 sec: 2.10x slower                                                                                                  |
| sqlglot_parse            | 1.75 ms                                                                                                           | 3.68 ms: 2.10x slower                                                                                                   |
| raytrace                 | 362 ms                                                                                                            | 776 ms: 2.15x slower                                                                                                    |
| sympy_sum                | 212 ms                                                                                                            | 457 ms: 2.16x slower                                                                                                    |
| sqlglot_transpile        | 2.26 ms                                                                                                           | 4.89 ms: 2.17x slower                                                                                                   |
| go                       | 160 ms                                                                                                            | 353 ms: 2.20x slower                                                                                                    |
| deltablue                | 4.57 ms                                                                                                           | 11.6 ms: 2.53x slower                                                                                                   |
| unpack_sequence          | 59.7 ns                                                                                                           | 197 ns: 3.30x slower                                                                                                    |
| Geometric mean           | (ref)                                                                                                             | 1.46x slower                                                                                                            |

Benchmark hidden because not significant (7): pickle_list, regex_effbot, xml_etree_parse, asyncio_websockets, pidigits, xml_etree_iterparse, regex_dna

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.44x
- 95% likely to have a slowdown of 1.41x
- 99% likely to have a slowdown of 1.37x

# Memory
- memory change: 1.18x