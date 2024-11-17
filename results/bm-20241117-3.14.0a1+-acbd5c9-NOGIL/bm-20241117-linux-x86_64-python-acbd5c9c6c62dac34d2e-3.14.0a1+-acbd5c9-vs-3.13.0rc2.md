# Results vs. 3.13.0rc2

- fork: python
- ref: acbd5c9c6c62dac34d2e
- machine: linux-x86_64
- commit hash: acbd5c9
- commit date: 2024-11-17
- overall geometric mean: 1.43x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.34x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 653 ms: 1.47x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.64 sec: 1.16x slower                                                 |
| html5lib       | 92.6 ms                                                      | 137 ms: 1.48x slower                                                   |
| Geometric mean | (ref)                                                        | 1.36x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|--------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 766 ms                                                       | 721 ms: 1.06x faster                                                   |
| asyncio_tcp        | 948 ms                                                       | 1.05 sec: 1.10x slower                                                 |
| asyncio_tcp_ssl    | 2.77 sec                                                     | 3.29 sec: 1.18x slower                                                 |
| async_generators   | 567 ms                                                       | 696 ms: 1.23x slower                                                   |
| coroutines         | 30.9 ms                                                      | 39.9 ms: 1.29x slower                                                  |
| Geometric mean     | (ref)                                                        | 1.14x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 182 ms: 1.57x slower                                                   |
| nbody          | 119 ms                                                       | 261 ms: 2.20x slower                                                   |
| Geometric mean | (ref)                                                        | 1.51x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 34.5 ms: 1.05x slower                                                  |
| regex_dna      | 282 ms                                                       | 307 ms: 1.09x slower                                                   |
| regex_compile  | 182 ms                                                       | 271 ms: 1.49x slower                                                   |
| Geometric mean | (ref)                                                        | 1.14x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 159 ms: 1.11x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 211 ms: 1.09x faster                                                   |
| pickle               | 15.1 us                                                      | 15.9 us: 1.05x slower                                                  |
| json_loads           | 34.3 us                                                      | 38.3 us: 1.12x slower                                                  |
| unpickle_list        | 6.68 us                                                      | 7.52 us: 1.13x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 163 ms: 1.33x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 19.5 ms: 1.38x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 125 ms: 1.46x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 4.08 sec: 1.47x slower                                                 |
| unpickle_pure_python | 290 us                                                       | 553 us: 1.91x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 811 us: 1.95x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.22x slower                                                           |

