# Results vs. 3.12.6

- fork: python
- ref: a15feded71dd47202db1
- machine: linux-x86_64
- commit hash: a15fede
- commit date: 2024-07-23
- overall geometric mean: 1.37x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 650 ms: 1.42x slower                                                  |
| docutils       | 4.00 sec                                               | 4.88 sec: 1.22x slower                                                |
| html5lib       | 88.9 ms                                                | 139 ms: 1.57x slower                                                  |
| tornado_http   | 266 ms                                                 | 349 ms: 1.31x slower                                                  |
| Geometric mean | (ref)                                                  | 1.38x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.16 sec: 1.66x faster                                                |
| async_tree_none_tg         | 704 ms                                                 | 485 ms: 1.45x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.30 sec: 1.42x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 671 ms: 1.39x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 721 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 817 ms: 1.35x faster                                                  |
| async_tree_none            | 741 ms                                                 | 588 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 944 ms: 1.14x faster                                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.36 sec: 1.20x slower                                                |
| asyncio_tcp                | 923 ms                                                 | 1.12 sec: 1.21x slower                                                |
| async_generators           | 589 ms                                                 | 739 ms: 1.25x slower                                                  |
| coroutines                 | 29.5 ms                                                | 43.2 ms: 1.46x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.13x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 243 ms: 1.03x faster                                                  |
| float          | 123 ms                                                 | 202 ms: 1.64x slower                                                  |
| nbody          | 119 ms                                                 | 288 ms: 2.41x slower                                                  |
| Geometric mean | (ref)                                                  | 1.57x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.57 ms: 1.12x faster                                                 |
| regex_dna      | 278 ms                                                 | 294 ms: 1.06x slower                                                  |
| regex_v8       | 32.5 ms                                                | 36.3 ms: 1.12x slower                                                 |
| regex_compile  | 187 ms                                                 | 291 ms: 1.56x slower                                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 42.5 us: 1.24x faster                                                 |
| pickle               | 16.4 us                                                | 14.5 us: 1.13x faster                                                 |
| pickle_list          | 6.97 us                                                | 6.30 us: 1.11x faster                                                 |
| json_loads           | 37.9 us                                                | 42.7 us: 1.13x slower                                                 |
| unpickle_list        | 6.83 us                                                | 8.14 us: 1.19x slower                                                 |
| xml_etree_generate   | 127 ms                                                 | 162 ms: 1.28x slower                                                  |
| json_dumps           | 14.3 ms                                                | 19.0 ms: 1.33x slower                                                 |
| tomli_loads          | 2.88 sec                                               | 4.22 sec: 1.46x slower                                                |
| xml_etree_process    | 83.7 ms                                                | 127 ms: 1.51x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 805 us: 1.85x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 609 us: 2.03x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.20x slower                                                          |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.6 ms: 1.17x slower                                                 |
| python_startup         | 23.7 ms                                                | 29.7 ms: 1.25x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 116 ms: 1.71x slower                                                  |
| django_template | 44.9 ms                                                | 80.4 ms: 1.79x slower                                                 |
| genshi_text     | 30.2 ms                                                | 54.9 ms: 1.82x slower                                                 |
| mako            | 15.7 ms                                                | 30.4 ms: 1.93x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.81x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-a15feded71dd47202db1-3.14.0a0-a15fede |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.16 sec: 1.66x faster                                                |
| bench_mp_pool              | 20.7 ms                                                | 13.4 ms: 1.54x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 485 ms: 1.45x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.30 sec: 1.42x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 671 ms: 1.39x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 721 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 817 ms: 1.35x faster                                                  |
| async_tree_none            | 741 ms                                                 | 588 ms: 1.26x faster                                                  |
| pickle_dict                | 52.7 us                                                | 42.5 us: 1.24x faster                                                 |
| gc_traversal               | 5.86 ms                                                | 4.76 ms: 1.23x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 944 ms: 1.14x faster                                                  |
| pickle                     | 16.4 us                                                | 14.5 us: 1.13x faster                                                 |
| regex_effbot               | 5.13 ms                                                | 4.57 ms: 1.12x faster                                                 |
| pickle_list                | 6.97 us                                                | 6.30 us: 1.11x faster                                                 |
| pidigits                   | 250 ms                                                 | 243 ms: 1.03x faster                                                  |
| regex_dna                  | 278 ms                                                 | 294 ms: 1.06x slower                                                  |
| pathlib                    | 31.6 ms                                                | 34.8 ms: 1.10x slower                                                 |
| regex_v8                   | 32.5 ms                                                | 36.3 ms: 1.12x slower                                                 |
| sqlite_synth               | 3.87 us                                                | 4.35 us: 1.12x slower                                                 |
| json_loads                 | 37.9 us                                                | 42.7 us: 1.13x slower                                                 |
| bench_thread_pool          | 3.48 ms                                                | 4.01 ms: 1.15x slower                                                 |
| json                       | 6.85 ms                                                | 7.98 ms: 1.17x slower                                                 |
| python_startup_no_site     | 17.6 ms                                                | 20.6 ms: 1.17x slower                                                 |
| unpickle_list              | 6.83 us                                                | 8.14 us: 1.19x slower                                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.36 sec: 1.20x slower                                                |
| asyncio_tcp                | 923 ms                                                 | 1.12 sec: 1.21x slower                                                |
| docutils                   | 4.00 sec                                               | 4.88 sec: 1.22x slower                                                |
| python_startup             | 23.7 ms                                                | 29.7 ms: 1.25x slower                                                 |
| async_generators           | 589 ms                                                 | 739 ms: 1.25x slower                                                  |
| scimark_fft                | 500 ms                                                 | 633 ms: 1.27x slower                                                  |
| pycparser                  | 1.79 sec                                               | 2.28 sec: 1.27x slower                                                |
| xml_etree_generate         | 127 ms                                                 | 162 ms: 1.28x slower                                                  |
| mdp                        | 3.97 sec                                               | 5.14 sec: 1.29x slower                                                |
| deepcopy                   | 468 us                                                 | 606 us: 1.29x slower                                                  |
| pylint                     | 465 ms                                                 | 607 ms: 1.31x slower                                                  |
| tornado_http               | 266 ms                                                 | 349 ms: 1.31x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.89 ms: 1.33x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 19.0 ms: 1.33x slower                                                 |
| meteor_contest             | 146 ms                                                 | 196 ms: 1.34x slower                                                  |
| nqueens                    | 117 ms                                                 | 157 ms: 1.35x slower                                                  |
| telco                      | 9.59 ms                                                | 13.2 ms: 1.38x slower                                                 |
| deepcopy_memo              | 52.4 us                                                | 72.8 us: 1.39x slower                                                 |
| generators                 | 41.1 ms                                                | 58.0 ms: 1.41x slower                                                 |
| 2to3                       | 456 ms                                                 | 650 ms: 1.42x slower                                                  |
| crypto_pyaes               | 107 ms                                                 | 155 ms: 1.44x slower                                                  |
| comprehensions             | 27.1 us                                                | 39.2 us: 1.45x slower                                                 |
| sympy_integrate            | 29.8 ms                                                | 43.3 ms: 1.45x slower                                                 |
| dulwich_log                | 100 ms                                                 | 146 ms: 1.46x slower                                                  |
| coroutines                 | 29.5 ms                                                | 43.2 ms: 1.46x slower                                                 |
| tomli_loads                | 2.88 sec                                               | 4.22 sec: 1.46x slower                                                |
| deepcopy_reduce            | 4.04 us                                                | 6.01 us: 1.49x slower                                                 |
| fannkuch                   | 540 ms                                                 | 808 ms: 1.49x slower                                                  |
| sqlglot_normalize          | 157 ms                                                 | 238 ms: 1.51x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 127 ms: 1.51x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 339 us: 1.51x slower                                                  |
| pyflate                    | 727 ms                                                 | 1.13 sec: 1.55x slower                                                |
| regex_compile              | 187 ms                                                 | 291 ms: 1.56x slower                                                  |
| html5lib                   | 88.9 ms                                                | 139 ms: 1.57x slower                                                  |
| coverage                   | 95.4 ms                                                | 150 ms: 1.57x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 10.3 sec: 1.57x slower                                                |
| spectral_norm              | 156 ms                                                 | 246 ms: 1.58x slower                                                  |
| logging_simple             | 9.45 us                                                | 15.3 us: 1.62x slower                                                 |
| float                      | 123 ms                                                 | 202 ms: 1.64x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.74 ms: 1.64x slower                                                 |
| sqlglot_optimize           | 76.0 ms                                                | 128 ms: 1.68x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 116 ms: 1.71x slower                                                  |
| sympy_str                  | 385 ms                                                 | 667 ms: 1.73x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.71 sec: 1.76x slower                                                |
| scimark_monte_carlo        | 96.4 ms                                                | 171 ms: 1.78x slower                                                  |
| django_template            | 44.9 ms                                                | 80.4 ms: 1.79x slower                                                 |
| logging_silent             | 139 ns                                                 | 251 ns: 1.80x slower                                                  |
| logging_format             | 9.59 us                                                | 17.3 us: 1.80x slower                                                 |
| pprint_pformat             | 1.98 sec                                               | 3.58 sec: 1.81x slower                                                |
| genshi_text                | 30.2 ms                                                | 54.9 ms: 1.82x slower                                                 |
| pickle_pure_python         | 436 us                                                 | 805 us: 1.85x slower                                                  |
| richards_super             | 72.8 ms                                                | 136 ms: 1.87x slower                                                  |
| richards                   | 60.3 ms                                                | 115 ms: 1.91x slower                                                  |
| mako                       | 15.7 ms                                                | 30.4 ms: 1.93x slower                                                 |
| hexiom                     | 8.27 ms                                                | 16.2 ms: 1.95x slower                                                 |
| raytrace                   | 408 ms                                                 | 802 ms: 1.97x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 609 us: 2.03x slower                                                  |
| scimark_sor                | 167 ms                                                 | 341 ms: 2.05x slower                                                  |
| chaos                      | 84.9 ms                                                | 175 ms: 2.06x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 4.92 ms: 2.10x slower                                                 |
| sympy_sum                  | 222 ms                                                 | 477 ms: 2.15x slower                                                  |
| sympy_expand               | 582 ms                                                 | 1.25 sec: 2.16x slower                                                |
| scimark_lu                 | 152 ms                                                 | 332 ms: 2.18x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.96 ms: 2.22x slower                                                 |
| nbody                      | 119 ms                                                 | 288 ms: 2.41x slower                                                  |
| go                         | 172 ms                                                 | 421 ms: 2.45x slower                                                  |
| deltablue                  | 4.27 ms                                                | 11.7 ms: 2.73x slower                                                 |
| unpack_sequence            | 60.2 ns                                                | 210 ns: 3.48x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.37x slower                                                          |

Benchmark hidden because not significant (5): xml_etree_parse, xml_etree_iterparse, create_gc_cycles, asyncio_websockets, unpickle
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.32x
- 95% likely to have a slowdown of 1.29x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.16x