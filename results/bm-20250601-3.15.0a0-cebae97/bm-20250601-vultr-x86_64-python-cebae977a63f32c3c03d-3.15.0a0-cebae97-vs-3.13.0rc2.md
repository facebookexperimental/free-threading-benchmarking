# Results vs. 3.13.0rc2

- fork: python
- ref: cebae977a63f32c3c03d
- machine: linux-x86_64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.059x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 254 ms: 1.02x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.56 sec: 1.03x faster                                                |
| html5lib       | 68.6 ms                                                                | 61.7 ms: 1.11x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 881 ms                                                                 | 603 ms: 1.46x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 316 ms: 1.45x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 628 ms: 1.44x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 313 ms: 1.31x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 255 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 275 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 518 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 507 ms: 1.25x faster                                                  |
| async_generators           | 375 ms                                                                 | 342 ms: 1.10x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.54 sec: 1.01x slower                                                |
| asyncio_tcp                | 502 ms                                                                 | 515 ms: 1.02x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 23.9 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.20x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 199 ms: 1.09x faster                                                  |
| float          | 76.7 ms                                                                | 72.4 ms: 1.06x faster                                                 |
| nbody          | 85.3 ms                                                                | 88.3 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.55 ms: 1.26x faster                                                 |
| regex_dna      | 189 ms                                                                 | 166 ms: 1.14x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 21.0 ms: 1.11x faster                                                 |
| regex_compile  | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.14x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 32.7 us                                                                | 31.5 us: 1.04x faster                                                 |
| tomli_loads          | 2.01 sec                                                               | 1.95 sec: 1.03x faster                                                |
| unpickle             | 14.6 us                                                                | 14.2 us: 1.03x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 83.6 ms: 1.02x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 134 ms: 1.01x faster                                                  |
| xml_etree_process    | 59.2 ms                                                                | 58.7 ms: 1.01x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 209 us: 1.00x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 96.4 ms: 1.02x slower                                                 |
| pickle_list          | 4.81 us                                                                | 4.93 us: 1.02x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 308 us: 1.06x slower                                                  |
| json_loads           | 27.3 us                                                                | 29.2 us: 1.07x slower                                                 |
| unpickle_list        | 4.60 us                                                                | 5.03 us: 1.09x slower                                                 |
| pickle               | 11.4 us                                                                | 12.5 us: 1.10x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.54 ms: 1.02x slower                                                 |
| python_startup         | 11.0 ms                                                                | 12.8 ms: 1.16x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.8 ms: 1.05x faster                                                 |
| genshi_xml      | 49.1 ms                                                                | 48.0 ms: 1.02x faster                                                 |
| django_template | 34.2 ms                                                                | 34.6 ms: 1.01x slower                                                 |
| mako            | 11.2 ms                                                                | 11.9 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.20 sec: 1.95x faster                                                |
| async_tree_io              | 881 ms                                                                 | 603 ms: 1.46x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 316 ms: 1.45x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 628 ms: 1.44x faster                                                  |
| deepcopy                   | 357 us                                                                 | 253 us: 1.41x faster                                                  |
| go                         | 141 ms                                                                 | 105 ms: 1.33x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 28.9 us: 1.32x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 313 ms: 1.31x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 255 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 275 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 518 ms: 1.29x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.55 ms: 1.26x faster                                                 |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 507 ms: 1.25x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 111 ms: 1.20x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.69 us: 1.16x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 166 ms: 1.14x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 66.5 ms: 1.12x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 61.7 ms: 1.11x faster                                                 |
| pylint                     | 317 ms                                                                 | 285 ms: 1.11x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.0 ms: 1.11x faster                                                 |
| async_generators           | 375 ms                                                                 | 342 ms: 1.10x faster                                                  |
| pyflate                    | 449 ms                                                                 | 413 ms: 1.09x faster                                                  |
| pidigits                   | 216 ms                                                                 | 199 ms: 1.09x faster                                                  |
| richards                   | 44.4 ms                                                                | 40.9 ms: 1.09x faster                                                 |
| richards_super             | 50.4 ms                                                                | 46.5 ms: 1.08x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 61.4 ms: 1.07x faster                                                 |
| telco                      | 7.77 ms                                                                | 7.31 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.19 sec: 1.06x faster                                                |
| float                      | 76.7 ms                                                                | 72.4 ms: 1.06x faster                                                 |
| regex_compile              | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| hexiom                     | 5.95 ms                                                                | 5.63 ms: 1.06x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.7 us: 1.06x faster                                                 |
| spectral_norm              | 108 ms                                                                 | 102 ms: 1.06x faster                                                  |
| genshi_text                | 21.7 ms                                                                | 20.8 ms: 1.05x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 18.9 ms: 1.04x faster                                                 |
| pickle_dict                | 32.7 us                                                                | 31.5 us: 1.04x faster                                                 |
| thrift                     | 772 us                                                                 | 745 us: 1.04x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.95 sec: 1.03x faster                                                |
| meteor_contest             | 101 ms                                                                 | 98.6 ms: 1.03x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 339 ms: 1.03x faster                                                  |
| unpickle                   | 14.6 us                                                                | 14.2 us: 1.03x faster                                                 |
| docutils                   | 2.63 sec                                                               | 2.56 sec: 1.03x faster                                                |
| nqueens                    | 77.7 ms                                                                | 75.9 ms: 1.02x faster                                                 |
| genshi_xml                 | 49.1 ms                                                                | 48.0 ms: 1.02x faster                                                 |
| sympy_str                  | 274 ms                                                                 | 268 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 83.6 ms: 1.02x faster                                                 |
| 2to3                       | 259 ms                                                                 | 254 ms: 1.02x faster                                                  |
| scimark_lu                 | 112 ms                                                                 | 110 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 154 us: 1.01x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 134 ms: 1.01x faster                                                  |
| xml_etree_process          | 59.2 ms                                                                | 58.7 ms: 1.01x faster                                                 |
| sympy_expand               | 454 ms                                                                 | 450 ms: 1.01x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 519 ms: 1.00x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 209 us: 1.00x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                |
| chaos                      | 56.3 ms                                                                | 56.6 ms: 1.01x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 10.7 ms: 1.01x slower                                                 |
| raytrace                   | 250 ms                                                                 | 253 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.80 ms: 1.01x slower                                                 |
| django_template            | 34.2 ms                                                                | 34.6 ms: 1.01x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                               | 1.54 sec: 1.01x slower                                                |
| python_startup_no_site     | 7.41 ms                                                                | 7.54 ms: 1.02x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.6 ms: 1.02x slower                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 96.4 ms: 1.02x slower                                                 |
| pickle_list                | 4.81 us                                                                | 4.93 us: 1.02x slower                                                 |
| asyncio_tcp                | 502 ms                                                                 | 515 ms: 1.02x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 23.9 ms: 1.03x slower                                                 |
| nbody                      | 85.3 ms                                                                | 88.3 ms: 1.03x slower                                                 |
| json                       | 4.98 ms                                                                | 5.22 ms: 1.05x slower                                                 |
| unpack_sequence            | 39.3 ns                                                                | 41.3 ns: 1.05x slower                                                 |
| generators                 | 28.5 ms                                                                | 30.1 ms: 1.05x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 308 us: 1.06x slower                                                  |
| mako                       | 11.2 ms                                                                | 11.9 ms: 1.06x slower                                                 |
| json_loads                 | 27.3 us                                                                | 29.2 us: 1.07x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.31 ms: 1.07x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.39 us: 1.07x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 773 ms: 1.08x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.62 us: 1.08x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.58 sec: 1.08x slower                                                |
| unpickle_list              | 4.60 us                                                                | 5.03 us: 1.09x slower                                                 |
| pickle                     | 11.4 us                                                                | 12.5 us: 1.10x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.05 ms: 1.13x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.8 ms: 1.16x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.56 ms: 1.37x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 2.03 ms: 1.53x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 469 ns: 4.77x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 101 ms: 9.19x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (5): sqlite_synth, fannkuch, crypto_pyaes, sympy_sum, coverage
Ignored benchmarks (10) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.059x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.15x