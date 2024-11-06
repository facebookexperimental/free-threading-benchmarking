# Results vs. base

- fork: python
- ref: 83ba8c2bba834c0b92de
- machine: linux-x86_64
- commit hash: 83ba8c2
- commit date: 2024-11-05
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.30x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241105-3.14.0a1+-83ba8c2/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json | results/bm-20241105-3.14.0a1+-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 488 ms                                                                                                            | 704 ms: 1.44x slower                                                                                                    |
| docutils       | 4.21 sec                                                                                                          | 5.08 sec: 1.21x slower                                                                                                  |
| html5lib       | 97.6 ms                                                                                                           | 148 ms: 1.52x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.38x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | results/bm-20241105-3.14.0a1+-83ba8c2/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json | results/bm-20241105-3.14.0a1+-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json |
|--------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets | 998 ms                                                                                                            | 1.02 sec: 1.03x slower                                                                                                  |
| async_generators   | 684 ms                                                                                                            | 769 ms: 1.12x slower                                                                                                    |
| asyncio_tcp        | 912 ms                                                                                                            | 1.07 sec: 1.17x slower                                                                                                  |
| coroutines         | 34.7 ms                                                                                                           | 41.5 ms: 1.20x slower                                                                                                   |
| asyncio_tcp_ssl    | 2.75 sec                                                                                                          | 3.31 sec: 1.20x slower                                                                                                  |
| Geometric mean     | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241105-3.14.0a1+-83ba8c2/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json | results/bm-20241105-3.14.0a1+-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 236 ms                                                                                                            | 252 ms: 1.07x slower                                                                                                    |
| float          | 147 ms                                                                                                            | 230 ms: 1.56x slower                                                                                                    |
| nbody          | 199 ms                                                                                                            | 328 ms: 1.65x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.40x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241105-3.14.0a1+-83ba8c2/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json | results/bm-20241105-3.14.0a1+-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 5.43 ms                                                                                                           | 5.22 ms: 1.04x faster                                                                                                   |
| regex_dna      | 287 ms                                                                                                            | 303 ms: 1.06x slower                                                                                                    |
| regex_compile  | 206 ms                                                                                                            | 328 ms: 1.59x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241105-3.14.0a1+-83ba8c2/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json | results/bm-20241105-3.14.0a1+-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pickle_list          | 6.98 us                                                                                                           | 6.00 us: 1.16x faster                                                                                                   |
| pickle               | 17.1 us                                                                                                           | 16.1 us: 1.06x faster                                                                                                   |
| pickle_dict          | 44.6 us                                                                                                           | 46.4 us: 1.04x slower                                                                                                   |
| unpickle_list        | 7.84 us                                                                                                           | 8.17 us: 1.04x slower                                                                                                   |
| xml_etree_generate   | 144 ms                                                                                                            | 172 ms: 1.19x slower                                                                                                    |
| unpickle             | 21.9 us                                                                                                           | 26.6 us: 1.21x slower                                                                                                   |
| json_loads           | 37.7 us                                                                                                           | 48.5 us: 1.28x slower                                                                                                   |
| json_dumps           | 16.4 ms                                                                                                           | 21.5 ms: 1.31x slower                                                                                                   |
| xml_etree_process    | 97.7 ms                                                                                                           | 140 ms: 1.43x slower                                                                                                    |
| tomli_loads          | 3.06 sec                                                                                                          | 4.45 sec: 1.45x slower                                                                                                  |
| pickle_pure_python   | 533 us                                                                                                            | 907 us: 1.70x slower                                                                                                    |
| unpickle_pure_python | 339 us                                                                                                            | 622 us: 1.83x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.21x slower                                                                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241105-3.14.0a1+-83ba8c2/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json | results/bm-20241105-3.14.0a1+-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 15.7 ms                                                                                                           | 19.9 ms: 1.27x slower                                                                                                   |
| python_startup         | 22.0 ms                                                                                                           | 29.2 ms: 1.33x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.30x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241105-3.14.0a1+-83ba8c2/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json | results/bm-20241105-3.14.0a1+-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 58.9 ms                                                                                                           | 92.0 ms: 1.56x slower                                                                                                   |
| genshi_text     | 41.2 ms                                                                                                           | 67.2 ms: 1.63x slower                                                                                                   |
| genshi_xml      | 87.2 ms                                                                                                           | 147 ms: 1.69x slower                                                                                                    |
| mako            | 19.8 ms                                                                                                           | 33.8 ms: 1.70x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.64x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                | results/bm-20241105-3.14.0a1+-83ba8c2/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json | results/bm-20241105-3.14.0a1+-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool            | 77.7 ms                                                                                                           | 61.6 ms: 1.26x faster                                                                                                   |
| create_gc_cycles         | 2.52 ms                                                                                                           | 2.00 ms: 1.26x faster                                                                                                   |
| pickle_list              | 6.98 us                                                                                                           | 6.00 us: 1.16x faster                                                                                                   |
| gc_traversal             | 6.55 ms                                                                                                           | 6.13 ms: 1.07x faster                                                                                                   |
| pickle                   | 17.1 us                                                                                                           | 16.1 us: 1.06x faster                                                                                                   |
| regex_effbot             | 5.43 ms                                                                                                           | 5.22 ms: 1.04x faster                                                                                                   |
| asyncio_websockets       | 998 ms                                                                                                            | 1.02 sec: 1.03x slower                                                                                                  |
| pickle_dict              | 44.6 us                                                                                                           | 46.4 us: 1.04x slower                                                                                                   |
| unpickle_list            | 7.84 us                                                                                                           | 8.17 us: 1.04x slower                                                                                                   |
| regex_dna                | 287 ms                                                                                                            | 303 ms: 1.06x slower                                                                                                    |
| pidigits                 | 236 ms                                                                                                            | 252 ms: 1.07x slower                                                                                                    |
| async_generators         | 684 ms                                                                                                            | 769 ms: 1.12x slower                                                                                                    |
| asyncio_tcp              | 912 ms                                                                                                            | 1.07 sec: 1.17x slower                                                                                                  |
| sqlite_synth             | 3.98 us                                                                                                           | 4.74 us: 1.19x slower                                                                                                   |
| pylint                   | 511 ms                                                                                                            | 610 ms: 1.19x slower                                                                                                    |
| json                     | 7.17 ms                                                                                                           | 8.55 ms: 1.19x slower                                                                                                   |
| xml_etree_generate       | 144 ms                                                                                                            | 172 ms: 1.19x slower                                                                                                    |
| coroutines               | 34.7 ms                                                                                                           | 41.5 ms: 1.20x slower                                                                                                   |
| asyncio_tcp_ssl          | 2.75 sec                                                                                                          | 3.31 sec: 1.20x slower                                                                                                  |
| scimark_fft              | 510 ms                                                                                                            | 614 ms: 1.20x slower                                                                                                    |
| docutils                 | 4.21 sec                                                                                                          | 5.08 sec: 1.21x slower                                                                                                  |
| unpickle                 | 21.9 us                                                                                                           | 26.6 us: 1.21x slower                                                                                                   |
| mdp                      | 4.08 sec                                                                                                          | 4.99 sec: 1.22x slower                                                                                                  |
| scimark_sparse_mat_mult  | 7.74 ms                                                                                                           | 9.62 ms: 1.24x slower                                                                                                   |
| coverage                 | 116 ms                                                                                                            | 145 ms: 1.25x slower                                                                                                    |
| pathlib                  | 29.1 ms                                                                                                           | 36.6 ms: 1.26x slower                                                                                                   |
| pycparser                | 2.09 sec                                                                                                          | 2.63 sec: 1.26x slower                                                                                                  |
| python_startup_no_site   | 15.7 ms                                                                                                           | 19.9 ms: 1.27x slower                                                                                                   |
| json_loads               | 37.7 us                                                                                                           | 48.5 us: 1.28x slower                                                                                                   |
| bench_thread_pool        | 2.90 ms                                                                                                           | 3.74 ms: 1.29x slower                                                                                                   |
| spectral_norm            | 188 ms                                                                                                            | 244 ms: 1.30x slower                                                                                                    |
| json_dumps               | 16.4 ms                                                                                                           | 21.5 ms: 1.31x slower                                                                                                   |
| telco                    | 11.4 ms                                                                                                           | 15.2 ms: 1.33x slower                                                                                                   |
| python_startup           | 22.0 ms                                                                                                           | 29.2 ms: 1.33x slower                                                                                                   |
| dulwich_log              | 109 ms                                                                                                            | 146 ms: 1.35x slower                                                                                                    |
| fannkuch                 | 560 ms                                                                                                            | 761 ms: 1.36x slower                                                                                                    |
| sqlglot_normalize        | 191 ms                                                                                                            | 271 ms: 1.42x slower                                                                                                    |
| meteor_contest           | 154 ms                                                                                                            | 220 ms: 1.43x slower                                                                                                    |
| xml_etree_process        | 97.7 ms                                                                                                           | 140 ms: 1.43x slower                                                                                                    |
| 2to3                     | 488 ms                                                                                                            | 704 ms: 1.44x slower                                                                                                    |
| bpe_tokeniser            | 7.22 sec                                                                                                          | 10.5 sec: 1.45x slower                                                                                                  |
| tomli_loads              | 3.06 sec                                                                                                          | 4.45 sec: 1.45x slower                                                                                                  |
| typing_runtime_protocols | 259 us                                                                                                            | 385 us: 1.49x slower                                                                                                    |
| deepcopy_reduce          | 4.23 us                                                                                                           | 6.30 us: 1.49x slower                                                                                                   |
| generators               | 45.2 ms                                                                                                           | 67.3 ms: 1.49x slower                                                                                                   |
| deepcopy                 | 427 us                                                                                                            | 637 us: 1.49x slower                                                                                                    |
| sqlglot_optimize         | 93.8 ms                                                                                                           | 141 ms: 1.50x slower                                                                                                    |
| pyflate                  | 757 ms                                                                                                            | 1.14 sec: 1.50x slower                                                                                                  |
| html5lib                 | 97.6 ms                                                                                                           | 148 ms: 1.52x slower                                                                                                    |
| crypto_pyaes             | 104 ms                                                                                                            | 158 ms: 1.52x slower                                                                                                    |
| nqueens                  | 117 ms                                                                                                            | 181 ms: 1.54x slower                                                                                                    |
| django_template          | 58.9 ms                                                                                                           | 92.0 ms: 1.56x slower                                                                                                   |
| float                    | 147 ms                                                                                                            | 230 ms: 1.56x slower                                                                                                    |
| sympy_integrate          | 30.3 ms                                                                                                           | 47.3 ms: 1.56x slower                                                                                                   |
| pprint_pformat           | 2.28 sec                                                                                                          | 3.58 sec: 1.57x slower                                                                                                  |
| regex_compile            | 206 ms                                                                                                            | 328 ms: 1.59x slower                                                                                                    |
| thrift                   | 1.20 ms                                                                                                           | 1.93 ms: 1.60x slower                                                                                                   |
| comprehensions           | 28.4 us                                                                                                           | 45.7 us: 1.61x slower                                                                                                   |
| scimark_monte_carlo      | 101 ms                                                                                                            | 164 ms: 1.61x slower                                                                                                    |
| genshi_text              | 41.2 ms                                                                                                           | 67.2 ms: 1.63x slower                                                                                                   |
| richards_super           | 87.5 ms                                                                                                           | 144 ms: 1.64x slower                                                                                                    |
| logging_silent           | 165 ns                                                                                                            | 272 ns: 1.65x slower                                                                                                    |
| nbody                    | 199 ms                                                                                                            | 328 ms: 1.65x slower                                                                                                    |
| deepcopy_memo            | 49.2 us                                                                                                           | 81.5 us: 1.66x slower                                                                                                   |
| logging_simple           | 10.1 us                                                                                                           | 16.9 us: 1.68x slower                                                                                                   |
| genshi_xml               | 87.2 ms                                                                                                           | 147 ms: 1.69x slower                                                                                                    |
| pickle_pure_python       | 533 us                                                                                                            | 907 us: 1.70x slower                                                                                                    |
| mako                     | 19.8 ms                                                                                                           | 33.8 ms: 1.70x slower                                                                                                   |
| pprint_safe_repr         | 1.04 sec                                                                                                          | 1.78 sec: 1.70x slower                                                                                                  |
| scimark_sor              | 209 ms                                                                                                            | 358 ms: 1.71x slower                                                                                                    |
| richards                 | 73.1 ms                                                                                                           | 127 ms: 1.73x slower                                                                                                    |
| sympy_str                | 408 ms                                                                                                            | 721 ms: 1.76x slower                                                                                                    |
| logging_format           | 10.8 us                                                                                                           | 19.5 us: 1.80x slower                                                                                                   |
| hexiom                   | 9.80 ms                                                                                                           | 17.9 ms: 1.83x slower                                                                                                   |
| unpickle_pure_python     | 339 us                                                                                                            | 622 us: 1.83x slower                                                                                                    |
| chaos                    | 95.4 ms                                                                                                           | 176 ms: 1.85x slower                                                                                                    |
| raytrace                 | 465 ms                                                                                                            | 872 ms: 1.88x slower                                                                                                    |
| sympy_expand             | 698 ms                                                                                                            | 1.33 sec: 1.91x slower                                                                                                  |
| sympy_sum                | 247 ms                                                                                                            | 476 ms: 1.93x slower                                                                                                    |
| scimark_lu               | 169 ms                                                                                                            | 326 ms: 1.93x slower                                                                                                    |
| sqlglot_transpile        | 2.55 ms                                                                                                           | 5.25 ms: 2.06x slower                                                                                                   |
| sqlglot_parse            | 2.10 ms                                                                                                           | 4.35 ms: 2.07x slower                                                                                                   |
| go                       | 198 ms                                                                                                            | 409 ms: 2.07x slower                                                                                                    |
| deltablue                | 5.74 ms                                                                                                           | 12.8 ms: 2.23x slower                                                                                                   |
| unpack_sequence          | 70.7 ns                                                                                                           | 227 ns: 3.21x slower                                                                                                    |
| Geometric mean           | (ref)                                                                                                             | 1.41x slower                                                                                                            |

Benchmark hidden because not significant (3): regex_v8, xml_etree_parse, xml_etree_iterparse

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.34x
- 99% likely to have a slowdown of 1.30x

# Memory
- memory change: 1.18x