# Results vs. 3.13.0rc2

- fork: python
- ref: c9b399fbdb01584dcfff
- machine: linux-x86_64
- commit hash: c9b399f
- commit date: 2024-11-19
- overall geometric mean: 1.43x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.35x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 648 ms: 1.46x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.60 sec: 1.15x slower                                                 |
| html5lib       | 92.6 ms                                                      | 147 ms: 1.58x slower                                                   |
| Geometric mean | (ref)                                                        | 1.38x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|--------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 766 ms                                                       | 744 ms: 1.03x faster                                                   |
| asyncio_tcp        | 948 ms                                                       | 1.03 sec: 1.09x slower                                                 |
| asyncio_tcp_ssl    | 2.77 sec                                                     | 3.21 sec: 1.16x slower                                                 |
| async_generators   | 567 ms                                                       | 679 ms: 1.20x slower                                                   |
| coroutines         | 30.9 ms                                                      | 40.9 ms: 1.32x slower                                                  |
| Geometric mean     | (ref)                                                        | 1.14x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 201 ms: 1.74x slower                                                   |
| nbody          | 119 ms                                                       | 257 ms: 2.16x slower                                                   |
| Geometric mean | (ref)                                                        | 1.55x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 36.3 ms: 1.11x slower                                                  |
| regex_compile  | 182 ms                                                       | 287 ms: 1.58x slower                                                   |
| Geometric mean | (ref)                                                        | 1.14x slower                                                           |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 231 ms                                                       | 212 ms: 1.09x faster                                                   |
| xml_etree_iterparse  | 177 ms                                                       | 167 ms: 1.06x faster                                                   |
| pickle               | 15.1 us                                                      | 15.7 us: 1.04x slower                                                  |
| unpickle_list        | 6.68 us                                                      | 7.70 us: 1.15x slower                                                  |
| json_loads           | 34.3 us                                                      | 40.7 us: 1.19x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 164 ms: 1.34x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 19.5 ms: 1.38x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 126 ms: 1.47x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 4.09 sec: 1.47x slower                                                 |
| unpickle_pure_python | 290 us                                                       | 524 us: 1.81x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 776 us: 1.86x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.22x slower                                                           |

