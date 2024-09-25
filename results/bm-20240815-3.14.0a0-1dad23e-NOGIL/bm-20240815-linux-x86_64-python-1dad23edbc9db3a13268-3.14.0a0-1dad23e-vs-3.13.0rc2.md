# Results vs. 3.13.0rc2

- fork: python
- ref: 1dad23edbc9db3a13268
- machine: linux-x86_64
- commit hash: 1dad23e
- commit date: 2024-08-15
- overall geometric mean: 1.46x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.34x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 687 ms: 1.54x slower                                                  |
| docutils       | 4.01 sec                                                     | 5.35 sec: 1.33x slower                                                |
| html5lib       | 92.6 ms                                                      | 147 ms: 1.59x slower                                                  |
| tornado_http   | 251 ms                                                       | 350 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                        | 1.46x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg       | 1.40 sec                                                     | 1.14 sec: 1.23x faster                                                |
| async_tree_io          | 1.39 sec                                                     | 1.28 sec: 1.09x faster                                                |
| async_tree_memoization | 709 ms                                                       | 774 ms: 1.09x slower                                                  |
| async_tree_none        | 572 ms                                                       | 626 ms: 1.09x slower                                                  |
| asyncio_tcp            | 948 ms                                                       | 1.16 sec: 1.22x slower                                                |
| asyncio_tcp_ssl        | 2.77 sec                                                     | 3.47 sec: 1.25x slower                                                |
| async_generators       | 567 ms                                                       | 731 ms: 1.29x slower                                                  |
| coroutines             | 30.9 ms                                                      | 42.9 ms: 1.39x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                          |

Benchmark hidden because not significant (5): async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, asyncio_websockets, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 195 ms: 1.68x slower                                                  |
| nbody          | 119 ms                                                       | 307 ms: 2.58x slower                                                  |
| Geometric mean | (ref)                                                        | 1.63x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 5.00 ms: 1.06x slower                                                 |
| regex_dna      | 282 ms                                                       | 300 ms: 1.06x slower                                                  |
| regex_v8       | 32.8 ms                                                      | 36.8 ms: 1.12x slower                                                 |
| regex_compile  | 182 ms                                                       | 310 ms: 1.70x slower                                                  |
| Geometric mean | (ref)                                                        | 1.21x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 47.2 us                                                      | 42.2 us: 1.12x faster                                                 |
| pickle               | 15.1 us                                                      | 13.8 us: 1.09x faster                                                 |
| unpickle             | 20.5 us                                                      | 23.4 us: 1.14x slower                                                 |
| unpickle_list        | 6.68 us                                                      | 7.89 us: 1.18x slower                                                 |
| json_loads           | 34.3 us                                                      | 44.8 us: 1.31x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 19.0 ms: 1.34x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 167 ms: 1.36x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 130 ms: 1.51x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 4.23 sec: 1.52x slower                                                |
| pickle_pure_python   | 416 us                                                       | 783 us: 1.88x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 578 us: 1.99x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                          |

