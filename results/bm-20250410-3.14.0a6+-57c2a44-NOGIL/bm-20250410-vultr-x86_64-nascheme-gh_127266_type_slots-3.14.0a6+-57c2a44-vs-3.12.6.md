# Results vs. 3.12.6

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 57c2a44
- commit date: 2025-04-10
- overall geometric mean: 1.094x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 316 ms: 1.20x slower                                                     |
| docutils       | 2.64 sec                                               | 2.91 sec: 1.10x slower                                                   |
| html5lib       | 63.6 ms                                                | 76.9 ms: 1.21x slower                                                    |
| Geometric mean | (ref)                                                  | 1.17x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 580 ms: 1.91x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 320 ms: 1.75x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                     |
| async_tree_none            | 464 ms                                                 | 290 ms: 1.60x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 349 ms: 1.59x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 520 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 551 ms: 1.30x faster                                                     |
| async_generators           | 384 ms                                                 | 389 ms: 1.01x slower                                                     |
| coroutines                 | 23.9 ms                                                | 25.6 ms: 1.07x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.41x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 84.0 ms: 1.04x slower                                                    |
| pidigits       | 184 ms                                                 | 202 ms: 1.10x slower                                                     |
| nbody          | 89.3 ms                                                | 152 ms: 1.70x slower                                                     |
| Geometric mean | (ref)                                                  | 1.25x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                    |
| regex_v8       | 20.6 ms                                                | 21.1 ms: 1.02x slower                                                    |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                     |
| regex_compile  | 142 ms                                                 | 173 ms: 1.21x slower                                                     |
| Geometric mean | (ref)                                                  | 1.04x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 92.9 ms: 1.04x faster                                                    |
| json_loads           | 26.5 us                                                | 30.9 us: 1.16x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.19x slower                                                     |
| tomli_loads          | 2.11 sec                                               | 2.62 sec: 1.24x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 74.4 ms: 1.26x slower                                                    |
| json_dumps           | 10.4 ms                                                | 13.1 ms: 1.27x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 282 us: 1.28x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 399 us: 1.30x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.17x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.2 ms: 1.56x slower                                                    |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 45.4 ms: 1.31x slower                                                    |
| genshi_xml      | 50.2 ms                                                | 67.4 ms: 1.34x slower                                                    |
| genshi_text     | 22.8 ms                                                | 31.6 ms: 1.39x slower                                                    |
| mako            | 11.0 ms                                                | 16.6 ms: 1.51x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 580 ms: 1.91x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 1.81 ms: 1.91x faster                                                    |
| async_tree_io              | 1.08 sec                                               | 613 ms: 1.77x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 320 ms: 1.75x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                     |
| mdp                        | 2.42 sec                                               | 1.46 sec: 1.66x faster                                                   |
| async_tree_none            | 464 ms                                                 | 290 ms: 1.60x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 349 ms: 1.59x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 520 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 551 ms: 1.30x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                    |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.07 us: 1.06x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 92.9 ms: 1.04x faster                                                    |
| deepcopy                   | 352 us                                                 | 339 us: 1.04x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 77.7 ms: 1.02x faster                                                    |
| async_generators           | 384 ms                                                 | 389 ms: 1.01x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 21.1 ms: 1.02x slower                                                    |
| float                      | 80.8 ms                                                | 84.0 ms: 1.04x slower                                                    |
| json                       | 5.02 ms                                                | 5.32 ms: 1.06x slower                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 5.02 sec: 1.06x slower                                                   |
| deepcopy_memo              | 40.3 us                                                | 42.8 us: 1.06x slower                                                    |
| coroutines                 | 23.9 ms                                                | 25.6 ms: 1.07x slower                                                    |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                     |
| pycparser                  | 1.17 sec                                               | 1.26 sec: 1.08x slower                                                   |
| pidigits                   | 184 ms                                                 | 202 ms: 1.10x slower                                                     |
| docutils                   | 2.64 sec                                               | 2.91 sec: 1.10x slower                                                   |
| spectral_norm              | 110 ms                                                 | 122 ms: 1.10x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.45 us: 1.12x slower                                                    |
| comprehensions             | 19.8 us                                                | 22.5 us: 1.13x slower                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 163 ms: 1.14x slower                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 25.0 ms: 1.15x slower                                                    |
| go                         | 139 ms                                                 | 161 ms: 1.16x slower                                                     |
| json_loads                 | 26.5 us                                                | 30.9 us: 1.16x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 196 ms: 1.18x slower                                                     |
| raytrace                   | 299 ms                                                 | 356 ms: 1.19x slower                                                     |
| generators                 | 32.2 ms                                                | 38.4 ms: 1.19x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.19x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 24.6 ms: 1.19x slower                                                    |
| 2to3                       | 264 ms                                                 | 316 ms: 1.20x slower                                                     |
| logging_silent             | 109 ns                                                 | 131 ns: 1.20x slower                                                     |
| scimark_fft                | 342 ms                                                 | 412 ms: 1.20x slower                                                     |
| sympy_str                  | 292 ms                                                 | 352 ms: 1.21x slower                                                     |
| html5lib                   | 63.6 ms                                                | 76.9 ms: 1.21x slower                                                    |
| pprint_safe_repr           | 743 ms                                                 | 901 ms: 1.21x slower                                                     |
| regex_compile              | 142 ms                                                 | 173 ms: 1.21x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 94.0 ms: 1.23x slower                                                    |
| chaos                      | 62.8 ms                                                | 77.2 ms: 1.23x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.87 sec: 1.23x slower                                                   |
| pyflate                    | 448 ms                                                 | 553 ms: 1.23x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.62 sec: 1.24x slower                                                   |
| sympy_expand               | 468 ms                                                 | 590 ms: 1.26x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 74.4 ms: 1.26x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 206 us: 1.26x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 13.1 ms: 1.27x slower                                                    |
| logging_simple             | 6.63 us                                                | 8.40 us: 1.27x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.39 ms: 1.27x slower                                                    |
| nqueens                    | 80.1 ms                                                | 102 ms: 1.27x slower                                                     |
| scimark_sor                | 130 ms                                                 | 165 ms: 1.27x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 282 us: 1.28x slower                                                     |
| logging_format             | 7.35 us                                                | 9.47 us: 1.29x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 399 us: 1.30x slower                                                     |
| django_template            | 34.7 ms                                                | 45.4 ms: 1.31x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 91.3 ms: 1.33x slower                                                    |
| hexiom                     | 6.17 ms                                                | 8.25 ms: 1.34x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 153 ms: 1.34x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 67.4 ms: 1.34x slower                                                    |
| deltablue                  | 3.45 ms                                                | 4.64 ms: 1.35x slower                                                    |
| richards_super             | 51.9 ms                                                | 70.1 ms: 1.35x slower                                                    |
| richards                   | 45.9 ms                                                | 62.1 ms: 1.35x slower                                                    |
| meteor_contest             | 104 ms                                                 | 140 ms: 1.35x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 6.04 ms: 1.38x slower                                                    |
| telco                      | 6.53 ms                                                | 9.00 ms: 1.38x slower                                                    |
| genshi_text                | 22.8 ms                                                | 31.6 ms: 1.39x slower                                                    |
| fannkuch                   | 372 ms                                                 | 542 ms: 1.46x slower                                                     |
| mako                       | 11.0 ms                                                | 16.6 ms: 1.51x slower                                                    |
| coverage                   | 71.4 ms                                                | 111 ms: 1.55x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 11.2 ms: 1.56x slower                                                    |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                    |
| nbody                      | 89.3 ms                                                | 152 ms: 1.70x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 3.20 ms: 3.40x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 98.6 ms: 9.13x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.15x slower                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250410-3.14.0a6+-57c2a44-NOGIL/bm-20250410-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-57c2a44.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.094x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.38x