# Results vs. 3.13.0rc2

- fork: python
- ref: 0f866cbfefd797b4dae2
- machine: linux-x86_64
- commit hash: 0f866cb
- commit date: 2025-06-10
- overall geometric mean: 1.071x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 248 ms: 1.05x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.51 sec: 1.05x faster                                                |
| html5lib       | 68.6 ms                                                                | 61.8 ms: 1.11x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 307 ms: 1.50x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 622 ms: 1.45x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 609 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 308 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 269 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 508 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 507 ms: 1.25x faster                                                  |
| async_generators           | 375 ms                                                                 | 330 ms: 1.13x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 198 ms: 1.09x faster                                                  |
| float          | 76.7 ms                                                                | 72.2 ms: 1.06x faster                                                 |
| nbody          | 85.3 ms                                                                | 88.2 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.58 ms: 1.24x faster                                                 |
| regex_dna      | 189 ms                                                                 | 172 ms: 1.10x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 21.7 ms: 1.07x faster                                                 |
| regex_compile  | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.11x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.92 sec: 1.05x faster                                                |
| xml_etree_parse      | 136 ms                                                                 | 132 ms: 1.03x faster                                                  |
| xml_etree_iterparse  | 94.4 ms                                                                | 91.9 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 83.4 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.2 ms                                                                | 58.9 ms: 1.01x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 209 us: 1.01x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                 |
| json_loads           | 27.3 us                                                                | 28.3 us: 1.04x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 308 us: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.32 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 21.7 ms                                                                | 20.6 ms: 1.06x faster                                                 |
| genshi_xml     | 49.1 ms                                                                | 47.9 ms: 1.02x faster                                                 |
| mako           | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.16 sec: 2.02x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 307 ms: 1.50x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 622 ms: 1.45x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 609 ms: 1.45x faster                                                  |
| deepcopy                   | 357 us                                                                 | 251 us: 1.42x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 308 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.33x faster                                                  |
| go                         | 141 ms                                                                 | 107 ms: 1.32x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 269 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 508 ms: 1.31x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 29.2 us: 1.30x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 507 ms: 1.25x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.58 ms: 1.24x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 112 ms: 1.19x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.64 us: 1.18x faster                                                 |
| pylint                     | 317 ms                                                                 | 278 ms: 1.14x faster                                                  |
| async_generators           | 375 ms                                                                 | 330 ms: 1.13x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 66.6 ms: 1.12x faster                                                 |
| pyflate                    | 449 ms                                                                 | 405 ms: 1.11x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 96.9 ms: 1.11x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 61.8 ms: 1.11x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 172 ms: 1.10x faster                                                  |
| pidigits                   | 216 ms                                                                 | 198 ms: 1.09x faster                                                  |
| richards_super             | 50.4 ms                                                                | 46.7 ms: 1.08x faster                                                 |
| telco                      | 7.77 ms                                                                | 7.21 ms: 1.08x faster                                                 |
| richards                   | 44.4 ms                                                                | 41.3 ms: 1.08x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.15 sec: 1.07x faster                                                |
| regex_v8                   | 23.2 ms                                                                | 21.7 ms: 1.07x faster                                                 |
| float                      | 76.7 ms                                                                | 72.2 ms: 1.06x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 329 ms: 1.06x faster                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.2 ms: 1.06x faster                                                 |
| regex_compile              | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| genshi_text                | 21.7 ms                                                                | 20.6 ms: 1.06x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.7 us: 1.05x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 18.7 ms: 1.05x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.67 ms: 1.05x faster                                                 |
| thrift                     | 772 us                                                                 | 736 us: 1.05x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.51 sec: 1.05x faster                                                |
| tomli_loads                | 2.01 sec                                                               | 1.92 sec: 1.05x faster                                                |
| 2to3                       | 259 ms                                                                 | 248 ms: 1.05x faster                                                  |
| sympy_str                  | 274 ms                                                                 | 265 ms: 1.03x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 132 ms: 1.03x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 151 us: 1.03x faster                                                  |
| generators                 | 28.5 ms                                                                | 27.7 ms: 1.03x faster                                                 |
| pycparser                  | 1.12 sec                                                               | 1.09 sec: 1.03x faster                                                |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.62 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.9 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 83.4 ms: 1.02x faster                                                 |
| genshi_xml                 | 49.1 ms                                                                | 47.9 ms: 1.02x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 76.0 ms: 1.02x faster                                                 |
| scimark_lu                 | 112 ms                                                                 | 110 ms: 1.02x faster                                                  |
| meteor_contest             | 101 ms                                                                 | 99.7 ms: 1.02x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 67.1 ms: 1.02x faster                                                 |
| sympy_expand               | 454 ms                                                                 | 446 ms: 1.02x faster                                                  |
| coverage                   | 82.5 ms                                                                | 81.3 ms: 1.01x faster                                                 |
| sympy_sum                  | 154 ms                                                                 | 152 ms: 1.01x faster                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 7.32 ms: 1.01x faster                                                 |
| chaos                      | 56.3 ms                                                                | 56.0 ms: 1.01x faster                                                 |
| xml_etree_process          | 59.2 ms                                                                | 58.9 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 208 us                                                                 | 209 us: 1.01x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                 |
| fannkuch                   | 376 ms                                                                 | 381 ms: 1.01x slower                                                  |
| raytrace                   | 250 ms                                                                 | 254 ms: 1.02x slower                                                  |
| json                       | 4.98 ms                                                                | 5.13 ms: 1.03x slower                                                 |
| nbody                      | 85.3 ms                                                                | 88.2 ms: 1.03x slower                                                 |
| json_loads                 | 27.3 us                                                                | 28.3 us: 1.04x slower                                                 |
| mako                       | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.30 us: 1.06x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 308 us: 1.06x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.50 us: 1.06x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.55 sec: 1.07x slower                                                |
| deltablue                  | 3.10 ms                                                                | 3.31 ms: 1.07x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 768 ms: 1.07x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.04 ms: 1.13x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.08 ms: 1.23x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.93 ms: 1.45x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 469 ns: 4.78x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 98.9 ms: 8.99x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (5): sqlite_synth, django_template, asyncio_websockets, coroutines, pathlib
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250610-3.15.0a0-0f866cb/bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x