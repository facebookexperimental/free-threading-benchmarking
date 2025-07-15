# Results vs. 3.12.6

- fork: kumaraditya303
- ref: asyncio_perf
- machine: linux-x86_64
- commit hash: 89e46c7
- commit date: 2025-07-15
- overall geometric mean: 1.018x slower
- HPT reliability: 91.11%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 283 ms: 1.07x slower                                                  |
| docutils       | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 514 ms: 2.16x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 540 ms: 2.01x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 224 ms: 1.99x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 281 ms: 1.99x faster                                                  |
| async_tree_none            | 464 ms                                                 | 254 ms: 1.83x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 473 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                  |
| async_generators           | 384 ms                                                 | 363 ms: 1.06x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.8 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.9 ms: 1.17x faster                                                 |
| pidigits       | 184 ms                                                 | 204 ms: 1.11x slower                                                  |
| nbody          | 89.3 ms                                                | 122 ms: 1.37x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                 |
| regex_compile  | 142 ms                                                 | 143 ms: 1.00x slower                                                  |
| regex_v8       | 20.6 ms                                                | 20.9 ms: 1.01x slower                                                 |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.8 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.17 sec: 1.03x slower                                                |
| unpickle_pure_python | 221 us                                                 | 231 us: 1.05x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 338 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.3 ms: 1.12x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.6 ms: 1.16x slower                                                 |
| json_loads           | 26.5 us                                                | 31.1 us: 1.17x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.2 ms: 1.17x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.37 ms: 1.31x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 40.1 ms: 1.16x slower                                                 |
| genshi_xml      | 50.2 ms                                                | 58.4 ms: 1.16x slower                                                 |
| genshi_text     | 22.8 ms                                                | 27.0 ms: 1.18x slower                                                 |
| mako            | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 514 ms: 2.16x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 540 ms: 2.01x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 224 ms: 1.99x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 281 ms: 1.99x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                |
| gc_traversal               | 3.46 ms                                                | 1.87 ms: 1.85x faster                                                 |
| async_tree_none            | 464 ms                                                 | 254 ms: 1.83x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 308 ms: 1.80x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 473 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                  |
| deepcopy                   | 352 us                                                 | 293 us: 1.20x faster                                                  |
| float                      | 80.8 ms                                                | 68.9 ms: 1.17x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 34.6 us: 1.16x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                 |
| go                         | 139 ms                                                 | 121 ms: 1.16x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.8 ms: 1.10x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 72.0 ms: 1.10x faster                                                 |
| logging_silent             | 109 ns                                                 | 100 ns: 1.09x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.41 sec: 1.07x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| async_generators           | 384 ms                                                 | 363 ms: 1.06x faster                                                  |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                                  |
| generators                 | 32.2 ms                                                | 31.0 ms: 1.04x faster                                                 |
| pylint                     | 319 ms                                                 | 307 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.01 us: 1.02x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.01x faster                                                |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| chaos                      | 62.8 ms                                                | 63.0 ms: 1.00x slower                                                 |
| regex_compile              | 142 ms                                                 | 143 ms: 1.00x slower                                                  |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 20.9 ms: 1.01x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                |
| html5lib                   | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.17 sec: 1.03x slower                                                |
| hexiom                     | 6.17 ms                                                | 6.35 ms: 1.03x slower                                                 |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.55 ms: 1.03x slower                                                 |
| pyflate                    | 448 ms                                                 | 462 ms: 1.03x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.8 ms: 1.04x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 774 ms: 1.04x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 231 us: 1.05x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.59 sec: 1.05x slower                                                |
| json                       | 5.02 ms                                                | 5.30 ms: 1.06x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.03 us: 1.06x slower                                                 |
| scimark_fft                | 342 ms                                                 | 363 ms: 1.06x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                 |
| 2to3                       | 264 ms                                                 | 283 ms: 1.07x slower                                                  |
| sympy_str                  | 292 ms                                                 | 313 ms: 1.07x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 179 ms: 1.08x slower                                                  |
| logging_format             | 7.35 us                                                | 8.00 us: 1.09x slower                                                 |
| thrift                     | 791 us                                                 | 866 us: 1.09x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 338 us: 1.10x slower                                                  |
| richards                   | 45.9 ms                                                | 50.8 ms: 1.11x slower                                                 |
| pidigits                   | 184 ms                                                 | 204 ms: 1.11x slower                                                  |
| nqueens                    | 80.1 ms                                                | 88.7 ms: 1.11x slower                                                 |
| sympy_expand               | 468 ms                                                 | 521 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 95.3 ms: 1.12x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 85.9 ms: 1.12x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 128 ms: 1.12x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 77.2 ms: 1.13x slower                                                 |
| richards_super             | 51.9 ms                                                | 59.1 ms: 1.14x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 189 us: 1.16x slower                                                  |
| django_template            | 34.7 ms                                                | 40.1 ms: 1.16x slower                                                 |
| meteor_contest             | 104 ms                                                 | 120 ms: 1.16x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 58.4 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 68.6 ms: 1.16x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.1 us: 1.17x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.2 ms: 1.17x slower                                                 |
| genshi_text                | 22.8 ms                                                | 27.0 ms: 1.18x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.29 ms: 1.20x slower                                                 |
| fannkuch                   | 372 ms                                                 | 457 ms: 1.23x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.37 ms: 1.31x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.45 ms: 1.33x slower                                                 |
| nbody                      | 89.3 ms                                                | 122 ms: 1.37x slower                                                  |
| mako                       | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| coverage                   | 71.4 ms                                                | 111 ms: 1.55x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.15 ms: 3.35x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.01x slower                                                 |
| telco                      | 6.53 ms                                                | 177 ms: 27.17x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                          |

Benchmark hidden because not significant (1): raytrace
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250715-3.15.0a0-89e46c7-NOGIL/bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.018x slower

# HPT report

- Reliability score: 91.11% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x