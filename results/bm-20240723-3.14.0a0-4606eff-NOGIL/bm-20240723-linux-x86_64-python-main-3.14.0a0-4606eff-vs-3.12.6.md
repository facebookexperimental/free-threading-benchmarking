# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 4606eff
- commit date: 2024-07-23
- overall geometric mean: 1.36x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 456 ms                                                 | 664 ms: 1.45x slower                                  |
| docutils       | 4.00 sec                                               | 4.86 sec: 1.22x slower                                |
| html5lib       | 88.9 ms                                                | 157 ms: 1.76x slower                                  |
| tornado_http   | 266 ms                                                 | 320 ms: 1.20x slower                                  |
| Geometric mean | (ref)                                                  | 1.39x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.17 sec: 1.66x faster                                |
| async_tree_io              | 1.85 sec                                               | 1.22 sec: 1.51x faster                                |
| async_tree_none_tg         | 704 ms                                                 | 493 ms: 1.43x faster                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 654 ms: 1.42x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 733 ms: 1.33x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 859 ms: 1.28x faster                                  |
| async_tree_none            | 741 ms                                                 | 593 ms: 1.25x faster                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 945 ms: 1.14x faster                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.27 sec: 1.16x slower                                |
| asyncio_tcp                | 923 ms                                                 | 1.12 sec: 1.22x slower                                |
| async_generators           | 589 ms                                                 | 724 ms: 1.23x slower                                  |
| coroutines                 | 29.5 ms                                                | 45.6 ms: 1.55x slower                                 |
| Geometric mean             | (ref)                                                  | 1.12x faster                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 123 ms                                                 | 200 ms: 1.63x slower                                  |
| nbody          | 119 ms                                                 | 283 ms: 2.37x slower                                  |
| Geometric mean | (ref)                                                  | 1.55x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.80 ms: 1.07x faster                                 |
| regex_dna      | 278 ms                                                 | 301 ms: 1.08x slower                                  |
| regex_compile  | 187 ms                                                 | 292 ms: 1.56x slower                                  |
| Geometric mean | (ref)                                                  | 1.13x slower                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 42.9 us: 1.23x faster                                 |
| pickle               | 16.4 us                                                | 14.3 us: 1.15x faster                                 |
| xml_etree_parse      | 241 ms                                                 | 213 ms: 1.13x faster                                  |
| pickle_list          | 6.97 us                                                | 6.45 us: 1.08x faster                                 |
| unpickle_list        | 6.83 us                                                | 7.21 us: 1.06x slower                                 |
| json_loads           | 37.9 us                                                | 45.2 us: 1.19x slower                                 |
| xml_etree_generate   | 127 ms                                                 | 158 ms: 1.24x slower                                  |
| json_dumps           | 14.3 ms                                                | 18.9 ms: 1.32x slower                                 |
| tomli_loads          | 2.88 sec                                               | 4.14 sec: 1.43x slower                                |
| xml_etree_process    | 83.7 ms                                                | 124 ms: 1.48x slower                                  |
| pickle_pure_python   | 436 us                                                 | 760 us: 1.75x slower                                  |
| unpickle_pure_python | 300 us                                                 | 540 us: 1.80x slower                                  |
| Geometric mean       | (ref)                                                  | 1.16x slower                                          |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.9 ms: 1.19x slower                                 |
| python_startup         | 23.7 ms                                                | 29.5 ms: 1.24x slower                                 |
| Geometric mean         | (ref)                                                  | 1.21x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 122 ms: 1.81x slower                                  |
| genshi_text     | 30.2 ms                                                | 55.7 ms: 1.84x slower                                 |
| django_template | 44.9 ms                                                | 84.5 ms: 1.88x slower                                 |
| mako            | 15.7 ms                                                | 31.9 ms: 2.02x slower                                 |
| Geometric mean  | (ref)                                                  | 1.89x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240723-linux-x86_64-python-main-3.14.0a0-4606eff |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.17 sec: 1.66x faster                                |
| bench_mp_pool              | 20.7 ms                                                | 13.3 ms: 1.55x faster                                 |
| async_tree_io              | 1.85 sec                                               | 1.22 sec: 1.51x faster                                |
| async_tree_none_tg         | 704 ms                                                 | 493 ms: 1.43x faster                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 654 ms: 1.42x faster                                  |
| async_tree_memoization     | 977 ms                                                 | 733 ms: 1.33x faster                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 859 ms: 1.28x faster                                  |
| gc_traversal               | 5.86 ms                                                | 4.60 ms: 1.27x faster                                 |
| async_tree_none            | 741 ms                                                 | 593 ms: 1.25x faster                                  |
| pickle_dict                | 52.7 us                                                | 42.9 us: 1.23x faster                                 |
| pickle                     | 16.4 us                                                | 14.3 us: 1.15x faster                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 945 ms: 1.14x faster                                  |
| xml_etree_parse            | 241 ms                                                 | 213 ms: 1.13x faster                                  |
| pickle_list                | 6.97 us                                                | 6.45 us: 1.08x faster                                 |
| regex_effbot               | 5.13 ms                                                | 4.80 ms: 1.07x faster                                 |
| create_gc_cycles           | 1.94 ms                                                | 1.82 ms: 1.06x faster                                 |
| unpickle_list              | 6.83 us                                                | 7.21 us: 1.06x slower                                 |
| regex_dna                  | 278 ms                                                 | 301 ms: 1.08x slower                                  |
| sqlite_synth               | 3.87 us                                                | 4.23 us: 1.09x slower                                 |
| bench_thread_pool          | 3.48 ms                                                | 4.01 ms: 1.15x slower                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.27 sec: 1.16x slower                                |
| python_startup_no_site     | 17.6 ms                                                | 20.9 ms: 1.19x slower                                 |
| json_loads                 | 37.9 us                                                | 45.2 us: 1.19x slower                                 |
| tornado_http               | 266 ms                                                 | 320 ms: 1.20x slower                                  |
| pycparser                  | 1.79 sec                                               | 2.16 sec: 1.21x slower                                |
| docutils                   | 4.00 sec                                               | 4.86 sec: 1.22x slower                                |
| asyncio_tcp                | 923 ms                                                 | 1.12 sec: 1.22x slower                                |
| async_generators           | 589 ms                                                 | 724 ms: 1.23x slower                                  |
| scimark_fft                | 500 ms                                                 | 617 ms: 1.23x slower                                  |
| xml_etree_generate         | 127 ms                                                 | 158 ms: 1.24x slower                                  |
| python_startup             | 23.7 ms                                                | 29.5 ms: 1.24x slower                                 |
| pylint                     | 465 ms                                                 | 582 ms: 1.25x slower                                  |
| json                       | 6.85 ms                                                | 8.61 ms: 1.26x slower                                 |
| deepcopy                   | 468 us                                                 | 594 us: 1.27x slower                                  |
| mdp                        | 3.97 sec                                               | 5.10 sec: 1.29x slower                                |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.70 ms: 1.30x slower                                 |
| nqueens                    | 117 ms                                                 | 152 ms: 1.30x slower                                  |
| json_dumps                 | 14.3 ms                                                | 18.9 ms: 1.32x slower                                 |
| deepcopy_memo              | 52.4 us                                                | 69.7 us: 1.33x slower                                 |
| generators                 | 41.1 ms                                                | 54.9 ms: 1.33x slower                                 |
| meteor_contest             | 146 ms                                                 | 199 ms: 1.36x slower                                  |
| dulwich_log                | 100 ms                                                 | 140 ms: 1.39x slower                                  |
| telco                      | 9.59 ms                                                | 13.4 ms: 1.39x slower                                 |
| comprehensions             | 27.1 us                                                | 38.3 us: 1.41x slower                                 |
| tomli_loads                | 2.88 sec                                               | 4.14 sec: 1.43x slower                                |
| fannkuch                   | 540 ms                                                 | 783 ms: 1.45x slower                                  |
| deepcopy_reduce            | 4.04 us                                                | 5.85 us: 1.45x slower                                 |
| 2to3                       | 456 ms                                                 | 664 ms: 1.45x slower                                  |
| sqlglot_normalize          | 157 ms                                                 | 230 ms: 1.46x slower                                  |
| crypto_pyaes               | 107 ms                                                 | 157 ms: 1.47x slower                                  |
| sympy_integrate            | 29.8 ms                                                | 43.9 ms: 1.48x slower                                 |
| xml_etree_process          | 83.7 ms                                                | 124 ms: 1.48x slower                                  |
| typing_runtime_protocols   | 224 us                                                 | 342 us: 1.52x slower                                  |
| bpe_tokeniser              | 6.59 sec                                               | 10.1 sec: 1.53x slower                                |
| coroutines                 | 29.5 ms                                                | 45.6 ms: 1.55x slower                                 |
| pyflate                    | 727 ms                                                 | 1.13 sec: 1.56x slower                                |
| regex_compile              | 187 ms                                                 | 292 ms: 1.56x slower                                  |
| coverage                   | 95.4 ms                                                | 151 ms: 1.59x slower                                  |
| spectral_norm              | 156 ms                                                 | 247 ms: 1.59x slower                                  |
| logging_simple             | 9.45 us                                                | 15.2 us: 1.61x slower                                 |
| float                      | 123 ms                                                 | 200 ms: 1.63x slower                                  |
| sqlglot_optimize           | 76.0 ms                                                | 124 ms: 1.64x slower                                  |
| thrift                     | 1.06 ms                                                | 1.75 ms: 1.65x slower                                 |
| scimark_monte_carlo        | 96.4 ms                                                | 163 ms: 1.69x slower                                  |
| logging_format             | 9.59 us                                                | 16.6 us: 1.73x slower                                 |
| pickle_pure_python         | 436 us                                                 | 760 us: 1.75x slower                                  |
| html5lib                   | 88.9 ms                                                | 157 ms: 1.76x slower                                  |
| logging_silent             | 139 ns                                                 | 246 ns: 1.76x slower                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.71 sec: 1.77x slower                                |
| sympy_str                  | 385 ms                                                 | 685 ms: 1.78x slower                                  |
| pprint_pformat             | 1.98 sec                                               | 3.55 sec: 1.79x slower                                |
| unpickle_pure_python       | 300 us                                                 | 540 us: 1.80x slower                                  |
| genshi_xml                 | 67.6 ms                                                | 122 ms: 1.81x slower                                  |
| richards_super             | 72.8 ms                                                | 133 ms: 1.82x slower                                  |
| genshi_text                | 30.2 ms                                                | 55.7 ms: 1.84x slower                                 |
| richards                   | 60.3 ms                                                | 112 ms: 1.85x slower                                  |
| django_template            | 44.9 ms                                                | 84.5 ms: 1.88x slower                                 |
| sqlglot_transpile          | 2.34 ms                                                | 4.58 ms: 1.96x slower                                 |
| raytrace                   | 408 ms                                                 | 807 ms: 1.98x slower                                  |
| mako                       | 15.7 ms                                                | 31.9 ms: 2.02x slower                                 |
| hexiom                     | 8.27 ms                                                | 16.7 ms: 2.03x slower                                 |
| scimark_sor                | 167 ms                                                 | 341 ms: 2.05x slower                                  |
| chaos                      | 84.9 ms                                                | 175 ms: 2.06x slower                                  |
| scimark_lu                 | 152 ms                                                 | 314 ms: 2.06x slower                                  |
| sympy_sum                  | 222 ms                                                 | 476 ms: 2.14x slower                                  |
| sympy_expand               | 582 ms                                                 | 1.27 sec: 2.18x slower                                |
| sqlglot_parse              | 1.79 ms                                                | 3.99 ms: 2.23x slower                                 |
| nbody                      | 119 ms                                                 | 283 ms: 2.37x slower                                  |
| go                         | 172 ms                                                 | 411 ms: 2.38x slower                                  |
| deltablue                  | 4.27 ms                                                | 11.4 ms: 2.67x slower                                 |
| unpack_sequence            | 60.2 ns                                                | 200 ns: 3.32x slower                                  |
| Geometric mean             | (ref)                                                  | 1.36x slower                                          |

Benchmark hidden because not significant (6): xml_etree_iterparse, pidigits, unpickle, asyncio_websockets, pathlib, regex_v8
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.16x