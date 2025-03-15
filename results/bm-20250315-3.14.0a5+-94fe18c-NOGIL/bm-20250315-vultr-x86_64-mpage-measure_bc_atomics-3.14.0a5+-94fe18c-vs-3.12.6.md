# Results vs. 3.12.6

- fork: mpage
- ref: measure_bc_atomics
- machine: linux-x86_64
- commit hash: 94fe18c
- commit date: 2025-03-15
- overall geometric mean: 1.042x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 297 ms: 1.13x slower                                                |
| docutils       | 2.64 sec                                               | 2.79 sec: 1.06x slower                                              |
| html5lib       | 63.6 ms                                                | 69.2 ms: 1.09x slower                                               |
| Geometric mean | (ref)                                                  | 1.09x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 547 ms: 2.03x faster                                                |
| async_tree_none_tg         | 446 ms                                                 | 236 ms: 1.89x faster                                                |
| async_tree_io              | 1.08 sec                                               | 583 ms: 1.86x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.70x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 337 ms: 1.65x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 518 ms: 1.38x faster                                                |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                        |

Benchmark hidden because not significant (2): coroutines, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.9 ms: 1.06x faster                                               |
| pidigits       | 184 ms                                                 | 202 ms: 1.10x slower                                                |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                |
| Geometric mean | (ref)                                                  | 1.15x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.14x faster                                               |
| regex_dna      | 168 ms                                                 | 169 ms: 1.01x slower                                                |
| regex_compile  | 142 ms                                                 | 156 ms: 1.09x slower                                                |
| regex_v8       | 20.6 ms                                                | 23.6 ms: 1.15x slower                                               |
| Geometric mean | (ref)                                                  | 1.03x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.9 ms: 1.10x faster                                               |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.07x faster                                                |
| json_loads           | 26.5 us                                                | 29.1 us: 1.10x slower                                               |
| tomli_loads          | 2.11 sec                                               | 2.37 sec: 1.12x slower                                              |
| xml_etree_generate   | 85.2 ms                                                | 96.7 ms: 1.13x slower                                               |
| unpickle_pure_python | 221 us                                                 | 254 us: 1.15x slower                                                |
| pickle_pure_python   | 308 us                                                 | 357 us: 1.16x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 70.5 ms: 1.20x slower                                               |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.23x slower                                               |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                               |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                               |
| Geometric mean         | (ref)                                                  | 1.56x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.9 ms: 1.19x slower                                               |
| genshi_text     | 22.8 ms                                                | 27.9 ms: 1.22x slower                                               |
| django_template | 34.7 ms                                                | 43.1 ms: 1.24x slower                                               |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                               |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 547 ms: 2.03x faster                                                |
| gc_traversal               | 3.46 ms                                                | 1.74 ms: 1.98x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 236 ms: 1.89x faster                                                |
| async_tree_io              | 1.08 sec                                               | 583 ms: 1.86x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.70x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 337 ms: 1.65x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 518 ms: 1.38x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.14x faster                                               |
| deepcopy                   | 352 us                                                 | 312 us: 1.13x faster                                                |
| xml_etree_iterparse        | 96.7 ms                                                | 87.9 ms: 1.10x faster                                               |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                               |
| dulwich_log                | 78.9 ms                                                | 73.0 ms: 1.08x faster                                               |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.08x faster                                               |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.07x faster                                                |
| float                      | 80.8 ms                                                | 75.9 ms: 1.06x faster                                               |
| deepcopy_memo              | 40.3 us                                                | 38.6 us: 1.04x faster                                               |
| async_generators           | 384 ms                                                 | 374 ms: 1.03x faster                                                |
| regex_dna                  | 168 ms                                                 | 169 ms: 1.01x slower                                                |
| go                         | 139 ms                                                 | 141 ms: 1.01x slower                                                |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.01x slower                                              |
| deepcopy_reduce            | 3.08 us                                                | 3.13 us: 1.02x slower                                               |
| bpe_tokeniser              | 4.74 sec                                               | 4.82 sec: 1.02x slower                                              |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                                |
| logging_silent             | 109 ns                                                 | 112 ns: 1.03x slower                                                |
| comprehensions             | 19.8 us                                                | 20.5 us: 1.03x slower                                               |
| scimark_sor                | 130 ms                                                 | 135 ms: 1.04x slower                                                |
| docutils                   | 2.64 sec                                               | 2.79 sec: 1.06x slower                                              |
| logging_simple             | 6.63 us                                                | 7.05 us: 1.06x slower                                               |
| raytrace                   | 299 ms                                                 | 322 ms: 1.08x slower                                                |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.5 ms: 1.08x slower                                               |
| html5lib                   | 63.6 ms                                                | 69.2 ms: 1.09x slower                                               |
| thrift                     | 791 us                                                 | 862 us: 1.09x slower                                                |
| regex_compile              | 142 ms                                                 | 156 ms: 1.09x slower                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                                |
| json_loads                 | 26.5 us                                                | 29.1 us: 1.10x slower                                               |
| chaos                      | 62.8 ms                                                | 69.0 ms: 1.10x slower                                               |
| pidigits                   | 184 ms                                                 | 202 ms: 1.10x slower                                                |
| logging_format             | 7.35 us                                                | 8.08 us: 1.10x slower                                               |
| pprint_safe_repr           | 743 ms                                                 | 828 ms: 1.11x slower                                                |
| deltablue                  | 3.45 ms                                                | 3.87 ms: 1.12x slower                                               |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.12x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.71 sec: 1.12x slower                                              |
| tomli_loads                | 2.11 sec                                               | 2.37 sec: 1.12x slower                                              |
| 2to3                       | 264 ms                                                 | 297 ms: 1.13x slower                                                |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.13x slower                                                |
| pyflate                    | 448 ms                                                 | 507 ms: 1.13x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 96.7 ms: 1.13x slower                                               |
| sqlglot_transpile          | 1.67 ms                                                | 1.90 ms: 1.14x slower                                               |
| crypto_pyaes               | 76.6 ms                                                | 87.4 ms: 1.14x slower                                               |
| regex_v8                   | 20.6 ms                                                | 23.6 ms: 1.15x slower                                               |
| sqlglot_optimize           | 53.3 ms                                                | 61.2 ms: 1.15x slower                                               |
| mdp                        | 2.42 sec                                               | 2.78 sec: 1.15x slower                                              |
| unpickle_pure_python       | 221 us                                                 | 254 us: 1.15x slower                                                |
| sympy_str                  | 292 ms                                                 | 335 ms: 1.15x slower                                                |
| scimark_fft                | 342 ms                                                 | 394 ms: 1.15x slower                                                |
| pickle_pure_python         | 308 us                                                 | 357 us: 1.16x slower                                                |
| sympy_integrate            | 20.5 ms                                                | 23.9 ms: 1.16x slower                                               |
| sqlglot_parse              | 1.36 ms                                                | 1.58 ms: 1.17x slower                                               |
| richards                   | 45.9 ms                                                | 53.7 ms: 1.17x slower                                               |
| sympy_expand               | 468 ms                                                 | 551 ms: 1.18x slower                                                |
| genshi_xml                 | 50.2 ms                                                | 59.9 ms: 1.19x slower                                               |
| xml_etree_process          | 59.0 ms                                                | 70.5 ms: 1.20x slower                                               |
| typing_runtime_protocols   | 163 us                                                 | 195 us: 1.20x slower                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 82.6 ms: 1.21x slower                                               |
| richards_super             | 51.9 ms                                                | 63.2 ms: 1.22x slower                                               |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.22x slower                                               |
| genshi_text                | 22.8 ms                                                | 27.9 ms: 1.22x slower                                               |
| hexiom                     | 6.17 ms                                                | 7.57 ms: 1.23x slower                                               |
| nqueens                    | 80.1 ms                                                | 98.5 ms: 1.23x slower                                               |
| scimark_lu                 | 114 ms                                                 | 141 ms: 1.23x slower                                                |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.23x slower                                               |
| django_template            | 34.7 ms                                                | 43.1 ms: 1.24x slower                                               |
| meteor_contest             | 104 ms                                                 | 132 ms: 1.27x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.79 ms: 1.32x slower                                               |
| fannkuch                   | 372 ms                                                 | 497 ms: 1.34x slower                                                |
| telco                      | 6.53 ms                                                | 8.84 ms: 1.35x slower                                               |
| coverage                   | 71.4 ms                                                | 97.5 ms: 1.37x slower                                               |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                               |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                               |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                               |
| bench_thread_pool          | 941 us                                                 | 3.15 ms: 3.35x slower                                               |
| bench_mp_pool              | 10.8 ms                                                | 94.9 ms: 8.78x slower                                               |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                        |

Benchmark hidden because not significant (5): pylint, coroutines, asyncio_websockets, generators, json
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250315-3.14.0a5+-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5+-94fe18c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.042x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.36x