Benchmark hidden because not significant (3): pickle_dict, pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.0 ms: 1.24x slower                                                  |
| python_startup         | 22.4 ms                                                      | 27.9 ms: 1.25x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 121 ms: 1.68x slower                                                   |
| genshi_text     | 31.7 ms                                                      | 55.5 ms: 1.75x slower                                                  |
| mako            | 15.9 ms                                                      | 30.1 ms: 1.89x slower                                                  |
| django_template | 44.3 ms                                                      | 85.2 ms: 1.92x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.81x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 5.70 ms                                                      | 3.88 ms: 1.47x faster                                                  |
| create_gc_cycles         | 2.41 ms                                                      | 1.96 ms: 1.23x faster                                                  |
| xml_etree_iterparse      | 177 ms                                                       | 159 ms: 1.11x faster                                                   |
| xml_etree_parse          | 231 ms                                                       | 211 ms: 1.09x faster                                                   |
| asyncio_websockets       | 766 ms                                                       | 721 ms: 1.06x faster                                                   |
| regex_v8                 | 32.8 ms                                                      | 34.5 ms: 1.05x slower                                                  |
| pickle                   | 15.1 us                                                      | 15.9 us: 1.05x slower                                                  |
| regex_dna                | 282 ms                                                       | 307 ms: 1.09x slower                                                   |
| asyncio_tcp              | 948 ms                                                       | 1.05 sec: 1.10x slower                                                 |
| bench_thread_pool        | 2.89 ms                                                      | 3.20 ms: 1.11x slower                                                  |
| pathlib                  | 29.9 ms                                                      | 33.2 ms: 1.11x slower                                                  |
| deepcopy                 | 498 us                                                       | 556 us: 1.12x slower                                                   |
| json_loads               | 34.3 us                                                      | 38.3 us: 1.12x slower                                                  |
| unpickle_list            | 6.68 us                                                      | 7.52 us: 1.13x slower                                                  |
| telco                    | 12.2 ms                                                      | 13.7 ms: 1.13x slower                                                  |
| json                     | 6.51 ms                                                      | 7.37 ms: 1.13x slower                                                  |
| docutils                 | 4.01 sec                                                     | 4.64 sec: 1.16x slower                                                 |
| scimark_fft              | 473 ms                                                       | 555 ms: 1.17x slower                                                   |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.29 sec: 1.18x slower                                                 |
| pylint                   | 470 ms                                                       | 561 ms: 1.19x slower                                                   |
| async_generators         | 567 ms                                                       | 696 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 8.31 ms: 1.23x slower                                                  |
| python_startup_no_site   | 15.3 ms                                                      | 19.0 ms: 1.24x slower                                                  |
| meteor_contest           | 150 ms                                                       | 186 ms: 1.24x slower                                                   |
| python_startup           | 22.4 ms                                                      | 27.9 ms: 1.25x slower                                                  |
| mdp                      | 3.80 sec                                                     | 4.88 sec: 1.28x slower                                                 |
| coroutines               | 30.9 ms                                                      | 39.9 ms: 1.29x slower                                                  |
| generators               | 40.0 ms                                                      | 53.0 ms: 1.32x slower                                                  |
| pycparser                | 1.57 sec                                                     | 2.08 sec: 1.33x slower                                                 |
| xml_etree_generate       | 122 ms                                                       | 163 ms: 1.33x slower                                                   |
| coverage                 | 107 ms                                                       | 144 ms: 1.34x slower                                                   |
| json_dumps               | 14.1 ms                                                      | 19.5 ms: 1.38x slower                                                  |
| deepcopy_memo            | 50.1 us                                                      | 69.3 us: 1.38x slower                                                  |
| fannkuch                 | 547 ms                                                       | 760 ms: 1.39x slower                                                   |
| bpe_tokeniser            | 6.28 sec                                                     | 8.82 sec: 1.40x slower                                                 |
| crypto_pyaes             | 100 ms                                                       | 143 ms: 1.42x slower                                                   |
| nqueens                  | 112 ms                                                       | 159 ms: 1.43x slower                                                   |
| dulwich_log              | 93.7 ms                                                      | 135 ms: 1.44x slower                                                   |
| sympy_integrate          | 30.2 ms                                                      | 43.8 ms: 1.45x slower                                                  |
| xml_etree_process        | 85.9 ms                                                      | 125 ms: 1.46x slower                                                   |
| typing_runtime_protocols | 226 us                                                       | 331 us: 1.47x slower                                                   |
| 2to3                     | 445 ms                                                       | 653 ms: 1.47x slower                                                   |
| tomli_loads              | 2.78 sec                                                     | 4.08 sec: 1.47x slower                                                 |
| html5lib                 | 92.6 ms                                                      | 137 ms: 1.48x slower                                                   |
| regex_compile            | 182 ms                                                       | 271 ms: 1.49x slower                                                   |
| spectral_norm            | 157 ms                                                       | 234 ms: 1.50x slower                                                   |
| deepcopy_reduce          | 4.10 us                                                      | 6.17 us: 1.50x slower                                                  |
| richards                 | 65.5 ms                                                      | 103 ms: 1.57x slower                                                   |
| float                    | 116 ms                                                       | 182 ms: 1.57x slower                                                   |
| pyflate                  | 664 ms                                                       | 1.06 sec: 1.59x slower                                                 |
| thrift                   | 1.10 ms                                                      | 1.75 ms: 1.59x slower                                                  |
| sqlglot_optimize         | 74.7 ms                                                      | 121 ms: 1.62x slower                                                   |
| sqlglot_normalize        | 140 ms                                                       | 227 ms: 1.63x slower                                                   |
| richards_super           | 73.2 ms                                                      | 123 ms: 1.67x slower                                                   |
| pprint_safe_repr         | 987 ms                                                       | 1.66 sec: 1.68x slower                                                 |
| genshi_xml               | 72.1 ms                                                      | 121 ms: 1.68x slower                                                   |
| pprint_pformat           | 1.94 sec                                                     | 3.28 sec: 1.69x slower                                                 |
| sympy_str                | 379 ms                                                       | 650 ms: 1.72x slower                                                   |
| comprehensions           | 22.2 us                                                      | 38.2 us: 1.72x slower                                                  |
| scimark_monte_carlo      | 90.6 ms                                                      | 158 ms: 1.74x slower                                                   |
| genshi_text              | 31.7 ms                                                      | 55.5 ms: 1.75x slower                                                  |
| logging_simple           | 8.56 us                                                      | 15.3 us: 1.79x slower                                                  |
| go                       | 191 ms                                                       | 344 ms: 1.80x slower                                                   |
| chaos                    | 83.6 ms                                                      | 151 ms: 1.80x slower                                                   |
| logging_format           | 9.24 us                                                      | 17.1 us: 1.85x slower                                                  |
| scimark_sor              | 179 ms                                                       | 337 ms: 1.89x slower                                                   |
| mako                     | 15.9 ms                                                      | 30.1 ms: 1.89x slower                                                  |
| unpickle_pure_python     | 290 us                                                       | 553 us: 1.91x slower                                                   |
| django_template          | 44.3 ms                                                      | 85.2 ms: 1.92x slower                                                  |
| pickle_pure_python       | 416 us                                                       | 811 us: 1.95x slower                                                   |
| hexiom                   | 8.11 ms                                                      | 15.8 ms: 1.95x slower                                                  |
| logging_silent           | 130 ns                                                       | 257 ns: 1.98x slower                                                   |
| scimark_lu               | 146 ms                                                       | 292 ms: 2.00x slower                                                   |
| sympy_expand             | 601 ms                                                       | 1.22 sec: 2.02x slower                                                 |
| sqlglot_transpile        | 2.20 ms                                                      | 4.51 ms: 2.05x slower                                                  |
| raytrace                 | 344 ms                                                       | 736 ms: 2.14x slower                                                   |
| sympy_sum                | 210 ms                                                       | 453 ms: 2.15x slower                                                   |
| sqlglot_parse            | 1.76 ms                                                      | 3.79 ms: 2.16x slower                                                  |
| nbody                    | 119 ms                                                       | 261 ms: 2.20x slower                                                   |
| unpack_sequence          | 74.3 ns                                                      | 190 ns: 2.55x slower                                                   |
| deltablue                | 4.44 ms                                                      | 11.4 ms: 2.58x slower                                                  |
| bench_mp_pool            | 18.7 ms                                                      | 58.0 ms: 3.11x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.43x slower                                                           |

Benchmark hidden because not significant (6): pickle_dict, pickle_list, pidigits, regex_effbot, unpickle, sqlite_synth
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.38x
- 95% likely to have a slowdown of 1.37x
- 99% likely to have a slowdown of 1.34x

# Memory
- memory change: 1.19x