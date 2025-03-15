# Results vs. 3.13.0rc2

- fork: python
- ref: 1a8e5742cdcf3dba7fc5
- machine: linux-x86_64
- commit hash: 1a8e574
- commit date: 2025-03-13
- overall geometric mean: 1.021x faster
- HPT reliability: 77.45%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 258 ms: 1.00x faster                                                   |
| docutils       | 2.63 sec                                                               | 2.61 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 628 ms: 1.44x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 630 ms: 1.40x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 329 ms: 1.40x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 517 ms: 1.29x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 318 ms: 1.29x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 504 ms: 1.26x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 267 ms: 1.25x faster                                                   |
| async_generators           | 375 ms                                                                 | 339 ms: 1.10x faster                                                   |
| Geometric mean             | (ref)                                                                  | 1.24x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 187 ms: 1.16x faster                                                   |
| float          | 76.7 ms                                                                | 75.8 ms: 1.01x faster                                                  |
| nbody          | 85.3 ms                                                                | 102 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                  |
| regex_dna      | 189 ms                                                                 | 179 ms: 1.05x faster                                                   |
| regex_compile  | 131 ms                                                                 | 130 ms: 1.01x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 24.5 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 130 ms: 1.05x faster                                                   |
| json_loads           | 27.3 us                                                                | 27.0 us: 1.01x faster                                                  |
| xml_etree_iterparse  | 94.4 ms                                                                | 93.4 ms: 1.01x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.00 sec: 1.01x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 86.5 ms: 1.01x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 60.1 ms: 1.01x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 11.2 ms: 1.06x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 224 us: 1.08x slower                                                   |
| pickle_pure_python   | 292 us                                                                 | 324 us: 1.11x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.63 ms: 1.16x slower                                                  |
| python_startup         | 11.0 ms                                                                | 14.9 ms: 1.35x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 21.9 ms: 1.01x slower                                                  |
| genshi_xml      | 49.1 ms                                                                | 51.0 ms: 1.04x slower                                                  |
| mako            | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                                  |
| django_template | 34.2 ms                                                                | 37.2 ms: 1.09x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 628 ms: 1.44x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 630 ms: 1.40x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 329 ms: 1.40x faster                                                   |
| deepcopy                   | 357 us                                                                 | 261 us: 1.37x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 517 ms: 1.29x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 318 ms: 1.29x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 504 ms: 1.26x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 267 ms: 1.25x faster                                                   |
| go                         | 141 ms                                                                 | 113 ms: 1.24x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 30.8 us: 1.24x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                  |
| pidigits                   | 216 ms                                                                 | 187 ms: 1.16x faster                                                   |
| scimark_sor                | 134 ms                                                                 | 116 ms: 1.15x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.73 us: 1.14x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 95.9 ms: 1.12x faster                                                  |
| pylint                     | 317 ms                                                                 | 285 ms: 1.11x faster                                                   |
| async_generators           | 375 ms                                                                 | 339 ms: 1.10x faster                                                   |
| dulwich_log                | 74.5 ms                                                                | 67.5 ms: 1.10x faster                                                  |
| pyflate                    | 449 ms                                                                 | 425 ms: 1.06x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 179 ms: 1.05x faster                                                   |
| xml_etree_parse            | 136 ms                                                                 | 130 ms: 1.05x faster                                                   |
| scimark_fft                | 348 ms                                                                 | 334 ms: 1.04x faster                                                   |
| richards                   | 44.4 ms                                                                | 42.7 ms: 1.04x faster                                                  |
| logging_format             | 6.92 us                                                                | 6.73 us: 1.03x faster                                                  |
| thrift                     | 772 us                                                                 | 754 us: 1.02x faster                                                   |
| json                       | 4.98 ms                                                                | 4.89 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.21 us: 1.02x faster                                                  |
| telco                      | 7.77 ms                                                                | 7.64 ms: 1.02x faster                                                  |
| coverage                   | 82.5 ms                                                                | 81.1 ms: 1.02x faster                                                  |
| logging_simple             | 6.14 us                                                                | 6.05 us: 1.01x faster                                                  |
| regex_compile              | 131 ms                                                                 | 130 ms: 1.01x faster                                                   |
| json_loads                 | 27.3 us                                                                | 27.0 us: 1.01x faster                                                  |
| float                      | 76.7 ms                                                                | 75.8 ms: 1.01x faster                                                  |
| sqlglot_normalize          | 106 ms                                                                 | 104 ms: 1.01x faster                                                   |
| xml_etree_iterparse        | 94.4 ms                                                                | 93.4 ms: 1.01x faster                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.70 ms: 1.01x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.61 sec: 1.01x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.43 sec: 1.01x faster                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.00 sec: 1.01x faster                                                 |
| 2to3                       | 259 ms                                                                 | 258 ms: 1.00x faster                                                   |
| genshi_text                | 21.7 ms                                                                | 21.9 ms: 1.01x slower                                                  |
| deltablue                  | 3.10 ms                                                                | 3.12 ms: 1.01x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 156 ms: 1.01x slower                                                   |
| scimark_monte_carlo        | 65.8 ms                                                                | 66.6 ms: 1.01x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 86.5 ms: 1.01x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 158 us: 1.01x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 99.6 ns: 1.01x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 60.1 ms: 1.01x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.6 ms: 1.02x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 278 ms: 1.02x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 114 ms: 1.02x slower                                                   |
| sympy_integrate            | 19.7 ms                                                                | 20.1 ms: 1.02x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 737 ms: 1.03x slower                                                   |
| hexiom                     | 5.95 ms                                                                | 6.10 ms: 1.03x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 465 ms: 1.03x slower                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.50 sec: 1.03x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.16 sec: 1.04x slower                                                 |
| comprehensions             | 16.6 us                                                                | 17.2 us: 1.04x slower                                                  |
| chaos                      | 56.3 ms                                                                | 58.5 ms: 1.04x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 51.0 ms: 1.04x slower                                                  |
| generators                 | 28.5 ms                                                                | 29.7 ms: 1.04x slower                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.62 ms: 1.04x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 81.4 ms: 1.05x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 71.5 ms: 1.05x slower                                                  |
| regex_v8                   | 23.2 ms                                                                | 24.5 ms: 1.06x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                                | 1.32 ms: 1.06x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 11.2 ms: 1.06x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 401 ms: 1.07x slower                                                   |
| mdp                        | 2.34 sec                                                               | 2.50 sec: 1.07x slower                                                 |
| raytrace                   | 250 ms                                                                 | 267 ms: 1.07x slower                                                   |
| unpickle_pure_python       | 208 us                                                                 | 224 us: 1.08x slower                                                   |
| mako                       | 11.2 ms                                                                | 12.1 ms: 1.08x slower                                                  |
| django_template            | 34.2 ms                                                                | 37.2 ms: 1.09x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 324 us: 1.11x slower                                                   |
| bench_thread_pool          | 924 us                                                                 | 1.05 ms: 1.14x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 8.63 ms: 1.16x slower                                                  |
| nbody                      | 85.3 ms                                                                | 102 ms: 1.20x slower                                                   |
| python_startup             | 11.0 ms                                                                | 14.9 ms: 1.35x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.83 ms: 1.37x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 4.76 ms: 1.44x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 88.2 ms: 8.01x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (5): richards_super, asyncio_websockets, meteor_contest, sqlglot_optimize, coroutines
Ignored benchmarks (15) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250313-3.14.0a5+-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5+-1a8e574.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 77.45% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x