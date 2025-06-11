# Results vs. 3.13.0rc2

- fork: python
- ref: 0f866cbfefd797b4dae2
- machine: linux-x86_64
- commit hash: 0f866cb
- commit date: 2025-06-10
- overall geometric mean: 1.018x slower
- HPT reliability: 95.20%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 281 ms: 1.08x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.68 sec: 1.02x slower                                                |
| html5lib       | 68.6 ms                                                                | 66.5 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 523 ms: 1.72x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 549 ms: 1.60x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 225 ms: 1.48x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 311 ms: 1.48x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 284 ms: 1.44x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 257 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 467 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 494 ms: 1.35x faster                                                  |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 24.0 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.32x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 182 ms: 1.19x faster                                                  |
| float          | 76.7 ms                                                                | 68.7 ms: 1.12x faster                                                 |
| nbody          | 85.3 ms                                                                | 119 ms: 1.40x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.70 ms: 1.19x faster                                                 |
| regex_v8       | 23.2 ms                                                                | 20.4 ms: 1.14x faster                                                 |
| regex_dna      | 189 ms                                                                 | 177 ms: 1.07x faster                                                  |
| regex_compile  | 131 ms                                                                 | 143 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 86.9 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.14 sec: 1.07x slower                                                |
| unpickle_pure_python | 208 us                                                                 | 228 us: 1.09x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 95.2 ms: 1.11x slower                                                 |
| json_loads           | 27.3 us                                                                | 30.9 us: 1.13x slower                                                 |
| json_dumps           | 10.6 ms                                                                | 12.1 ms: 1.13x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 335 us: 1.15x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 68.4 ms: 1.15x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.56 ms: 1.29x slower                                                 |
| python_startup         | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.37x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 39.4 ms: 1.15x slower                                                 |
| genshi_xml      | 49.1 ms                                                                | 58.7 ms: 1.20x slower                                                 |
| genshi_text     | 21.7 ms                                                                | 26.8 ms: 1.23x slower                                                 |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.24x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.31 sec: 1.79x faster                                                |
| gc_traversal               | 3.32 ms                                                                | 1.90 ms: 1.74x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 523 ms: 1.72x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 549 ms: 1.60x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 225 ms: 1.48x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 311 ms: 1.48x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 284 ms: 1.44x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 257 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 467 ms: 1.36x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 494 ms: 1.35x faster                                                  |
| deepcopy                   | 357 us                                                                 | 286 us: 1.25x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.70 ms: 1.19x faster                                                 |
| pidigits                   | 216 ms                                                                 | 182 ms: 1.19x faster                                                  |
| go                         | 141 ms                                                                 | 122 ms: 1.16x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 20.4 ms: 1.14x faster                                                 |
| float                      | 76.7 ms                                                                | 68.7 ms: 1.12x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 2.03 us: 1.11x faster                                                 |
| deepcopy_memo              | 38.1 us                                                                | 34.4 us: 1.11x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 86.9 ms: 1.09x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 125 ms: 1.07x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 177 ms: 1.07x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.95 us: 1.06x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 71.1 ms: 1.05x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 66.5 ms: 1.03x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.39 sec: 1.01x faster                                                |
| async_generators           | 375 ms                                                                 | 370 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                  |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                |
| docutils                   | 2.63 sec                                                               | 2.68 sec: 1.02x slower                                                |
| coroutines                 | 23.3 ms                                                                | 24.0 ms: 1.03x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 111 ms: 1.03x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 363 ms: 1.04x slower                                                  |
| json                       | 4.98 ms                                                                | 5.24 ms: 1.05x slower                                                 |
| comprehensions             | 16.6 us                                                                | 17.6 us: 1.06x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.34 ms: 1.06x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.14 sec: 1.07x slower                                                |
| pyflate                    | 449 ms                                                                 | 479 ms: 1.07x slower                                                  |
| 2to3                       | 259 ms                                                                 | 281 ms: 1.08x slower                                                  |
| regex_compile              | 131 ms                                                                 | 143 ms: 1.08x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.47 ms: 1.09x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 228 us: 1.09x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.47 ms: 1.10x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 85.7 ms: 1.10x slower                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.24 ms: 1.10x slower                                                 |
| generators                 | 28.5 ms                                                                | 31.7 ms: 1.11x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 21.9 ms: 1.11x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 95.2 ms: 1.11x slower                                                 |
| chaos                      | 56.3 ms                                                                | 62.8 ms: 1.12x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 127 ms: 1.13x slower                                                  |
| json_loads                 | 27.3 us                                                                | 30.9 us: 1.13x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 12.1 ms: 1.13x slower                                                 |
| sympy_str                  | 274 ms                                                                 | 311 ms: 1.14x slower                                                  |
| thrift                     | 772 us                                                                 | 877 us: 1.14x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 520 ms: 1.15x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 335 us: 1.15x slower                                                  |
| django_template            | 34.2 ms                                                                | 39.4 ms: 1.15x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 68.4 ms: 1.15x slower                                                 |
| sympy_sum                  | 154 ms                                                                 | 179 ms: 1.16x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.60 ms: 1.16x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 77.0 ms: 1.17x slower                                                 |
| richards                   | 44.4 ms                                                                | 52.0 ms: 1.17x slower                                                 |
| raytrace                   | 250 ms                                                                 | 294 ms: 1.18x slower                                                  |
| richards_super             | 50.4 ms                                                                | 59.7 ms: 1.18x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 186 us: 1.19x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 860 ms: 1.20x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 58.7 ms: 1.20x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 123 ms: 1.21x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.78 sec: 1.22x slower                                                |
| logging_simple             | 6.14 us                                                                | 7.52 us: 1.22x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 462 ms: 1.23x slower                                                  |
| genshi_text                | 21.7 ms                                                                | 26.8 ms: 1.23x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.58 us: 1.24x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 86.0 ms: 1.26x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 9.56 ms: 1.29x slower                                                 |
| coverage                   | 82.5 ms                                                                | 110 ms: 1.33x slower                                                  |
| nbody                      | 85.3 ms                                                                | 119 ms: 1.40x slower                                                  |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.41x slower                                                 |
| python_startup             | 11.0 ms                                                                | 16.0 ms: 1.45x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 3.10 ms: 3.36x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 527 ns: 5.37x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 104 ms: 9.44x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.08x slower                                                          |

Benchmark hidden because not significant (2): pylint, pathlib
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250610-3.15.0a0-0f866cb-NOGIL/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.018x slower

# HPT report

- Reliability score: 95.20% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x