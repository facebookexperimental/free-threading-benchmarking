# Results vs. 3.12.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4606eff
- commit date: 2024-07-23
- overall geometric mean: 1.34x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 2.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 444 ms                                                                | 664 ms: 1.49x slower                                  |
| docutils       | 4.06 sec                                                              | 4.86 sec: 1.20x slower                                |
| html5lib       | 95.8 ms                                                               | 157 ms: 1.64x slower                                  |
| tornado_http   | 262 ms                                                                | 320 ms: 1.22x slower                                  |
| Geometric mean | (ref)                                                                 | 1.37x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.17 sec: 1.55x faster                                |
| async_tree_io              | 1.79 sec                                                              | 1.22 sec: 1.46x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 654 ms: 1.43x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 493 ms: 1.40x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 733 ms: 1.29x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 859 ms: 1.28x faster                                  |
| async_tree_none            | 740 ms                                                                | 593 ms: 1.25x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 945 ms: 1.20x faster                                  |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.27 sec: 1.17x slower                                |
| async_generators           | 617 ms                                                                | 724 ms: 1.17x slower                                  |
| asyncio_tcp                | 958 ms                                                                | 1.12 sec: 1.17x slower                                |
| coroutines                 | 30.1 ms                                                               | 45.6 ms: 1.51x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.13x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 255 ms                                                                | 243 ms: 1.05x faster                                  |
| float          | 127 ms                                                                | 200 ms: 1.58x slower                                  |
| nbody          | 125 ms                                                                | 283 ms: 2.27x slower                                  |
| Geometric mean | (ref)                                                                 | 1.51x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.97 ms                                                               | 4.80 ms: 1.03x faster                                 |
| regex_dna      | 287 ms                                                                | 301 ms: 1.05x slower                                  |
| regex_v8       | 31.1 ms                                                               | 33.7 ms: 1.08x slower                                 |
| regex_compile  | 197 ms                                                                | 292 ms: 1.48x slower                                  |
| Geometric mean | (ref)                                                                 | 1.13x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 46.5 us                                                               | 42.9 us: 1.09x faster                                 |
| xml_etree_parse      | 230 ms                                                                | 213 ms: 1.08x faster                                  |
| pickle               | 14.8 us                                                               | 14.3 us: 1.04x faster                                 |
| xml_etree_iterparse  | 157 ms                                                                | 164 ms: 1.04x slower                                  |
| unpickle             | 19.7 us                                                               | 21.2 us: 1.07x slower                                 |
| xml_etree_generate   | 128 ms                                                                | 158 ms: 1.23x slower                                  |
| json_loads           | 36.6 us                                                               | 45.2 us: 1.24x slower                                 |
| tomli_loads          | 2.99 sec                                                              | 4.14 sec: 1.39x slower                                |
| json_dumps           | 13.6 ms                                                               | 18.9 ms: 1.39x slower                                 |
| xml_etree_process    | 85.7 ms                                                               | 124 ms: 1.44x slower                                  |
| unpickle_pure_python | 319 us                                                                | 540 us: 1.69x slower                                  |
| pickle_pure_python   | 447 us                                                                | 760 us: 1.70x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.19x slower                                          |

