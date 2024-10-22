# Results vs. base

- fork: python
- ref: d0bfff47fb2aea9272b5
- machine: linux-x86_64
- commit hash: d0bfff4
- commit date: 2024-10-21
- overall geometric mean: 1.51x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.44x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241021-3.14.0a1+-d0bfff4/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json | results/bm-20241021-3.14.0a1+-d0bfff4-NOGIL/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 445 ms                                                                                                            | 691 ms: 1.55x slower                                                                                                    |
| docutils       | 4.05 sec                                                                                                          | 4.96 sec: 1.22x slower                                                                                                  |
| html5lib       | 87.3 ms                                                                                                           | 155 ms: 1.78x slower                                                                                                    |
| tornado_http   | 279 ms                                                                                                            | 409 ms: 1.47x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.49x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | results/bm-20241021-3.14.0a1+-d0bfff4/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json | results/bm-20241021-3.14.0a1+-d0bfff4-NOGIL/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json |
|------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_tcp_ssl  | 2.82 sec                                                                                                          | 3.37 sec: 1.19x slower                                                                                                  |
| asyncio_tcp      | 968 ms                                                                                                            | 1.22 sec: 1.26x slower                                                                                                  |
| async_generators | 588 ms                                                                                                            | 754 ms: 1.28x slower                                                                                                    |
| coroutines       | 31.7 ms                                                                                                           | 41.3 ms: 1.30x slower                                                                                                   |
| Geometric mean   | (ref)                                                                                                             | 1.20x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241021-3.14.0a1+-d0bfff4/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json | results/bm-20241021-3.14.0a1+-d0bfff4-NOGIL/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 112 ms                                                                                                            | 190 ms: 1.70x slower                                                                                                    |
| nbody          | 124 ms                                                                                                            | 290 ms: 2.34x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.57x slower                                                                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241021-3.14.0a1+-d0bfff4/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json | results/bm-20241021-3.14.0a1+-d0bfff4-NOGIL/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 5.00 ms                                                                                                           | 4.70 ms: 1.06x faster                                                                                                   |
| regex_compile  | 179 ms                                                                                                            | 291 ms: 1.63x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241021-3.14.0a1+-d0bfff4/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json | results/bm-20241021-3.14.0a1+-d0bfff4-NOGIL/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pickle_dict          | 44.7 us                                                                                                           | 46.6 us: 1.04x slower                                                                                                   |
| xml_etree_parse      | 226 ms                                                                                                            | 252 ms: 1.11x slower                                                                                                    |
| xml_etree_iterparse  | 158 ms                                                                                                            | 178 ms: 1.13x slower                                                                                                    |
| json_loads           | 35.0 us                                                                                                           | 40.4 us: 1.15x slower                                                                                                   |
| unpickle             | 20.5 us                                                                                                           | 25.1 us: 1.22x slower                                                                                                   |
| xml_etree_generate   | 118 ms                                                                                                            | 164 ms: 1.38x slower                                                                                                    |
| json_dumps           | 15.1 ms                                                                                                           | 21.2 ms: 1.40x slower                                                                                                   |
| tomli_loads          | 2.88 sec                                                                                                          | 4.36 sec: 1.52x slower                                                                                                  |
| xml_etree_process    | 84.6 ms                                                                                                           | 131 ms: 1.55x slower                                                                                                    |
| unpickle_pure_python | 331 us                                                                                                            | 563 us: 1.70x slower                                                                                                    |
| pickle_pure_python   | 446 us                                                                                                            | 777 us: 1.74x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.26x slower                                                                                                            |

