# Results vs. 3.12.6

- fork: python
- ref: 3db3bba4d1feb3a9fbfc
- machine: linux-x86_64
- commit hash: 3db3bba
- commit date: 2026-06-24
- overall geometric mean: 1.030x slower
- HPT reliability: 84.10%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 293 ms: 1.11x slower                                                  |
| docutils       | 2.64 sec                                               | 2.97 sec: 1.13x slower                                                |
| html5lib       | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 674 ms: 1.65x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 698 ms: 1.55x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 390 ms: 1.44x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 322 ms: 1.39x faster                                                  |
| async_tree_none            | 464 ms                                                 | 337 ms: 1.38x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 414 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 577 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 595 ms: 1.20x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| async_generators           | 384 ms                                                 | 387 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 187 ms: 1.02x slower                                                  |
| float          | 80.8 ms                                                | 85.0 ms: 1.05x slower                                                 |
| nbody          | 89.3 ms                                                | 126 ms: 1.42x slower                                                  |
| Geometric mean | (ref)                                                  | 1.15x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                 |
| regex_dna      | 168 ms                                                 | 162 ms: 1.04x faster                                                  |
| regex_compile  | 142 ms                                                 | 138 ms: 1.03x faster                                                  |
| regex_v8       | 20.6 ms                                                | 20.4 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.96 sec: 1.08x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 94.9 ms: 1.02x faster                                                 |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.02x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 142 ms: 1.02x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 236 us: 1.07x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 336 us: 1.09x slower                                                  |
| json_loads           | 26.5 us                                                | 30.2 us: 1.14x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.19x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 74.8 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.21 ms: 1.29x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.56x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.42x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 40.1 ms: 1.16x slower                                                 |
| mako            | 11.0 ms                                                | 16.2 ms: 1.47x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 134 ms: 2.38x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.78 ms: 1.94x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.85x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 674 ms: 1.65x faster                                                  |
| bench_mp_pool              | 10.8 ms                                                | 6.79 ms: 1.59x faster                                                 |
| async_tree_io              | 1.08 sec                                               | 698 ms: 1.55x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 390 ms: 1.44x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 322 ms: 1.39x faster                                                  |
| async_tree_none            | 464 ms                                                 | 337 ms: 1.38x faster                                                  |
| deepcopy                   | 352 us                                                 | 261 us: 1.35x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 414 ms: 1.34x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 30.6 us: 1.32x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 577 ms: 1.25x faster                                                  |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                 |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 595 ms: 1.20x faster                                                  |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.78 ms: 1.14x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.5 us: 1.13x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 144 us: 1.13x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 1.96 us: 1.12x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 72.0 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.37 sec: 1.08x faster                                                |
| deepcopy_reduce            | 3.08 us                                                | 2.86 us: 1.08x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.96 sec: 1.08x faster                                                |
| scimark_sor                | 130 ms                                                 | 122 ms: 1.07x faster                                                  |
| logging_silent             | 109 ns                                                 | 103 ns: 1.05x faster                                                  |
| regex_dna                  | 168 ms                                                 | 162 ms: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                |
| regex_compile              | 142 ms                                                 | 138 ms: 1.03x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 94.9 ms: 1.02x faster                                                 |
| regex_v8                   | 20.6 ms                                                | 20.4 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 513 ms: 1.01x faster                                                  |
| chaos                      | 62.8 ms                                                | 62.5 ms: 1.01x faster                                                 |
| raytrace                   | 299 ms                                                 | 301 ms: 1.01x slower                                                  |
| async_generators           | 384 ms                                                 | 387 ms: 1.01x slower                                                  |
| pidigits                   | 184 ms                                                 | 187 ms: 1.02x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.02x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 142 ms: 1.02x slower                                                  |
| scimark_fft                | 342 ms                                                 | 349 ms: 1.02x slower                                                  |
| pyflate                    | 448 ms                                                 | 459 ms: 1.02x slower                                                  |
| html5lib                   | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                 |
| generators                 | 32.2 ms                                                | 33.2 ms: 1.03x slower                                                 |
| logging_simple             | 6.63 us                                                | 6.88 us: 1.04x slower                                                 |
| float                      | 80.8 ms                                                | 85.0 ms: 1.05x slower                                                 |
| json                       | 5.02 ms                                                | 5.29 ms: 1.05x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.53 ms: 1.06x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.66 ms: 1.06x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.06x slower                                                 |
| logging_format             | 7.35 us                                                | 7.87 us: 1.07x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 236 us: 1.07x slower                                                  |
| sympy_str                  | 292 ms                                                 | 313 ms: 1.07x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 179 ms: 1.08x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 804 ms: 1.08x slower                                                  |
| nqueens                    | 80.1 ms                                                | 87.3 ms: 1.09x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 336 us: 1.09x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.67 sec: 1.10x slower                                                |
| 2to3                       | 264 ms                                                 | 293 ms: 1.11x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 128 ms: 1.12x slower                                                  |
| sympy_expand               | 468 ms                                                 | 525 ms: 1.12x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.97 sec: 1.13x slower                                                |
| richards                   | 45.9 ms                                                | 52.2 ms: 1.14x slower                                                 |
| json_loads                 | 26.5 us                                                | 30.2 us: 1.14x slower                                                 |
| richards_super             | 51.9 ms                                                | 59.6 ms: 1.15x slower                                                 |
| django_template            | 34.7 ms                                                | 40.1 ms: 1.16x slower                                                 |
| thrift                     | 791 us                                                 | 918 us: 1.16x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 79.3 ms: 1.16x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 89.0 ms: 1.16x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.19x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.23x slower                                                 |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.24x slower                                                  |
| fannkuch                   | 372 ms                                                 | 463 ms: 1.24x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.51 ms: 1.26x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 74.8 ms: 1.27x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.21 ms: 1.29x slower                                                 |
| nbody                      | 89.3 ms                                                | 126 ms: 1.42x slower                                                  |
| mako                       | 11.0 ms                                                | 16.2 ms: 1.47x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.56x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.48 ms: 1.57x slower                                                 |
| coverage                   | 71.4 ms                                                | 113 ms: 1.59x slower                                                  |
| telco                      | 6.53 ms                                                | 176 ms: 27.00x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (1): spectral_norm
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260624-3.16.0a0-3db3bba-NOGIL/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.030x slower

# HPT report

- Reliability score: 84.10% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x