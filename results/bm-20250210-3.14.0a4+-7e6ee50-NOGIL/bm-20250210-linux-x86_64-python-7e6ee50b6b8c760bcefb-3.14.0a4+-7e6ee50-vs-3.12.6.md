# Results vs. 3.12.6

- fork: python
- ref: 7e6ee50b6b8c760bcefb
- machine: linux-x86_64
- commit hash: 7e6ee50
- commit date: 2025-02-10
- overall geometric mean: 1.020x slower
- HPT reliability: 99.59%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 530 ms: 1.16x slower                                                   |
| docutils       | 4.00 sec                                               | 4.12 sec: 1.03x slower                                                 |
| html5lib       | 88.9 ms                                                | 93.1 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 772 ms: 2.51x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 835 ms: 2.21x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 348 ms: 2.03x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 496 ms: 1.88x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 528 ms: 1.85x faster                                                   |
| async_tree_none            | 741 ms                                                 | 418 ms: 1.77x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 671 ms: 1.64x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 734 ms: 1.47x faster                                                   |
| async_generators           | 589 ms                                                 | 565 ms: 1.04x faster                                                   |
| coroutines                 | 29.5 ms                                                | 31.4 ms: 1.06x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.59x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 106 ms: 1.16x faster                                                   |
| pidigits       | 250 ms                                                 | 233 ms: 1.07x faster                                                   |
| nbody          | 119 ms                                                 | 179 ms: 1.50x slower                                                   |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.49 ms: 1.14x faster                                                  |
| regex_compile  | 187 ms                                                 | 196 ms: 1.05x slower                                                   |
| regex_dna      | 278 ms                                                 | 296 ms: 1.06x slower                                                   |
| regex_v8       | 32.5 ms                                                | 36.4 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 137 ms: 1.24x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 218 ms: 1.11x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 3.03 sec: 1.05x slower                                                 |
| json_loads           | 37.9 us                                                | 40.1 us: 1.06x slower                                                  |
| xml_etree_generate   | 127 ms                                                 | 137 ms: 1.08x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 326 us: 1.09x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 495 us: 1.14x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 99.8 ms: 1.19x slower                                                  |
| json_dumps           | 14.3 ms                                                | 17.6 ms: 1.23x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.9 ms: 1.13x slower                                                  |
| python_startup         | 23.7 ms                                                | 32.4 ms: 1.37x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 79.4 ms: 1.17x slower                                                  |
| django_template | 44.9 ms                                                | 58.4 ms: 1.30x slower                                                  |
| genshi_text     | 30.2 ms                                                | 40.5 ms: 1.34x slower                                                  |
| mako            | 15.7 ms                                                | 24.2 ms: 1.54x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.33x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 772 ms: 2.51x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 835 ms: 2.21x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 348 ms: 2.03x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 496 ms: 1.88x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 528 ms: 1.85x faster                                                   |
| async_tree_none            | 741 ms                                                 | 418 ms: 1.77x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 671 ms: 1.64x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 3.97 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 734 ms: 1.47x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 137 ms: 1.24x faster                                                   |
| deepcopy                   | 468 us                                                 | 388 us: 1.20x faster                                                   |
| float                      | 123 ms                                                 | 106 ms: 1.16x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.49 ms: 1.14x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.59 sec: 1.13x faster                                                 |
| xml_etree_parse            | 241 ms                                                 | 218 ms: 1.11x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 48.7 us: 1.08x faster                                                  |
| pidigits                   | 250 ms                                                 | 233 ms: 1.07x faster                                                   |
| sqlite_synth               | 3.87 us                                                | 3.61 us: 1.07x faster                                                  |
| async_generators           | 589 ms                                                 | 565 ms: 1.04x faster                                                   |
| docutils                   | 4.00 sec                                               | 4.12 sec: 1.03x slower                                                 |
| deepcopy_reduce            | 4.04 us                                                | 4.22 us: 1.05x slower                                                  |
| html5lib                   | 88.9 ms                                                | 93.1 ms: 1.05x slower                                                  |
| tomli_loads                | 2.88 sec                                               | 3.03 sec: 1.05x slower                                                 |
| regex_compile              | 187 ms                                                 | 196 ms: 1.05x slower                                                   |
| json_loads                 | 37.9 us                                                | 40.1 us: 1.06x slower                                                  |
| coroutines                 | 29.5 ms                                                | 31.4 ms: 1.06x slower                                                  |
| mdp                        | 3.97 sec                                               | 4.22 sec: 1.06x slower                                                 |
| regex_dna                  | 278 ms                                                 | 296 ms: 1.06x slower                                                   |
| scimark_sor                | 167 ms                                                 | 178 ms: 1.07x slower                                                   |
| go                         | 172 ms                                                 | 185 ms: 1.07x slower                                                   |
| sympy_sum                  | 222 ms                                                 | 238 ms: 1.07x slower                                                   |
| sympy_str                  | 385 ms                                                 | 414 ms: 1.07x slower                                                   |
| xml_etree_generate         | 127 ms                                                 | 137 ms: 1.08x slower                                                   |
| logging_simple             | 9.45 us                                                | 10.2 us: 1.08x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 326 us: 1.09x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 82.8 ms: 1.09x slower                                                  |
| nqueens                    | 117 ms                                                 | 128 ms: 1.09x slower                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 7.25 sec: 1.10x slower                                                 |
| sympy_integrate            | 29.8 ms                                                | 33.0 ms: 1.11x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 2.59 ms: 1.11x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 36.4 ms: 1.12x slower                                                  |
| raytrace                   | 408 ms                                                 | 459 ms: 1.13x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 172 ms: 1.13x slower                                                   |
| richards_super             | 72.8 ms                                                | 82.4 ms: 1.13x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 19.9 ms: 1.13x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 3.94 ms: 1.13x slower                                                  |
| chaos                      | 84.9 ms                                                | 96.2 ms: 1.13x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 495 us: 1.14x slower                                                   |
| generators                 | 41.1 ms                                                | 46.8 ms: 1.14x slower                                                  |
| dulwich_log                | 100 ms                                                 | 114 ms: 1.14x slower                                                   |
| logging_format             | 9.59 us                                                | 11.0 us: 1.15x slower                                                  |
| json                       | 6.85 ms                                                | 7.87 ms: 1.15x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.71 ms: 1.15x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.22 ms: 1.15x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 111 ms: 1.16x slower                                                   |
| meteor_contest             | 146 ms                                                 | 170 ms: 1.16x slower                                                   |
| 2to3                       | 456 ms                                                 | 530 ms: 1.16x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.30 sec: 1.16x slower                                                 |
| sqlalchemy_imperative      | 24.7 ms                                                | 28.9 ms: 1.17x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.13 sec: 1.17x slower                                                 |
| sympy_expand               | 582 ms                                                 | 681 ms: 1.17x slower                                                   |
| genshi_xml                 | 67.6 ms                                                | 79.4 ms: 1.17x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 99.8 ms: 1.19x slower                                                  |
| fannkuch                   | 540 ms                                                 | 645 ms: 1.19x slower                                                   |
| typing_runtime_protocols   | 224 us                                                 | 269 us: 1.20x slower                                                   |
| hexiom                     | 8.27 ms                                                | 10.0 ms: 1.21x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 17.6 ms: 1.23x slower                                                  |
| telco                      | 9.59 ms                                                | 11.8 ms: 1.23x slower                                                  |
| richards                   | 60.3 ms                                                | 75.0 ms: 1.24x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.27 ms: 1.27x slower                                                  |
| django_template            | 44.9 ms                                                | 58.4 ms: 1.30x slower                                                  |
| genshi_text                | 30.2 ms                                                | 40.5 ms: 1.34x slower                                                  |
| python_startup             | 23.7 ms                                                | 32.4 ms: 1.37x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.78 ms: 1.44x slower                                                  |
| coverage                   | 95.4 ms                                                | 142 ms: 1.49x slower                                                   |
| nbody                      | 119 ms                                                 | 179 ms: 1.50x slower                                                   |
| deltablue                  | 4.27 ms                                                | 6.49 ms: 1.52x slower                                                  |
| mako                       | 15.7 ms                                                | 24.2 ms: 1.54x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 84.2 ms: 4.07x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (11): pathlib, comprehensions, spectral_norm, sqlglot_normalize, pylint, asyncio_websockets, pyflate, sqlalchemy_declarative, logging_silent, scimark_fft, crypto_pyaes
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.020x slower

# HPT report

- Reliability score: 99.59% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.35x