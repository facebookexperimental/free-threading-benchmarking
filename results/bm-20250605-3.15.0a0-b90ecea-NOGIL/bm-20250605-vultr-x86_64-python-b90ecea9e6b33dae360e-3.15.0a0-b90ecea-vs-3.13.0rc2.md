# Results vs. 3.13.0rc2

- fork: python
- ref: b90ecea9e6b33dae360e
- machine: linux-x86_64
- commit hash: b90ecea
- commit date: 2025-06-05
- overall geometric mean: 1.019x slower
- HPT reliability: 94.85%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.41x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 283 ms: 1.09x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                |
| html5lib       | 68.6 ms                                                                | 66.9 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 527 ms: 1.71x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 555 ms: 1.59x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 228 ms: 1.46x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 285 ms: 1.44x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 258 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 464 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 489 ms: 1.36x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                                  |
| async_generators           | 375 ms                                                                 | 373 ms: 1.00x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.32x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 190 ms: 1.14x faster                                                  |
| float          | 76.7 ms                                                                | 68.8 ms: 1.12x faster                                                 |
| nbody          | 85.3 ms                                                                | 120 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.66 ms: 1.21x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 20.2 ms: 1.15x faster                                                 |
| regex_dna      | 189 ms                                                                 | 172 ms: 1.09x faster                                                  |
| regex_compile  | 131 ms                                                                 | 144 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.5 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.14 sec: 1.06x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 229 us: 1.10x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 94.8 ms: 1.11x slower                                                 |
| json_loads           | 27.3 us                                                                | 31.0 us: 1.13x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 12.1 ms: 1.14x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 336 us: 1.15x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 68.8 ms: 1.16x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.58 ms: 1.29x slower                                                 |
| python_startup         | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 39.8 ms: 1.17x slower                                                 |
| genshi_xml      | 49.1 ms                                                                | 58.3 ms: 1.19x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 26.4 ms: 1.21x slower                                                 |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.24x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.31 sec: 1.78x faster                                                |
| gc_traversal               | 3.32 ms                                                                | 1.90 ms: 1.75x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 527 ms: 1.71x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 555 ms: 1.59x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 228 ms: 1.46x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 285 ms: 1.44x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 258 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 464 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 489 ms: 1.36x faster                                                  |
| deepcopy                   | 357 us                                                                 | 295 us: 1.21x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.66 ms: 1.21x faster                                                 |
| go                         | 141 ms                                                                 | 121 ms: 1.16x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 20.2 ms: 1.15x faster                                                 |
| pidigits                   | 216 ms                                                                 | 190 ms: 1.14x faster                                                  |
| float                      | 76.7 ms                                                                | 68.8 ms: 1.12x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 122 ms: 1.09x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 34.8 us: 1.09x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 172 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.07 us: 1.09x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.5 ms: 1.08x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.97 us: 1.05x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 71.4 ms: 1.04x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 66.9 ms: 1.03x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.37 sec: 1.02x faster                                                |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| asyncio_websockets         | 517 ms                                                                 | 514 ms: 1.01x faster                                                  |
| async_generators           | 375 ms                                                                 | 373 ms: 1.00x faster                                                  |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.01x slower                                                |
| pathlib                    | 19.3 ms                                                                | 19.6 ms: 1.02x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 110 ms: 1.02x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 356 ms: 1.02x slower                                                  |
| docutils                   | 2.63 sec                                                               | 2.70 sec: 1.03x slower                                                |
| pyflate                    | 449 ms                                                                 | 470 ms: 1.05x slower                                                  |
| comprehensions             | 16.6 us                                                                | 17.4 us: 1.05x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.30 ms: 1.06x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.14 sec: 1.06x slower                                                |
| json                       | 4.98 ms                                                                | 5.30 ms: 1.06x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 84.6 ms: 1.09x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.17 ms: 1.09x slower                                                 |
| 2to3                       | 259 ms                                                                 | 283 ms: 1.09x slower                                                  |
| generators                 | 28.5 ms                                                                | 31.1 ms: 1.09x slower                                                 |
| regex_compile              | 131 ms                                                                 | 144 ms: 1.09x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.46 ms: 1.10x slower                                                 |
| chaos                      | 56.3 ms                                                                | 61.9 ms: 1.10x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 229 us: 1.10x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.59 ms: 1.11x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 94.8 ms: 1.11x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 22.1 ms: 1.12x slower                                                 |
| thrift                     | 772 us                                                                 | 870 us: 1.13x slower                                                  |
| json_loads                 | 27.3 us                                                                | 31.0 us: 1.13x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 128 ms: 1.13x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 12.1 ms: 1.14x slower                                                 |
| richards                   | 44.4 ms                                                                | 50.8 ms: 1.14x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 315 ms: 1.15x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 336 us: 1.15x slower                                                  |
| richards_super             | 50.4 ms                                                                | 58.2 ms: 1.15x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.58 ms: 1.16x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 68.8 ms: 1.16x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 528 ms: 1.16x slower                                                  |
| django_template            | 34.2 ms                                                                | 39.8 ms: 1.17x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 76.8 ms: 1.17x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 181 ms: 1.17x slower                                                  |
| raytrace                   | 250 ms                                                                 | 294 ms: 1.18x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 58.3 ms: 1.19x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 188 us: 1.21x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 26.4 ms: 1.21x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 878 ms: 1.22x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 124 ms: 1.22x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 465 ms: 1.24x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.82 sec: 1.25x slower                                                |
| logging_simple             | 6.14 us                                                                | 7.71 us: 1.26x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 85.9 ms: 1.26x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.75 us: 1.27x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 9.58 ms: 1.29x slower                                                 |
| coverage                   | 82.5 ms                                                                | 111 ms: 1.34x slower                                                  |
| nbody                      | 85.3 ms                                                                | 120 ms: 1.41x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                                 |
| python_startup             | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.11 ms: 3.36x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 524 ns: 5.34x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 103 ms: 9.37x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.019x slower

# HPT report

- Reliability score: 94.85% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.41x