# Results vs. 3.12.6

- fork: python
- ref: f0dcb29d3affbbe1ec25
- machine: linux-x86_64
- commit hash: f0dcb29
- commit date: 2025-04-07
- overall geometric mean: 1.090x faster
- HPT reliability: 98.30%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 268 ms: 1.02x slower                                                   |
| html5lib       | 63.6 ms                                                | 60.7 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 476 ms: 2.33x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 208 ms: 2.14x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 262 ms: 2.14x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 508 ms: 2.13x faster                                                   |
| async_tree_none            | 464 ms                                                 | 242 ms: 1.92x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 290 ms: 1.91x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 426 ms: 1.69x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 456 ms: 1.57x faster                                                   |
| async_generators           | 384 ms                                                 | 321 ms: 1.20x faster                                                   |
| coroutines                 | 23.9 ms                                                | 20.0 ms: 1.20x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.69x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 64.2 ms: 1.26x faster                                                  |
| pidigits       | 184 ms                                                 | 187 ms: 1.01x slower                                                   |
| nbody          | 89.3 ms                                                | 110 ms: 1.23x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 134 ms: 1.06x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 3.03 ms: 1.05x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                  |
| regex_dna      | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 84.3 ms: 1.15x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 1.94 sec: 1.09x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 218 us: 1.01x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 142 ms: 1.02x slower                                                   |
| xml_etree_process    | 59.0 ms                                                | 60.4 ms: 1.02x slower                                                  |
| json_loads           | 26.5 us                                                | 28.8 us: 1.09x slower                                                  |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (2): pickle_pure_python, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.0 ms: 1.54x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.56x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 50.5 ms: 1.01x slower                                                  |
| genshi_text     | 22.8 ms                                                | 23.0 ms: 1.01x slower                                                  |
| django_template | 34.7 ms                                                | 36.1 ms: 1.04x slower                                                  |
| mako            | 11.0 ms                                                | 14.1 ms: 1.28x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.08x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 476 ms: 2.33x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 208 ms: 2.14x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 262 ms: 2.14x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 508 ms: 2.13x faster                                                   |
| mdp                        | 2.42 sec                                               | 1.23 sec: 1.96x faster                                                 |
| async_tree_none            | 464 ms                                                 | 242 ms: 1.92x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 290 ms: 1.91x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 426 ms: 1.69x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 2.11 ms: 1.64x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 456 ms: 1.57x faster                                                   |
| logging_silent             | 109 ns                                                 | 78.6 ns: 1.39x faster                                                  |
| deepcopy                   | 352 us                                                 | 254 us: 1.39x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 31.6 us: 1.27x faster                                                  |
| float                      | 80.8 ms                                                | 64.2 ms: 1.26x faster                                                  |
| scimark_sor                | 130 ms                                                 | 106 ms: 1.23x faster                                                   |
| go                         | 139 ms                                                 | 116 ms: 1.20x faster                                                   |
| async_generators           | 384 ms                                                 | 321 ms: 1.20x faster                                                   |
| coroutines                 | 23.9 ms                                                | 20.0 ms: 1.20x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.59 us: 1.19x faster                                                  |
| spectral_norm              | 110 ms                                                 | 93.5 ms: 1.18x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.0 us: 1.17x faster                                                  |
| generators                 | 32.2 ms                                                | 27.7 ms: 1.16x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.6 ms: 1.16x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 84.3 ms: 1.15x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.19 sec: 1.13x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 1.95 us: 1.13x faster                                                  |
| chaos                      | 62.8 ms                                                | 55.8 ms: 1.13x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 70.4 ms: 1.12x faster                                                  |
| raytrace                   | 299 ms                                                 | 267 ms: 1.12x faster                                                   |
| pylint                     | 319 ms                                                 | 291 ms: 1.10x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.94 sec: 1.09x faster                                                 |
| scimark_fft                | 342 ms                                                 | 316 ms: 1.08x faster                                                   |
| regex_compile              | 142 ms                                                 | 134 ms: 1.06x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 64.8 ms: 1.06x faster                                                  |
| html5lib                   | 63.6 ms                                                | 60.7 ms: 1.05x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 3.03 ms: 1.05x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.42 us: 1.03x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.01x faster                                                 |
| nqueens                    | 80.1 ms                                                | 79.1 ms: 1.01x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.41 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 218 us: 1.01x faster                                                   |
| hexiom                     | 6.17 ms                                                | 6.11 ms: 1.01x faster                                                  |
| logging_format             | 7.35 us                                                | 7.28 us: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 746 ms: 1.00x slower                                                   |
| genshi_xml                 | 50.2 ms                                                | 50.5 ms: 1.01x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 77.1 ms: 1.01x slower                                                  |
| sympy_str                  | 292 ms                                                 | 294 ms: 1.01x slower                                                   |
| genshi_text                | 22.8 ms                                                | 23.0 ms: 1.01x slower                                                  |
| pidigits                   | 184 ms                                                 | 187 ms: 1.01x slower                                                   |
| json                       | 5.02 ms                                                | 5.10 ms: 1.01x slower                                                  |
| 2to3                       | 264 ms                                                 | 268 ms: 1.02x slower                                                   |
| xml_etree_parse            | 139 ms                                                 | 142 ms: 1.02x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 60.4 ms: 1.02x slower                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 146 ms: 1.02x slower                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.52 ms: 1.03x slower                                                  |
| richards_super             | 51.9 ms                                                | 53.7 ms: 1.04x slower                                                  |
| django_template            | 34.7 ms                                                | 36.1 ms: 1.04x slower                                                  |
| sympy_expand               | 468 ms                                                 | 489 ms: 1.05x slower                                                   |
| typing_runtime_protocols   | 163 us                                                 | 171 us: 1.05x slower                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 22.8 ms: 1.05x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.7 ms: 1.05x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.8 us: 1.09x slower                                                  |
| fannkuch                   | 372 ms                                                 | 416 ms: 1.12x slower                                                   |
| regex_dna                  | 168 ms                                                 | 188 ms: 1.12x slower                                                   |
| meteor_contest             | 104 ms                                                 | 120 ms: 1.16x slower                                                   |
| telco                      | 6.53 ms                                                | 7.60 ms: 1.16x slower                                                  |
| nbody                      | 89.3 ms                                                | 110 ms: 1.23x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.23x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.36 ms: 1.24x slower                                                  |
| mako                       | 11.0 ms                                                | 14.1 ms: 1.28x slower                                                  |
| coverage                   | 71.4 ms                                                | 93.4 ms: 1.31x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 11.0 ms: 1.54x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 3.07 ms: 3.26x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 93.9 ms: 8.70x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (8): richards, sympy_sum, docutils, pyflate, sympy_integrate, pickle_pure_python, xml_etree_generate, pprint_pformat
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250407-3.14.0a6+-f0dcb29-CLANG,NOGIL/bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 98.30% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.41x