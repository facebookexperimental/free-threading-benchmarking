# Results vs. 3.13.0rc2

- fork: kumaraditya303
- ref: asyncio_perf
- machine: linux-x86_64
- commit hash: 89e46c7
- commit date: 2025-07-15
- overall geometric mean: 1.051x slower
- HPT reliability: 96.51%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 283 ms: 1.09x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.69 sec: 1.03x slower                                                |
| html5lib       | 67.0 ms                                                      | 65.3 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 514 ms: 1.78x faster                                                  |
| async_tree_io              | 876 ms                                                       | 540 ms: 1.62x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 224 ms: 1.50x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 308 ms: 1.50x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 281 ms: 1.47x faster                                                  |
| async_tree_none            | 354 ms                                                       | 254 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 473 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 499 ms: 1.33x faster                                                  |
| async_generators           | 377 ms                                                       | 363 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.8 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 68.9 ms: 1.12x faster                                                 |
| pidigits       | 217 ms                                                       | 204 ms: 1.06x faster                                                  |
| nbody          | 85.1 ms                                                      | 122 ms: 1.43x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 20.9 ms: 1.09x faster                                                 |
| regex_dna      | 180 ms                                                       | 173 ms: 1.04x faster                                                  |
| regex_compile  | 132 ms                                                       | 143 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.8 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.17 sec: 1.08x slower                                                |
| unpickle_pure_python | 210 us                                                       | 231 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 95.3 ms: 1.12x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 338 us: 1.15x slower                                                  |
| json_loads           | 27.0 us                                                      | 31.1 us: 1.15x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 12.2 ms: 1.15x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 68.6 ms: 1.16x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.37 ms: 1.27x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.8 ms: 1.44x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.35x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 40.1 ms: 1.18x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 58.4 ms: 1.20x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 27.0 ms: 1.25x slower                                                 |
| mako            | 11.3 ms                                                      | 15.5 ms: 1.37x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.25x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.80x faster                                                |
| async_tree_io_tg           | 913 ms                                                       | 514 ms: 1.78x faster                                                  |
| gc_traversal               | 3.14 ms                                                      | 1.87 ms: 1.68x faster                                                 |
| async_tree_io              | 876 ms                                                       | 540 ms: 1.62x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 224 ms: 1.50x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 308 ms: 1.50x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 281 ms: 1.47x faster                                                  |
| async_tree_none            | 354 ms                                                       | 254 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 473 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 499 ms: 1.33x faster                                                  |
| deepcopy                   | 355 us                                                       | 293 us: 1.21x faster                                                  |
| go                         | 141 ms                                                       | 121 ms: 1.17x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 34.6 us: 1.13x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                                 |
| float                      | 77.5 ms                                                      | 68.9 ms: 1.12x faster                                                 |
| scimark_sor                | 134 ms                                                       | 123 ms: 1.09x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 20.9 ms: 1.09x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.04 us: 1.08x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.8 ms: 1.08x faster                                                 |
| pidigits                   | 217 ms                                                       | 204 ms: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| regex_dna                  | 180 ms                                                       | 173 ms: 1.04x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 72.0 ms: 1.04x faster                                                 |
| async_generators           | 377 ms                                                       | 363 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.01 us: 1.03x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 65.3 ms: 1.03x faster                                                 |
| logging_silent             | 103 ns                                                       | 100 ns: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.41 sec: 1.01x faster                                                |
| spectral_norm              | 111 ms                                                       | 111 ms: 1.00x slower                                                  |
| pathlib                    | 19.2 ms                                                      | 19.4 ms: 1.01x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.69 sec: 1.03x slower                                                |
| pyflate                    | 449 ms                                                       | 462 ms: 1.03x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.15 sec: 1.03x slower                                                |
| scimark_fft                | 349 ms                                                       | 363 ms: 1.04x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 774 ms: 1.05x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.8 ms: 1.05x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.35 ms: 1.06x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.59 sec: 1.06x slower                                                |
| comprehensions             | 16.5 us                                                      | 17.6 us: 1.07x slower                                                 |
| json                       | 4.93 ms                                                      | 5.30 ms: 1.08x slower                                                 |
| generators                 | 28.8 ms                                                      | 31.0 ms: 1.08x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.17 sec: 1.08x slower                                                |
| regex_compile              | 132 ms                                                       | 143 ms: 1.08x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.45 ms: 1.08x slower                                                 |
| 2to3                       | 260 ms                                                       | 283 ms: 1.09x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 231 us: 1.10x slower                                                  |
| chaos                      | 57.3 ms                                                      | 63.0 ms: 1.10x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 21.9 ms: 1.11x slower                                                 |
| thrift                     | 778 us                                                       | 866 us: 1.11x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 95.3 ms: 1.12x slower                                                 |
| richards                   | 45.2 ms                                                      | 50.8 ms: 1.12x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.29 ms: 1.12x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 88.7 ms: 1.13x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.55 ms: 1.14x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 128 ms: 1.14x slower                                                  |
| sympy_expand               | 457 ms                                                       | 521 ms: 1.14x slower                                                  |
| sympy_str                  | 275 ms                                                       | 313 ms: 1.14x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.03 us: 1.14x slower                                                 |
| richards_super             | 51.6 ms                                                      | 59.1 ms: 1.14x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 338 us: 1.15x slower                                                  |
| json_loads                 | 27.0 us                                                      | 31.1 us: 1.15x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 179 ms: 1.15x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 12.2 ms: 1.15x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 68.6 ms: 1.16x slower                                                 |
| logging_format             | 6.84 us                                                      | 8.00 us: 1.17x slower                                                 |
| django_template            | 34.1 ms                                                      | 40.1 ms: 1.18x slower                                                 |
| raytrace                   | 253 ms                                                       | 298 ms: 1.18x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 77.2 ms: 1.18x slower                                                 |
| meteor_contest             | 102 ms                                                       | 120 ms: 1.18x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 58.4 ms: 1.20x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 189 us: 1.22x slower                                                  |
| fannkuch                   | 370 ms                                                       | 457 ms: 1.23x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 27.0 ms: 1.25x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 85.9 ms: 1.27x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.37 ms: 1.27x slower                                                 |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.34x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.5 ms: 1.37x slower                                                 |
| nbody                      | 85.1 ms                                                      | 122 ms: 1.43x slower                                                  |
| python_startup             | 11.0 ms                                                      | 15.8 ms: 1.44x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.15 ms: 3.43x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.83x slower                                                  |
| telco                      | 7.82 ms                                                      | 177 ms: 22.67x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.10x slower                                                          |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250715-3.15.0a0-89e46c7-NOGIL/bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.051x slower

# HPT report

- Reliability score: 96.51% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x