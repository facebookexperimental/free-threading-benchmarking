# Results vs. 3.12.6

- fork: python
- ref: 3db3bba4d1feb3a9fbfc
- machine: linux-x86_64
- commit hash: 3db3bba
- commit date: 2026-06-24
- overall geometric mean: 1.075x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                                  |
| docutils       | 2.64 sec                                               | 2.38 sec: 1.11x faster                                                |
| html5lib       | 63.6 ms                                                | 59.0 ms: 1.08x faster                                                 |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 289 ms: 1.61x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 368 ms: 1.52x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 720 ms: 1.50x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 301 ms: 1.48x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 376 ms: 1.48x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 767 ms: 1.45x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 546 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 558 ms: 1.29x faster                                                  |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.32x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 74.1 ms: 1.09x faster                                                 |
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| nbody          | 89.3 ms                                                | 91.8 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 120 ms: 1.19x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                 |
| regex_dna      | 168 ms                                                 | 177 ms: 1.06x slower                                                  |
| regex_v8       | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 90.0 ms: 1.07x faster                                                 |
| json_dumps           | 10.4 ms                                                | 9.79 ms: 1.06x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.05x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 85.6 ms: 1.00x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 60.4 ms: 1.02x slower                                                 |
| json_loads           | 26.5 us                                                | 27.3 us: 1.03x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 143 ms: 1.03x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 6.94 ms: 1.03x faster                                                 |
| python_startup         | 9.93 ms                                                | 12.3 ms: 1.24x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 35.7 ms: 1.03x slower                                                 |
| mako            | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 114 ms: 2.80x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.13 sec: 2.14x faster                                                |
| async_tree_none            | 464 ms                                                 | 289 ms: 1.61x faster                                                  |
| deepcopy                   | 352 us                                                 | 229 us: 1.54x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 26.4 us: 1.52x faster                                                 |
| async_tree_memoization_tg  | 560 ms                                                 | 368 ms: 1.52x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 720 ms: 1.50x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 301 ms: 1.48x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 376 ms: 1.48x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 767 ms: 1.45x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 117 us: 1.39x faster                                                  |
| go                         | 139 ms                                                 | 102 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 546 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 558 ms: 1.29x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.6 us: 1.27x faster                                                 |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.53 us: 1.22x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                 |
| raytrace                   | 299 ms                                                 | 250 ms: 1.20x faster                                                  |
| regex_compile              | 142 ms                                                 | 120 ms: 1.19x faster                                                  |
| spectral_norm              | 110 ms                                                 | 93.9 ms: 1.17x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 67.4 ms: 1.17x faster                                                 |
| chaos                      | 62.8 ms                                                | 54.1 ms: 1.16x faster                                                 |
| generators                 | 32.2 ms                                                | 27.9 ms: 1.16x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                  |
| logging_silent             | 109 ns                                                 | 96.0 ns: 1.14x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.20 sec: 1.13x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                 |
| pyflate                    | 448 ms                                                 | 402 ms: 1.12x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.38 sec: 1.11x faster                                                |
| crypto_pyaes               | 76.6 ms                                                | 69.2 ms: 1.11x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.61 ms: 1.10x faster                                                 |
| richards                   | 45.9 ms                                                | 42.0 ms: 1.09x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.07 us: 1.09x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 62.8 ms: 1.09x faster                                                 |
| float                      | 80.8 ms                                                | 74.1 ms: 1.09x faster                                                 |
| richards_super             | 51.9 ms                                                | 48.0 ms: 1.08x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                                 |
| html5lib                   | 63.6 ms                                                | 59.0 ms: 1.08x faster                                                 |
| nqueens                    | 80.1 ms                                                | 74.3 ms: 1.08x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 90.0 ms: 1.07x faster                                                 |
| sympy_str                  | 292 ms                                                 | 273 ms: 1.07x faster                                                  |
| scimark_fft                | 342 ms                                                 | 321 ms: 1.06x faster                                                  |
| logging_format             | 7.35 us                                                | 6.90 us: 1.06x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.25 ms: 1.06x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 156 ms: 1.06x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.79 ms: 1.06x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.05x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                |
| meteor_contest             | 104 ms                                                 | 99.1 ms: 1.04x faster                                                 |
| 2to3                       | 264 ms                                                 | 253 ms: 1.04x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.47 sec: 1.04x faster                                                |
| python_startup_no_site     | 7.16 ms                                                | 6.94 ms: 1.03x faster                                                 |
| thrift                     | 791 us                                                 | 770 us: 1.03x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 723 ms: 1.03x faster                                                  |
| sympy_expand               | 468 ms                                                 | 456 ms: 1.03x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 113 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                 |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 85.6 ms: 1.00x slower                                                 |
| json                       | 5.02 ms                                                | 5.08 ms: 1.01x slower                                                 |
| fannkuch                   | 372 ms                                                 | 378 ms: 1.02x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 60.4 ms: 1.02x slower                                                 |
| nbody                      | 89.3 ms                                                | 91.8 ms: 1.03x slower                                                 |
| django_template            | 34.7 ms                                                | 35.7 ms: 1.03x slower                                                 |
| json_loads                 | 26.5 us                                                | 27.3 us: 1.03x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 143 ms: 1.03x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                  |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.06x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 3.72 ms: 1.08x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.74 ms: 1.08x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 22.2 ms: 1.08x slower                                                 |
| mako                       | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                 |
| coverage                   | 71.4 ms                                                | 83.9 ms: 1.17x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.3 ms: 1.24x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.33 ms: 1.42x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.68 ms: 1.53x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 227 ms: 21.05x slower                                                 |
| telco                      | 6.53 ms                                                | 158 ms: 24.20x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (2): pickle_pure_python, sqlite_synth
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260624-3.16.0a0-3db3bba/bm-20260624-vultr-x86_64-python-3db3bba4d1feb3a9fbfc-3.16.0a0-3db3bba.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.075x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.14x