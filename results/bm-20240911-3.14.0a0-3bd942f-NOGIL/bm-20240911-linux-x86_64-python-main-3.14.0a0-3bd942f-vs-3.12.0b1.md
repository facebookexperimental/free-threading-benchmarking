# Results vs. 3.12.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 3bd942f
- commit date: 2024-09-11
- overall geometric mean: 1.34x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x slower
- Memory change: 2.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 444 ms                                                                | 626 ms: 1.41x slower                                  |
| docutils       | 4.06 sec                                                              | 4.76 sec: 1.17x slower                                |
| html5lib       | 95.8 ms                                                               | 141 ms: 1.47x slower                                  |
| tornado_http   | 262 ms                                                                | 352 ms: 1.34x slower                                  |
| Geometric mean | (ref)                                                                 | 1.34x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.13 sec: 1.60x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 653 ms: 1.43x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 495 ms: 1.40x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.31 sec: 1.36x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 829 ms: 1.33x faster                                  |
| async_tree_none            | 740 ms                                                                | 575 ms: 1.29x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 748 ms: 1.27x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 980 ms: 1.16x faster                                  |
| asyncio_websockets         | 766 ms                                                                | 738 ms: 1.04x faster                                  |
| asyncio_tcp                | 958 ms                                                                | 1.09 sec: 1.14x slower                                |
| async_generators           | 617 ms                                                                | 712 ms: 1.15x slower                                  |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.27 sec: 1.17x slower                                |
| coroutines                 | 30.1 ms                                                               | 45.1 ms: 1.50x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.13x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 255 ms                                                                | 242 ms: 1.05x faster                                  |
| float          | 127 ms                                                                | 201 ms: 1.58x slower                                  |
| nbody          | 125 ms                                                                | 312 ms: 2.50x slower                                  |
| Geometric mean | (ref)                                                                 | 1.56x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.97 ms                                                               | 4.56 ms: 1.09x faster                                 |
| regex_v8       | 31.1 ms                                                               | 36.1 ms: 1.16x slower                                 |
| regex_compile  | 197 ms                                                                | 290 ms: 1.47x slower                                  |
| Geometric mean | (ref)                                                                 | 1.12x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 46.5 us                                                               | 43.5 us: 1.07x faster                                 |
| unpickle_list        | 7.19 us                                                               | 7.59 us: 1.06x slower                                 |
| xml_etree_iterparse  | 157 ms                                                                | 175 ms: 1.11x slower                                  |
| unpickle             | 19.7 us                                                               | 22.7 us: 1.15x slower                                 |
| json_loads           | 36.6 us                                                               | 42.8 us: 1.17x slower                                 |
| xml_etree_generate   | 128 ms                                                                | 157 ms: 1.22x slower                                  |
| json_dumps           | 13.6 ms                                                               | 18.9 ms: 1.39x slower                                 |
| xml_etree_process    | 85.7 ms                                                               | 121 ms: 1.42x slower                                  |
| tomli_loads          | 2.99 sec                                                              | 4.35 sec: 1.46x slower                                |
| unpickle_pure_python | 319 us                                                                | 547 us: 1.71x slower                                  |
| pickle_pure_python   | 447 us                                                                | 804 us: 1.80x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.22x slower                                          |

