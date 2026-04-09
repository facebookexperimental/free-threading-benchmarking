# Results vs. 3.12.6

- fork: python
- ref: efde4333bfcdd1e24c2a
- machine: linux-x86_64
- commit hash: efde433
- commit date: 2026-04-08
- overall geometric mean: 1.024x slower
- HPT reliability: 63.51%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 284 ms: 1.08x slower                                                   |
| docutils       | 2.64 sec                                               | 2.63 sec: 1.00x faster                                                 |
| html5lib       | 63.6 ms                                                | 65.7 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 612 ms: 1.81x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 638 ms: 1.70x faster                                                   |
| async_tree_none            | 464 ms                                                 | 292 ms: 1.59x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 357 ms: 1.55x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 511 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 538 ms: 1.33x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 508 ms: 1.02x faster                                                   |
| async_generators           | 384 ms                                                 | 380 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.41x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 73.6 ms: 1.10x faster                                                  |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                   |
| nbody          | 89.3 ms                                                | 123 ms: 1.37x slower                                                   |
| Geometric mean | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.74 ms: 1.16x faster                                                  |
| regex_compile  | 142 ms                                                 | 141 ms: 1.01x faster                                                   |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                  |
| regex_dna      | 168 ms                                                 | 175 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.3 ms: 1.11x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 237 us: 1.07x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 338 us: 1.10x slower                                                   |
| json_loads           | 26.5 us                                                | 29.3 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 68.4 ms: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.93 ms: 1.39x slower                                                  |
| python_startup         | 9.93 ms                                                | 16.2 ms: 1.63x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 54.0 ms: 1.08x slower                                                  |
| genshi_text     | 22.8 ms                                                | 25.3 ms: 1.11x slower                                                  |
| django_template | 34.7 ms                                                | 39.2 ms: 1.13x slower                                                  |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.18x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 612 ms: 1.81x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.97 ms: 1.75x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 325 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 262 ms: 1.70x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 638 ms: 1.70x faster                                                   |
| async_tree_none            | 464 ms                                                 | 292 ms: 1.59x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 357 ms: 1.55x faster                                                   |
| bench_mp_pool              | 10.8 ms                                                | 7.05 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 511 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 538 ms: 1.33x faster                                                   |
| deepcopy                   | 352 us                                                 | 268 us: 1.31x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 31.2 us: 1.29x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.74 ms: 1.16x faster                                                  |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                   |
| sqlite_synth               | 2.20 us                                                | 1.94 us: 1.13x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 70.2 ms: 1.12x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.9 us: 1.11x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 87.3 ms: 1.11x faster                                                  |
| float                      | 80.8 ms                                                | 73.6 ms: 1.10x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.92 sec: 1.10x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.37 sec: 1.08x faster                                                 |
| pylint                     | 319 ms                                                 | 297 ms: 1.07x faster                                                   |
| logging_silent             | 109 ns                                                 | 102 ns: 1.07x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                   |
| scimark_sor                | 130 ms                                                 | 122 ms: 1.06x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.95 us: 1.04x faster                                                  |
| spectral_norm              | 110 ms                                                 | 107 ms: 1.03x faster                                                   |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 508 ms: 1.02x faster                                                   |
| regex_compile              | 142 ms                                                 | 141 ms: 1.01x faster                                                   |
| async_generators           | 384 ms                                                 | 380 ms: 1.01x faster                                                   |
| chaos                      | 62.8 ms                                                | 62.3 ms: 1.01x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.63 sec: 1.00x faster                                                 |
| raytrace                   | 299 ms                                                 | 302 ms: 1.01x slower                                                   |
| logging_simple             | 6.63 us                                                | 6.74 us: 1.02x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                  |
| generators                 | 32.2 ms                                                | 33.0 ms: 1.02x slower                                                  |
| scimark_fft                | 342 ms                                                 | 353 ms: 1.03x slower                                                   |
| html5lib                   | 63.6 ms                                                | 65.7 ms: 1.03x slower                                                  |
| pyflate                    | 448 ms                                                 | 463 ms: 1.03x slower                                                   |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                   |
| regex_dna                  | 168 ms                                                 | 175 ms: 1.04x slower                                                   |
| logging_format             | 7.35 us                                                | 7.69 us: 1.05x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 21.7 ms: 1.06x slower                                                  |
| sympy_str                  | 292 ms                                                 | 311 ms: 1.07x slower                                                   |
| sympy_sum                  | 166 ms                                                 | 177 ms: 1.07x slower                                                   |
| hexiom                     | 6.17 ms                                                | 6.61 ms: 1.07x slower                                                  |
| unpickle_pure_python       | 221 us                                                 | 237 us: 1.07x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 54.0 ms: 1.08x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 800 ms: 1.08x slower                                                   |
| 2to3                       | 264 ms                                                 | 284 ms: 1.08x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.66 sec: 1.09x slower                                                 |
| nqueens                    | 80.1 ms                                                | 87.5 ms: 1.09x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 338 us: 1.10x slower                                                   |
| scimark_lu                 | 114 ms                                                 | 126 ms: 1.10x slower                                                   |
| json_loads                 | 26.5 us                                                | 29.3 us: 1.10x slower                                                  |
| genshi_text                | 22.8 ms                                                | 25.3 ms: 1.11x slower                                                  |
| richards                   | 45.9 ms                                                | 51.4 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 95.5 ms: 1.12x slower                                                  |
| thrift                     | 791 us                                                 | 890 us: 1.12x slower                                                   |
| sympy_expand               | 468 ms                                                 | 527 ms: 1.13x slower                                                   |
| richards_super             | 51.9 ms                                                | 58.5 ms: 1.13x slower                                                  |
| django_template            | 34.7 ms                                                | 39.2 ms: 1.13x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 78.8 ms: 1.15x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 88.3 ms: 1.15x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.4 ms: 1.16x slower                                                  |
| typing_runtime_protocols   | 163 us                                                 | 193 us: 1.18x slower                                                   |
| meteor_contest             | 104 ms                                                 | 126 ms: 1.22x slower                                                   |
| fannkuch                   | 372 ms                                                 | 457 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.44 ms: 1.24x slower                                                  |
| nbody                      | 89.3 ms                                                | 123 ms: 1.37x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 9.93 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.53 ms: 1.40x slower                                                  |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.46 ms: 1.55x slower                                                  |
| coverage                   | 71.4 ms                                                | 111 ms: 1.56x slower                                                   |
| python_startup             | 9.93 ms                                                | 16.2 ms: 1.63x slower                                                  |
| telco                      | 6.53 ms                                                | 171 ms: 26.17x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (2): json, deltablue
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260408-3.15.0a8+-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8+-efde433.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.024x slower

# HPT report

- Reliability score: 63.51% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.43x