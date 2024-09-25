# Results vs. 3.12.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5a4fb7e
- commit date: 2024-09-06
- overall geometric mean: 1.40x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.32x slower
- Memory change: 2.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 444 ms                                                                | 682 ms: 1.54x slower                                  |
| docutils       | 4.06 sec                                                              | 5.10 sec: 1.25x slower                                |
| html5lib       | 95.8 ms                                                               | 147 ms: 1.54x slower                                  |
| tornado_http   | 262 ms                                                                | 420 ms: 1.60x slower                                  |
| Geometric mean | (ref)                                                                 | 1.48x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.24 sec: 1.46x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 674 ms: 1.39x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.32 sec: 1.35x faster                                |
| async_tree_none_tg         | 692 ms                                                                | 540 ms: 1.28x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 885 ms: 1.24x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 770 ms: 1.23x faster                                  |
| async_tree_none            | 740 ms                                                                | 607 ms: 1.22x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 937 ms: 1.21x faster                                  |
| asyncio_websockets         | 766 ms                                                                | 818 ms: 1.07x slower                                  |
| async_generators           | 617 ms                                                                | 723 ms: 1.17x slower                                  |
| asyncio_tcp                | 958 ms                                                                | 1.22 sec: 1.27x slower                                |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.67 sec: 1.31x slower                                |
| coroutines                 | 30.1 ms                                                               | 42.2 ms: 1.40x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.08x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 127 ms                                                                | 203 ms: 1.60x slower                                  |
| nbody          | 125 ms                                                                | 315 ms: 2.53x slower                                  |
| Geometric mean | (ref)                                                                 | 1.60x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 287 ms                                                                | 299 ms: 1.04x slower                                  |
| regex_v8       | 31.1 ms                                                               | 37.6 ms: 1.21x slower                                 |
| regex_compile  | 197 ms                                                                | 305 ms: 1.55x slower                                  |
| Geometric mean | (ref)                                                                 | 1.20x slower                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle               | 14.8 us                                                               | 13.8 us: 1.07x faster                                 |
| xml_etree_iterparse  | 157 ms                                                                | 168 ms: 1.07x slower                                  |
| unpickle             | 19.7 us                                                               | 23.1 us: 1.17x slower                                 |
| json_loads           | 36.6 us                                                               | 47.7 us: 1.31x slower                                 |
| json_dumps           | 13.6 ms                                                               | 18.0 ms: 1.33x slower                                 |
| xml_etree_generate   | 128 ms                                                                | 179 ms: 1.40x slower                                  |
| tomli_loads          | 2.99 sec                                                              | 4.37 sec: 1.47x slower                                |
| xml_etree_process    | 85.7 ms                                                               | 136 ms: 1.58x slower                                  |
| pickle_pure_python   | 447 us                                                                | 762 us: 1.70x slower                                  |
| unpickle_pure_python | 319 us                                                                | 563 us: 1.76x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.24x slower                                          |

