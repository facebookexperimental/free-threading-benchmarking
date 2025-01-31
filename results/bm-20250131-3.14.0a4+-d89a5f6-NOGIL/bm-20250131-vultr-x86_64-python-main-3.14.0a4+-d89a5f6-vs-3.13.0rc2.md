# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d89a5f6
- commit date: 2025-01-31
- overall geometric mean: 1.057x slower
- HPT reliability: 99.93%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 296 ms: 1.14x slower                                   |
| docutils       | 2.62 sec                                                     | 2.75 sec: 1.05x slower                                 |
| html5lib       | 67.0 ms                                                      | 69.4 ms: 1.04x slower                                  |
| Geometric mean | (ref)                                                        | 1.07x slower                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 559 ms: 1.63x faster                                   |
| async_tree_io              | 876 ms                                                       | 597 ms: 1.47x faster                                   |
| async_tree_memoization     | 461 ms                                                       | 345 ms: 1.34x faster                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                   |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 495 ms: 1.29x faster                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 529 ms: 1.26x faster                                   |
| async_tree_none            | 354 ms                                                       | 282 ms: 1.25x faster                                   |
| coroutines                 | 23.6 ms                                                      | 22.6 ms: 1.04x faster                                  |
| async_generators           | 377 ms                                                       | 368 ms: 1.03x faster                                   |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                   |
| Geometric mean             | (ref)                                                        | 1.26x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 197 ms: 1.10x faster                                   |
| float          | 77.5 ms                                                      | 73.9 ms: 1.05x faster                                  |
| nbody          | 85.1 ms                                                      | 126 ms: 1.48x slower                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                  |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                   |
| regex_v8       | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                  |
| regex_compile  | 132 ms                                                       | 145 ms: 1.10x slower                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.3 ms: 1.09x faster                                  |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                   |
| xml_etree_generate   | 85.4 ms                                                      | 94.9 ms: 1.11x slower                                  |
| tomli_loads          | 2.01 sec                                                     | 2.26 sec: 1.12x slower                                 |
| xml_etree_process    | 59.3 ms                                                      | 67.4 ms: 1.14x slower                                  |
| unpickle_pure_python | 210 us                                                       | 241 us: 1.15x slower                                   |
| json_loads           | 27.0 us                                                      | 31.4 us: 1.16x slower                                  |
| json_dumps           | 10.5 ms                                                      | 12.6 ms: 1.20x slower                                  |
| pickle_pure_python   | 294 us                                                       | 356 us: 1.21x slower                                   |
| Geometric mean       | (ref)                                                        | 1.10x slower                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.61 ms: 1.30x slower                                  |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                  |
| Geometric mean         | (ref)                                                        | 1.35x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 57.5 ms: 1.18x slower                                  |
| django_template | 34.1 ms                                                      | 40.7 ms: 1.19x slower                                  |
| genshi_text     | 21.5 ms                                                      | 26.8 ms: 1.25x slower                                  |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                  |
| Geometric mean  | (ref)                                                        | 1.25x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| gc_traversal               | 3.14 ms                                                      | 1.64 ms: 1.91x faster                                  |
| async_tree_io_tg           | 913 ms                                                       | 559 ms: 1.63x faster                                   |
| async_tree_io              | 876 ms                                                       | 597 ms: 1.47x faster                                   |
| async_tree_memoization     | 461 ms                                                       | 345 ms: 1.34x faster                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                   |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 495 ms: 1.29x faster                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 529 ms: 1.26x faster                                   |
| async_tree_none            | 354 ms                                                       | 282 ms: 1.25x faster                                   |
| deepcopy                   | 355 us                                                       | 300 us: 1.18x faster                                   |
| regex_effbot               | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                  |
| pidigits                   | 217 ms                                                       | 197 ms: 1.10x faster                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.3 ms: 1.09x faster                                  |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.08x faster                                  |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                   |
| spectral_norm              | 111 ms                                                       | 105 ms: 1.06x faster                                   |
| go                         | 141 ms                                                       | 133 ms: 1.06x faster                                   |
| deepcopy_memo              | 39.1 us                                                      | 36.9 us: 1.06x faster                                  |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                  |
| float                      | 77.5 ms                                                      | 73.9 ms: 1.05x faster                                  |
| scimark_sor                | 134 ms                                                       | 128 ms: 1.05x faster                                   |
| coroutines                 | 23.6 ms                                                      | 22.6 ms: 1.04x faster                                  |
| async_generators           | 377 ms                                                       | 368 ms: 1.03x faster                                   |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                   |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.37 ms: 1.02x slower                                  |
| pycparser                  | 1.12 sec                                                     | 1.16 sec: 1.03x slower                                 |
| html5lib                   | 67.0 ms                                                      | 69.4 ms: 1.04x slower                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.61 sec: 1.04x slower                                 |
| regex_v8                   | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                  |
| docutils                   | 2.62 sec                                                     | 2.75 sec: 1.05x slower                                 |
| pprint_safe_repr           | 738 ms                                                       | 778 ms: 1.05x slower                                   |
| pyflate                    | 449 ms                                                       | 476 ms: 1.06x slower                                   |
| generators                 | 28.8 ms                                                      | 30.6 ms: 1.06x slower                                  |
| logging_silent             | 103 ns                                                       | 109 ns: 1.06x slower                                   |
| dulwich_log                | 74.8 ms                                                      | 80.3 ms: 1.07x slower                                  |
| scimark_fft                | 349 ms                                                       | 375 ms: 1.07x slower                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.61 sec: 1.08x slower                                 |
| telco                      | 7.82 ms                                                      | 8.44 ms: 1.08x slower                                  |
| json                       | 4.93 ms                                                      | 5.38 ms: 1.09x slower                                  |
| regex_compile              | 132 ms                                                       | 145 ms: 1.10x slower                                   |
| sqlglot_normalize          | 106 ms                                                       | 116 ms: 1.10x slower                                   |
| xml_etree_generate         | 85.4 ms                                                      | 94.9 ms: 1.11x slower                                  |
| tomli_loads                | 2.01 sec                                                     | 2.26 sec: 1.12x slower                                 |
| mdp                        | 2.36 sec                                                     | 2.65 sec: 1.13x slower                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 59.7 ms: 1.13x slower                                  |
| xml_etree_process          | 59.3 ms                                                      | 67.4 ms: 1.14x slower                                  |
| 2to3                       | 260 ms                                                       | 296 ms: 1.14x slower                                   |
| logging_simple             | 6.16 us                                                      | 7.02 us: 1.14x slower                                  |
| unpickle_pure_python       | 210 us                                                       | 241 us: 1.15x slower                                   |
| thrift                     | 778 us                                                       | 898 us: 1.15x slower                                   |
| logging_format             | 6.84 us                                                      | 7.96 us: 1.16x slower                                  |
| json_loads                 | 27.0 us                                                      | 31.4 us: 1.16x slower                                  |
| chaos                      | 57.3 ms                                                      | 66.8 ms: 1.17x slower                                  |
| coverage                   | 83.0 ms                                                      | 97.0 ms: 1.17x slower                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.53 ms: 1.17x slower                                  |
| sympy_sum                  | 156 ms                                                       | 183 ms: 1.17x slower                                   |
| genshi_xml                 | 48.8 ms                                                      | 57.5 ms: 1.18x slower                                  |
| comprehensions             | 16.5 us                                                      | 19.4 us: 1.18x slower                                  |
| sympy_expand               | 457 ms                                                       | 541 ms: 1.18x slower                                   |
| sqlglot_transpile          | 1.56 ms                                                      | 1.85 ms: 1.19x slower                                  |
| scimark_lu                 | 113 ms                                                       | 134 ms: 1.19x slower                                   |
| sympy_integrate            | 19.8 ms                                                      | 23.6 ms: 1.19x slower                                  |
| sympy_str                  | 275 ms                                                       | 327 ms: 1.19x slower                                   |
| django_template            | 34.1 ms                                                      | 40.7 ms: 1.19x slower                                  |
| nqueens                    | 78.6 ms                                                      | 93.8 ms: 1.19x slower                                  |
| hexiom                     | 5.99 ms                                                      | 7.16 ms: 1.20x slower                                  |
| json_dumps                 | 10.5 ms                                                      | 12.6 ms: 1.20x slower                                  |
| richards                   | 45.2 ms                                                      | 54.4 ms: 1.20x slower                                  |
| pickle_pure_python         | 294 us                                                       | 356 us: 1.21x slower                                   |
| sqlglot_parse              | 1.25 ms                                                      | 1.53 ms: 1.22x slower                                  |
| richards_super             | 51.6 ms                                                      | 63.3 ms: 1.23x slower                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 80.5 ms: 1.23x slower                                  |
| genshi_text                | 21.5 ms                                                      | 26.8 ms: 1.25x slower                                  |
| typing_runtime_protocols   | 155 us                                                       | 193 us: 1.25x slower                                   |
| raytrace                   | 253 ms                                                       | 317 ms: 1.25x slower                                   |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                   |
| crypto_pyaes               | 67.9 ms                                                      | 87.3 ms: 1.29x slower                                  |
| fannkuch                   | 370 ms                                                       | 480 ms: 1.30x slower                                   |
| python_startup_no_site     | 7.39 ms                                                      | 9.61 ms: 1.30x slower                                  |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                  |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                  |
| deltablue                  | 3.12 ms                                                      | 4.57 ms: 1.46x slower                                  |
| nbody                      | 85.1 ms                                                      | 126 ms: 1.48x slower                                   |
| bench_thread_pool          | 919 us                                                       | 3.31 ms: 3.60x slower                                  |
| bench_mp_pool              | 11.0 ms                                                      | 91.7 ms: 8.34x slower                                  |
| Geometric mean             | (ref)                                                        | 1.10x slower                                           |

Benchmark hidden because not significant (2): pylint, deepcopy_reduce
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250131-3.14.0a4+-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.057x slower

# HPT report

- Reliability score: 99.93% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.34x