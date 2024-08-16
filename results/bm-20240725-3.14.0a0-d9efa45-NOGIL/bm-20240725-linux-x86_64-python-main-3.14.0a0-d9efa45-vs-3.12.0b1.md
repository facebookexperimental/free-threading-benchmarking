# Results vs. 3.12.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d9efa45
- commit date: 2024-07-25
- overall geometric mean: 1.35x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 2.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 444 ms                                                                | 690 ms: 1.55x slower                                  |
| docutils       | 4.06 sec                                                              | 5.03 sec: 1.24x slower                                |
| html5lib       | 95.8 ms                                                               | 138 ms: 1.44x slower                                  |
| tornado_http   | 262 ms                                                                | 358 ms: 1.37x slower                                  |
| Geometric mean | (ref)                                                                 | 1.39x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.19 sec: 1.51x faster                                |
| async_tree_none_tg         | 692 ms                                                                | 471 ms: 1.47x faster                                  |
| async_tree_memoization_tg  | 935 ms                                                                | 641 ms: 1.46x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.28 sec: 1.40x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 843 ms: 1.30x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 744 ms: 1.28x faster                                  |
| async_tree_none            | 740 ms                                                                | 600 ms: 1.23x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 975 ms: 1.16x faster                                  |
| asyncio_tcp                | 958 ms                                                                | 1.10 sec: 1.15x slower                                |
| async_generators           | 617 ms                                                                | 741 ms: 1.20x slower                                  |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.42 sec: 1.22x slower                                |
| coroutines                 | 30.1 ms                                                               | 42.7 ms: 1.42x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.12x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 127 ms                                                                | 201 ms: 1.59x slower                                  |
| nbody          | 125 ms                                                                | 291 ms: 2.33x slower                                  |
| Geometric mean | (ref)                                                                 | 1.53x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.97 ms                                                               | 4.78 ms: 1.04x faster                                 |
| regex_v8       | 31.1 ms                                                               | 36.8 ms: 1.18x slower                                 |
| regex_compile  | 197 ms                                                                | 292 ms: 1.48x slower                                  |
| Geometric mean | (ref)                                                                 | 1.14x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 230 ms                                                                | 213 ms: 1.08x faster                                  |
| unpickle_list        | 7.19 us                                                               | 6.83 us: 1.05x faster                                 |
| unpickle             | 19.7 us                                                               | 22.0 us: 1.11x slower                                 |
| xml_etree_iterparse  | 157 ms                                                                | 177 ms: 1.13x slower                                  |
| json_loads           | 36.6 us                                                               | 44.5 us: 1.22x slower                                 |
| xml_etree_generate   | 128 ms                                                                | 163 ms: 1.27x slower                                  |
| json_dumps           | 13.6 ms                                                               | 18.3 ms: 1.35x slower                                 |
| tomli_loads          | 2.99 sec                                                              | 4.33 sec: 1.45x slower                                |
| xml_etree_process    | 85.7 ms                                                               | 137 ms: 1.60x slower                                  |
| pickle_pure_python   | 447 us                                                                | 768 us: 1.72x slower                                  |
| unpickle_pure_python | 319 us                                                                | 573 us: 1.80x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.22x slower                                          |

