# Results vs. 3.13.0rc2

- fork: python
- ref: e73e7a7abdc3fed252af
- machine: linux-x86_64
- commit hash: e73e7a7
- commit date: 2024-08-07
- overall geometric mean: 1.40x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 651 ms: 1.46x slower                                                  |
| docutils       | 4.01 sec                                                     | 4.92 sec: 1.23x slower                                                |
| html5lib       | 92.6 ms                                                      | 137 ms: 1.48x slower                                                  |
| tornado_http   | 251 ms                                                       | 319 ms: 1.27x slower                                                  |
| Geometric mean | (ref)                                                        | 1.35x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|---------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg          | 1.40 sec                                                     | 1.12 sec: 1.25x faster                                                |
| async_tree_io             | 1.39 sec                                                     | 1.25 sec: 1.11x faster                                                |
| async_tree_memoization_tg | 670 ms                                                       | 619 ms: 1.08x faster                                                  |
| async_tree_cpu_io_mixed   | 889 ms                                                       | 951 ms: 1.07x slower                                                  |
| asyncio_tcp               | 948 ms                                                       | 1.09 sec: 1.15x slower                                                |
| asyncio_tcp_ssl           | 2.77 sec                                                     | 3.34 sec: 1.20x slower                                                |
| async_generators          | 567 ms                                                       | 747 ms: 1.32x slower                                                  |
| coroutines                | 30.9 ms                                                      | 42.7 ms: 1.39x slower                                                 |
| Geometric mean            | (ref)                                                        | 1.05x slower                                                          |

Benchmark hidden because not significant (5): async_tree_none_tg, asyncio_websockets, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 239 ms: 1.05x faster                                                  |
| float          | 116 ms                                                       | 194 ms: 1.67x slower                                                  |
| nbody          | 119 ms                                                       | 281 ms: 2.37x slower                                                  |
| Geometric mean | (ref)                                                        | 1.56x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 35.6 ms: 1.09x slower                                                 |
| regex_compile  | 182 ms                                                       | 296 ms: 1.63x slower                                                  |
| Geometric mean | (ref)                                                        | 1.17x slower                                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 47.2 us                                                      | 43.1 us: 1.09x faster                                                 |
| xml_etree_parse      | 231 ms                                                       | 218 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 177 ms                                                       | 168 ms: 1.05x faster                                                  |
| unpickle             | 20.5 us                                                      | 22.3 us: 1.09x slower                                                 |
| unpickle_list        | 6.68 us                                                      | 7.70 us: 1.15x slower                                                 |
| json_loads           | 34.3 us                                                      | 41.2 us: 1.20x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 18.0 ms: 1.27x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 159 ms: 1.30x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 127 ms: 1.48x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 4.14 sec: 1.49x slower                                                |
| unpickle_pure_python | 290 us                                                       | 544 us: 1.87x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 846 us: 2.03x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.22x slower                                                          |

