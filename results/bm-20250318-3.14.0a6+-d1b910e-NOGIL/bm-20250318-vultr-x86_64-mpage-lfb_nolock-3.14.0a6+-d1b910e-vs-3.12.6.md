# Results vs. 3.12.6

- fork: mpage
- ref: lfb_nolock
- machine: linux-x86_64
- commit hash: d1b910e
- commit date: 2025-03-18
- overall geometric mean: 1.009x slower
- HPT reliability: 98.83%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 289 ms: 1.10x slower                                        |
| docutils       | 2.64 sec                                               | 2.75 sec: 1.04x slower                                      |
| html5lib       | 63.6 ms                                                | 69.8 ms: 1.10x slower                                       |
| Geometric mean | (ref)                                                  | 1.08x slower                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 524 ms: 2.12x faster                                        |
| async_tree_none_tg         | 446 ms                                                 | 226 ms: 1.97x faster                                        |
| async_tree_io              | 1.08 sec                                               | 553 ms: 1.96x faster                                        |
| async_tree_memoization_tg  | 560 ms                                                 | 291 ms: 1.92x faster                                        |
| async_tree_none            | 464 ms                                                 | 263 ms: 1.77x faster                                        |
| async_tree_memoization     | 555 ms                                                 | 322 ms: 1.72x faster                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 476 ms: 1.52x faster                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 508 ms: 1.41x faster                                        |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                        |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.02x faster                                       |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 80.8 ms                                                | 67.3 ms: 1.20x faster                                       |
| pidigits       | 184 ms                                                 | 196 ms: 1.06x slower                                        |
| nbody          | 89.3 ms                                                | 114 ms: 1.28x slower                                        |
| Geometric mean | (ref)                                                  | 1.04x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.63 ms: 1.20x faster                                       |
| regex_v8       | 20.6 ms                                                | 21.5 ms: 1.04x slower                                       |
| regex_dna      | 168 ms                                                 | 177 ms: 1.06x slower                                        |
| regex_compile  | 142 ms                                                 | 152 ms: 1.07x slower                                        |
| Geometric mean | (ref)                                                  | 1.01x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.6 ms: 1.10x faster                                       |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                        |
| tomli_loads          | 2.11 sec                                               | 2.22 sec: 1.06x slower                                      |
| unpickle_pure_python | 221 us                                                 | 243 us: 1.10x slower                                        |
| json_loads           | 26.5 us                                                | 29.3 us: 1.10x slower                                       |
| pickle_pure_python   | 308 us                                                 | 346 us: 1.12x slower                                        |
| xml_etree_generate   | 85.2 ms                                                | 96.9 ms: 1.14x slower                                       |
| xml_etree_process    | 59.0 ms                                                | 68.3 ms: 1.16x slower                                       |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.23x slower                                       |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                       |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                       |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.9 ms: 1.15x slower                                       |
| genshi_text     | 22.8 ms                                                | 27.0 ms: 1.18x slower                                       |
| django_template | 34.7 ms                                                | 42.0 ms: 1.21x slower                                       |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                       |
| Geometric mean  | (ref)                                                  | 1.24x slower                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 524 ms: 2.12x faster                                        |
| async_tree_none_tg         | 446 ms                                                 | 226 ms: 1.97x faster                                        |
| async_tree_io              | 1.08 sec                                               | 553 ms: 1.96x faster                                        |
| gc_traversal               | 3.46 ms                                                | 1.78 ms: 1.94x faster                                       |
| async_tree_memoization_tg  | 560 ms                                                 | 291 ms: 1.92x faster                                        |
| async_tree_none            | 464 ms                                                 | 263 ms: 1.77x faster                                        |
| async_tree_memoization     | 555 ms                                                 | 322 ms: 1.72x faster                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 476 ms: 1.52x faster                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 508 ms: 1.41x faster                                        |
| regex_effbot               | 3.17 ms                                                | 2.63 ms: 1.20x faster                                       |
| float                      | 80.8 ms                                                | 67.3 ms: 1.20x faster                                       |
| deepcopy                   | 352 us                                                 | 300 us: 1.17x faster                                        |
| sqlite_synth               | 2.20 us                                                | 1.99 us: 1.11x faster                                       |
| pathlib                    | 21.5 ms                                                | 19.5 ms: 1.10x faster                                       |
| xml_etree_iterparse        | 96.7 ms                                                | 87.6 ms: 1.10x faster                                       |
| deepcopy_memo              | 40.3 us                                                | 36.9 us: 1.09x faster                                       |
| dulwich_log                | 78.9 ms                                                | 72.7 ms: 1.08x faster                                       |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                        |
| go                         | 139 ms                                                 | 130 ms: 1.07x faster                                        |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                      |
| bpe_tokeniser              | 4.74 sec                                               | 4.61 sec: 1.03x faster                                      |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                        |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                        |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.02x faster                                       |
| scimark_sor                | 130 ms                                                 | 128 ms: 1.01x faster                                        |
| raytrace                   | 299 ms                                                 | 301 ms: 1.01x slower                                        |
| deepcopy_reduce            | 3.08 us                                                | 3.10 us: 1.01x slower                                       |
| logging_silent             | 109 ns                                                 | 111 ns: 1.02x slower                                        |
| comprehensions             | 19.8 us                                                | 20.4 us: 1.03x slower                                       |
| docutils                   | 2.64 sec                                               | 2.75 sec: 1.04x slower                                      |
| regex_v8                   | 20.6 ms                                                | 21.5 ms: 1.04x slower                                       |
| chaos                      | 62.8 ms                                                | 65.5 ms: 1.04x slower                                       |
| deltablue                  | 3.45 ms                                                | 3.59 ms: 1.04x slower                                       |
| generators                 | 32.2 ms                                                | 34.0 ms: 1.05x slower                                       |
| tomli_loads                | 2.11 sec                                               | 2.22 sec: 1.06x slower                                      |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.06x slower                                        |
| scimark_fft                | 342 ms                                                 | 363 ms: 1.06x slower                                        |
| pidigits                   | 184 ms                                                 | 196 ms: 1.06x slower                                        |
| logging_simple             | 6.63 us                                                | 7.05 us: 1.06x slower                                       |
| regex_compile              | 142 ms                                                 | 152 ms: 1.07x slower                                        |
| pyflate                    | 448 ms                                                 | 480 ms: 1.07x slower                                        |
| pprint_safe_repr           | 743 ms                                                 | 799 ms: 1.08x slower                                        |
| thrift                     | 791 us                                                 | 853 us: 1.08x slower                                        |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.6 ms: 1.08x slower                                       |
| pprint_pformat             | 1.52 sec                                               | 1.66 sec: 1.09x slower                                      |
| 2to3                       | 264 ms                                                 | 289 ms: 1.10x slower                                        |
| html5lib                   | 63.6 ms                                                | 69.8 ms: 1.10x slower                                       |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                        |
| unpickle_pure_python       | 221 us                                                 | 243 us: 1.10x slower                                        |
| json_loads                 | 26.5 us                                                | 29.3 us: 1.10x slower                                       |
| crypto_pyaes               | 76.6 ms                                                | 84.6 ms: 1.10x slower                                       |
| logging_format             | 7.35 us                                                | 8.11 us: 1.10x slower                                       |
| scimark_monte_carlo        | 68.4 ms                                                | 75.8 ms: 1.11x slower                                       |
| sympy_sum                  | 166 ms                                                 | 184 ms: 1.11x slower                                        |
| richards                   | 45.9 ms                                                | 51.6 ms: 1.12x slower                                       |
| pickle_pure_python         | 308 us                                                 | 346 us: 1.12x slower                                        |
| mdp                        | 2.42 sec                                               | 2.73 sec: 1.13x slower                                      |
| sympy_str                  | 292 ms                                                 | 330 ms: 1.13x slower                                        |
| xml_etree_generate         | 85.2 ms                                                | 96.9 ms: 1.14x slower                                       |
| sympy_integrate            | 20.5 ms                                                | 23.5 ms: 1.14x slower                                       |
| genshi_xml                 | 50.2 ms                                                | 57.9 ms: 1.15x slower                                       |
| richards_super             | 51.9 ms                                                | 60.1 ms: 1.16x slower                                       |
| xml_etree_process          | 59.0 ms                                                | 68.3 ms: 1.16x slower                                       |
| nqueens                    | 80.1 ms                                                | 92.8 ms: 1.16x slower                                       |
| sympy_expand               | 468 ms                                                 | 546 ms: 1.17x slower                                        |
| typing_runtime_protocols   | 163 us                                                 | 192 us: 1.18x slower                                        |
| genshi_text                | 22.8 ms                                                | 27.0 ms: 1.18x slower                                       |
| hexiom                     | 6.17 ms                                                | 7.32 ms: 1.19x slower                                       |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.22 ms: 1.19x slower                                       |
| scimark_lu                 | 114 ms                                                 | 136 ms: 1.19x slower                                        |
| django_template            | 34.7 ms                                                | 42.0 ms: 1.21x slower                                       |
| meteor_contest             | 104 ms                                                 | 127 ms: 1.23x slower                                        |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.23x slower                                       |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.23x slower                                       |
| fannkuch                   | 372 ms                                                 | 461 ms: 1.24x slower                                        |
| nbody                      | 89.3 ms                                                | 114 ms: 1.28x slower                                        |
| telco                      | 6.53 ms                                                | 8.60 ms: 1.32x slower                                       |
| coverage                   | 71.4 ms                                                | 96.2 ms: 1.35x slower                                       |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                       |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                       |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                       |
| bench_thread_pool          | 941 us                                                 | 3.13 ms: 3.32x slower                                       |
| bench_mp_pool              | 10.8 ms                                                | 97.0 ms: 8.98x slower                                       |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, json
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250318-3.14.0a6+-d1b910e-NOGIL/bm-20250318-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-d1b910e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.009x slower

# HPT report

- Reliability score: 98.83% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x