Benchmark hidden because not significant (3): pickle_list, pickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 21.2 ms: 1.30x slower                                 |
| python_startup         | 21.2 ms                                                               | 30.9 ms: 1.46x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.38x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 116 ms: 1.57x slower                                  |
| django_template | 48.6 ms                                                               | 83.8 ms: 1.73x slower                                 |
| mako            | 17.2 ms                                                               | 31.2 ms: 1.81x slower                                 |
| genshi_text     | 31.9 ms                                                               | 58.2 ms: 1.83x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.73x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240911-linux-x86_64-python-main-3.14.0a0-3bd942f |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.13 sec: 1.60x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 653 ms: 1.43x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 495 ms: 1.40x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.31 sec: 1.36x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 829 ms: 1.33x faster                                  |
| async_tree_none            | 740 ms                                                                | 575 ms: 1.29x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 748 ms: 1.27x faster                                  |
| gc_traversal               | 5.61 ms                                                               | 4.51 ms: 1.24x faster                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 980 ms: 1.16x faster                                  |
| create_gc_cycles           | 2.02 ms                                                               | 1.83 ms: 1.10x faster                                 |
| regex_effbot               | 4.97 ms                                                               | 4.56 ms: 1.09x faster                                 |
| pickle_dict                | 46.5 us                                                               | 43.5 us: 1.07x faster                                 |
| pidigits                   | 255 ms                                                                | 242 ms: 1.05x faster                                  |
| asyncio_websockets         | 766 ms                                                                | 738 ms: 1.04x faster                                  |
| unpickle_list              | 7.19 us                                                               | 7.59 us: 1.06x slower                                 |
| xml_etree_iterparse        | 157 ms                                                                | 175 ms: 1.11x slower                                  |
| sqlite_synth               | 3.75 us                                                               | 4.19 us: 1.12x slower                                 |
| dulwich_log                | 114 ms                                                                | 130 ms: 1.14x slower                                  |
| asyncio_tcp                | 958 ms                                                                | 1.09 sec: 1.14x slower                                |
| unpickle                   | 19.7 us                                                               | 22.7 us: 1.15x slower                                 |
| deepcopy                   | 503 us                                                                | 579 us: 1.15x slower                                  |
| async_generators           | 617 ms                                                                | 712 ms: 1.15x slower                                  |
| pathlib                    | 31.7 ms                                                               | 36.6 ms: 1.15x slower                                 |
| regex_v8                   | 31.1 ms                                                               | 36.1 ms: 1.16x slower                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.27 sec: 1.17x slower                                |
| docutils                   | 4.06 sec                                                              | 4.76 sec: 1.17x slower                                |
| json_loads                 | 36.6 us                                                               | 42.8 us: 1.17x slower                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 8.77 ms: 1.17x slower                                 |
| scimark_fft                | 499 ms                                                                | 587 ms: 1.18x slower                                  |
| pylint                     | 501 ms                                                                | 593 ms: 1.18x slower                                  |
| generators                 | 46.0 ms                                                               | 54.8 ms: 1.19x slower                                 |
| json                       | 6.68 ms                                                               | 7.97 ms: 1.19x slower                                 |
| xml_etree_generate         | 128 ms                                                                | 157 ms: 1.22x slower                                  |
| meteor_contest             | 149 ms                                                                | 186 ms: 1.25x slower                                  |
| deepcopy_memo              | 57.5 us                                                               | 73.7 us: 1.28x slower                                 |
| comprehensions             | 29.6 us                                                               | 38.4 us: 1.30x slower                                 |
| python_startup_no_site     | 16.3 ms                                                               | 21.2 ms: 1.30x slower                                 |
| pycparser                  | 1.73 sec                                                              | 2.28 sec: 1.31x slower                                |
| deepcopy_reduce            | 4.45 us                                                               | 5.88 us: 1.32x slower                                 |
| mdp                        | 3.84 sec                                                              | 5.11 sec: 1.33x slower                                |
| tornado_http               | 262 ms                                                                | 352 ms: 1.34x slower                                  |
| bench_thread_pool          | 3.11 ms                                                               | 4.19 ms: 1.35x slower                                 |
| crypto_pyaes               | 112 ms                                                                | 151 ms: 1.35x slower                                  |
| logging_format             | 11.8 us                                                               | 16.0 us: 1.35x slower                                 |
| json_dumps                 | 13.6 ms                                                               | 18.9 ms: 1.39x slower                                 |
| fannkuch                   | 551 ms                                                                | 767 ms: 1.39x slower                                  |
| sympy_integrate            | 31.4 ms                                                               | 43.8 ms: 1.40x slower                                 |
| thrift                     | 1.17 ms                                                               | 1.65 ms: 1.41x slower                                 |
| 2to3                       | 444 ms                                                                | 626 ms: 1.41x slower                                  |
| xml_etree_process          | 85.7 ms                                                               | 121 ms: 1.42x slower                                  |
| telco                      | 9.71 ms                                                               | 14.0 ms: 1.44x slower                                 |
| nqueens                    | 110 ms                                                                | 160 ms: 1.45x slower                                  |
| python_startup             | 21.2 ms                                                               | 30.9 ms: 1.46x slower                                 |
| tomli_loads                | 2.99 sec                                                              | 4.35 sec: 1.46x slower                                |
| html5lib                   | 95.8 ms                                                               | 141 ms: 1.47x slower                                  |
| regex_compile              | 197 ms                                                                | 290 ms: 1.47x slower                                  |
| coroutines                 | 30.1 ms                                                               | 45.1 ms: 1.50x slower                                 |
| coverage                   | 97.6 ms                                                               | 147 ms: 1.51x slower                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 10.0 sec: 1.51x slower                                |
| logging_simple             | 9.89 us                                                               | 15.0 us: 1.52x slower                                 |
| genshi_xml                 | 73.6 ms                                                               | 116 ms: 1.57x slower                                  |
| sympy_str                  | 425 ms                                                                | 672 ms: 1.58x slower                                  |
| float                      | 127 ms                                                                | 201 ms: 1.58x slower                                  |
| scimark_monte_carlo        | 98.5 ms                                                               | 157 ms: 1.59x slower                                  |
| spectral_norm              | 158 ms                                                                | 254 ms: 1.61x slower                                  |
| sqlglot_optimize           | 76.5 ms                                                               | 125 ms: 1.63x slower                                  |
| pyflate                    | 661 ms                                                                | 1.08 sec: 1.63x slower                                |
| sqlglot_normalize          | 148 ms                                                                | 245 ms: 1.65x slower                                  |
| richards                   | 63.4 ms                                                               | 105 ms: 1.65x slower                                  |
| unpickle_pure_python       | 319 us                                                                | 547 us: 1.71x slower                                  |
| django_template            | 48.6 ms                                                               | 83.8 ms: 1.73x slower                                 |
| pprint_pformat             | 2.03 sec                                                              | 3.52 sec: 1.73x slower                                |
| pprint_safe_repr           | 970 ms                                                                | 1.69 sec: 1.74x slower                                |
| chaos                      | 93.7 ms                                                               | 168 ms: 1.79x slower                                  |
| pickle_pure_python         | 447 us                                                                | 804 us: 1.80x slower                                  |
| hexiom                     | 8.87 ms                                                               | 16.0 ms: 1.80x slower                                 |
| mako                       | 17.2 ms                                                               | 31.2 ms: 1.81x slower                                 |
| typing_runtime_protocols   | 199 us                                                                | 364 us: 1.82x slower                                  |
| genshi_text                | 31.9 ms                                                               | 58.2 ms: 1.83x slower                                 |
| sqlglot_parse              | 1.89 ms                                                               | 3.50 ms: 1.85x slower                                 |
| raytrace                   | 418 ms                                                                | 791 ms: 1.89x slower                                  |
| richards_super             | 67.9 ms                                                               | 130 ms: 1.92x slower                                  |
| sympy_expand               | 689 ms                                                                | 1.36 sec: 1.97x slower                                |
| scimark_sor                | 171 ms                                                                | 337 ms: 1.97x slower                                  |
| sqlglot_transpile          | 2.28 ms                                                               | 4.53 ms: 1.98x slower                                 |
| scimark_lu                 | 155 ms                                                                | 309 ms: 1.99x slower                                  |
| go                         | 185 ms                                                                | 369 ms: 2.00x slower                                  |
| logging_silent             | 135 ns                                                                | 272 ns: 2.01x slower                                  |
| sympy_sum                  | 229 ms                                                                | 464 ms: 2.03x slower                                  |
| deltablue                  | 5.05 ms                                                               | 10.9 ms: 2.16x slower                                 |
| nbody                      | 125 ms                                                                | 312 ms: 2.50x slower                                  |
| unpack_sequence            | 68.5 ns                                                               | 187 ns: 2.74x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.34x slower                                          |

Benchmark hidden because not significant (5): bench_mp_pool, regex_dna, pickle_list, pickle, xml_etree_parse
Ignored benchmarks (8) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.21x

# Memory
- memory change: 2.26x