# Results vs. 3.13.0rc2

- fork: colesbury
- ref: cheaper_steal
- machine: linux-x86_64
- commit hash: ed7085a
- commit date: 2024-11-18
- overall geometric mean: 1.55x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.38x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 410 ms: 1.58x slower                                               |
| docutils       | 2.62 sec                                                     | 3.34 sec: 1.28x slower                                             |
| html5lib       | 67.0 ms                                                      | 102 ms: 1.53x slower                                               |
| Geometric mean | (ref)                                                        | 1.46x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|--------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| asyncio_websockets | 520 ms                                                       | 523 ms: 1.00x slower                                               |
| asyncio_tcp        | 505 ms                                                       | 582 ms: 1.15x slower                                               |
| asyncio_tcp_ssl    | 1.51 sec                                                     | 1.80 sec: 1.19x slower                                             |
| coroutines         | 23.6 ms                                                      | 29.3 ms: 1.25x slower                                              |
| async_generators   | 377 ms                                                       | 485 ms: 1.29x slower                                               |
| Geometric mean     | (ref)                                                        | 1.17x slower                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.17x faster                                               |
| float          | 77.5 ms                                                      | 147 ms: 1.90x slower                                               |
| nbody          | 85.1 ms                                                      | 192 ms: 2.26x slower                                               |
| Geometric mean | (ref)                                                        | 1.54x slower                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                              |
| regex_dna      | 180 ms                                                       | 191 ms: 1.06x slower                                               |
| regex_v8       | 22.7 ms                                                      | 25.3 ms: 1.11x slower                                              |
| regex_compile  | 132 ms                                                       | 226 ms: 1.71x slower                                               |
| Geometric mean | (ref)                                                        | 1.17x slower                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 134 ms: 1.02x faster                                               |
| pickle_dict          | 32.5 us                                                      | 32.7 us: 1.01x slower                                              |
| pickle_list          | 4.93 us                                                      | 5.07 us: 1.03x slower                                              |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                              |
| pickle               | 11.3 us                                                      | 12.2 us: 1.08x slower                                              |
| unpickle_list        | 4.71 us                                                      | 5.09 us: 1.08x slower                                              |
| xml_etree_iterparse  | 94.9 ms                                                      | 108 ms: 1.14x slower                                               |
| xml_etree_generate   | 85.4 ms                                                      | 112 ms: 1.31x slower                                               |
| json_dumps           | 10.5 ms                                                      | 15.1 ms: 1.43x slower                                              |
| xml_etree_process    | 59.3 ms                                                      | 92.2 ms: 1.55x slower                                              |
| tomli_loads          | 2.01 sec                                                     | 3.14 sec: 1.56x slower                                             |
| unpickle_pure_python | 210 us                                                       | 422 us: 2.01x slower                                               |
| pickle_pure_python   | 294 us                                                       | 620 us: 2.11x slower                                               |
| Geometric mean       | (ref)                                                        | 1.27x slower                                                       |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.40x slower                                              |
| python_startup         | 11.0 ms                                                      | 15.8 ms: 1.44x slower                                              |
| Geometric mean         | (ref)                                                        | 1.42x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 78.5 ms: 1.61x slower                                              |
| genshi_text     | 21.5 ms                                                      | 38.9 ms: 1.81x slower                                              |
| django_template | 34.1 ms                                                      | 63.2 ms: 1.85x slower                                              |
| mako            | 11.3 ms                                                      | 21.4 ms: 1.89x slower                                              |
| Geometric mean  | (ref)                                                        | 1.79x slower                                                       |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1+-ed7085a |
|--------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits                 | 217 ms                                                       | 186 ms: 1.17x faster                                               |
| gc_traversal             | 3.14 ms                                                      | 2.71 ms: 1.16x faster                                              |
| create_gc_cycles         | 1.34 ms                                                      | 1.22 ms: 1.09x faster                                              |
| regex_effbot             | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                              |
| xml_etree_parse          | 136 ms                                                       | 134 ms: 1.02x faster                                               |
| asyncio_websockets       | 520 ms                                                       | 523 ms: 1.00x slower                                               |
| pickle_dict              | 32.5 us                                                      | 32.7 us: 1.01x slower                                              |
| pickle_list              | 4.93 us                                                      | 5.07 us: 1.03x slower                                              |
| json_loads               | 27.0 us                                                      | 28.4 us: 1.05x slower                                              |
| json                     | 4.93 ms                                                      | 5.19 ms: 1.05x slower                                              |
| regex_dna                | 180 ms                                                       | 191 ms: 1.06x slower                                               |
| pickle                   | 11.3 us                                                      | 12.2 us: 1.08x slower                                              |
| unpickle_list            | 4.71 us                                                      | 5.09 us: 1.08x slower                                              |
| sqlite_synth             | 2.21 us                                                      | 2.46 us: 1.11x slower                                              |
| regex_v8                 | 22.7 ms                                                      | 25.3 ms: 1.11x slower                                              |
| pathlib                  | 19.2 ms                                                      | 21.7 ms: 1.13x slower                                              |
| xml_etree_iterparse      | 94.9 ms                                                      | 108 ms: 1.14x slower                                               |
| asyncio_tcp              | 505 ms                                                       | 582 ms: 1.15x slower                                               |
| scimark_fft              | 349 ms                                                       | 404 ms: 1.16x slower                                               |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.80 sec: 1.19x slower                                             |
| deepcopy                 | 355 us                                                       | 425 us: 1.20x slower                                               |
| telco                    | 7.82 ms                                                      | 9.39 ms: 1.20x slower                                              |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.72 ms: 1.22x slower                                              |
| coverage                 | 83.0 ms                                                      | 101 ms: 1.22x slower                                               |
| coroutines               | 23.6 ms                                                      | 29.3 ms: 1.25x slower                                              |
| mdp                      | 2.36 sec                                                     | 3.00 sec: 1.27x slower                                             |
| docutils                 | 2.62 sec                                                     | 3.34 sec: 1.28x slower                                             |
| async_generators         | 377 ms                                                       | 485 ms: 1.29x slower                                               |
| xml_etree_generate       | 85.4 ms                                                      | 112 ms: 1.31x slower                                               |
| pylint                   | 317 ms                                                       | 416 ms: 1.31x slower                                               |
| meteor_contest           | 102 ms                                                       | 137 ms: 1.35x slower                                               |
| generators               | 28.8 ms                                                      | 39.1 ms: 1.36x slower                                              |
| deepcopy_memo            | 39.1 us                                                      | 53.4 us: 1.37x slower                                              |
| bpe_tokeniser            | 4.45 sec                                                     | 6.10 sec: 1.37x slower                                             |
| dulwich_log              | 74.8 ms                                                      | 104 ms: 1.38x slower                                               |
| python_startup_no_site   | 7.39 ms                                                      | 10.3 ms: 1.40x slower                                              |
| json_dumps               | 10.5 ms                                                      | 15.1 ms: 1.43x slower                                              |
| deepcopy_reduce          | 3.11 us                                                      | 4.47 us: 1.43x slower                                              |
| nqueens                  | 78.6 ms                                                      | 113 ms: 1.44x slower                                               |
| python_startup           | 11.0 ms                                                      | 15.8 ms: 1.44x slower                                              |
| spectral_norm            | 111 ms                                                       | 161 ms: 1.45x slower                                               |
| pycparser                | 1.12 sec                                                     | 1.69 sec: 1.51x slower                                             |
| fannkuch                 | 370 ms                                                       | 560 ms: 1.51x slower                                               |
| html5lib                 | 67.0 ms                                                      | 102 ms: 1.53x slower                                               |
| xml_etree_process        | 59.3 ms                                                      | 92.2 ms: 1.55x slower                                              |
| tomli_loads              | 2.01 sec                                                     | 3.14 sec: 1.56x slower                                             |
| 2to3                     | 260 ms                                                       | 410 ms: 1.58x slower                                               |
| crypto_pyaes             | 67.9 ms                                                      | 107 ms: 1.58x slower                                               |
| genshi_xml               | 48.8 ms                                                      | 78.5 ms: 1.61x slower                                              |
| thrift                   | 778 us                                                       | 1.26 ms: 1.61x slower                                              |
| typing_runtime_protocols | 155 us                                                       | 251 us: 1.62x slower                                               |
| sympy_integrate          | 19.8 ms                                                      | 32.9 ms: 1.66x slower                                              |
| sqlglot_normalize        | 106 ms                                                       | 179 ms: 1.69x slower                                               |
| pyflate                  | 449 ms                                                       | 761 ms: 1.70x slower                                               |
| sqlglot_optimize         | 52.7 ms                                                      | 89.5 ms: 1.70x slower                                              |
| regex_compile            | 132 ms                                                       | 226 ms: 1.71x slower                                               |
| pprint_safe_repr         | 738 ms                                                       | 1.32 sec: 1.79x slower                                             |
| genshi_text              | 21.5 ms                                                      | 38.9 ms: 1.81x slower                                              |
| pprint_pformat           | 1.50 sec                                                     | 2.72 sec: 1.82x slower                                             |
| comprehensions           | 16.5 us                                                      | 30.3 us: 1.84x slower                                              |
| django_template          | 34.1 ms                                                      | 63.2 ms: 1.85x slower                                              |
| mako                     | 11.3 ms                                                      | 21.4 ms: 1.89x slower                                              |
| float                    | 77.5 ms                                                      | 147 ms: 1.90x slower                                               |
| scimark_monte_carlo      | 65.4 ms                                                      | 125 ms: 1.91x slower                                               |
| logging_format           | 6.84 us                                                      | 13.2 us: 1.92x slower                                              |
| logging_simple           | 6.16 us                                                      | 11.9 us: 1.93x slower                                              |
| sympy_str                | 275 ms                                                       | 537 ms: 1.95x slower                                               |
| scimark_sor              | 134 ms                                                       | 263 ms: 1.96x slower                                               |
| richards                 | 45.2 ms                                                      | 88.6 ms: 1.96x slower                                              |
| unpickle_pure_python     | 210 us                                                       | 422 us: 2.01x slower                                               |
| logging_silent           | 103 ns                                                       | 206 ns: 2.01x slower                                               |
| hexiom                   | 5.99 ms                                                      | 12.2 ms: 2.03x slower                                              |
| richards_super           | 51.6 ms                                                      | 107 ms: 2.06x slower                                               |
| chaos                    | 57.3 ms                                                      | 120 ms: 2.09x slower                                               |
| go                       | 141 ms                                                       | 296 ms: 2.10x slower                                               |
| pickle_pure_python       | 294 us                                                       | 620 us: 2.11x slower                                               |
| sqlglot_transpile        | 1.56 ms                                                      | 3.29 ms: 2.11x slower                                              |
| scimark_lu               | 113 ms                                                       | 243 ms: 2.16x slower                                               |
| sqlglot_parse            | 1.25 ms                                                      | 2.80 ms: 2.25x slower                                              |
| nbody                    | 85.1 ms                                                      | 192 ms: 2.26x slower                                               |
| sympy_expand             | 457 ms                                                       | 1.05 sec: 2.30x slower                                             |
| sympy_sum                | 156 ms                                                       | 379 ms: 2.44x slower                                               |
| raytrace                 | 253 ms                                                       | 624 ms: 2.47x slower                                               |
| deltablue                | 3.12 ms                                                      | 9.11 ms: 2.92x slower                                              |
| unpack_sequence          | 44.8 ns                                                      | 145 ns: 3.23x slower                                               |
| bench_thread_pool        | 919 us                                                       | 3.48 ms: 3.78x slower                                              |
| bench_mp_pool            | 11.0 ms                                                      | 69.7 ms: 6.34x slower                                              |
| Geometric mean           | (ref)                                                        | 1.55x slower                                                       |

Benchmark hidden because not significant (1): unpickle
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.45x
- 95% likely to have a slowdown of 1.43x
- 99% likely to have a slowdown of 1.38x

# Memory
- memory change: 1.22x