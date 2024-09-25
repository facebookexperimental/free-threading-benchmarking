# Results vs. 3.12.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: e001027
- commit date: 2024-08-15
- overall geometric mean: 1.39x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x slower
- Memory change: 2.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 444 ms                                                                | 698 ms: 1.57x slower                                  |
| docutils       | 4.06 sec                                                              | 5.02 sec: 1.24x slower                                |
| html5lib       | 95.8 ms                                                               | 149 ms: 1.56x slower                                  |
| tornado_http   | 262 ms                                                                | 429 ms: 1.63x slower                                  |
| Geometric mean | (ref)                                                                 | 1.49x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.19 sec: 1.52x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 647 ms: 1.44x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 510 ms: 1.36x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.34 sec: 1.33x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 846 ms: 1.30x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 759 ms: 1.25x faster                                  |
| async_tree_none            | 740 ms                                                                | 614 ms: 1.20x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 974 ms: 1.17x faster                                  |
| asyncio_tcp                | 958 ms                                                                | 1.12 sec: 1.17x slower                                |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.41 sec: 1.22x slower                                |
| async_generators           | 617 ms                                                                | 763 ms: 1.24x slower                                  |
| coroutines                 | 30.1 ms                                                               | 43.6 ms: 1.45x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.10x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 255 ms                                                                | 275 ms: 1.08x slower                                  |
| float          | 127 ms                                                                | 191 ms: 1.50x slower                                  |
| nbody          | 125 ms                                                                | 317 ms: 2.54x slower                                  |
| Geometric mean | (ref)                                                                 | 1.60x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 287 ms                                                                | 297 ms: 1.04x slower                                  |
| regex_v8       | 31.1 ms                                                               | 36.7 ms: 1.18x slower                                 |
| regex_compile  | 197 ms                                                                | 303 ms: 1.54x slower                                  |
| Geometric mean | (ref)                                                                 | 1.16x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 6.40 us                                                               | 6.74 us: 1.05x slower                                 |
| pickle               | 14.8 us                                                               | 15.8 us: 1.07x slower                                 |
| unpickle_list        | 7.19 us                                                               | 7.97 us: 1.11x slower                                 |
| xml_etree_iterparse  | 157 ms                                                                | 177 ms: 1.12x slower                                  |
| unpickle             | 19.7 us                                                               | 23.1 us: 1.17x slower                                 |
| json_dumps           | 13.6 ms                                                               | 17.9 ms: 1.32x slower                                 |
| json_loads           | 36.6 us                                                               | 48.4 us: 1.32x slower                                 |
| xml_etree_generate   | 128 ms                                                                | 180 ms: 1.40x slower                                  |
| tomli_loads          | 2.99 sec                                                              | 4.36 sec: 1.46x slower                                |
| xml_etree_process    | 85.7 ms                                                               | 133 ms: 1.55x slower                                  |
| unpickle_pure_python | 319 us                                                                | 574 us: 1.80x slower                                  |
| pickle_pure_python   | 447 us                                                                | 910 us: 2.03x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.29x slower                                          |

