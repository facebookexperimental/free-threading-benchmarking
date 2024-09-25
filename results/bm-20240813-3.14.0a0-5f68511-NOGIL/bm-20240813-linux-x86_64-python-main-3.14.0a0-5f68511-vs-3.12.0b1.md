# Results vs. 3.12.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5f68511
- commit date: 2024-08-13
- overall geometric mean: 1.38x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 2.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 444 ms                                                                | 661 ms: 1.49x slower                                  |
| docutils       | 4.06 sec                                                              | 5.15 sec: 1.27x slower                                |
| html5lib       | 95.8 ms                                                               | 145 ms: 1.51x slower                                  |
| tornado_http   | 262 ms                                                                | 360 ms: 1.37x slower                                  |
| Geometric mean | (ref)                                                                 | 1.40x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.17 sec: 1.55x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 671 ms: 1.39x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.30 sec: 1.37x faster                                |
| async_tree_none_tg         | 692 ms                                                                | 521 ms: 1.33x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 849 ms: 1.29x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 787 ms: 1.21x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 945 ms: 1.20x faster                                  |
| async_tree_none            | 740 ms                                                                | 621 ms: 1.19x faster                                  |
| async_generators           | 617 ms                                                                | 744 ms: 1.21x slower                                  |
| asyncio_tcp                | 958 ms                                                                | 1.17 sec: 1.22x slower                                |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.55 sec: 1.27x slower                                |
| coroutines                 | 30.1 ms                                                               | 44.5 ms: 1.48x slower                                 |
| Geometric mean             | (ref)                                                                 | 1.09x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 255 ms                                                                | 242 ms: 1.05x faster                                  |
| float          | 127 ms                                                                | 206 ms: 1.62x slower                                  |
| nbody          | 125 ms                                                                | 293 ms: 2.35x slower                                  |
| Geometric mean | (ref)                                                                 | 1.54x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 4.97 ms                                                               | 4.62 ms: 1.08x faster                                 |
| regex_v8       | 31.1 ms                                                               | 36.7 ms: 1.18x slower                                 |
| regex_compile  | 197 ms                                                                | 290 ms: 1.47x slower                                  |
| Geometric mean | (ref)                                                                 | 1.13x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 6.40 us                                                               | 6.17 us: 1.04x faster                                 |
| xml_etree_iterparse  | 157 ms                                                                | 168 ms: 1.07x slower                                  |
| unpickle             | 19.7 us                                                               | 22.2 us: 1.12x slower                                 |
| unpickle_list        | 7.19 us                                                               | 8.50 us: 1.18x slower                                 |
| json_loads           | 36.6 us                                                               | 43.2 us: 1.18x slower                                 |
| xml_etree_generate   | 128 ms                                                                | 159 ms: 1.24x slower                                  |
| json_dumps           | 13.6 ms                                                               | 19.1 ms: 1.41x slower                                 |
| tomli_loads          | 2.99 sec                                                              | 4.26 sec: 1.43x slower                                |
| xml_etree_process    | 85.7 ms                                                               | 137 ms: 1.60x slower                                  |
| pickle_pure_python   | 447 us                                                                | 803 us: 1.80x slower                                  |
| unpickle_pure_python | 319 us                                                                | 619 us: 1.94x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.24x slower                                          |