Benchmark hidden because not significant (3): pickle_dict, pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 18.8 ms: 1.22x slower                                                  |
| python_startup         | 22.4 ms                                                      | 29.5 ms: 1.32x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.27x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 112 ms: 1.55x slower                                                   |
| genshi_text     | 31.7 ms                                                      | 50.2 ms: 1.59x slower                                                  |
| django_template | 44.3 ms                                                      | 79.0 ms: 1.78x slower                                                  |
| mako            | 15.9 ms                                                      | 30.4 ms: 1.91x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.70x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 5.70 ms                                                      | 4.04 ms: 1.41x faster                                                  |
| create_gc_cycles         | 2.41 ms                                                      | 1.83 ms: 1.32x faster                                                  |
| xml_etree_parse          | 231 ms                                                       | 212 ms: 1.09x faster                                                   |
| xml_etree_iterparse      | 177 ms                                                       | 167 ms: 1.06x faster                                                   |
| asyncio_websockets       | 766 ms                                                       | 744 ms: 1.03x faster                                                   |
| pickle                   | 15.1 us                                                      | 15.7 us: 1.04x slower                                                  |
| telco                    | 12.2 ms                                                      | 13.1 ms: 1.08x slower                                                  |
| asyncio_tcp              | 948 ms                                                       | 1.03 sec: 1.09x slower                                                 |
| regex_v8                 | 32.8 ms                                                      | 36.3 ms: 1.11x slower                                                  |
| deepcopy                 | 498 us                                                       | 564 us: 1.13x slower                                                   |
| docutils                 | 4.01 sec                                                     | 4.60 sec: 1.15x slower                                                 |
| scimark_fft              | 473 ms                                                       | 545 ms: 1.15x slower                                                   |
| unpickle_list            | 6.68 us                                                      | 7.70 us: 1.15x slower                                                  |
| json                     | 6.51 ms                                                      | 7.53 ms: 1.16x slower                                                  |
| pathlib                  | 29.9 ms                                                      | 34.6 ms: 1.16x slower                                                  |
| bench_thread_pool        | 2.89 ms                                                      | 3.34 ms: 1.16x slower                                                  |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.21 sec: 1.16x slower                                                 |
| json_loads               | 34.3 us                                                      | 40.7 us: 1.19x slower                                                  |
| async_generators         | 567 ms                                                       | 679 ms: 1.20x slower                                                   |
| python_startup_no_site   | 15.3 ms                                                      | 18.8 ms: 1.22x slower                                                  |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 8.36 ms: 1.24x slower                                                  |
| pylint                   | 470 ms                                                       | 589 ms: 1.25x slower                                                   |
| mdp                      | 3.80 sec                                                     | 4.79 sec: 1.26x slower                                                 |
| meteor_contest           | 150 ms                                                       | 191 ms: 1.27x slower                                                   |
| python_startup           | 22.4 ms                                                      | 29.5 ms: 1.32x slower                                                  |
| coroutines               | 30.9 ms                                                      | 40.9 ms: 1.32x slower                                                  |
| spectral_norm            | 157 ms                                                       | 209 ms: 1.33x slower                                                   |
| generators               | 40.0 ms                                                      | 53.5 ms: 1.34x slower                                                  |
| xml_etree_generate       | 122 ms                                                       | 164 ms: 1.34x slower                                                   |
| pycparser                | 1.57 sec                                                     | 2.13 sec: 1.35x slower                                                 |
| coverage                 | 107 ms                                                       | 147 ms: 1.37x slower                                                   |
| nqueens                  | 112 ms                                                       | 153 ms: 1.37x slower                                                   |
| json_dumps               | 14.1 ms                                                      | 19.5 ms: 1.38x slower                                                  |
| fannkuch                 | 547 ms                                                       | 759 ms: 1.39x slower                                                   |
| dulwich_log              | 93.7 ms                                                      | 130 ms: 1.39x slower                                                   |
| deepcopy_memo            | 50.1 us                                                      | 69.9 us: 1.39x slower                                                  |
| bpe_tokeniser            | 6.28 sec                                                     | 8.77 sec: 1.40x slower                                                 |
| deepcopy_reduce          | 4.10 us                                                      | 5.74 us: 1.40x slower                                                  |
| sympy_integrate          | 30.2 ms                                                      | 43.3 ms: 1.43x slower                                                  |
| 2to3                     | 445 ms                                                       | 648 ms: 1.46x slower                                                   |
| crypto_pyaes             | 100 ms                                                       | 146 ms: 1.46x slower                                                   |
| xml_etree_process        | 85.9 ms                                                      | 126 ms: 1.47x slower                                                   |
| tomli_loads              | 2.78 sec                                                     | 4.09 sec: 1.47x slower                                                 |
| thrift                   | 1.10 ms                                                      | 1.65 ms: 1.50x slower                                                  |
| genshi_xml               | 72.1 ms                                                      | 112 ms: 1.55x slower                                                   |
| typing_runtime_protocols | 226 us                                                       | 353 us: 1.57x slower                                                   |
| sqlglot_optimize         | 74.7 ms                                                      | 117 ms: 1.57x slower                                                   |
| pyflate                  | 664 ms                                                       | 1.04 sec: 1.57x slower                                                 |
| regex_compile            | 182 ms                                                       | 287 ms: 1.58x slower                                                   |
| html5lib                 | 92.6 ms                                                      | 147 ms: 1.58x slower                                                   |
| genshi_text              | 31.7 ms                                                      | 50.2 ms: 1.59x slower                                                  |
| comprehensions           | 22.2 us                                                      | 35.7 us: 1.61x slower                                                  |
| richards                 | 65.5 ms                                                      | 107 ms: 1.64x slower                                                   |
| sqlglot_normalize        | 140 ms                                                       | 232 ms: 1.66x slower                                                   |
| pprint_safe_repr         | 987 ms                                                       | 1.64 sec: 1.67x slower                                                 |
| scimark_monte_carlo      | 90.6 ms                                                      | 154 ms: 1.70x slower                                                   |
| pprint_pformat           | 1.94 sec                                                     | 3.37 sec: 1.74x slower                                                 |
| float                    | 116 ms                                                       | 201 ms: 1.74x slower                                                   |
| sympy_str                | 379 ms                                                       | 662 ms: 1.75x slower                                                   |
| richards_super           | 73.2 ms                                                      | 128 ms: 1.75x slower                                                   |
| logging_simple           | 8.56 us                                                      | 15.1 us: 1.76x slower                                                  |
| go                       | 191 ms                                                       | 336 ms: 1.76x slower                                                   |
| django_template          | 44.3 ms                                                      | 79.0 ms: 1.78x slower                                                  |
| logging_format           | 9.24 us                                                      | 16.6 us: 1.80x slower                                                  |
| unpickle_pure_python     | 290 us                                                       | 524 us: 1.81x slower                                                   |
| chaos                    | 83.6 ms                                                      | 153 ms: 1.83x slower                                                   |
| pickle_pure_python       | 416 us                                                       | 776 us: 1.86x slower                                                   |
| scimark_sor              | 179 ms                                                       | 334 ms: 1.87x slower                                                   |
| logging_silent           | 130 ns                                                       | 246 ns: 1.89x slower                                                   |
| mako                     | 15.9 ms                                                      | 30.4 ms: 1.91x slower                                                  |
| sqlglot_transpile        | 2.20 ms                                                      | 4.23 ms: 1.93x slower                                                  |
| scimark_lu               | 146 ms                                                       | 290 ms: 1.98x slower                                                   |
| hexiom                   | 8.11 ms                                                      | 16.3 ms: 2.01x slower                                                  |
| sympy_expand             | 601 ms                                                       | 1.21 sec: 2.02x slower                                                 |
| raytrace                 | 344 ms                                                       | 741 ms: 2.15x slower                                                   |
| nbody                    | 119 ms                                                       | 257 ms: 2.16x slower                                                   |
| sqlglot_parse            | 1.76 ms                                                      | 3.82 ms: 2.18x slower                                                  |
| sympy_sum                | 210 ms                                                       | 482 ms: 2.30x slower                                                   |
| deltablue                | 4.44 ms                                                      | 11.3 ms: 2.54x slower                                                  |
| unpack_sequence          | 74.3 ns                                                      | 209 ns: 2.81x slower                                                   |
| bench_mp_pool            | 18.7 ms                                                      | 63.7 ms: 3.41x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.43x slower                                                           |

Benchmark hidden because not significant (7): regex_effbot, pickle_dict, pickle_list, pidigits, regex_dna, sqlite_synth, unpickle
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.38x
- 95% likely to have a slowdown of 1.36x
- 99% likely to have a slowdown of 1.35x

# Memory
- memory change: 1.19x