Benchmark hidden because not significant (3): pickle, pickle_list, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241021-3.14.0a1+-d0bfff4/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json | results/bm-20241021-3.14.0a1+-d0bfff4-NOGIL/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                                                                           | 20.6 ms: 1.35x slower                                                                                                   |
| python_startup         | 22.3 ms                                                                                                           | 33.6 ms: 1.50x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.42x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241021-3.14.0a1+-d0bfff4/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json | results/bm-20241021-3.14.0a1+-d0bfff4-NOGIL/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 71.7 ms                                                                                                           | 110 ms: 1.53x slower                                                                                                    |
| django_template | 45.7 ms                                                                                                           | 82.2 ms: 1.80x slower                                                                                                   |
| genshi_text     | 32.7 ms                                                                                                           | 60.5 ms: 1.85x slower                                                                                                   |
| mako            | 16.6 ms                                                                                                           | 32.3 ms: 1.95x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.77x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                | results/bm-20241021-3.14.0a1+-d0bfff4/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json | results/bm-20241021-3.14.0a1+-d0bfff4-NOGIL/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| create_gc_cycles         | 2.43 ms                                                                                                           | 1.97 ms: 1.24x faster                                                                                                   |
| bench_mp_pool            | 69.4 ms                                                                                                           | 62.2 ms: 1.12x faster                                                                                                   |
| regex_effbot             | 5.00 ms                                                                                                           | 4.70 ms: 1.06x faster                                                                                                   |
| pickle_dict              | 44.7 us                                                                                                           | 46.6 us: 1.04x slower                                                                                                   |
| json                     | 6.91 ms                                                                                                           | 7.43 ms: 1.08x slower                                                                                                   |
| sqlite_synth             | 4.13 us                                                                                                           | 4.46 us: 1.08x slower                                                                                                   |
| gc_traversal             | 5.38 ms                                                                                                           | 5.83 ms: 1.08x slower                                                                                                   |
| xml_etree_parse          | 226 ms                                                                                                            | 252 ms: 1.11x slower                                                                                                    |
| xml_etree_iterparse      | 158 ms                                                                                                            | 178 ms: 1.13x slower                                                                                                    |
| json_loads               | 35.0 us                                                                                                           | 40.4 us: 1.15x slower                                                                                                   |
| asyncio_tcp_ssl          | 2.82 sec                                                                                                          | 3.37 sec: 1.19x slower                                                                                                  |
| unpickle                 | 20.5 us                                                                                                           | 25.1 us: 1.22x slower                                                                                                   |
| docutils                 | 4.05 sec                                                                                                          | 4.96 sec: 1.22x slower                                                                                                  |
| asyncio_tcp              | 968 ms                                                                                                            | 1.22 sec: 1.26x slower                                                                                                  |
| pylint                   | 489 ms                                                                                                            | 618 ms: 1.26x slower                                                                                                    |
| coverage                 | 115 ms                                                                                                            | 146 ms: 1.27x slower                                                                                                    |
| telco                    | 11.2 ms                                                                                                           | 14.2 ms: 1.28x slower                                                                                                   |
| mdp                      | 3.96 sec                                                                                                          | 5.07 sec: 1.28x slower                                                                                                  |
| async_generators         | 588 ms                                                                                                            | 754 ms: 1.28x slower                                                                                                    |
| pathlib                  | 28.5 ms                                                                                                           | 36.6 ms: 1.28x slower                                                                                                   |
| coroutines               | 31.7 ms                                                                                                           | 41.3 ms: 1.30x slower                                                                                                   |
| scimark_sparse_mat_mult  | 7.24 ms                                                                                                           | 9.53 ms: 1.32x slower                                                                                                   |
| python_startup_no_site   | 15.3 ms                                                                                                           | 20.6 ms: 1.35x slower                                                                                                   |
| scimark_fft              | 481 ms                                                                                                            | 658 ms: 1.37x slower                                                                                                    |
| generators               | 39.6 ms                                                                                                           | 54.5 ms: 1.38x slower                                                                                                   |
| xml_etree_generate       | 118 ms                                                                                                            | 164 ms: 1.38x slower                                                                                                    |
| json_dumps               | 15.1 ms                                                                                                           | 21.2 ms: 1.40x slower                                                                                                   |
| bench_thread_pool        | 2.79 ms                                                                                                           | 3.93 ms: 1.41x slower                                                                                                   |
| pycparser                | 1.57 sec                                                                                                          | 2.29 sec: 1.46x slower                                                                                                  |
| tornado_http             | 279 ms                                                                                                            | 409 ms: 1.47x slower                                                                                                    |
| nqueens                  | 111 ms                                                                                                            | 163 ms: 1.47x slower                                                                                                    |
| python_startup           | 22.3 ms                                                                                                           | 33.6 ms: 1.50x slower                                                                                                   |
| thrift                   | 1.10 ms                                                                                                           | 1.66 ms: 1.50x slower                                                                                                   |
| crypto_pyaes             | 96.1 ms                                                                                                           | 145 ms: 1.51x slower                                                                                                    |
| tomli_loads              | 2.88 sec                                                                                                          | 4.36 sec: 1.52x slower                                                                                                  |
| sympy_integrate          | 30.4 ms                                                                                                           | 46.2 ms: 1.52x slower                                                                                                   |
| fannkuch                 | 517 ms                                                                                                            | 790 ms: 1.53x slower                                                                                                    |
| genshi_xml               | 71.7 ms                                                                                                           | 110 ms: 1.53x slower                                                                                                    |
| deepcopy                 | 366 us                                                                                                            | 564 us: 1.54x slower                                                                                                    |
| xml_etree_process        | 84.6 ms                                                                                                           | 131 ms: 1.55x slower                                                                                                    |
| 2to3                     | 445 ms                                                                                                            | 691 ms: 1.55x slower                                                                                                    |
| dulwich_log              | 94.0 ms                                                                                                           | 148 ms: 1.58x slower                                                                                                    |
| meteor_contest           | 145 ms                                                                                                            | 230 ms: 1.59x slower                                                                                                    |
| sqlglot_optimize         | 78.7 ms                                                                                                           | 125 ms: 1.59x slower                                                                                                    |
| typing_runtime_protocols | 219 us                                                                                                            | 352 us: 1.61x slower                                                                                                    |
| sqlglot_normalize        | 146 ms                                                                                                            | 235 ms: 1.62x slower                                                                                                    |
| regex_compile            | 179 ms                                                                                                            | 291 ms: 1.63x slower                                                                                                    |
| spectral_norm            | 158 ms                                                                                                            | 257 ms: 1.63x slower                                                                                                    |
| deepcopy_reduce          | 3.61 us                                                                                                           | 5.93 us: 1.64x slower                                                                                                   |
| bpe_tokeniser            | 6.08 sec                                                                                                          | 10.2 sec: 1.67x slower                                                                                                  |
| pyflate                  | 674 ms                                                                                                            | 1.13 sec: 1.68x slower                                                                                                  |
| unpickle_pure_python     | 331 us                                                                                                            | 563 us: 1.70x slower                                                                                                    |
| float                    | 112 ms                                                                                                            | 190 ms: 1.70x slower                                                                                                    |
| comprehensions           | 22.5 us                                                                                                           | 39.0 us: 1.73x slower                                                                                                   |
| pickle_pure_python       | 446 us                                                                                                            | 777 us: 1.74x slower                                                                                                    |
| richards                 | 59.8 ms                                                                                                           | 106 ms: 1.77x slower                                                                                                    |
| html5lib                 | 87.3 ms                                                                                                           | 155 ms: 1.78x slower                                                                                                    |
| deepcopy_memo            | 40.2 us                                                                                                           | 72.0 us: 1.79x slower                                                                                                   |
| django_template          | 45.7 ms                                                                                                           | 82.2 ms: 1.80x slower                                                                                                   |
| logging_simple           | 8.71 us                                                                                                           | 15.7 us: 1.80x slower                                                                                                   |
| richards_super           | 69.4 ms                                                                                                           | 126 ms: 1.81x slower                                                                                                    |
| pprint_pformat           | 1.97 sec                                                                                                          | 3.63 sec: 1.84x slower                                                                                                  |
| genshi_text              | 32.7 ms                                                                                                           | 60.5 ms: 1.85x slower                                                                                                   |
| logging_format           | 9.46 us                                                                                                           | 17.6 us: 1.86x slower                                                                                                   |
| sympy_str                | 365 ms                                                                                                            | 690 ms: 1.89x slower                                                                                                    |
| logging_silent           | 133 ns                                                                                                            | 258 ns: 1.93x slower                                                                                                    |
| mako                     | 16.6 ms                                                                                                           | 32.3 ms: 1.95x slower                                                                                                   |
| pprint_safe_repr         | 949 ms                                                                                                            | 1.88 sec: 1.98x slower                                                                                                  |
| chaos                    | 83.7 ms                                                                                                           | 166 ms: 1.99x slower                                                                                                    |
| scimark_lu               | 155 ms                                                                                                            | 313 ms: 2.02x slower                                                                                                    |
| scimark_monte_carlo      | 91.4 ms                                                                                                           | 186 ms: 2.03x slower                                                                                                    |
| hexiom                   | 8.67 ms                                                                                                           | 18.0 ms: 2.08x slower                                                                                                   |
| sqlglot_transpile        | 2.37 ms                                                                                                           | 4.99 ms: 2.10x slower                                                                                                   |
| scimark_sor              | 173 ms                                                                                                            | 373 ms: 2.16x slower                                                                                                    |
| sympy_expand             | 613 ms                                                                                                            | 1.36 sec: 2.21x slower                                                                                                  |
| sympy_sum                | 215 ms                                                                                                            | 488 ms: 2.27x slower                                                                                                    |
| sqlglot_parse            | 1.78 ms                                                                                                           | 4.06 ms: 2.28x slower                                                                                                   |
| raytrace                 | 354 ms                                                                                                            | 811 ms: 2.29x slower                                                                                                    |
| go                       | 163 ms                                                                                                            | 381 ms: 2.34x slower                                                                                                    |
| nbody                    | 124 ms                                                                                                            | 290 ms: 2.34x slower                                                                                                    |
| deltablue                | 4.43 ms                                                                                                           | 11.5 ms: 2.58x slower                                                                                                   |
| unpack_sequence          | 66.1 ns                                                                                                           | 193 ns: 2.92x slower                                                                                                    |
| Geometric mean           | (ref)                                                                                                             | 1.51x slower                                                                                                            |

Benchmark hidden because not significant (7): pidigits, pickle, pickle_list, regex_dna, asyncio_websockets, regex_v8, unpickle_list

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.48x
- 95% likely to have a slowdown of 1.47x
- 99% likely to have a slowdown of 1.44x

# Memory
- memory change: 1.15x