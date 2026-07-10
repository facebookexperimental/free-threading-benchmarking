# Results vs. 3.13.0rc2

- fork: python
- ref: b2d8db1ac818e74ffe66
- machine: linux-x86_64
- commit hash: b2d8db1
- commit date: 2026-07-09
- overall geometric mean: 1.068x slower
- HPT reliability: 97.85%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 296 ms: 1.14x slower                                                  |
| docutils       | 2.63 sec                                                               | 2.97 sec: 1.13x slower                                                |
| html5lib       | 68.6 ms                                                                | 66.3 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 687 ms: 1.31x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 707 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 604 ms: 1.10x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 419 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 583 ms: 1.09x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 397 ms: 1.03x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 345 ms: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                  |
| async_generators           | 375 ms                                                                 | 382 ms: 1.02x slower                                                  |
| coroutines                 | 23.3 ms                                                                | 24.1 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 180 ms: 1.20x faster                                                  |
| float          | 76.7 ms                                                                | 84.2 ms: 1.10x slower                                                 |
| nbody          | 85.3 ms                                                                | 126 ms: 1.47x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 19.9 ms: 1.16x faster                                                 |
| regex_effbot   | 3.21 ms                                                                | 2.89 ms: 1.11x faster                                                 |
| regex_dna      | 189 ms                                                                 | 177 ms: 1.07x faster                                                  |
| regex_compile  | 131 ms                                                                 | 168 ms: 1.28x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.97 sec: 1.02x faster                                                |
| xml_etree_iterparse  | 94.4 ms                                                                | 95.1 ms: 1.01x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 141 ms: 1.03x slower                                                  |
| json_loads           | 27.3 us                                                                | 30.0 us: 1.10x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 335 us: 1.15x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 240 us: 1.15x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 101 ms: 1.18x slower                                                  |
| xml_etree_process    | 59.2 ms                                                                | 74.6 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                                          |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.18 ms: 1.24x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.4 ms: 1.40x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.32x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 40.5 ms: 1.18x slower                                                 |
| mako            | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 131 ms: 2.42x faster                                                  |
| gc_traversal               | 3.32 ms                                                                | 1.76 ms: 1.89x faster                                                 |
| mdp                        | 2.34 sec                                                               | 1.31 sec: 1.79x faster                                                |
| bench_mp_pool              | 11.0 ms                                                                | 6.89 ms: 1.60x faster                                                 |
| deepcopy                   | 357 us                                                                 | 270 us: 1.32x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 687 ms: 1.31x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 707 ms: 1.25x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 31.1 us: 1.22x faster                                                 |
| pidigits                   | 216 ms                                                                 | 180 ms: 1.20x faster                                                  |
| go                         | 141 ms                                                                 | 121 ms: 1.17x faster                                                  |
| regex_v8                   | 23.2 ms                                                                | 19.9 ms: 1.16x faster                                                 |
| sqlite_synth               | 2.25 us                                                                | 1.97 us: 1.14x faster                                                 |
| regex_effbot               | 3.21 ms                                                                | 2.89 ms: 1.11x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 604 ms: 1.10x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 419 ms: 1.10x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 122 ms: 1.09x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 583 ms: 1.09x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 143 us: 1.09x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 17.8 ms: 1.08x faster                                                 |
| regex_dna                  | 189 ms                                                                 | 177 ms: 1.07x faster                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 2.97 us: 1.05x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 70.9 ms: 1.05x faster                                                 |
| html5lib                   | 68.6 ms                                                                | 66.3 ms: 1.03x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 397 ms: 1.03x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 345 ms: 1.02x faster                                                  |
| tomli_loads                | 2.01 sec                                                               | 1.97 sec: 1.02x faster                                                |
| bpe_tokeniser              | 4.46 sec                                                               | 4.38 sec: 1.02x faster                                                |
| asyncio_websockets         | 517 ms                                                                 | 513 ms: 1.01x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 349 ms: 1.00x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.12 sec: 1.00x slower                                                |
| xml_etree_iterparse        | 94.4 ms                                                                | 95.1 ms: 1.01x slower                                                 |
| async_generators           | 375 ms                                                                 | 382 ms: 1.02x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.36 ms: 1.02x slower                                                 |
| coroutines                 | 23.3 ms                                                                | 24.1 ms: 1.03x slower                                                 |
| xml_etree_parse            | 136 ms                                                                 | 141 ms: 1.03x slower                                                  |
| pyflate                    | 449 ms                                                                 | 469 ms: 1.04x slower                                                  |
| logging_silent             | 98.2 ns                                                                | 104 ns: 1.06x slower                                                  |
| json                       | 4.98 ms                                                                | 5.30 ms: 1.06x slower                                                 |
| comprehensions             | 16.6 us                                                                | 18.0 us: 1.08x slower                                                 |
| json_loads                 | 27.3 us                                                                | 30.0 us: 1.10x slower                                                 |
| float                      | 76.7 ms                                                                | 84.2 ms: 1.10x slower                                                 |
| chaos                      | 56.3 ms                                                                | 62.0 ms: 1.10x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 21.8 ms: 1.11x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.59 ms: 1.11x slower                                                 |
| pprint_safe_repr           | 719 ms                                                                 | 807 ms: 1.12x slower                                                  |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.34 ms: 1.12x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.97 sec: 1.13x slower                                                |
| sympy_str                  | 274 ms                                                                 | 311 ms: 1.13x slower                                                  |
| 2to3                       | 259 ms                                                                 | 296 ms: 1.14x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.02 us: 1.14x slower                                                 |
| generators                 | 28.5 ms                                                                | 32.6 ms: 1.14x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 129 ms: 1.15x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.67 sec: 1.15x slower                                                |
| nqueens                    | 77.7 ms                                                                | 89.2 ms: 1.15x slower                                                 |
| sympy_expand               | 454 ms                                                                 | 522 ms: 1.15x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 335 us: 1.15x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 240 us: 1.15x slower                                                  |
| logging_format             | 6.92 us                                                                | 8.04 us: 1.16x slower                                                 |
| thrift                     | 772 us                                                                 | 899 us: 1.16x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 180 ms: 1.17x slower                                                  |
| richards                   | 44.4 ms                                                                | 52.0 ms: 1.17x slower                                                 |
| richards_super             | 50.4 ms                                                                | 59.5 ms: 1.18x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 101 ms: 1.18x slower                                                  |
| django_template            | 34.2 ms                                                                | 40.5 ms: 1.18x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.70 ms: 1.19x slower                                                 |
| scimark_monte_carlo        | 65.8 ms                                                                | 78.7 ms: 1.20x slower                                                 |
| raytrace                   | 250 ms                                                                 | 304 ms: 1.22x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 465 ms: 1.24x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.18 ms: 1.24x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 126 ms: 1.24x slower                                                  |
| xml_etree_process          | 59.2 ms                                                                | 74.6 ms: 1.26x slower                                                 |
| regex_compile              | 131 ms                                                                 | 168 ms: 1.28x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 90.3 ms: 1.32x slower                                                 |
| mako                       | 11.2 ms                                                                | 15.7 ms: 1.40x slower                                                 |
| coverage                   | 82.5 ms                                                                | 115 ms: 1.40x slower                                                  |
| python_startup             | 11.0 ms                                                                | 15.4 ms: 1.40x slower                                                 |
| nbody                      | 85.3 ms                                                                | 126 ms: 1.47x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.49 ms: 1.61x slower                                                 |
| telco                      | 7.77 ms                                                                | 175 ms: 22.46x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.07x slower                                                          |

Benchmark hidden because not significant (3): async_tree_none_tg, spectral_norm, json_dumps
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260709-3.16.0a0-b2d8db1-NOGIL/bm-20260709-vultr-x86_64-python-b2d8db1ac818e74ffe66-3.16.0a0-b2d8db1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.068x slower

# HPT report

- Reliability score: 97.85% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x