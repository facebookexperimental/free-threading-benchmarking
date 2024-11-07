# Results vs. base

- fork: python
- ref: 2a6b6b33dfe0f3c435ab
- machine: linux-x86_64
- commit hash: 2a6b6b3
- commit date: 2024-11-06
- overall geometric mean: 1.53x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.40x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                                                            | 417 ms: 1.64x slower                                                                                                    |
| docutils       | 2.61 sec                                                                                                          | 3.41 sec: 1.30x slower                                                                                                  |
| html5lib       | 66.5 ms                                                                                                           | 107 ms: 1.61x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.51x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|--------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets | 520 ms                                                                                                            | 516 ms: 1.01x faster                                                                                                    |
| asyncio_tcp        | 506 ms                                                                                                            | 584 ms: 1.15x slower                                                                                                    |
| asyncio_tcp_ssl    | 1.52 sec                                                                                                          | 1.84 sec: 1.21x slower                                                                                                  |
| coroutines         | 23.6 ms                                                                                                           | 31.2 ms: 1.32x slower                                                                                                   |
| async_generators   | 373 ms                                                                                                            | 499 ms: 1.34x slower                                                                                                    |
| Geometric mean     | (ref)                                                                                                             | 1.20x slower                                                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 222 ms                                                                                                            | 188 ms: 1.18x faster                                                                                                    |
| float          | 79.7 ms                                                                                                           | 152 ms: 1.91x slower                                                                                                    |
| nbody          | 95.6 ms                                                                                                           | 205 ms: 2.15x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.51x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 24.6 ms                                                                                                           | 25.2 ms: 1.02x slower                                                                                                   |
| regex_dna      | 184 ms                                                                                                            | 189 ms: 1.03x slower                                                                                                    |
| regex_compile  | 132 ms                                                                                                            | 233 ms: 1.77x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pickle_dict          | 32.8 us                                                                                                           | 31.4 us: 1.05x faster                                                                                                   |
| pickle_list          | 4.90 us                                                                                                           | 4.73 us: 1.03x faster                                                                                                   |
| pickle               | 11.3 us                                                                                                           | 10.9 us: 1.03x faster                                                                                                   |
| xml_etree_parse      | 135 ms                                                                                                            | 134 ms: 1.01x faster                                                                                                    |
| unpickle_list        | 4.68 us                                                                                                           | 4.91 us: 1.05x slower                                                                                                   |
| unpickle             | 13.3 us                                                                                                           | 14.9 us: 1.12x slower                                                                                                   |
| xml_etree_iterparse  | 95.9 ms                                                                                                           | 110 ms: 1.14x slower                                                                                                    |
| json_loads           | 25.7 us                                                                                                           | 29.9 us: 1.16x slower                                                                                                   |
| json_dumps           | 11.6 ms                                                                                                           | 15.2 ms: 1.31x slower                                                                                                   |
| xml_etree_generate   | 85.4 ms                                                                                                           | 114 ms: 1.33x slower                                                                                                    |
| tomli_loads          | 2.10 sec                                                                                                          | 3.22 sec: 1.53x slower                                                                                                  |
| xml_etree_process    | 59.5 ms                                                                                                           | 94.9 ms: 1.60x slower                                                                                                   |
| unpickle_pure_python | 217 us                                                                                                            | 417 us: 1.92x slower                                                                                                    |
| pickle_pure_python   | 317 us                                                                                                            | 627 us: 1.98x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.25x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                                                           | 10.3 ms: 1.38x slower                                                                                                   |
| python_startup         | 11.0 ms                                                                                                           | 15.7 ms: 1.43x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.41x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 50.9 ms                                                                                                           | 82.2 ms: 1.61x slower                                                                                                   |
| mako            | 12.0 ms                                                                                                           | 20.6 ms: 1.72x slower                                                                                                   |
| genshi_text     | 22.6 ms                                                                                                           | 40.3 ms: 1.79x slower                                                                                                   |
| django_template | 35.2 ms                                                                                                           | 64.9 ms: 1.85x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.74x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                | results/bm-20241106-3.14.0a1+-2a6b6b3/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json | results/bm-20241106-3.14.0a1+-2a6b6b3-NOGIL/bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal             | 3.24 ms                                                                                                           | 2.47 ms: 1.31x faster                                                                                                   |
| create_gc_cycles         | 1.35 ms                                                                                                           | 1.13 ms: 1.19x faster                                                                                                   |
| pidigits                 | 222 ms                                                                                                            | 188 ms: 1.18x faster                                                                                                    |
| pickle_dict              | 32.8 us                                                                                                           | 31.4 us: 1.05x faster                                                                                                   |
| pickle_list              | 4.90 us                                                                                                           | 4.73 us: 1.03x faster                                                                                                   |
| pickle                   | 11.3 us                                                                                                           | 10.9 us: 1.03x faster                                                                                                   |
| xml_etree_parse          | 135 ms                                                                                                            | 134 ms: 1.01x faster                                                                                                    |
| asyncio_websockets       | 520 ms                                                                                                            | 516 ms: 1.01x faster                                                                                                    |
| regex_v8                 | 24.6 ms                                                                                                           | 25.2 ms: 1.02x slower                                                                                                   |
| regex_dna                | 184 ms                                                                                                            | 189 ms: 1.03x slower                                                                                                    |
| unpickle_list            | 4.68 us                                                                                                           | 4.91 us: 1.05x slower                                                                                                   |
| json                     | 4.88 ms                                                                                                           | 5.46 ms: 1.12x slower                                                                                                   |
| unpickle                 | 13.3 us                                                                                                           | 14.9 us: 1.12x slower                                                                                                   |
| sqlite_synth             | 2.19 us                                                                                                           | 2.48 us: 1.13x slower                                                                                                   |
| xml_etree_iterparse      | 95.9 ms                                                                                                           | 110 ms: 1.14x slower                                                                                                    |
| bench_mp_pool            | 63.5 ms                                                                                                           | 72.6 ms: 1.14x slower                                                                                                   |
| asyncio_tcp              | 506 ms                                                                                                            | 584 ms: 1.15x slower                                                                                                    |
| json_loads               | 25.7 us                                                                                                           | 29.9 us: 1.16x slower                                                                                                   |
| asyncio_tcp_ssl          | 1.52 sec                                                                                                          | 1.84 sec: 1.21x slower                                                                                                  |
| scimark_fft              | 345 ms                                                                                                            | 418 ms: 1.21x slower                                                                                                    |
| pathlib                  | 18.1 ms                                                                                                           | 22.3 ms: 1.23x slower                                                                                                   |
| coverage                 | 81.1 ms                                                                                                           | 102 ms: 1.26x slower                                                                                                    |
| telco                    | 7.44 ms                                                                                                           | 9.36 ms: 1.26x slower                                                                                                   |
| scimark_sparse_mat_mult  | 4.73 ms                                                                                                           | 6.10 ms: 1.29x slower                                                                                                   |
| docutils                 | 2.61 sec                                                                                                          | 3.41 sec: 1.30x slower                                                                                                  |
| json_dumps               | 11.6 ms                                                                                                           | 15.2 ms: 1.31x slower                                                                                                   |
| coroutines               | 23.6 ms                                                                                                           | 31.2 ms: 1.32x slower                                                                                                   |
| mdp                      | 2.37 sec                                                                                                          | 3.16 sec: 1.33x slower                                                                                                  |
| xml_etree_generate       | 85.4 ms                                                                                                           | 114 ms: 1.33x slower                                                                                                    |
| pylint                   | 318 ms                                                                                                            | 424 ms: 1.34x slower                                                                                                    |
| async_generators         | 373 ms                                                                                                            | 499 ms: 1.34x slower                                                                                                    |
| dulwich_log              | 75.8 ms                                                                                                           | 104 ms: 1.37x slower                                                                                                    |
| meteor_contest           | 100 ms                                                                                                            | 138 ms: 1.37x slower                                                                                                    |
| python_startup_no_site   | 7.41 ms                                                                                                           | 10.3 ms: 1.38x slower                                                                                                   |
| bpe_tokeniser            | 4.35 sec                                                                                                          | 6.14 sec: 1.41x slower                                                                                                  |
| python_startup           | 11.0 ms                                                                                                           | 15.7 ms: 1.43x slower                                                                                                   |
| nqueens                  | 79.3 ms                                                                                                           | 115 ms: 1.44x slower                                                                                                    |
| spectral_norm            | 114 ms                                                                                                            | 166 ms: 1.46x slower                                                                                                    |
| generators               | 28.8 ms                                                                                                           | 42.5 ms: 1.48x slower                                                                                                   |
| fannkuch                 | 377 ms                                                                                                            | 565 ms: 1.50x slower                                                                                                    |
| pycparser                | 1.14 sec                                                                                                          | 1.74 sec: 1.53x slower                                                                                                  |
| tomli_loads              | 2.10 sec                                                                                                          | 3.22 sec: 1.53x slower                                                                                                  |
| typing_runtime_protocols | 159 us                                                                                                            | 251 us: 1.58x slower                                                                                                    |
| crypto_pyaes             | 67.8 ms                                                                                                           | 108 ms: 1.59x slower                                                                                                    |
| xml_etree_process        | 59.5 ms                                                                                                           | 94.9 ms: 1.60x slower                                                                                                   |
| html5lib                 | 66.5 ms                                                                                                           | 107 ms: 1.61x slower                                                                                                    |
| genshi_xml               | 50.9 ms                                                                                                           | 82.2 ms: 1.61x slower                                                                                                   |
| 2to3                     | 254 ms                                                                                                            | 417 ms: 1.64x slower                                                                                                    |
| deepcopy                 | 265 us                                                                                                            | 437 us: 1.65x slower                                                                                                    |
| sympy_integrate          | 20.0 ms                                                                                                           | 33.2 ms: 1.66x slower                                                                                                   |
| deepcopy_reduce          | 2.72 us                                                                                                           | 4.55 us: 1.67x slower                                                                                                   |
| sqlglot_optimize         | 53.8 ms                                                                                                           | 90.9 ms: 1.69x slower                                                                                                   |
| sqlglot_normalize        | 107 ms                                                                                                            | 181 ms: 1.69x slower                                                                                                    |
| mako                     | 12.0 ms                                                                                                           | 20.6 ms: 1.72x slower                                                                                                   |
| pyflate                  | 449 ms                                                                                                            | 775 ms: 1.72x slower                                                                                                    |
| thrift                   | 750 us                                                                                                            | 1.30 ms: 1.73x slower                                                                                                   |
| regex_compile            | 132 ms                                                                                                            | 233 ms: 1.77x slower                                                                                                    |
| deepcopy_memo            | 30.0 us                                                                                                           | 53.1 us: 1.77x slower                                                                                                   |
| genshi_text              | 22.6 ms                                                                                                           | 40.3 ms: 1.79x slower                                                                                                   |
| comprehensions           | 17.2 us                                                                                                           | 30.8 us: 1.79x slower                                                                                                   |
| django_template          | 35.2 ms                                                                                                           | 64.9 ms: 1.85x slower                                                                                                   |
| pprint_safe_repr         | 717 ms                                                                                                            | 1.33 sec: 1.85x slower                                                                                                  |
| pprint_pformat           | 1.48 sec                                                                                                          | 2.75 sec: 1.86x slower                                                                                                  |
| float                    | 79.7 ms                                                                                                           | 152 ms: 1.91x slower                                                                                                    |
| unpickle_pure_python     | 217 us                                                                                                            | 417 us: 1.92x slower                                                                                                    |
| richards                 | 47.0 ms                                                                                                           | 90.6 ms: 1.93x slower                                                                                                   |
| scimark_monte_carlo      | 65.4 ms                                                                                                           | 128 ms: 1.96x slower                                                                                                    |
| pickle_pure_python       | 317 us                                                                                                            | 627 us: 1.98x slower                                                                                                    |
| sympy_str                | 274 ms                                                                                                            | 543 ms: 1.98x slower                                                                                                    |
| logging_format           | 6.91 us                                                                                                           | 13.8 us: 1.99x slower                                                                                                   |
| scimark_sor              | 136 ms                                                                                                            | 275 ms: 2.01x slower                                                                                                    |
| logging_simple           | 6.22 us                                                                                                           | 12.6 us: 2.02x slower                                                                                                   |
| logging_silent           | 106 ns                                                                                                            | 214 ns: 2.02x slower                                                                                                    |
| hexiom                   | 6.07 ms                                                                                                           | 12.4 ms: 2.05x slower                                                                                                   |
| chaos                    | 59.3 ms                                                                                                           | 123 ms: 2.08x slower                                                                                                    |
| sqlglot_transpile        | 1.61 ms                                                                                                           | 3.34 ms: 2.08x slower                                                                                                   |
| richards_super           | 52.3 ms                                                                                                           | 111 ms: 2.11x slower                                                                                                    |
| scimark_lu               | 116 ms                                                                                                            | 248 ms: 2.14x slower                                                                                                    |
| nbody                    | 95.6 ms                                                                                                           | 205 ms: 2.15x slower                                                                                                    |
| sqlglot_parse            | 1.31 ms                                                                                                           | 2.87 ms: 2.19x slower                                                                                                   |
| sympy_expand             | 461 ms                                                                                                            | 1.06 sec: 2.29x slower                                                                                                  |
| raytrace                 | 266 ms                                                                                                            | 635 ms: 2.39x slower                                                                                                    |
| go                       | 122 ms                                                                                                            | 299 ms: 2.45x slower                                                                                                    |
| sympy_sum                | 153 ms                                                                                                            | 382 ms: 2.50x slower                                                                                                    |
| deltablue                | 3.28 ms                                                                                                           | 9.22 ms: 2.81x slower                                                                                                   |
| unpack_sequence          | 51.6 ns                                                                                                           | 153 ns: 2.96x slower                                                                                                    |
| bench_thread_pool        | 1.01 ms                                                                                                           | 3.49 ms: 3.45x slower                                                                                                   |
| Geometric mean           | (ref)                                                                                                             | 1.53x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_effbot

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.47x
- 95% likely to have a slowdown of 1.44x
- 99% likely to have a slowdown of 1.40x

# Memory
- memory change: 1.21x