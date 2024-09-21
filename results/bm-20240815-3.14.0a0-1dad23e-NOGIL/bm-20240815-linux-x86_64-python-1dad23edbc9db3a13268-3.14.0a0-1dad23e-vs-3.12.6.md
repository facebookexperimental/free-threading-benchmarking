# Results vs. 3.12.6

- fork: python
- ref: 1dad23edbc9db3a13268
- machine: linux-x86_64
- commit hash: 1dad23e
- commit date: 2024-08-15
- overall geometric mean: 1.40x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 687 ms: 1.51x slower                                                  |
| docutils       | 4.00 sec                                               | 5.35 sec: 1.34x slower                                                |
| html5lib       | 88.9 ms                                                | 147 ms: 1.66x slower                                                  |
| tornado_http   | 266 ms                                                 | 350 ms: 1.32x slower                                                  |
| Geometric mean | (ref)                                                  | 1.45x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.14 sec: 1.70x faster                                                |
| async_tree_io              | 1.85 sec                                               | 1.28 sec: 1.45x faster                                                |
| async_tree_none_tg         | 704 ms                                                 | 490 ms: 1.44x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 672 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 836 ms: 1.32x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 774 ms: 1.26x faster                                                  |
| async_tree_none            | 741 ms                                                 | 626 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 926 ms: 1.16x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 781 ms: 1.04x slower                                                  |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.47 sec: 1.24x slower                                                |
| async_generators           | 589 ms                                                 | 731 ms: 1.24x slower                                                  |
| asyncio_tcp                | 923 ms                                                 | 1.16 sec: 1.25x slower                                                |
| coroutines                 | 29.5 ms                                                | 42.9 ms: 1.46x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.11x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 123 ms                                                 | 195 ms: 1.58x slower                                                  |
| nbody          | 119 ms                                                 | 307 ms: 2.58x slower                                                  |
| Geometric mean | (ref)                                                  | 1.60x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 278 ms                                                 | 300 ms: 1.08x slower                                                  |
| regex_v8       | 32.5 ms                                                | 36.8 ms: 1.13x slower                                                 |
| regex_compile  | 187 ms                                                 | 310 ms: 1.66x slower                                                  |
| Geometric mean | (ref)                                                  | 1.18x slower                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 42.2 us: 1.25x faster                                                 |
| pickle               | 16.4 us                                                | 13.8 us: 1.18x faster                                                 |
| xml_etree_parse      | 241 ms                                                 | 229 ms: 1.05x faster                                                  |
| unpickle             | 21.2 us                                                | 23.4 us: 1.10x slower                                                 |
| unpickle_list        | 6.83 us                                                | 7.89 us: 1.15x slower                                                 |
| json_loads           | 37.9 us                                                | 44.8 us: 1.18x slower                                                 |
| xml_etree_generate   | 127 ms                                                 | 167 ms: 1.31x slower                                                  |
| json_dumps           | 14.3 ms                                                | 19.0 ms: 1.32x slower                                                 |
| tomli_loads          | 2.88 sec                                               | 4.23 sec: 1.47x slower                                                |
| xml_etree_process    | 83.7 ms                                                | 130 ms: 1.55x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 783 us: 1.80x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 578 us: 1.93x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.20x slower                                                          |

