# Results vs. 3.12.6

- fork: mpage
- ref: lfb_nolock
- machine: linux-x86_64
- commit hash: a350570
- commit date: 2025-03-19
- overall geometric mean: 1.005x slower
- HPT reliability: 96.26%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 288 ms: 1.09x slower                                        |
| docutils       | 2.64 sec                                               | 2.75 sec: 1.04x slower                                      |
| html5lib       | 63.6 ms                                                | 67.2 ms: 1.06x slower                                       |
| Geometric mean | (ref)                                                  | 1.06x slower                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 525 ms: 2.11x faster                                        |
| async_tree_none_tg         | 446 ms                                                 | 225 ms: 1.98x faster                                        |
| async_tree_io              | 1.08 sec                                               | 557 ms: 1.95x faster                                        |
| async_tree_memoization_tg  | 560 ms                                                 | 289 ms: 1.93x faster                                        |
| async_tree_none            | 464 ms                                                 | 261 ms: 1.78x faster                                        |
| async_tree_memoization     | 555 ms                                                 | 322 ms: 1.73x faster                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 555 ms: 1.30x faster                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 587 ms: 1.22x faster                                        |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                        |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                       |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 80.8 ms                                                | 65.3 ms: 1.24x faster                                       |
| nbody          | 89.3 ms                                                | 105 ms: 1.18x slower                                        |
| pidigits       | 184 ms                                                 | 228 ms: 1.24x slower                                        |
| Geometric mean | (ref)                                                  | 1.06x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.63 ms: 1.20x faster                                       |
| regex_dna      | 168 ms                                                 | 165 ms: 1.01x faster                                        |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                       |
| regex_compile  | 142 ms                                                 | 151 ms: 1.06x slower                                        |
| Geometric mean | (ref)                                                  | 1.03x faster                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.5 ms: 1.09x faster                                       |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                        |
| unpickle_pure_python | 221 us                                                 | 236 us: 1.07x slower                                        |
| tomli_loads          | 2.11 sec                                               | 2.26 sec: 1.07x slower                                      |
| pickle_pure_python   | 308 us                                                 | 342 us: 1.11x slower                                        |
| json_loads           | 26.5 us                                                | 29.5 us: 1.11x slower                                       |
| xml_etree_generate   | 85.2 ms                                                | 96.3 ms: 1.13x slower                                       |
| xml_etree_process    | 59.0 ms                                                | 68.7 ms: 1.17x slower                                       |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.23x slower                                       |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                       |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.59x slower                                       |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.9 ms: 1.15x slower                                       |
| genshi_text     | 22.8 ms                                                | 26.9 ms: 1.18x slower                                       |
| django_template | 34.7 ms                                                | 41.4 ms: 1.19x slower                                       |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                       |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 525 ms: 2.11x faster                                        |
| async_tree_none_tg         | 446 ms                                                 | 225 ms: 1.98x faster                                        |
| async_tree_io              | 1.08 sec                                               | 557 ms: 1.95x faster                                        |
| async_tree_memoization_tg  | 560 ms                                                 | 289 ms: 1.93x faster                                        |
| gc_traversal               | 3.46 ms                                                | 1.79 ms: 1.93x faster                                       |
| async_tree_none            | 464 ms                                                 | 261 ms: 1.78x faster                                        |
| async_tree_memoization     | 555 ms                                                 | 322 ms: 1.73x faster                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 555 ms: 1.30x faster                                        |
| float                      | 80.8 ms                                                | 65.3 ms: 1.24x faster                                       |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 587 ms: 1.22x faster                                        |
| regex_effbot               | 3.17 ms                                                | 2.63 ms: 1.20x faster                                       |
| deepcopy                   | 352 us                                                 | 299 us: 1.18x faster                                        |
| deepcopy_memo              | 40.3 us                                                | 36.5 us: 1.10x faster                                       |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                       |
| go                         | 139 ms                                                 | 127 ms: 1.10x faster                                        |
| xml_etree_iterparse        | 96.7 ms                                                | 88.5 ms: 1.09x faster                                       |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                       |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                        |
| dulwich_log                | 78.9 ms                                                | 73.1 ms: 1.08x faster                                       |
| logging_silent             | 109 ns                                                 | 105 ns: 1.04x faster                                        |
| bpe_tokeniser              | 4.74 sec                                               | 4.57 sec: 1.04x faster                                      |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                        |
| coroutines                 | 23.9 ms                                                | 23.2 ms: 1.03x faster                                       |
| spectral_norm              | 110 ms                                                 | 107 ms: 1.03x faster                                        |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                      |
| raytrace                   | 299 ms                                                 | 292 ms: 1.03x faster                                        |
| scimark_sor                | 130 ms                                                 | 127 ms: 1.02x faster                                        |
| regex_dna                  | 168 ms                                                 | 165 ms: 1.01x faster                                        |
| comprehensions             | 19.8 us                                                | 19.8 us: 1.00x faster                                       |
| deepcopy_reduce            | 3.08 us                                                | 3.09 us: 1.00x slower                                       |
| deltablue                  | 3.45 ms                                                | 3.47 ms: 1.01x slower                                       |
| json                       | 5.02 ms                                                | 5.06 ms: 1.01x slower                                       |
| chaos                      | 62.8 ms                                                | 63.6 ms: 1.01x slower                                       |
| scimark_fft                | 342 ms                                                 | 347 ms: 1.02x slower                                        |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                       |
| pyflate                    | 448 ms                                                 | 460 ms: 1.03x slower                                        |
| docutils                   | 2.64 sec                                               | 2.75 sec: 1.04x slower                                      |
| html5lib                   | 63.6 ms                                                | 67.2 ms: 1.06x slower                                       |
| thrift                     | 791 us                                                 | 837 us: 1.06x slower                                        |
| logging_simple             | 6.63 us                                                | 7.02 us: 1.06x slower                                       |
| regex_compile              | 142 ms                                                 | 151 ms: 1.06x slower                                        |
| unpickle_pure_python       | 221 us                                                 | 236 us: 1.07x slower                                        |
| pprint_safe_repr           | 743 ms                                                 | 798 ms: 1.07x slower                                        |
| tomli_loads                | 2.11 sec                                               | 2.26 sec: 1.07x slower                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 74.1 ms: 1.08x slower                                       |
| pprint_pformat             | 1.52 sec                                               | 1.65 sec: 1.09x slower                                      |
| logging_format             | 7.35 us                                                | 7.99 us: 1.09x slower                                       |
| crypto_pyaes               | 76.6 ms                                                | 83.4 ms: 1.09x slower                                       |
| 2to3                       | 264 ms                                                 | 288 ms: 1.09x slower                                        |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.9 ms: 1.10x slower                                       |
| sqlalchemy_declarative     | 143 ms                                                 | 158 ms: 1.10x slower                                        |
| pickle_pure_python         | 308 us                                                 | 342 us: 1.11x slower                                        |
| json_loads                 | 26.5 us                                                | 29.5 us: 1.11x slower                                       |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.12x slower                                        |
| richards                   | 45.9 ms                                                | 51.5 ms: 1.12x slower                                       |
| mdp                        | 2.42 sec                                               | 2.73 sec: 1.13x slower                                      |
| xml_etree_generate         | 85.2 ms                                                | 96.3 ms: 1.13x slower                                       |
| sympy_str                  | 292 ms                                                 | 332 ms: 1.14x slower                                        |
| sympy_integrate            | 20.5 ms                                                | 23.6 ms: 1.15x slower                                       |
| genshi_xml                 | 50.2 ms                                                | 57.9 ms: 1.15x slower                                       |
| nqueens                    | 80.1 ms                                                | 92.4 ms: 1.15x slower                                       |
| richards_super             | 51.9 ms                                                | 60.2 ms: 1.16x slower                                       |
| xml_etree_process          | 59.0 ms                                                | 68.7 ms: 1.17x slower                                       |
| sympy_expand               | 468 ms                                                 | 546 ms: 1.17x slower                                        |
| nbody                      | 89.3 ms                                                | 105 ms: 1.18x slower                                        |
| hexiom                     | 6.17 ms                                                | 7.27 ms: 1.18x slower                                       |
| genshi_text                | 22.8 ms                                                | 26.9 ms: 1.18x slower                                       |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.19 ms: 1.18x slower                                       |
| scimark_lu                 | 114 ms                                                 | 135 ms: 1.18x slower                                        |
| typing_runtime_protocols   | 163 us                                                 | 194 us: 1.19x slower                                        |
| django_template            | 34.7 ms                                                | 41.4 ms: 1.19x slower                                       |
| fannkuch                   | 372 ms                                                 | 452 ms: 1.21x slower                                        |
| meteor_contest             | 104 ms                                                 | 126 ms: 1.22x slower                                        |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.23x slower                                       |
| pidigits                   | 184 ms                                                 | 228 ms: 1.24x slower                                        |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.24x slower                                       |
| telco                      | 6.53 ms                                                | 8.68 ms: 1.33x slower                                       |
| coverage                   | 71.4 ms                                                | 95.7 ms: 1.34x slower                                       |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                       |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                       |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.59x slower                                       |
| bench_thread_pool          | 941 us                                                 | 3.13 ms: 3.33x slower                                       |
| bench_mp_pool              | 10.8 ms                                                | 96.7 ms: 8.96x slower                                       |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                |

Benchmark hidden because not significant (3): pylint, generators, asyncio_websockets
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250319-3.14.0a6+-a350570-NOGIL/bm-20250319-vultr-x86_64-mpage-lfb_nolock-3.14.0a6+-a350570.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.005x slower

# HPT report

- Reliability score: 96.26% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x