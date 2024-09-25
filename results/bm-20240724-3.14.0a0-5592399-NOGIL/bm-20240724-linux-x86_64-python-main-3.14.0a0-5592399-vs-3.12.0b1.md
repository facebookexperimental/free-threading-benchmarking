# Results vs. 3.12.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5592399
- commit date: 2024-07-24
- overall geometric mean: 1.35x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 2.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 444 ms                                                                | 662 ms: 1.49x slower                                  |
| docutils       | 4.06 sec                                                              | 4.97 sec: 1.22x slower                                |
| html5lib       | 95.8 ms                                                               | 137 ms: 1.43x slower                                  |
| tornado_http   | 262 ms                                                                | 339 ms: 1.29x slower                                  |
| Geometric mean | (ref)                                                                 | 1.35x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.17 sec: 1.55x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 652 ms: 1.43x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.27 sec: 1.41x faster                                |
| async_tree_none_tg         | 692 ms                                                                | 514 ms: 1.35x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 850 ms: 1.29x faster                                  |
| async_tree_none            | 740 ms                                                                | 586 ms: 1.26x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 759 ms: 1.25x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 959 ms: 1.18x faster                                  |
| asyncio_tcp                | 958 ms                                                                | 1.08 sec: 1.12x slower                                |
| async_generators           | 617 ms                                                                | 721 ms: 1.17x slower                                  |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.42 sec: 1.22x slower                                |
| coroutines                 | 30.1 ms                                                               | 41.7 ms: 1.38x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.12x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 255 ms                                                                | 241 ms: 1.06x faster                                  |
| float          | 127 ms                                                                | 211 ms: 1.66x slower                                  |
| nbody          | 125 ms                                                                | 278 ms: 2.23x slower                                  |
| Geometric mean | (ref)                                                                 | 1.52x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.97 ms                                                               | 4.76 ms: 1.04x faster                                 |
| regex_v8       | 31.1 ms                                                               | 37.6 ms: 1.21x slower                                 |
| regex_compile  | 197 ms                                                                | 307 ms: 1.56x slower                                  |
| Geometric mean | (ref)                                                                 | 1.16x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| xml_etree_parse      | 230 ms                                                                | 208 ms: 1.10x faster                                  |
| pickle_list          | 6.40 us                                                               | 6.68 us: 1.04x slower                                 |
| xml_etree_iterparse  | 157 ms                                                                | 169 ms: 1.07x slower                                  |
| unpickle_list        | 7.19 us                                                               | 7.97 us: 1.11x slower                                 |
| unpickle             | 19.7 us                                                               | 22.0 us: 1.11x slower                                 |
| json_loads           | 36.6 us                                                               | 45.6 us: 1.25x slower                                 |
| xml_etree_generate   | 128 ms                                                                | 164 ms: 1.28x slower                                  |
| json_dumps           | 13.6 ms                                                               | 19.0 ms: 1.40x slower                                 |
| tomli_loads          | 2.99 sec                                                              | 4.32 sec: 1.45x slower                                |
| xml_etree_process    | 85.7 ms                                                               | 127 ms: 1.48x slower                                  |
| unpickle_pure_python | 319 us                                                                | 547 us: 1.71x slower                                  |
| pickle_pure_python   | 447 us                                                                | 801 us: 1.79x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.23x slower                                          |

