# Results vs. 3.12.6

- fork: python
- ref: 0f866cbfefd797b4dae2
- machine: linux-x86_64
- commit hash: 0f866cb
- commit date: 2025-06-10
- overall geometric mean: 1.017x faster
- HPT reliability: 85.43%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.07x slower                                                  |
| docutils       | 2.64 sec                                               | 2.68 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 66.5 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 523 ms: 2.12x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 225 ms: 1.98x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 549 ms: 1.97x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                                  |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 467 ms: 1.55x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                                  |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                          |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 68.7 ms: 1.18x faster                                                 |
| pidigits       | 184 ms                                                 | 182 ms: 1.01x faster                                                  |
| nbody          | 89.3 ms                                                | 119 ms: 1.33x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.4 ms: 1.01x faster                                                 |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.9 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.14 sec: 1.02x slower                                                |
| unpickle_pure_python | 221 us                                                 | 228 us: 1.03x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 335 us: 1.09x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.2 ms: 1.12x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.4 ms: 1.16x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.1 ms: 1.16x slower                                                 |
| json_loads           | 26.5 us                                                | 30.9 us: 1.17x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.56 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 39.4 ms: 1.13x slower                                                 |
| genshi_xml      | 50.2 ms                                                | 58.7 ms: 1.17x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.8 ms: 1.17x slower                                                 |
| mako            | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 523 ms: 2.12x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 225 ms: 1.98x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 549 ms: 1.97x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.84x faster                                                |
| gc_traversal               | 3.46 ms                                                | 1.90 ms: 1.82x faster                                                 |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 467 ms: 1.55x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                                  |
| deepcopy                   | 352 us                                                 | 286 us: 1.23x faster                                                  |
| float                      | 80.8 ms                                                | 68.7 ms: 1.18x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.70 ms: 1.17x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 34.4 us: 1.17x faster                                                 |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 86.9 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.1 ms: 1.11x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.95 us: 1.04x faster                                                 |
| scimark_sor                | 130 ms                                                 | 125 ms: 1.04x faster                                                  |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                  |
| pylint                     | 319 ms                                                 | 307 ms: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                |
| raytrace                   | 299 ms                                                 | 294 ms: 1.02x faster                                                  |
| generators                 | 32.2 ms                                                | 31.7 ms: 1.02x faster                                                 |
| pidigits                   | 184 ms                                                 | 182 ms: 1.01x faster                                                  |
| regex_v8                   | 20.6 ms                                                | 20.4 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                                  |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.68 sec: 1.02x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.14 sec: 1.02x slower                                                |
| hexiom                     | 6.17 ms                                                | 6.34 ms: 1.03x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 228 us: 1.03x slower                                                  |
| json                       | 5.02 ms                                                | 5.24 ms: 1.04x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.60 ms: 1.04x slower                                                 |
| html5lib                   | 63.6 ms                                                | 66.5 ms: 1.05x slower                                                 |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                  |
| scimark_fft                | 342 ms                                                 | 363 ms: 1.06x slower                                                  |
| 2to3                       | 264 ms                                                 | 281 ms: 1.07x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                 |
| sympy_str                  | 292 ms                                                 | 311 ms: 1.07x slower                                                  |
| pyflate                    | 448 ms                                                 | 479 ms: 1.07x slower                                                  |
| nqueens                    | 80.1 ms                                                | 85.7 ms: 1.07x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 179 ms: 1.08x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 335 us: 1.09x slower                                                  |
| thrift                     | 791 us                                                 | 877 us: 1.11x slower                                                  |
| sympy_expand               | 468 ms                                                 | 520 ms: 1.11x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 127 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 95.2 ms: 1.12x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 86.0 ms: 1.12x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 77.0 ms: 1.12x slower                                                 |
| richards                   | 45.9 ms                                                | 52.0 ms: 1.13x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.52 us: 1.13x slower                                                 |
| django_template            | 34.7 ms                                                | 39.4 ms: 1.13x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 186 us: 1.14x slower                                                  |
| richards_super             | 51.9 ms                                                | 59.7 ms: 1.15x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 860 ms: 1.16x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.4 ms: 1.16x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.1 ms: 1.16x slower                                                 |
| json_loads                 | 26.5 us                                                | 30.9 us: 1.17x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.78 sec: 1.17x slower                                                |
| logging_format             | 7.35 us                                                | 8.58 us: 1.17x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 58.7 ms: 1.17x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.8 ms: 1.17x slower                                                 |
| meteor_contest             | 104 ms                                                 | 123 ms: 1.19x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.24 ms: 1.19x slower                                                 |
| fannkuch                   | 372 ms                                                 | 462 ms: 1.24x slower                                                  |
| telco                      | 6.53 ms                                                | 8.47 ms: 1.30x slower                                                 |
| nbody                      | 89.3 ms                                                | 119 ms: 1.33x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.56 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.47 ms: 1.35x slower                                                 |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.44x slower                                                 |
| coverage                   | 71.4 ms                                                | 110 ms: 1.54x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.10 ms: 3.30x slower                                                 |
| logging_silent             | 109 ns                                                 | 527 ns: 4.84x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 104 ms: 9.61x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                          |

Benchmark hidden because not significant (3): chaos, regex_compile, coroutines
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.017x faster

# HPT report

- Reliability score: 85.43% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.42x