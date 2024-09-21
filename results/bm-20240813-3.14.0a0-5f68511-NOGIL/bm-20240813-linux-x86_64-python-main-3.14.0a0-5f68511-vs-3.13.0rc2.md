# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5f68511
- commit date: 2024-08-13
- overall geometric mean: 1.46x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.33x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 445 ms                                                       | 661 ms: 1.48x slower                                  |
| docutils       | 4.01 sec                                                     | 5.15 sec: 1.28x slower                                |
| html5lib       | 92.6 ms                                                      | 145 ms: 1.56x slower                                  |
| tornado_http   | 251 ms                                                       | 360 ms: 1.43x slower                                  |
| Geometric mean | (ref)                                                        | 1.44x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|-------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.40 sec                                                     | 1.17 sec: 1.20x faster                                |
| async_tree_io           | 1.39 sec                                                     | 1.30 sec: 1.06x faster                                |
| async_tree_cpu_io_mixed | 889 ms                                                       | 945 ms: 1.06x slower                                  |
| async_tree_none         | 572 ms                                                       | 621 ms: 1.09x slower                                  |
| async_tree_memoization  | 709 ms                                                       | 787 ms: 1.11x slower                                  |
| asyncio_tcp             | 948 ms                                                       | 1.17 sec: 1.23x slower                                |
| asyncio_tcp_ssl         | 2.77 sec                                                     | 3.55 sec: 1.28x slower                                |
| async_generators        | 567 ms                                                       | 744 ms: 1.31x slower                                  |
| coroutines              | 30.9 ms                                                      | 44.5 ms: 1.44x slower                                 |
| Geometric mean          | (ref)                                                        | 1.09x slower                                          |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, asyncio_websockets, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 116 ms                                                       | 206 ms: 1.78x slower                                  |
| nbody          | 119 ms                                                       | 293 ms: 2.47x slower                                  |
| Geometric mean | (ref)                                                        | 1.62x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 36.7 ms: 1.12x slower                                 |
| regex_compile  | 182 ms                                                       | 290 ms: 1.59x slower                                  |
| Geometric mean | (ref)                                                        | 1.16x slower                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 6.86 us                                                      | 6.17 us: 1.11x faster                                 |
| pickle_dict          | 47.2 us                                                      | 45.2 us: 1.04x faster                                 |
| pickle               | 15.1 us                                                      | 14.6 us: 1.04x faster                                 |
| unpickle             | 20.5 us                                                      | 22.2 us: 1.08x slower                                 |
| json_loads           | 34.3 us                                                      | 43.2 us: 1.26x slower                                 |
| unpickle_list        | 6.68 us                                                      | 8.50 us: 1.27x slower                                 |
| xml_etree_generate   | 122 ms                                                       | 159 ms: 1.30x slower                                  |
| json_dumps           | 14.1 ms                                                      | 19.1 ms: 1.35x slower                                 |
| tomli_loads          | 2.78 sec                                                     | 4.26 sec: 1.53x slower                                |
| xml_etree_process    | 85.9 ms                                                      | 137 ms: 1.60x slower                                  |
| pickle_pure_python   | 416 us                                                       | 803 us: 1.93x slower                                  |
| unpickle_pure_python | 290 us                                                       | 619 us: 2.13x slower                                  |
| Geometric mean       | (ref)                                                        | 1.25x slower                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 21.2 ms: 1.38x slower                                 |
| python_startup         | 22.4 ms                                                      | 31.5 ms: 1.41x slower                                 |
| Geometric mean         | (ref)                                                        | 1.40x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 117 ms: 1.62x slower                                  |
| genshi_text     | 31.7 ms                                                      | 55.9 ms: 1.77x slower                                 |
| django_template | 44.3 ms                                                      | 85.9 ms: 1.94x slower                                 |
| mako            | 15.9 ms                                                      | 32.0 ms: 2.00x slower                                 |
| Geometric mean  | (ref)                                                        | 1.83x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|--------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg         | 1.40 sec                                                     | 1.17 sec: 1.20x faster                                |
| create_gc_cycles         | 2.41 ms                                                      | 2.01 ms: 1.20x faster                                 |
| bench_mp_pool            | 18.7 ms                                                      | 16.8 ms: 1.11x faster                                 |
| pickle_list              | 6.86 us                                                      | 6.17 us: 1.11x faster                                 |
| async_tree_io            | 1.39 sec                                                     | 1.30 sec: 1.06x faster                                |
| gc_traversal             | 5.70 ms                                                      | 5.42 ms: 1.05x faster                                 |
| pickle_dict              | 47.2 us                                                      | 45.2 us: 1.04x faster                                 |
| pickle                   | 15.1 us                                                      | 14.6 us: 1.04x faster                                 |
| async_tree_cpu_io_mixed  | 889 ms                                                       | 945 ms: 1.06x slower                                  |
| unpickle                 | 20.5 us                                                      | 22.2 us: 1.08x slower                                 |
| async_tree_none          | 572 ms                                                       | 621 ms: 1.09x slower                                  |
| sqlite_synth             | 3.99 us                                                      | 4.38 us: 1.10x slower                                 |
| async_tree_memoization   | 709 ms                                                       | 787 ms: 1.11x slower                                  |
| regex_v8                 | 32.8 ms                                                      | 36.7 ms: 1.12x slower                                 |
| deepcopy                 | 498 us                                                       | 571 us: 1.15x slower                                  |
| pathlib                  | 29.9 ms                                                      | 34.5 ms: 1.15x slower                                 |
| telco                    | 12.2 ms                                                      | 14.8 ms: 1.21x slower                                 |
| asyncio_tcp              | 948 ms                                                       | 1.17 sec: 1.23x slower                                |
| pylint                   | 470 ms                                                       | 588 ms: 1.25x slower                                  |
| json_loads               | 34.3 us                                                      | 43.2 us: 1.26x slower                                 |
| unpickle_list            | 6.68 us                                                      | 8.50 us: 1.27x slower                                 |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.55 sec: 1.28x slower                                |
| docutils                 | 4.01 sec                                                     | 5.15 sec: 1.28x slower                                |
| xml_etree_generate       | 122 ms                                                       | 159 ms: 1.30x slower                                  |
| async_generators         | 567 ms                                                       | 744 ms: 1.31x slower                                  |
| json                     | 6.51 ms                                                      | 8.55 ms: 1.31x slower                                 |
| scimark_fft              | 473 ms                                                       | 628 ms: 1.33x slower                                  |
| json_dumps               | 14.1 ms                                                      | 19.1 ms: 1.35x slower                                 |
| coverage                 | 107 ms                                                       | 146 ms: 1.35x slower                                  |
| mdp                      | 3.80 sec                                                     | 5.24 sec: 1.38x slower                                |
| python_startup_no_site   | 15.3 ms                                                      | 21.2 ms: 1.38x slower                                 |
| pycparser                | 1.57 sec                                                     | 2.18 sec: 1.39x slower                                |
| meteor_contest           | 150 ms                                                       | 210 ms: 1.40x slower                                  |
| python_startup           | 22.4 ms                                                      | 31.5 ms: 1.41x slower                                 |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 9.62 ms: 1.42x slower                                 |
| tornado_http             | 251 ms                                                       | 360 ms: 1.43x slower                                  |
| coroutines               | 30.9 ms                                                      | 44.5 ms: 1.44x slower                                 |
| deepcopy_memo            | 50.1 us                                                      | 72.7 us: 1.45x slower                                 |
| generators               | 40.0 ms                                                      | 58.3 ms: 1.46x slower                                 |
| fannkuch                 | 547 ms                                                       | 804 ms: 1.47x slower                                  |
| 2to3                     | 445 ms                                                       | 661 ms: 1.48x slower                                  |
| deepcopy_reduce          | 4.10 us                                                      | 6.14 us: 1.50x slower                                 |
| nqueens                  | 112 ms                                                       | 170 ms: 1.53x slower                                  |
| tomli_loads              | 2.78 sec                                                     | 4.26 sec: 1.53x slower                                |
| typing_runtime_protocols | 226 us                                                       | 350 us: 1.55x slower                                  |
| html5lib                 | 92.6 ms                                                      | 145 ms: 1.56x slower                                  |
| crypto_pyaes             | 100 ms                                                       | 157 ms: 1.56x slower                                  |
| thrift                   | 1.10 ms                                                      | 1.72 ms: 1.57x slower                                 |
| regex_compile            | 182 ms                                                       | 290 ms: 1.59x slower                                  |
| xml_etree_process        | 85.9 ms                                                      | 137 ms: 1.60x slower                                  |
| genshi_xml               | 72.1 ms                                                      | 117 ms: 1.62x slower                                  |
| richards                 | 65.5 ms                                                      | 106 ms: 1.62x slower                                  |
| spectral_norm            | 157 ms                                                       | 258 ms: 1.65x slower                                  |
| sqlglot_normalize        | 140 ms                                                       | 231 ms: 1.65x slower                                  |
| sqlglot_optimize         | 74.7 ms                                                      | 124 ms: 1.66x slower                                  |
| bench_thread_pool        | 2.89 ms                                                      | 4.83 ms: 1.67x slower                                 |
| bpe_tokeniser            | 6.28 sec                                                     | 10.6 sec: 1.68x slower                                |
| pyflate                  | 664 ms                                                       | 1.13 sec: 1.70x slower                                |
| sympy_integrate          | 30.2 ms                                                      | 51.8 ms: 1.71x slower                                 |
| pprint_safe_repr         | 987 ms                                                       | 1.71 sec: 1.73x slower                                |
| genshi_text              | 31.7 ms                                                      | 55.9 ms: 1.77x slower                                 |
| logging_simple           | 8.56 us                                                      | 15.2 us: 1.78x slower                                 |
| float                    | 116 ms                                                       | 206 ms: 1.78x slower                                  |
| richards_super           | 73.2 ms                                                      | 131 ms: 1.79x slower                                  |
| comprehensions           | 22.2 us                                                      | 40.4 us: 1.82x slower                                 |
| pprint_pformat           | 1.94 sec                                                     | 3.54 sec: 1.82x slower                                |
| sympy_str                | 379 ms                                                       | 709 ms: 1.87x slower                                  |
| logging_format           | 9.24 us                                                      | 17.5 us: 1.90x slower                                 |
| scimark_monte_carlo      | 90.6 ms                                                      | 174 ms: 1.92x slower                                  |
| pickle_pure_python       | 416 us                                                       | 803 us: 1.93x slower                                  |
| django_template          | 44.3 ms                                                      | 85.9 ms: 1.94x slower                                 |
| sqlglot_transpile        | 2.20 ms                                                      | 4.33 ms: 1.97x slower                                 |
| mako                     | 15.9 ms                                                      | 32.0 ms: 2.00x slower                                 |
| logging_silent           | 130 ns                                                       | 262 ns: 2.02x slower                                  |
| scimark_sor              | 179 ms                                                       | 368 ms: 2.06x slower                                  |
| hexiom                   | 8.11 ms                                                      | 16.8 ms: 2.07x slower                                 |
| scimark_lu               | 146 ms                                                       | 305 ms: 2.09x slower                                  |
| chaos                    | 83.6 ms                                                      | 177 ms: 2.11x slower                                  |
| unpickle_pure_python     | 290 us                                                       | 619 us: 2.13x slower                                  |
| sympy_expand             | 601 ms                                                       | 1.30 sec: 2.17x slower                                |
| sqlglot_parse            | 1.76 ms                                                      | 3.84 ms: 2.18x slower                                 |
| sympy_sum                | 210 ms                                                       | 479 ms: 2.28x slower                                  |
| raytrace                 | 344 ms                                                       | 804 ms: 2.34x slower                                  |
| unpack_sequence          | 74.3 ns                                                      | 180 ns: 2.42x slower                                  |
| go                       | 191 ms                                                       | 465 ms: 2.43x slower                                  |
| nbody                    | 119 ms                                                       | 293 ms: 2.47x slower                                  |
| deltablue                | 4.44 ms                                                      | 12.0 ms: 2.70x slower                                 |
| Geometric mean           | (ref)                                                        | 1.46x slower                                          |

Benchmark hidden because not significant (9): xml_etree_iterparse, pidigits, xml_etree_parse, regex_effbot, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, regex_dna, asyncio_websockets, async_tree_none_tg
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.38x
- 95% likely to have a slowdown of 1.37x
- 99% likely to have a slowdown of 1.33x

# Memory
- memory change: 1.15x