# Results vs. 3.13.0rc2

- fork: python
- ref: 9ad0c7b0f14c5fcda6bf
- machine: linux-x86_64
- commit hash: 9ad0c7b
- commit date: 2025-05-13
- overall geometric mean: 1.070x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 250 ms: 1.04x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.51 sec: 1.05x faster                                                |
| html5lib       | 68.6 ms                                                                | 60.8 ms: 1.13x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 310 ms: 1.48x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 598 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 629 ms: 1.43x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 311 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 255 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 522 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 512 ms: 1.24x faster                                                  |
| async_generators           | 375 ms                                                                 | 336 ms: 1.11x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.26x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 197 ms: 1.10x faster                                                  |
| float          | 76.7 ms                                                                | 70.3 ms: 1.09x faster                                                 |
| nbody          | 85.3 ms                                                                | 88.8 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.69 ms: 1.19x faster                                                 |
| regex_dna      | 189 ms                                                                 | 173 ms: 1.09x faster                                                  |
| regex_compile  | 131 ms                                                                 | 123 ms: 1.06x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 22.3 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|---------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads         | 2.01 sec                                                               | 1.89 sec: 1.06x faster                                                |
| xml_etree_parse     | 136 ms                                                                 | 131 ms: 1.04x faster                                                  |
| xml_etree_generate  | 85.4 ms                                                                | 82.4 ms: 1.04x faster                                                 |
| xml_etree_iterparse | 94.4 ms                                                                | 91.0 ms: 1.04x faster                                                 |
| xml_etree_process   | 59.2 ms                                                                | 57.5 ms: 1.03x faster                                                 |
| json_dumps          | 10.6 ms                                                                | 10.8 ms: 1.01x slower                                                 |
| pickle_pure_python  | 292 us                                                                 | 303 us: 1.04x slower                                                  |
| json_loads          | 27.3 us                                                                | 29.4 us: 1.08x slower                                                 |
| Geometric mean      | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.33 ms: 1.01x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 21.7 ms                                                                | 20.2 ms: 1.08x faster                                                 |
| genshi_xml     | 49.1 ms                                                                | 47.6 ms: 1.03x faster                                                 |
| mako           | 11.2 ms                                                                | 11.9 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.16 sec: 2.02x faster                                                |
| async_tree_memoization     | 459 ms                                                                 | 310 ms: 1.48x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 598 ms: 1.47x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 629 ms: 1.43x faster                                                  |
| deepcopy                   | 357 us                                                                 | 252 us: 1.42x faster                                                  |
| go                         | 141 ms                                                                 | 106 ms: 1.33x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 28.8 us: 1.32x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 311 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 255 ms: 1.31x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 271 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 522 ms: 1.28x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 512 ms: 1.24x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 109 ms: 1.22x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.69 ms: 1.19x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.66 us: 1.17x faster                                                 |
| pylint                     | 317 ms                                                                 | 278 ms: 1.14x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 94.8 ms: 1.13x faster                                                 |
| pyflate                    | 449 ms                                                                 | 397 ms: 1.13x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 60.8 ms: 1.13x faster                                                 |
| richards                   | 44.4 ms                                                                | 39.8 ms: 1.11x faster                                                 |
| async_generators           | 375 ms                                                                 | 336 ms: 1.11x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 66.9 ms: 1.11x faster                                                 |
| richards_super             | 50.4 ms                                                                | 45.6 ms: 1.10x faster                                                 |
| pidigits                   | 216 ms                                                                 | 197 ms: 1.10x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 173 ms: 1.09x faster                                                  |
| float                      | 76.7 ms                                                                | 70.3 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.13 sec: 1.08x faster                                                |
| genshi_text                | 21.7 ms                                                                | 20.2 ms: 1.08x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.57 ms: 1.07x faster                                                 |
| regex_compile              | 131 ms                                                                 | 123 ms: 1.06x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.89 sec: 1.06x faster                                                |
| telco                      | 7.77 ms                                                                | 7.35 ms: 1.06x faster                                                 |
| thrift                     | 772 us                                                                 | 731 us: 1.06x faster                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.4 ms: 1.06x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 330 ms: 1.05x faster                                                  |
| sympy_integrate            | 19.7 ms                                                                | 18.8 ms: 1.05x faster                                                 |
| docutils                   | 2.63 sec                                                               | 2.51 sec: 1.05x faster                                                |
| scimark_lu                 | 112 ms                                                                 | 107 ms: 1.05x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 22.3 ms: 1.04x faster                                                 |
| 2to3                       | 259 ms                                                                 | 250 ms: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 131 ms: 1.04x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 82.4 ms: 1.04x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 91.0 ms: 1.04x faster                                                 |
| generators                 | 28.5 ms                                                                | 27.7 ms: 1.03x faster                                                 |
| genshi_xml                 | 49.1 ms                                                                | 47.6 ms: 1.03x faster                                                 |
| xml_etree_process          | 59.2 ms                                                                | 57.5 ms: 1.03x faster                                                 |
| pycparser                  | 1.12 sec                                                               | 1.09 sec: 1.03x faster                                                |
| sympy_str                  | 274 ms                                                                 | 267 ms: 1.03x faster                                                  |
| chaos                      | 56.3 ms                                                                | 54.9 ms: 1.02x faster                                                 |
| meteor_contest             | 101 ms                                                                 | 99.3 ms: 1.02x faster                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 153 us: 1.02x faster                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 708 ms: 1.02x faster                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 7.33 ms: 1.01x faster                                                 |
| fannkuch                   | 376 ms                                                                 | 372 ms: 1.01x faster                                                  |
| coverage                   | 82.5 ms                                                                | 81.7 ms: 1.01x faster                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.45 sec: 1.01x faster                                                |
| sympy_sum                  | 154 ms                                                                 | 153 ms: 1.01x faster                                                  |
| nqueens                    | 77.7 ms                                                                | 78.1 ms: 1.00x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 68.6 ms: 1.01x slower                                                 |
| raytrace                   | 250 ms                                                                 | 252 ms: 1.01x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.5 ms: 1.01x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 10.8 ms: 1.01x slower                                                 |
| comprehensions             | 16.6 us                                                                | 16.8 us: 1.02x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.16 ms: 1.02x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 303 us: 1.04x slower                                                  |
| nbody                      | 85.3 ms                                                                | 88.8 ms: 1.04x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.24 us: 1.05x slower                                                 |
| mako                       | 11.2 ms                                                                | 11.9 ms: 1.06x slower                                                 |
| json                       | 4.98 ms                                                                | 5.28 ms: 1.06x slower                                                 |
| logging_simple             | 6.14 us                                                                | 6.58 us: 1.07x slower                                                 |
| json_loads                 | 27.3 us                                                                | 29.4 us: 1.08x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.05 ms: 1.13x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.6 ms: 1.14x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.72 ms: 1.42x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.90 ms: 1.42x slower                                                 |
| logging_silent             | 98.2 ns                                                                | 467 ns: 4.76x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 99.0 ms: 9.00x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (6): sqlite_synth, django_template, sympy_expand, asyncio_websockets, unpickle_pure_python, scimark_sparse_mat_mult
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.15x