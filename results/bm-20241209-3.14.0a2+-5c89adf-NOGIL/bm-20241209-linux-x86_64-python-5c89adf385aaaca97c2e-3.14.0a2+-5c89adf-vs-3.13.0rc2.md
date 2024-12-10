# Results vs. 3.13.0rc2

- fork: python
- ref: 5c89adf385aaaca97c2e
- machine: linux-x86_64
- commit hash: 5c89adf
- commit date: 2024-12-09
- overall geometric mean: 1.194x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 616 ms: 1.38x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.37 sec: 1.09x slower                                                 |
| html5lib       | 92.6 ms                                                      | 129 ms: 1.40x slower                                                   |
| Geometric mean | (ref)                                                        | 1.28x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|---------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg          | 1.40 sec                                                     | 1.05 sec: 1.33x faster                                                 |
| async_tree_io             | 1.39 sec                                                     | 1.08 sec: 1.29x faster                                                 |
| async_tree_memoization_tg | 670 ms                                                       | 609 ms: 1.10x faster                                                   |
| async_tree_none_tg        | 504 ms                                                       | 464 ms: 1.09x faster                                                   |
| async_tree_memoization    | 709 ms                                                       | 657 ms: 1.08x faster                                                   |
| async_tree_none           | 572 ms                                                       | 530 ms: 1.08x faster                                                   |
| async_tree_cpu_io_mixed   | 889 ms                                                       | 842 ms: 1.06x faster                                                   |
| coroutines                | 30.9 ms                                                      | 33.6 ms: 1.09x slower                                                  |
| async_generators          | 567 ms                                                       | 654 ms: 1.15x slower                                                   |
| Geometric mean            | (ref)                                                        | 1.07x faster                                                           |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 229 ms: 1.09x faster                                                   |
| float          | 116 ms                                                       | 169 ms: 1.46x slower                                                   |
| nbody          | 119 ms                                                       | 176 ms: 1.48x slower                                                   |
| Geometric mean | (ref)                                                        | 1.25x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.40 ms: 1.08x faster                                                  |
| regex_dna      | 282 ms                                                       | 296 ms: 1.05x slower                                                   |
| regex_compile  | 182 ms                                                       | 225 ms: 1.24x slower                                                   |
| Geometric mean | (ref)                                                        | 1.05x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 147 ms: 1.20x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 216 ms: 1.07x faster                                                   |
| xml_etree_generate   | 122 ms                                                       | 131 ms: 1.07x slower                                                   |
| json_loads           | 34.3 us                                                      | 38.4 us: 1.12x slower                                                  |
| xml_etree_process    | 85.9 ms                                                      | 101 ms: 1.18x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.50 sec: 1.26x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 17.8 ms: 1.26x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 411 us: 1.42x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 626 us: 1.50x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.9 ms: 1.30x slower                                                  |
| python_startup         | 22.4 ms                                                      | 32.3 ms: 1.44x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 91.5 ms: 1.27x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 42.8 ms: 1.35x slower                                                  |
| django_template | 44.3 ms                                                      | 63.7 ms: 1.44x slower                                                  |
| mako            | 15.9 ms                                                      | 26.9 ms: 1.68x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.43x slower                                                           |

