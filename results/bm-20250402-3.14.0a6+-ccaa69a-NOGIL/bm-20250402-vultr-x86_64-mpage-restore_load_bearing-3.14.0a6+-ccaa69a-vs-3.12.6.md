# Results vs. 3.12.6

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: ccaa69a
- commit date: 2025-04-02
- overall geometric mean: 1.003x slower
- HPT reliability: 97.84%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 289 ms: 1.10x slower                                                  |
| docutils       | 2.64 sec                                               | 2.77 sec: 1.05x slower                                                |
| html5lib       | 63.6 ms                                                | 70.6 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 535 ms: 2.07x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 232 ms: 1.93x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 564 ms: 1.92x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 292 ms: 1.92x faster                                                  |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.74x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 322 ms: 1.72x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 482 ms: 1.50x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                  |
| async_generators           | 384 ms                                                 | 365 ms: 1.05x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.52x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.0 ms: 1.15x faster                                                 |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                  |
| nbody          | 89.3 ms                                                | 113 ms: 1.27x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                 |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                                  |
| regex_dna      | 168 ms                                                 | 182 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.3 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.23 sec: 1.06x slower                                                |
| unpickle_pure_python | 221 us                                                 | 240 us: 1.09x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 343 us: 1.11x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                 |
| json_loads           | 26.5 us                                                | 30.7 us: 1.16x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.3 ms: 1.17x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.2 ms: 1.56x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.6 ms: 1.15x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                 |
| django_template | 34.7 ms                                                | 40.8 ms: 1.18x slower                                                 |
| mako            | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 535 ms: 2.07x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.78 ms: 1.94x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 232 ms: 1.93x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 564 ms: 1.92x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 292 ms: 1.92x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.35 sec: 1.80x faster                                                |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.74x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 322 ms: 1.72x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 482 ms: 1.50x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                  |
| deepcopy                   | 352 us                                                 | 298 us: 1.18x faster                                                  |
| float                      | 80.8 ms                                                | 70.0 ms: 1.15x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.3 ms: 1.11x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 36.6 us: 1.10x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 73.5 ms: 1.07x faster                                                 |
| async_generators           | 384 ms                                                 | 365 ms: 1.05x faster                                                  |
| go                         | 139 ms                                                 | 133 ms: 1.05x faster                                                  |
| spectral_norm              | 110 ms                                                 | 106 ms: 1.04x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.58 sec: 1.03x faster                                                |
| scimark_sor                | 130 ms                                                 | 126 ms: 1.03x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.04 us: 1.01x faster                                                 |
| raytrace                   | 299 ms                                                 | 302 ms: 1.01x slower                                                  |
| scimark_fft                | 342 ms                                                 | 347 ms: 1.02x slower                                                  |
| comprehensions             | 19.8 us                                                | 20.2 us: 1.02x slower                                                 |
| chaos                      | 62.8 ms                                                | 63.9 ms: 1.02x slower                                                 |
| logging_silent             | 109 ns                                                 | 112 ns: 1.03x slower                                                  |
| json                       | 5.02 ms                                                | 5.25 ms: 1.05x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.77 sec: 1.05x slower                                                |
| pyflate                    | 448 ms                                                 | 471 ms: 1.05x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.23 sec: 1.06x slower                                                |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                  |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.72 ms: 1.08x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 802 ms: 1.08x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.18 us: 1.08x slower                                                 |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.08x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 240 us: 1.09x slower                                                  |
| 2to3                       | 264 ms                                                 | 289 ms: 1.10x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.68 sec: 1.10x slower                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 75.6 ms: 1.11x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 158 ms: 1.11x slower                                                  |
| html5lib                   | 63.6 ms                                                | 70.6 ms: 1.11x slower                                                 |
| logging_format             | 7.35 us                                                | 8.16 us: 1.11x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.2 ms: 1.11x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 343 us: 1.11x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 85.8 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 23.1 ms: 1.12x slower                                                 |
| nqueens                    | 80.1 ms                                                | 90.4 ms: 1.13x slower                                                 |
| sympy_str                  | 292 ms                                                 | 331 ms: 1.13x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.01 ms: 1.14x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 57.6 ms: 1.15x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.11 ms: 1.15x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 132 ms: 1.16x slower                                                  |
| json_loads                 | 26.5 us                                                | 30.7 us: 1.16x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.5 ms: 1.16x slower                                                 |
| sympy_expand               | 468 ms                                                 | 544 ms: 1.16x slower                                                  |
| richards                   | 45.9 ms                                                | 53.7 ms: 1.17x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 69.3 ms: 1.17x slower                                                 |
| django_template            | 34.7 ms                                                | 40.8 ms: 1.18x slower                                                 |
| richards_super             | 51.9 ms                                                | 61.5 ms: 1.19x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 197 us: 1.21x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.23x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                 |
| fannkuch                   | 372 ms                                                 | 461 ms: 1.24x slower                                                  |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.24x slower                                                  |
| nbody                      | 89.3 ms                                                | 113 ms: 1.27x slower                                                  |
| telco                      | 6.53 ms                                                | 8.58 ms: 1.31x slower                                                 |
| mako                       | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 11.2 ms: 1.56x slower                                                 |
| coverage                   | 71.4 ms                                                | 113 ms: 1.58x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.15 ms: 3.35x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 96.2 ms: 8.91x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                          |

Benchmark hidden because not significant (4): pylint, generators, asyncio_websockets, pycparser
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250402-3.14.0a6+-ccaa69a-NOGIL/bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.003x slower

# HPT report

- Reliability score: 97.84% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x