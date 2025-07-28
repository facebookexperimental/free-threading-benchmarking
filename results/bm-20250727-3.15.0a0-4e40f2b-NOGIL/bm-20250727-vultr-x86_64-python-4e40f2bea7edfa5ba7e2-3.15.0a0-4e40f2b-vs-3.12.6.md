# Results vs. 3.12.6

- fork: python
- ref: 4e40f2bea7edfa5ba7e2
- machine: linux-x86_64
- commit hash: 4e40f2b
- commit date: 2025-07-27
- overall geometric mean: 1.027x slower
- HPT reliability: 97.43%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 286 ms: 1.09x slower                                                  |
| docutils       | 2.64 sec                                               | 2.73 sec: 1.03x slower                                                |
| html5lib       | 63.6 ms                                                | 67.0 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 517 ms: 2.15x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 537 ms: 2.02x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 224 ms: 1.99x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 282 ms: 1.98x faster                                                  |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.81x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 474 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 500 ms: 1.43x faster                                                  |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.55x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.9 ms: 1.14x faster                                                 |
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                                  |
| nbody          | 89.3 ms                                                | 127 ms: 1.42x slower                                                  |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                 |
| regex_compile  | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| regex_dna      | 168 ms                                                 | 172 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.16 sec: 1.02x slower                                                |
| unpickle_pure_python | 221 us                                                 | 233 us: 1.06x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.9 ms: 1.13x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 347 us: 1.13x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.7 ms: 1.13x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                 |
| json_loads           | 26.5 us                                                | 31.7 us: 1.19x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.54 ms: 1.33x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.45x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 58.5 ms: 1.17x slower                                                 |
| django_template | 34.7 ms                                                | 40.7 ms: 1.17x slower                                                 |
| genshi_text     | 22.8 ms                                                | 27.3 ms: 1.20x slower                                                 |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.24x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 517 ms: 2.15x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 537 ms: 2.02x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 224 ms: 1.99x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 282 ms: 1.98x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                                |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.81x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 310 ms: 1.79x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.96 ms: 1.76x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 474 ms: 1.52x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 500 ms: 1.43x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                 |
| deepcopy                   | 352 us                                                 | 301 us: 1.17x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 34.8 us: 1.16x faster                                                 |
| go                         | 139 ms                                                 | 122 ms: 1.14x faster                                                  |
| float                      | 80.8 ms                                                | 70.9 ms: 1.14x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.7 us: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 88.1 ms: 1.10x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.9 ms: 1.10x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.10x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.06 us: 1.07x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.44 sec: 1.07x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| logging_silent             | 109 ns                                                 | 105 ns: 1.03x faster                                                  |
| scimark_sor                | 130 ms                                                 | 126 ms: 1.03x faster                                                  |
| async_generators           | 384 ms                                                 | 377 ms: 1.02x faster                                                  |
| generators                 | 32.2 ms                                                | 31.9 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                  |
| regex_compile              | 142 ms                                                 | 144 ms: 1.01x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.01x slower                                                |
| chaos                      | 62.8 ms                                                | 63.9 ms: 1.02x slower                                                 |
| raytrace                   | 299 ms                                                 | 305 ms: 1.02x slower                                                  |
| pyflate                    | 448 ms                                                 | 458 ms: 1.02x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.16 sec: 1.02x slower                                                |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.5 ms: 1.03x slower                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.16 us: 1.03x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.73 sec: 1.03x slower                                                |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.39 ms: 1.04x slower                                                 |
| logging_simple             | 6.63 us                                                | 6.98 us: 1.05x slower                                                 |
| html5lib                   | 63.6 ms                                                | 67.0 ms: 1.05x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 233 us: 1.06x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.66 ms: 1.06x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 793 ms: 1.07x slower                                                  |
| scimark_fft                | 342 ms                                                 | 366 ms: 1.07x slower                                                  |
| json                       | 5.02 ms                                                | 5.39 ms: 1.07x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.63 sec: 1.07x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 22.2 ms: 1.08x slower                                                 |
| 2to3                       | 264 ms                                                 | 286 ms: 1.09x slower                                                  |
| sympy_str                  | 292 ms                                                 | 317 ms: 1.09x slower                                                  |
| logging_format             | 7.35 us                                                | 7.99 us: 1.09x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 181 ms: 1.09x slower                                                  |
| nqueens                    | 80.1 ms                                                | 87.3 ms: 1.09x slower                                                 |
| thrift                     | 791 us                                                 | 887 us: 1.12x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 128 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 95.9 ms: 1.13x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 86.3 ms: 1.13x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 347 us: 1.13x slower                                                  |
| sympy_expand               | 468 ms                                                 | 528 ms: 1.13x slower                                                  |
| richards                   | 45.9 ms                                                | 51.9 ms: 1.13x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.7 ms: 1.13x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 78.7 ms: 1.15x slower                                                 |
| meteor_contest             | 104 ms                                                 | 120 ms: 1.16x slower                                                  |
| richards_super             | 51.9 ms                                                | 60.0 ms: 1.16x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 189 us: 1.16x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 58.5 ms: 1.17x slower                                                 |
| django_template            | 34.7 ms                                                | 40.7 ms: 1.17x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 69.5 ms: 1.18x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.7 us: 1.19x slower                                                 |
| genshi_text                | 22.8 ms                                                | 27.3 ms: 1.20x slower                                                 |
| fannkuch                   | 372 ms                                                 | 450 ms: 1.21x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.42 ms: 1.23x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.54 ms: 1.33x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.54 ms: 1.41x slower                                                 |
| nbody                      | 89.3 ms                                                | 127 ms: 1.42x slower                                                  |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                 |
| coverage                   | 71.4 ms                                                | 111 ms: 1.55x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.35x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.05x slower                                                 |
| telco                      | 6.53 ms                                                | 177 ms: 27.16x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (2): pylint, regex_v8
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250727-3.15.0a0-4e40f2b-NOGIL/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.027x slower

# HPT report

- Reliability score: 97.43% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x