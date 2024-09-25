# Results vs. 3.12.0b1

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.35x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 2.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 444 ms                                                                | 648 ms: 1.46x slower                                         |
| chameleon      | 9.30 ms                                                               | 18.1 ms: 1.95x slower                                        |
| docutils       | 4.06 sec                                                              | 4.93 sec: 1.21x slower                                       |
| html5lib       | 95.8 ms                                                               | 147 ms: 1.53x slower                                         |
| tornado_http   | 262 ms                                                                | 356 ms: 1.36x slower                                         |
| Geometric mean | (ref)                                                                 | 1.48x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.17 sec: 1.55x faster                                       |
| async_tree_io              | 1.79 sec                                                              | 1.29 sec: 1.38x faster                                       |
| async_tree_memoization_tg  | 935 ms                                                                | 729 ms: 1.28x faster                                         |
| async_tree_memoization     | 949 ms                                                                | 766 ms: 1.24x faster                                         |
| async_tree_none_tg         | 692 ms                                                                | 583 ms: 1.19x faster                                         |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 938 ms: 1.17x faster                                         |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 988 ms: 1.15x faster                                         |
| async_tree_none            | 740 ms                                                                | 654 ms: 1.13x faster                                         |
| async_generators           | 617 ms                                                                | 718 ms: 1.16x slower                                         |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.29 sec: 1.18x slower                                       |
| asyncio_tcp                | 958 ms                                                                | 1.17 sec: 1.22x slower                                       |
| coroutines                 | 30.1 ms                                                               | 42.2 ms: 1.40x slower                                        |
| Geometric mean             | (ref)                                                                 | 1.08x faster                                                 |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 127 ms                                                                | 193 ms: 1.52x slower                                         |
| nbody          | 125 ms                                                                | 267 ms: 2.14x slower                                         |
| Geometric mean | (ref)                                                                 | 1.47x slower                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 4.97 ms                                                               | 5.22 ms: 1.05x slower                                        |
| regex_dna      | 287 ms                                                                | 312 ms: 1.09x slower                                         |
| regex_v8       | 31.1 ms                                                               | 35.5 ms: 1.14x slower                                        |
| regex_compile  | 197 ms                                                                | 271 ms: 1.38x slower                                         |
| Geometric mean | (ref)                                                                 | 1.16x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_parse      | 230 ms                                                                | 200 ms: 1.15x faster                                         |
| pickle_dict          | 46.5 us                                                               | 43.3 us: 1.08x faster                                        |
| unpickle             | 19.7 us                                                               | 21.4 us: 1.09x slower                                        |
| pickle_list          | 6.40 us                                                               | 6.97 us: 1.09x slower                                        |
| json_loads           | 36.6 us                                                               | 42.7 us: 1.17x slower                                        |
| xml_etree_generate   | 128 ms                                                                | 153 ms: 1.19x slower                                         |
| json_dumps           | 13.6 ms                                                               | 18.0 ms: 1.32x slower                                        |
| tomli_loads          | 2.99 sec                                                              | 4.19 sec: 1.40x slower                                       |
| xml_etree_process    | 85.7 ms                                                               | 126 ms: 1.47x slower                                         |
| unpickle_pure_python | 319 us                                                                | 515 us: 1.61x slower                                         |
| pickle_pure_python   | 447 us                                                                | 872 us: 1.95x slower                                         |
| Geometric mean       | (ref)                                                                 | 1.19x slower                                                 |