Benchmark hidden because not significant (2): unpickle_list, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 20.9 ms: 1.28x slower                                 |
| python_startup         | 21.2 ms                                                               | 29.5 ms: 1.39x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.34x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 122 ms: 1.66x slower                                  |
| django_template | 48.6 ms                                                               | 84.5 ms: 1.74x slower                                 |
| genshi_text     | 31.9 ms                                                               | 55.7 ms: 1.75x slower                                 |
| mako            | 17.2 ms                                                               | 31.9 ms: 1.85x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.75x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.17 sec: 1.55x faster                                |
| async_tree_io              | 1.79 sec                                                              | 1.22 sec: 1.46x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 654 ms: 1.43x faster                                  |
| async_tree_none_tg         | 692 ms                                                                | 493 ms: 1.40x faster                                  |
| bench_mp_pool              | 18.4 ms                                                               | 13.3 ms: 1.38x faster                                 |
| async_tree_memoization     | 949 ms                                                                | 733 ms: 1.29x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 859 ms: 1.28x faster                                  |
| async_tree_none            | 740 ms                                                                | 593 ms: 1.25x faster                                  |
| gc_traversal               | 5.61 ms                                                               | 4.60 ms: 1.22x faster                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 945 ms: 1.20x faster                                  |
| create_gc_cycles           | 2.02 ms                                                               | 1.82 ms: 1.11x faster                                 |
| pickle_dict                | 46.5 us                                                               | 42.9 us: 1.09x faster                                 |
| xml_etree_parse            | 230 ms                                                                | 213 ms: 1.08x faster                                  |
| pidigits                   | 255 ms                                                                | 243 ms: 1.05x faster                                  |
| pickle                     | 14.8 us                                                               | 14.3 us: 1.04x faster                                 |
| regex_effbot               | 4.97 ms                                                               | 4.80 ms: 1.03x faster                                 |
| xml_etree_iterparse        | 157 ms                                                                | 164 ms: 1.04x slower                                  |
| regex_dna                  | 287 ms                                                                | 301 ms: 1.05x slower                                  |
| unpickle                   | 19.7 us                                                               | 21.2 us: 1.07x slower                                 |
| regex_v8                   | 31.1 ms                                                               | 33.7 ms: 1.08x slower                                 |
| sqlite_synth               | 3.75 us                                                               | 4.23 us: 1.13x slower                                 |
| pylint                     | 501 ms                                                                | 582 ms: 1.16x slower                                  |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 8.70 ms: 1.16x slower                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.27 sec: 1.17x slower                                |
| async_generators           | 617 ms                                                                | 724 ms: 1.17x slower                                  |
| asyncio_tcp                | 958 ms                                                                | 1.12 sec: 1.17x slower                                |
| deepcopy                   | 503 us                                                                | 594 us: 1.18x slower                                  |
| generators                 | 46.0 ms                                                               | 54.9 ms: 1.19x slower                                 |
| docutils                   | 4.06 sec                                                              | 4.86 sec: 1.20x slower                                |
| deepcopy_memo              | 57.5 us                                                               | 69.7 us: 1.21x slower                                 |
| tornado_http               | 262 ms                                                                | 320 ms: 1.22x slower                                  |
| dulwich_log                | 114 ms                                                                | 140 ms: 1.22x slower                                  |
| xml_etree_generate         | 128 ms                                                                | 158 ms: 1.23x slower                                  |
| scimark_fft                | 499 ms                                                                | 617 ms: 1.24x slower                                  |
| json_loads                 | 36.6 us                                                               | 45.2 us: 1.24x slower                                 |
| pycparser                  | 1.73 sec                                                              | 2.16 sec: 1.25x slower                                |
| python_startup_no_site     | 16.3 ms                                                               | 20.9 ms: 1.28x slower                                 |
| json                       | 6.68 ms                                                               | 8.61 ms: 1.29x slower                                 |
| bench_thread_pool          | 3.11 ms                                                               | 4.01 ms: 1.29x slower                                 |
| comprehensions             | 29.6 us                                                               | 38.3 us: 1.30x slower                                 |
| deepcopy_reduce            | 4.45 us                                                               | 5.85 us: 1.31x slower                                 |
| mdp                        | 3.84 sec                                                              | 5.10 sec: 1.33x slower                                |
| meteor_contest             | 149 ms                                                                | 199 ms: 1.34x slower                                  |
| telco                      | 9.71 ms                                                               | 13.4 ms: 1.38x slower                                 |
| nqueens                    | 110 ms                                                                | 152 ms: 1.38x slower                                  |
| tomli_loads                | 2.99 sec                                                              | 4.14 sec: 1.39x slower                                |
| python_startup             | 21.2 ms                                                               | 29.5 ms: 1.39x slower                                 |
| json_dumps                 | 13.6 ms                                                               | 18.9 ms: 1.39x slower                                 |
| sympy_integrate            | 31.4 ms                                                               | 43.9 ms: 1.40x slower                                 |
| logging_format             | 11.8 us                                                               | 16.6 us: 1.41x slower                                 |
| crypto_pyaes               | 112 ms                                                                | 157 ms: 1.41x slower                                  |
| fannkuch                   | 551 ms                                                                | 783 ms: 1.42x slower                                  |
| xml_etree_process          | 85.7 ms                                                               | 124 ms: 1.44x slower                                  |
| regex_compile              | 197 ms                                                                | 292 ms: 1.48x slower                                  |
| 2to3                       | 444 ms                                                                | 664 ms: 1.49x slower                                  |
| thrift                     | 1.17 ms                                                               | 1.75 ms: 1.50x slower                                 |
| coroutines                 | 30.1 ms                                                               | 45.6 ms: 1.51x slower                                 |
| bpe_tokeniser              | 6.63 sec                                                              | 10.1 sec: 1.52x slower                                |
| logging_simple             | 9.89 us                                                               | 15.2 us: 1.54x slower                                 |
| sqlglot_normalize          | 148 ms                                                                | 230 ms: 1.55x slower                                  |
| coverage                   | 97.6 ms                                                               | 151 ms: 1.55x slower                                  |
| spectral_norm              | 158 ms                                                                | 247 ms: 1.57x slower                                  |
| float                      | 127 ms                                                                | 200 ms: 1.58x slower                                  |
| sympy_str                  | 425 ms                                                                | 685 ms: 1.61x slower                                  |
| sqlglot_optimize           | 76.5 ms                                                               | 124 ms: 1.62x slower                                  |
| html5lib                   | 95.8 ms                                                               | 157 ms: 1.64x slower                                  |
| scimark_monte_carlo        | 98.5 ms                                                               | 163 ms: 1.65x slower                                  |
| genshi_xml                 | 73.6 ms                                                               | 122 ms: 1.66x slower                                  |
| unpickle_pure_python       | 319 us                                                                | 540 us: 1.69x slower                                  |
| pickle_pure_python         | 447 us                                                                | 760 us: 1.70x slower                                  |
| pyflate                    | 661 ms                                                                | 1.13 sec: 1.71x slower                                |
| typing_runtime_protocols   | 199 us                                                                | 342 us: 1.71x slower                                  |
| django_template            | 48.6 ms                                                               | 84.5 ms: 1.74x slower                                 |
| genshi_text                | 31.9 ms                                                               | 55.7 ms: 1.75x slower                                 |
| pprint_pformat             | 2.03 sec                                                              | 3.55 sec: 1.75x slower                                |
| richards                   | 63.4 ms                                                               | 112 ms: 1.76x slower                                  |
| pprint_safe_repr           | 970 ms                                                                | 1.71 sec: 1.77x slower                                |
| logging_silent             | 135 ns                                                                | 246 ns: 1.82x slower                                  |
| sympy_expand               | 689 ms                                                                | 1.27 sec: 1.84x slower                                |
| mako                       | 17.2 ms                                                               | 31.9 ms: 1.85x slower                                 |
| chaos                      | 93.7 ms                                                               | 175 ms: 1.87x slower                                  |
| hexiom                     | 8.87 ms                                                               | 16.7 ms: 1.89x slower                                 |
| raytrace                   | 418 ms                                                                | 807 ms: 1.93x slower                                  |
| richards_super             | 67.9 ms                                                               | 133 ms: 1.96x slower                                  |
| scimark_sor                | 171 ms                                                                | 341 ms: 1.99x slower                                  |
| sqlglot_transpile          | 2.28 ms                                                               | 4.58 ms: 2.01x slower                                 |
| scimark_lu                 | 155 ms                                                                | 314 ms: 2.03x slower                                  |
| sympy_sum                  | 229 ms                                                                | 476 ms: 2.08x slower                                  |
| sqlglot_parse              | 1.89 ms                                                               | 3.99 ms: 2.11x slower                                 |
| go                         | 185 ms                                                                | 411 ms: 2.22x slower                                  |
| deltablue                  | 5.05 ms                                                               | 11.4 ms: 2.26x slower                                 |
| nbody                      | 125 ms                                                                | 283 ms: 2.27x slower                                  |
| unpack_sequence            | 68.5 ns                                                               | 200 ns: 2.92x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.34x slower                                          |

Benchmark hidden because not significant (4): asyncio_websockets, unpickle_list, pickle_list, pathlib
Ignored benchmarks (8) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 2.25x