Benchmark hidden because not significant (3): pickle_list, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 20.9 ms: 1.37x slower                                                 |
| python_startup         | 22.4 ms                                                      | 30.8 ms: 1.38x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 124 ms: 1.72x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 55.2 ms: 1.74x slower                                                 |
| mako            | 15.9 ms                                                      | 31.5 ms: 1.98x slower                                                 |
| django_template | 44.3 ms                                                      | 87.7 ms: 1.98x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.85x slower                                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|--------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| create_gc_cycles         | 2.41 ms                                                      | 1.87 ms: 1.29x faster                                                 |
| async_tree_io_tg         | 1.40 sec                                                     | 1.14 sec: 1.23x faster                                                |
| gc_traversal             | 5.70 ms                                                      | 5.05 ms: 1.13x faster                                                 |
| pickle_dict              | 47.2 us                                                      | 42.2 us: 1.12x faster                                                 |
| pickle                   | 15.1 us                                                      | 13.8 us: 1.09x faster                                                 |
| async_tree_io            | 1.39 sec                                                     | 1.28 sec: 1.09x faster                                                |
| regex_effbot             | 4.74 ms                                                      | 5.00 ms: 1.06x slower                                                 |
| regex_dna                | 282 ms                                                       | 300 ms: 1.06x slower                                                  |
| sqlite_synth             | 3.99 us                                                      | 4.29 us: 1.08x slower                                                 |
| async_tree_memoization   | 709 ms                                                       | 774 ms: 1.09x slower                                                  |
| async_tree_none          | 572 ms                                                       | 626 ms: 1.09x slower                                                  |
| regex_v8                 | 32.8 ms                                                      | 36.8 ms: 1.12x slower                                                 |
| telco                    | 12.2 ms                                                      | 13.7 ms: 1.13x slower                                                 |
| unpickle                 | 20.5 us                                                      | 23.4 us: 1.14x slower                                                 |
| unpickle_list            | 6.68 us                                                      | 7.89 us: 1.18x slower                                                 |
| asyncio_tcp              | 948 ms                                                       | 1.16 sec: 1.22x slower                                                |
| pathlib                  | 29.9 ms                                                      | 37.4 ms: 1.25x slower                                                 |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.47 sec: 1.25x slower                                                |
| deepcopy                 | 498 us                                                       | 626 us: 1.26x slower                                                  |
| async_generators         | 567 ms                                                       | 731 ms: 1.29x slower                                                  |
| pylint                   | 470 ms                                                       | 606 ms: 1.29x slower                                                  |
| json_loads               | 34.3 us                                                      | 44.8 us: 1.31x slower                                                 |
| json                     | 6.51 ms                                                      | 8.59 ms: 1.32x slower                                                 |
| docutils                 | 4.01 sec                                                     | 5.35 sec: 1.33x slower                                                |
| json_dumps               | 14.1 ms                                                      | 19.0 ms: 1.34x slower                                                 |
| meteor_contest           | 150 ms                                                       | 202 ms: 1.35x slower                                                  |
| xml_etree_generate       | 122 ms                                                       | 167 ms: 1.36x slower                                                  |
| python_startup_no_site   | 15.3 ms                                                      | 20.9 ms: 1.37x slower                                                 |
| python_startup           | 22.4 ms                                                      | 30.8 ms: 1.38x slower                                                 |
| mdp                      | 3.80 sec                                                     | 5.24 sec: 1.38x slower                                                |
| scimark_fft              | 473 ms                                                       | 657 ms: 1.39x slower                                                  |
| coroutines               | 30.9 ms                                                      | 42.9 ms: 1.39x slower                                                 |
| tornado_http             | 251 ms                                                       | 350 ms: 1.39x slower                                                  |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 9.49 ms: 1.41x slower                                                 |
| pycparser                | 1.57 sec                                                     | 2.23 sec: 1.42x slower                                                |
| generators               | 40.0 ms                                                      | 58.2 ms: 1.45x slower                                                 |
| nqueens                  | 112 ms                                                       | 164 ms: 1.47x slower                                                  |
| coverage                 | 107 ms                                                       | 159 ms: 1.48x slower                                                  |
| fannkuch                 | 547 ms                                                       | 814 ms: 1.49x slower                                                  |
| sympy_integrate          | 30.2 ms                                                      | 45.4 ms: 1.50x slower                                                 |
| thrift                   | 1.10 ms                                                      | 1.66 ms: 1.51x slower                                                 |
| xml_etree_process        | 85.9 ms                                                      | 130 ms: 1.51x slower                                                  |
| typing_runtime_protocols | 226 us                                                       | 342 us: 1.51x slower                                                  |
| tomli_loads              | 2.78 sec                                                     | 4.23 sec: 1.52x slower                                                |
| 2to3                     | 445 ms                                                       | 687 ms: 1.54x slower                                                  |
| deepcopy_memo            | 50.1 us                                                      | 77.4 us: 1.54x slower                                                 |
| spectral_norm            | 157 ms                                                       | 247 ms: 1.58x slower                                                  |
| html5lib                 | 92.6 ms                                                      | 147 ms: 1.59x slower                                                  |
| crypto_pyaes             | 100 ms                                                       | 161 ms: 1.61x slower                                                  |
| deepcopy_reduce          | 4.10 us                                                      | 6.61 us: 1.61x slower                                                 |
| richards                 | 65.5 ms                                                      | 107 ms: 1.63x slower                                                  |
| sqlglot_optimize         | 74.7 ms                                                      | 122 ms: 1.63x slower                                                  |
| sqlglot_normalize        | 140 ms                                                       | 235 ms: 1.68x slower                                                  |
| float                    | 116 ms                                                       | 195 ms: 1.68x slower                                                  |
| pyflate                  | 664 ms                                                       | 1.12 sec: 1.69x slower                                                |
| bpe_tokeniser            | 6.28 sec                                                     | 10.7 sec: 1.70x slower                                                |
| regex_compile            | 182 ms                                                       | 310 ms: 1.70x slower                                                  |
| genshi_xml               | 72.1 ms                                                      | 124 ms: 1.72x slower                                                  |
| logging_simple           | 8.56 us                                                      | 14.9 us: 1.74x slower                                                 |
| genshi_text              | 31.7 ms                                                      | 55.2 ms: 1.74x slower                                                 |
| comprehensions           | 22.2 us                                                      | 39.2 us: 1.76x slower                                                 |
| scimark_monte_carlo      | 90.6 ms                                                      | 161 ms: 1.78x slower                                                  |
| pprint_safe_repr         | 987 ms                                                       | 1.80 sec: 1.82x slower                                                |
| richards_super           | 73.2 ms                                                      | 133 ms: 1.82x slower                                                  |
| sympy_str                | 379 ms                                                       | 697 ms: 1.84x slower                                                  |
| bench_thread_pool        | 2.89 ms                                                      | 5.33 ms: 1.85x slower                                                 |
| pprint_pformat           | 1.94 sec                                                     | 3.62 sec: 1.86x slower                                                |
| logging_format           | 9.24 us                                                      | 17.3 us: 1.87x slower                                                 |
| pickle_pure_python       | 416 us                                                       | 783 us: 1.88x slower                                                  |
| mako                     | 15.9 ms                                                      | 31.5 ms: 1.98x slower                                                 |
| django_template          | 44.3 ms                                                      | 87.7 ms: 1.98x slower                                                 |
| scimark_sor              | 179 ms                                                       | 355 ms: 1.99x slower                                                  |
| unpickle_pure_python     | 290 us                                                       | 578 us: 1.99x slower                                                  |
| logging_silent           | 130 ns                                                       | 266 ns: 2.05x slower                                                  |
| hexiom                   | 8.11 ms                                                      | 16.9 ms: 2.09x slower                                                 |
| sympy_expand             | 601 ms                                                       | 1.26 sec: 2.09x slower                                                |
| sqlglot_transpile        | 2.20 ms                                                      | 4.65 ms: 2.12x slower                                                 |
| chaos                    | 83.6 ms                                                      | 177 ms: 2.12x slower                                                  |
| sqlglot_parse            | 1.76 ms                                                      | 3.77 ms: 2.14x slower                                                 |
| scimark_lu               | 146 ms                                                       | 319 ms: 2.18x slower                                                  |
| sympy_sum                | 210 ms                                                       | 462 ms: 2.20x slower                                                  |
| raytrace                 | 344 ms                                                       | 789 ms: 2.29x slower                                                  |
| go                       | 191 ms                                                       | 440 ms: 2.30x slower                                                  |
| nbody                    | 119 ms                                                       | 307 ms: 2.58x slower                                                  |
| deltablue                | 4.44 ms                                                      | 11.8 ms: 2.66x slower                                                 |
| unpack_sequence          | 74.3 ns                                                      | 212 ns: 2.85x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.46x slower                                                          |

Benchmark hidden because not significant (10): async_tree_none_tg, pickle_list, async_tree_cpu_io_mixed_tg, bench_mp_pool, xml_etree_parse, xml_etree_iterparse, pidigits, async_tree_memoization_tg, asyncio_websockets, async_tree_cpu_io_mixed
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.39x
- 95% likely to have a slowdown of 1.38x
- 99% likely to have a slowdown of 1.34x

# Memory
- memory change: 1.15x