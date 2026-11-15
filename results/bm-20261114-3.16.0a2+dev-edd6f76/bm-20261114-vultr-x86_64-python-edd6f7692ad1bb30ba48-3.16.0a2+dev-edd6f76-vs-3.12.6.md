# Results vs. 3.12.6

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: linux-x86_64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.092x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                                      |
| docutils       | 2.64 sec                                               | 2.28 sec: 1.16x faster                                                    |
| html5lib       | 63.6 ms                                                | 58.4 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                  | 1.10x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_generators           | 384 ms                                                 | 227 ms: 1.70x faster                                                      |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.69x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 660 ms: 1.64x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 344 ms: 1.63x faster                                                      |
| async_tree_io_tg           | 1.11 sec                                               | 688 ms: 1.61x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 347 ms: 1.60x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 283 ms: 1.58x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 513 ms: 1.41x faster                                                      |
| asyncio_tcp                | 519 ms                                                 | 447 ms: 1.16x faster                                                      |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.46 sec: 1.03x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                      |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 71.8 ms: 1.12x faster                                                     |
| pidigits       | 184 ms                                                 | 178 ms: 1.04x faster                                                      |
| nbody          | 89.3 ms                                                | 90.3 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                  | 1.05x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.65 ms: 1.20x faster                                                     |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                     |
| regex_dna      | 168 ms                                                 | 172 ms: 1.03x slower                                                      |
| regex_compile  | 142 ms                                                 | 147 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                  | 1.03x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.79 sec: 1.18x faster                                                    |
| json_dumps           | 10.4 ms                                                | 9.27 ms: 1.12x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 91.8 ms: 1.05x faster                                                     |
| unpickle_pure_python | 221 us                                                 | 211 us: 1.04x faster                                                      |
| xml_etree_generate   | 85.2 ms                                                | 86.4 ms: 1.01x slower                                                     |
| unpickle             | 14.1 us                                                | 14.3 us: 1.02x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 315 us: 1.02x slower                                                      |
| json_loads           | 26.5 us                                                | 27.3 us: 1.03x slower                                                     |
| xml_etree_parse      | 139 ms                                                 | 144 ms: 1.04x slower                                                      |
| xml_etree_process    | 59.0 ms                                                | 61.9 ms: 1.05x slower                                                     |
| pickle_dict          | 31.8 us                                                | 33.5 us: 1.06x slower                                                     |
| unpickle_list        | 4.67 us                                                | 5.11 us: 1.09x slower                                                     |
| pickle_list          | 4.77 us                                                | 5.42 us: 1.14x slower                                                     |
| pickle               | 10.9 us                                                | 12.6 us: 1.15x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.32 ms: 1.02x slower                                                     |
| python_startup         | 9.93 ms                                                | 11.0 ms: 1.11x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                | 11.4 ms: 1.04x slower                                                     |
| django_template | 34.7 ms                                                | 36.3 ms: 1.05x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 108 ms: 2.96x faster                                                      |
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.12x faster                                                    |
| async_generators           | 384 ms                                                 | 227 ms: 1.70x faster                                                      |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.69x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 660 ms: 1.64x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 344 ms: 1.63x faster                                                      |
| async_tree_io_tg           | 1.11 sec                                               | 688 ms: 1.61x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 347 ms: 1.60x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 283 ms: 1.58x faster                                                      |
| deepcopy                   | 352 us                                                 | 232 us: 1.52x faster                                                      |
| typing_runtime_protocols   | 163 us                                                 | 108 us: 1.51x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 27.8 us: 1.45x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 503 ms: 1.42x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 513 ms: 1.41x faster                                                      |
| go                         | 139 ms                                                 | 104 ms: 1.34x faster                                                      |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                     |
| spectral_norm              | 110 ms                                                 | 89.4 ms: 1.23x faster                                                     |
| pathlib                    | 21.5 ms                                                | 17.8 ms: 1.21x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.54 us: 1.21x faster                                                     |
| scimark_sor                | 130 ms                                                 | 108 ms: 1.20x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.65 ms: 1.20x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 66.5 ms: 1.18x faster                                                     |
| tomli_loads                | 2.11 sec                                               | 1.79 sec: 1.18x faster                                                    |
| raytrace                   | 299 ms                                                 | 257 ms: 1.16x faster                                                      |
| asyncio_tcp                | 519 ms                                                 | 447 ms: 1.16x faster                                                      |
| docutils                   | 2.64 sec                                               | 2.28 sec: 1.16x faster                                                    |
| crypto_pyaes               | 76.6 ms                                                | 66.3 ms: 1.15x faster                                                     |
| chaos                      | 62.8 ms                                                | 54.7 ms: 1.15x faster                                                     |
| generators                 | 32.2 ms                                                | 28.1 ms: 1.15x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.16 sec: 1.14x faster                                                    |
| pyflate                    | 448 ms                                                 | 398 ms: 1.12x faster                                                      |
| float                      | 80.8 ms                                                | 71.8 ms: 1.12x faster                                                     |
| scimark_fft                | 342 ms                                                 | 304 ms: 1.12x faster                                                      |
| json_dumps                 | 10.4 ms                                                | 9.27 ms: 1.12x faster                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 62.0 ms: 1.10x faster                                                     |
| logging_silent             | 109 ns                                                 | 98.8 ns: 1.10x faster                                                     |
| unpack_sequence            | 52.1 ns                                                | 47.5 ns: 1.10x faster                                                     |
| hexiom                     | 6.17 ms                                                | 5.63 ms: 1.10x faster                                                     |
| html5lib                   | 63.6 ms                                                | 58.4 ms: 1.09x faster                                                     |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                                     |
| nqueens                    | 80.1 ms                                                | 74.2 ms: 1.08x faster                                                     |
| logging_simple             | 6.63 us                                                | 6.20 us: 1.07x faster                                                     |
| sympy_sum                  | 166 ms                                                 | 157 ms: 1.06x faster                                                      |
| logging_format             | 7.35 us                                                | 6.97 us: 1.05x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 91.8 ms: 1.05x faster                                                     |
| unpickle_pure_python       | 221 us                                                 | 211 us: 1.04x faster                                                      |
| 2to3                       | 264 ms                                                 | 253 ms: 1.04x faster                                                      |
| sympy_str                  | 292 ms                                                 | 280 ms: 1.04x faster                                                      |
| deltablue                  | 3.45 ms                                                | 3.32 ms: 1.04x faster                                                     |
| pidigits                   | 184 ms                                                 | 178 ms: 1.04x faster                                                      |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.46 sec: 1.03x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.4 ms: 1.02x faster                                                     |
| meteor_contest             | 104 ms                                                 | 101 ms: 1.02x faster                                                      |
| pprint_pformat             | 1.52 sec                                               | 1.49 sec: 1.02x faster                                                    |
| pprint_safe_repr           | 743 ms                                                 | 731 ms: 1.02x faster                                                      |
| json                       | 5.02 ms                                                | 4.94 ms: 1.02x faster                                                     |
| richards_super             | 51.9 ms                                                | 51.2 ms: 1.01x faster                                                     |
| richards                   | 45.9 ms                                                | 45.4 ms: 1.01x faster                                                     |
| fannkuch                   | 372 ms                                                 | 374 ms: 1.00x slower                                                      |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                                    |
| nbody                      | 89.3 ms                                                | 90.3 ms: 1.01x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 86.4 ms: 1.01x slower                                                     |
| sympy_expand               | 468 ms                                                 | 474 ms: 1.01x slower                                                      |
| unpickle                   | 14.1 us                                                | 14.3 us: 1.02x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 7.32 ms: 1.02x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 315 us: 1.02x slower                                                      |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.03x slower                                                      |
| json_loads                 | 26.5 us                                                | 27.3 us: 1.03x slower                                                     |
| regex_compile              | 142 ms                                                 | 147 ms: 1.03x slower                                                      |
| mako                       | 11.0 ms                                                | 11.4 ms: 1.04x slower                                                     |
| gc_traversal               | 3.46 ms                                                | 3.60 ms: 1.04x slower                                                     |
| xml_etree_parse            | 139 ms                                                 | 144 ms: 1.04x slower                                                      |
| scimark_lu                 | 114 ms                                                 | 119 ms: 1.04x slower                                                      |
| django_template            | 34.7 ms                                                | 36.3 ms: 1.05x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 61.9 ms: 1.05x slower                                                     |
| asyncio_websockets         | 517 ms                                                 | 544 ms: 1.05x slower                                                      |
| pickle_dict                | 31.8 us                                                | 33.5 us: 1.06x slower                                                     |
| unpickle_list              | 4.67 us                                                | 5.11 us: 1.09x slower                                                     |
| python_startup             | 9.93 ms                                                | 11.0 ms: 1.11x slower                                                     |
| pickle_list                | 4.77 us                                                | 5.42 us: 1.14x slower                                                     |
| pickle                     | 10.9 us                                                | 12.6 us: 1.15x slower                                                     |
| coverage                   | 71.4 ms                                                | 84.5 ms: 1.18x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.37 ms: 1.26x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.33 ms: 1.41x slower                                                     |
| telco                      | 6.53 ms                                                | 161 ms: 24.61x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 276 ms: 25.56x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                              |

Benchmark hidden because not significant (3): sqlite_synth, scimark_sparse_mat_mult, thrift
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20261114-3.16.0a2+dev-edd6f76/bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.092x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x