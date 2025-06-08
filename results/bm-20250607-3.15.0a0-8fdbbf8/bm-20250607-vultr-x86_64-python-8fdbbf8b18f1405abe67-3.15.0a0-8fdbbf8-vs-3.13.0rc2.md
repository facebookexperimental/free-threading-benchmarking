# Results vs. 3.13.0rc2

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: linux-x86_64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.064x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 250 ms: 1.04x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.54 sec: 1.03x faster                                                |
| html5lib       | 68.6 ms                                                                | 61.1 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 307 ms: 1.50x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 593 ms: 1.49x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 623 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 306 ms: 1.34x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.32x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 270 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 521 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 514 ms: 1.23x faster                                                  |
| async_generators           | 375 ms                                                                 | 340 ms: 1.10x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.22x faster                                                          |

Benchmark hidden because not significant (3): asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 197 ms: 1.10x faster                                                  |
| float          | 76.7 ms                                                                | 71.8 ms: 1.07x faster                                                 |
| nbody          | 85.3 ms                                                                | 87.5 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.88 ms: 1.11x faster                                                 |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| regex_compile  | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 23.0 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|---------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle            | 14.6 us                                                                | 13.8 us: 1.05x faster                                                 |
| tomli_loads         | 2.01 sec                                                               | 1.95 sec: 1.03x faster                                                |
| xml_etree_generate  | 85.4 ms                                                                | 83.3 ms: 1.02x faster                                                 |
| xml_etree_parse     | 136 ms                                                                 | 133 ms: 1.02x faster                                                  |
| xml_etree_iterparse | 94.4 ms                                                                | 92.4 ms: 1.02x faster                                                 |
| xml_etree_process   | 59.2 ms                                                                | 58.5 ms: 1.01x faster                                                 |
| pickle_dict         | 32.7 us                                                                | 32.4 us: 1.01x faster                                                 |
| json_dumps          | 10.6 ms                                                                | 10.9 ms: 1.02x slower                                                 |
| pickle_pure_python  | 292 us                                                                 | 307 us: 1.05x slower                                                  |
| json_loads          | 27.3 us                                                                | 29.1 us: 1.06x slower                                                 |
| pickle_list         | 4.81 us                                                                | 5.14 us: 1.07x slower                                                 |
| pickle              | 11.4 us                                                                | 12.2 us: 1.07x slower                                                 |
| unpickle_list       | 4.60 us                                                                | 5.00 us: 1.09x slower                                                 |
| Geometric mean      | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.33 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.6 ms: 1.15x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.5 ms: 1.06x faster                                                 |
| genshi_xml      | 49.1 ms                                                                | 48.4 ms: 1.01x faster                                                 |
| django_template | 34.2 ms                                                                | 34.8 ms: 1.02x slower                                                 |
| mako            | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.15 sec: 2.03x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 307 ms: 1.50x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 593 ms: 1.49x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 623 ms: 1.45x faster                                                  |
| deepcopy                   | 357 us                                                                 | 252 us: 1.42x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 306 ms: 1.34x faster                                                  |
| go                         | 141 ms                                                                 | 105 ms: 1.33x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 251 ms: 1.32x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 28.9 us: 1.32x faster                                                 |
| async_tree_none            | 353 ms                                                                 | 270 ms: 1.31x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 521 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 514 ms: 1.23x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 111 ms: 1.20x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.67 us: 1.17x faster                                                 |
| pylint                     | 317 ms                                                                 | 278 ms: 1.14x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 61.1 ms: 1.12x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 66.4 ms: 1.12x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.88 ms: 1.11x faster                                                 |
| pyflate                    | 449 ms                                                                 | 406 ms: 1.11x faster                                                  |
| async_generators           | 375 ms                                                                 | 340 ms: 1.10x faster                                                  |
| pidigits                   | 216 ms                                                                 | 197 ms: 1.10x faster                                                  |
| hexiom                     | 5.95 ms                                                                | 5.46 ms: 1.09x faster                                                 |
| richards_super             | 50.4 ms                                                                | 46.3 ms: 1.09x faster                                                 |
| richards                   | 44.4 ms                                                                | 41.1 ms: 1.08x faster                                                 |
| telco                      | 7.77 ms                                                                | 7.24 ms: 1.07x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.16 sec: 1.07x faster                                                |
| float                      | 76.7 ms                                                                | 71.8 ms: 1.07x faster                                                 |
| regex_compile              | 131 ms                                                                 | 124 ms: 1.06x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 101 ms: 1.06x faster                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.0 ms: 1.06x faster                                                 |
| genshi_text                | 21.7 ms                                                                | 20.5 ms: 1.06x faster                                                 |
| unpickle                   | 14.6 us                                                                | 13.8 us: 1.05x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.7 us: 1.05x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 18.8 ms: 1.05x faster                                                 |
| thrift                     | 772 us                                                                 | 735 us: 1.05x faster                                                  |
| 2to3                       | 259 ms                                                                 | 250 ms: 1.04x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.54 sec: 1.03x faster                                                |
| tomli_loads                | 2.01 sec                                                               | 1.95 sec: 1.03x faster                                                |
| generators                 | 28.5 ms                                                                | 27.7 ms: 1.03x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 98.7 ms: 1.03x faster                                                 |
| sympy_str                  | 274 ms                                                                 | 267 ms: 1.03x faster                                                  |
| nqueens                    | 77.7 ms                                                                | 75.8 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 83.3 ms: 1.02x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 340 ms: 1.02x faster                                                  |
| scimark_lu                 | 112 ms                                                                 | 110 ms: 1.02x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 133 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 92.4 ms: 1.02x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 153 us: 1.02x faster                                                  |
| genshi_xml                 | 49.1 ms                                                                | 48.4 ms: 1.01x faster                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 67.3 ms: 1.01x faster                                                 |
| xml_etree_process          | 59.2 ms                                                                | 58.5 ms: 1.01x faster                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 7.33 ms: 1.01x faster                                                 |
| coroutines                 | 23.3 ms                                                                | 23.1 ms: 1.01x faster                                                 |
| pickle_dict                | 32.7 us                                                                | 32.4 us: 1.01x faster                                                 |
| sympy_expand               | 454 ms                                                                 | 450 ms: 1.01x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 23.0 ms: 1.01x faster                                                 |
| sympy_sum                  | 154 ms                                                                 | 153 ms: 1.01x faster                                                  |
| fannkuch                   | 376 ms                                                                 | 378 ms: 1.00x slower                                                  |
| raytrace                   | 250 ms                                                                 | 253 ms: 1.01x slower                                                  |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                                 |
| chaos                      | 56.3 ms                                                                | 57.0 ms: 1.01x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.83 ms: 1.02x slower                                                 |
| django_template            | 34.2 ms                                                                | 34.8 ms: 1.02x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 10.9 ms: 1.02x slower                                                 |
| nbody                      | 85.3 ms                                                                | 87.5 ms: 1.02x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.23 ms: 1.04x slower                                                 |
| mako                       | 11.2 ms                                                                | 11.8 ms: 1.05x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 307 us: 1.05x slower                                                  |
| json                       | 4.98 ms                                                                | 5.26 ms: 1.06x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.32 us: 1.06x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 763 ms: 1.06x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.53 us: 1.06x slower                                                 |
| unpack_sequence            | 39.3 ns                                                                | 41.8 ns: 1.06x slower                                                 |
| json_loads                 | 27.3 us                                                                | 29.1 us: 1.06x slower                                                 |
| pickle_list                | 4.81 us                                                                | 5.14 us: 1.07x slower                                                 |
| pickle                     | 11.4 us                                                                | 12.2 us: 1.07x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.57 sec: 1.08x slower                                                |
| unpickle_list              | 4.60 us                                                                | 5.00 us: 1.09x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.04 ms: 1.13x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.6 ms: 1.15x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.26 ms: 1.28x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.89 ms: 1.42x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 470 ns: 4.79x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 98.9 ms: 8.99x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (6): asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets, sqlite_synth, unpickle_pure_python, coverage
Ignored benchmarks (10) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-vultr-x86_64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.064x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.15x