Benchmark hidden because not significant (2): pickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.4 ms: 1.26x slower                                                 |
| python_startup         | 22.4 ms                                                      | 28.9 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.28x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 111 ms: 1.54x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 53.4 ms: 1.69x slower                                                 |
| django_template | 44.3 ms                                                      | 79.6 ms: 1.80x slower                                                 |
| mako            | 15.9 ms                                                      | 31.0 ms: 1.94x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.74x slower                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|---------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal              | 5.70 ms                                                      | 4.19 ms: 1.36x faster                                                 |
| create_gc_cycles          | 2.41 ms                                                      | 1.80 ms: 1.34x faster                                                 |
| async_tree_io_tg          | 1.40 sec                                                     | 1.12 sec: 1.25x faster                                                |
| async_tree_io             | 1.39 sec                                                     | 1.25 sec: 1.11x faster                                                |
| pickle_dict               | 47.2 us                                                      | 43.1 us: 1.09x faster                                                 |
| async_tree_memoization_tg | 670 ms                                                       | 619 ms: 1.08x faster                                                  |
| xml_etree_parse           | 231 ms                                                       | 218 ms: 1.06x faster                                                  |
| xml_etree_iterparse       | 177 ms                                                       | 168 ms: 1.05x faster                                                  |
| pidigits                  | 251 ms                                                       | 239 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed   | 889 ms                                                       | 951 ms: 1.07x slower                                                  |
| regex_v8                  | 32.8 ms                                                      | 35.6 ms: 1.09x slower                                                 |
| unpickle                  | 20.5 us                                                      | 22.3 us: 1.09x slower                                                 |
| pathlib                   | 29.9 ms                                                      | 33.0 ms: 1.10x slower                                                 |
| sqlite_synth              | 3.99 us                                                      | 4.42 us: 1.11x slower                                                 |
| deepcopy                  | 498 us                                                       | 560 us: 1.12x slower                                                  |
| asyncio_tcp               | 948 ms                                                       | 1.09 sec: 1.15x slower                                                |
| telco                     | 12.2 ms                                                      | 14.0 ms: 1.15x slower                                                 |
| unpickle_list             | 6.68 us                                                      | 7.70 us: 1.15x slower                                                 |
| json_loads                | 34.3 us                                                      | 41.2 us: 1.20x slower                                                 |
| asyncio_tcp_ssl           | 2.77 sec                                                     | 3.34 sec: 1.20x slower                                                |
| docutils                  | 4.01 sec                                                     | 4.92 sec: 1.23x slower                                                |
| pylint                    | 470 ms                                                       | 579 ms: 1.23x slower                                                  |
| json                      | 6.51 ms                                                      | 8.10 ms: 1.24x slower                                                 |
| python_startup_no_site    | 15.3 ms                                                      | 19.4 ms: 1.26x slower                                                 |
| tornado_http              | 251 ms                                                       | 319 ms: 1.27x slower                                                  |
| json_dumps                | 14.1 ms                                                      | 18.0 ms: 1.27x slower                                                 |
| meteor_contest            | 150 ms                                                       | 192 ms: 1.28x slower                                                  |
| python_startup            | 22.4 ms                                                      | 28.9 ms: 1.29x slower                                                 |
| xml_etree_generate        | 122 ms                                                       | 159 ms: 1.30x slower                                                  |
| async_generators          | 567 ms                                                       | 747 ms: 1.32x slower                                                  |
| scimark_fft               | 473 ms                                                       | 624 ms: 1.32x slower                                                  |
| scimark_sparse_mat_mult   | 6.76 ms                                                      | 8.91 ms: 1.32x slower                                                 |
| deepcopy_memo             | 50.1 us                                                      | 67.1 us: 1.34x slower                                                 |
| mdp                       | 3.80 sec                                                     | 5.13 sec: 1.35x slower                                                |
| coverage                  | 107 ms                                                       | 146 ms: 1.36x slower                                                  |
| generators                | 40.0 ms                                                      | 55.0 ms: 1.38x slower                                                 |
| coroutines                | 30.9 ms                                                      | 42.7 ms: 1.39x slower                                                 |
| nqueens                   | 112 ms                                                       | 155 ms: 1.39x slower                                                  |
| deepcopy_reduce           | 4.10 us                                                      | 5.70 us: 1.39x slower                                                 |
| fannkuch                  | 547 ms                                                       | 762 ms: 1.39x slower                                                  |
| pycparser                 | 1.57 sec                                                     | 2.21 sec: 1.41x slower                                                |
| typing_runtime_protocols  | 226 us                                                       | 327 us: 1.45x slower                                                  |
| 2to3                      | 445 ms                                                       | 651 ms: 1.46x slower                                                  |
| html5lib                  | 92.6 ms                                                      | 137 ms: 1.48x slower                                                  |
| xml_etree_process         | 85.9 ms                                                      | 127 ms: 1.48x slower                                                  |
| sympy_integrate           | 30.2 ms                                                      | 44.9 ms: 1.49x slower                                                 |
| tomli_loads               | 2.78 sec                                                     | 4.14 sec: 1.49x slower                                                |
| richards                  | 65.5 ms                                                      | 99.2 ms: 1.52x slower                                                 |
| thrift                    | 1.10 ms                                                      | 1.67 ms: 1.52x slower                                                 |
| genshi_xml                | 72.1 ms                                                      | 111 ms: 1.54x slower                                                  |
| crypto_pyaes              | 100 ms                                                       | 156 ms: 1.56x slower                                                  |
| bench_thread_pool         | 2.89 ms                                                      | 4.52 ms: 1.57x slower                                                 |
| spectral_norm             | 157 ms                                                       | 247 ms: 1.58x slower                                                  |
| pyflate                   | 664 ms                                                       | 1.07 sec: 1.61x slower                                                |
| bpe_tokeniser             | 6.28 sec                                                     | 10.1 sec: 1.61x slower                                                |
| sqlglot_optimize          | 74.7 ms                                                      | 121 ms: 1.62x slower                                                  |
| regex_compile             | 182 ms                                                       | 296 ms: 1.63x slower                                                  |
| sqlglot_normalize         | 140 ms                                                       | 229 ms: 1.64x slower                                                  |
| pprint_safe_repr          | 987 ms                                                       | 1.65 sec: 1.67x slower                                                |
| float                     | 116 ms                                                       | 194 ms: 1.67x slower                                                  |
| genshi_text               | 31.7 ms                                                      | 53.4 ms: 1.69x slower                                                 |
| richards_super            | 73.2 ms                                                      | 127 ms: 1.73x slower                                                  |
| comprehensions            | 22.2 us                                                      | 38.7 us: 1.74x slower                                                 |
| pprint_pformat            | 1.94 sec                                                     | 3.39 sec: 1.74x slower                                                |
| scimark_monte_carlo       | 90.6 ms                                                      | 159 ms: 1.76x slower                                                  |
| logging_format            | 9.24 us                                                      | 16.4 us: 1.77x slower                                                 |
| sympy_str                 | 379 ms                                                       | 675 ms: 1.78x slower                                                  |
| logging_simple            | 8.56 us                                                      | 15.4 us: 1.79x slower                                                 |
| django_template           | 44.3 ms                                                      | 79.6 ms: 1.80x slower                                                 |
| unpickle_pure_python      | 290 us                                                       | 544 us: 1.87x slower                                                  |
| scimark_sor               | 179 ms                                                       | 340 ms: 1.90x slower                                                  |
| logging_silent            | 130 ns                                                       | 249 ns: 1.92x slower                                                  |
| mako                      | 15.9 ms                                                      | 31.0 ms: 1.94x slower                                                 |
| sqlglot_transpile         | 2.20 ms                                                      | 4.32 ms: 1.97x slower                                                 |
| hexiom                    | 8.11 ms                                                      | 16.3 ms: 2.01x slower                                                 |
| pickle_pure_python        | 416 us                                                       | 846 us: 2.03x slower                                                  |
| chaos                     | 83.6 ms                                                      | 170 ms: 2.03x slower                                                  |
| sympy_sum                 | 210 ms                                                       | 443 ms: 2.11x slower                                                  |
| scimark_lu                | 146 ms                                                       | 313 ms: 2.14x slower                                                  |
| sympy_expand              | 601 ms                                                       | 1.29 sec: 2.14x slower                                                |
| sqlglot_parse             | 1.76 ms                                                      | 3.76 ms: 2.14x slower                                                 |
| go                        | 191 ms                                                       | 434 ms: 2.27x slower                                                  |
| raytrace                  | 344 ms                                                       | 801 ms: 2.33x slower                                                  |
| nbody                     | 119 ms                                                       | 281 ms: 2.37x slower                                                  |
| unpack_sequence           | 74.3 ns                                                      | 190 ns: 2.56x slower                                                  |
| deltablue                 | 4.44 ms                                                      | 11.6 ms: 2.61x slower                                                 |
| Geometric mean            | (ref)                                                        | 1.40x slower                                                          |

Benchmark hidden because not significant (10): pickle, async_tree_none_tg, asyncio_websockets, bench_mp_pool, pickle_list, async_tree_memoization, async_tree_none, regex_effbot, async_tree_cpu_io_mixed_tg, regex_dna
Ignored benchmarks (6) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 1.14x