# Results vs. 3.12.0b1

- fork: python
- ref: e73e7a7abdc3fed252af
- machine: linux-x86_64
- commit hash: e73e7a7
- commit date: 2024-08-07
- overall geometric mean: 1.33x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 2.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 444 ms                                                                | 651 ms: 1.47x slower                                                  |
| docutils       | 4.06 sec                                                              | 4.92 sec: 1.21x slower                                                |
| html5lib       | 95.8 ms                                                               | 137 ms: 1.43x slower                                                  |
| tornado_http   | 262 ms                                                                | 319 ms: 1.21x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.32x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.12 sec: 1.61x faster                                                |
| async_tree_memoization_tg  | 935 ms                                                                | 619 ms: 1.51x faster                                                  |
| async_tree_io              | 1.79 sec                                                              | 1.25 sec: 1.43x faster                                                |
| async_tree_none_tg         | 692 ms                                                                | 489 ms: 1.42x faster                                                  |
| async_tree_memoization     | 949 ms                                                                | 724 ms: 1.31x faster                                                  |
| async_tree_none            | 740 ms                                                                | 584 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 874 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 951 ms: 1.19x faster                                                  |
| asyncio_tcp                | 958 ms                                                                | 1.09 sec: 1.14x slower                                                |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.34 sec: 1.19x slower                                                |
| async_generators           | 617 ms                                                                | 747 ms: 1.21x slower                                                  |
| coroutines                 | 30.1 ms                                                               | 42.7 ms: 1.42x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.14x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 255 ms                                                                | 239 ms: 1.06x faster                                                  |
| float          | 127 ms                                                                | 194 ms: 1.53x slower                                                  |
| nbody          | 125 ms                                                                | 281 ms: 2.26x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.48x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 31.1 ms                                                               | 35.6 ms: 1.14x slower                                                 |
| regex_compile  | 197 ms                                                                | 296 ms: 1.50x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.14x slower                                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 46.5 us                                                               | 43.1 us: 1.08x faster                                                 |
| xml_etree_parse      | 230 ms                                                                | 218 ms: 1.05x faster                                                  |
| xml_etree_iterparse  | 157 ms                                                                | 168 ms: 1.07x slower                                                  |
| unpickle_list        | 7.19 us                                                               | 7.70 us: 1.07x slower                                                 |
| pickle_list          | 6.40 us                                                               | 6.90 us: 1.08x slower                                                 |
| json_loads           | 36.6 us                                                               | 41.2 us: 1.13x slower                                                 |
| unpickle             | 19.7 us                                                               | 22.3 us: 1.13x slower                                                 |
| xml_etree_generate   | 128 ms                                                                | 159 ms: 1.24x slower                                                  |
| json_dumps           | 13.6 ms                                                               | 18.0 ms: 1.33x slower                                                 |
| tomli_loads          | 2.99 sec                                                              | 4.14 sec: 1.39x slower                                                |
| xml_etree_process    | 85.7 ms                                                               | 127 ms: 1.48x slower                                                  |
| unpickle_pure_python | 319 us                                                                | 544 us: 1.71x slower                                                  |
| pickle_pure_python   | 447 us                                                                | 846 us: 1.89x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.21x slower                                                          |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 19.4 ms: 1.19x slower                                                 |
| python_startup         | 21.2 ms                                                               | 28.9 ms: 1.36x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.27x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 111 ms: 1.51x slower                                                  |
| django_template | 48.6 ms                                                               | 79.6 ms: 1.64x slower                                                 |
| genshi_text     | 31.9 ms                                                               | 53.4 ms: 1.67x slower                                                 |
| mako            | 17.2 ms                                                               | 31.0 ms: 1.80x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.65x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.12 sec: 1.61x faster                                                |
| async_tree_memoization_tg  | 935 ms                                                                | 619 ms: 1.51x faster                                                  |
| async_tree_io              | 1.79 sec                                                              | 1.25 sec: 1.43x faster                                                |
| async_tree_none_tg         | 692 ms                                                                | 489 ms: 1.42x faster                                                  |
| gc_traversal               | 5.61 ms                                                               | 4.19 ms: 1.34x faster                                                 |
| async_tree_memoization     | 949 ms                                                                | 724 ms: 1.31x faster                                                  |
| async_tree_none            | 740 ms                                                                | 584 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 874 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 951 ms: 1.19x faster                                                  |
| create_gc_cycles           | 2.02 ms                                                               | 1.80 ms: 1.13x faster                                                 |
| pickle_dict                | 46.5 us                                                               | 43.1 us: 1.08x faster                                                 |
| pidigits                   | 255 ms                                                                | 239 ms: 1.06x faster                                                  |
| xml_etree_parse            | 230 ms                                                                | 218 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 157 ms                                                                | 168 ms: 1.07x slower                                                  |
| unpickle_list              | 7.19 us                                                               | 7.70 us: 1.07x slower                                                 |
| pickle_list                | 6.40 us                                                               | 6.90 us: 1.08x slower                                                 |
| deepcopy                   | 503 us                                                                | 560 us: 1.11x slower                                                  |
| json_loads                 | 36.6 us                                                               | 41.2 us: 1.13x slower                                                 |
| unpickle                   | 19.7 us                                                               | 22.3 us: 1.13x slower                                                 |
| asyncio_tcp                | 958 ms                                                                | 1.09 sec: 1.14x slower                                                |
| regex_v8                   | 31.1 ms                                                               | 35.6 ms: 1.14x slower                                                 |
| pylint                     | 501 ms                                                                | 579 ms: 1.16x slower                                                  |
| deepcopy_memo              | 57.5 us                                                               | 67.1 us: 1.17x slower                                                 |
| sqlite_synth               | 3.75 us                                                               | 4.42 us: 1.18x slower                                                 |
| python_startup_no_site     | 16.3 ms                                                               | 19.4 ms: 1.19x slower                                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 8.91 ms: 1.19x slower                                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.34 sec: 1.19x slower                                                |
| generators                 | 46.0 ms                                                               | 55.0 ms: 1.20x slower                                                 |
| async_generators           | 617 ms                                                                | 747 ms: 1.21x slower                                                  |
| docutils                   | 4.06 sec                                                              | 4.92 sec: 1.21x slower                                                |
| json                       | 6.68 ms                                                               | 8.10 ms: 1.21x slower                                                 |
| tornado_http               | 262 ms                                                                | 319 ms: 1.21x slower                                                  |
| xml_etree_generate         | 128 ms                                                                | 159 ms: 1.24x slower                                                  |
| scimark_fft                | 499 ms                                                                | 624 ms: 1.25x slower                                                  |
| pycparser                  | 1.73 sec                                                              | 2.21 sec: 1.28x slower                                                |
| deepcopy_reduce            | 4.45 us                                                               | 5.70 us: 1.28x slower                                                 |
| meteor_contest             | 149 ms                                                                | 192 ms: 1.29x slower                                                  |
| comprehensions             | 29.6 us                                                               | 38.7 us: 1.31x slower                                                 |
| json_dumps                 | 13.6 ms                                                               | 18.0 ms: 1.33x slower                                                 |
| mdp                        | 3.84 sec                                                              | 5.13 sec: 1.33x slower                                                |
| python_startup             | 21.2 ms                                                               | 28.9 ms: 1.36x slower                                                 |
| fannkuch                   | 551 ms                                                                | 762 ms: 1.38x slower                                                  |
| logging_format             | 11.8 us                                                               | 16.4 us: 1.39x slower                                                 |
| tomli_loads                | 2.99 sec                                                              | 4.14 sec: 1.39x slower                                                |
| crypto_pyaes               | 112 ms                                                                | 156 ms: 1.40x slower                                                  |
| nqueens                    | 110 ms                                                                | 155 ms: 1.41x slower                                                  |
| coroutines                 | 30.1 ms                                                               | 42.7 ms: 1.42x slower                                                 |
| html5lib                   | 95.8 ms                                                               | 137 ms: 1.43x slower                                                  |
| thrift                     | 1.17 ms                                                               | 1.67 ms: 1.43x slower                                                 |
| sympy_integrate            | 31.4 ms                                                               | 44.9 ms: 1.43x slower                                                 |
| telco                      | 9.71 ms                                                               | 14.0 ms: 1.44x slower                                                 |
| bench_thread_pool          | 3.11 ms                                                               | 4.52 ms: 1.45x slower                                                 |
| 2to3                       | 444 ms                                                                | 651 ms: 1.47x slower                                                  |
| xml_etree_process          | 85.7 ms                                                               | 127 ms: 1.48x slower                                                  |
| coverage                   | 97.6 ms                                                               | 146 ms: 1.50x slower                                                  |
| regex_compile              | 197 ms                                                                | 296 ms: 1.50x slower                                                  |
| genshi_xml                 | 73.6 ms                                                               | 111 ms: 1.51x slower                                                  |
| float                      | 127 ms                                                                | 194 ms: 1.53x slower                                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 10.1 sec: 1.53x slower                                                |
| sqlglot_normalize          | 148 ms                                                                | 229 ms: 1.54x slower                                                  |
| logging_simple             | 9.89 us                                                               | 15.4 us: 1.55x slower                                                 |
| richards                   | 63.4 ms                                                               | 99.2 ms: 1.56x slower                                                 |
| spectral_norm              | 158 ms                                                                | 247 ms: 1.57x slower                                                  |
| sqlglot_optimize           | 76.5 ms                                                               | 121 ms: 1.58x slower                                                  |
| sympy_str                  | 425 ms                                                                | 675 ms: 1.59x slower                                                  |
| pyflate                    | 661 ms                                                                | 1.07 sec: 1.61x slower                                                |
| scimark_monte_carlo        | 98.5 ms                                                               | 159 ms: 1.61x slower                                                  |
| django_template            | 48.6 ms                                                               | 79.6 ms: 1.64x slower                                                 |
| typing_runtime_protocols   | 199 us                                                                | 327 us: 1.64x slower                                                  |
| pprint_pformat             | 2.03 sec                                                              | 3.39 sec: 1.67x slower                                                |
| genshi_text                | 31.9 ms                                                               | 53.4 ms: 1.67x slower                                                 |
| pprint_safe_repr           | 970 ms                                                                | 1.65 sec: 1.70x slower                                                |
| unpickle_pure_python       | 319 us                                                                | 544 us: 1.71x slower                                                  |
| mako                       | 17.2 ms                                                               | 31.0 ms: 1.80x slower                                                 |
| chaos                      | 93.7 ms                                                               | 170 ms: 1.81x slower                                                  |
| hexiom                     | 8.87 ms                                                               | 16.3 ms: 1.84x slower                                                 |
| logging_silent             | 135 ns                                                                | 249 ns: 1.84x slower                                                  |
| sympy_expand               | 689 ms                                                                | 1.29 sec: 1.87x slower                                                |
| richards_super             | 67.9 ms                                                               | 127 ms: 1.87x slower                                                  |
| pickle_pure_python         | 447 us                                                                | 846 us: 1.89x slower                                                  |
| sqlglot_transpile          | 2.28 ms                                                               | 4.32 ms: 1.89x slower                                                 |
| raytrace                   | 418 ms                                                                | 801 ms: 1.92x slower                                                  |
| sympy_sum                  | 229 ms                                                                | 443 ms: 1.94x slower                                                  |
| sqlglot_parse              | 1.89 ms                                                               | 3.76 ms: 1.99x slower                                                 |
| scimark_sor                | 171 ms                                                                | 340 ms: 1.99x slower                                                  |
| scimark_lu                 | 155 ms                                                                | 313 ms: 2.02x slower                                                  |
| nbody                      | 125 ms                                                                | 281 ms: 2.26x slower                                                  |
| deltablue                  | 5.05 ms                                                               | 11.6 ms: 2.29x slower                                                 |
| go                         | 185 ms                                                                | 434 ms: 2.35x slower                                                  |
| unpack_sequence            | 68.5 ns                                                               | 190 ns: 2.78x slower                                                  |
| Geometric mean             | (ref)                                                                 | 1.33x slower                                                          |

Benchmark hidden because not significant (6): regex_effbot, pickle, asyncio_websockets, regex_dna, bench_mp_pool, pathlib
Ignored benchmarks (9) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 2.25x