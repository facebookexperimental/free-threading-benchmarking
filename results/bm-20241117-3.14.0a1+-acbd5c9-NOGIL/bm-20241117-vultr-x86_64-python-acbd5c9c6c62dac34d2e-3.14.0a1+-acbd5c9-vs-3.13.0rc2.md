# Results vs. 3.13.0rc2

- fork: python
- ref: acbd5c9c6c62dac34d2e
- machine: linux-x86_64
- commit hash: acbd5c9
- commit date: 2024-11-17
- overall geometric mean: 1.58x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.41x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 418 ms: 1.61x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.43 sec: 1.31x slower                                                 |
| html5lib       | 67.0 ms                                                      | 107 ms: 1.60x slower                                                   |
| Geometric mean | (ref)                                                        | 1.50x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|--------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 520 ms                                                       | 518 ms: 1.01x faster                                                   |
| asyncio_tcp        | 505 ms                                                       | 583 ms: 1.15x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                                     | 1.81 sec: 1.20x slower                                                 |
| async_generators   | 377 ms                                                       | 492 ms: 1.30x slower                                                   |
| coroutines         | 23.6 ms                                                      | 32.0 ms: 1.36x slower                                                  |
| Geometric mean     | (ref)                                                        | 1.20x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 216 ms: 1.00x faster                                                   |
| float          | 77.5 ms                                                      | 153 ms: 1.98x slower                                                   |
| nbody          | 85.1 ms                                                      | 207 ms: 2.43x slower                                                   |
| Geometric mean | (ref)                                                        | 1.69x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.11 ms: 1.01x slower                                                  |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                  |
| regex_compile  | 132 ms                                                       | 231 ms: 1.75x slower                                                   |
| Geometric mean | (ref)                                                        | 1.18x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.03x faster                                                   |
| unpickle             | 14.3 us                                                      | 14.7 us: 1.02x slower                                                  |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                  |
| pickle_list          | 4.93 us                                                      | 5.20 us: 1.06x slower                                                  |
| pickle               | 11.3 us                                                      | 12.5 us: 1.10x slower                                                  |
| unpickle_list        | 4.71 us                                                      | 5.20 us: 1.10x slower                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 109 ms: 1.15x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 115 ms: 1.35x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 15.4 ms: 1.47x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 94.1 ms: 1.59x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 3.28 sec: 1.63x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 432 us: 2.06x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 635 us: 2.16x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.29x slower                                                           |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 83.2 ms: 1.71x slower                                                  |
| mako            | 11.3 ms                                                      | 20.9 ms: 1.85x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 40.6 ms: 1.88x slower                                                  |
| django_template | 34.1 ms                                                      | 65.3 ms: 1.91x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.84x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.58 ms: 1.22x faster                                                  |
| create_gc_cycles         | 1.34 ms                                                      | 1.13 ms: 1.18x faster                                                  |
| xml_etree_parse          | 136 ms                                                       | 133 ms: 1.03x faster                                                   |
| asyncio_websockets       | 520 ms                                                       | 518 ms: 1.01x faster                                                   |
| pidigits                 | 217 ms                                                       | 216 ms: 1.00x faster                                                   |
| regex_effbot             | 3.08 ms                                                      | 3.11 ms: 1.01x slower                                                  |
| regex_dna                | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| unpickle                 | 14.3 us                                                      | 14.7 us: 1.02x slower                                                  |
| json_loads               | 27.0 us                                                      | 28.4 us: 1.05x slower                                                  |
| pickle_list              | 4.93 us                                                      | 5.20 us: 1.06x slower                                                  |
| json                     | 4.93 ms                                                      | 5.26 ms: 1.07x slower                                                  |
| regex_v8                 | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                  |
| pickle                   | 11.3 us                                                      | 12.5 us: 1.10x slower                                                  |
| unpickle_list            | 4.71 us                                                      | 5.20 us: 1.10x slower                                                  |
| sqlite_synth             | 2.21 us                                                      | 2.48 us: 1.12x slower                                                  |
| pathlib                  | 19.2 ms                                                      | 22.1 ms: 1.15x slower                                                  |
| xml_etree_iterparse      | 94.9 ms                                                      | 109 ms: 1.15x slower                                                   |
| asyncio_tcp              | 505 ms                                                       | 583 ms: 1.15x slower                                                   |
| telco                    | 7.82 ms                                                      | 9.27 ms: 1.19x slower                                                  |
| scimark_fft              | 349 ms                                                       | 418 ms: 1.20x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.81 sec: 1.20x slower                                                 |
| deepcopy                 | 355 us                                                       | 438 us: 1.23x slower                                                   |
| coverage                 | 83.0 ms                                                      | 103 ms: 1.24x slower                                                   |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.94 ms: 1.26x slower                                                  |
| async_generators         | 377 ms                                                       | 492 ms: 1.30x slower                                                   |
| docutils                 | 2.62 sec                                                     | 3.43 sec: 1.31x slower                                                 |
| pylint                   | 317 ms                                                       | 423 ms: 1.33x slower                                                   |
| mdp                      | 2.36 sec                                                     | 3.14 sec: 1.33x slower                                                 |
| xml_etree_generate       | 85.4 ms                                                      | 115 ms: 1.35x slower                                                   |
| coroutines               | 23.6 ms                                                      | 32.0 ms: 1.36x slower                                                  |
| meteor_contest           | 102 ms                                                       | 139 ms: 1.37x slower                                                   |
| bpe_tokeniser            | 4.45 sec                                                     | 6.18 sec: 1.39x slower                                                 |
| python_startup_no_site   | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                  |
| deepcopy_memo            | 39.1 us                                                      | 54.7 us: 1.40x slower                                                  |
| dulwich_log              | 74.8 ms                                                      | 105 ms: 1.41x slower                                                   |
| python_startup           | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                  |
| generators               | 28.8 ms                                                      | 41.5 ms: 1.44x slower                                                  |
| deepcopy_reduce          | 3.11 us                                                      | 4.53 us: 1.46x slower                                                  |
| nqueens                  | 78.6 ms                                                      | 115 ms: 1.47x slower                                                   |
| json_dumps               | 10.5 ms                                                      | 15.4 ms: 1.47x slower                                                  |
| spectral_norm            | 111 ms                                                       | 163 ms: 1.47x slower                                                   |
| fannkuch                 | 370 ms                                                       | 571 ms: 1.54x slower                                                   |
| pycparser                | 1.12 sec                                                     | 1.74 sec: 1.56x slower                                                 |
| xml_etree_process        | 59.3 ms                                                      | 94.1 ms: 1.59x slower                                                  |
| crypto_pyaes             | 67.9 ms                                                      | 109 ms: 1.60x slower                                                   |
| html5lib                 | 67.0 ms                                                      | 107 ms: 1.60x slower                                                   |
| 2to3                     | 260 ms                                                       | 418 ms: 1.61x slower                                                   |
| tomli_loads              | 2.01 sec                                                     | 3.28 sec: 1.63x slower                                                 |
| typing_runtime_protocols | 155 us                                                       | 253 us: 1.64x slower                                                   |
| thrift                   | 778 us                                                       | 1.30 ms: 1.67x slower                                                  |
| sympy_integrate          | 19.8 ms                                                      | 33.4 ms: 1.69x slower                                                  |
| genshi_xml               | 48.8 ms                                                      | 83.2 ms: 1.71x slower                                                  |
| sqlglot_normalize        | 106 ms                                                       | 182 ms: 1.72x slower                                                   |
| sqlglot_optimize         | 52.7 ms                                                      | 90.9 ms: 1.72x slower                                                  |
| regex_compile            | 132 ms                                                       | 231 ms: 1.75x slower                                                   |
| pyflate                  | 449 ms                                                       | 797 ms: 1.78x slower                                                   |
| pprint_safe_repr         | 738 ms                                                       | 1.34 sec: 1.82x slower                                                 |
| mako                     | 11.3 ms                                                      | 20.9 ms: 1.85x slower                                                  |
| pprint_pformat           | 1.50 sec                                                     | 2.77 sec: 1.85x slower                                                 |
| comprehensions           | 16.5 us                                                      | 31.0 us: 1.88x slower                                                  |
| genshi_text              | 21.5 ms                                                      | 40.6 ms: 1.88x slower                                                  |
| django_template          | 34.1 ms                                                      | 65.3 ms: 1.91x slower                                                  |
| scimark_monte_carlo      | 65.4 ms                                                      | 129 ms: 1.97x slower                                                   |
| float                    | 77.5 ms                                                      | 153 ms: 1.98x slower                                                   |
| sympy_str                | 275 ms                                                       | 544 ms: 1.98x slower                                                   |
| logging_simple           | 6.16 us                                                      | 12.4 us: 2.01x slower                                                  |
| logging_format           | 6.84 us                                                      | 13.9 us: 2.02x slower                                                  |
| scimark_sor              | 134 ms                                                       | 273 ms: 2.03x slower                                                   |
| unpickle_pure_python     | 210 us                                                       | 432 us: 2.06x slower                                                   |
| hexiom                   | 5.99 ms                                                      | 12.7 ms: 2.12x slower                                                  |
| richards                 | 45.2 ms                                                      | 96.0 ms: 2.12x slower                                                  |
| sqlglot_transpile        | 1.56 ms                                                      | 3.35 ms: 2.15x slower                                                  |
| chaos                    | 57.3 ms                                                      | 123 ms: 2.15x slower                                                   |
| go                       | 141 ms                                                       | 303 ms: 2.16x slower                                                   |
| pickle_pure_python       | 294 us                                                       | 635 us: 2.16x slower                                                   |
| logging_silent           | 103 ns                                                       | 222 ns: 2.17x slower                                                   |
| richards_super           | 51.6 ms                                                      | 112 ms: 2.17x slower                                                   |
| scimark_lu               | 113 ms                                                       | 248 ms: 2.20x slower                                                   |
| sqlglot_parse            | 1.25 ms                                                      | 2.89 ms: 2.32x slower                                                  |
| sympy_expand             | 457 ms                                                       | 1.06 sec: 2.32x slower                                                 |
| nbody                    | 85.1 ms                                                      | 207 ms: 2.43x slower                                                   |
| sympy_sum                | 156 ms                                                       | 383 ms: 2.46x slower                                                   |
| raytrace                 | 253 ms                                                       | 640 ms: 2.54x slower                                                   |
| deltablue                | 3.12 ms                                                      | 9.33 ms: 2.99x slower                                                  |
| unpack_sequence          | 44.8 ns                                                      | 151 ns: 3.37x slower                                                   |
| bench_thread_pool        | 919 us                                                       | 3.49 ms: 3.79x slower                                                  |
| bench_mp_pool            | 11.0 ms                                                      | 72.7 ms: 6.61x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.58x slower                                                           |

Benchmark hidden because not significant (1): pickle_dict
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.48x
- 95% likely to have a slowdown of 1.46x
- 99% likely to have a slowdown of 1.41x

# Memory
- memory change: 1.22x