# Results vs. 3.12.6

- fork: python
- ref: acefff95eab3db6b7cf8
- machine: linux-x86_64
- commit hash: acefff9
- commit date: 2026-05-17
- overall geometric mean: 1.061x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.64 sec                                               | 2.41 sec: 1.09x faster                                                |
| html5lib       | 63.6 ms                                                | 61.0 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 293 ms: 1.58x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 364 ms: 1.54x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 719 ms: 1.51x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 301 ms: 1.48x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 377 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 756 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 539 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 555 ms: 1.30x faster                                                  |
| async_generators           | 384 ms                                                 | 342 ms: 1.12x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.8 ms: 1.04x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.32x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.6 ms: 1.07x faster                                                 |
| pidigits       | 184 ms                                                 | 188 ms: 1.02x slower                                                  |
| nbody          | 89.3 ms                                                | 97.4 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.97 ms: 1.07x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                 |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 89.4 ms: 1.08x faster                                                 |
| json_dumps           | 10.4 ms                                                | 9.82 ms: 1.05x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 216 us: 1.02x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 86.7 ms: 1.02x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 141 ms: 1.02x slower                                                  |
| json_loads           | 26.5 us                                                | 27.7 us: 1.04x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 61.6 ms: 1.04x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 321 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                 |
| mako            | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 114 ms: 2.79x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.12x faster                                                |
| async_tree_none            | 464 ms                                                 | 293 ms: 1.58x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 364 ms: 1.54x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 719 ms: 1.51x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 301 ms: 1.48x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 377 ms: 1.47x faster                                                  |
| deepcopy                   | 352 us                                                 | 239 us: 1.47x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 756 ms: 1.47x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 27.6 us: 1.46x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 120 us: 1.36x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 539 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 555 ms: 1.30x faster                                                  |
| go                         | 139 ms                                                 | 107 ms: 1.30x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.6 ms: 1.23x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.60 us: 1.18x faster                                                 |
| scimark_sor                | 130 ms                                                 | 111 ms: 1.17x faster                                                  |
| spectral_norm              | 110 ms                                                 | 95.3 ms: 1.16x faster                                                 |
| generators                 | 32.2 ms                                                | 28.0 ms: 1.15x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                |
| raytrace                   | 299 ms                                                 | 260 ms: 1.15x faster                                                  |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 69.9 ms: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.21 sec: 1.13x faster                                                |
| chaos                      | 62.8 ms                                                | 55.9 ms: 1.12x faster                                                 |
| async_generators           | 384 ms                                                 | 342 ms: 1.12x faster                                                  |
| pyflate                    | 448 ms                                                 | 401 ms: 1.12x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.96 us: 1.11x faster                                                 |
| logging_format             | 7.35 us                                                | 6.69 us: 1.10x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.41 sec: 1.09x faster                                                |
| crypto_pyaes               | 76.6 ms                                                | 70.3 ms: 1.09x faster                                                 |
| logging_silent             | 109 ns                                                 | 100 ns: 1.09x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 89.4 ms: 1.08x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.1 ms: 1.08x faster                                                 |
| nqueens                    | 80.1 ms                                                | 74.6 ms: 1.07x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                  |
| float                      | 80.8 ms                                                | 75.6 ms: 1.07x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.97 ms: 1.07x faster                                                 |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.06x faster                                                  |
| scimark_fft                | 342 ms                                                 | 321 ms: 1.06x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 64.3 ms: 1.06x faster                                                 |
| richards                   | 45.9 ms                                                | 43.3 ms: 1.06x faster                                                 |
| json_dumps                 | 10.4 ms                                                | 9.82 ms: 1.05x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.88 ms: 1.05x faster                                                 |
| html5lib                   | 63.6 ms                                                | 61.0 ms: 1.04x faster                                                 |
| richards_super             | 51.9 ms                                                | 49.9 ms: 1.04x faster                                                 |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 216 us: 1.02x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.50 sec: 1.01x faster                                                |
| deltablue                  | 3.45 ms                                                | 3.42 ms: 1.01x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 116 ms: 1.01x slower                                                  |
| fannkuch                   | 372 ms                                                 | 378 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.24 us: 1.02x slower                                                 |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 86.7 ms: 1.02x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 141 ms: 1.02x slower                                                  |
| pidigits                   | 184 ms                                                 | 188 ms: 1.02x slower                                                  |
| thrift                     | 791 us                                                 | 809 us: 1.02x slower                                                  |
| sympy_expand               | 468 ms                                                 | 479 ms: 1.02x slower                                                  |
| json                       | 5.02 ms                                                | 5.17 ms: 1.03x slower                                                 |
| django_template            | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.8 ms: 1.04x slower                                                 |
| json_loads                 | 26.5 us                                                | 27.7 us: 1.04x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 61.6 ms: 1.04x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 321 us: 1.05x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.64 ms: 1.06x slower                                                 |
| nbody                      | 89.3 ms                                                | 97.4 ms: 1.09x slower                                                 |
| mako                       | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                 |
| regex_dna                  | 168 ms                                                 | 185 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 84.6 ms: 1.18x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.19 ms: 1.21x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.33 ms: 1.42x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.82 ms: 1.66x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 237 ms: 21.98x slower                                                 |
| telco                      | 6.53 ms                                                | 162 ms: 24.83x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): pprint_safe_repr
Ignored benchmarks (26) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260517-3.16.0a0-acefff9/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.061x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.18x