# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a9bb3c7
- commit date: 2024-07-23
- overall geometric mean: 1.32x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                                 | 661 ms: 1.45x slower                                  |
| docutils       | 4.00 sec                                               | 4.69 sec: 1.17x slower                                |
| html5lib       | 88.9 ms                                                | 135 ms: 1.52x slower                                  |
| tornado_http   | 266 ms                                                 | 320 ms: 1.20x slower                                  |
| Geometric mean | (ref)                                                  | 1.33x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.15 sec: 1.68x faster                                |
| async_tree_io              | 1.85 sec                                               | 1.25 sec: 1.48x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 632 ms: 1.47x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 479 ms: 1.47x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 806 ms: 1.37x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 728 ms: 1.34x faster                                  |
| async_tree_none            | 741 ms                                                 | 578 ms: 1.28x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 926 ms: 1.16x faster                                  |
| asyncio_websockets         | 748 ms                                                 | 714 ms: 1.05x faster                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.12 sec: 1.11x slower                                |
| asyncio_tcp                | 923 ms                                                 | 1.05 sec: 1.13x slower                                |
| async_generators           | 589 ms                                                 | 739 ms: 1.26x slower                                  |
| coroutines                 | 29.5 ms                                                | 40.7 ms: 1.38x slower                                 |
| Geometric mean             | (ref)                                                  | 1.16x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 250 ms                                                 | 241 ms: 1.04x faster                                  |
| float          | 123 ms                                                 | 199 ms: 1.62x slower                                  |
| nbody          | 119 ms                                                 | 284 ms: 2.38x slower                                  |
| Geometric mean | (ref)                                                  | 1.55x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.60 ms: 1.12x faster                                 |
| regex_v8       | 32.5 ms                                                | 35.5 ms: 1.09x slower                                 |
| regex_compile  | 187 ms                                                 | 287 ms: 1.54x slower                                  |
| Geometric mean | (ref)                                                  | 1.11x slower                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 40.4 us: 1.31x faster                                 |
| xml_etree_parse      | 241 ms                                                 | 203 ms: 1.19x faster                                  |
| pickle               | 16.4 us                                                | 14.4 us: 1.14x faster                                 |
| xml_etree_iterparse  | 169 ms                                                 | 152 ms: 1.12x faster                                  |
| pickle_list          | 6.97 us                                                | 6.56 us: 1.06x faster                                 |
| unpickle_list        | 6.83 us                                                | 7.37 us: 1.08x slower                                 |
| json_loads           | 37.9 us                                                | 41.9 us: 1.11x slower                                 |
| xml_etree_generate   | 127 ms                                                 | 160 ms: 1.26x slower                                  |
| json_dumps           | 14.3 ms                                                | 18.2 ms: 1.27x slower                                 |
| xml_etree_process    | 83.7 ms                                                | 119 ms: 1.42x slower                                  |
| tomli_loads          | 2.88 sec                                               | 4.17 sec: 1.45x slower                                |
| unpickle_pure_python | 300 us                                                 | 526 us: 1.75x slower                                  |
| pickle_pure_python   | 436 us                                                 | 792 us: 1.82x slower                                  |
| Geometric mean       | (ref)                                                  | 1.14x slower                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 18.6 ms: 1.06x slower                                 |
| python_startup         | 23.7 ms                                                | 27.3 ms: 1.15x slower                                 |
| Geometric mean         | (ref)                                                  | 1.10x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 117 ms: 1.72x slower                                  |
| django_template | 44.9 ms                                                | 80.7 ms: 1.79x slower                                 |
| genshi_text     | 30.2 ms                                                | 54.8 ms: 1.81x slower                                 |
| mako            | 15.7 ms                                                | 29.7 ms: 1.89x slower                                 |
| Geometric mean  | (ref)                                                  | 1.80x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| bench_mp_pool              | 20.7 ms                                                | 12.0 ms: 1.73x faster                                 |
| async_tree_io_tg           | 1.93 sec                                               | 1.15 sec: 1.68x faster                                |
| async_tree_io              | 1.85 sec                                               | 1.25 sec: 1.48x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 632 ms: 1.47x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 479 ms: 1.47x faster                                  |
| gc_traversal               | 5.86 ms                                                | 4.22 ms: 1.39x faster                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 806 ms: 1.37x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 728 ms: 1.34x faster                                  |
| pickle_dict                | 52.7 us                                                | 40.4 us: 1.31x faster                                 |
| async_tree_none            | 741 ms                                                 | 578 ms: 1.28x faster                                  |
| xml_etree_parse            | 241 ms                                                 | 203 ms: 1.19x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 926 ms: 1.16x faster                                  |
| pickle                     | 16.4 us                                                | 14.4 us: 1.14x faster                                 |
| xml_etree_iterparse        | 169 ms                                                 | 152 ms: 1.12x faster                                  |
| regex_effbot               | 5.13 ms                                                | 4.60 ms: 1.12x faster                                 |
| create_gc_cycles           | 1.94 ms                                                | 1.77 ms: 1.10x faster                                 |
| pickle_list                | 6.97 us                                                | 6.56 us: 1.06x faster                                 |
| asyncio_websockets         | 748 ms                                                 | 714 ms: 1.05x faster                                  |
| pidigits                   | 250 ms                                                 | 241 ms: 1.04x faster                                  |
| python_startup_no_site     | 17.6 ms                                                | 18.6 ms: 1.06x slower                                 |
| unpickle_list              | 6.83 us                                                | 7.37 us: 1.08x slower                                 |
| regex_v8                   | 32.5 ms                                                | 35.5 ms: 1.09x slower                                 |
| json_loads                 | 37.9 us                                                | 41.9 us: 1.11x slower                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.12 sec: 1.11x slower                                |
| sqlite_synth               | 3.87 us                                                | 4.31 us: 1.11x slower                                 |
| asyncio_tcp                | 923 ms                                                 | 1.05 sec: 1.13x slower                                |
| python_startup             | 23.7 ms                                                | 27.3 ms: 1.15x slower                                 |
| docutils                   | 4.00 sec                                               | 4.69 sec: 1.17x slower                                |
| json                       | 6.85 ms                                                | 8.04 ms: 1.17x slower                                 |
| pylint                     | 465 ms                                                 | 554 ms: 1.19x slower                                  |
| pycparser                  | 1.79 sec                                               | 2.15 sec: 1.20x slower                                |
| tornado_http               | 266 ms                                                 | 320 ms: 1.20x slower                                  |
| scimark_fft                | 500 ms                                                 | 616 ms: 1.23x slower                                  |
| async_generators           | 589 ms                                                 | 739 ms: 1.26x slower                                  |
| xml_etree_generate         | 127 ms                                                 | 160 ms: 1.26x slower                                  |
| json_dumps                 | 14.3 ms                                                | 18.2 ms: 1.27x slower                                 |
| mdp                        | 3.97 sec                                               | 5.07 sec: 1.28x slower                                |
| generators                 | 41.1 ms                                                | 52.7 ms: 1.28x slower                                 |
| deepcopy                   | 468 us                                                 | 608 us: 1.30x slower                                  |
| nqueens                    | 117 ms                                                 | 153 ms: 1.31x slower                                  |
| deepcopy_memo              | 52.4 us                                                | 69.3 us: 1.32x slower                                 |
| meteor_contest             | 146 ms                                                 | 196 ms: 1.34x slower                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 9.03 ms: 1.35x slower                                 |
| dulwich_log                | 100 ms                                                 | 135 ms: 1.35x slower                                  |
| telco                      | 9.59 ms                                                | 13.2 ms: 1.37x slower                                 |
| coroutines                 | 29.5 ms                                                | 40.7 ms: 1.38x slower                                 |
| crypto_pyaes               | 107 ms                                                 | 150 ms: 1.40x slower                                  |
| xml_etree_process          | 83.7 ms                                                | 119 ms: 1.42x slower                                  |
| tomli_loads                | 2.88 sec                                               | 4.17 sec: 1.45x slower                                |
| 2to3                       | 456 ms                                                 | 661 ms: 1.45x slower                                  |
| sympy_integrate            | 29.8 ms                                                | 43.4 ms: 1.46x slower                                 |
| fannkuch                   | 540 ms                                                 | 794 ms: 1.47x slower                                  |
| bpe_tokeniser              | 6.59 sec                                               | 9.73 sec: 1.48x slower                                |
| pyflate                    | 727 ms                                                 | 1.08 sec: 1.48x slower                                |
| deepcopy_reduce            | 4.04 us                                                | 6.01 us: 1.49x slower                                 |
| sqlglot_normalize          | 157 ms                                                 | 235 ms: 1.49x slower                                  |
| typing_runtime_protocols   | 224 us                                                 | 337 us: 1.50x slower                                  |
| html5lib                   | 88.9 ms                                                | 135 ms: 1.52x slower                                  |
| regex_compile              | 187 ms                                                 | 287 ms: 1.54x slower                                  |
| comprehensions             | 27.1 us                                                | 42.1 us: 1.55x slower                                 |
| coverage                   | 95.4 ms                                                | 149 ms: 1.56x slower                                  |
| spectral_norm              | 156 ms                                                 | 245 ms: 1.57x slower                                  |
| sqlglot_optimize           | 76.0 ms                                                | 121 ms: 1.59x slower                                  |
| thrift                     | 1.06 ms                                                | 1.71 ms: 1.62x slower                                 |
| float                      | 123 ms                                                 | 199 ms: 1.62x slower                                  |
| richards                   | 60.3 ms                                                | 99.0 ms: 1.64x slower                                 |
| logging_simple             | 9.45 us                                                | 15.5 us: 1.64x slower                                 |
| richards_super             | 72.8 ms                                                | 122 ms: 1.68x slower                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 165 ms: 1.71x slower                                  |
| logging_silent             | 139 ns                                                 | 240 ns: 1.72x slower                                  |
| sympy_str                  | 385 ms                                                 | 664 ms: 1.72x slower                                  |
| genshi_xml                 | 67.6 ms                                                | 117 ms: 1.72x slower                                  |
| unpickle_pure_python       | 300 us                                                 | 526 us: 1.75x slower                                  |
| logging_format             | 9.59 us                                                | 16.8 us: 1.76x slower                                 |
| pprint_pformat             | 1.98 sec                                               | 3.50 sec: 1.77x slower                                |
| pprint_safe_repr           | 967 ms                                                 | 1.71 sec: 1.77x slower                                |
| django_template            | 44.9 ms                                                | 80.7 ms: 1.79x slower                                 |
| genshi_text                | 30.2 ms                                                | 54.8 ms: 1.81x slower                                 |
| pickle_pure_python         | 436 us                                                 | 792 us: 1.82x slower                                  |
| sqlglot_transpile          | 2.34 ms                                                | 4.33 ms: 1.85x slower                                 |
| mako                       | 15.7 ms                                                | 29.7 ms: 1.89x slower                                 |
| raytrace                   | 408 ms                                                 | 784 ms: 1.92x slower                                  |
| chaos                      | 84.9 ms                                                | 165 ms: 1.95x slower                                  |
| hexiom                     | 8.27 ms                                                | 16.5 ms: 1.99x slower                                 |
| scimark_sor                | 167 ms                                                 | 337 ms: 2.02x slower                                  |
| sympy_sum                  | 222 ms                                                 | 460 ms: 2.07x slower                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.77 ms: 2.11x slower                                 |
| scimark_lu                 | 152 ms                                                 | 326 ms: 2.15x slower                                  |
| sympy_expand               | 582 ms                                                 | 1.27 sec: 2.18x slower                                |
| go                         | 172 ms                                                 | 395 ms: 2.30x slower                                  |
| nbody                      | 119 ms                                                 | 284 ms: 2.38x slower                                  |
| deltablue                  | 4.27 ms                                                | 10.8 ms: 2.54x slower                                 |
| unpack_sequence            | 60.2 ns                                                | 191 ns: 3.17x slower                                  |
| Geometric mean             | (ref)                                                  | 1.32x slower                                          |

Benchmark hidden because not significant (4): pathlib, unpickle, regex_dna, bench_thread_pool
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.16x