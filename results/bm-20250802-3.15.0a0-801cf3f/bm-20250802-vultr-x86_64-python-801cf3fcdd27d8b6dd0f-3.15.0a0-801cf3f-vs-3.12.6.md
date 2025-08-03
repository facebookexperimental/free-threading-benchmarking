# Results vs. 3.12.6

- fork: python
- ref: 801cf3fcdd27d8b6dd0f
- machine: linux-x86_64
- commit hash: 801cf3f
- commit date: 2025-08-02
- overall geometric mean: 1.069x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                |
| html5lib       | 63.6 ms                                                | 60.5 ms: 1.05x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 555 ms                                                 | 305 ms: 1.82x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 612 ms: 1.81x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 603 ms: 1.80x faster                                                  |
| async_tree_none            | 464 ms                                                 | 266 ms: 1.75x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 257 ms: 1.74x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 497 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 497 ms: 1.44x faster                                                  |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 498 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.02x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.5 ms: 1.11x faster                                                 |
| pidigits       | 184 ms                                                 | 213 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                 |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                  |
| regex_v8       | 20.6 ms                                                | 22.4 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.93 sec: 1.09x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.2 ms: 1.05x faster                                                 |
| pickle_dict          | 31.8 us                                                | 30.8 us: 1.03x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 83.2 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 57.8 ms: 1.02x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 303 us: 1.01x faster                                                  |
| unpickle             | 14.1 us                                                | 13.9 us: 1.01x faster                                                 |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                 |
| unpickle_list        | 4.67 us                                                | 4.94 us: 1.06x slower                                                 |
| pickle_list          | 4.77 us                                                | 5.06 us: 1.06x slower                                                 |
| json_loads           | 26.5 us                                                | 28.9 us: 1.09x slower                                                 |
| pickle               | 10.9 us                                                | 12.2 us: 1.12x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.24 ms: 1.01x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.3 ms: 1.12x faster                                                 |
| genshi_xml     | 50.2 ms                                                | 47.8 ms: 1.05x faster                                                 |
| mako           | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.11x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 305 ms: 1.82x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 612 ms: 1.81x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 603 ms: 1.80x faster                                                  |
| async_tree_none            | 464 ms                                                 | 266 ms: 1.75x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 257 ms: 1.74x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 497 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 497 ms: 1.44x faster                                                  |
| deepcopy                   | 352 us                                                 | 253 us: 1.39x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.0 us: 1.39x faster                                                 |
| go                         | 139 ms                                                 | 105 ms: 1.33x faster                                                  |
| unpack_sequence            | 52.1 ns                                                | 39.9 ns: 1.30x faster                                                 |
| comprehensions             | 19.8 us                                                | 15.6 us: 1.27x faster                                                 |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.22x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.1 ms: 1.19x faster                                                 |
| raytrace                   | 299 ms                                                 | 251 ms: 1.19x faster                                                  |
| spectral_norm              | 110 ms                                                 | 92.7 ms: 1.19x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.64 us: 1.17x faster                                                 |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| generators                 | 32.2 ms                                                | 27.9 ms: 1.15x faster                                                 |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.81 us: 1.14x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.16 sec: 1.14x faster                                                |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                  |
| pyflate                    | 448 ms                                                 | 395 ms: 1.13x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.1 ms: 1.13x faster                                                 |
| chaos                      | 62.8 ms                                                | 55.7 ms: 1.13x faster                                                 |
| logging_silent             | 109 ns                                                 | 96.6 ns: 1.13x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 68.1 ms: 1.12x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.3 ms: 1.12x faster                                                 |
| logging_format             | 7.35 us                                                | 6.58 us: 1.12x faster                                                 |
| float                      | 80.8 ms                                                | 72.5 ms: 1.11x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 61.6 ms: 1.11x faster                                                 |
| richards                   | 45.9 ms                                                | 41.5 ms: 1.11x faster                                                 |
| richards_super             | 51.9 ms                                                | 47.2 ms: 1.10x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.93 sec: 1.09x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 682 ms: 1.09x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.40 sec: 1.09x faster                                                |
| hexiom                     | 6.17 ms                                                | 5.69 ms: 1.08x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                  |
| sympy_str                  | 292 ms                                                 | 272 ms: 1.07x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 107 ms: 1.06x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 154 us: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| scimark_fft                | 342 ms                                                 | 324 ms: 1.05x faster                                                  |
| html5lib                   | 63.6 ms                                                | 60.5 ms: 1.05x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 47.8 ms: 1.05x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.28 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 92.2 ms: 1.05x faster                                                 |
| meteor_contest             | 104 ms                                                 | 98.8 ms: 1.05x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 498 ms: 1.04x faster                                                  |
| nqueens                    | 80.1 ms                                                | 77.2 ms: 1.04x faster                                                 |
| pickle_dict                | 31.8 us                                                | 30.8 us: 1.03x faster                                                 |
| thrift                     | 791 us                                                 | 768 us: 1.03x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                |
| xml_etree_generate         | 85.2 ms                                                | 83.2 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 57.8 ms: 1.02x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.02x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 303 us: 1.01x faster                                                  |
| unpickle                   | 14.1 us                                                | 13.9 us: 1.01x faster                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.24 ms: 1.01x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.26 us: 1.03x slower                                                 |
| fannkuch                   | 372 ms                                                 | 384 ms: 1.03x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                 |
| json                       | 5.02 ms                                                | 5.22 ms: 1.04x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.58 ms: 1.04x slower                                                 |
| unpickle_list              | 4.67 us                                                | 4.94 us: 1.06x slower                                                 |
| pickle_list                | 4.77 us                                                | 5.06 us: 1.06x slower                                                 |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.4 ms: 1.09x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.9 us: 1.09x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.11x slower                                                 |
| pickle                     | 10.9 us                                                | 12.2 us: 1.12x slower                                                 |
| coverage                   | 71.4 ms                                                | 81.4 ms: 1.14x slower                                                 |
| pidigits                   | 184 ms                                                 | 213 ms: 1.16x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.36 ms: 1.26x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.96 ms: 1.80x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.50x slower                                                  |
| telco                      | 6.53 ms                                                | 158 ms: 24.23x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (5): django_template, nbody, asyncio_websockets, sympy_expand, asyncio_tcp_ssl
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.069x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x