# Results vs. 3.12.0b1

- fork: python
- ref: a15feded71dd47202db1
- machine: linux-x86_64
- commit hash: a15fede
- commit date: 2024-07-23
- overall geometric mean: 1.35x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 2.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 444 ms                                                                | 650 ms: 1.46x slower                                                  |
| docutils       | 4.06 sec                                                              | 4.88 sec: 1.20x slower                                                |
| html5lib       | 95.8 ms                                                               | 139 ms: 1.46x slower                                                  |
| tornado_http   | 262 ms                                                                | 349 ms: 1.33x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.36x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.16 sec: 1.55x faster                                                |
| async_tree_none_tg         | 692 ms                                                                | 485 ms: 1.43x faster                                                  |
| async_tree_memoization_tg  | 935 ms                                                                | 671 ms: 1.39x faster                                                  |
| async_tree_io              | 1.79 sec                                                              | 1.30 sec: 1.38x faster                                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 817 ms: 1.35x faster                                                  |
| async_tree_memoization     | 949 ms                                                                | 721 ms: 1.32x faster                                                  |
| async_tree_none            | 740 ms                                                                | 588 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 944 ms: 1.20x faster                                                  |
| asyncio_tcp                | 958 ms                                                                | 1.12 sec: 1.17x slower                                                |
| async_generators           | 617 ms                                                                | 739 ms: 1.20x slower                                                  |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.36 sec: 1.20x slower                                                |
| coroutines                 | 30.1 ms                                                               | 43.2 ms: 1.43x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.13x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 255 ms                                                                | 243 ms: 1.05x faster                                                  |
| float          | 127 ms                                                                | 202 ms: 1.59x slower                                                  |
| nbody          | 125 ms                                                                | 288 ms: 2.31x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.52x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.97 ms                                                               | 4.57 ms: 1.09x faster                                                 |
| regex_v8       | 31.1 ms                                                               | 36.3 ms: 1.17x slower                                                 |
| regex_compile  | 197 ms                                                                | 291 ms: 1.48x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.13x slower                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 46.5 us                                                               | 42.5 us: 1.10x faster                                                 |
| xml_etree_iterparse  | 157 ms                                                                | 169 ms: 1.07x slower                                                  |
| unpickle             | 19.7 us                                                               | 22.3 us: 1.13x slower                                                 |
| unpickle_list        | 7.19 us                                                               | 8.14 us: 1.13x slower                                                 |
| json_loads           | 36.6 us                                                               | 42.7 us: 1.17x slower                                                 |
| xml_etree_generate   | 128 ms                                                                | 162 ms: 1.27x slower                                                  |
| json_dumps           | 13.6 ms                                                               | 19.0 ms: 1.40x slower                                                 |
| tomli_loads          | 2.99 sec                                                              | 4.22 sec: 1.41x slower                                                |
| xml_etree_process    | 85.7 ms                                                               | 127 ms: 1.48x slower                                                  |
| pickle_pure_python   | 447 us                                                                | 805 us: 1.80x slower                                                  |
| unpickle_pure_python | 319 us                                                                | 609 us: 1.91x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.23x slower                                                          |

