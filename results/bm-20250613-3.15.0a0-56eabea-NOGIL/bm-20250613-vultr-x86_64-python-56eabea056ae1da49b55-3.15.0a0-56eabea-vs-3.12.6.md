# Results vs. 3.12.6

- fork: python
- ref: 56eabea056ae1da49b55
- machine: linux-x86_64
- commit hash: 56eabea
- commit date: 2025-06-13
- overall geometric mean: 1.016x faster
- HPT reliability: 82.14%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.07x slower                                                  |
| docutils       | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                |
| html5lib       | 63.6 ms                                                | 66.5 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 524 ms: 2.12x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 552 ms: 1.96x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 228 ms: 1.96x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 287 ms: 1.95x faster                                                  |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 469 ms: 1.54x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 495 ms: 1.44x faster                                                  |
| async_generators           | 384 ms                                                 | 368 ms: 1.04x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                          |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.6 ms: 1.16x faster                                                 |
| pidigits       | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| nbody          | 89.3 ms                                                | 122 ms: 1.37x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.1 ms: 1.03x faster                                                 |
| regex_dna      | 168 ms                                                 | 169 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.6 ms: 1.09x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                |
| unpickle_pure_python | 221 us                                                 | 228 us: 1.03x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 337 us: 1.09x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.0 ms: 1.11x slower                                                 |
| json_dumps           | 10.4 ms                                                | 11.9 ms: 1.15x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.0 ms: 1.17x slower                                                 |
| json_loads           | 26.5 us                                                | 31.3 us: 1.18x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.58 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 39.5 ms: 1.14x slower                                                 |
| genshi_xml      | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.4 ms: 1.16x slower                                                 |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.22x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 524 ms: 2.12x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 552 ms: 1.96x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 228 ms: 1.96x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 287 ms: 1.95x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                |
| gc_traversal               | 3.46 ms                                                | 1.91 ms: 1.81x faster                                                 |
| async_tree_none            | 464 ms                                                 | 260 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 469 ms: 1.54x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 495 ms: 1.44x faster                                                  |
| deepcopy                   | 352 us                                                 | 287 us: 1.23x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                 |
| float                      | 80.8 ms                                                | 69.6 ms: 1.16x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 34.7 us: 1.16x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.3 us: 1.15x faster                                                 |
| go                         | 139 ms                                                 | 122 ms: 1.15x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 72.0 ms: 1.10x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 88.6 ms: 1.09x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.8 ms: 1.09x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.38 sec: 1.08x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                  |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                                  |
| async_generators           | 384 ms                                                 | 368 ms: 1.04x faster                                                  |
| pylint                     | 319 ms                                                 | 306 ms: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                |
| regex_v8                   | 20.6 ms                                                | 20.1 ms: 1.03x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.02 us: 1.02x faster                                                 |
| pidigits                   | 184 ms                                                 | 181 ms: 1.02x faster                                                  |
| generators                 | 32.2 ms                                                | 31.8 ms: 1.01x faster                                                 |
| raytrace                   | 299 ms                                                 | 296 ms: 1.01x faster                                                  |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| chaos                      | 62.8 ms                                                | 62.2 ms: 1.01x faster                                                 |
| regex_dna                  | 168 ms                                                 | 169 ms: 1.01x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.67 sec: 1.01x slower                                                |
| tomli_loads                | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                |
| deltablue                  | 3.45 ms                                                | 3.56 ms: 1.03x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 228 us: 1.03x slower                                                  |
| pyflate                    | 448 ms                                                 | 464 ms: 1.04x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.43 ms: 1.04x slower                                                 |
| html5lib                   | 63.6 ms                                                | 66.5 ms: 1.05x slower                                                 |
| nqueens                    | 80.1 ms                                                | 85.0 ms: 1.06x slower                                                 |
| json                       | 5.02 ms                                                | 5.33 ms: 1.06x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.06x slower                                                 |
| 2to3                       | 264 ms                                                 | 281 ms: 1.07x slower                                                  |
| sympy_str                  | 292 ms                                                 | 313 ms: 1.07x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.07x slower                                                  |
| scimark_fft                | 342 ms                                                 | 368 ms: 1.08x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 337 us: 1.09x slower                                                  |
| thrift                     | 791 us                                                 | 874 us: 1.10x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 85.2 ms: 1.11x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 95.0 ms: 1.11x slower                                                 |
| sympy_expand               | 468 ms                                                 | 523 ms: 1.12x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 128 ms: 1.12x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 77.4 ms: 1.13x slower                                                 |
| django_template            | 34.7 ms                                                | 39.5 ms: 1.14x slower                                                 |
| richards                   | 45.9 ms                                                | 52.5 ms: 1.14x slower                                                 |
| genshi_xml                 | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 187 us: 1.14x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.9 ms: 1.15x slower                                                 |
| richards_super             | 51.9 ms                                                | 59.7 ms: 1.15x slower                                                 |
| meteor_contest             | 104 ms                                                 | 120 ms: 1.15x slower                                                  |
| genshi_text                | 22.8 ms                                                | 26.4 ms: 1.16x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.68 us: 1.16x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 868 ms: 1.17x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 69.0 ms: 1.17x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.79 sec: 1.18x slower                                                |
| json_loads                 | 26.5 us                                                | 31.3 us: 1.18x slower                                                 |
| logging_format             | 7.35 us                                                | 8.68 us: 1.18x slower                                                 |
| fannkuch                   | 372 ms                                                 | 458 ms: 1.23x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.49 ms: 1.25x slower                                                 |
| telco                      | 6.53 ms                                                | 8.53 ms: 1.31x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.58 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.48 ms: 1.35x slower                                                 |
| nbody                      | 89.3 ms                                                | 122 ms: 1.37x slower                                                  |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                 |
| coverage                   | 71.4 ms                                                | 110 ms: 1.55x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.10 ms: 3.30x slower                                                 |
| logging_silent             | 109 ns                                                 | 522 ns: 4.79x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.57x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (3): coroutines, asyncio_websockets, regex_compile
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.016x faster

# HPT report

- Reliability score: 82.14% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.42x