Benchmark hidden because not significant (3): pickle_dict, pickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 19.9 ms: 1.22x slower                                 |
| python_startup         | 21.2 ms                                                               | 29.3 ms: 1.38x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.30x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 117 ms: 1.59x slower                                  |
| django_template | 48.6 ms                                                               | 81.6 ms: 1.68x slower                                 |
| mako            | 17.2 ms                                                               | 29.5 ms: 1.71x slower                                 |
| genshi_text     | 31.9 ms                                                               | 57.9 ms: 1.82x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.70x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240725-linux-x86_64-python-main-3.14.0a0-d9efa45 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.19 sec: 1.51x faster                                |
| async_tree_none_tg         | 692 ms                                                                | 471 ms: 1.47x faster                                  |
| async_tree_memoization_tg  | 935 ms                                                                | 641 ms: 1.46x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.28 sec: 1.40x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 843 ms: 1.30x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 744 ms: 1.28x faster                                  |
| async_tree_none            | 740 ms                                                                | 600 ms: 1.23x faster                                  |
| gc_traversal               | 5.61 ms                                                               | 4.66 ms: 1.20x faster                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 975 ms: 1.16x faster                                  |
| bench_mp_pool              | 18.4 ms                                                               | 15.8 ms: 1.16x faster                                 |
| create_gc_cycles           | 2.02 ms                                                               | 1.87 ms: 1.08x faster                                 |
| xml_etree_parse            | 230 ms                                                                | 213 ms: 1.08x faster                                  |
| unpickle_list              | 7.19 us                                                               | 6.83 us: 1.05x faster                                 |
| regex_effbot               | 4.97 ms                                                               | 4.78 ms: 1.04x faster                                 |
| unpickle                   | 19.7 us                                                               | 22.0 us: 1.11x slower                                 |
| pathlib                    | 31.7 ms                                                               | 35.5 ms: 1.12x slower                                 |
| deepcopy                   | 503 us                                                                | 566 us: 1.12x slower                                  |
| xml_etree_iterparse        | 157 ms                                                                | 177 ms: 1.13x slower                                  |
| sqlite_synth               | 3.75 us                                                               | 4.23 us: 1.13x slower                                 |
| asyncio_tcp                | 958 ms                                                                | 1.10 sec: 1.15x slower                                |
| deepcopy_memo              | 57.5 us                                                               | 67.8 us: 1.18x slower                                 |
| regex_v8                   | 31.1 ms                                                               | 36.8 ms: 1.18x slower                                 |
| pylint                     | 501 ms                                                                | 595 ms: 1.19x slower                                  |
| async_generators           | 617 ms                                                                | 741 ms: 1.20x slower                                  |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 9.05 ms: 1.21x slower                                 |
| json_loads                 | 36.6 us                                                               | 44.5 us: 1.22x slower                                 |
| python_startup_no_site     | 16.3 ms                                                               | 19.9 ms: 1.22x slower                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.42 sec: 1.22x slower                                |
| docutils                   | 4.06 sec                                                              | 5.03 sec: 1.24x slower                                |
| scimark_fft                | 499 ms                                                                | 621 ms: 1.24x slower                                  |
| generators                 | 46.0 ms                                                               | 57.4 ms: 1.25x slower                                 |
| xml_etree_generate         | 128 ms                                                                | 163 ms: 1.27x slower                                  |
| json                       | 6.68 ms                                                               | 8.50 ms: 1.27x slower                                 |
| pycparser                  | 1.73 sec                                                              | 2.21 sec: 1.27x slower                                |
| bench_thread_pool          | 3.11 ms                                                               | 3.97 ms: 1.28x slower                                 |
| comprehensions             | 29.6 us                                                               | 39.2 us: 1.33x slower                                 |
| mdp                        | 3.84 sec                                                              | 5.12 sec: 1.33x slower                                |
| crypto_pyaes               | 112 ms                                                                | 149 ms: 1.33x slower                                  |
| json_dumps                 | 13.6 ms                                                               | 18.3 ms: 1.35x slower                                 |
| deepcopy_reduce            | 4.45 us                                                               | 6.02 us: 1.35x slower                                 |
| tornado_http               | 262 ms                                                                | 358 ms: 1.37x slower                                  |
| nqueens                    | 110 ms                                                                | 151 ms: 1.37x slower                                  |
| python_startup             | 21.2 ms                                                               | 29.3 ms: 1.38x slower                                 |
| meteor_contest             | 149 ms                                                                | 206 ms: 1.38x slower                                  |
| sympy_integrate            | 31.4 ms                                                               | 44.3 ms: 1.41x slower                                 |
| coroutines                 | 30.1 ms                                                               | 42.7 ms: 1.42x slower                                 |
| telco                      | 9.71 ms                                                               | 13.8 ms: 1.42x slower                                 |
| html5lib                   | 95.8 ms                                                               | 138 ms: 1.44x slower                                  |
| tomli_loads                | 2.99 sec                                                              | 4.33 sec: 1.45x slower                                |
| fannkuch                   | 551 ms                                                                | 802 ms: 1.46x slower                                  |
| regex_compile              | 197 ms                                                                | 292 ms: 1.48x slower                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 9.93 sec: 1.50x slower                                |
| thrift                     | 1.17 ms                                                               | 1.77 ms: 1.51x slower                                 |
| coverage                   | 97.6 ms                                                               | 149 ms: 1.53x slower                                  |
| logging_format             | 11.8 us                                                               | 18.2 us: 1.54x slower                                 |
| spectral_norm              | 158 ms                                                                | 244 ms: 1.55x slower                                  |
| 2to3                       | 444 ms                                                                | 690 ms: 1.55x slower                                  |
| sqlglot_normalize          | 148 ms                                                                | 233 ms: 1.57x slower                                  |
| float                      | 127 ms                                                                | 201 ms: 1.59x slower                                  |
| genshi_xml                 | 73.6 ms                                                               | 117 ms: 1.59x slower                                  |
| xml_etree_process          | 85.7 ms                                                               | 137 ms: 1.60x slower                                  |
| logging_simple             | 9.89 us                                                               | 15.9 us: 1.60x slower                                 |
| sqlglot_optimize           | 76.5 ms                                                               | 123 ms: 1.61x slower                                  |
| richards                   | 63.4 ms                                                               | 105 ms: 1.65x slower                                  |
| pyflate                    | 661 ms                                                                | 1.09 sec: 1.66x slower                                |
| sympy_str                  | 425 ms                                                                | 713 ms: 1.68x slower                                  |
| django_template            | 48.6 ms                                                               | 81.6 ms: 1.68x slower                                 |
| scimark_monte_carlo        | 98.5 ms                                                               | 168 ms: 1.71x slower                                  |
| mako                       | 17.2 ms                                                               | 29.5 ms: 1.71x slower                                 |
| pickle_pure_python         | 447 us                                                                | 768 us: 1.72x slower                                  |
| pprint_pformat             | 2.03 sec                                                              | 3.60 sec: 1.78x slower                                |
| pprint_safe_repr           | 970 ms                                                                | 1.74 sec: 1.79x slower                                |
| unpickle_pure_python       | 319 us                                                                | 573 us: 1.80x slower                                  |
| genshi_text                | 31.9 ms                                                               | 57.9 ms: 1.82x slower                                 |
| hexiom                     | 8.87 ms                                                               | 16.3 ms: 1.84x slower                                 |
| chaos                      | 93.7 ms                                                               | 175 ms: 1.87x slower                                  |
| sympy_expand               | 689 ms                                                                | 1.29 sec: 1.88x slower                                |
| typing_runtime_protocols   | 199 us                                                                | 377 us: 1.89x slower                                  |
| logging_silent             | 135 ns                                                                | 259 ns: 1.91x slower                                  |
| raytrace                   | 418 ms                                                                | 805 ms: 1.93x slower                                  |
| richards_super             | 67.9 ms                                                               | 134 ms: 1.97x slower                                  |
| scimark_sor                | 171 ms                                                                | 342 ms: 2.00x slower                                  |
| sqlglot_parse              | 1.89 ms                                                               | 3.81 ms: 2.01x slower                                 |
| sqlglot_transpile          | 2.28 ms                                                               | 4.65 ms: 2.04x slower                                 |
| scimark_lu                 | 155 ms                                                                | 323 ms: 2.09x slower                                  |
| sympy_sum                  | 229 ms                                                                | 487 ms: 2.13x slower                                  |
| go                         | 185 ms                                                                | 405 ms: 2.19x slower                                  |
| nbody                      | 125 ms                                                                | 291 ms: 2.33x slower                                  |
| deltablue                  | 5.05 ms                                                               | 12.1 ms: 2.40x slower                                 |
| unpack_sequence            | 68.5 ns                                                               | 190 ns: 2.78x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.35x slower                                          |

Benchmark hidden because not significant (6): pickle_dict, pidigits, pickle, asyncio_websockets, regex_dna, pickle_list
Ignored benchmarks (9) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.31x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 2.26x