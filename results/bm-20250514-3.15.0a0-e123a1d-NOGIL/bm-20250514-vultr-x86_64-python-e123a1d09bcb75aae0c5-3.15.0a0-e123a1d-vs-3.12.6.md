# Results vs. 3.12.6

- fork: python
- ref: e123a1d09bcb75aae0c5
- machine: linux-x86_64
- commit hash: e123a1d
- commit date: 2025-05-14
- overall geometric mean: 1.014x faster
- HPT reliability: 86.40%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 285 ms: 1.08x slower                                                  |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 65.8 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 521 ms: 2.13x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 550 ms: 1.97x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.96x faster                                                  |
| async_tree_none            | 464 ms                                                 | 261 ms: 1.78x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 510 ms: 1.40x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                 |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.54x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.0 ms: 1.15x faster                                                 |
| pidigits       | 184 ms                                                 | 199 ms: 1.08x slower                                                  |
| nbody          | 89.3 ms                                                | 120 ms: 1.34x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                 |
| regex_compile  | 142 ms                                                 | 145 ms: 1.02x slower                                                  |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                 |
| regex_dna      | 168 ms                                                 | 177 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.3 ms: 1.09x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                |
| unpickle_pure_python | 221 us                                                 | 229 us: 1.04x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 334 us: 1.09x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 95.4 ms: 1.12x slower                                                 |
| json_loads           | 26.5 us                                                | 30.6 us: 1.15x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.6 ms: 1.16x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                 |
| python_startup         | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.8 ms: 1.11x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.2 ms: 1.15x slower                                                 |
| django_template | 34.7 ms                                                | 40.5 ms: 1.17x slower                                                 |
| mako            | 11.0 ms                                                | 15.6 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.20x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 521 ms: 2.13x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 284 ms: 1.97x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 550 ms: 1.97x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 227 ms: 1.96x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.89 ms: 1.83x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                                |
| async_tree_none            | 464 ms                                                 | 261 ms: 1.78x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 510 ms: 1.40x faster                                                  |
| deepcopy                   | 352 us                                                 | 292 us: 1.21x faster                                                  |
| float                      | 80.8 ms                                                | 70.0 ms: 1.15x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 35.5 us: 1.14x faster                                                 |
| go                         | 139 ms                                                 | 123 ms: 1.13x faster                                                  |
| generators                 | 32.2 ms                                                | 28.9 ms: 1.12x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.0 ms: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.6 ms: 1.10x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 88.3 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.43 sec: 1.07x faster                                                |
| scimark_sor                | 130 ms                                                 | 122 ms: 1.07x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.07 us: 1.06x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| pylint                     | 319 ms                                                 | 304 ms: 1.05x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.0 ms: 1.04x faster                                                 |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                |
| deepcopy_reduce            | 3.08 us                                                | 2.99 us: 1.03x faster                                                 |
| comprehensions             | 19.8 us                                                | 19.3 us: 1.03x faster                                                 |
| raytrace                   | 299 ms                                                 | 294 ms: 1.02x faster                                                  |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| chaos                      | 62.8 ms                                                | 62.1 ms: 1.01x faster                                                 |
| regex_compile              | 142 ms                                                 | 145 ms: 1.02x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                |
| deltablue                  | 3.45 ms                                                | 3.53 ms: 1.02x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                |
| json                       | 5.02 ms                                                | 5.16 ms: 1.03x slower                                                 |
| html5lib                   | 63.6 ms                                                | 65.8 ms: 1.04x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 229 us: 1.04x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 776 ms: 1.04x slower                                                  |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.05x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.61 sec: 1.06x slower                                                |
| hexiom                     | 6.17 ms                                                | 6.58 ms: 1.07x slower                                                 |
| scimark_fft                | 342 ms                                                 | 365 ms: 1.07x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.07x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 22.2 ms: 1.08x slower                                                 |
| pidigits                   | 184 ms                                                 | 199 ms: 1.08x slower                                                  |
| 2to3                       | 264 ms                                                 | 285 ms: 1.08x slower                                                  |
| thrift                     | 791 us                                                 | 858 us: 1.08x slower                                                  |
| pyflate                    | 448 ms                                                 | 486 ms: 1.08x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 334 us: 1.09x slower                                                  |
| sympy_str                  | 292 ms                                                 | 317 ms: 1.09x slower                                                  |
| nqueens                    | 80.1 ms                                                | 87.6 ms: 1.09x slower                                                 |
| richards                   | 45.9 ms                                                | 50.5 ms: 1.10x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 126 ms: 1.11x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 55.8 ms: 1.11x slower                                                 |
| richards_super             | 51.9 ms                                                | 57.7 ms: 1.11x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 85.4 ms: 1.12x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 95.4 ms: 1.12x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 76.7 ms: 1.12x slower                                                 |
| sympy_expand               | 468 ms                                                 | 532 ms: 1.14x slower                                                  |
| genshi_text                | 22.8 ms                                                | 26.2 ms: 1.15x slower                                                 |
| json_loads                 | 26.5 us                                                | 30.6 us: 1.15x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.69 us: 1.16x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 68.6 ms: 1.16x slower                                                 |
| django_template            | 34.7 ms                                                | 40.5 ms: 1.17x slower                                                 |
| logging_format             | 7.35 us                                                | 8.77 us: 1.19x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 197 us: 1.21x slower                                                  |
| meteor_contest             | 104 ms                                                 | 127 ms: 1.22x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.42 ms: 1.23x slower                                                 |
| fannkuch                   | 372 ms                                                 | 475 ms: 1.28x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 9.57 ms: 1.34x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.46 ms: 1.34x slower                                                 |
| nbody                      | 89.3 ms                                                | 120 ms: 1.34x slower                                                  |
| telco                      | 6.53 ms                                                | 8.80 ms: 1.35x slower                                                 |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.41x slower                                                 |
| coverage                   | 71.4 ms                                                | 109 ms: 1.52x slower                                                  |
| python_startup             | 9.93 ms                                                | 16.0 ms: 1.61x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.13 ms: 3.33x slower                                                 |
| logging_silent             | 109 ns                                                 | 539 ns: 4.95x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 103 ms: 9.58x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250514-3.15.0a0-e123a1d-NOGIL/bm-20250514-vultr-x86_64-python-e123a1d09bcb75aae0c5-3.15.0a0-e123a1d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.014x faster

# HPT report

- Reliability score: 86.40% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.42x