Benchmark hidden because not significant (2): pickle, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 19.3 ms: 1.19x slower                                 |
| python_startup         | 21.2 ms                                                               | 29.1 ms: 1.37x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.28x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text     | 31.9 ms                                                               | 53.7 ms: 1.68x slower                                 |
| genshi_xml      | 73.6 ms                                                               | 125 ms: 1.70x slower                                  |
| django_template | 48.6 ms                                                               | 86.4 ms: 1.78x slower                                 |
| mako            | 17.2 ms                                                               | 31.1 ms: 1.81x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.74x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.17 sec: 1.55x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 652 ms: 1.43x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.27 sec: 1.41x faster                                |
| async_tree_none_tg         | 692 ms                                                                | 514 ms: 1.35x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 850 ms: 1.29x faster                                  |
| bench_mp_pool              | 18.4 ms                                                               | 14.4 ms: 1.27x faster                                 |
| async_tree_none            | 740 ms                                                                | 586 ms: 1.26x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 759 ms: 1.25x faster                                  |
| gc_traversal               | 5.61 ms                                                               | 4.51 ms: 1.24x faster                                 |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 959 ms: 1.18x faster                                  |
| xml_etree_parse            | 230 ms                                                                | 208 ms: 1.10x faster                                  |
| pidigits                   | 255 ms                                                                | 241 ms: 1.06x faster                                  |
| create_gc_cycles           | 2.02 ms                                                               | 1.93 ms: 1.05x faster                                 |
| regex_effbot               | 4.97 ms                                                               | 4.76 ms: 1.04x faster                                 |
| pickle_list                | 6.40 us                                                               | 6.68 us: 1.04x slower                                 |
| xml_etree_iterparse        | 157 ms                                                                | 169 ms: 1.07x slower                                  |
| pathlib                    | 31.7 ms                                                               | 34.2 ms: 1.08x slower                                 |
| deepcopy                   | 503 us                                                                | 556 us: 1.10x slower                                  |
| unpickle_list              | 7.19 us                                                               | 7.97 us: 1.11x slower                                 |
| unpickle                   | 19.7 us                                                               | 22.0 us: 1.11x slower                                 |
| asyncio_tcp                | 958 ms                                                                | 1.08 sec: 1.12x slower                                |
| generators                 | 46.0 ms                                                               | 53.4 ms: 1.16x slower                                 |
| async_generators           | 617 ms                                                                | 721 ms: 1.17x slower                                  |
| sqlite_synth               | 3.75 us                                                               | 4.39 us: 1.17x slower                                 |
| dulwich_log                | 114 ms                                                                | 134 ms: 1.18x slower                                  |
| pylint                     | 501 ms                                                                | 592 ms: 1.18x slower                                  |
| python_startup_no_site     | 16.3 ms                                                               | 19.3 ms: 1.19x slower                                 |
| regex_v8                   | 31.1 ms                                                               | 37.6 ms: 1.21x slower                                 |
| json                       | 6.68 ms                                                               | 8.11 ms: 1.21x slower                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 9.09 ms: 1.22x slower                                 |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.42 sec: 1.22x slower                                |
| docutils                   | 4.06 sec                                                              | 4.97 sec: 1.22x slower                                |
| deepcopy_memo              | 57.5 us                                                               | 70.5 us: 1.23x slower                                 |
| scimark_fft                | 499 ms                                                                | 616 ms: 1.23x slower                                  |
| json_loads                 | 36.6 us                                                               | 45.6 us: 1.25x slower                                 |
| xml_etree_generate         | 128 ms                                                                | 164 ms: 1.28x slower                                  |
| mdp                        | 3.84 sec                                                              | 4.96 sec: 1.29x slower                                |
| tornado_http               | 262 ms                                                                | 339 ms: 1.29x slower                                  |
| pycparser                  | 1.73 sec                                                              | 2.25 sec: 1.30x slower                                |
| meteor_contest             | 149 ms                                                                | 198 ms: 1.33x slower                                  |
| comprehensions             | 29.6 us                                                               | 39.9 us: 1.35x slower                                 |
| crypto_pyaes               | 112 ms                                                                | 152 ms: 1.36x slower                                  |
| python_startup             | 21.2 ms                                                               | 29.1 ms: 1.37x slower                                 |
| bench_thread_pool          | 3.11 ms                                                               | 4.26 ms: 1.37x slower                                 |
| coroutines                 | 30.1 ms                                                               | 41.7 ms: 1.38x slower                                 |
| json_dumps                 | 13.6 ms                                                               | 19.0 ms: 1.40x slower                                 |
| sympy_integrate            | 31.4 ms                                                               | 44.1 ms: 1.41x slower                                 |
| telco                      | 9.71 ms                                                               | 13.8 ms: 1.43x slower                                 |
| html5lib                   | 95.8 ms                                                               | 137 ms: 1.43x slower                                  |
| deepcopy_reduce            | 4.45 us                                                               | 6.40 us: 1.44x slower                                 |
| fannkuch                   | 551 ms                                                                | 792 ms: 1.44x slower                                  |
| tomli_loads                | 2.99 sec                                                              | 4.32 sec: 1.45x slower                                |
| nqueens                    | 110 ms                                                                | 161 ms: 1.47x slower                                  |
| xml_etree_process          | 85.7 ms                                                               | 127 ms: 1.48x slower                                  |
| thrift                     | 1.17 ms                                                               | 1.74 ms: 1.49x slower                                 |
| 2to3                       | 444 ms                                                                | 662 ms: 1.49x slower                                  |
| coverage                   | 97.6 ms                                                               | 148 ms: 1.51x slower                                  |
| logging_format             | 11.8 us                                                               | 17.9 us: 1.51x slower                                 |
| sqlglot_normalize          | 148 ms                                                                | 227 ms: 1.53x slower                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 10.2 sec: 1.54x slower                                |
| regex_compile              | 197 ms                                                                | 307 ms: 1.56x slower                                  |
| spectral_norm              | 158 ms                                                                | 246 ms: 1.56x slower                                  |
| sympy_str                  | 425 ms                                                                | 679 ms: 1.60x slower                                  |
| sqlglot_optimize           | 76.5 ms                                                               | 123 ms: 1.61x slower                                  |
| float                      | 127 ms                                                                | 211 ms: 1.66x slower                                  |
| scimark_monte_carlo        | 98.5 ms                                                               | 164 ms: 1.67x slower                                  |
| logging_simple             | 9.89 us                                                               | 16.5 us: 1.67x slower                                 |
| genshi_text                | 31.9 ms                                                               | 53.7 ms: 1.68x slower                                 |
| richards                   | 63.4 ms                                                               | 107 ms: 1.68x slower                                  |
| pyflate                    | 661 ms                                                                | 1.12 sec: 1.69x slower                                |
| genshi_xml                 | 73.6 ms                                                               | 125 ms: 1.70x slower                                  |
| unpickle_pure_python       | 319 us                                                                | 547 us: 1.71x slower                                  |
| pprint_pformat             | 2.03 sec                                                              | 3.52 sec: 1.74x slower                                |
| typing_runtime_protocols   | 199 us                                                                | 354 us: 1.77x slower                                  |
| django_template            | 48.6 ms                                                               | 86.4 ms: 1.78x slower                                 |
| pickle_pure_python         | 447 us                                                                | 801 us: 1.79x slower                                  |
| pprint_safe_repr           | 970 ms                                                                | 1.75 sec: 1.80x slower                                |
| mako                       | 17.2 ms                                                               | 31.1 ms: 1.81x slower                                 |
| hexiom                     | 8.87 ms                                                               | 16.1 ms: 1.82x slower                                 |
| sympy_expand               | 689 ms                                                                | 1.26 sec: 1.83x slower                                |
| chaos                      | 93.7 ms                                                               | 176 ms: 1.87x slower                                  |
| richards_super             | 67.9 ms                                                               | 127 ms: 1.88x slower                                  |
| raytrace                   | 418 ms                                                                | 803 ms: 1.92x slower                                  |
| logging_silent             | 135 ns                                                                | 266 ns: 1.97x slower                                  |
| sqlglot_transpile          | 2.28 ms                                                               | 4.52 ms: 1.98x slower                                 |
| scimark_lu                 | 155 ms                                                                | 315 ms: 2.04x slower                                  |
| scimark_sor                | 171 ms                                                                | 353 ms: 2.07x slower                                  |
| sympy_sum                  | 229 ms                                                                | 483 ms: 2.11x slower                                  |
| sqlglot_parse              | 1.89 ms                                                               | 4.03 ms: 2.13x slower                                 |
| nbody                      | 125 ms                                                                | 278 ms: 2.23x slower                                  |
| go                         | 185 ms                                                                | 420 ms: 2.27x slower                                  |
| deltablue                  | 5.05 ms                                                               | 11.8 ms: 2.33x slower                                 |
| unpack_sequence            | 68.5 ns                                                               | 194 ns: 2.83x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.35x slower                                          |

Benchmark hidden because not significant (4): pickle, pickle_dict, regex_dna, asyncio_websockets
Ignored benchmarks (8) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 2.27x