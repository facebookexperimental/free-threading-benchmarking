# Results vs. 3.12.6

- fork: python
- ref: e2118b0ac21191bfeecd
- machine: linux-x86_64
- commit hash: e2118b0
- commit date: 2026-08-25
- overall geometric mean: 1.066x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 260 ms: 1.01x faster                                                  |
| docutils       | 2.64 sec                                               | 2.36 sec: 1.12x faster                                                |
| html5lib       | 63.6 ms                                                | 58.1 ms: 1.09x faster                                                 |
| Geometric mean | (ref)                                                  | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 291 ms: 1.60x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 366 ms: 1.53x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 296 ms: 1.51x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 720 ms: 1.50x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 378 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 761 ms: 1.46x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 539 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 558 ms: 1.30x faster                                                  |
| async_generators           | 384 ms                                                 | 347 ms: 1.11x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.32x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.8 ms: 1.11x faster                                                 |
| pidigits       | 184 ms                                                 | 187 ms: 1.02x slower                                                  |
| nbody          | 89.3 ms                                                | 91.5 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.58 ms: 1.23x faster                                                 |
| regex_compile  | 142 ms                                                 | 148 ms: 1.04x slower                                                  |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                  |
| regex_v8       | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.79 sec: 1.18x faster                                                |
| json_dumps           | 10.4 ms                                                | 9.38 ms: 1.10x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 91.1 ms: 1.06x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 214 us: 1.03x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 304 us: 1.01x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 142 ms: 1.03x slower                                                  |
| json_loads           | 26.5 us                                                | 27.4 us: 1.03x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 88.3 ms: 1.04x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 62.8 ms: 1.06x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.70 ms: 1.08x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.9 ms: 1.30x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.18x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 37.0 ms: 1.07x slower                                                 |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.07x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 114 ms: 2.79x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.13 sec: 2.13x faster                                                |
| async_tree_none            | 464 ms                                                 | 291 ms: 1.60x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 366 ms: 1.53x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 296 ms: 1.51x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 720 ms: 1.50x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 27.0 us: 1.49x faster                                                 |
| deepcopy                   | 352 us                                                 | 236 us: 1.49x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 378 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 761 ms: 1.46x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 120 us: 1.36x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 539 ms: 1.33x faster                                                  |
| go                         | 139 ms                                                 | 105 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 558 ms: 1.30x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.9 us: 1.24x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.58 ms: 1.23x faster                                                 |
| spectral_norm              | 110 ms                                                 | 90.1 ms: 1.22x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.9 ms: 1.20x faster                                                 |
| scimark_sor                | 130 ms                                                 | 109 ms: 1.19x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.79 sec: 1.18x faster                                                |
| deepcopy_reduce            | 3.08 us                                                | 2.62 us: 1.17x faster                                                 |
| raytrace                   | 299 ms                                                 | 255 ms: 1.17x faster                                                  |
| chaos                      | 62.8 ms                                                | 53.8 ms: 1.17x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 68.5 ms: 1.15x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 67.4 ms: 1.14x faster                                                 |
| scimark_fft                | 342 ms                                                 | 304 ms: 1.12x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.23 sec: 1.12x faster                                                |
| pyflate                    | 448 ms                                                 | 401 ms: 1.12x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.36 sec: 1.12x faster                                                |
| float                      | 80.8 ms                                                | 72.8 ms: 1.11x faster                                                 |
| async_generators           | 384 ms                                                 | 347 ms: 1.11x faster                                                  |
| generators                 | 32.2 ms                                                | 29.2 ms: 1.11x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.00 us: 1.10x faster                                                 |
| json_dumps                 | 10.4 ms                                                | 9.38 ms: 1.10x faster                                                 |
| logging_silent             | 109 ns                                                 | 99.1 ns: 1.10x faster                                                 |
| nqueens                    | 80.1 ms                                                | 73.0 ms: 1.10x faster                                                 |
| html5lib                   | 63.6 ms                                                | 58.1 ms: 1.09x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.67 ms: 1.09x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 63.2 ms: 1.08x faster                                                 |
| logging_format             | 7.35 us                                                | 6.83 us: 1.08x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.3 ms: 1.06x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 91.1 ms: 1.06x faster                                                 |
| sympy_str                  | 292 ms                                                 | 280 ms: 1.04x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 160 ms: 1.04x faster                                                  |
| richards                   | 45.9 ms                                                | 44.4 ms: 1.03x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.47 sec: 1.03x faster                                                |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                |
| unpickle_pure_python       | 221 us                                                 | 214 us: 1.03x faster                                                  |
| json                       | 5.02 ms                                                | 4.90 ms: 1.03x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 724 ms: 1.03x faster                                                  |
| richards_super             | 51.9 ms                                                | 50.9 ms: 1.02x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.39 ms: 1.02x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                 |
| 2to3                       | 264 ms                                                 | 260 ms: 1.01x faster                                                  |
| pickle_pure_python         | 308 us                                                 | 304 us: 1.01x faster                                                  |
| sympy_expand               | 468 ms                                                 | 476 ms: 1.02x slower                                                  |
| pidigits                   | 184 ms                                                 | 187 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.25 us: 1.02x slower                                                 |
| nbody                      | 89.3 ms                                                | 91.5 ms: 1.02x slower                                                 |
| xml_etree_parse            | 139 ms                                                 | 142 ms: 1.03x slower                                                  |
| scimark_lu                 | 114 ms                                                 | 117 ms: 1.03x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.4 us: 1.03x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 88.3 ms: 1.04x slower                                                 |
| regex_compile              | 142 ms                                                 | 148 ms: 1.04x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                  |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.8 ms: 1.06x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 62.8 ms: 1.06x slower                                                 |
| django_template            | 34.7 ms                                                | 37.0 ms: 1.07x slower                                                 |
| mako                       | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.70 ms: 1.08x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 3.76 ms: 1.09x slower                                                 |
| coverage                   | 71.4 ms                                                | 85.4 ms: 1.20x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.9 ms: 1.30x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.35 ms: 1.44x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.64 ms: 1.51x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 229 ms: 21.19x slower                                                 |
| telco                      | 6.53 ms                                                | 161 ms: 24.60x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (4): meteor_contest, thrift, scimark_sparse_mat_mult, fannkuch
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260825-3.16.0a0-e2118b0/bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.066x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x