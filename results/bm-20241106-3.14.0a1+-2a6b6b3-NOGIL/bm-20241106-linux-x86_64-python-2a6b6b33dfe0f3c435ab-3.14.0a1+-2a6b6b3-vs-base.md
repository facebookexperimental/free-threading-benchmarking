# Results vs. base

- fork: python
- ref: 2a6b6b33dfe0f3c435ab
- machine: linux-x86_64
- commit hash: 2a6b6b3
- commit date: 2024-11-06
- overall geometric mean: 1.43x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.34x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 434 ms                                                                                                            | 659 ms: 1.52x slower                                                                                                    |
| docutils       | 3.75 sec                                                                                                          | 4.71 sec: 1.26x slower                                                                                                  |
| html5lib       | 87.9 ms                                                                                                           | 130 ms: 1.47x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.41x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_tcp      | 884 ms                                                                                                            | 1.02 sec: 1.16x slower                                                                                                  |
| asyncio_tcp_ssl  | 2.78 sec                                                                                                          | 3.30 sec: 1.19x slower                                                                                                  |
| async_generators | 583 ms                                                                                                            | 723 ms: 1.24x slower                                                                                                    |
| coroutines       | 32.4 ms                                                                                                           | 41.8 ms: 1.29x slower                                                                                                   |
| Geometric mean   | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 117 ms                                                                                                            | 186 ms: 1.59x slower                                                                                                    |
| nbody          | 134 ms                                                                                                            | 263 ms: 1.97x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.48x slower                                                                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 5.05 ms                                                                                                           | 4.74 ms: 1.06x faster                                                                                                   |
| regex_v8       | 32.4 ms                                                                                                           | 36.2 ms: 1.12x slower                                                                                                   |
| regex_compile  | 169 ms                                                                                                            | 288 ms: 1.70x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pickle_list          | 6.95 us                                                                                                           | 5.87 us: 1.18x faster                                                                                                   |
| pickle               | 15.4 us                                                                                                           | 13.9 us: 1.11x faster                                                                                                   |
| xml_etree_parse      | 234 ms                                                                                                            | 216 ms: 1.08x faster                                                                                                    |
| unpickle_list        | 6.91 us                                                                                                           | 7.39 us: 1.07x slower                                                                                                   |
| json_loads           | 37.8 us                                                                                                           | 41.5 us: 1.10x slower                                                                                                   |
| unpickle             | 20.5 us                                                                                                           | 23.3 us: 1.14x slower                                                                                                   |
| json_dumps           | 15.9 ms                                                                                                           | 19.5 ms: 1.23x slower                                                                                                   |
| xml_etree_generate   | 123 ms                                                                                                            | 156 ms: 1.27x slower                                                                                                    |
| tomli_loads          | 2.77 sec                                                                                                          | 4.11 sec: 1.48x slower                                                                                                  |
| xml_etree_process    | 86.5 ms                                                                                                           | 133 ms: 1.53x slower                                                                                                    |
| pickle_pure_python   | 463 us                                                                                                            | 797 us: 1.72x slower                                                                                                    |
| unpickle_pure_python | 293 us                                                                                                            | 520 us: 1.77x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmark hidden because not significant (2): xml_etree_iterparse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 13.9 ms                                                                                                           | 18.9 ms: 1.36x slower                                                                                                   |
| python_startup         | 20.1 ms                                                                                                           | 27.5 ms: 1.37x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.36x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 48.7 ms                                                                                                           | 79.1 ms: 1.63x slower                                                                                                   |
| genshi_xml      | 68.7 ms                                                                                                           | 119 ms: 1.74x slower                                                                                                    |
| genshi_text     | 31.6 ms                                                                                                           | 55.5 ms: 1.75x slower                                                                                                   |
| mako            | 15.6 ms                                                                                                           | 29.1 ms: 1.87x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.74x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal             | 5.61 ms                                                                                                           | 4.11 ms: 1.37x faster                                                                                                   |
| create_gc_cycles         | 2.48 ms                                                                                                           | 1.85 ms: 1.34x faster                                                                                                   |
| pickle_list              | 6.95 us                                                                                                           | 5.87 us: 1.18x faster                                                                                                   |
| bench_mp_pool            | 67.7 ms                                                                                                           | 60.0 ms: 1.13x faster                                                                                                   |
| pickle                   | 15.4 us                                                                                                           | 13.9 us: 1.11x faster                                                                                                   |
| xml_etree_parse          | 234 ms                                                                                                            | 216 ms: 1.08x faster                                                                                                    |
| regex_effbot             | 5.05 ms                                                                                                           | 4.74 ms: 1.06x faster                                                                                                   |
| unpickle_list            | 6.91 us                                                                                                           | 7.39 us: 1.07x slower                                                                                                   |
| sqlite_synth             | 3.89 us                                                                                                           | 4.23 us: 1.09x slower                                                                                                   |
| pathlib                  | 28.6 ms                                                                                                           | 31.3 ms: 1.09x slower                                                                                                   |
| json_loads               | 37.8 us                                                                                                           | 41.5 us: 1.10x slower                                                                                                   |
| regex_v8                 | 32.4 ms                                                                                                           | 36.2 ms: 1.12x slower                                                                                                   |
| scimark_fft              | 498 ms                                                                                                            | 562 ms: 1.13x slower                                                                                                    |
| unpickle                 | 20.5 us                                                                                                           | 23.3 us: 1.14x slower                                                                                                   |
| asyncio_tcp              | 884 ms                                                                                                            | 1.02 sec: 1.16x slower                                                                                                  |
| asyncio_tcp_ssl          | 2.78 sec                                                                                                          | 3.30 sec: 1.19x slower                                                                                                  |
| bench_thread_pool        | 2.80 ms                                                                                                           | 3.34 ms: 1.19x slower                                                                                                   |
| json_dumps               | 15.9 ms                                                                                                           | 19.5 ms: 1.23x slower                                                                                                   |
| async_generators         | 583 ms                                                                                                            | 723 ms: 1.24x slower                                                                                                    |
| telco                    | 10.7 ms                                                                                                           | 13.3 ms: 1.25x slower                                                                                                   |
| pylint                   | 460 ms                                                                                                            | 576 ms: 1.25x slower                                                                                                    |
| docutils                 | 3.75 sec                                                                                                          | 4.71 sec: 1.26x slower                                                                                                  |
| xml_etree_generate       | 123 ms                                                                                                            | 156 ms: 1.27x slower                                                                                                    |
| coroutines               | 32.4 ms                                                                                                           | 41.8 ms: 1.29x slower                                                                                                   |
| pycparser                | 1.59 sec                                                                                                          | 2.06 sec: 1.30x slower                                                                                                  |
| meteor_contest           | 148 ms                                                                                                            | 192 ms: 1.30x slower                                                                                                    |
| json                     | 6.70 ms                                                                                                           | 8.70 ms: 1.30x slower                                                                                                   |
| scimark_sparse_mat_mult  | 6.51 ms                                                                                                           | 8.50 ms: 1.31x slower                                                                                                   |
| coverage                 | 111 ms                                                                                                            | 145 ms: 1.31x slower                                                                                                    |
| nqueens                  | 113 ms                                                                                                            | 152 ms: 1.34x slower                                                                                                    |
| dulwich_log              | 95.8 ms                                                                                                           | 130 ms: 1.35x slower                                                                                                    |
| python_startup_no_site   | 13.9 ms                                                                                                           | 18.9 ms: 1.36x slower                                                                                                   |
| mdp                      | 3.45 sec                                                                                                          | 4.71 sec: 1.36x slower                                                                                                  |
| python_startup           | 20.1 ms                                                                                                           | 27.5 ms: 1.37x slower                                                                                                   |
| generators               | 38.5 ms                                                                                                           | 53.6 ms: 1.39x slower                                                                                                   |
| spectral_norm            | 157 ms                                                                                                            | 220 ms: 1.40x slower                                                                                                    |
| fannkuch                 | 540 ms                                                                                                            | 759 ms: 1.41x slower                                                                                                    |
| thrift                   | 1.19 ms                                                                                                           | 1.72 ms: 1.45x slower                                                                                                   |
| crypto_pyaes             | 104 ms                                                                                                            | 151 ms: 1.46x slower                                                                                                    |
| html5lib                 | 87.9 ms                                                                                                           | 130 ms: 1.47x slower                                                                                                    |
| tomli_loads              | 2.77 sec                                                                                                          | 4.11 sec: 1.48x slower                                                                                                  |
| deepcopy                 | 373 us                                                                                                            | 555 us: 1.49x slower                                                                                                    |
| richards                 | 70.1 ms                                                                                                           | 105 ms: 1.50x slower                                                                                                    |
| 2to3                     | 434 ms                                                                                                            | 659 ms: 1.52x slower                                                                                                    |
| sympy_integrate          | 29.8 ms                                                                                                           | 45.5 ms: 1.53x slower                                                                                                   |
| xml_etree_process        | 86.5 ms                                                                                                           | 133 ms: 1.53x slower                                                                                                    |
| bpe_tokeniser            | 5.84 sec                                                                                                          | 9.01 sec: 1.54x slower                                                                                                  |
| pyflate                  | 649 ms                                                                                                            | 1.01 sec: 1.55x slower                                                                                                  |
| comprehensions           | 23.8 us                                                                                                           | 37.0 us: 1.56x slower                                                                                                   |
| logging_format           | 10.8 us                                                                                                           | 16.9 us: 1.56x slower                                                                                                   |
| deepcopy_reduce          | 3.77 us                                                                                                           | 5.92 us: 1.57x slower                                                                                                   |
| typing_runtime_protocols | 212 us                                                                                                            | 336 us: 1.58x slower                                                                                                    |
| float                    | 117 ms                                                                                                            | 186 ms: 1.59x slower                                                                                                    |
| django_template          | 48.7 ms                                                                                                           | 79.1 ms: 1.63x slower                                                                                                   |
| sqlglot_normalize        | 146 ms                                                                                                            | 238 ms: 1.64x slower                                                                                                    |
| deepcopy_memo            | 42.9 us                                                                                                           | 70.8 us: 1.65x slower                                                                                                   |
| pprint_safe_repr         | 990 ms                                                                                                            | 1.65 sec: 1.66x slower                                                                                                  |
| regex_compile            | 169 ms                                                                                                            | 288 ms: 1.70x slower                                                                                                    |
| sqlglot_optimize         | 74.8 ms                                                                                                           | 127 ms: 1.70x slower                                                                                                    |
| pprint_pformat           | 1.96 sec                                                                                                          | 3.34 sec: 1.71x slower                                                                                                  |
| pickle_pure_python       | 463 us                                                                                                            | 797 us: 1.72x slower                                                                                                    |
| genshi_xml               | 68.7 ms                                                                                                           | 119 ms: 1.74x slower                                                                                                    |
| genshi_text              | 31.6 ms                                                                                                           | 55.5 ms: 1.75x slower                                                                                                   |
| scimark_monte_carlo      | 88.4 ms                                                                                                           | 155 ms: 1.76x slower                                                                                                    |
| unpickle_pure_python     | 293 us                                                                                                            | 520 us: 1.77x slower                                                                                                    |
| sympy_str                | 371 ms                                                                                                            | 660 ms: 1.78x slower                                                                                                    |
| richards_super           | 72.9 ms                                                                                                           | 133 ms: 1.83x slower                                                                                                    |
| logging_simple           | 8.09 us                                                                                                           | 14.9 us: 1.84x slower                                                                                                   |
| logging_silent           | 140 ns                                                                                                            | 260 ns: 1.86x slower                                                                                                    |
| mako                     | 15.6 ms                                                                                                           | 29.1 ms: 1.87x slower                                                                                                   |
| scimark_sor              | 183 ms                                                                                                            | 351 ms: 1.92x slower                                                                                                    |
| scimark_lu               | 156 ms                                                                                                            | 300 ms: 1.93x slower                                                                                                    |
| hexiom                   | 8.46 ms                                                                                                           | 16.3 ms: 1.93x slower                                                                                                   |
| chaos                    | 85.2 ms                                                                                                           | 166 ms: 1.94x slower                                                                                                    |
| nbody                    | 134 ms                                                                                                            | 263 ms: 1.97x slower                                                                                                    |
| sqlglot_transpile        | 2.42 ms                                                                                                           | 4.86 ms: 2.01x slower                                                                                                   |
| sqlglot_parse            | 1.84 ms                                                                                                           | 3.81 ms: 2.06x slower                                                                                                   |
| raytrace                 | 354 ms                                                                                                            | 749 ms: 2.12x slower                                                                                                    |
| sympy_expand             | 604 ms                                                                                                            | 1.29 sec: 2.13x slower                                                                                                  |
| go                       | 165 ms                                                                                                            | 362 ms: 2.20x slower                                                                                                    |
| sympy_sum                | 208 ms                                                                                                            | 468 ms: 2.25x slower                                                                                                    |
| deltablue                | 4.64 ms                                                                                                           | 11.0 ms: 2.38x slower                                                                                                   |
| unpack_sequence          | 61.6 ns                                                                                                           | 199 ns: 3.23x slower                                                                                                    |
| Geometric mean           | (ref)                                                                                                             | 1.43x slower                                                                                                            |

Benchmark hidden because not significant (5): xml_etree_iterparse, pickle_dict, asyncio_websockets, regex_dna, pidigits

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.39x
- 95% likely to have a slowdown of 1.37x
- 99% likely to have a slowdown of 1.34x

# Memory
- memory change: 1.18x