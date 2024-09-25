# Results vs. 3.12.6

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.37x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 648 ms: 1.42x slower                                         |
| chameleon      | 9.31 ms                                                | 18.1 ms: 1.94x slower                                        |
| docutils       | 4.00 sec                                               | 4.93 sec: 1.23x slower                                       |
| html5lib       | 88.9 ms                                                | 147 ms: 1.65x slower                                         |
| tornado_http   | 266 ms                                                 | 356 ms: 1.34x slower                                         |
| Geometric mean | (ref)                                                  | 1.50x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.17 sec: 1.66x faster                                       |
| async_tree_io              | 1.85 sec                                               | 1.29 sec: 1.43x faster                                       |
| async_tree_memoization_tg  | 930 ms                                                 | 729 ms: 1.28x faster                                         |
| async_tree_memoization     | 977 ms                                                 | 766 ms: 1.27x faster                                         |
| async_tree_none_tg         | 704 ms                                                 | 583 ms: 1.21x faster                                         |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 938 ms: 1.17x faster                                         |
| async_tree_none            | 741 ms                                                 | 654 ms: 1.13x faster                                         |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 988 ms: 1.09x faster                                         |
| asyncio_websockets         | 748 ms                                                 | 780 ms: 1.04x slower                                         |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.29 sec: 1.17x slower                                       |
| async_generators           | 589 ms                                                 | 718 ms: 1.22x slower                                         |
| asyncio_tcp                | 923 ms                                                 | 1.17 sec: 1.27x slower                                       |
| coroutines                 | 29.5 ms                                                | 42.2 ms: 1.43x slower                                        |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 123 ms                                                 | 193 ms: 1.57x slower                                         |
| nbody          | 119 ms                                                 | 267 ms: 2.24x slower                                         |
| Geometric mean | (ref)                                                  | 1.52x slower                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| regex_v8       | 32.5 ms                                                | 35.5 ms: 1.09x slower                                        |
| regex_dna      | 278 ms                                                 | 312 ms: 1.12x slower                                         |
| regex_compile  | 187 ms                                                 | 271 ms: 1.45x slower                                         |
| Geometric mean | (ref)                                                  | 1.16x slower                                                 |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 43.3 us: 1.22x faster                                        |
| xml_etree_parse      | 241 ms                                                 | 200 ms: 1.21x faster                                         |
| pickle               | 16.4 us                                                | 14.4 us: 1.14x faster                                        |
| xml_etree_iterparse  | 169 ms                                                 | 159 ms: 1.06x faster                                         |
| json_loads           | 37.9 us                                                | 42.7 us: 1.13x slower                                        |
| xml_etree_generate   | 127 ms                                                 | 153 ms: 1.20x slower                                         |
| json_dumps           | 14.3 ms                                                | 18.0 ms: 1.25x slower                                        |
| tomli_loads          | 2.88 sec                                               | 4.19 sec: 1.45x slower                                       |
| xml_etree_process    | 83.7 ms                                                | 126 ms: 1.51x slower                                         |
| unpickle_pure_python | 300 us                                                 | 515 us: 1.72x slower                                         |
| pickle_pure_python   | 436 us                                                 | 872 us: 2.00x slower                                         |
| Geometric mean       | (ref)                                                  | 1.15x slower                                                 |

