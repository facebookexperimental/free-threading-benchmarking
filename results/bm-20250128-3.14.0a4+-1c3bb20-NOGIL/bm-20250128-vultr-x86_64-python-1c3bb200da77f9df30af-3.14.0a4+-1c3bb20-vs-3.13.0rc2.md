# Results vs. 3.13.0rc2

- fork: python
- ref: 1c3bb200da77f9df30af
- machine: linux-x86_64
- commit hash: 1c3bb20
- commit date: 2025-01-28
- overall geometric mean: 1.107x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 313 ms: 1.20x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.88 sec: 1.10x slower                                                 |
| html5lib       | 67.0 ms                                                      | 73.8 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                        | 1.13x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 587 ms: 1.56x faster                                                   |
| async_tree_io              | 876 ms                                                       | 616 ms: 1.42x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 359 ms: 1.28x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 325 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 512 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 543 ms: 1.23x faster                                                   |
| async_tree_none            | 354 ms                                                       | 294 ms: 1.20x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| async_generators           | 377 ms                                                       | 375 ms: 1.00x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.6 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                   |
| float          | 77.5 ms                                                      | 77.9 ms: 1.01x slower                                                  |
| nbody          | 85.1 ms                                                      | 140 ms: 1.64x slower                                                   |
| Geometric mean | (ref)                                                        | 1.14x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                  |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                                  |
| regex_compile  | 132 ms                                                       | 157 ms: 1.19x slower                                                   |
| Geometric mean | (ref)                                                        | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 89.0 ms: 1.07x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                   |
| json_loads           | 27.0 us                                                      | 31.0 us: 1.15x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 98.7 ms: 1.16x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 70.8 ms: 1.19x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.43 sec: 1.21x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 259 us: 1.23x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 13.1 ms: 1.25x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 382 us: 1.30x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.15x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.60 ms: 1.30x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 61.9 ms: 1.27x slower                                                  |
| django_template | 34.1 ms                                                      | 44.1 ms: 1.29x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 28.5 ms: 1.32x slower                                                  |
| mako            | 11.3 ms                                                      | 16.2 ms: 1.43x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.33x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 587 ms: 1.56x faster                                                   |
| async_tree_io              | 876 ms                                                       | 616 ms: 1.42x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 255 ms: 1.32x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 359 ms: 1.28x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 325 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 512 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 543 ms: 1.23x faster                                                   |
| async_tree_none            | 354 ms                                                       | 294 ms: 1.20x faster                                                   |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                   |
| deepcopy                   | 355 us                                                       | 322 us: 1.10x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.07 us: 1.07x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 89.0 ms: 1.07x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 18.8 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| async_generators           | 377 ms                                                       | 375 ms: 1.00x faster                                                   |
| spectral_norm              | 111 ms                                                       | 111 ms: 1.00x faster                                                   |
| gc_traversal               | 3.14 ms                                                      | 3.16 ms: 1.00x slower                                                  |
| deepcopy_memo              | 39.1 us                                                      | 39.3 us: 1.01x slower                                                  |
| float                      | 77.5 ms                                                      | 77.9 ms: 1.01x slower                                                  |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.37 ms: 1.02x slower                                                  |
| go                         | 141 ms                                                       | 145 ms: 1.03x slower                                                   |
| scimark_sor                | 134 ms                                                       | 139 ms: 1.03x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.6 ms: 1.04x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.30 us: 1.06x slower                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.83 sec: 1.09x slower                                                 |
| json                       | 4.93 ms                                                      | 5.36 ms: 1.09x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.22 sec: 1.09x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.88 sec: 1.10x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 73.8 ms: 1.10x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 84.1 ms: 1.12x slower                                                  |
| telco                      | 7.82 ms                                                      | 8.82 ms: 1.13x slower                                                  |
| scimark_fft                | 349 ms                                                       | 396 ms: 1.13x slower                                                   |
| json_loads                 | 27.0 us                                                      | 31.0 us: 1.15x slower                                                  |
| generators                 | 28.8 ms                                                      | 33.2 ms: 1.15x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 98.7 ms: 1.16x slower                                                  |
| pyflate                    | 449 ms                                                       | 519 ms: 1.16x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 854 ms: 1.16x slower                                                   |
| sqlglot_normalize          | 106 ms                                                       | 124 ms: 1.17x slower                                                   |
| logging_silent             | 103 ns                                                       | 121 ns: 1.17x slower                                                   |
| coverage                   | 83.0 ms                                                      | 97.6 ms: 1.18x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.76 sec: 1.18x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.79 sec: 1.19x slower                                                 |
| regex_compile              | 132 ms                                                       | 157 ms: 1.19x slower                                                   |
| thrift                     | 778 us                                                       | 927 us: 1.19x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 70.8 ms: 1.19x slower                                                  |
| sqlglot_optimize           | 52.7 ms                                                      | 63.1 ms: 1.20x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.40 us: 1.20x slower                                                  |
| 2to3                       | 260 ms                                                       | 313 ms: 1.20x slower                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.43 sec: 1.21x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.72 ms: 1.21x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 190 ms: 1.22x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 259 us: 1.23x slower                                                   |
| logging_format             | 6.84 us                                                      | 8.50 us: 1.24x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 24.7 ms: 1.24x slower                                                  |
| sympy_expand               | 457 ms                                                       | 570 ms: 1.25x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 13.1 ms: 1.25x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 98.1 ms: 1.25x slower                                                  |
| sympy_str                  | 275 ms                                                       | 345 ms: 1.26x slower                                                   |
| scimark_lu                 | 113 ms                                                       | 142 ms: 1.26x slower                                                   |
| chaos                      | 57.3 ms                                                      | 72.4 ms: 1.26x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.97 ms: 1.27x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 7.59 ms: 1.27x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 61.9 ms: 1.27x slower                                                  |
| django_template            | 34.1 ms                                                      | 44.1 ms: 1.29x slower                                                  |
| comprehensions             | 16.5 us                                                      | 21.3 us: 1.29x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 84.5 ms: 1.29x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 382 us: 1.30x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 9.60 ms: 1.30x slower                                                  |
| meteor_contest             | 102 ms                                                       | 132 ms: 1.30x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                      | 1.63 ms: 1.31x slower                                                  |
| richards                   | 45.2 ms                                                      | 59.3 ms: 1.31x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 89.3 ms: 1.32x slower                                                  |
| richards_super             | 51.6 ms                                                      | 68.1 ms: 1.32x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 28.5 ms: 1.32x slower                                                  |
| fannkuch                   | 370 ms                                                       | 490 ms: 1.33x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 205 us: 1.33x slower                                                   |
| raytrace                   | 253 ms                                                       | 341 ms: 1.35x slower                                                   |
| python_startup             | 11.0 ms                                                      | 15.3 ms: 1.39x slower                                                  |
| mako                       | 11.3 ms                                                      | 16.2 ms: 1.43x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 4.83 ms: 1.55x slower                                                  |
| nbody                      | 85.1 ms                                                      | 140 ms: 1.64x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 3.33 ms: 3.62x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 95.2 ms: 8.65x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.16x slower                                                           |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.107x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.35x