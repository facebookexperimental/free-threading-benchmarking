# Results vs. 3.12.6

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 395a6d3
- commit date: 2025-04-01
- overall geometric mean: 1.112x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 248 ms: 1.06x faster                                                     |
| docutils       | 2.64 sec                                               | 2.51 sec: 1.05x faster                                                   |
| Geometric mean | (ref)                                                  | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.80x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 623 ms: 1.78x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 610 ms: 1.77x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                     |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                     |
| async_generators           | 384 ms                                                 | 327 ms: 1.18x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.7 ms: 1.05x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.6 ms: 1.13x faster                                                    |
| pidigits       | 184 ms                                                 | 196 ms: 1.06x slower                                                     |
| nbody          | 89.3 ms                                                | 97.2 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                  | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.61 ms: 1.21x faster                                                    |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                     |
| regex_dna      | 168 ms                                                 | 167 ms: 1.01x faster                                                     |
| regex_v8       | 20.6 ms                                                | 21.9 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                  | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.94 sec: 1.08x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 91.3 ms: 1.06x faster                                                    |
| unpickle_pure_python | 221 us                                                 | 211 us: 1.05x faster                                                     |
| pickle_pure_python   | 308 us                                                 | 302 us: 1.02x faster                                                     |
| xml_etree_generate   | 85.2 ms                                                | 83.8 ms: 1.02x faster                                                    |
| xml_etree_process    | 59.0 ms                                                | 58.1 ms: 1.02x faster                                                    |
| json_loads           | 26.5 us                                                | 27.0 us: 1.02x slower                                                    |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.58 ms: 1.20x slower                                                    |
| python_startup         | 9.93 ms                                                | 14.9 ms: 1.50x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.34x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                    |
| genshi_xml      | 50.2 ms                                                | 47.7 ms: 1.05x faster                                                    |
| django_template | 34.7 ms                                                | 34.5 ms: 1.00x faster                                                    |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.17 sec: 2.07x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 310 ms: 1.80x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 623 ms: 1.78x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 610 ms: 1.77x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 256 ms: 1.74x faster                                                     |
| async_tree_none            | 464 ms                                                 | 270 ms: 1.72x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 491 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                     |
| deepcopy                   | 352 us                                                 | 253 us: 1.39x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 29.4 us: 1.37x faster                                                    |
| go                         | 139 ms                                                 | 111 ms: 1.26x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.61 ms: 1.21x faster                                                    |
| comprehensions             | 19.8 us                                                | 16.4 us: 1.21x faster                                                    |
| generators                 | 32.2 ms                                                | 26.7 ms: 1.21x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 65.5 ms: 1.20x faster                                                    |
| logging_silent             | 109 ns                                                 | 92.1 ns: 1.18x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.61 us: 1.18x faster                                                    |
| spectral_norm              | 110 ms                                                 | 93.6 ms: 1.18x faster                                                    |
| async_generators           | 384 ms                                                 | 327 ms: 1.18x faster                                                     |
| raytrace                   | 299 ms                                                 | 255 ms: 1.17x faster                                                     |
| deltablue                  | 3.45 ms                                                | 2.97 ms: 1.16x faster                                                    |
| pylint                     | 319 ms                                                 | 275 ms: 1.16x faster                                                     |
| scimark_sor                | 130 ms                                                 | 112 ms: 1.16x faster                                                     |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.2 ms: 1.13x faster                                                    |
| chaos                      | 62.8 ms                                                | 55.5 ms: 1.13x faster                                                    |
| crypto_pyaes               | 76.6 ms                                                | 67.7 ms: 1.13x faster                                                    |
| float                      | 80.8 ms                                                | 71.6 ms: 1.13x faster                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 127 ms: 1.13x faster                                                     |
| richards                   | 45.9 ms                                                | 40.9 ms: 1.12x faster                                                    |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                                    |
| genshi_text                | 22.8 ms                                                | 20.4 ms: 1.12x faster                                                    |
| richards_super             | 51.9 ms                                                | 46.4 ms: 1.12x faster                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.25 sec: 1.11x faster                                                   |
| logging_format             | 7.35 us                                                | 6.63 us: 1.11x faster                                                    |
| logging_simple             | 6.63 us                                                | 6.00 us: 1.10x faster                                                    |
| pyflate                    | 448 ms                                                 | 409 ms: 1.09x faster                                                     |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                    |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.09x faster                                                     |
| sympy_str                  | 292 ms                                                 | 269 ms: 1.08x faster                                                     |
| tomli_loads                | 2.11 sec                                               | 1.94 sec: 1.08x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 151 us: 1.08x faster                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 63.4 ms: 1.08x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                     |
| scimark_fft                | 342 ms                                                 | 320 ms: 1.07x faster                                                     |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.06x faster                                                   |
| 2to3                       | 264 ms                                                 | 248 ms: 1.06x faster                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 702 ms: 1.06x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 91.3 ms: 1.06x faster                                                    |
| coroutines                 | 23.9 ms                                                | 22.7 ms: 1.05x faster                                                    |
| hexiom                     | 6.17 ms                                                | 5.86 ms: 1.05x faster                                                    |
| genshi_xml                 | 50.2 ms                                                | 47.7 ms: 1.05x faster                                                    |
| docutils                   | 2.64 sec                                               | 2.51 sec: 1.05x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 211 us: 1.05x faster                                                     |
| json                       | 5.02 ms                                                | 4.82 ms: 1.04x faster                                                    |
| scimark_lu                 | 114 ms                                                 | 110 ms: 1.04x faster                                                     |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                     |
| nqueens                    | 80.1 ms                                                | 77.9 ms: 1.03x faster                                                    |
| sympy_expand               | 468 ms                                                 | 456 ms: 1.03x faster                                                     |
| pickle_pure_python         | 308 us                                                 | 302 us: 1.02x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.17 us: 1.02x faster                                                    |
| xml_etree_generate         | 85.2 ms                                                | 83.8 ms: 1.02x faster                                                    |
| xml_etree_process          | 59.0 ms                                                | 58.1 ms: 1.02x faster                                                    |
| regex_dna                  | 168 ms                                                 | 167 ms: 1.01x faster                                                     |
| django_template            | 34.7 ms                                                | 34.5 ms: 1.00x faster                                                    |
| json_loads                 | 26.5 us                                                | 27.0 us: 1.02x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.49 ms: 1.02x slower                                                    |
| fannkuch                   | 372 ms                                                 | 391 ms: 1.05x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 21.9 ms: 1.06x slower                                                    |
| pidigits                   | 184 ms                                                 | 196 ms: 1.06x slower                                                     |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                    |
| nbody                      | 89.3 ms                                                | 97.2 ms: 1.09x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.10x slower                                                    |
| coverage                   | 71.4 ms                                                | 78.8 ms: 1.10x slower                                                    |
| telco                      | 6.53 ms                                                | 7.26 ms: 1.11x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 8.58 ms: 1.20x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 4.60 ms: 1.33x slower                                                    |
| python_startup             | 9.93 ms                                                | 14.9 ms: 1.50x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.70x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 88.4 ms: 8.19x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250401-3.14.0a6+-395a6d3/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-395a6d3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.112x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.13x