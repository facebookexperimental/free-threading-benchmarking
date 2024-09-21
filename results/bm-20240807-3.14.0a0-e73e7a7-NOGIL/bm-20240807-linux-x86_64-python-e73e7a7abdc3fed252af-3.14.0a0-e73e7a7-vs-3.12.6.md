# Results vs. 3.12.6

- fork: python
- ref: e73e7a7abdc3fed252af
- machine: linux-x86_64
- commit hash: e73e7a7
- commit date: 2024-08-07
- overall geometric mean: 1.35x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 651 ms: 1.43x slower                                                  |
| docutils       | 4.00 sec                                               | 4.92 sec: 1.23x slower                                                |
| html5lib       | 88.9 ms                                                | 137 ms: 1.54x slower                                                  |
| tornado_http   | 266 ms                                                 | 319 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                  | 1.34x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.12 sec: 1.73x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 619 ms: 1.50x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.25 sec: 1.48x faster                                                |
| async_tree_none_tg         | 704 ms                                                 | 489 ms: 1.44x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 724 ms: 1.35x faster                                                  |
| async_tree_none            | 741 ms                                                 | 584 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 874 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 951 ms: 1.13x faster                                                  |
| asyncio_tcp                | 923 ms                                                 | 1.09 sec: 1.18x slower                                                |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.34 sec: 1.19x slower                                                |
| async_generators           | 589 ms                                                 | 747 ms: 1.27x slower                                                  |
| coroutines                 | 29.5 ms                                                | 42.7 ms: 1.45x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.13x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 239 ms: 1.04x faster                                                  |
| float          | 123 ms                                                 | 194 ms: 1.58x slower                                                  |
| nbody          | 119 ms                                                 | 281 ms: 2.36x slower                                                  |
| Geometric mean | (ref)                                                  | 1.53x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.84 ms: 1.06x faster                                                 |
| regex_dna      | 278 ms                                                 | 290 ms: 1.04x slower                                                  |
| regex_v8       | 32.5 ms                                                | 35.6 ms: 1.10x slower                                                 |
| regex_compile  | 187 ms                                                 | 296 ms: 1.59x slower                                                  |
| Geometric mean | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 43.1 us: 1.22x faster                                                 |
| pickle               | 16.4 us                                                | 14.5 us: 1.13x faster                                                 |
| xml_etree_parse      | 241 ms                                                 | 218 ms: 1.11x faster                                                  |
| json_loads           | 37.9 us                                                | 41.2 us: 1.09x slower                                                 |
| unpickle_list        | 6.83 us                                                | 7.70 us: 1.13x slower                                                 |
| xml_etree_generate   | 127 ms                                                 | 159 ms: 1.25x slower                                                  |
| json_dumps           | 14.3 ms                                                | 18.0 ms: 1.26x slower                                                 |
| tomli_loads          | 2.88 sec                                               | 4.14 sec: 1.44x slower                                                |
| xml_etree_process    | 83.7 ms                                                | 127 ms: 1.52x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 544 us: 1.82x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 846 us: 1.94x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.18x slower                                                          |

