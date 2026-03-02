# Results vs. 3.12.6

- fork: python
- ref: c9a5d9aae48a9faa553a
- machine: linux-x86_64
- commit hash: c9a5d9a
- commit date: 2026-03-01
- overall geometric mean: 1.072x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 251 ms: 1.05x faster                                                   |
| docutils       | 2.64 sec                                               | 2.59 sec: 1.02x faster                                                 |
| html5lib       | 63.6 ms                                                | 59.5 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 570 ms: 1.95x faster                                                   |
| async_tree_none            | 464 ms                                                 | 245 ms: 1.90x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 583 ms: 1.86x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                   |
| async_generators           | 384 ms                                                 | 337 ms: 1.14x faster                                                   |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.51x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.8 ms: 1.14x faster                                                  |
| nbody          | 89.3 ms                                                | 90.6 ms: 1.01x slower                                                  |
| pidigits       | 184 ms                                                 | 201 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                  |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                   |
| regex_v8       | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.84 sec: 1.15x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 85.0 ms: 1.14x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| json_dumps           | 10.4 ms                                                | 9.87 ms: 1.05x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 83.8 ms: 1.02x faster                                                  |
| json_loads           | 26.5 us                                                | 28.0 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.41 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.1 ms: 1.08x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 49.1 ms: 1.02x faster                                                  |
| django_template | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                  |
| mako            | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.00x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.11x faster                                                 |
| async_tree_io_tg           | 1.11 sec                                               | 570 ms: 1.95x faster                                                   |
| async_tree_none            | 464 ms                                                 | 245 ms: 1.90x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 583 ms: 1.86x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 241 ms: 1.85x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 308 ms: 1.82x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 307 ms: 1.81x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 26.5 us: 1.52x faster                                                  |
| deepcopy                   | 352 us                                                 | 233 us: 1.51x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 499 ms: 1.43x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                   |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                   |
| pathlib                    | 21.5 ms                                                | 17.5 ms: 1.23x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.1 us: 1.23x faster                                                  |
| scimark_sor                | 130 ms                                                 | 106 ms: 1.22x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.54 us: 1.21x faster                                                  |
| raytrace                   | 299 ms                                                 | 252 ms: 1.19x faster                                                   |
| spectral_norm              | 110 ms                                                 | 93.2 ms: 1.18x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 67.3 ms: 1.17x faster                                                  |
| chaos                      | 62.8 ms                                                | 53.8 ms: 1.17x faster                                                  |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.84 sec: 1.15x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                  |
| async_generators           | 384 ms                                                 | 337 ms: 1.14x faster                                                   |
| float                      | 80.8 ms                                                | 70.8 ms: 1.14x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 85.0 ms: 1.14x faster                                                  |
| generators                 | 32.2 ms                                                | 28.6 ms: 1.13x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 68.0 ms: 1.13x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.22 sec: 1.12x faster                                                 |
| scimark_fft                | 342 ms                                                 | 307 ms: 1.11x faster                                                   |
| pylint                     | 319 ms                                                 | 286 ms: 1.11x faster                                                   |
| pyflate                    | 448 ms                                                 | 405 ms: 1.11x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 62.0 ms: 1.10x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.04 us: 1.10x faster                                                  |
| richards                   | 45.9 ms                                                | 42.2 ms: 1.09x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.71 ms: 1.08x faster                                                  |
| genshi_text                | 22.8 ms                                                | 21.1 ms: 1.08x faster                                                  |
| richards_super             | 51.9 ms                                                | 48.1 ms: 1.08x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                  |
| logging_format             | 7.35 us                                                | 6.86 us: 1.07x faster                                                  |
| logging_silent             | 109 ns                                                 | 102 ns: 1.07x faster                                                   |
| html5lib                   | 63.6 ms                                                | 59.5 ms: 1.07x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 156 ms: 1.06x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.06x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 108 ms: 1.06x faster                                                   |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 132 ms: 1.05x faster                                                   |
| 2to3                       | 264 ms                                                 | 251 ms: 1.05x faster                                                   |
| json_dumps                 | 10.4 ms                                                | 9.87 ms: 1.05x faster                                                  |
| sympy_str                  | 292 ms                                                 | 278 ms: 1.05x faster                                                   |
| deltablue                  | 3.45 ms                                                | 3.29 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.46 sec: 1.04x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 721 ms: 1.03x faster                                                   |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.03x faster                                                   |
| genshi_xml                 | 50.2 ms                                                | 49.1 ms: 1.02x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.59 sec: 1.02x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 160 us: 1.02x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 83.8 ms: 1.02x faster                                                  |
| nqueens                    | 80.1 ms                                                | 79.5 ms: 1.01x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.44 ms: 1.01x slower                                                  |
| thrift                     | 791 us                                                 | 800 us: 1.01x slower                                                   |
| nbody                      | 89.3 ms                                                | 90.6 ms: 1.01x slower                                                  |
| sympy_expand               | 468 ms                                                 | 477 ms: 1.02x slower                                                   |
| sqlite_synth               | 2.20 us                                                | 2.25 us: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                  |
| django_template            | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.41 ms: 1.04x slower                                                  |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.04x slower                                                   |
| fannkuch                   | 372 ms                                                 | 388 ms: 1.04x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                   |
| json_loads                 | 26.5 us                                                | 28.0 us: 1.06x slower                                                  |
| mako                       | 11.0 ms                                                | 11.9 ms: 1.08x slower                                                  |
| pidigits                   | 184 ms                                                 | 201 ms: 1.09x slower                                                   |
| coverage                   | 71.4 ms                                                | 81.8 ms: 1.15x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.5 ms: 1.26x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.65 ms: 1.34x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.31 ms: 1.39x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.71x slower                                                  |
| telco                      | 6.53 ms                                                | 157 ms: 23.98x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 291 ms: 26.91x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_process, pickle_pure_python, json
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260301-3.15.0a6+-c9a5d9a/bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6+-c9a5d9a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.17x