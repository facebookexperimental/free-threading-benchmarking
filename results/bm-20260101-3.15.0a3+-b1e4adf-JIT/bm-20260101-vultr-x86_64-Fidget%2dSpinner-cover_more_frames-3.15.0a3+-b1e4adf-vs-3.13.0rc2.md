# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: cover_more_frames
- machine: linux-x86_64
- commit hash: b1e4adf
- commit date: 2026-01-01
- overall geometric mean: 1.092x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                          |
| docutils       | 2.62 sec                                                     | 2.68 sec: 1.02x slower                                                        |
| html5lib       | 67.0 ms                                                      | 64.1 ms: 1.05x faster                                                         |
| Geometric mean | (ref)                                                        | 1.02x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 548 ms: 1.60x faster                                                          |
| async_tree_io_tg           | 913 ms                                                       | 580 ms: 1.58x faster                                                          |
| async_tree_memoization     | 461 ms                                                       | 298 ms: 1.54x faster                                                          |
| async_tree_none            | 354 ms                                                       | 237 ms: 1.49x faster                                                          |
| async_tree_none_tg         | 336 ms                                                       | 238 ms: 1.41x faster                                                          |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 476 ms: 1.40x faster                                                          |
| async_tree_memoization_tg  | 414 ms                                                       | 301 ms: 1.38x faster                                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 475 ms: 1.34x faster                                                          |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                          |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                         |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                          |
| Geometric mean             | (ref)                                                        | 1.32x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 57.5 ms: 1.35x faster                                                         |
| nbody          | 85.1 ms                                                      | 73.9 ms: 1.15x faster                                                         |
| pidigits       | 217 ms                                                       | 193 ms: 1.12x faster                                                          |
| Geometric mean | (ref)                                                        | 1.20x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                         |
| regex_compile  | 132 ms                                                       | 120 ms: 1.10x faster                                                          |
| regex_dna      | 180 ms                                                       | 167 ms: 1.08x faster                                                          |
| regex_v8       | 22.7 ms                                                      | 22.3 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                        | 1.08x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                       | 177 us: 1.18x faster                                                          |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.7 ms: 1.13x faster                                                         |
| json_dumps           | 10.5 ms                                                      | 9.36 ms: 1.13x faster                                                         |
| xml_etree_generate   | 85.4 ms                                                      | 77.4 ms: 1.10x faster                                                         |
| xml_etree_process    | 59.3 ms                                                      | 54.8 ms: 1.08x faster                                                         |
| pickle_pure_python   | 294 us                                                       | 275 us: 1.07x faster                                                          |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                          |
| tomli_loads          | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                        |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.08x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.36 ms: 1.00x faster                                                         |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                         |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.6 ms: 1.07x faster                                                         |
| genshi_text     | 21.5 ms                                                      | 20.2 ms: 1.07x faster                                                         |
| genshi_xml      | 48.8 ms                                                      | 49.3 ms: 1.01x slower                                                         |
| django_template | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                         |
| Geometric mean  | (ref)                                                        | 1.02x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 17.9 ms: 2.53x faster                                                         |
| richards_super             | 51.6 ms                                                      | 21.3 ms: 2.43x faster                                                         |
| mdp                        | 2.36 sec                                                     | 1.35 sec: 1.75x faster                                                        |
| async_tree_io              | 876 ms                                                       | 548 ms: 1.60x faster                                                          |
| async_tree_io_tg           | 913 ms                                                       | 580 ms: 1.58x faster                                                          |
| deepcopy_memo              | 39.1 us                                                      | 24.8 us: 1.57x faster                                                         |
| async_tree_memoization     | 461 ms                                                       | 298 ms: 1.54x faster                                                          |
| go                         | 141 ms                                                       | 91.4 ms: 1.54x faster                                                         |
| async_tree_none            | 354 ms                                                       | 237 ms: 1.49x faster                                                          |
| deepcopy                   | 355 us                                                       | 238 us: 1.49x faster                                                          |
| async_tree_none_tg         | 336 ms                                                       | 238 ms: 1.41x faster                                                          |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 476 ms: 1.40x faster                                                          |
| async_tree_memoization_tg  | 414 ms                                                       | 301 ms: 1.38x faster                                                          |
| float                      | 77.5 ms                                                      | 57.5 ms: 1.35x faster                                                         |
| scimark_fft                | 349 ms                                                       | 260 ms: 1.34x faster                                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 475 ms: 1.34x faster                                                          |
| scimark_sor                | 134 ms                                                       | 101 ms: 1.33x faster                                                          |
| spectral_norm              | 111 ms                                                       | 85.8 ms: 1.29x faster                                                         |
| pyflate                    | 449 ms                                                       | 357 ms: 1.26x faster                                                          |
| scimark_monte_carlo        | 65.4 ms                                                      | 52.4 ms: 1.25x faster                                                         |
| logging_silent             | 103 ns                                                       | 83.8 ns: 1.22x faster                                                         |
| deepcopy_reduce            | 3.11 us                                                      | 2.56 us: 1.22x faster                                                         |
| unpickle_pure_python       | 210 us                                                       | 177 us: 1.18x faster                                                          |
| deltablue                  | 3.12 ms                                                      | 2.64 ms: 1.18x faster                                                         |
| pprint_safe_repr           | 738 ms                                                       | 628 ms: 1.17x faster                                                          |
| pprint_pformat             | 1.50 sec                                                     | 1.29 sec: 1.16x faster                                                        |
| nbody                      | 85.1 ms                                                      | 73.9 ms: 1.15x faster                                                         |
| scimark_lu                 | 113 ms                                                       | 98.1 ms: 1.15x faster                                                         |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.7 ms: 1.13x faster                                                         |
| json_dumps                 | 10.5 ms                                                      | 9.36 ms: 1.13x faster                                                         |
| pidigits                   | 217 ms                                                       | 193 ms: 1.12x faster                                                          |
| regex_effbot               | 3.08 ms                                                      | 2.78 ms: 1.11x faster                                                         |
| xml_etree_generate         | 85.4 ms                                                      | 77.4 ms: 1.10x faster                                                         |
| bpe_tokeniser              | 4.45 sec                                                     | 4.04 sec: 1.10x faster                                                        |
| regex_compile              | 132 ms                                                       | 120 ms: 1.10x faster                                                          |
| pathlib                    | 19.2 ms                                                      | 17.5 ms: 1.09x faster                                                         |
| xml_etree_process          | 59.3 ms                                                      | 54.8 ms: 1.08x faster                                                         |
| regex_dna                  | 180 ms                                                       | 167 ms: 1.08x faster                                                          |
| chaos                      | 57.3 ms                                                      | 53.4 ms: 1.07x faster                                                         |
| thrift                     | 778 us                                                       | 727 us: 1.07x faster                                                          |
| mako                       | 11.3 ms                                                      | 10.6 ms: 1.07x faster                                                         |
| pickle_pure_python         | 294 us                                                       | 275 us: 1.07x faster                                                          |
| genshi_text                | 21.5 ms                                                      | 20.2 ms: 1.07x faster                                                         |
| fannkuch                   | 370 ms                                                       | 349 ms: 1.06x faster                                                          |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.44 ms: 1.06x faster                                                         |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                          |
| dulwich_log                | 74.8 ms                                                      | 70.7 ms: 1.06x faster                                                         |
| logging_simple             | 6.16 us                                                      | 5.86 us: 1.05x faster                                                         |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                          |
| html5lib                   | 67.0 ms                                                      | 64.1 ms: 1.05x faster                                                         |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                          |
| logging_format             | 6.84 us                                                      | 6.58 us: 1.04x faster                                                         |
| meteor_contest             | 102 ms                                                       | 98.3 ms: 1.03x faster                                                         |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                         |
| pycparser                  | 1.12 sec                                                     | 1.09 sec: 1.03x faster                                                        |
| crypto_pyaes               | 67.9 ms                                                      | 66.0 ms: 1.03x faster                                                         |
| coverage                   | 83.0 ms                                                      | 80.7 ms: 1.03x faster                                                         |
| regex_v8                   | 22.7 ms                                                      | 22.3 ms: 1.02x faster                                                         |
| tomli_loads                | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                        |
| python_startup_no_site     | 7.39 ms                                                      | 7.36 ms: 1.00x faster                                                         |
| typing_runtime_protocols   | 155 us                                                       | 156 us: 1.01x slower                                                          |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                         |
| genshi_xml                 | 48.8 ms                                                      | 49.3 ms: 1.01x slower                                                         |
| sympy_integrate            | 19.8 ms                                                      | 20.1 ms: 1.01x slower                                                         |
| generators                 | 28.8 ms                                                      | 29.3 ms: 1.02x slower                                                         |
| docutils                   | 2.62 sec                                                     | 2.68 sec: 1.02x slower                                                        |
| django_template            | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                         |
| raytrace                   | 253 ms                                                       | 261 ms: 1.03x slower                                                          |
| json_loads                 | 27.0 us                                                      | 27.9 us: 1.03x slower                                                         |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                          |
| nqueens                    | 78.6 ms                                                      | 84.4 ms: 1.07x slower                                                         |
| sympy_sum                  | 156 ms                                                       | 167 ms: 1.08x slower                                                          |
| sympy_str                  | 275 ms                                                       | 302 ms: 1.10x slower                                                          |
| sympy_expand               | 457 ms                                                       | 508 ms: 1.11x slower                                                          |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                         |
| gc_traversal               | 3.14 ms                                                      | 4.04 ms: 1.28x slower                                                         |
| create_gc_cycles           | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                         |
| bench_thread_pool          | 919 us                                                       | 1.30 ms: 1.42x slower                                                         |
| telco                      | 7.82 ms                                                      | 159 ms: 20.37x slower                                                         |
| bench_mp_pool              | 11.0 ms                                                      | 258 ms: 23.45x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                                  |

Benchmark hidden because not significant (4): pylint, json, sqlite_synth, hexiom
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260101-3.15.0a3+-b1e4adf-JIT/bm-20260101-vultr-x86_64-Fidget%2dSpinner-cover_more_frames-3.15.0a3+-b1e4adf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.092x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.18x