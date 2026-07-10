# Results vs. 3.13.0rc2

- fork: python
- ref: b2d8db1ac818e74ffe66
- machine: linux-x86_64
- commit hash: b2d8db1
- commit date: 2026-07-09
- overall geometric mean: 1.037x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 258 ms: 1.01x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.39 sec: 1.10x faster                                                |
| html5lib       | 68.6 ms                                                                | 57.5 ms: 1.19x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 881 ms                                                                 | 713 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 541 ms: 1.23x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 288 ms: 1.23x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 375 ms: 1.22x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 753 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 561 ms: 1.13x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 364 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 296 ms: 1.13x faster                                                  |
| async_generators           | 375 ms                                                                 | 340 ms: 1.10x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.7 ms: 1.02x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 543 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.14x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 188 ms: 1.15x faster                                                  |
| float          | 76.7 ms                                                                | 74.3 ms: 1.03x faster                                                 |
| nbody          | 85.3 ms                                                                | 93.0 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.56 ms: 1.26x faster                                                 |
| regex_dna      | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 21.7 ms: 1.07x faster                                                 |
| regex_compile  | 131 ms                                                                 | 148 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.81 sec: 1.11x faster                                                |
| json_dumps           | 10.6 ms                                                                | 9.85 ms: 1.08x faster                                                 |
| xml_etree_iterparse  | 94.4 ms                                                                | 88.6 ms: 1.06x faster                                                 |
| unpickle_pure_python | 208 us                                                                 | 212 us: 1.02x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 87.8 ms: 1.03x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 61.7 ms: 1.04x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 308 us: 1.06x slower                                                  |
| xml_etree_parse      | 136 ms                                                                 | 144 ms: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 6.96 ms: 1.07x faster                                                 |
| python_startup         | 11.0 ms                                                                | 12.3 ms: 1.12x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.02x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 36.2 ms: 1.06x slower                                                 |
| mako            | 11.2 ms                                                                | 12.0 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 115 ms: 2.77x faster                                                  |
| mdp                        | 2.34 sec                                                               | 1.14 sec: 2.06x faster                                                |
| deepcopy                   | 357 us                                                                 | 231 us: 1.54x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 26.8 us: 1.42x faster                                                 |
| go                         | 141 ms                                                                 | 103 ms: 1.37x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 118 us: 1.32x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.56 ms: 1.26x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 106 ms: 1.25x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 713 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 541 ms: 1.23x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 288 ms: 1.23x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 375 ms: 1.22x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.57 us: 1.22x faster                                                 |
| async_tree_io_tg           | 901 ms                                                                 | 753 ms: 1.20x faster                                                  |
| html5lib                   | 68.6 ms                                                                | 57.5 ms: 1.19x faster                                                 |
| pyflate                    | 449 ms                                                                 | 382 ms: 1.18x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 93.1 ms: 1.15x faster                                                 |
| pidigits                   | 216 ms                                                                 | 188 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 561 ms: 1.13x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 364 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 296 ms: 1.13x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.81 sec: 1.11x faster                                                |
| async_generators           | 375 ms                                                                 | 340 ms: 1.10x faster                                                  |
| docutils                   | 2.63 sec                                                               | 2.39 sec: 1.10x faster                                                |
| pathlib                    | 19.3 ms                                                                | 17.5 ms: 1.10x faster                                                 |
| scimark_fft                | 348 ms                                                                 | 318 ms: 1.10x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 68.5 ms: 1.09x faster                                                 |
| json_dumps                 | 10.6 ms                                                                | 9.85 ms: 1.08x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 176 ms: 1.07x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 21.7 ms: 1.07x faster                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 6.96 ms: 1.07x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.6 ms: 1.06x faster                                                 |
| nqueens                    | 77.7 ms                                                                | 73.6 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.22 sec: 1.06x faster                                                |
| richards                   | 44.4 ms                                                                | 42.2 ms: 1.05x faster                                                 |
| comprehensions             | 16.6 us                                                                | 15.9 us: 1.04x faster                                                 |
| logging_silent             | 98.2 ns                                                                | 94.3 ns: 1.04x faster                                                 |
| chaos                      | 56.3 ms                                                                | 54.1 ms: 1.04x faster                                                 |
| richards_super             | 50.4 ms                                                                | 48.4 ms: 1.04x faster                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 63.4 ms: 1.04x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.59 ms: 1.04x faster                                                 |
| sympy_integrate            | 19.7 ms                                                                | 19.1 ms: 1.03x faster                                                 |
| float                      | 76.7 ms                                                                | 74.3 ms: 1.03x faster                                                 |
| hexiom                     | 5.95 ms                                                                | 5.76 ms: 1.03x faster                                                 |
| logging_simple             | 6.14 us                                                                | 5.99 us: 1.03x faster                                                 |
| logging_format             | 6.92 us                                                                | 6.76 us: 1.02x faster                                                 |
| pycparser                  | 1.12 sec                                                               | 1.10 sec: 1.02x faster                                                |
| meteor_contest             | 101 ms                                                                 | 100 ms: 1.01x faster                                                  |
| fannkuch                   | 376 ms                                                                 | 373 ms: 1.01x faster                                                  |
| sympy_str                  | 274 ms                                                                 | 272 ms: 1.01x faster                                                  |
| 2to3                       | 259 ms                                                                 | 258 ms: 1.01x faster                                                  |
| generators                 | 28.5 ms                                                                | 28.7 ms: 1.01x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 457 ms: 1.01x slower                                                  |
| raytrace                   | 250 ms                                                                 | 252 ms: 1.01x slower                                                  |
| scimark_lu                 | 112 ms                                                                 | 114 ms: 1.01x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 156 ms: 1.01x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 69.0 ms: 1.01x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 727 ms: 1.01x slower                                                  |
| thrift                     | 772 us                                                                 | 781 us: 1.01x slower                                                  |
| coverage                   | 82.5 ms                                                                | 83.6 ms: 1.01x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.48 sec: 1.02x slower                                                |
| coroutines                 | 23.3 ms                                                                | 23.7 ms: 1.02x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 212 us: 1.02x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 87.8 ms: 1.03x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 61.7 ms: 1.04x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.23 ms: 1.04x slower                                                 |
| asyncio_websockets         | 517 ms                                                                 | 543 ms: 1.05x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 308 us: 1.06x slower                                                  |
| xml_etree_parse            | 136 ms                                                                 | 144 ms: 1.06x slower                                                  |
| django_template            | 34.2 ms                                                                | 36.2 ms: 1.06x slower                                                 |
| mako                       | 11.2 ms                                                                | 12.0 ms: 1.07x slower                                                 |
| nbody                      | 85.3 ms                                                                | 93.0 ms: 1.09x slower                                                 |
| python_startup             | 11.0 ms                                                                | 12.3 ms: 1.12x slower                                                 |
| regex_compile              | 131 ms                                                                 | 148 ms: 1.13x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 3.83 ms: 1.15x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.66 ms: 1.25x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.34 ms: 1.45x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 221 ms: 20.11x slower                                                 |
| telco                      | 7.77 ms                                                                | 157 ms: 20.13x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (3): json_loads, json, sqlite_synth
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260709-3.16.0a0-b2d8db1/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.037x faster

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x