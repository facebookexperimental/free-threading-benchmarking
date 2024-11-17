# Results vs. base

- fork: python
- ref: acbd5c9c6c62dac34d2e
- machine: linux-x86_64
- commit hash: acbd5c9
- commit date: 2024-11-17
- overall geometric mean: 1.42x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.33x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241117-3.14.0a1+-acbd5c9/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json | results/bm-20241117-3.14.0a1+-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 432 ms                                                                                                            | 653 ms: 1.51x slower                                                                                                    |
| docutils       | 3.90 sec                                                                                                          | 4.64 sec: 1.19x slower                                                                                                  |
| html5lib       | 87.7 ms                                                                                                           | 137 ms: 1.56x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.41x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | results/bm-20241117-3.14.0a1+-acbd5c9/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json | results/bm-20241117-3.14.0a1+-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json |
|--------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets | 755 ms                                                                                                            | 721 ms: 1.05x faster                                                                                                    |
| async_generators   | 616 ms                                                                                                            | 696 ms: 1.13x slower                                                                                                    |
| asyncio_tcp        | 909 ms                                                                                                            | 1.05 sec: 1.15x slower                                                                                                  |
| asyncio_tcp_ssl    | 2.82 sec                                                                                                          | 3.29 sec: 1.16x slower                                                                                                  |
| coroutines         | 32.1 ms                                                                                                           | 39.9 ms: 1.24x slower                                                                                                   |
| Geometric mean     | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241117-3.14.0a1+-acbd5c9/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json | results/bm-20241117-3.14.0a1+-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 234 ms                                                                                                            | 249 ms: 1.07x slower                                                                                                    |
| float          | 115 ms                                                                                                            | 182 ms: 1.58x slower                                                                                                    |
| nbody          | 132 ms                                                                                                            | 261 ms: 1.98x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.50x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241117-3.14.0a1+-acbd5c9/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json | results/bm-20241117-3.14.0a1+-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 293 ms                                                                                                            | 307 ms: 1.05x slower                                                                                                    |
| regex_compile  | 173 ms                                                                                                            | 271 ms: 1.57x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241117-3.14.0a1+-acbd5c9/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json | results/bm-20241117-3.14.0a1+-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 241 ms                                                                                                            | 211 ms: 1.14x faster                                                                                                    |
| pickle_list          | 7.19 us                                                                                                           | 6.80 us: 1.06x faster                                                                                                   |
| unpickle_list        | 7.19 us                                                                                                           | 7.52 us: 1.05x slower                                                                                                   |
| json_loads           | 34.0 us                                                                                                           | 38.3 us: 1.12x slower                                                                                                   |
| json_dumps           | 15.8 ms                                                                                                           | 19.5 ms: 1.23x slower                                                                                                   |
| xml_etree_generate   | 125 ms                                                                                                            | 163 ms: 1.30x slower                                                                                                    |
| xml_etree_process    | 86.9 ms                                                                                                           | 125 ms: 1.44x slower                                                                                                    |
| tomli_loads          | 2.73 sec                                                                                                          | 4.08 sec: 1.49x slower                                                                                                  |
| unpickle_pure_python | 310 us                                                                                                            | 553 us: 1.79x slower                                                                                                    |
| pickle_pure_python   | 439 us                                                                                                            | 811 us: 1.85x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmark hidden because not significant (4): xml_etree_iterparse, pickle, pickle_dict, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241117-3.14.0a1+-acbd5c9/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json | results/bm-20241117-3.14.0a1+-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 21.0 ms                                                                                                           | 27.9 ms: 1.33x slower                                                                                                   |
| python_startup_no_site | 14.0 ms                                                                                                           | 19.0 ms: 1.36x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.34x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241117-3.14.0a1+-acbd5c9/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json | results/bm-20241117-3.14.0a1+-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| mako            | 16.9 ms                                                                                                           | 30.1 ms: 1.78x slower                                                                                                   |
| genshi_xml      | 67.6 ms                                                                                                           | 121 ms: 1.80x slower                                                                                                    |
| django_template | 47.3 ms                                                                                                           | 85.2 ms: 1.80x slower                                                                                                   |
| genshi_text     | 30.4 ms                                                                                                           | 55.5 ms: 1.83x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.80x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                | results/bm-20241117-3.14.0a1+-acbd5c9/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json | results/bm-20241117-3.14.0a1+-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal             | 5.78 ms                                                                                                           | 3.88 ms: 1.49x faster                                                                                                   |
| bench_mp_pool            | 72.4 ms                                                                                                           | 58.0 ms: 1.25x faster                                                                                                   |
| create_gc_cycles         | 2.44 ms                                                                                                           | 1.96 ms: 1.24x faster                                                                                                   |
| xml_etree_parse          | 241 ms                                                                                                            | 211 ms: 1.14x faster                                                                                                    |
| pickle_list              | 7.19 us                                                                                                           | 6.80 us: 1.06x faster                                                                                                   |
| asyncio_websockets       | 755 ms                                                                                                            | 721 ms: 1.05x faster                                                                                                    |
| regex_dna                | 293 ms                                                                                                            | 307 ms: 1.05x slower                                                                                                    |
| unpickle_list            | 7.19 us                                                                                                           | 7.52 us: 1.05x slower                                                                                                   |
| pidigits                 | 234 ms                                                                                                            | 249 ms: 1.07x slower                                                                                                    |
| json                     | 6.65 ms                                                                                                           | 7.37 ms: 1.11x slower                                                                                                   |
| json_loads               | 34.0 us                                                                                                           | 38.3 us: 1.12x slower                                                                                                   |
| async_generators         | 616 ms                                                                                                            | 696 ms: 1.13x slower                                                                                                    |
| asyncio_tcp              | 909 ms                                                                                                            | 1.05 sec: 1.15x slower                                                                                                  |
| asyncio_tcp_ssl          | 2.82 sec                                                                                                          | 3.29 sec: 1.16x slower                                                                                                  |
| scimark_fft              | 475 ms                                                                                                            | 555 ms: 1.17x slower                                                                                                    |
| docutils                 | 3.90 sec                                                                                                          | 4.64 sec: 1.19x slower                                                                                                  |
| meteor_contest           | 154 ms                                                                                                            | 186 ms: 1.21x slower                                                                                                    |
| pylint                   | 462 ms                                                                                                            | 561 ms: 1.22x slower                                                                                                    |
| coverage                 | 117 ms                                                                                                            | 144 ms: 1.23x slower                                                                                                    |
| pathlib                  | 26.9 ms                                                                                                           | 33.2 ms: 1.23x slower                                                                                                   |
| json_dumps               | 15.8 ms                                                                                                           | 19.5 ms: 1.23x slower                                                                                                   |
| generators               | 42.6 ms                                                                                                           | 53.0 ms: 1.24x slower                                                                                                   |
| coroutines               | 32.1 ms                                                                                                           | 39.9 ms: 1.24x slower                                                                                                   |
| telco                    | 10.8 ms                                                                                                           | 13.7 ms: 1.27x slower                                                                                                   |
| xml_etree_generate       | 125 ms                                                                                                            | 163 ms: 1.30x slower                                                                                                    |
| python_startup           | 21.0 ms                                                                                                           | 27.9 ms: 1.33x slower                                                                                                   |
| scimark_sparse_mat_mult  | 6.19 ms                                                                                                           | 8.31 ms: 1.34x slower                                                                                                   |
| dulwich_log              | 101 ms                                                                                                            | 135 ms: 1.35x slower                                                                                                    |
| crypto_pyaes             | 105 ms                                                                                                            | 143 ms: 1.35x slower                                                                                                    |
| pycparser                | 1.54 sec                                                                                                          | 2.08 sec: 1.35x slower                                                                                                  |
| python_startup_no_site   | 14.0 ms                                                                                                           | 19.0 ms: 1.36x slower                                                                                                   |
| mdp                      | 3.52 sec                                                                                                          | 4.88 sec: 1.39x slower                                                                                                  |
| deepcopy                 | 388 us                                                                                                            | 556 us: 1.43x slower                                                                                                    |
| fannkuch                 | 530 ms                                                                                                            | 760 ms: 1.43x slower                                                                                                    |
| xml_etree_process        | 86.9 ms                                                                                                           | 125 ms: 1.44x slower                                                                                                    |
| bpe_tokeniser            | 5.98 sec                                                                                                          | 8.82 sec: 1.47x slower                                                                                                  |
| tomli_loads              | 2.73 sec                                                                                                          | 4.08 sec: 1.49x slower                                                                                                  |
| nqueens                  | 106 ms                                                                                                            | 159 ms: 1.51x slower                                                                                                    |
| 2to3                     | 432 ms                                                                                                            | 653 ms: 1.51x slower                                                                                                    |
| spectral_norm            | 153 ms                                                                                                            | 234 ms: 1.53x slower                                                                                                    |
| typing_runtime_protocols | 215 us                                                                                                            | 331 us: 1.54x slower                                                                                                    |
| sympy_integrate          | 28.2 ms                                                                                                           | 43.8 ms: 1.55x slower                                                                                                   |
| html5lib                 | 87.7 ms                                                                                                           | 137 ms: 1.56x slower                                                                                                    |
| pyflate                  | 676 ms                                                                                                            | 1.06 sec: 1.56x slower                                                                                                  |
| regex_compile            | 173 ms                                                                                                            | 271 ms: 1.57x slower                                                                                                    |
| float                    | 115 ms                                                                                                            | 182 ms: 1.58x slower                                                                                                    |
| sqlglot_normalize        | 143 ms                                                                                                            | 227 ms: 1.59x slower                                                                                                    |
| deepcopy_reduce          | 3.87 us                                                                                                           | 6.17 us: 1.59x slower                                                                                                   |
| richards                 | 63.8 ms                                                                                                           | 103 ms: 1.61x slower                                                                                                    |
| deepcopy_memo            | 42.8 us                                                                                                           | 69.3 us: 1.62x slower                                                                                                   |
| comprehensions           | 22.9 us                                                                                                           | 38.2 us: 1.67x slower                                                                                                   |
| richards_super           | 73.5 ms                                                                                                           | 123 ms: 1.67x slower                                                                                                    |
| sqlglot_optimize         | 71.3 ms                                                                                                           | 121 ms: 1.70x slower                                                                                                    |
| scimark_monte_carlo      | 92.7 ms                                                                                                           | 158 ms: 1.70x slower                                                                                                    |
| pprint_pformat           | 1.88 sec                                                                                                          | 3.28 sec: 1.74x slower                                                                                                  |
| sympy_str                | 374 ms                                                                                                            | 650 ms: 1.74x slower                                                                                                    |
| logging_simple           | 8.82 us                                                                                                           | 15.3 us: 1.74x slower                                                                                                   |
| thrift                   | 1.00 ms                                                                                                           | 1.75 ms: 1.74x slower                                                                                                   |
| chaos                    | 85.5 ms                                                                                                           | 151 ms: 1.76x slower                                                                                                    |
| mako                     | 16.9 ms                                                                                                           | 30.1 ms: 1.78x slower                                                                                                   |
| unpickle_pure_python     | 310 us                                                                                                            | 553 us: 1.79x slower                                                                                                    |
| pprint_safe_repr         | 926 ms                                                                                                            | 1.66 sec: 1.79x slower                                                                                                  |
| genshi_xml               | 67.6 ms                                                                                                           | 121 ms: 1.80x slower                                                                                                    |
| logging_silent           | 143 ns                                                                                                            | 257 ns: 1.80x slower                                                                                                    |
| django_template          | 47.3 ms                                                                                                           | 85.2 ms: 1.80x slower                                                                                                   |
| genshi_text              | 30.4 ms                                                                                                           | 55.5 ms: 1.83x slower                                                                                                   |
| pickle_pure_python       | 439 us                                                                                                            | 811 us: 1.85x slower                                                                                                    |
| hexiom                   | 8.54 ms                                                                                                           | 15.8 ms: 1.85x slower                                                                                                   |
| sqlglot_transpile        | 2.38 ms                                                                                                           | 4.51 ms: 1.89x slower                                                                                                   |
| logging_format           | 9.00 us                                                                                                           | 17.1 us: 1.90x slower                                                                                                   |
| scimark_lu               | 149 ms                                                                                                            | 292 ms: 1.96x slower                                                                                                    |
| nbody                    | 132 ms                                                                                                            | 261 ms: 1.98x slower                                                                                                    |
| scimark_sor              | 169 ms                                                                                                            | 337 ms: 1.99x slower                                                                                                    |
| sympy_expand             | 605 ms                                                                                                            | 1.22 sec: 2.01x slower                                                                                                  |
| sqlglot_parse            | 1.87 ms                                                                                                           | 3.79 ms: 2.03x slower                                                                                                   |
| raytrace                 | 354 ms                                                                                                            | 736 ms: 2.08x slower                                                                                                    |
| go                       | 162 ms                                                                                                            | 344 ms: 2.12x slower                                                                                                    |
| sympy_sum                | 208 ms                                                                                                            | 453 ms: 2.18x slower                                                                                                    |
| deltablue                | 4.77 ms                                                                                                           | 11.4 ms: 2.40x slower                                                                                                   |
| unpack_sequence          | 63.1 ns                                                                                                           | 190 ns: 3.00x slower                                                                                                    |
| Geometric mean           | (ref)                                                                                                             | 1.42x slower                                                                                                            |

Benchmark hidden because not significant (8): xml_etree_iterparse, bench_thread_pool, regex_effbot, regex_v8, pickle, pickle_dict, unpickle, sqlite_synth

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.39x
- 95% likely to have a slowdown of 1.36x
- 99% likely to have a slowdown of 1.33x

# Memory
- memory change: 1.18x