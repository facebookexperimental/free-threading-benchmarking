# Results vs. 3.12.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 8145ebe
- commit date: 2024-09-12
- overall geometric mean: 1.35x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 2.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 444 ms                                                                | 669 ms: 1.51x slower                                  |
| docutils       | 4.06 sec                                                              | 4.89 sec: 1.20x slower                                |
| html5lib       | 95.8 ms                                                               | 133 ms: 1.39x slower                                  |
| tornado_http   | 262 ms                                                                | 374 ms: 1.42x slower                                  |
| Geometric mean | (ref)                                                                 | 1.38x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.17 sec: 1.54x faster                                |
| async_tree_io              | 1.79 sec                                                              | 1.24 sec: 1.44x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 651 ms: 1.44x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 497 ms: 1.39x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 844 ms: 1.30x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 751 ms: 1.26x faster                                  |
| async_tree_none            | 740 ms                                                                | 609 ms: 1.21x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 948 ms: 1.20x faster                                  |
| asyncio_websockets         | 766 ms                                                                | 802 ms: 1.05x slower                                  |
| asyncio_tcp                | 958 ms                                                                | 1.10 sec: 1.15x slower                                |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.36 sec: 1.20x slower                                |
| async_generators           | 617 ms                                                                | 742 ms: 1.20x slower                                  |
| coroutines                 | 30.1 ms                                                               | 44.4 ms: 1.47x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.12x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 127 ms                                                                | 196 ms: 1.55x slower                                  |
| nbody          | 125 ms                                                                | 281 ms: 2.26x slower                                  |
| Geometric mean | (ref)                                                                 | 1.50x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.97 ms                                                               | 4.42 ms: 1.12x faster                                 |
| regex_v8       | 31.1 ms                                                               | 37.2 ms: 1.20x slower                                 |
| regex_compile  | 197 ms                                                                | 288 ms: 1.46x slower                                  |
| Geometric mean | (ref)                                                                 | 1.11x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| unpickle_list        | 7.19 us                                                               | 7.64 us: 1.06x slower                                 |
| pickle_list          | 6.40 us                                                               | 6.85 us: 1.07x slower                                 |
| xml_etree_iterparse  | 157 ms                                                                | 175 ms: 1.11x slower                                  |
| unpickle             | 19.7 us                                                               | 22.3 us: 1.13x slower                                 |
| json_loads           | 36.6 us                                                               | 41.7 us: 1.14x slower                                 |
| json_dumps           | 13.6 ms                                                               | 17.8 ms: 1.31x slower                                 |
| xml_etree_generate   | 128 ms                                                                | 170 ms: 1.32x slower                                  |
| tomli_loads          | 2.99 sec                                                              | 4.34 sec: 1.45x slower                                |
| xml_etree_process    | 85.7 ms                                                               | 126 ms: 1.47x slower                                  |
| unpickle_pure_python | 319 us                                                                | 516 us: 1.62x slower                                  |
| pickle_pure_python   | 447 us                                                                | 847 us: 1.89x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.23x slower                                          |

