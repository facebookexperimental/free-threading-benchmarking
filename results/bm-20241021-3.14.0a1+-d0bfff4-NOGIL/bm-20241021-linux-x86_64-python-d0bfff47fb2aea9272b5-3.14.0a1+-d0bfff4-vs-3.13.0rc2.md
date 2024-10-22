# Results vs. 3.13.0rc2

- fork: python
- ref: d0bfff47fb2aea9272b5
- machine: linux-x86_64
- commit hash: d0bfff4
- commit date: 2024-10-21
- overall geometric mean: 1.53x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.44x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 691 ms: 1.55x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.96 sec: 1.24x slower                                                 |
| html5lib       | 92.6 ms                                                      | 155 ms: 1.68x slower                                                   |
| tornado_http   | 251 ms                                                       | 409 ms: 1.63x slower                                                   |
| Geometric mean | (ref)                                                        | 1.51x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp_ssl  | 2.77 sec                                                     | 3.37 sec: 1.22x slower                                                 |
| asyncio_tcp      | 948 ms                                                       | 1.22 sec: 1.29x slower                                                 |
| async_generators | 567 ms                                                       | 754 ms: 1.33x slower                                                   |
| coroutines       | 30.9 ms                                                      | 41.3 ms: 1.34x slower                                                  |
| Geometric mean   | (ref)                                                        | 1.23x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 190 ms: 1.64x slower                                                   |
| nbody          | 119 ms                                                       | 290 ms: 2.44x slower                                                   |
| Geometric mean | (ref)                                                        | 1.58x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 34.8 ms: 1.06x slower                                                  |
| regex_compile  | 182 ms                                                       | 291 ms: 1.60x slower                                                   |
| Geometric mean | (ref)                                                        | 1.14x slower                                                           |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_list          | 6.86 us                                                      | 6.40 us: 1.07x faster                                                  |
| xml_etree_parse      | 231 ms                                                       | 252 ms: 1.09x slower                                                   |
| unpickle_list        | 6.68 us                                                      | 7.86 us: 1.18x slower                                                  |
| json_loads           | 34.3 us                                                      | 40.4 us: 1.18x slower                                                  |
| unpickle             | 20.5 us                                                      | 25.1 us: 1.22x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 164 ms: 1.34x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 21.2 ms: 1.50x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 131 ms: 1.53x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 4.36 sec: 1.57x slower                                                 |
| pickle_pure_python   | 416 us                                                       | 777 us: 1.87x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 563 us: 1.94x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.28x slower                                                           |

