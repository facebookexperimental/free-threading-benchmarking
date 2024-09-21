# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5f68511
- commit date: 2024-08-13
- overall geometric mean: 1.40x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                                 | 661 ms: 1.45x slower                                  |
| docutils       | 4.00 sec                                               | 5.15 sec: 1.29x slower                                |
| html5lib       | 88.9 ms                                                | 145 ms: 1.63x slower                                  |
| tornado_http   | 266 ms                                                 | 360 ms: 1.35x slower                                  |
| Geometric mean | (ref)                                                  | 1.42x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.17 sec: 1.66x faster                                |
| async_tree_io              | 1.85 sec                                               | 1.30 sec: 1.42x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 671 ms: 1.39x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 521 ms: 1.35x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 849 ms: 1.30x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 787 ms: 1.24x faster                                  |
| async_tree_none            | 741 ms                                                 | 621 ms: 1.19x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 945 ms: 1.14x faster                                  |
| asyncio_websockets         | 748 ms                                                 | 788 ms: 1.05x slower                                  |
| asyncio_tcp                | 923 ms                                                 | 1.17 sec: 1.26x slower                                |
| async_generators           | 589 ms                                                 | 744 ms: 1.26x slower                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.55 sec: 1.26x slower                                |
| coroutines                 | 29.5 ms                                                | 44.5 ms: 1.51x slower                                 |
| Geometric mean             | (ref)                                                  | 1.09x faster                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 123 ms                                                 | 206 ms: 1.67x slower                                  |
| nbody          | 119 ms                                                 | 293 ms: 2.46x slower                                  |
| Geometric mean | (ref)                                                  | 1.59x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.62 ms: 1.11x faster                                 |
| regex_dna      | 278 ms                                                 | 289 ms: 1.04x slower                                  |
| regex_v8       | 32.5 ms                                                | 36.7 ms: 1.13x slower                                 |
| regex_compile  | 187 ms                                                 | 290 ms: 1.56x slower                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 45.2 us: 1.17x faster                                 |
| pickle_list          | 6.97 us                                                | 6.17 us: 1.13x faster                                 |
| pickle               | 16.4 us                                                | 14.6 us: 1.12x faster                                 |
| xml_etree_parse      | 241 ms                                                 | 223 ms: 1.08x faster                                  |
| json_loads           | 37.9 us                                                | 43.2 us: 1.14x slower                                 |
| unpickle_list        | 6.83 us                                                | 8.50 us: 1.24x slower                                 |
| xml_etree_generate   | 127 ms                                                 | 159 ms: 1.25x slower                                  |
| json_dumps           | 14.3 ms                                                | 19.1 ms: 1.33x slower                                 |
| tomli_loads          | 2.88 sec                                               | 4.26 sec: 1.48x slower                                |
| xml_etree_process    | 83.7 ms                                                | 137 ms: 1.64x slower                                  |
| pickle_pure_python   | 436 us                                                 | 803 us: 1.84x slower                                  |
| unpickle_pure_python | 300 us                                                 | 619 us: 2.07x slower                                  |
| Geometric mean       | (ref)                                                  | 1.21x slower                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 21.2 ms: 1.21x slower                                 |
| python_startup         | 23.7 ms                                                | 31.5 ms: 1.33x slower                                 |
| Geometric mean         | (ref)                                                  | 1.27x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 117 ms: 1.72x slower                                  |
| genshi_text     | 30.2 ms                                                | 55.9 ms: 1.85x slower                                 |
| django_template | 44.9 ms                                                | 85.9 ms: 1.91x slower                                 |
| mako            | 15.7 ms                                                | 32.0 ms: 2.03x slower                                 |
| Geometric mean  | (ref)                                                  | 1.88x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.17 sec: 1.66x faster                                |
| async_tree_io              | 1.85 sec                                               | 1.30 sec: 1.42x faster                                |
| async_tree_memoization_tg  | 930 ms                                                 | 671 ms: 1.39x faster                                  |
| async_tree_none_tg         | 704 ms                                                 | 521 ms: 1.35x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 849 ms: 1.30x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 787 ms: 1.24x faster                                  |
| bench_mp_pool              | 20.7 ms                                                | 16.8 ms: 1.23x faster                                 |
| async_tree_none            | 741 ms                                                 | 621 ms: 1.19x faster                                  |
| pickle_dict                | 52.7 us                                                | 45.2 us: 1.17x faster                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 945 ms: 1.14x faster                                  |
| pickle_list                | 6.97 us                                                | 6.17 us: 1.13x faster                                 |
| pickle                     | 16.4 us                                                | 14.6 us: 1.12x faster                                 |
| regex_effbot               | 5.13 ms                                                | 4.62 ms: 1.11x faster                                 |
| gc_traversal               | 5.86 ms                                                | 5.42 ms: 1.08x faster                                 |
| xml_etree_parse            | 241 ms                                                 | 223 ms: 1.08x faster                                  |
| regex_dna                  | 278 ms                                                 | 289 ms: 1.04x slower                                  |
| asyncio_websockets         | 748 ms                                                 | 788 ms: 1.05x slower                                  |
| pathlib                    | 31.6 ms                                                | 34.5 ms: 1.09x slower                                 |
| regex_v8                   | 32.5 ms                                                | 36.7 ms: 1.13x slower                                 |
| sqlite_synth               | 3.87 us                                                | 4.38 us: 1.13x slower                                 |
| json_loads                 | 37.9 us                                                | 43.2 us: 1.14x slower                                 |
| python_startup_no_site     | 17.6 ms                                                | 21.2 ms: 1.21x slower                                 |
| pycparser                  | 1.79 sec                                               | 2.18 sec: 1.22x slower                                |
| deepcopy                   | 468 us                                                 | 571 us: 1.22x slower                                  |
| unpickle_list              | 6.83 us                                                | 8.50 us: 1.24x slower                                 |
| xml_etree_generate         | 127 ms                                                 | 159 ms: 1.25x slower                                  |
| json                       | 6.85 ms                                                | 8.55 ms: 1.25x slower                                 |
| scimark_fft                | 500 ms                                                 | 628 ms: 1.26x slower                                  |
| asyncio_tcp                | 923 ms                                                 | 1.17 sec: 1.26x slower                                |
| async_generators           | 589 ms                                                 | 744 ms: 1.26x slower                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.55 sec: 1.26x slower                                |
| pylint                     | 465 ms                                                 | 588 ms: 1.27x slower                                  |
| docutils                   | 4.00 sec                                               | 5.15 sec: 1.29x slower                                |
| mdp                        | 3.97 sec                                               | 5.24 sec: 1.32x slower                                |
| python_startup             | 23.7 ms                                                | 31.5 ms: 1.33x slower                                 |
| json_dumps                 | 14.3 ms                                                | 19.1 ms: 1.33x slower                                 |
| tornado_http               | 266 ms                                                 | 360 ms: 1.35x slower                                  |
| deepcopy_memo              | 52.4 us                                                | 72.7 us: 1.39x slower                                 |
| bench_thread_pool          | 3.48 ms                                                | 4.83 ms: 1.39x slower                                 |
| generators                 | 41.1 ms                                                | 58.3 ms: 1.42x slower                                 |
| meteor_contest             | 146 ms                                                 | 210 ms: 1.43x slower                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 9.62 ms: 1.44x slower                                 |
| 2to3                       | 456 ms                                                 | 661 ms: 1.45x slower                                  |
| nqueens                    | 117 ms                                                 | 170 ms: 1.46x slower                                  |
| crypto_pyaes               | 107 ms                                                 | 157 ms: 1.46x slower                                  |
| sqlglot_normalize          | 157 ms                                                 | 231 ms: 1.47x slower                                  |
| tomli_loads                | 2.88 sec                                               | 4.26 sec: 1.48x slower                                |
| fannkuch                   | 540 ms                                                 | 804 ms: 1.49x slower                                  |
| comprehensions             | 27.1 us                                                | 40.4 us: 1.49x slower                                 |
| coroutines                 | 29.5 ms                                                | 44.5 ms: 1.51x slower                                 |
| deepcopy_reduce            | 4.04 us                                                | 6.14 us: 1.52x slower                                 |
| coverage                   | 95.4 ms                                                | 146 ms: 1.53x slower                                  |
| telco                      | 9.59 ms                                                | 14.8 ms: 1.54x slower                                 |
| pyflate                    | 727 ms                                                 | 1.13 sec: 1.55x slower                                |
| regex_compile              | 187 ms                                                 | 290 ms: 1.56x slower                                  |
| typing_runtime_protocols   | 224 us                                                 | 350 us: 1.56x slower                                  |
| bpe_tokeniser              | 6.59 sec                                               | 10.6 sec: 1.60x slower                                |
| logging_simple             | 9.45 us                                                | 15.2 us: 1.61x slower                                 |
| html5lib                   | 88.9 ms                                                | 145 ms: 1.63x slower                                  |
| thrift                     | 1.06 ms                                                | 1.72 ms: 1.63x slower                                 |
| sqlglot_optimize           | 76.0 ms                                                | 124 ms: 1.63x slower                                  |
| xml_etree_process          | 83.7 ms                                                | 137 ms: 1.64x slower                                  |
| spectral_norm              | 156 ms                                                 | 258 ms: 1.66x slower                                  |
| float                      | 123 ms                                                 | 206 ms: 1.67x slower                                  |
| genshi_xml                 | 67.6 ms                                                | 117 ms: 1.72x slower                                  |
| sympy_integrate            | 29.8 ms                                                | 51.8 ms: 1.74x slower                                 |
| richards                   | 60.3 ms                                                | 106 ms: 1.76x slower                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.71 sec: 1.77x slower                                |
| pprint_pformat             | 1.98 sec                                               | 3.54 sec: 1.79x slower                                |
| richards_super             | 72.8 ms                                                | 131 ms: 1.80x slower                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 174 ms: 1.81x slower                                  |
| logging_format             | 9.59 us                                                | 17.5 us: 1.83x slower                                 |
| sympy_str                  | 385 ms                                                 | 709 ms: 1.84x slower                                  |
| pickle_pure_python         | 436 us                                                 | 803 us: 1.84x slower                                  |
| genshi_text                | 30.2 ms                                                | 55.9 ms: 1.85x slower                                 |
| sqlglot_transpile          | 2.34 ms                                                | 4.33 ms: 1.85x slower                                 |
| logging_silent             | 139 ns                                                 | 262 ns: 1.88x slower                                  |
| django_template            | 44.9 ms                                                | 85.9 ms: 1.91x slower                                 |
| raytrace                   | 408 ms                                                 | 804 ms: 1.97x slower                                  |
| scimark_lu                 | 152 ms                                                 | 305 ms: 2.01x slower                                  |
| hexiom                     | 8.27 ms                                                | 16.8 ms: 2.03x slower                                 |
| mako                       | 15.7 ms                                                | 32.0 ms: 2.03x slower                                 |
| unpickle_pure_python       | 300 us                                                 | 619 us: 2.07x slower                                  |
| chaos                      | 84.9 ms                                                | 177 ms: 2.08x slower                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.84 ms: 2.14x slower                                 |
| sympy_sum                  | 222 ms                                                 | 479 ms: 2.16x slower                                  |
| scimark_sor                | 167 ms                                                 | 368 ms: 2.21x slower                                  |
| sympy_expand               | 582 ms                                                 | 1.30 sec: 2.24x slower                                |
| nbody                      | 119 ms                                                 | 293 ms: 2.46x slower                                  |
| go                         | 172 ms                                                 | 465 ms: 2.70x slower                                  |
| deltablue                  | 4.27 ms                                                | 12.0 ms: 2.81x slower                                 |
| unpack_sequence            | 60.2 ns                                                | 180 ns: 2.99x slower                                  |
| Geometric mean             | (ref)                                                  | 1.40x slower                                          |

Benchmark hidden because not significant (4): pidigits, xml_etree_iterparse, create_gc_cycles, unpickle
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.15x