Benchmark hidden because not significant (2): pickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.9 ms: 1.19x slower                                                 |
| python_startup         | 23.7 ms                                                | 30.8 ms: 1.30x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 55.2 ms: 1.83x slower                                                 |
| genshi_xml      | 67.6 ms                                                | 124 ms: 1.84x slower                                                  |
| django_template | 44.9 ms                                                | 87.7 ms: 1.95x slower                                                 |
| mako            | 15.7 ms                                                | 31.5 ms: 2.00x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.90x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.14 sec: 1.70x faster                                                |
| async_tree_io              | 1.85 sec                                               | 1.28 sec: 1.45x faster                                                |
| async_tree_none_tg         | 704 ms                                                 | 490 ms: 1.44x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 672 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 836 ms: 1.32x faster                                                  |
| async_tree_memoization     | 977 ms                                                 | 774 ms: 1.26x faster                                                  |
| pickle_dict                | 52.7 us                                                | 42.2 us: 1.25x faster                                                 |
| async_tree_none            | 741 ms                                                 | 626 ms: 1.19x faster                                                  |
| pickle                     | 16.4 us                                                | 13.8 us: 1.18x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 926 ms: 1.16x faster                                                  |
| gc_traversal               | 5.86 ms                                                | 5.05 ms: 1.16x faster                                                 |
| bench_mp_pool              | 20.7 ms                                                | 18.5 ms: 1.12x faster                                                 |
| xml_etree_parse            | 241 ms                                                 | 229 ms: 1.05x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 781 ms: 1.04x slower                                                  |
| regex_dna                  | 278 ms                                                 | 300 ms: 1.08x slower                                                  |
| unpickle                   | 21.2 us                                                | 23.4 us: 1.10x slower                                                 |
| sqlite_synth               | 3.87 us                                                | 4.29 us: 1.11x slower                                                 |
| regex_v8                   | 32.5 ms                                                | 36.8 ms: 1.13x slower                                                 |
| unpickle_list              | 6.83 us                                                | 7.89 us: 1.15x slower                                                 |
| pathlib                    | 31.6 ms                                                | 37.4 ms: 1.18x slower                                                 |
| json_loads                 | 37.9 us                                                | 44.8 us: 1.18x slower                                                 |
| python_startup_no_site     | 17.6 ms                                                | 20.9 ms: 1.19x slower                                                 |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.47 sec: 1.24x slower                                                |
| async_generators           | 589 ms                                                 | 731 ms: 1.24x slower                                                  |
| pycparser                  | 1.79 sec                                               | 2.23 sec: 1.24x slower                                                |
| asyncio_tcp                | 923 ms                                                 | 1.16 sec: 1.25x slower                                                |
| json                       | 6.85 ms                                                | 8.59 ms: 1.25x slower                                                 |
| python_startup             | 23.7 ms                                                | 30.8 ms: 1.30x slower                                                 |
| pylint                     | 465 ms                                                 | 606 ms: 1.30x slower                                                  |
| xml_etree_generate         | 127 ms                                                 | 167 ms: 1.31x slower                                                  |
| scimark_fft                | 500 ms                                                 | 657 ms: 1.31x slower                                                  |
| tornado_http               | 266 ms                                                 | 350 ms: 1.32x slower                                                  |
| mdp                        | 3.97 sec                                               | 5.24 sec: 1.32x slower                                                |
| json_dumps                 | 14.3 ms                                                | 19.0 ms: 1.32x slower                                                 |
| deepcopy                   | 468 us                                                 | 626 us: 1.34x slower                                                  |
| docutils                   | 4.00 sec                                               | 5.35 sec: 1.34x slower                                                |
| meteor_contest             | 146 ms                                                 | 202 ms: 1.38x slower                                                  |
| nqueens                    | 117 ms                                                 | 164 ms: 1.40x slower                                                  |
| generators                 | 41.1 ms                                                | 58.2 ms: 1.41x slower                                                 |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 9.49 ms: 1.42x slower                                                 |
| telco                      | 9.59 ms                                                | 13.7 ms: 1.43x slower                                                 |
| comprehensions             | 27.1 us                                                | 39.2 us: 1.45x slower                                                 |
| coroutines                 | 29.5 ms                                                | 42.9 ms: 1.46x slower                                                 |
| tomli_loads                | 2.88 sec                                               | 4.23 sec: 1.47x slower                                                |
| deepcopy_memo              | 52.4 us                                                | 77.4 us: 1.48x slower                                                 |
| sqlglot_normalize          | 157 ms                                                 | 235 ms: 1.49x slower                                                  |
| crypto_pyaes               | 107 ms                                                 | 161 ms: 1.50x slower                                                  |
| 2to3                       | 456 ms                                                 | 687 ms: 1.51x slower                                                  |
| fannkuch                   | 540 ms                                                 | 814 ms: 1.51x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 342 us: 1.52x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 45.4 ms: 1.53x slower                                                 |
| bench_thread_pool          | 3.48 ms                                                | 5.33 ms: 1.53x slower                                                 |
| pyflate                    | 727 ms                                                 | 1.12 sec: 1.54x slower                                                |
| xml_etree_process          | 83.7 ms                                                | 130 ms: 1.55x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.66 ms: 1.57x slower                                                 |
| logging_simple             | 9.45 us                                                | 14.9 us: 1.58x slower                                                 |
| float                      | 123 ms                                                 | 195 ms: 1.58x slower                                                  |
| spectral_norm              | 156 ms                                                 | 247 ms: 1.59x slower                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 122 ms: 1.61x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 10.7 sec: 1.62x slower                                                |
| deepcopy_reduce            | 4.04 us                                                | 6.61 us: 1.64x slower                                                 |
| html5lib                   | 88.9 ms                                                | 147 ms: 1.66x slower                                                  |
| regex_compile              | 187 ms                                                 | 310 ms: 1.66x slower                                                  |
| coverage                   | 95.4 ms                                                | 159 ms: 1.66x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 161 ms: 1.67x slower                                                  |
| richards                   | 60.3 ms                                                | 107 ms: 1.77x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 783 us: 1.80x slower                                                  |
| logging_format             | 9.59 us                                                | 17.3 us: 1.80x slower                                                 |
| sympy_str                  | 385 ms                                                 | 697 ms: 1.81x slower                                                  |
| genshi_text                | 30.2 ms                                                | 55.2 ms: 1.83x slower                                                 |
| pprint_pformat             | 1.98 sec                                               | 3.62 sec: 1.83x slower                                                |
| richards_super             | 72.8 ms                                                | 133 ms: 1.83x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 124 ms: 1.84x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.80 sec: 1.86x slower                                                |
| logging_silent             | 139 ns                                                 | 266 ns: 1.91x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 578 us: 1.93x slower                                                  |
| raytrace                   | 408 ms                                                 | 789 ms: 1.94x slower                                                  |
| django_template            | 44.9 ms                                                | 87.7 ms: 1.95x slower                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 4.65 ms: 1.99x slower                                                 |
| mako                       | 15.7 ms                                                | 31.5 ms: 2.00x slower                                                 |
| hexiom                     | 8.27 ms                                                | 16.9 ms: 2.05x slower                                                 |
| sympy_sum                  | 222 ms                                                 | 462 ms: 2.08x slower                                                  |
| chaos                      | 84.9 ms                                                | 177 ms: 2.09x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 319 ms: 2.10x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 3.77 ms: 2.11x slower                                                 |
| scimark_sor                | 167 ms                                                 | 355 ms: 2.13x slower                                                  |
| sympy_expand               | 582 ms                                                 | 1.26 sec: 2.16x slower                                                |
| go                         | 172 ms                                                 | 440 ms: 2.56x slower                                                  |
| nbody                      | 119 ms                                                 | 307 ms: 2.58x slower                                                  |
| deltablue                  | 4.27 ms                                                | 11.8 ms: 2.77x slower                                                 |
| unpack_sequence            | 60.2 ns                                                | 212 ns: 3.52x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.40x slower                                                          |

Benchmark hidden because not significant (5): pickle_list, create_gc_cycles, regex_effbot, pidigits, xml_etree_iterparse
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.34x
- 95% likely to have a slowdown of 1.33x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.15x