Benchmark hidden because not significant (3): pickle, pickle_list, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 20.6 ms: 1.27x slower                                                 |
| python_startup         | 21.2 ms                                                               | 29.7 ms: 1.40x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.33x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 116 ms: 1.57x slower                                                  |
| django_template | 48.6 ms                                                               | 80.4 ms: 1.66x slower                                                 |
| genshi_text     | 31.9 ms                                                               | 54.9 ms: 1.72x slower                                                 |
| mako            | 17.2 ms                                                               | 30.4 ms: 1.76x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.68x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.16 sec: 1.55x faster                                                |
| async_tree_none_tg         | 692 ms                                                                | 485 ms: 1.43x faster                                                  |
| async_tree_memoization_tg  | 935 ms                                                                | 671 ms: 1.39x faster                                                  |
| async_tree_io              | 1.79 sec                                                              | 1.30 sec: 1.38x faster                                                |
| bench_mp_pool              | 18.4 ms                                                               | 13.4 ms: 1.37x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 817 ms: 1.35x faster                                                  |
| async_tree_memoization     | 949 ms                                                                | 721 ms: 1.32x faster                                                  |
| async_tree_none            | 740 ms                                                                | 588 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 944 ms: 1.20x faster                                                  |
| gc_traversal               | 5.61 ms                                                               | 4.76 ms: 1.18x faster                                                 |
| pickle_dict                | 46.5 us                                                               | 42.5 us: 1.10x faster                                                 |
| regex_effbot               | 4.97 ms                                                               | 4.57 ms: 1.09x faster                                                 |
| pidigits                   | 255 ms                                                                | 243 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 157 ms                                                                | 169 ms: 1.07x slower                                                  |
| pathlib                    | 31.7 ms                                                               | 34.8 ms: 1.10x slower                                                 |
| unpickle                   | 19.7 us                                                               | 22.3 us: 1.13x slower                                                 |
| unpickle_list              | 7.19 us                                                               | 8.14 us: 1.13x slower                                                 |
| sqlite_synth               | 3.75 us                                                               | 4.35 us: 1.16x slower                                                 |
| asyncio_tcp                | 958 ms                                                                | 1.12 sec: 1.17x slower                                                |
| regex_v8                   | 31.1 ms                                                               | 36.3 ms: 1.17x slower                                                 |
| json_loads                 | 36.6 us                                                               | 42.7 us: 1.17x slower                                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 8.89 ms: 1.19x slower                                                 |
| json                       | 6.68 ms                                                               | 7.98 ms: 1.20x slower                                                 |
| async_generators           | 617 ms                                                                | 739 ms: 1.20x slower                                                  |
| docutils                   | 4.06 sec                                                              | 4.88 sec: 1.20x slower                                                |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.36 sec: 1.20x slower                                                |
| deepcopy                   | 503 us                                                                | 606 us: 1.20x slower                                                  |
| pylint                     | 501 ms                                                                | 607 ms: 1.21x slower                                                  |
| generators                 | 46.0 ms                                                               | 58.0 ms: 1.26x slower                                                 |
| python_startup_no_site     | 16.3 ms                                                               | 20.6 ms: 1.27x slower                                                 |
| xml_etree_generate         | 128 ms                                                                | 162 ms: 1.27x slower                                                  |
| deepcopy_memo              | 57.5 us                                                               | 72.8 us: 1.27x slower                                                 |
| scimark_fft                | 499 ms                                                                | 633 ms: 1.27x slower                                                  |
| dulwich_log                | 114 ms                                                                | 146 ms: 1.28x slower                                                  |
| bench_thread_pool          | 3.11 ms                                                               | 4.01 ms: 1.29x slower                                                 |
| pycparser                  | 1.73 sec                                                              | 2.28 sec: 1.31x slower                                                |
| meteor_contest             | 149 ms                                                                | 196 ms: 1.32x slower                                                  |
| comprehensions             | 29.6 us                                                               | 39.2 us: 1.33x slower                                                 |
| tornado_http               | 262 ms                                                                | 349 ms: 1.33x slower                                                  |
| mdp                        | 3.84 sec                                                              | 5.14 sec: 1.34x slower                                                |
| deepcopy_reduce            | 4.45 us                                                               | 6.01 us: 1.35x slower                                                 |
| telco                      | 9.71 ms                                                               | 13.2 ms: 1.36x slower                                                 |
| sympy_integrate            | 31.4 ms                                                               | 43.3 ms: 1.38x slower                                                 |
| crypto_pyaes               | 112 ms                                                                | 155 ms: 1.38x slower                                                  |
| python_startup             | 21.2 ms                                                               | 29.7 ms: 1.40x slower                                                 |
| json_dumps                 | 13.6 ms                                                               | 19.0 ms: 1.40x slower                                                 |
| tomli_loads                | 2.99 sec                                                              | 4.22 sec: 1.41x slower                                                |
| nqueens                    | 110 ms                                                                | 157 ms: 1.43x slower                                                  |
| coroutines                 | 30.1 ms                                                               | 43.2 ms: 1.43x slower                                                 |
| html5lib                   | 95.8 ms                                                               | 139 ms: 1.46x slower                                                  |
| logging_format             | 11.8 us                                                               | 17.3 us: 1.46x slower                                                 |
| 2to3                       | 444 ms                                                                | 650 ms: 1.46x slower                                                  |
| fannkuch                   | 551 ms                                                                | 808 ms: 1.47x slower                                                  |
| xml_etree_process          | 85.7 ms                                                               | 127 ms: 1.48x slower                                                  |
| regex_compile              | 197 ms                                                                | 291 ms: 1.48x slower                                                  |
| thrift                     | 1.17 ms                                                               | 1.74 ms: 1.49x slower                                                 |
| coverage                   | 97.6 ms                                                               | 150 ms: 1.53x slower                                                  |
| logging_simple             | 9.89 us                                                               | 15.3 us: 1.54x slower                                                 |
| spectral_norm              | 158 ms                                                                | 246 ms: 1.56x slower                                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 10.3 sec: 1.56x slower                                                |
| sympy_str                  | 425 ms                                                                | 667 ms: 1.57x slower                                                  |
| genshi_xml                 | 73.6 ms                                                               | 116 ms: 1.57x slower                                                  |
| float                      | 127 ms                                                                | 202 ms: 1.59x slower                                                  |
| sqlglot_normalize          | 148 ms                                                                | 238 ms: 1.60x slower                                                  |
| django_template            | 48.6 ms                                                               | 80.4 ms: 1.66x slower                                                 |
| sqlglot_optimize           | 76.5 ms                                                               | 128 ms: 1.67x slower                                                  |
| typing_runtime_protocols   | 199 us                                                                | 339 us: 1.70x slower                                                  |
| pyflate                    | 661 ms                                                                | 1.13 sec: 1.71x slower                                                |
| genshi_text                | 31.9 ms                                                               | 54.9 ms: 1.72x slower                                                 |
| scimark_monte_carlo        | 98.5 ms                                                               | 171 ms: 1.74x slower                                                  |
| pprint_safe_repr           | 970 ms                                                                | 1.71 sec: 1.76x slower                                                |
| mako                       | 17.2 ms                                                               | 30.4 ms: 1.76x slower                                                 |
| pprint_pformat             | 2.03 sec                                                              | 3.58 sec: 1.77x slower                                                |
| pickle_pure_python         | 447 us                                                                | 805 us: 1.80x slower                                                  |
| richards                   | 63.4 ms                                                               | 115 ms: 1.82x slower                                                  |
| sympy_expand               | 689 ms                                                                | 1.25 sec: 1.82x slower                                                |
| hexiom                     | 8.87 ms                                                               | 16.2 ms: 1.82x slower                                                 |
| logging_silent             | 135 ns                                                                | 251 ns: 1.86x slower                                                  |
| chaos                      | 93.7 ms                                                               | 175 ms: 1.86x slower                                                  |
| unpickle_pure_python       | 319 us                                                                | 609 us: 1.91x slower                                                  |
| raytrace                   | 418 ms                                                                | 802 ms: 1.92x slower                                                  |
| scimark_sor                | 171 ms                                                                | 341 ms: 1.99x slower                                                  |
| richards_super             | 67.9 ms                                                               | 136 ms: 2.00x slower                                                  |
| sympy_sum                  | 229 ms                                                                | 477 ms: 2.08x slower                                                  |
| sqlglot_parse              | 1.89 ms                                                               | 3.96 ms: 2.09x slower                                                 |
| scimark_lu                 | 155 ms                                                                | 332 ms: 2.15x slower                                                  |
| sqlglot_transpile          | 2.28 ms                                                               | 4.92 ms: 2.15x slower                                                 |
| go                         | 185 ms                                                                | 421 ms: 2.28x slower                                                  |
| nbody                      | 125 ms                                                                | 288 ms: 2.31x slower                                                  |
| deltablue                  | 5.05 ms                                                               | 11.7 ms: 2.31x slower                                                 |
| unpack_sequence            | 68.5 ns                                                               | 210 ns: 3.06x slower                                                  |
| Geometric mean             | (ref)                                                                 | 1.35x slower                                                          |

Benchmark hidden because not significant (6): create_gc_cycles, pickle, asyncio_websockets, pickle_list, xml_etree_parse, regex_dna
Ignored benchmarks (8) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.31x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 2.27x