Benchmark hidden because not significant (3): unpickle_list, pickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 21.9 ms: 1.35x slower                                        |
| python_startup         | 21.2 ms                                                               | 33.8 ms: 1.59x slower                                        |
| Geometric mean         | (ref)                                                                 | 1.46x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| django_template | 48.6 ms                                                               | 76.1 ms: 1.57x slower                                        |
| genshi_xml      | 73.6 ms                                                               | 118 ms: 1.61x slower                                         |
| genshi_text     | 31.9 ms                                                               | 54.3 ms: 1.70x slower                                        |
| mako            | 17.2 ms                                                               | 29.9 ms: 1.74x slower                                        |
| Geometric mean  | (ref)                                                                 | 1.65x slower                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.17 sec: 1.55x faster                                       |
| async_tree_io              | 1.79 sec                                                              | 1.29 sec: 1.38x faster                                       |
| bench_mp_pool              | 18.4 ms                                                               | 13.3 ms: 1.38x faster                                        |
| async_tree_memoization_tg  | 935 ms                                                                | 729 ms: 1.28x faster                                         |
| gc_traversal               | 5.61 ms                                                               | 4.47 ms: 1.25x faster                                        |
| async_tree_memoization     | 949 ms                                                                | 766 ms: 1.24x faster                                         |
| async_tree_none_tg         | 692 ms                                                                | 583 ms: 1.19x faster                                         |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 938 ms: 1.17x faster                                         |
| xml_etree_parse            | 230 ms                                                                | 200 ms: 1.15x faster                                         |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 988 ms: 1.15x faster                                         |
| async_tree_none            | 740 ms                                                                | 654 ms: 1.13x faster                                         |
| pickle_dict                | 46.5 us                                                               | 43.3 us: 1.08x faster                                        |
| create_gc_cycles           | 2.02 ms                                                               | 1.91 ms: 1.06x faster                                        |
| regex_effbot               | 4.97 ms                                                               | 5.22 ms: 1.05x slower                                        |
| unpickle                   | 19.7 us                                                               | 21.4 us: 1.09x slower                                        |
| regex_dna                  | 287 ms                                                                | 312 ms: 1.09x slower                                         |
| pickle_list                | 6.40 us                                                               | 6.97 us: 1.09x slower                                        |
| dulwich_log                | 114 ms                                                                | 128 ms: 1.12x slower                                         |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 8.40 ms: 1.12x slower                                        |
| pathlib                    | 31.7 ms                                                               | 36.1 ms: 1.14x slower                                        |
| regex_v8                   | 31.1 ms                                                               | 35.5 ms: 1.14x slower                                        |
| sqlite_synth               | 3.75 us                                                               | 4.31 us: 1.15x slower                                        |
| pylint                     | 501 ms                                                                | 576 ms: 1.15x slower                                         |
| async_generators           | 617 ms                                                                | 718 ms: 1.16x slower                                         |
| json_loads                 | 36.6 us                                                               | 42.7 us: 1.17x slower                                        |
| generators                 | 46.0 ms                                                               | 54.0 ms: 1.17x slower                                        |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.29 sec: 1.18x slower                                       |
| xml_etree_generate         | 128 ms                                                                | 153 ms: 1.19x slower                                         |
| json                       | 6.68 ms                                                               | 7.98 ms: 1.19x slower                                        |
| scimark_fft                | 499 ms                                                                | 604 ms: 1.21x slower                                         |
| docutils                   | 4.06 sec                                                              | 4.93 sec: 1.21x slower                                       |
| asyncio_tcp                | 958 ms                                                                | 1.17 sec: 1.22x slower                                       |
| pycparser                  | 1.73 sec                                                              | 2.13 sec: 1.23x slower                                       |
| bench_thread_pool          | 3.11 ms                                                               | 3.85 ms: 1.24x slower                                        |
| comprehensions             | 29.6 us                                                               | 36.9 us: 1.25x slower                                        |
| crypto_pyaes               | 112 ms                                                                | 142 ms: 1.27x slower                                         |
| mdp                        | 3.84 sec                                                              | 4.87 sec: 1.27x slower                                       |
| gunicorn                   | 1.98 ms                                                               | 2.53 ms: 1.28x slower                                        |
| json_dumps                 | 13.6 ms                                                               | 18.0 ms: 1.32x slower                                        |
| meteor_contest             | 149 ms                                                                | 198 ms: 1.33x slower                                         |
| fannkuch                   | 551 ms                                                                | 738 ms: 1.34x slower                                         |
| python_startup_no_site     | 16.3 ms                                                               | 21.9 ms: 1.35x slower                                        |
| tornado_http               | 262 ms                                                                | 356 ms: 1.36x slower                                         |
| nqueens                    | 110 ms                                                                | 151 ms: 1.38x slower                                         |
| regex_compile              | 197 ms                                                                | 271 ms: 1.38x slower                                         |
| sympy_integrate            | 31.4 ms                                                               | 43.4 ms: 1.38x slower                                        |
| coroutines                 | 30.1 ms                                                               | 42.2 ms: 1.40x slower                                        |
| tomli_loads                | 2.99 sec                                                              | 4.19 sec: 1.40x slower                                       |
| thrift                     | 1.17 ms                                                               | 1.65 ms: 1.41x slower                                        |
| 2to3                       | 444 ms                                                                | 648 ms: 1.46x slower                                         |
| spectral_norm              | 158 ms                                                                | 231 ms: 1.46x slower                                         |
| deepcopy_memo              | 57.5 us                                                               | 84.2 us: 1.47x slower                                        |
| telco                      | 9.71 ms                                                               | 14.3 ms: 1.47x slower                                        |
| xml_etree_process          | 85.7 ms                                                               | 126 ms: 1.47x slower                                         |
| deepcopy                   | 503 us                                                                | 744 us: 1.48x slower                                         |
| logging_format             | 11.8 us                                                               | 17.6 us: 1.49x slower                                        |
| bpe_tokeniser              | 6.63 sec                                                              | 9.94 sec: 1.50x slower                                       |
| coverage                   | 97.6 ms                                                               | 148 ms: 1.52x slower                                         |
| float                      | 127 ms                                                                | 193 ms: 1.52x slower                                         |
| sqlglot_normalize          | 148 ms                                                                | 225 ms: 1.52x slower                                         |
| html5lib                   | 95.8 ms                                                               | 147 ms: 1.53x slower                                         |
| aiohttp                    | 1.92 ms                                                               | 2.97 ms: 1.55x slower                                        |
| pyflate                    | 661 ms                                                                | 1.03 sec: 1.56x slower                                       |
| sympy_str                  | 425 ms                                                                | 664 ms: 1.56x slower                                         |
| django_template            | 48.6 ms                                                               | 76.1 ms: 1.57x slower                                        |
| deepcopy_reduce            | 4.45 us                                                               | 7.05 us: 1.58x slower                                        |
| python_startup             | 21.2 ms                                                               | 33.8 ms: 1.59x slower                                        |
| sqlglot_optimize           | 76.5 ms                                                               | 122 ms: 1.59x slower                                         |
| genshi_xml                 | 73.6 ms                                                               | 118 ms: 1.61x slower                                         |
| unpickle_pure_python       | 319 us                                                                | 515 us: 1.61x slower                                         |
| logging_simple             | 9.89 us                                                               | 16.1 us: 1.63x slower                                        |
| typing_runtime_protocols   | 199 us                                                                | 329 us: 1.65x slower                                         |
| pprint_pformat             | 2.03 sec                                                              | 3.42 sec: 1.69x slower                                       |
| scimark_monte_carlo        | 98.5 ms                                                               | 167 ms: 1.70x slower                                         |
| genshi_text                | 31.9 ms                                                               | 54.3 ms: 1.70x slower                                        |
| richards                   | 63.4 ms                                                               | 108 ms: 1.70x slower                                         |
| mako                       | 17.2 ms                                                               | 29.9 ms: 1.74x slower                                        |
| raytrace                   | 418 ms                                                                | 740 ms: 1.77x slower                                         |
| pprint_safe_repr           | 970 ms                                                                | 1.74 sec: 1.79x slower                                       |
| chaos                      | 93.7 ms                                                               | 168 ms: 1.79x slower                                         |
| sympy_expand               | 689 ms                                                                | 1.24 sec: 1.80x slower                                       |
| hexiom                     | 8.87 ms                                                               | 16.3 ms: 1.84x slower                                        |
| sqlglot_transpile          | 2.28 ms                                                               | 4.25 ms: 1.86x slower                                        |
| richards_super             | 67.9 ms                                                               | 130 ms: 1.92x slower                                         |
| logging_silent             | 135 ns                                                                | 262 ns: 1.93x slower                                         |
| chameleon                  | 9.30 ms                                                               | 18.1 ms: 1.95x slower                                        |
| pickle_pure_python         | 447 us                                                                | 872 us: 1.95x slower                                         |
| sqlglot_parse              | 1.89 ms                                                               | 3.76 ms: 1.99x slower                                        |
| scimark_sor                | 171 ms                                                                | 345 ms: 2.02x slower                                         |
| scimark_lu                 | 155 ms                                                                | 313 ms: 2.03x slower                                         |
| sympy_sum                  | 229 ms                                                                | 466 ms: 2.03x slower                                         |
| deltablue                  | 5.05 ms                                                               | 10.7 ms: 2.12x slower                                        |
| nbody                      | 125 ms                                                                | 267 ms: 2.14x slower                                         |
| go                         | 185 ms                                                                | 401 ms: 2.17x slower                                         |
| flaskblogging              | 6.74 ms                                                               | 17.1 ms: 2.55x slower                                        |
| unpack_sequence            | 68.5 ns                                                               | 193 ns: 2.81x slower                                         |
| Geometric mean             | (ref)                                                                 | 1.35x slower                                                 |

Benchmark hidden because not significant (5): unpickle_list, pickle, pidigits, xml_etree_iterparse, asyncio_websockets
Ignored benchmarks (4) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: dask, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 2.20x