Benchmark hidden because not significant (3): pickle_dict, xml_etree_iterparse, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 20.6 ms: 1.35x slower                                                  |
| python_startup         | 22.4 ms                                                      | 33.6 ms: 1.50x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.42x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 110 ms: 1.52x slower                                                   |
| django_template | 44.3 ms                                                      | 82.2 ms: 1.86x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 60.5 ms: 1.91x slower                                                  |
| mako            | 15.9 ms                                                      | 32.3 ms: 2.03x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.82x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| create_gc_cycles         | 2.41 ms                                                      | 1.97 ms: 1.23x faster                                                  |
| pickle_list              | 6.86 us                                                      | 6.40 us: 1.07x faster                                                  |
| regex_v8                 | 32.8 ms                                                      | 34.8 ms: 1.06x slower                                                  |
| xml_etree_parse          | 231 ms                                                       | 252 ms: 1.09x slower                                                   |
| sqlite_synth             | 3.99 us                                                      | 4.46 us: 1.12x slower                                                  |
| deepcopy                 | 498 us                                                       | 564 us: 1.13x slower                                                   |
| json                     | 6.51 ms                                                      | 7.43 ms: 1.14x slower                                                  |
| telco                    | 12.2 ms                                                      | 14.2 ms: 1.17x slower                                                  |
| unpickle_list            | 6.68 us                                                      | 7.86 us: 1.18x slower                                                  |
| json_loads               | 34.3 us                                                      | 40.4 us: 1.18x slower                                                  |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.37 sec: 1.22x slower                                                 |
| unpickle                 | 20.5 us                                                      | 25.1 us: 1.22x slower                                                  |
| pathlib                  | 29.9 ms                                                      | 36.6 ms: 1.23x slower                                                  |
| docutils                 | 4.01 sec                                                     | 4.96 sec: 1.24x slower                                                 |
| asyncio_tcp              | 948 ms                                                       | 1.22 sec: 1.29x slower                                                 |
| pylint                   | 470 ms                                                       | 618 ms: 1.31x slower                                                   |
| async_generators         | 567 ms                                                       | 754 ms: 1.33x slower                                                   |
| mdp                      | 3.80 sec                                                     | 5.07 sec: 1.33x slower                                                 |
| coroutines               | 30.9 ms                                                      | 41.3 ms: 1.34x slower                                                  |
| xml_etree_generate       | 122 ms                                                       | 164 ms: 1.34x slower                                                   |
| python_startup_no_site   | 15.3 ms                                                      | 20.6 ms: 1.35x slower                                                  |
| coverage                 | 107 ms                                                       | 146 ms: 1.36x slower                                                   |
| bench_thread_pool        | 2.89 ms                                                      | 3.93 ms: 1.36x slower                                                  |
| generators               | 40.0 ms                                                      | 54.5 ms: 1.36x slower                                                  |
| scimark_fft              | 473 ms                                                       | 658 ms: 1.39x slower                                                   |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 9.53 ms: 1.41x slower                                                  |
| deepcopy_memo            | 50.1 us                                                      | 72.0 us: 1.44x slower                                                  |
| fannkuch                 | 547 ms                                                       | 790 ms: 1.44x slower                                                   |
| deepcopy_reduce          | 4.10 us                                                      | 5.93 us: 1.45x slower                                                  |
| crypto_pyaes             | 100 ms                                                       | 145 ms: 1.45x slower                                                   |
| pycparser                | 1.57 sec                                                     | 2.29 sec: 1.46x slower                                                 |
| nqueens                  | 112 ms                                                       | 163 ms: 1.46x slower                                                   |
| json_dumps               | 14.1 ms                                                      | 21.2 ms: 1.50x slower                                                  |
| python_startup           | 22.4 ms                                                      | 33.6 ms: 1.50x slower                                                  |
| thrift                   | 1.10 ms                                                      | 1.66 ms: 1.51x slower                                                  |
| genshi_xml               | 72.1 ms                                                      | 110 ms: 1.52x slower                                                   |
| xml_etree_process        | 85.9 ms                                                      | 131 ms: 1.53x slower                                                   |
| sympy_integrate          | 30.2 ms                                                      | 46.2 ms: 1.53x slower                                                  |
| meteor_contest           | 150 ms                                                       | 230 ms: 1.54x slower                                                   |
| 2to3                     | 445 ms                                                       | 691 ms: 1.55x slower                                                   |
| typing_runtime_protocols | 226 us                                                       | 352 us: 1.56x slower                                                   |
| tomli_loads              | 2.78 sec                                                     | 4.36 sec: 1.57x slower                                                 |
| dulwich_log              | 93.7 ms                                                      | 148 ms: 1.58x slower                                                   |
| regex_compile            | 182 ms                                                       | 291 ms: 1.60x slower                                                   |
| richards                 | 65.5 ms                                                      | 106 ms: 1.62x slower                                                   |
| bpe_tokeniser            | 6.28 sec                                                     | 10.2 sec: 1.62x slower                                                 |
| tornado_http             | 251 ms                                                       | 409 ms: 1.63x slower                                                   |
| float                    | 116 ms                                                       | 190 ms: 1.64x slower                                                   |
| spectral_norm            | 157 ms                                                       | 257 ms: 1.64x slower                                                   |
| sqlglot_optimize         | 74.7 ms                                                      | 125 ms: 1.68x slower                                                   |
| html5lib                 | 92.6 ms                                                      | 155 ms: 1.68x slower                                                   |
| sqlglot_normalize        | 140 ms                                                       | 235 ms: 1.68x slower                                                   |
| pyflate                  | 664 ms                                                       | 1.13 sec: 1.70x slower                                                 |
| richards_super           | 73.2 ms                                                      | 126 ms: 1.72x slower                                                   |
| comprehensions           | 22.2 us                                                      | 39.0 us: 1.75x slower                                                  |
| sympy_str                | 379 ms                                                       | 690 ms: 1.82x slower                                                   |
| logging_simple           | 8.56 us                                                      | 15.7 us: 1.83x slower                                                  |
| django_template          | 44.3 ms                                                      | 82.2 ms: 1.86x slower                                                  |
| pickle_pure_python       | 416 us                                                       | 777 us: 1.87x slower                                                   |
| pprint_pformat           | 1.94 sec                                                     | 3.63 sec: 1.87x slower                                                 |
| pprint_safe_repr         | 987 ms                                                       | 1.88 sec: 1.91x slower                                                 |
| logging_format           | 9.24 us                                                      | 17.6 us: 1.91x slower                                                  |
| genshi_text              | 31.7 ms                                                      | 60.5 ms: 1.91x slower                                                  |
| unpickle_pure_python     | 290 us                                                       | 563 us: 1.94x slower                                                   |
| logging_silent           | 130 ns                                                       | 258 ns: 1.98x slower                                                   |
| chaos                    | 83.6 ms                                                      | 166 ms: 1.99x slower                                                   |
| go                       | 191 ms                                                       | 381 ms: 1.99x slower                                                   |
| mako                     | 15.9 ms                                                      | 32.3 ms: 2.03x slower                                                  |
| scimark_monte_carlo      | 90.6 ms                                                      | 186 ms: 2.05x slower                                                   |
| scimark_sor              | 179 ms                                                       | 373 ms: 2.09x slower                                                   |
| scimark_lu               | 146 ms                                                       | 313 ms: 2.14x slower                                                   |
| hexiom                   | 8.11 ms                                                      | 18.0 ms: 2.22x slower                                                  |
| sympy_expand             | 601 ms                                                       | 1.36 sec: 2.26x slower                                                 |
| sqlglot_transpile        | 2.20 ms                                                      | 4.99 ms: 2.27x slower                                                  |
| sqlglot_parse            | 1.76 ms                                                      | 4.06 ms: 2.31x slower                                                  |
| sympy_sum                | 210 ms                                                       | 488 ms: 2.32x slower                                                   |
| raytrace                 | 344 ms                                                       | 811 ms: 2.35x slower                                                   |
| nbody                    | 119 ms                                                       | 290 ms: 2.44x slower                                                   |
| deltablue                | 4.44 ms                                                      | 11.5 ms: 2.58x slower                                                  |
| unpack_sequence          | 74.3 ns                                                      | 193 ns: 2.60x slower                                                   |
| bench_mp_pool            | 18.7 ms                                                      | 62.2 ms: 3.33x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.53x slower                                                           |

Benchmark hidden because not significant (8): pidigits, pickle_dict, regex_effbot, xml_etree_iterparse, pickle, asyncio_websockets, regex_dna, gc_traversal
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.48x
- 95% likely to have a slowdown of 1.47x
- 99% likely to have a slowdown of 1.44x

# Memory
- memory change: 1.16x