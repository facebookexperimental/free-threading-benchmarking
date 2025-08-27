# Results vs. 3.12.6

- fork: python
- ref: ffaec6e2a11fb7b41fac
- machine: linux-x86_64
- commit hash: ffaec6e
- commit date: 2025-08-27
- overall geometric mean: 1.073x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.05x faster                                                  |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                |
| html5lib       | 63.6 ms                                                | 61.5 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                  |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.82x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 619 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 314 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                  |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.1 ms: 1.12x faster                                                 |
| nbody          | 89.3 ms                                                | 91.3 ms: 1.02x slower                                                 |
| pidigits       | 184 ms                                                 | 218 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.60 ms: 1.22x faster                                                 |
| regex_compile  | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| regex_dna      | 168 ms                                                 | 167 ms: 1.01x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.89 sec: 1.12x faster                                                |
| json_dumps           | 10.4 ms                                                | 9.69 ms: 1.07x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 210 us: 1.05x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 92.6 ms: 1.04x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 57.8 ms: 1.02x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 304 us: 1.01x faster                                                  |
| json_loads           | 26.5 us                                                | 28.3 us: 1.07x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.21 ms: 1.01x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.12x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                 |
| genshi_xml     | 50.2 ms                                                | 48.9 ms: 1.03x faster                                                 |
| mako           | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.09x faster                                                |
| async_tree_io              | 1.08 sec                                               | 594 ms: 1.82x faster                                                  |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.82x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 619 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 314 ms: 1.77x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.44x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 505 ms: 1.43x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 28.8 us: 1.40x faster                                                 |
| deepcopy                   | 352 us                                                 | 252 us: 1.40x faster                                                  |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.6 us: 1.27x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.60 ms: 1.22x faster                                                 |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.20x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 66.1 ms: 1.19x faster                                                 |
| raytrace                   | 299 ms                                                 | 251 ms: 1.19x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.61 us: 1.18x faster                                                 |
| generators                 | 32.2 ms                                                | 27.6 ms: 1.17x faster                                                 |
| spectral_norm              | 110 ms                                                 | 94.4 ms: 1.17x faster                                                 |
| regex_compile              | 142 ms                                                 | 123 ms: 1.16x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.74 us: 1.15x faster                                                 |
| logging_format             | 7.35 us                                                | 6.44 us: 1.14x faster                                                 |
| pylint                     | 319 ms                                                 | 279 ms: 1.14x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.1 ms: 1.13x faster                                                 |
| async_generators           | 384 ms                                                 | 340 ms: 1.13x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.20 sec: 1.13x faster                                                |
| chaos                      | 62.8 ms                                                | 55.8 ms: 1.13x faster                                                 |
| pyflate                    | 448 ms                                                 | 399 ms: 1.12x faster                                                  |
| float                      | 80.8 ms                                                | 72.1 ms: 1.12x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.08 ms: 1.12x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.89 sec: 1.12x faster                                                |
| richards                   | 45.9 ms                                                | 41.3 ms: 1.11x faster                                                 |
| logging_silent             | 109 ns                                                 | 98.5 ns: 1.11x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 69.3 ms: 1.11x faster                                                 |
| richards_super             | 51.9 ms                                                | 47.0 ms: 1.10x faster                                                 |
| genshi_text                | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.63 ms: 1.10x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 18.8 ms: 1.09x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 680 ms: 1.09x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.39 sec: 1.09x faster                                                |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.09x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 63.0 ms: 1.09x faster                                                 |
| sympy_str                  | 292 ms                                                 | 269 ms: 1.08x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.08 sec: 1.08x faster                                                |
| thrift                     | 791 us                                                 | 738 us: 1.07x faster                                                  |
| json_dumps                 | 10.4 ms                                                | 9.69 ms: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 154 us: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 250 ms: 1.05x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 210 us: 1.05x faster                                                  |
| nqueens                    | 80.1 ms                                                | 76.4 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 92.6 ms: 1.04x faster                                                 |
| meteor_contest             | 104 ms                                                 | 99.9 ms: 1.04x faster                                                 |
| html5lib                   | 63.6 ms                                                | 61.5 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 82.4 ms: 1.03x faster                                                 |
| scimark_fft                | 342 ms                                                 | 331 ms: 1.03x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                |
| genshi_xml                 | 50.2 ms                                                | 48.9 ms: 1.03x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 57.8 ms: 1.02x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                 |
| pickle_pure_python         | 308 us                                                 | 304 us: 1.01x faster                                                  |
| regex_dna                  | 168 ms                                                 | 167 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.21 ms: 1.01x slower                                                 |
| fannkuch                   | 372 ms                                                 | 380 ms: 1.02x slower                                                  |
| nbody                      | 89.3 ms                                                | 91.3 ms: 1.02x slower                                                 |
| json                       | 5.02 ms                                                | 5.21 ms: 1.04x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.29 us: 1.04x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                 |
| json_loads                 | 26.5 us                                                | 28.3 us: 1.07x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.70 ms: 1.07x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.01 ms: 1.07x slower                                                 |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| coverage                   | 71.4 ms                                                | 81.9 ms: 1.15x slower                                                 |
| pidigits                   | 184 ms                                                 | 218 ms: 1.19x slower                                                  |
| python_startup             | 9.93 ms                                                | 12.4 ms: 1.25x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.37 ms: 1.26x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.93 ms: 1.77x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.56x slower                                                  |
| telco                      | 6.53 ms                                                | 158 ms: 24.14x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (3): sympy_expand, django_template, asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.073x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x