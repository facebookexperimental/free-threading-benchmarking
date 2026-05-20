# Results vs. 3.12.6

- fork: python
- ref: de9c32fc34fe2e000de1
- machine: linux-x86_64
- commit hash: de9c32f
- commit date: 2026-05-20
- overall geometric mean: 1.062x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.64 sec                                               | 2.40 sec: 1.10x faster                                                |
| html5lib       | 63.6 ms                                                | 61.0 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 294 ms: 1.58x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 368 ms: 1.52x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 724 ms: 1.50x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 301 ms: 1.48x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 378 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 765 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 545 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 559 ms: 1.29x faster                                                  |
| async_generators           | 384 ms                                                 | 345 ms: 1.11x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.31x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.6 ms: 1.07x faster                                                 |
| nbody          | 89.3 ms                                                | 90.5 ms: 1.01x slower                                                 |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.00x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.91 ms: 1.09x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.9 ms: 1.06x slower                                                 |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 89.6 ms: 1.08x faster                                                 |
| json_dumps           | 10.4 ms                                                | 9.88 ms: 1.05x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 216 us: 1.02x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 86.9 ms: 1.02x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 142 ms: 1.03x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 317 us: 1.03x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 61.4 ms: 1.04x slower                                                 |
| json_loads           | 26.5 us                                                | 27.7 us: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 35.5 ms: 1.02x slower                                                 |
| mako            | 11.0 ms                                                | 12.3 ms: 1.12x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 115 ms: 2.78x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.12x faster                                                |
| async_tree_none            | 464 ms                                                 | 294 ms: 1.58x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 368 ms: 1.52x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 724 ms: 1.50x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 301 ms: 1.48x faster                                                  |
| deepcopy                   | 352 us                                                 | 239 us: 1.47x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 378 ms: 1.47x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 27.5 us: 1.47x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 765 ms: 1.45x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 118 us: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 545 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 559 ms: 1.29x faster                                                  |
| go                         | 139 ms                                                 | 108 ms: 1.29x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.1 us: 1.23x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.22x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.59 us: 1.19x faster                                                 |
| scimark_sor                | 130 ms                                                 | 109 ms: 1.19x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                |
| raytrace                   | 299 ms                                                 | 261 ms: 1.15x faster                                                  |
| spectral_norm              | 110 ms                                                 | 96.2 ms: 1.15x faster                                                 |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 69.7 ms: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.20 sec: 1.13x faster                                                |
| chaos                      | 62.8 ms                                                | 55.7 ms: 1.13x faster                                                 |
| async_generators           | 384 ms                                                 | 345 ms: 1.11x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.96 us: 1.11x faster                                                 |
| logging_silent             | 109 ns                                                 | 98.6 ns: 1.10x faster                                                 |
| generators                 | 32.2 ms                                                | 29.2 ms: 1.10x faster                                                 |
| logging_format             | 7.35 us                                                | 6.69 us: 1.10x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.40 sec: 1.10x faster                                                |
| pyflate                    | 448 ms                                                 | 409 ms: 1.10x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.91 ms: 1.09x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 89.6 ms: 1.08x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 71.1 ms: 1.08x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                 |
| scimark_fft                | 342 ms                                                 | 319 ms: 1.07x faster                                                  |
| float                      | 80.8 ms                                                | 75.6 ms: 1.07x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 156 ms: 1.06x faster                                                  |
| nqueens                    | 80.1 ms                                                | 75.4 ms: 1.06x faster                                                 |
| sympy_str                  | 292 ms                                                 | 276 ms: 1.06x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.84 ms: 1.06x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 65.0 ms: 1.05x faster                                                 |
| meteor_contest             | 104 ms                                                 | 98.7 ms: 1.05x faster                                                 |
| richards                   | 45.9 ms                                                | 43.8 ms: 1.05x faster                                                 |
| json_dumps                 | 10.4 ms                                                | 9.88 ms: 1.05x faster                                                 |
| html5lib                   | 63.6 ms                                                | 61.0 ms: 1.04x faster                                                 |
| richards_super             | 51.9 ms                                                | 50.0 ms: 1.04x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 216 us: 1.02x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.50 sec: 1.01x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 739 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.22 us: 1.01x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 115 ms: 1.01x slower                                                  |
| thrift                     | 791 us                                                 | 801 us: 1.01x slower                                                  |
| nbody                      | 89.3 ms                                                | 90.5 ms: 1.01x slower                                                 |
| fannkuch                   | 372 ms                                                 | 379 ms: 1.02x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 86.9 ms: 1.02x slower                                                 |
| django_template            | 34.7 ms                                                | 35.5 ms: 1.02x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.02x slower                                                 |
| json                       | 5.02 ms                                                | 5.15 ms: 1.03x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 142 ms: 1.03x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 317 us: 1.03x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 61.4 ms: 1.04x slower                                                 |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.7 us: 1.04x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.9 ms: 1.06x slower                                                 |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.73 ms: 1.08x slower                                                 |
| mako                       | 11.0 ms                                                | 12.3 ms: 1.12x slower                                                 |
| coverage                   | 71.4 ms                                                | 84.6 ms: 1.18x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.15 ms: 1.20x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.35 ms: 1.43x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.67x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 243 ms: 22.46x slower                                                 |
| telco                      | 6.53 ms                                                | 161 ms: 24.67x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (2): deltablue, sympy_expand
Ignored benchmarks (26) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260520-3.16.0a0-de9c32f/bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.062x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.17x