Benchmark hidden because not significant (3): pickle_list, unpickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 21.9 ms: 1.24x slower                                        |
| python_startup         | 23.7 ms                                                | 33.8 ms: 1.43x slower                                        |
| Geometric mean         | (ref)                                                  | 1.33x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 76.1 ms: 1.69x slower                                        |
| genshi_xml      | 67.6 ms                                                | 118 ms: 1.75x slower                                         |
| genshi_text     | 30.2 ms                                                | 54.3 ms: 1.80x slower                                        |
| mako            | 15.7 ms                                                | 29.9 ms: 1.90x slower                                        |
| Geometric mean  | (ref)                                                  | 1.78x slower                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.17 sec: 1.66x faster                                       |
| bench_mp_pool              | 20.7 ms                                                | 13.3 ms: 1.55x faster                                        |
| async_tree_io              | 1.85 sec                                               | 1.29 sec: 1.43x faster                                       |
| gc_traversal               | 5.86 ms                                                | 4.47 ms: 1.31x faster                                        |
| async_tree_memoization_tg  | 930 ms                                                 | 729 ms: 1.28x faster                                         |
| async_tree_memoization     | 977 ms                                                 | 766 ms: 1.27x faster                                         |
| pickle_dict                | 52.7 us                                                | 43.3 us: 1.22x faster                                        |
| async_tree_none_tg         | 704 ms                                                 | 583 ms: 1.21x faster                                         |
| xml_etree_parse            | 241 ms                                                 | 200 ms: 1.21x faster                                         |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 938 ms: 1.17x faster                                         |
| pickle                     | 16.4 us                                                | 14.4 us: 1.14x faster                                        |
| async_tree_none            | 741 ms                                                 | 654 ms: 1.13x faster                                         |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 988 ms: 1.09x faster                                         |
| xml_etree_iterparse        | 169 ms                                                 | 159 ms: 1.06x faster                                         |
| asyncio_websockets         | 748 ms                                                 | 780 ms: 1.04x slower                                         |
| regex_v8                   | 32.5 ms                                                | 35.5 ms: 1.09x slower                                        |
| bench_thread_pool          | 3.48 ms                                                | 3.85 ms: 1.11x slower                                        |
| sqlite_synth               | 3.87 us                                                | 4.31 us: 1.11x slower                                        |
| regex_dna                  | 278 ms                                                 | 312 ms: 1.12x slower                                         |
| json_loads                 | 37.9 us                                                | 42.7 us: 1.13x slower                                        |
| pathlib                    | 31.6 ms                                                | 36.1 ms: 1.14x slower                                        |
| json                       | 6.85 ms                                                | 7.98 ms: 1.16x slower                                        |
| asyncio_tcp_ssl            | 2.81 sec                                               | 3.29 sec: 1.17x slower                                       |
| pycparser                  | 1.79 sec                                               | 2.13 sec: 1.19x slower                                       |
| xml_etree_generate         | 127 ms                                                 | 153 ms: 1.20x slower                                         |
| scimark_fft                | 500 ms                                                 | 604 ms: 1.21x slower                                         |
| async_generators           | 589 ms                                                 | 718 ms: 1.22x slower                                         |
| mdp                        | 3.97 sec                                               | 4.87 sec: 1.23x slower                                       |
| docutils                   | 4.00 sec                                               | 4.93 sec: 1.23x slower                                       |
| pylint                     | 465 ms                                                 | 576 ms: 1.24x slower                                         |
| python_startup_no_site     | 17.6 ms                                                | 21.9 ms: 1.24x slower                                        |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.40 ms: 1.25x slower                                        |
| json_dumps                 | 14.3 ms                                                | 18.0 ms: 1.25x slower                                        |
| asyncio_tcp                | 923 ms                                                 | 1.17 sec: 1.27x slower                                       |
| dulwich_log                | 100 ms                                                 | 128 ms: 1.28x slower                                         |
| nqueens                    | 117 ms                                                 | 151 ms: 1.30x slower                                         |
| generators                 | 41.1 ms                                                | 54.0 ms: 1.31x slower                                        |
| crypto_pyaes               | 107 ms                                                 | 142 ms: 1.32x slower                                         |
| tornado_http               | 266 ms                                                 | 356 ms: 1.34x slower                                         |
| meteor_contest             | 146 ms                                                 | 198 ms: 1.36x slower                                         |
| comprehensions             | 27.1 us                                                | 36.9 us: 1.36x slower                                        |
| fannkuch                   | 540 ms                                                 | 738 ms: 1.37x slower                                         |
| gunicorn                   | 1.81 ms                                                | 2.53 ms: 1.40x slower                                        |
| pyflate                    | 727 ms                                                 | 1.03 sec: 1.42x slower                                       |
| 2to3                       | 456 ms                                                 | 648 ms: 1.42x slower                                         |
| python_startup             | 23.7 ms                                                | 33.8 ms: 1.43x slower                                        |
| coroutines                 | 29.5 ms                                                | 42.2 ms: 1.43x slower                                        |
| sqlglot_normalize          | 157 ms                                                 | 225 ms: 1.43x slower                                         |
| tomli_loads                | 2.88 sec                                               | 4.19 sec: 1.45x slower                                       |
| regex_compile              | 187 ms                                                 | 271 ms: 1.45x slower                                         |
| sympy_integrate            | 29.8 ms                                                | 43.4 ms: 1.46x slower                                        |
| typing_runtime_protocols   | 224 us                                                 | 329 us: 1.47x slower                                         |
| spectral_norm              | 156 ms                                                 | 231 ms: 1.48x slower                                         |
| telco                      | 9.59 ms                                                | 14.3 ms: 1.49x slower                                        |
| aiohttp                    | 1.99 ms                                                | 2.97 ms: 1.49x slower                                        |
| bpe_tokeniser              | 6.59 sec                                               | 9.94 sec: 1.51x slower                                       |
| xml_etree_process          | 83.7 ms                                                | 126 ms: 1.51x slower                                         |
| coverage                   | 95.4 ms                                                | 148 ms: 1.55x slower                                         |
| thrift                     | 1.06 ms                                                | 1.65 ms: 1.55x slower                                        |
| float                      | 123 ms                                                 | 193 ms: 1.57x slower                                         |
| deepcopy                   | 468 us                                                 | 744 us: 1.59x slower                                         |
| sqlglot_optimize           | 76.0 ms                                                | 122 ms: 1.60x slower                                         |
| deepcopy_memo              | 52.4 us                                                | 84.2 us: 1.61x slower                                        |
| html5lib                   | 88.9 ms                                                | 147 ms: 1.65x slower                                         |
| django_template            | 44.9 ms                                                | 76.1 ms: 1.69x slower                                        |
| logging_simple             | 9.45 us                                                | 16.1 us: 1.70x slower                                        |
| unpickle_pure_python       | 300 us                                                 | 515 us: 1.72x slower                                         |
| sympy_str                  | 385 ms                                                 | 664 ms: 1.72x slower                                         |
| pprint_pformat             | 1.98 sec                                               | 3.42 sec: 1.73x slower                                       |
| scimark_monte_carlo        | 96.4 ms                                                | 167 ms: 1.74x slower                                         |
| deepcopy_reduce            | 4.04 us                                                | 7.05 us: 1.75x slower                                        |
| genshi_xml                 | 67.6 ms                                                | 118 ms: 1.75x slower                                         |
| richards                   | 60.3 ms                                                | 108 ms: 1.79x slower                                         |
| richards_super             | 72.8 ms                                                | 130 ms: 1.79x slower                                         |
| pprint_safe_repr           | 967 ms                                                 | 1.74 sec: 1.79x slower                                       |
| genshi_text                | 30.2 ms                                                | 54.3 ms: 1.80x slower                                        |
| raytrace                   | 408 ms                                                 | 740 ms: 1.82x slower                                         |
| sqlglot_transpile          | 2.34 ms                                                | 4.25 ms: 1.82x slower                                        |
| logging_format             | 9.59 us                                                | 17.6 us: 1.83x slower                                        |
| logging_silent             | 139 ns                                                 | 262 ns: 1.88x slower                                         |
| mako                       | 15.7 ms                                                | 29.9 ms: 1.90x slower                                        |
| chameleon                  | 9.31 ms                                                | 18.1 ms: 1.94x slower                                        |
| hexiom                     | 8.27 ms                                                | 16.3 ms: 1.97x slower                                        |
| chaos                      | 84.9 ms                                                | 168 ms: 1.98x slower                                         |
| pickle_pure_python         | 436 us                                                 | 872 us: 2.00x slower                                         |
| scimark_lu                 | 152 ms                                                 | 313 ms: 2.06x slower                                         |
| scimark_sor                | 167 ms                                                 | 345 ms: 2.07x slower                                         |
| sympy_sum                  | 222 ms                                                 | 466 ms: 2.10x slower                                         |
| sqlglot_parse              | 1.79 ms                                                | 3.76 ms: 2.10x slower                                        |
| sympy_expand               | 582 ms                                                 | 1.24 sec: 2.14x slower                                       |
| nbody                      | 119 ms                                                 | 267 ms: 2.24x slower                                         |
| flaskblogging              | 7.48 ms                                                | 17.1 ms: 2.29x slower                                        |
| go                         | 172 ms                                                 | 401 ms: 2.33x slower                                         |
| deltablue                  | 4.27 ms                                                | 10.7 ms: 2.51x slower                                        |
| unpack_sequence            | 60.2 ns                                                | 193 ns: 3.20x slower                                         |
| Geometric mean             | (ref)                                                  | 1.37x slower                                                 |

Benchmark hidden because not significant (6): create_gc_cycles, pidigits, pickle_list, unpickle, regex_effbot, unpickle_list
Ignored benchmarks (4) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: dask, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.31x
- 95% likely to have a slowdown of 1.29x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.14x