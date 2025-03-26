# Results vs. 3.12.6

- fork: DinoV
- ref: nolock_loadattr_with
- machine: linux-x86_64
- commit hash: aeb389d
- commit date: 2025-03-25
- overall geometric mean: 1.045x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 298 ms: 1.13x slower                                                  |
| docutils       | 2.64 sec                                               | 2.77 sec: 1.05x slower                                                |
| html5lib       | 63.6 ms                                                | 71.7 ms: 1.13x slower                                                 |
| Geometric mean | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 557 ms: 1.99x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 237 ms: 1.88x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 302 ms: 1.85x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 588 ms: 1.84x faster                                                  |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 337 ms: 1.65x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 524 ms: 1.37x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                 |
| async_generators           | 384 ms                                                 | 387 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 76.5 ms: 1.06x faster                                                 |
| pidigits       | 184 ms                                                 | 208 ms: 1.13x slower                                                  |
| nbody          | 89.3 ms                                                | 132 ms: 1.48x slower                                                  |
| Geometric mean | (ref)                                                  | 1.17x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.64 ms: 1.20x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                 |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                  |
| regex_compile  | 142 ms                                                 | 158 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.4 ms: 1.09x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| json_loads           | 26.5 us                                                | 29.4 us: 1.11x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 2.35 sec: 1.12x slower                                                |
| xml_etree_generate   | 85.2 ms                                                | 97.3 ms: 1.14x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 252 us: 1.14x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 364 us: 1.18x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 71.1 ms: 1.21x slower                                                 |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.56x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.57x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.5 ms: 1.19x slower                                                 |
| django_template | 34.7 ms                                                | 42.4 ms: 1.22x slower                                                 |
| genshi_text     | 22.8 ms                                                | 28.3 ms: 1.24x slower                                                 |
| mako            | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 557 ms: 1.99x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.80 ms: 1.92x faster                                                 |
| async_tree_none_tg         | 446 ms                                                 | 237 ms: 1.88x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 302 ms: 1.85x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 588 ms: 1.84x faster                                                  |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 337 ms: 1.65x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 485 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 524 ms: 1.37x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.64 ms: 1.20x faster                                                 |
| deepcopy                   | 352 us                                                 | 313 us: 1.12x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 88.4 ms: 1.09x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| pathlib                    | 21.5 ms                                                | 20.1 ms: 1.07x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 73.7 ms: 1.07x faster                                                 |
| float                      | 80.8 ms                                                | 76.5 ms: 1.06x faster                                                 |
| generators                 | 32.2 ms                                                | 31.0 ms: 1.04x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 39.3 us: 1.02x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                 |
| async_generators           | 384 ms                                                 | 387 ms: 1.01x slower                                                  |
| json                       | 5.02 ms                                                | 5.07 ms: 1.01x slower                                                 |
| spectral_norm              | 110 ms                                                 | 112 ms: 1.02x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                |
| bpe_tokeniser              | 4.74 sec                                               | 4.88 sec: 1.03x slower                                                |
| logging_silent             | 109 ns                                                 | 112 ns: 1.03x slower                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.19 us: 1.04x slower                                                 |
| go                         | 139 ms                                                 | 144 ms: 1.04x slower                                                  |
| comprehensions             | 19.8 us                                                | 20.7 us: 1.04x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                 |
| scimark_sor                | 130 ms                                                 | 136 ms: 1.05x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.77 sec: 1.05x slower                                                |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                  |
| raytrace                   | 299 ms                                                 | 322 ms: 1.08x slower                                                  |
| chaos                      | 62.8 ms                                                | 68.4 ms: 1.09x slower                                                 |
| json_loads                 | 26.5 us                                                | 29.4 us: 1.11x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.34 us: 1.11x slower                                                 |
| thrift                     | 791 us                                                 | 876 us: 1.11x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 158 ms: 1.11x slower                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.2 ms: 1.11x slower                                                 |
| regex_compile              | 142 ms                                                 | 158 ms: 1.11x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.35 sec: 1.12x slower                                                |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.86 ms: 1.12x slower                                                 |
| pidigits                   | 184 ms                                                 | 208 ms: 1.13x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 838 ms: 1.13x slower                                                  |
| html5lib                   | 63.6 ms                                                | 71.7 ms: 1.13x slower                                                 |
| pyflate                    | 448 ms                                                 | 506 ms: 1.13x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.73 sec: 1.13x slower                                                |
| 2to3                       | 264 ms                                                 | 298 ms: 1.13x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.73 sec: 1.14x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 97.3 ms: 1.14x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 252 us: 1.14x slower                                                  |
| logging_format             | 7.35 us                                                | 8.41 us: 1.15x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 87.9 ms: 1.15x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 23.7 ms: 1.15x slower                                                 |
| sympy_str                  | 292 ms                                                 | 338 ms: 1.16x slower                                                  |
| scimark_fft                | 342 ms                                                 | 397 ms: 1.16x slower                                                  |
| sympy_expand               | 468 ms                                                 | 553 ms: 1.18x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 364 us: 1.18x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 59.5 ms: 1.19x slower                                                 |
| richards                   | 45.9 ms                                                | 54.7 ms: 1.19x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 71.1 ms: 1.21x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 83.4 ms: 1.22x slower                                                 |
| nqueens                    | 80.1 ms                                                | 97.6 ms: 1.22x slower                                                 |
| richards_super             | 51.9 ms                                                | 63.4 ms: 1.22x slower                                                 |
| django_template            | 34.7 ms                                                | 42.4 ms: 1.22x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.63 ms: 1.24x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.24x slower                                                 |
| genshi_text                | 22.8 ms                                                | 28.3 ms: 1.24x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 203 us: 1.24x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 143 ms: 1.25x slower                                                  |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.26x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.78 ms: 1.31x slower                                                 |
| fannkuch                   | 372 ms                                                 | 497 ms: 1.33x slower                                                  |
| telco                      | 6.53 ms                                                | 9.09 ms: 1.39x slower                                                 |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                 |
| nbody                      | 89.3 ms                                                | 132 ms: 1.48x slower                                                  |
| coverage                   | 71.4 ms                                                | 109 ms: 1.52x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.56x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.36x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 97.4 ms: 9.02x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250325-3.14.0a6+-aeb389d-NOGIL/bm-20250325-vultr-x86_64-DinoV-nolock_loadattr_with-3.14.0a6+-aeb389d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.045x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.37x