Benchmark hidden because not significant (3): pickle_list, xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.4 ms: 1.10x slower                                                 |
| python_startup         | 23.7 ms                                                | 28.9 ms: 1.22x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 111 ms: 1.64x slower                                                  |
| genshi_text     | 30.2 ms                                                | 53.4 ms: 1.77x slower                                                 |
| django_template | 44.9 ms                                                | 79.6 ms: 1.77x slower                                                 |
| mako            | 15.7 ms                                                | 31.0 ms: 1.97x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.78x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.12 sec: 1.73x faster                                                |
| async_tree_memoization_tg  | 930 ms                                                 | 619 ms: 1.50x faster                                                  |
| async_tree_io              | 1.85 sec                                               | 1.25 sec: 1.48x faster                                                |
| async_tree_none_tg         | 704 ms                                                 | 489 ms: 1.44x faster                                                  |
| gc_traversal               | 5.86 ms                                                | 4.19 ms: 1.40x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 724 ms: 1.35x faster                                                  |
| async_tree_none            | 741 ms                                                 | 584 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 874 ms: 1.26x faster                                                  |
| pickle_dict                | 52.7 us                                                | 43.1 us: 1.22x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 951 ms: 1.13x faster                                                  |
| pickle                     | 16.4 us                                                | 14.5 us: 1.13x faster                                                 |
| xml_etree_parse            | 241 ms                                                 | 218 ms: 1.11x faster                                                  |
| create_gc_cycles           | 1.94 ms                                                | 1.80 ms: 1.08x faster                                                 |
| regex_effbot               | 5.13 ms                                                | 4.84 ms: 1.06x faster                                                 |
| pidigits                   | 250 ms                                                 | 239 ms: 1.04x faster                                                  |
| regex_dna                  | 278 ms                                                 | 290 ms: 1.04x slower                                                  |
| json_loads                 | 37.9 us                                                | 41.2 us: 1.09x slower                                                 |
| regex_v8                   | 32.5 ms                                                | 35.6 ms: 1.10x slower                                                 |
| python_startup_no_site     | 17.6 ms                                                | 19.4 ms: 1.10x slower                                                 |
| unpickle_list              | 6.83 us                                                | 7.70 us: 1.13x slower                                                 |
| sqlite_synth               | 3.87 us                                                | 4.42 us: 1.14x slower                                                 |
| asyncio_tcp                | 923 ms                                                 | 1.09 sec: 1.18x slower                                                |
| json                       | 6.85 ms                                                | 8.10 ms: 1.18x slower                                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.34 sec: 1.19x slower                                                |
| deepcopy                   | 468 us                                                 | 560 us: 1.20x slower                                                  |
| tornado_http               | 266 ms                                                 | 319 ms: 1.20x slower                                                  |
| python_startup             | 23.7 ms                                                | 28.9 ms: 1.22x slower                                                 |
| docutils                   | 4.00 sec                                               | 4.92 sec: 1.23x slower                                                |
| pycparser                  | 1.79 sec                                               | 2.21 sec: 1.24x slower                                                |
| pylint                     | 465 ms                                                 | 579 ms: 1.25x slower                                                  |
| scimark_fft                | 500 ms                                                 | 624 ms: 1.25x slower                                                  |
| xml_etree_generate         | 127 ms                                                 | 159 ms: 1.25x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 18.0 ms: 1.26x slower                                                 |
| async_generators           | 589 ms                                                 | 747 ms: 1.27x slower                                                  |
| deepcopy_memo              | 52.4 us                                                | 67.1 us: 1.28x slower                                                 |
| mdp                        | 3.97 sec                                               | 5.13 sec: 1.29x slower                                                |
| bench_thread_pool          | 3.48 ms                                                | 4.52 ms: 1.30x slower                                                 |
| meteor_contest             | 146 ms                                                 | 192 ms: 1.31x slower                                                  |
| nqueens                    | 117 ms                                                 | 155 ms: 1.33x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.91 ms: 1.33x slower                                                 |
| generators                 | 41.1 ms                                                | 55.0 ms: 1.34x slower                                                 |
| fannkuch                   | 540 ms                                                 | 762 ms: 1.41x slower                                                  |
| deepcopy_reduce            | 4.04 us                                                | 5.70 us: 1.41x slower                                                 |
| 2to3                       | 456 ms                                                 | 651 ms: 1.43x slower                                                  |
| comprehensions             | 27.1 us                                                | 38.7 us: 1.43x slower                                                 |
| tomli_loads                | 2.88 sec                                               | 4.14 sec: 1.44x slower                                                |
| coroutines                 | 29.5 ms                                                | 42.7 ms: 1.45x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 156 ms: 1.45x slower                                                  |
| sqlglot_normalize          | 157 ms                                                 | 229 ms: 1.46x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 327 us: 1.46x slower                                                  |
| telco                      | 9.59 ms                                                | 14.0 ms: 1.46x slower                                                 |
| pyflate                    | 727 ms                                                 | 1.07 sec: 1.47x slower                                                |
| sympy_integrate            | 29.8 ms                                                | 44.9 ms: 1.51x slower                                                 |
| xml_etree_process          | 83.7 ms                                                | 127 ms: 1.52x slower                                                  |
| coverage                   | 95.4 ms                                                | 146 ms: 1.53x slower                                                  |
| html5lib                   | 88.9 ms                                                | 137 ms: 1.54x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 10.1 sec: 1.54x slower                                                |
| float                      | 123 ms                                                 | 194 ms: 1.58x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.67 ms: 1.58x slower                                                 |
| regex_compile              | 187 ms                                                 | 296 ms: 1.59x slower                                                  |
| spectral_norm              | 156 ms                                                 | 247 ms: 1.59x slower                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 121 ms: 1.59x slower                                                  |
| logging_simple             | 9.45 us                                                | 15.4 us: 1.63x slower                                                 |
| richards                   | 60.3 ms                                                | 99.2 ms: 1.64x slower                                                 |
| genshi_xml                 | 67.6 ms                                                | 111 ms: 1.64x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 159 ms: 1.65x slower                                                  |
| logging_format             | 9.59 us                                                | 16.4 us: 1.71x slower                                                 |
| pprint_safe_repr           | 967 ms                                                 | 1.65 sec: 1.71x slower                                                |
| pprint_pformat             | 1.98 sec                                               | 3.39 sec: 1.71x slower                                                |
| richards_super             | 72.8 ms                                                | 127 ms: 1.74x slower                                                  |
| sympy_str                  | 385 ms                                                 | 675 ms: 1.75x slower                                                  |
| genshi_text                | 30.2 ms                                                | 53.4 ms: 1.77x slower                                                 |
| django_template            | 44.9 ms                                                | 79.6 ms: 1.77x slower                                                 |
| logging_silent             | 139 ns                                                 | 249 ns: 1.79x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 544 us: 1.82x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 4.32 ms: 1.85x slower                                                 |
| pickle_pure_python         | 436 us                                                 | 846 us: 1.94x slower                                                  |
| raytrace                   | 408 ms                                                 | 801 ms: 1.97x slower                                                  |
| mako                       | 15.7 ms                                                | 31.0 ms: 1.97x slower                                                 |
| hexiom                     | 8.27 ms                                                | 16.3 ms: 1.97x slower                                                 |
| sympy_sum                  | 222 ms                                                 | 443 ms: 2.00x slower                                                  |
| chaos                      | 84.9 ms                                                | 170 ms: 2.00x slower                                                  |
| scimark_sor                | 167 ms                                                 | 340 ms: 2.04x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 313 ms: 2.06x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.76 ms: 2.10x slower                                                 |
| sympy_expand               | 582 ms                                                 | 1.29 sec: 2.21x slower                                                |
| nbody                      | 119 ms                                                 | 281 ms: 2.36x slower                                                  |
| go                         | 172 ms                                                 | 434 ms: 2.52x slower                                                  |
| deltablue                  | 4.27 ms                                                | 11.6 ms: 2.71x slower                                                 |
| unpack_sequence            | 60.2 ns                                                | 190 ns: 3.16x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.35x slower                                                          |

Benchmark hidden because not significant (6): bench_mp_pool, pickle_list, xml_etree_iterparse, asyncio_websockets, pathlib, unpickle
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.15x