# Results vs. 3.12.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a9bb3c7
- commit date: 2024-07-23
- overall geometric mean: 1.30x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x slower
- Memory change: 2.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 444 ms                                                                | 661 ms: 1.49x slower                                  |
| docutils       | 4.06 sec                                                              | 4.69 sec: 1.15x slower                                |
| html5lib       | 95.8 ms                                                               | 135 ms: 1.41x slower                                  |
| tornado_http   | 262 ms                                                                | 320 ms: 1.22x slower                                  |
| Geometric mean | (ref)                                                                 | 1.31x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.15 sec: 1.57x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 632 ms: 1.48x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 479 ms: 1.45x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.25 sec: 1.43x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 806 ms: 1.36x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 728 ms: 1.30x faster                                  |
| async_tree_none            | 740 ms                                                                | 578 ms: 1.28x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 926 ms: 1.23x faster                                  |
| asyncio_websockets         | 766 ms                                                                | 714 ms: 1.07x faster                                  |
| asyncio_tcp                | 958 ms                                                                | 1.05 sec: 1.09x slower                                |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.12 sec: 1.11x slower                                |
| async_generators           | 617 ms                                                                | 739 ms: 1.20x slower                                  |
| coroutines                 | 30.1 ms                                                               | 40.7 ms: 1.35x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.17x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 255 ms                                                                | 241 ms: 1.06x faster                                  |
| float          | 127 ms                                                                | 199 ms: 1.57x slower                                  |
| nbody          | 125 ms                                                                | 284 ms: 2.28x slower                                  |
| Geometric mean | (ref)                                                                 | 1.50x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.97 ms                                                               | 4.60 ms: 1.08x faster                                 |
| regex_v8       | 31.1 ms                                                               | 35.5 ms: 1.14x slower                                 |
| regex_compile  | 197 ms                                                                | 287 ms: 1.46x slower                                  |
| Geometric mean | (ref)                                                                 | 1.11x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 46.5 us                                                               | 40.4 us: 1.15x faster                                 |
| xml_etree_parse      | 230 ms                                                                | 203 ms: 1.13x faster                                  |
| xml_etree_iterparse  | 157 ms                                                                | 152 ms: 1.04x faster                                  |
| unpickle             | 19.7 us                                                               | 21.3 us: 1.08x slower                                 |
| json_loads           | 36.6 us                                                               | 41.9 us: 1.15x slower                                 |
| xml_etree_generate   | 128 ms                                                                | 160 ms: 1.24x slower                                  |
| json_dumps           | 13.6 ms                                                               | 18.2 ms: 1.34x slower                                 |
| xml_etree_process    | 85.7 ms                                                               | 119 ms: 1.39x slower                                  |
| tomli_loads          | 2.99 sec                                                              | 4.17 sec: 1.40x slower                                |
| unpickle_pure_python | 319 us                                                                | 526 us: 1.65x slower                                  |
| pickle_pure_python   | 447 us                                                                | 792 us: 1.77x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.17x slower                                          |