Benchmark hidden because not significant (2): pickle_dict, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 22.7 ms: 1.40x slower                                 |
| python_startup         | 21.2 ms                                                               | 31.2 ms: 1.47x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.43x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 118 ms: 1.60x slower                                  |
| django_template | 48.6 ms                                                               | 80.8 ms: 1.66x slower                                 |
| mako            | 17.2 ms                                                               | 30.6 ms: 1.77x slower                                 |
| genshi_text     | 31.9 ms                                                               | 59.2 ms: 1.86x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.72x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.19 sec: 1.52x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 647 ms: 1.44x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 510 ms: 1.36x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.34 sec: 1.33x faster                                |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 846 ms: 1.30x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 759 ms: 1.25x faster                                  |
| async_tree_none            | 740 ms                                                                | 614 ms: 1.20x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 974 ms: 1.17x faster                                  |
| gc_traversal               | 5.61 ms                                                               | 5.18 ms: 1.08x faster                                 |
| regex_dna                  | 287 ms                                                                | 297 ms: 1.04x slower                                  |
| pickle_list                | 6.40 us                                                               | 6.74 us: 1.05x slower                                 |
| pickle                     | 14.8 us                                                               | 15.8 us: 1.07x slower                                 |
| pidigits                   | 255 ms                                                                | 275 ms: 1.08x slower                                  |
| unpickle_list              | 7.19 us                                                               | 7.97 us: 1.11x slower                                 |
| xml_etree_iterparse        | 157 ms                                                                | 177 ms: 1.12x slower                                  |
| generators                 | 46.0 ms                                                               | 53.0 ms: 1.15x slower                                 |
| sqlite_synth               | 3.75 us                                                               | 4.35 us: 1.16x slower                                 |
| pylint                     | 501 ms                                                                | 586 ms: 1.17x slower                                  |
| asyncio_tcp                | 958 ms                                                                | 1.12 sec: 1.17x slower                                |
| unpickle                   | 19.7 us                                                               | 23.1 us: 1.17x slower                                 |
| regex_v8                   | 31.1 ms                                                               | 36.7 ms: 1.18x slower                                 |
| pathlib                    | 31.7 ms                                                               | 37.5 ms: 1.18x slower                                 |
| deepcopy                   | 503 us                                                                | 596 us: 1.18x slower                                  |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 9.11 ms: 1.22x slower                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.41 sec: 1.22x slower                                |
| deepcopy_memo              | 57.5 us                                                               | 70.9 us: 1.23x slower                                 |
| docutils                   | 4.06 sec                                                              | 5.02 sec: 1.24x slower                                |
| async_generators           | 617 ms                                                                | 763 ms: 1.24x slower                                  |
| deepcopy_reduce            | 4.45 us                                                               | 5.58 us: 1.25x slower                                 |
| pycparser                  | 1.73 sec                                                              | 2.21 sec: 1.28x slower                                |
| scimark_fft                | 499 ms                                                                | 642 ms: 1.29x slower                                  |
| json                       | 6.68 ms                                                               | 8.77 ms: 1.31x slower                                 |
| json_dumps                 | 13.6 ms                                                               | 17.9 ms: 1.32x slower                                 |
| json_loads                 | 36.6 us                                                               | 48.4 us: 1.32x slower                                 |
| comprehensions             | 29.6 us                                                               | 39.5 us: 1.33x slower                                 |
| crypto_pyaes               | 112 ms                                                                | 150 ms: 1.34x slower                                  |
| meteor_contest             | 149 ms                                                                | 203 ms: 1.36x slower                                  |
| mdp                        | 3.84 sec                                                              | 5.29 sec: 1.38x slower                                |
| python_startup_no_site     | 16.3 ms                                                               | 22.7 ms: 1.40x slower                                 |
| xml_etree_generate         | 128 ms                                                                | 180 ms: 1.40x slower                                  |
| fannkuch                   | 551 ms                                                                | 786 ms: 1.43x slower                                  |
| coroutines                 | 30.1 ms                                                               | 43.6 ms: 1.45x slower                                 |
| thrift                     | 1.17 ms                                                               | 1.70 ms: 1.45x slower                                 |
| telco                      | 9.71 ms                                                               | 14.1 ms: 1.46x slower                                 |
| tomli_loads                | 2.99 sec                                                              | 4.36 sec: 1.46x slower                                |
| python_startup             | 21.2 ms                                                               | 31.2 ms: 1.47x slower                                 |
| float                      | 127 ms                                                                | 191 ms: 1.50x slower                                  |
| bench_thread_pool          | 3.11 ms                                                               | 4.67 ms: 1.50x slower                                 |
| logging_simple             | 9.89 us                                                               | 14.9 us: 1.51x slower                                 |
| logging_format             | 11.8 us                                                               | 17.9 us: 1.51x slower                                 |
| regex_compile              | 197 ms                                                                | 303 ms: 1.54x slower                                  |
| sympy_integrate            | 31.4 ms                                                               | 48.4 ms: 1.54x slower                                 |
| xml_etree_process          | 85.7 ms                                                               | 133 ms: 1.55x slower                                  |
| spectral_norm              | 158 ms                                                                | 245 ms: 1.55x slower                                  |
| html5lib                   | 95.8 ms                                                               | 149 ms: 1.56x slower                                  |
| coverage                   | 97.6 ms                                                               | 152 ms: 1.56x slower                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 10.3 sec: 1.56x slower                                |
| 2to3                       | 444 ms                                                                | 698 ms: 1.57x slower                                  |
| nqueens                    | 110 ms                                                                | 175 ms: 1.59x slower                                  |
| genshi_xml                 | 73.6 ms                                                               | 118 ms: 1.60x slower                                  |
| sqlglot_normalize          | 148 ms                                                                | 240 ms: 1.62x slower                                  |
| tornado_http               | 262 ms                                                                | 429 ms: 1.63x slower                                  |
| django_template            | 48.6 ms                                                               | 80.8 ms: 1.66x slower                                 |
| sqlglot_optimize           | 76.5 ms                                                               | 128 ms: 1.67x slower                                  |
| richards                   | 63.4 ms                                                               | 107 ms: 1.69x slower                                  |
| pyflate                    | 661 ms                                                                | 1.13 sec: 1.72x slower                                |
| sympy_str                  | 425 ms                                                                | 730 ms: 1.72x slower                                  |
| scimark_monte_carlo        | 98.5 ms                                                               | 170 ms: 1.73x slower                                  |
| pprint_pformat             | 2.03 sec                                                              | 3.57 sec: 1.76x slower                                |
| mako                       | 17.2 ms                                                               | 30.6 ms: 1.77x slower                                 |
| typing_runtime_protocols   | 199 us                                                                | 355 us: 1.78x slower                                  |
| unpickle_pure_python       | 319 us                                                                | 574 us: 1.80x slower                                  |
| pprint_safe_repr           | 970 ms                                                                | 1.77 sec: 1.83x slower                                |
| hexiom                     | 8.87 ms                                                               | 16.3 ms: 1.84x slower                                 |
| genshi_text                | 31.9 ms                                                               | 59.2 ms: 1.86x slower                                 |
| chaos                      | 93.7 ms                                                               | 175 ms: 1.87x slower                                  |
| sympy_expand               | 689 ms                                                                | 1.31 sec: 1.90x slower                                |
| raytrace                   | 418 ms                                                                | 816 ms: 1.95x slower                                  |
| logging_silent             | 135 ns                                                                | 267 ns: 1.97x slower                                  |
| sqlglot_transpile          | 2.28 ms                                                               | 4.53 ms: 1.98x slower                                 |
| sqlglot_parse              | 1.89 ms                                                               | 3.81 ms: 2.01x slower                                 |
| richards_super             | 67.9 ms                                                               | 137 ms: 2.01x slower                                  |
| pickle_pure_python         | 447 us                                                                | 910 us: 2.03x slower                                  |
| scimark_sor                | 171 ms                                                                | 354 ms: 2.07x slower                                  |
| scimark_lu                 | 155 ms                                                                | 330 ms: 2.14x slower                                  |
| sympy_sum                  | 229 ms                                                                | 509 ms: 2.22x slower                                  |
| deltablue                  | 5.05 ms                                                               | 11.3 ms: 2.24x slower                                 |
| go                         | 185 ms                                                                | 452 ms: 2.44x slower                                  |
| nbody                      | 125 ms                                                                | 317 ms: 2.54x slower                                  |
| unpack_sequence            | 68.5 ns                                                               | 191 ns: 2.79x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.39x slower                                          |

Benchmark hidden because not significant (6): bench_mp_pool, regex_effbot, create_gc_cycles, pickle_dict, xml_etree_parse, asyncio_websockets
Ignored benchmarks (9) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.36x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.26x

# Memory
- memory change: 2.24x