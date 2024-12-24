# Results vs. 3.13.0rc2

- fork: python
- ref: 30efede33ca1fe32debb
- machine: linux-x86_64
- commit hash: 30efede
- commit date: 2024-12-24
- overall geometric mean: 1.172x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 612 ms: 1.38x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.40 sec: 1.10x slower                                                 |
| html5lib       | 92.6 ms                                                      | 131 ms: 1.41x slower                                                   |
| Geometric mean | (ref)                                                        | 1.29x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 964 ms: 1.45x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 1.06 sec: 1.31x faster                                                 |
| async_tree_none_tg         | 504 ms                                                       | 421 ms: 1.20x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 571 ms: 1.17x faster                                                   |
| async_tree_none            | 572 ms                                                       | 504 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 776 ms: 1.10x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 671 ms: 1.06x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 35.0 ms: 1.13x slower                                                  |
| async_generators           | 567 ms                                                       | 658 ms: 1.16x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.10x faster                                                           |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 147 ms: 1.27x slower                                                   |
| nbody          | 119 ms                                                       | 177 ms: 1.49x slower                                                   |
| Geometric mean | (ref)                                                        | 1.22x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 300 ms: 1.07x slower                                                   |
| regex_v8       | 32.8 ms                                                      | 35.7 ms: 1.09x slower                                                  |
| regex_compile  | 182 ms                                                       | 219 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 148 ms: 1.19x faster                                                   |
| json_loads           | 34.3 us                                                      | 37.6 us: 1.10x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 3.25 sec: 1.17x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 101 ms: 1.18x slower                                                   |
| xml_etree_generate   | 122 ms                                                       | 147 ms: 1.20x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 17.6 ms: 1.25x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 418 us: 1.44x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 654 us: 1.57x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.17x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 20.4 ms: 1.33x slower                                                  |
| python_startup         | 22.4 ms                                                      | 31.0 ms: 1.39x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 87.7 ms: 1.22x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 40.0 ms: 1.26x slower                                                  |
| django_template | 44.3 ms                                                      | 59.3 ms: 1.34x slower                                                  |
| mako            | 15.9 ms                                                      | 26.8 ms: 1.68x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.36x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 964 ms: 1.45x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 1.06 sec: 1.31x faster                                                 |
| deepcopy                   | 498 us                                                       | 408 us: 1.22x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 421 ms: 1.20x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 148 ms: 1.19x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 571 ms: 1.17x faster                                                   |
| async_tree_none            | 572 ms                                                       | 504 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 776 ms: 1.10x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.68 us: 1.08x faster                                                  |
| async_tree_memoization     | 709 ms                                                       | 671 ms: 1.06x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 52.2 us: 1.04x slower                                                  |
| pathlib                    | 29.9 ms                                                      | 31.3 ms: 1.05x slower                                                  |
| spectral_norm              | 157 ms                                                       | 165 ms: 1.05x slower                                                   |
| regex_dna                  | 282 ms                                                       | 300 ms: 1.07x slower                                                   |
| telco                      | 12.2 ms                                                      | 13.0 ms: 1.07x slower                                                  |
| json                       | 6.51 ms                                                      | 7.04 ms: 1.08x slower                                                  |
| pylint                     | 470 ms                                                       | 509 ms: 1.08x slower                                                   |
| regex_v8                   | 32.8 ms                                                      | 35.7 ms: 1.09x slower                                                  |
| docutils                   | 4.01 sec                                                     | 4.40 sec: 1.10x slower                                                 |
| json_loads                 | 34.3 us                                                      | 37.6 us: 1.10x slower                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 4.57 us: 1.12x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 35.0 ms: 1.13x slower                                                  |
| mdp                        | 3.80 sec                                                     | 4.39 sec: 1.16x slower                                                 |
| async_generators           | 567 ms                                                       | 658 ms: 1.16x slower                                                   |
| scimark_fft                | 473 ms                                                       | 551 ms: 1.16x slower                                                   |
| nqueens                    | 112 ms                                                       | 130 ms: 1.17x slower                                                   |
| tomli_loads                | 2.78 sec                                                     | 3.25 sec: 1.17x slower                                                 |
| thrift                     | 1.10 ms                                                      | 1.29 ms: 1.18x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 101 ms: 1.18x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 35.8 ms: 1.18x slower                                                  |
| pycparser                  | 1.57 sec                                                     | 1.87 sec: 1.19x slower                                                 |
| sympy_expand               | 601 ms                                                       | 718 ms: 1.20x slower                                                   |
| xml_etree_generate         | 122 ms                                                       | 147 ms: 1.20x slower                                                   |
| gc_traversal               | 5.70 ms                                                      | 6.85 ms: 1.20x slower                                                  |
| regex_compile              | 182 ms                                                       | 219 ms: 1.20x slower                                                   |
| meteor_contest             | 150 ms                                                       | 181 ms: 1.21x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.18 ms: 1.21x slower                                                  |
| genshi_xml                 | 72.1 ms                                                      | 87.7 ms: 1.22x slower                                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 91.1 ms: 1.22x slower                                                  |
| sympy_str                  | 379 ms                                                       | 464 ms: 1.22x slower                                                   |
| dulwich_log                | 93.7 ms                                                      | 115 ms: 1.23x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 278 us: 1.23x slower                                                   |
| sympy_sum                  | 210 ms                                                       | 260 ms: 1.24x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 17.6 ms: 1.25x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 126 ms: 1.26x slower                                                   |
| genshi_text                | 31.7 ms                                                      | 40.0 ms: 1.26x slower                                                  |
| float                      | 116 ms                                                       | 147 ms: 1.27x slower                                                   |
| coverage                   | 107 ms                                                       | 136 ms: 1.27x slower                                                   |
| fannkuch                   | 547 ms                                                       | 697 ms: 1.27x slower                                                   |
| sqlglot_normalize          | 140 ms                                                       | 179 ms: 1.28x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 8.12 sec: 1.29x slower                                                 |
| pprint_safe_repr           | 987 ms                                                       | 1.28 sec: 1.30x slower                                                 |
| richards_super             | 73.2 ms                                                      | 96.8 ms: 1.32x slower                                                  |
| generators                 | 40.0 ms                                                      | 53.2 ms: 1.33x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 20.4 ms: 1.33x slower                                                  |
| django_template            | 44.3 ms                                                      | 59.3 ms: 1.34x slower                                                  |
| richards                   | 65.5 ms                                                      | 87.7 ms: 1.34x slower                                                  |
| logging_simple             | 8.56 us                                                      | 11.5 us: 1.34x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.62 sec: 1.35x slower                                                 |
| scimark_lu                 | 146 ms                                                       | 198 ms: 1.35x slower                                                   |
| 2to3                       | 445 ms                                                       | 612 ms: 1.38x slower                                                   |
| python_startup             | 22.4 ms                                                      | 31.0 ms: 1.39x slower                                                  |
| logging_format             | 9.24 us                                                      | 12.9 us: 1.40x slower                                                  |
| pyflate                    | 664 ms                                                       | 930 ms: 1.40x slower                                                   |
| create_gc_cycles           | 2.41 ms                                                      | 3.38 ms: 1.40x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 131 ms: 1.41x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 418 us: 1.44x slower                                                   |
| nbody                      | 119 ms                                                       | 177 ms: 1.49x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 4.32 ms: 1.50x slower                                                  |
| go                         | 191 ms                                                       | 289 ms: 1.51x slower                                                   |
| scimark_sor                | 179 ms                                                       | 272 ms: 1.52x slower                                                   |
| chaos                      | 83.6 ms                                                      | 129 ms: 1.55x slower                                                   |
| comprehensions             | 22.2 us                                                      | 34.7 us: 1.56x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 654 us: 1.57x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 142 ms: 1.57x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 13.0 ms: 1.60x slower                                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 3.60 ms: 1.64x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 2.94 ms: 1.68x slower                                                  |
| mako                       | 15.9 ms                                                      | 26.8 ms: 1.68x slower                                                  |
| logging_silent             | 130 ns                                                       | 222 ns: 1.71x slower                                                   |
| raytrace                   | 344 ms                                                       | 607 ms: 1.76x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 11.0 ms: 2.47x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 95.6 ms: 5.12x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.24x slower                                                           |

Benchmark hidden because not significant (5): pidigits, xml_etree_parse, async_tree_cpu_io_mixed, asyncio_websockets, regex_effbot
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.172x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.15x

# Memory
- memory change: 1.33x