All benchmarks:
===============

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|---------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg          | 1.40 sec                                                     | 1.05 sec: 1.33x faster                                                 |
| async_tree_io             | 1.39 sec                                                     | 1.08 sec: 1.29x faster                                                 |
| xml_etree_iterparse       | 177 ms                                                       | 147 ms: 1.20x faster                                                   |
| deepcopy                  | 498 us                                                       | 417 us: 1.19x faster                                                   |
| async_tree_memoization_tg | 670 ms                                                       | 609 ms: 1.10x faster                                                   |
| pidigits                  | 251 ms                                                       | 229 ms: 1.09x faster                                                   |
| sqlite_synth              | 3.99 us                                                      | 3.67 us: 1.09x faster                                                  |
| async_tree_none_tg        | 504 ms                                                       | 464 ms: 1.09x faster                                                   |
| async_tree_memoization    | 709 ms                                                       | 657 ms: 1.08x faster                                                   |
| async_tree_none           | 572 ms                                                       | 530 ms: 1.08x faster                                                   |
| regex_effbot              | 4.74 ms                                                      | 4.40 ms: 1.08x faster                                                  |
| xml_etree_parse           | 231 ms                                                       | 216 ms: 1.07x faster                                                   |
| telco                     | 12.2 ms                                                      | 11.5 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed   | 889 ms                                                       | 842 ms: 1.06x faster                                                   |
| regex_dna                 | 282 ms                                                       | 296 ms: 1.05x slower                                                   |
| xml_etree_generate        | 122 ms                                                       | 131 ms: 1.07x slower                                                   |
| pathlib                   | 29.9 ms                                                      | 32.2 ms: 1.08x slower                                                  |
| coroutines                | 30.9 ms                                                      | 33.6 ms: 1.09x slower                                                  |
| docutils                  | 4.01 sec                                                     | 4.37 sec: 1.09x slower                                                 |
| gc_traversal              | 5.70 ms                                                      | 6.22 ms: 1.09x slower                                                  |
| pylint                    | 470 ms                                                       | 526 ms: 1.12x slower                                                   |
| json_loads                | 34.3 us                                                      | 38.4 us: 1.12x slower                                                  |
| spectral_norm             | 157 ms                                                       | 177 ms: 1.13x slower                                                   |
| meteor_contest            | 150 ms                                                       | 171 ms: 1.14x slower                                                   |
| async_generators          | 567 ms                                                       | 654 ms: 1.15x slower                                                   |
| deepcopy_reduce           | 4.10 us                                                      | 4.73 us: 1.15x slower                                                  |
| xml_etree_process         | 85.9 ms                                                      | 101 ms: 1.18x slower                                                   |
| mdp                       | 3.80 sec                                                     | 4.50 sec: 1.19x slower                                                 |
| bpe_tokeniser             | 6.28 sec                                                     | 7.47 sec: 1.19x slower                                                 |
| scimark_sparse_mat_mult   | 6.76 ms                                                      | 8.09 ms: 1.20x slower                                                  |
| nqueens                   | 112 ms                                                       | 134 ms: 1.20x slower                                                   |
| scimark_fft               | 473 ms                                                       | 570 ms: 1.20x slower                                                   |
| typing_runtime_protocols  | 226 us                                                       | 273 us: 1.21x slower                                                   |
| sqlglot_optimize          | 74.7 ms                                                      | 90.7 ms: 1.21x slower                                                  |
| pycparser                 | 1.57 sec                                                     | 1.92 sec: 1.23x slower                                                 |
| regex_compile             | 182 ms                                                       | 225 ms: 1.24x slower                                                   |
| crypto_pyaes              | 100 ms                                                       | 125 ms: 1.25x slower                                                   |
| fannkuch                  | 547 ms                                                       | 682 ms: 1.25x slower                                                   |
| tomli_loads               | 2.78 sec                                                     | 3.50 sec: 1.26x slower                                                 |
| dulwich_log               | 93.7 ms                                                      | 118 ms: 1.26x slower                                                   |
| json_dumps                | 14.1 ms                                                      | 17.8 ms: 1.26x slower                                                  |
| sqlglot_normalize         | 140 ms                                                       | 177 ms: 1.27x slower                                                   |
| genshi_xml                | 72.1 ms                                                      | 91.5 ms: 1.27x slower                                                  |
| coverage                  | 107 ms                                                       | 137 ms: 1.27x slower                                                   |
| sympy_integrate           | 30.2 ms                                                      | 39.0 ms: 1.29x slower                                                  |
| generators                | 40.0 ms                                                      | 51.8 ms: 1.29x slower                                                  |
| python_startup_no_site    | 15.3 ms                                                      | 19.9 ms: 1.30x slower                                                  |
| pprint_safe_repr          | 987 ms                                                       | 1.29 sec: 1.31x slower                                                 |
| thrift                    | 1.10 ms                                                      | 1.47 ms: 1.33x slower                                                  |
| genshi_text               | 31.7 ms                                                      | 42.8 ms: 1.35x slower                                                  |
| pprint_pformat            | 1.94 sec                                                     | 2.67 sec: 1.37x slower                                                 |
| richards                  | 65.5 ms                                                      | 90.6 ms: 1.38x slower                                                  |
| 2to3                      | 445 ms                                                       | 616 ms: 1.38x slower                                                   |
| comprehensions            | 22.2 us                                                      | 31.0 us: 1.39x slower                                                  |
| html5lib                  | 92.6 ms                                                      | 129 ms: 1.40x slower                                                   |
| pyflate                   | 664 ms                                                       | 929 ms: 1.40x slower                                                   |
| create_gc_cycles          | 2.41 ms                                                      | 3.38 ms: 1.40x slower                                                  |
| richards_super            | 73.2 ms                                                      | 103 ms: 1.40x slower                                                   |
| unpickle_pure_python      | 290 us                                                       | 411 us: 1.42x slower                                                   |
| django_template           | 44.3 ms                                                      | 63.7 ms: 1.44x slower                                                  |
| python_startup            | 22.4 ms                                                      | 32.3 ms: 1.44x slower                                                  |
| float                     | 116 ms                                                       | 169 ms: 1.46x slower                                                   |
| scimark_lu                | 146 ms                                                       | 215 ms: 1.47x slower                                                   |
| nbody                     | 119 ms                                                       | 176 ms: 1.48x slower                                                   |
| pickle_pure_python        | 416 us                                                       | 626 us: 1.50x slower                                                   |
| bench_thread_pool         | 2.89 ms                                                      | 4.35 ms: 1.51x slower                                                  |
| logging_simple            | 8.56 us                                                      | 13.1 us: 1.53x slower                                                  |
| logging_format            | 9.24 us                                                      | 14.3 us: 1.55x slower                                                  |
| sympy_str                 | 379 ms                                                       | 589 ms: 1.55x slower                                                   |
| chaos                     | 83.6 ms                                                      | 130 ms: 1.56x slower                                                   |
| scimark_monte_carlo       | 90.6 ms                                                      | 142 ms: 1.57x slower                                                   |
| go                        | 191 ms                                                       | 322 ms: 1.68x slower                                                   |
| mako                      | 15.9 ms                                                      | 26.9 ms: 1.68x slower                                                  |
| scimark_sor               | 179 ms                                                       | 302 ms: 1.69x slower                                                   |
| hexiom                    | 8.11 ms                                                      | 13.9 ms: 1.71x slower                                                  |
| sympy_expand              | 601 ms                                                       | 1.10 sec: 1.83x slower                                                 |
| raytrace                  | 344 ms                                                       | 634 ms: 1.84x slower                                                   |
| sqlglot_parse             | 1.76 ms                                                      | 3.25 ms: 1.85x slower                                                  |
| sqlglot_transpile         | 2.20 ms                                                      | 4.19 ms: 1.91x slower                                                  |
| logging_silent            | 130 ns                                                       | 250 ns: 1.92x slower                                                   |
| sympy_sum                 | 210 ms                                                       | 413 ms: 1.97x slower                                                   |
| deltablue                 | 4.44 ms                                                      | 10.3 ms: 2.32x slower                                                  |
| bench_mp_pool             | 18.7 ms                                                      | 98.3 ms: 5.26x slower                                                  |
| Geometric mean            | (ref)                                                        | 1.27x slower                                                           |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed_tg, asyncio_websockets, deepcopy_memo, regex_v8, json
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.194x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.18x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.33x