Benchmark hidden because not significant (3): pickle, unpickle_list, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 18.6 ms: 1.14x slower                                 |
| python_startup         | 21.2 ms                                                               | 27.3 ms: 1.28x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.21x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 117 ms: 1.58x slower                                  |
| django_template | 48.6 ms                                                               | 80.7 ms: 1.66x slower                                 |
| genshi_text     | 31.9 ms                                                               | 54.8 ms: 1.72x slower                                 |
| mako            | 17.2 ms                                                               | 29.7 ms: 1.72x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.67x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.15 sec: 1.57x faster                                |
| bench_mp_pool              | 18.4 ms                                                               | 12.0 ms: 1.53x faster                                 |
| async_tree_memoization_tg  | 935 ms                                                                | 632 ms: 1.48x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 479 ms: 1.45x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.25 sec: 1.43x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 806 ms: 1.36x faster                                  |
| gc_traversal               | 5.61 ms                                                               | 4.22 ms: 1.33x faster                                 |
| async_tree_memoization     | 949 ms                                                                | 728 ms: 1.30x faster                                  |
| async_tree_none            | 740 ms                                                                | 578 ms: 1.28x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 926 ms: 1.23x faster                                  |
| pickle_dict                | 46.5 us                                                               | 40.4 us: 1.15x faster                                 |
| create_gc_cycles           | 2.02 ms                                                               | 1.77 ms: 1.14x faster                                 |
| xml_etree_parse            | 230 ms                                                                | 203 ms: 1.13x faster                                  |
| regex_effbot               | 4.97 ms                                                               | 4.60 ms: 1.08x faster                                 |
| asyncio_websockets         | 766 ms                                                                | 714 ms: 1.07x faster                                  |
| pidigits                   | 255 ms                                                                | 241 ms: 1.06x faster                                  |
| xml_etree_iterparse        | 157 ms                                                                | 152 ms: 1.04x faster                                  |
| unpickle                   | 19.7 us                                                               | 21.3 us: 1.08x slower                                 |
| asyncio_tcp                | 958 ms                                                                | 1.05 sec: 1.09x slower                                |
| pylint                     | 501 ms                                                                | 554 ms: 1.11x slower                                  |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.12 sec: 1.11x slower                                |
| regex_v8                   | 31.1 ms                                                               | 35.5 ms: 1.14x slower                                 |
| python_startup_no_site     | 16.3 ms                                                               | 18.6 ms: 1.14x slower                                 |
| generators                 | 46.0 ms                                                               | 52.7 ms: 1.15x slower                                 |
| json_loads                 | 36.6 us                                                               | 41.9 us: 1.15x slower                                 |
| sqlite_synth               | 3.75 us                                                               | 4.31 us: 1.15x slower                                 |
| docutils                   | 4.06 sec                                                              | 4.69 sec: 1.15x slower                                |
| dulwich_log                | 114 ms                                                                | 135 ms: 1.19x slower                                  |
| async_generators           | 617 ms                                                                | 739 ms: 1.20x slower                                  |
| bench_thread_pool          | 3.11 ms                                                               | 3.73 ms: 1.20x slower                                 |
| json                       | 6.68 ms                                                               | 8.04 ms: 1.20x slower                                 |
| deepcopy_memo              | 57.5 us                                                               | 69.3 us: 1.21x slower                                 |
| deepcopy                   | 503 us                                                                | 608 us: 1.21x slower                                  |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 9.03 ms: 1.21x slower                                 |
| tornado_http               | 262 ms                                                                | 320 ms: 1.22x slower                                  |
| scimark_fft                | 499 ms                                                                | 616 ms: 1.23x slower                                  |
| pycparser                  | 1.73 sec                                                              | 2.15 sec: 1.24x slower                                |
| xml_etree_generate         | 128 ms                                                                | 160 ms: 1.24x slower                                  |
| python_startup             | 21.2 ms                                                               | 27.3 ms: 1.28x slower                                 |
| meteor_contest             | 149 ms                                                                | 196 ms: 1.31x slower                                  |
| mdp                        | 3.84 sec                                                              | 5.07 sec: 1.32x slower                                |
| json_dumps                 | 13.6 ms                                                               | 18.2 ms: 1.34x slower                                 |
| crypto_pyaes               | 112 ms                                                                | 150 ms: 1.34x slower                                  |
| coroutines                 | 30.1 ms                                                               | 40.7 ms: 1.35x slower                                 |
| deepcopy_reduce            | 4.45 us                                                               | 6.01 us: 1.35x slower                                 |
| telco                      | 9.71 ms                                                               | 13.2 ms: 1.36x slower                                 |
| sympy_integrate            | 31.4 ms                                                               | 43.4 ms: 1.38x slower                                 |
| xml_etree_process          | 85.7 ms                                                               | 119 ms: 1.39x slower                                  |
| nqueens                    | 110 ms                                                                | 153 ms: 1.39x slower                                  |
| tomli_loads                | 2.99 sec                                                              | 4.17 sec: 1.40x slower                                |
| html5lib                   | 95.8 ms                                                               | 135 ms: 1.41x slower                                  |
| comprehensions             | 29.6 us                                                               | 42.1 us: 1.42x slower                                 |
| logging_format             | 11.8 us                                                               | 16.8 us: 1.42x slower                                 |
| fannkuch                   | 551 ms                                                                | 794 ms: 1.44x slower                                  |
| regex_compile              | 197 ms                                                                | 287 ms: 1.46x slower                                  |
| thrift                     | 1.17 ms                                                               | 1.71 ms: 1.46x slower                                 |
| bpe_tokeniser              | 6.63 sec                                                              | 9.73 sec: 1.47x slower                                |
| 2to3                       | 444 ms                                                                | 661 ms: 1.49x slower                                  |
| coverage                   | 97.6 ms                                                               | 149 ms: 1.53x slower                                  |
| spectral_norm              | 158 ms                                                                | 245 ms: 1.55x slower                                  |
| richards                   | 63.4 ms                                                               | 99.0 ms: 1.56x slower                                 |
| sympy_str                  | 425 ms                                                                | 664 ms: 1.56x slower                                  |
| logging_simple             | 9.89 us                                                               | 15.5 us: 1.57x slower                                 |
| float                      | 127 ms                                                                | 199 ms: 1.57x slower                                  |
| sqlglot_optimize           | 76.5 ms                                                               | 121 ms: 1.58x slower                                  |
| sqlglot_normalize          | 148 ms                                                                | 235 ms: 1.58x slower                                  |
| genshi_xml                 | 73.6 ms                                                               | 117 ms: 1.58x slower                                  |
| pyflate                    | 661 ms                                                                | 1.08 sec: 1.63x slower                                |
| unpickle_pure_python       | 319 us                                                                | 526 us: 1.65x slower                                  |
| django_template            | 48.6 ms                                                               | 80.7 ms: 1.66x slower                                 |
| scimark_monte_carlo        | 98.5 ms                                                               | 165 ms: 1.67x slower                                  |
| typing_runtime_protocols   | 199 us                                                                | 337 us: 1.69x slower                                  |
| genshi_text                | 31.9 ms                                                               | 54.8 ms: 1.72x slower                                 |
| mako                       | 17.2 ms                                                               | 29.7 ms: 1.72x slower                                 |
| pprint_pformat             | 2.03 sec                                                              | 3.50 sec: 1.72x slower                                |
| pprint_safe_repr           | 970 ms                                                                | 1.71 sec: 1.76x slower                                |
| chaos                      | 93.7 ms                                                               | 165 ms: 1.76x slower                                  |
| pickle_pure_python         | 447 us                                                                | 792 us: 1.77x slower                                  |
| logging_silent             | 135 ns                                                                | 240 ns: 1.77x slower                                  |
| richards_super             | 67.9 ms                                                               | 122 ms: 1.80x slower                                  |
| sympy_expand               | 689 ms                                                                | 1.27 sec: 1.84x slower                                |
| hexiom                     | 8.87 ms                                                               | 16.5 ms: 1.85x slower                                 |
| raytrace                   | 418 ms                                                                | 784 ms: 1.88x slower                                  |
| sqlglot_transpile          | 2.28 ms                                                               | 4.33 ms: 1.90x slower                                 |
| scimark_sor                | 171 ms                                                                | 337 ms: 1.97x slower                                  |
| sqlglot_parse              | 1.89 ms                                                               | 3.77 ms: 1.99x slower                                 |
| sympy_sum                  | 229 ms                                                                | 460 ms: 2.01x slower                                  |
| scimark_lu                 | 155 ms                                                                | 326 ms: 2.11x slower                                  |
| go                         | 185 ms                                                                | 395 ms: 2.14x slower                                  |
| deltablue                  | 5.05 ms                                                               | 10.8 ms: 2.14x slower                                 |
| nbody                      | 125 ms                                                                | 284 ms: 2.28x slower                                  |
| unpack_sequence            | 68.5 ns                                                               | 191 ns: 2.78x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.30x slower                                          |

Benchmark hidden because not significant (5): pickle, regex_dna, pathlib, unpickle_list, pickle_list
Ignored benchmarks (8) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.25x
- 95% likely to have a slowdown of 1.24x
- 99% likely to have a slowdown of 1.21x

# Memory
- memory change: 2.27x