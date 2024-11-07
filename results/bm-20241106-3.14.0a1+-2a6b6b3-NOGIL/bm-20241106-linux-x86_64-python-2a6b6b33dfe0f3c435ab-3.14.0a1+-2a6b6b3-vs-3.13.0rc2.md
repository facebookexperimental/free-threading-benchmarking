# Results vs. 3.13.0rc2

- fork: python
- ref: 2a6b6b33dfe0f3c435ab
- machine: linux-x86_64
- commit hash: 2a6b6b3
- commit date: 2024-11-06
- overall geometric mean: 1.44x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.34x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 659 ms: 1.48x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.71 sec: 1.18x slower                                                 |
| html5lib       | 92.6 ms                                                      | 130 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                        | 1.35x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 766 ms                                                       | 741 ms: 1.03x faster                                                   |
| asyncio_tcp        | 948 ms                                                       | 1.02 sec: 1.08x slower                                                 |
| asyncio_tcp_ssl    | 2.77 sec                                                     | 3.30 sec: 1.19x slower                                                 |
| async_generators   | 567 ms                                                       | 723 ms: 1.28x slower                                                   |
| coroutines         | 30.9 ms                                                      | 41.8 ms: 1.36x slower                                                  |
| Geometric mean     | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 186 ms: 1.60x slower                                                   |
| nbody          | 119 ms                                                       | 263 ms: 2.21x slower                                                   |
| Geometric mean | (ref)                                                        | 1.53x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 297 ms: 1.05x slower                                                   |
| regex_v8       | 32.8 ms                                                      | 36.2 ms: 1.10x slower                                                  |
| regex_compile  | 182 ms                                                       | 288 ms: 1.58x slower                                                   |
| Geometric mean | (ref)                                                        | 1.17x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_list          | 6.86 us                                                      | 5.87 us: 1.17x faster                                                  |
| xml_etree_iterparse  | 177 ms                                                       | 161 ms: 1.10x faster                                                   |
| pickle               | 15.1 us                                                      | 13.9 us: 1.09x faster                                                  |
| xml_etree_parse      | 231 ms                                                       | 216 ms: 1.07x faster                                                   |
| pickle_dict          | 47.2 us                                                      | 45.6 us: 1.04x faster                                                  |
| unpickle_list        | 6.68 us                                                      | 7.39 us: 1.11x slower                                                  |
| unpickle             | 20.5 us                                                      | 23.3 us: 1.13x slower                                                  |
| json_loads           | 34.3 us                                                      | 41.5 us: 1.21x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 156 ms: 1.27x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 19.5 ms: 1.38x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 4.11 sec: 1.48x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 133 ms: 1.54x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 520 us: 1.79x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 797 us: 1.91x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.20x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 27.5 ms: 1.23x slower                                                  |
| python_startup_no_site | 15.3 ms                                                      | 18.9 ms: 1.23x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.23x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 119 ms: 1.66x slower                                                   |
| genshi_text     | 31.7 ms                                                      | 55.5 ms: 1.75x slower                                                  |
| django_template | 44.3 ms                                                      | 79.1 ms: 1.79x slower                                                  |
| mako            | 15.9 ms                                                      | 29.1 ms: 1.83x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.75x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 5.70 ms                                                      | 4.11 ms: 1.39x faster                                                  |
| create_gc_cycles         | 2.41 ms                                                      | 1.85 ms: 1.30x faster                                                  |
| pickle_list              | 6.86 us                                                      | 5.87 us: 1.17x faster                                                  |
| xml_etree_iterparse      | 177 ms                                                       | 161 ms: 1.10x faster                                                   |
| pickle                   | 15.1 us                                                      | 13.9 us: 1.09x faster                                                  |
| xml_etree_parse          | 231 ms                                                       | 216 ms: 1.07x faster                                                   |
| pickle_dict              | 47.2 us                                                      | 45.6 us: 1.04x faster                                                  |
| asyncio_websockets       | 766 ms                                                       | 741 ms: 1.03x faster                                                   |
| pathlib                  | 29.9 ms                                                      | 31.3 ms: 1.05x slower                                                  |
| regex_dna                | 282 ms                                                       | 297 ms: 1.05x slower                                                   |
| sqlite_synth             | 3.99 us                                                      | 4.23 us: 1.06x slower                                                  |
| asyncio_tcp              | 948 ms                                                       | 1.02 sec: 1.08x slower                                                 |
| telco                    | 12.2 ms                                                      | 13.3 ms: 1.10x slower                                                  |
| regex_v8                 | 32.8 ms                                                      | 36.2 ms: 1.10x slower                                                  |
| unpickle_list            | 6.68 us                                                      | 7.39 us: 1.11x slower                                                  |
| deepcopy                 | 498 us                                                       | 555 us: 1.12x slower                                                   |
| unpickle                 | 20.5 us                                                      | 23.3 us: 1.13x slower                                                  |
| bench_thread_pool        | 2.89 ms                                                      | 3.34 ms: 1.16x slower                                                  |
| docutils                 | 4.01 sec                                                     | 4.71 sec: 1.18x slower                                                 |
| scimark_fft              | 473 ms                                                       | 562 ms: 1.19x slower                                                   |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.30 sec: 1.19x slower                                                 |
| json_loads               | 34.3 us                                                      | 41.5 us: 1.21x slower                                                  |
| pylint                   | 470 ms                                                       | 576 ms: 1.23x slower                                                   |
| python_startup           | 22.4 ms                                                      | 27.5 ms: 1.23x slower                                                  |
| python_startup_no_site   | 15.3 ms                                                      | 18.9 ms: 1.23x slower                                                  |
| mdp                      | 3.80 sec                                                     | 4.71 sec: 1.24x slower                                                 |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 8.50 ms: 1.26x slower                                                  |
| xml_etree_generate       | 122 ms                                                       | 156 ms: 1.27x slower                                                   |
| async_generators         | 567 ms                                                       | 723 ms: 1.28x slower                                                   |
| meteor_contest           | 150 ms                                                       | 192 ms: 1.28x slower                                                   |
| pycparser                | 1.57 sec                                                     | 2.06 sec: 1.31x slower                                                 |
| json                     | 6.51 ms                                                      | 8.70 ms: 1.34x slower                                                  |
| generators               | 40.0 ms                                                      | 53.6 ms: 1.34x slower                                                  |
| coverage                 | 107 ms                                                       | 145 ms: 1.35x slower                                                   |
| coroutines               | 30.9 ms                                                      | 41.8 ms: 1.36x slower                                                  |
| nqueens                  | 112 ms                                                       | 152 ms: 1.36x slower                                                   |
| json_dumps               | 14.1 ms                                                      | 19.5 ms: 1.38x slower                                                  |
| dulwich_log              | 93.7 ms                                                      | 130 ms: 1.38x slower                                                   |
| fannkuch                 | 547 ms                                                       | 759 ms: 1.39x slower                                                   |
| html5lib                 | 92.6 ms                                                      | 130 ms: 1.40x slower                                                   |
| spectral_norm            | 157 ms                                                       | 220 ms: 1.40x slower                                                   |
| deepcopy_memo            | 50.1 us                                                      | 70.8 us: 1.41x slower                                                  |
| bpe_tokeniser            | 6.28 sec                                                     | 9.01 sec: 1.43x slower                                                 |
| deepcopy_reduce          | 4.10 us                                                      | 5.92 us: 1.44x slower                                                  |
| tomli_loads              | 2.78 sec                                                     | 4.11 sec: 1.48x slower                                                 |
| 2to3                     | 445 ms                                                       | 659 ms: 1.48x slower                                                   |
| typing_runtime_protocols | 226 us                                                       | 336 us: 1.49x slower                                                   |
| sympy_integrate          | 30.2 ms                                                      | 45.5 ms: 1.51x slower                                                  |
| crypto_pyaes             | 100 ms                                                       | 151 ms: 1.51x slower                                                   |
| pyflate                  | 664 ms                                                       | 1.01 sec: 1.52x slower                                                 |
| xml_etree_process        | 85.9 ms                                                      | 133 ms: 1.54x slower                                                   |
| thrift                   | 1.10 ms                                                      | 1.72 ms: 1.57x slower                                                  |
| regex_compile            | 182 ms                                                       | 288 ms: 1.58x slower                                                   |
| float                    | 116 ms                                                       | 186 ms: 1.60x slower                                                   |
| richards                 | 65.5 ms                                                      | 105 ms: 1.61x slower                                                   |
| genshi_xml               | 72.1 ms                                                      | 119 ms: 1.66x slower                                                   |
| comprehensions           | 22.2 us                                                      | 37.0 us: 1.66x slower                                                  |
| pprint_safe_repr         | 987 ms                                                       | 1.65 sec: 1.67x slower                                                 |
| sqlglot_normalize        | 140 ms                                                       | 238 ms: 1.70x slower                                                   |
| sqlglot_optimize         | 74.7 ms                                                      | 127 ms: 1.71x slower                                                   |
| scimark_monte_carlo      | 90.6 ms                                                      | 155 ms: 1.72x slower                                                   |
| pprint_pformat           | 1.94 sec                                                     | 3.34 sec: 1.72x slower                                                 |
| sympy_str                | 379 ms                                                       | 660 ms: 1.74x slower                                                   |
| logging_simple           | 8.56 us                                                      | 14.9 us: 1.74x slower                                                  |
| genshi_text              | 31.7 ms                                                      | 55.5 ms: 1.75x slower                                                  |
| django_template          | 44.3 ms                                                      | 79.1 ms: 1.79x slower                                                  |
| unpickle_pure_python     | 290 us                                                       | 520 us: 1.79x slower                                                   |
| richards_super           | 73.2 ms                                                      | 133 ms: 1.82x slower                                                   |
| mako                     | 15.9 ms                                                      | 29.1 ms: 1.83x slower                                                  |
| logging_format           | 9.24 us                                                      | 16.9 us: 1.83x slower                                                  |
| go                       | 191 ms                                                       | 362 ms: 1.90x slower                                                   |
| pickle_pure_python       | 416 us                                                       | 797 us: 1.91x slower                                                   |
| scimark_sor              | 179 ms                                                       | 351 ms: 1.97x slower                                                   |
| chaos                    | 83.6 ms                                                      | 166 ms: 1.98x slower                                                   |
| logging_silent           | 130 ns                                                       | 260 ns: 2.00x slower                                                   |
| hexiom                   | 8.11 ms                                                      | 16.3 ms: 2.01x slower                                                  |
| scimark_lu               | 146 ms                                                       | 300 ms: 2.05x slower                                                   |
| sympy_expand             | 601 ms                                                       | 1.29 sec: 2.14x slower                                                 |
| sqlglot_parse            | 1.76 ms                                                      | 3.81 ms: 2.17x slower                                                  |
| raytrace                 | 344 ms                                                       | 749 ms: 2.18x slower                                                   |
| sqlglot_transpile        | 2.20 ms                                                      | 4.86 ms: 2.21x slower                                                  |
| nbody                    | 119 ms                                                       | 263 ms: 2.21x slower                                                   |
| sympy_sum                | 210 ms                                                       | 468 ms: 2.23x slower                                                   |
| deltablue                | 4.44 ms                                                      | 11.0 ms: 2.49x slower                                                  |
| unpack_sequence          | 74.3 ns                                                      | 199 ns: 2.68x slower                                                   |
| bench_mp_pool            | 18.7 ms                                                      | 60.0 ms: 3.21x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.44x slower                                                           |

Benchmark hidden because not significant (2): regex_effbot, pidigits
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.40x
- 95% likely to have a slowdown of 1.38x
- 99% likely to have a slowdown of 1.34x

# Memory
- memory change: 1.19x