Benchmark hidden because not significant (4): pickle_dict, xml_etree_parse, pickle_list, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 24.3 ms: 1.50x slower                                 |
| python_startup         | 21.2 ms                                                               | 37.1 ms: 1.75x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.62x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| django_template | 48.6 ms                                                               | 83.6 ms: 1.72x slower                                 |
| genshi_text     | 31.9 ms                                                               | 57.6 ms: 1.81x slower                                 |
| mako            | 17.2 ms                                                               | 31.9 ms: 1.85x slower                                 |
| genshi_xml      | 73.6 ms                                                               | 141 ms: 1.91x slower                                  |
| Geometric mean  | (ref)                                                                 | 1.82x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-main-3.14.0a0-5a4fb7e |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.24 sec: 1.46x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 674 ms: 1.39x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.32 sec: 1.35x faster                                |
| async_tree_none_tg         | 692 ms                                                                | 540 ms: 1.28x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 885 ms: 1.24x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 770 ms: 1.23x faster                                  |
| async_tree_none            | 740 ms                                                                | 607 ms: 1.22x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 937 ms: 1.21x faster                                  |
| gc_traversal               | 5.61 ms                                                               | 4.74 ms: 1.18x faster                                 |
| pickle                     | 14.8 us                                                               | 13.8 us: 1.07x faster                                 |
| regex_dna                  | 287 ms                                                                | 299 ms: 1.04x slower                                  |
| xml_etree_iterparse        | 157 ms                                                                | 168 ms: 1.07x slower                                  |
| asyncio_websockets         | 766 ms                                                                | 818 ms: 1.07x slower                                  |
| sqlite_synth               | 3.75 us                                                               | 4.25 us: 1.13x slower                                 |
| pathlib                    | 31.7 ms                                                               | 36.2 ms: 1.14x slower                                 |
| unpickle                   | 19.7 us                                                               | 23.1 us: 1.17x slower                                 |
| async_generators           | 617 ms                                                                | 723 ms: 1.17x slower                                  |
| regex_v8                   | 31.1 ms                                                               | 37.6 ms: 1.21x slower                                 |
| deepcopy                   | 503 us                                                                | 617 us: 1.23x slower                                  |
| generators                 | 46.0 ms                                                               | 56.6 ms: 1.23x slower                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 9.21 ms: 1.23x slower                                 |
| deepcopy_memo              | 57.5 us                                                               | 71.0 us: 1.24x slower                                 |
| docutils                   | 4.06 sec                                                              | 5.10 sec: 1.25x slower                                |
| dulwich_log                | 114 ms                                                                | 143 ms: 1.26x slower                                  |
| asyncio_tcp                | 958 ms                                                                | 1.22 sec: 1.27x slower                                |
| pylint                     | 501 ms                                                                | 641 ms: 1.28x slower                                  |
| deepcopy_reduce            | 4.45 us                                                               | 5.81 us: 1.30x slower                                 |
| json_loads                 | 36.6 us                                                               | 47.7 us: 1.31x slower                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.67 sec: 1.31x slower                                |
| meteor_contest             | 149 ms                                                                | 196 ms: 1.32x slower                                  |
| mdp                        | 3.84 sec                                                              | 5.07 sec: 1.32x slower                                |
| scimark_fft                | 499 ms                                                                | 659 ms: 1.32x slower                                  |
| pycparser                  | 1.73 sec                                                              | 2.29 sec: 1.32x slower                                |
| json_dumps                 | 13.6 ms                                                               | 18.0 ms: 1.33x slower                                 |
| json                       | 6.68 ms                                                               | 9.01 ms: 1.35x slower                                 |
| xml_etree_generate         | 128 ms                                                                | 179 ms: 1.40x slower                                  |
| comprehensions             | 29.6 us                                                               | 41.3 us: 1.40x slower                                 |
| coroutines                 | 30.1 ms                                                               | 42.2 ms: 1.40x slower                                 |
| crypto_pyaes               | 112 ms                                                                | 158 ms: 1.41x slower                                  |
| thrift                     | 1.17 ms                                                               | 1.68 ms: 1.43x slower                                 |
| tomli_loads                | 2.99 sec                                                              | 4.37 sec: 1.47x slower                                |
| fannkuch                   | 551 ms                                                                | 807 ms: 1.47x slower                                  |
| logging_format             | 11.8 us                                                               | 17.5 us: 1.48x slower                                 |
| coverage                   | 97.6 ms                                                               | 144 ms: 1.48x slower                                  |
| python_startup_no_site     | 16.3 ms                                                               | 24.3 ms: 1.50x slower                                 |
| telco                      | 9.71 ms                                                               | 14.9 ms: 1.53x slower                                 |
| 2to3                       | 444 ms                                                                | 682 ms: 1.54x slower                                  |
| html5lib                   | 95.8 ms                                                               | 147 ms: 1.54x slower                                  |
| nqueens                    | 110 ms                                                                | 170 ms: 1.55x slower                                  |
| regex_compile              | 197 ms                                                                | 305 ms: 1.55x slower                                  |
| sympy_integrate            | 31.4 ms                                                               | 49.3 ms: 1.57x slower                                 |
| xml_etree_process          | 85.7 ms                                                               | 136 ms: 1.58x slower                                  |
| float                      | 127 ms                                                                | 203 ms: 1.60x slower                                  |
| tornado_http               | 262 ms                                                                | 420 ms: 1.60x slower                                  |
| spectral_norm              | 158 ms                                                                | 253 ms: 1.61x slower                                  |
| logging_simple             | 9.89 us                                                               | 16.0 us: 1.62x slower                                 |
| bpe_tokeniser              | 6.63 sec                                                              | 10.8 sec: 1.62x slower                                |
| sqlglot_optimize           | 76.5 ms                                                               | 125 ms: 1.63x slower                                  |
| sympy_str                  | 425 ms                                                                | 708 ms: 1.67x slower                                  |
| sqlglot_normalize          | 148 ms                                                                | 248 ms: 1.67x slower                                  |
| pyflate                    | 661 ms                                                                | 1.11 sec: 1.68x slower                                |
| richards                   | 63.4 ms                                                               | 107 ms: 1.68x slower                                  |
| pickle_pure_python         | 447 us                                                                | 762 us: 1.70x slower                                  |
| pprint_safe_repr           | 970 ms                                                                | 1.66 sec: 1.71x slower                                |
| bench_thread_pool          | 3.11 ms                                                               | 5.33 ms: 1.72x slower                                 |
| django_template            | 48.6 ms                                                               | 83.6 ms: 1.72x slower                                 |
| scimark_monte_carlo        | 98.5 ms                                                               | 171 ms: 1.73x slower                                  |
| chaos                      | 93.7 ms                                                               | 163 ms: 1.73x slower                                  |
| python_startup             | 21.2 ms                                                               | 37.1 ms: 1.75x slower                                 |
| pprint_pformat             | 2.03 sec                                                              | 3.55 sec: 1.75x slower                                |
| unpickle_pure_python       | 319 us                                                                | 563 us: 1.76x slower                                  |
| typing_runtime_protocols   | 199 us                                                                | 357 us: 1.79x slower                                  |
| genshi_text                | 31.9 ms                                                               | 57.6 ms: 1.81x slower                                 |
| richards_super             | 67.9 ms                                                               | 126 ms: 1.85x slower                                  |
| mako                       | 17.2 ms                                                               | 31.9 ms: 1.85x slower                                 |
| raytrace                   | 418 ms                                                                | 798 ms: 1.91x slower                                  |
| genshi_xml                 | 73.6 ms                                                               | 141 ms: 1.91x slower                                  |
| sympy_expand               | 689 ms                                                                | 1.32 sec: 1.91x slower                                |
| hexiom                     | 8.87 ms                                                               | 17.1 ms: 1.93x slower                                 |
| logging_silent             | 135 ns                                                                | 266 ns: 1.97x slower                                  |
| sqlglot_parse              | 1.89 ms                                                               | 3.76 ms: 1.98x slower                                 |
| go                         | 185 ms                                                                | 370 ms: 2.00x slower                                  |
| sympy_sum                  | 229 ms                                                                | 472 ms: 2.06x slower                                  |
| sqlglot_transpile          | 2.28 ms                                                               | 4.73 ms: 2.07x slower                                 |
| scimark_sor                | 171 ms                                                                | 360 ms: 2.11x slower                                  |
| scimark_lu                 | 155 ms                                                                | 328 ms: 2.12x slower                                  |
| deltablue                  | 5.05 ms                                                               | 12.2 ms: 2.41x slower                                 |
| nbody                      | 125 ms                                                                | 315 ms: 2.53x slower                                  |
| unpack_sequence            | 68.5 ns                                                               | 207 ns: 3.02x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.40x slower                                          |

Benchmark hidden because not significant (8): create_gc_cycles, pickle_dict, xml_etree_parse, pidigits, pickle_list, unpickle_list, regex_effbot, bench_mp_pool
Ignored benchmarks (8) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.33x
- 99% likely to have a slowdown of 1.32x

# Memory
- memory change: 2.26x