Benchmark hidden because not significant (3): pickle_dict, xml_etree_parse, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.3 ms                                                               | 21.2 ms: 1.30x slower                                 |
| python_startup         | 21.2 ms                                                               | 31.5 ms: 1.48x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.39x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 73.6 ms                                                               | 117 ms: 1.58x slower                                  |
| genshi_text     | 31.9 ms                                                               | 55.9 ms: 1.75x slower                                 |
| django_template | 48.6 ms                                                               | 85.9 ms: 1.77x slower                                 |
| mako            | 17.2 ms                                                               | 32.0 ms: 1.86x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.74x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.80 sec                                                              | 1.17 sec: 1.55x faster                                |
| async_tree_memoization_tg  | 935 ms                                                                | 671 ms: 1.39x faster                                  |
| async_tree_io              | 1.79 sec                                                              | 1.30 sec: 1.37x faster                                |
| async_tree_none_tg         | 692 ms                                                                | 521 ms: 1.33x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                                              | 849 ms: 1.29x faster                                  |
| async_tree_memoization     | 949 ms                                                                | 787 ms: 1.21x faster                                  |
| async_tree_cpu_io_mixed    | 1.14 sec                                                              | 945 ms: 1.20x faster                                  |
| async_tree_none            | 740 ms                                                                | 621 ms: 1.19x faster                                  |
| regex_effbot               | 4.97 ms                                                               | 4.62 ms: 1.08x faster                                 |
| pidigits                   | 255 ms                                                                | 242 ms: 1.05x faster                                  |
| pickle_list                | 6.40 us                                                               | 6.17 us: 1.04x faster                                 |
| xml_etree_iterparse        | 157 ms                                                                | 168 ms: 1.07x slower                                  |
| pathlib                    | 31.7 ms                                                               | 34.5 ms: 1.09x slower                                 |
| unpickle                   | 19.7 us                                                               | 22.2 us: 1.12x slower                                 |
| deepcopy                   | 503 us                                                                | 571 us: 1.13x slower                                  |
| sqlite_synth               | 3.75 us                                                               | 4.38 us: 1.17x slower                                 |
| pylint                     | 501 ms                                                                | 588 ms: 1.17x slower                                  |
| regex_v8                   | 31.1 ms                                                               | 36.7 ms: 1.18x slower                                 |
| unpickle_list              | 7.19 us                                                               | 8.50 us: 1.18x slower                                 |
| json_loads                 | 36.6 us                                                               | 43.2 us: 1.18x slower                                 |
| async_generators           | 617 ms                                                                | 744 ms: 1.21x slower                                  |
| asyncio_tcp                | 958 ms                                                                | 1.17 sec: 1.22x slower                                |
| xml_etree_generate         | 128 ms                                                                | 159 ms: 1.24x slower                                  |
| scimark_fft                | 499 ms                                                                | 628 ms: 1.26x slower                                  |
| pycparser                  | 1.73 sec                                                              | 2.18 sec: 1.26x slower                                |
| generators                 | 46.0 ms                                                               | 58.3 ms: 1.27x slower                                 |
| deepcopy_memo              | 57.5 us                                                               | 72.7 us: 1.27x slower                                 |
| docutils                   | 4.06 sec                                                              | 5.15 sec: 1.27x slower                                |
| asyncio_tcp_ssl            | 2.80 sec                                                              | 3.55 sec: 1.27x slower                                |
| json                       | 6.68 ms                                                               | 8.55 ms: 1.28x slower                                 |
| scimark_sparse_mat_mult    | 7.47 ms                                                               | 9.62 ms: 1.29x slower                                 |
| python_startup_no_site     | 16.3 ms                                                               | 21.2 ms: 1.30x slower                                 |
| mdp                        | 3.84 sec                                                              | 5.24 sec: 1.36x slower                                |
| comprehensions             | 29.6 us                                                               | 40.4 us: 1.37x slower                                 |
| tornado_http               | 262 ms                                                                | 360 ms: 1.37x slower                                  |
| deepcopy_reduce            | 4.45 us                                                               | 6.14 us: 1.38x slower                                 |
| crypto_pyaes               | 112 ms                                                                | 157 ms: 1.40x slower                                  |
| json_dumps                 | 13.6 ms                                                               | 19.1 ms: 1.41x slower                                 |
| meteor_contest             | 149 ms                                                                | 210 ms: 1.41x slower                                  |
| tomli_loads                | 2.99 sec                                                              | 4.26 sec: 1.43x slower                                |
| fannkuch                   | 551 ms                                                                | 804 ms: 1.46x slower                                  |
| thrift                     | 1.17 ms                                                               | 1.72 ms: 1.47x slower                                 |
| regex_compile              | 197 ms                                                                | 290 ms: 1.47x slower                                  |
| coroutines                 | 30.1 ms                                                               | 44.5 ms: 1.48x slower                                 |
| python_startup             | 21.2 ms                                                               | 31.5 ms: 1.48x slower                                 |
| logging_format             | 11.8 us                                                               | 17.5 us: 1.48x slower                                 |
| 2to3                       | 444 ms                                                                | 661 ms: 1.49x slower                                  |
| coverage                   | 97.6 ms                                                               | 146 ms: 1.49x slower                                  |
| html5lib                   | 95.8 ms                                                               | 145 ms: 1.51x slower                                  |
| telco                      | 9.71 ms                                                               | 14.8 ms: 1.52x slower                                 |
| logging_simple             | 9.89 us                                                               | 15.2 us: 1.54x slower                                 |
| nqueens                    | 110 ms                                                                | 170 ms: 1.55x slower                                  |
| bench_thread_pool          | 3.11 ms                                                               | 4.83 ms: 1.55x slower                                 |
| sqlglot_normalize          | 148 ms                                                                | 231 ms: 1.56x slower                                  |
| genshi_xml                 | 73.6 ms                                                               | 117 ms: 1.58x slower                                  |
| bpe_tokeniser              | 6.63 sec                                                              | 10.6 sec: 1.59x slower                                |
| xml_etree_process          | 85.7 ms                                                               | 137 ms: 1.60x slower                                  |
| sqlglot_optimize           | 76.5 ms                                                               | 124 ms: 1.62x slower                                  |
| float                      | 127 ms                                                                | 206 ms: 1.62x slower                                  |
| spectral_norm              | 158 ms                                                                | 258 ms: 1.64x slower                                  |
| sympy_integrate            | 31.4 ms                                                               | 51.8 ms: 1.65x slower                                 |
| sympy_str                  | 425 ms                                                                | 709 ms: 1.67x slower                                  |
| richards                   | 63.4 ms                                                               | 106 ms: 1.67x slower                                  |
| pyflate                    | 661 ms                                                                | 1.13 sec: 1.70x slower                                |
| pprint_pformat             | 2.03 sec                                                              | 3.54 sec: 1.74x slower                                |
| genshi_text                | 31.9 ms                                                               | 55.9 ms: 1.75x slower                                 |
| typing_runtime_protocols   | 199 us                                                                | 350 us: 1.75x slower                                  |
| pprint_safe_repr           | 970 ms                                                                | 1.71 sec: 1.76x slower                                |
| scimark_monte_carlo        | 98.5 ms                                                               | 174 ms: 1.77x slower                                  |
| django_template            | 48.6 ms                                                               | 85.9 ms: 1.77x slower                                 |
| pickle_pure_python         | 447 us                                                                | 803 us: 1.80x slower                                  |
| mako                       | 17.2 ms                                                               | 32.0 ms: 1.86x slower                                 |
| chaos                      | 93.7 ms                                                               | 177 ms: 1.89x slower                                  |
| hexiom                     | 8.87 ms                                                               | 16.8 ms: 1.89x slower                                 |
| sympy_expand               | 689 ms                                                                | 1.30 sec: 1.89x slower                                |
| sqlglot_transpile          | 2.28 ms                                                               | 4.33 ms: 1.90x slower                                 |
| raytrace                   | 418 ms                                                                | 804 ms: 1.92x slower                                  |
| richards_super             | 67.9 ms                                                               | 131 ms: 1.93x slower                                  |
| logging_silent             | 135 ns                                                                | 262 ns: 1.94x slower                                  |
| unpickle_pure_python       | 319 us                                                                | 619 us: 1.94x slower                                  |
| scimark_lu                 | 155 ms                                                                | 305 ms: 1.97x slower                                  |
| sqlglot_parse              | 1.89 ms                                                               | 3.84 ms: 2.03x slower                                 |
| sympy_sum                  | 229 ms                                                                | 479 ms: 2.09x slower                                  |
| scimark_sor                | 171 ms                                                                | 368 ms: 2.15x slower                                  |
| nbody                      | 125 ms                                                                | 293 ms: 2.35x slower                                  |
| deltablue                  | 5.05 ms                                                               | 12.0 ms: 2.38x slower                                 |
| go                         | 185 ms                                                                | 465 ms: 2.51x slower                                  |
| unpack_sequence            | 68.5 ns                                                               | 180 ns: 2.63x slower                                  |
| Geometric mean             | (ref)                                                                 | 1.38x slower                                          |

Benchmark hidden because not significant (8): bench_mp_pool, gc_traversal, pickle_dict, xml_etree_parse, pickle, create_gc_cycles, regex_dna, asyncio_websockets
Ignored benchmarks (9) of results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 2.24x