Benchmark hidden because not significant (3): pickle_dict, xml_etree_parse, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 21.3 ms: 1.31x slower                                 |
| python_startup         | 21.2 ms                                                               | 32.2 ms: 1.52x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.41x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 118 ms: 1.60x slower                                  |
| django_template | 48.6 ms                                                               | 85.0 ms: 1.75x slower                                 |
| mako            | 17.2 ms                                                               | 31.6 ms: 1.84x slower                                 |
| genshi_text     | 31.9 ms                                                               | 60.8 ms: 1.91x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.77x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240912-linux-x86_64-python-main-3.14.0a0-8145ebe |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.17 sec: 1.54x faster                                |
| async_tree_io              | 1.79 sec                                                              | 1.24 sec: 1.44x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 651 ms: 1.44x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 497 ms: 1.39x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 844 ms: 1.30x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 751 ms: 1.26x faster                                  |
| async_tree_none            | 740 ms                                                                | 609 ms: 1.21x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 948 ms: 1.20x faster                                  |
| gc_traversal               | 5.61 ms                                                               | 4.89 ms: 1.15x faster                                 |
| regex_effbot               | 4.97 ms                                                               | 4.42 ms: 1.12x faster                                 |
| asyncio_websockets         | 766 ms                                                                | 802 ms: 1.05x slower                                  |
| unpickle_list              | 7.19 us                                                               | 7.64 us: 1.06x slower                                 |
| pickle_list                | 6.40 us                                                               | 6.85 us: 1.07x slower                                 |
| pathlib                    | 31.7 ms                                                               | 35.3 ms: 1.11x slower                                 |
| xml_etree_iterparse        | 157 ms                                                                | 175 ms: 1.11x slower                                  |
| unpickle                   | 19.7 us                                                               | 22.3 us: 1.13x slower                                 |
| json_loads                 | 36.6 us                                                               | 41.7 us: 1.14x slower                                 |
| generators                 | 46.0 ms                                                               | 52.8 ms: 1.15x slower                                 |
| asyncio_tcp                | 958 ms                                                                | 1.10 sec: 1.15x slower                                |
| deepcopy                   | 503 us                                                                | 581 us: 1.15x slower                                  |
| sqlite_synth               | 3.75 us                                                               | 4.43 us: 1.18x slower                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 8.92 ms: 1.19x slower                                 |
| regex_v8                   | 31.1 ms                                                               | 37.2 ms: 1.20x slower                                 |
| deepcopy_memo              | 57.5 us                                                               | 68.8 us: 1.20x slower                                 |
| json                       | 6.68 ms                                                               | 8.00 ms: 1.20x slower                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.36 sec: 1.20x slower                                |
| async_generators           | 617 ms                                                                | 742 ms: 1.20x slower                                  |
| docutils                   | 4.06 sec                                                              | 4.89 sec: 1.20x slower                                |
| pylint                     | 501 ms                                                                | 610 ms: 1.22x slower                                  |
| comprehensions             | 29.6 us                                                               | 37.2 us: 1.26x slower                                 |
| scimark_fft                | 499 ms                                                                | 631 ms: 1.26x slower                                  |
| pycparser                  | 1.73 sec                                                              | 2.24 sec: 1.29x slower                                |
| json_dumps                 | 13.6 ms                                                               | 17.8 ms: 1.31x slower                                 |
| python_startup_no_site     | 16.3 ms                                                               | 21.3 ms: 1.31x slower                                 |
| xml_etree_generate         | 128 ms                                                                | 170 ms: 1.32x slower                                  |
| deepcopy_reduce            | 4.45 us                                                               | 5.91 us: 1.33x slower                                 |
| crypto_pyaes               | 112 ms                                                                | 151 ms: 1.35x slower                                  |
| mdp                        | 3.84 sec                                                              | 5.21 sec: 1.36x slower                                |
| logging_format             | 11.8 us                                                               | 16.3 us: 1.38x slower                                 |
| html5lib                   | 95.8 ms                                                               | 133 ms: 1.39x slower                                  |
| dulwich_log                | 114 ms                                                                | 159 ms: 1.39x slower                                  |
| fannkuch                   | 551 ms                                                                | 767 ms: 1.39x slower                                  |
| meteor_contest             | 149 ms                                                                | 208 ms: 1.40x slower                                  |
| nqueens                    | 110 ms                                                                | 155 ms: 1.41x slower                                  |
| tornado_http               | 262 ms                                                                | 374 ms: 1.42x slower                                  |
| telco                      | 9.71 ms                                                               | 13.9 ms: 1.43x slower                                 |
| tomli_loads                | 2.99 sec                                                              | 4.34 sec: 1.45x slower                                |
| thrift                     | 1.17 ms                                                               | 1.71 ms: 1.46x slower                                 |
| regex_compile              | 197 ms                                                                | 288 ms: 1.46x slower                                  |
| xml_etree_process          | 85.7 ms                                                               | 126 ms: 1.47x slower                                  |
| coroutines                 | 30.1 ms                                                               | 44.4 ms: 1.47x slower                                 |
| sympy_integrate            | 31.4 ms                                                               | 46.3 ms: 1.48x slower                                 |
| 2to3                       | 444 ms                                                                | 669 ms: 1.51x slower                                  |
| python_startup             | 21.2 ms                                                               | 32.2 ms: 1.52x slower                                 |
| bench_thread_pool          | 3.11 ms                                                               | 4.74 ms: 1.53x slower                                 |
| logging_simple             | 9.89 us                                                               | 15.2 us: 1.53x slower                                 |
| sqlglot_optimize           | 76.5 ms                                                               | 117 ms: 1.53x slower                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 10.2 sec: 1.55x slower                                |
| float                      | 127 ms                                                                | 196 ms: 1.55x slower                                  |
| spectral_norm              | 158 ms                                                                | 245 ms: 1.56x slower                                  |
| pyflate                    | 661 ms                                                                | 1.04 sec: 1.57x slower                                |
| coverage                   | 97.6 ms                                                               | 156 ms: 1.60x slower                                  |
| genshi_xml                 | 73.6 ms                                                               | 118 ms: 1.60x slower                                  |
| sympy_str                  | 425 ms                                                                | 687 ms: 1.62x slower                                  |
| unpickle_pure_python       | 319 us                                                                | 516 us: 1.62x slower                                  |
| typing_runtime_protocols   | 199 us                                                                | 334 us: 1.68x slower                                  |
| sqlglot_normalize          | 148 ms                                                                | 250 ms: 1.69x slower                                  |
| scimark_monte_carlo        | 98.5 ms                                                               | 166 ms: 1.69x slower                                  |
| chaos                      | 93.7 ms                                                               | 159 ms: 1.70x slower                                  |
| richards                   | 63.4 ms                                                               | 108 ms: 1.70x slower                                  |
| pprint_pformat             | 2.03 sec                                                              | 3.52 sec: 1.73x slower                                |
| pprint_safe_repr           | 970 ms                                                                | 1.69 sec: 1.74x slower                                |
| django_template            | 48.6 ms                                                               | 85.0 ms: 1.75x slower                                 |
| hexiom                     | 8.87 ms                                                               | 16.0 ms: 1.80x slower                                 |
| richards_super             | 67.9 ms                                                               | 123 ms: 1.81x slower                                  |
| raytrace                   | 418 ms                                                                | 766 ms: 1.83x slower                                  |
| mako                       | 17.2 ms                                                               | 31.6 ms: 1.84x slower                                 |
| pickle_pure_python         | 447 us                                                                | 847 us: 1.89x slower                                  |
| logging_silent             | 135 ns                                                                | 256 ns: 1.90x slower                                  |
| genshi_text                | 31.9 ms                                                               | 60.8 ms: 1.91x slower                                 |
| sympy_expand               | 689 ms                                                                | 1.33 sec: 1.93x slower                                |
| sqlglot_transpile          | 2.28 ms                                                               | 4.40 ms: 1.93x slower                                 |
| go                         | 185 ms                                                                | 361 ms: 1.95x slower                                  |
| scimark_lu                 | 155 ms                                                                | 307 ms: 1.99x slower                                  |
| scimark_sor                | 171 ms                                                                | 345 ms: 2.01x slower                                  |
| sqlglot_parse              | 1.89 ms                                                               | 3.90 ms: 2.06x slower                                 |
| sympy_sum                  | 229 ms                                                                | 491 ms: 2.14x slower                                  |
| nbody                      | 125 ms                                                                | 281 ms: 2.26x slower                                  |
| deltablue                  | 5.05 ms                                                               | 11.6 ms: 2.31x slower                                 |
| unpack_sequence            | 68.5 ns                                                               | 201 ns: 2.93x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.35x slower                                          |

Benchmark hidden because not significant (7): pidigits, pickle_dict, bench_mp_pool, xml_etree_parse, regex_dna, create_gc_cycles, pickle
Ignored benchmarks (8) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 2.24x