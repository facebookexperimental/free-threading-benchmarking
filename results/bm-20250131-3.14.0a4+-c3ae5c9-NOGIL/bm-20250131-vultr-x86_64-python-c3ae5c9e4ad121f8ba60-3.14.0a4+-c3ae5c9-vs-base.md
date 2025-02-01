# Results vs. base

- fork: python
- ref: c3ae5c9e4ad121f8ba60
- machine: linux-x86_64
- commit hash: c3ae5c9
- commit date: 2025-01-31
- overall geometric mean: 1.029x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 305 ms                                                                 | 295 ms: 1.03x faster                                                   |
| docutils       | 2.81 sec                                                               | 2.74 sec: 1.02x faster                                                 |
| html5lib       | 71.8 ms                                                                | 69.2 ms: 1.04x faster                                                  |
| sphinx         | 1.11 sec                                                               | 1.09 sec: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 267 ms                                                                 | 254 ms: 1.05x faster                                                   |
| async_tree_memoization     | 361 ms                                                                 | 346 ms: 1.04x faster                                                   |
| async_tree_none            | 295 ms                                                                 | 282 ms: 1.04x faster                                                   |
| async_tree_io_tg           | 586 ms                                                                 | 561 ms: 1.04x faster                                                   |
| async_generators           | 381 ms                                                                 | 366 ms: 1.04x faster                                                   |
| async_tree_io              | 621 ms                                                                 | 596 ms: 1.04x faster                                                   |
| async_tree_memoization_tg  | 325 ms                                                                 | 313 ms: 1.04x faster                                                   |
| coroutines                 | 23.4 ms                                                                | 23.2 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg | 509 ms                                                                 | 548 ms: 1.07x slower                                                   |
| async_tree_cpu_io_mixed    | 541 ms                                                                 | 582 ms: 1.08x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 136 ms                                                                 | 125 ms: 1.09x faster                                                   |
| float          | 76.6 ms                                                                | 74.4 ms: 1.03x faster                                                  |
| pidigits       | 202 ms                                                                 | 201 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 151 ms                                                                 | 145 ms: 1.04x faster                                                   |
| regex_dna      | 178 ms                                                                 | 182 ms: 1.02x slower                                                   |
| regex_effbot   | 2.69 ms                                                                | 2.85 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_pure_python | 254 us                                                                 | 240 us: 1.06x faster                                                   |
| pickle_pure_python   | 382 us                                                                 | 360 us: 1.06x faster                                                   |
| xml_etree_process    | 70.7 ms                                                                | 67.1 ms: 1.05x faster                                                  |
| xml_etree_generate   | 98.2 ms                                                                | 94.5 ms: 1.04x faster                                                  |
| tomli_loads          | 2.35 sec                                                               | 2.27 sec: 1.03x faster                                                 |
| xml_etree_iterparse  | 88.7 ms                                                                | 86.4 ms: 1.03x faster                                                  |
| json_dumps           | 13.0 ms                                                                | 12.7 ms: 1.03x faster                                                  |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.01x faster                                                   |
| json_loads           | 31.0 us                                                                | 31.5 us: 1.02x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 9.65 ms                                                                | 9.60 ms: 1.01x faster                                                  |
| python_startup         | 15.4 ms                                                                | 15.3 ms: 1.01x faster                                                  |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 60.9 ms                                                                | 56.4 ms: 1.08x faster                                                  |
| genshi_text     | 27.9 ms                                                                | 26.5 ms: 1.05x faster                                                  |
| mako            | 16.1 ms                                                                | 15.3 ms: 1.05x faster                                                  |
| django_template | 42.5 ms                                                                | 41.0 ms: 1.04x faster                                                  |
| Geometric mean  | (ref)                                                                  | 1.06x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4+-31c82c2 | bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4+-c3ae5c9 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| generators                 | 33.7 ms                                                                | 30.6 ms: 1.10x faster                                                  |
| nbody                      | 136 ms                                                                 | 125 ms: 1.09x faster                                                   |
| genshi_xml                 | 60.9 ms                                                                | 56.4 ms: 1.08x faster                                                  |
| logging_format             | 8.41 us                                                                | 7.89 us: 1.07x faster                                                  |
| scimark_sor                | 137 ms                                                                 | 129 ms: 1.06x faster                                                   |
| logging_silent             | 114 ns                                                                 | 108 ns: 1.06x faster                                                   |
| unpickle_pure_python       | 254 us                                                                 | 240 us: 1.06x faster                                                   |
| pickle_pure_python         | 382 us                                                                 | 360 us: 1.06x faster                                                   |
| chaos                      | 70.2 ms                                                                | 66.4 ms: 1.06x faster                                                  |
| richards                   | 58.4 ms                                                                | 55.3 ms: 1.06x faster                                                  |
| sqlite_synth               | 2.13 us                                                                | 2.01 us: 1.06x faster                                                  |
| go                         | 141 ms                                                                 | 133 ms: 1.06x faster                                                   |
| richards_super             | 67.3 ms                                                                | 63.9 ms: 1.05x faster                                                  |
| xml_etree_process          | 70.7 ms                                                                | 67.1 ms: 1.05x faster                                                  |
| genshi_text                | 27.9 ms                                                                | 26.5 ms: 1.05x faster                                                  |
| mako                       | 16.1 ms                                                                | 15.3 ms: 1.05x faster                                                  |
| deltablue                  | 4.79 ms                                                                | 4.55 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 267 ms                                                                 | 254 ms: 1.05x faster                                                   |
| hexiom                     | 7.46 ms                                                                | 7.10 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 823 ms                                                                 | 783 ms: 1.05x faster                                                   |
| logging_simple             | 7.35 us                                                                | 7.01 us: 1.05x faster                                                  |
| deepcopy_memo              | 38.8 us                                                                | 36.9 us: 1.05x faster                                                  |
| pprint_pformat             | 1.69 sec                                                               | 1.61 sec: 1.05x faster                                                 |
| raytrace                   | 331 ms                                                                 | 316 ms: 1.05x faster                                                   |
| async_tree_memoization     | 361 ms                                                                 | 346 ms: 1.04x faster                                                   |
| async_tree_none            | 295 ms                                                                 | 282 ms: 1.04x faster                                                   |
| async_tree_io_tg           | 586 ms                                                                 | 561 ms: 1.04x faster                                                   |
| async_generators           | 381 ms                                                                 | 366 ms: 1.04x faster                                                   |
| async_tree_io              | 621 ms                                                                 | 596 ms: 1.04x faster                                                   |
| scimark_fft                | 387 ms                                                                 | 372 ms: 1.04x faster                                                   |
| scimark_monte_carlo        | 83.8 ms                                                                | 80.5 ms: 1.04x faster                                                  |
| regex_compile              | 151 ms                                                                 | 145 ms: 1.04x faster                                                   |
| sqlglot_normalize          | 122 ms                                                                 | 118 ms: 1.04x faster                                                   |
| async_tree_memoization_tg  | 325 ms                                                                 | 313 ms: 1.04x faster                                                   |
| typing_runtime_protocols   | 202 us                                                                 | 194 us: 1.04x faster                                                   |
| xml_etree_generate         | 98.2 ms                                                                | 94.5 ms: 1.04x faster                                                  |
| django_template            | 42.5 ms                                                                | 41.0 ms: 1.04x faster                                                  |
| scimark_lu                 | 137 ms                                                                 | 132 ms: 1.04x faster                                                   |
| html5lib                   | 71.8 ms                                                                | 69.2 ms: 1.04x faster                                                  |
| comprehensions             | 20.1 us                                                                | 19.4 us: 1.04x faster                                                  |
| nqueens                    | 96.4 ms                                                                | 93.2 ms: 1.03x faster                                                  |
| tomli_loads                | 2.35 sec                                                               | 2.27 sec: 1.03x faster                                                 |
| sqlalchemy_imperative      | 24.5 ms                                                                | 23.7 ms: 1.03x faster                                                  |
| deepcopy                   | 311 us                                                                 | 301 us: 1.03x faster                                                   |
| 2to3                       | 305 ms                                                                 | 295 ms: 1.03x faster                                                   |
| sqlglot_parse              | 1.59 ms                                                                | 1.54 ms: 1.03x faster                                                  |
| spectral_norm              | 109 ms                                                                 | 105 ms: 1.03x faster                                                   |
| deepcopy_reduce            | 3.19 us                                                                | 3.09 us: 1.03x faster                                                  |
| float                      | 76.6 ms                                                                | 74.4 ms: 1.03x faster                                                  |
| mdp                        | 2.69 sec                                                               | 2.61 sec: 1.03x faster                                                 |
| sqlglot_transpile          | 1.92 ms                                                                | 1.87 ms: 1.03x faster                                                  |
| pycparser                  | 1.19 sec                                                               | 1.16 sec: 1.03x faster                                                 |
| bpe_tokeniser              | 4.70 sec                                                               | 4.57 sec: 1.03x faster                                                 |
| xml_etree_iterparse        | 88.7 ms                                                                | 86.4 ms: 1.03x faster                                                  |
| pylint                     | 317 ms                                                                 | 309 ms: 1.03x faster                                                   |
| json_dumps                 | 13.0 ms                                                                | 12.7 ms: 1.03x faster                                                  |
| fannkuch                   | 492 ms                                                                 | 480 ms: 1.03x faster                                                   |
| sympy_integrate            | 24.3 ms                                                                | 23.7 ms: 1.03x faster                                                  |
| dulwich_log                | 82.9 ms                                                                | 80.9 ms: 1.03x faster                                                  |
| pathlib                    | 18.7 ms                                                                | 18.2 ms: 1.02x faster                                                  |
| sqlglot_optimize           | 61.4 ms                                                                | 60.0 ms: 1.02x faster                                                  |
| sqlalchemy_declarative     | 157 ms                                                                 | 154 ms: 1.02x faster                                                   |
| docutils                   | 2.81 sec                                                               | 2.74 sec: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 5.58 ms                                                                | 5.45 ms: 1.02x faster                                                  |
| coverage                   | 97.3 ms                                                                | 95.2 ms: 1.02x faster                                                  |
| many_optionals             | 1.18 ms                                                                | 1.15 ms: 1.02x faster                                                  |
| connected_components       | 496 ms                                                                 | 486 ms: 1.02x faster                                                   |
| sphinx                     | 1.11 sec                                                               | 1.09 sec: 1.02x faster                                                 |
| sympy_str                  | 336 ms                                                                 | 330 ms: 1.02x faster                                                   |
| pyflate                    | 494 ms                                                                 | 486 ms: 1.02x faster                                                   |
| sympy_expand               | 552 ms                                                                 | 542 ms: 1.02x faster                                                   |
| crypto_pyaes               | 88.0 ms                                                                | 86.4 ms: 1.02x faster                                                  |
| shortest_path              | 544 ms                                                                 | 535 ms: 1.02x faster                                                   |
| thrift                     | 910 us                                                                 | 897 us: 1.01x faster                                                   |
| subparsers                 | 25.5 ms                                                                | 25.1 ms: 1.01x faster                                                  |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.01x faster                                                   |
| sympy_sum                  | 186 ms                                                                 | 184 ms: 1.01x faster                                                   |
| bench_mp_pool              | 92.7 ms                                                                | 91.7 ms: 1.01x faster                                                  |
| create_gc_cycles           | 1.39 ms                                                                | 1.37 ms: 1.01x faster                                                  |
| gc_traversal               | 1.75 ms                                                                | 1.73 ms: 1.01x faster                                                  |
| coroutines                 | 23.4 ms                                                                | 23.2 ms: 1.01x faster                                                  |
| python_startup_no_site     | 9.65 ms                                                                | 9.60 ms: 1.01x faster                                                  |
| python_startup             | 15.4 ms                                                                | 15.3 ms: 1.01x faster                                                  |
| pidigits                   | 202 ms                                                                 | 201 ms: 1.01x faster                                                   |
| bench_thread_pool          | 3.33 ms                                                                | 3.31 ms: 1.00x faster                                                  |
| k_core                     | 2.31 sec                                                               | 2.30 sec: 1.00x faster                                                 |
| json_loads                 | 31.0 us                                                                | 31.5 us: 1.02x slower                                                  |
| regex_dna                  | 178 ms                                                                 | 182 ms: 1.02x slower                                                   |
| regex_effbot               | 2.69 ms                                                                | 2.85 ms: 1.06x slower                                                  |
| async_tree_cpu_io_mixed_tg | 509 ms                                                                 | 548 ms: 1.07x slower                                                   |
| async_tree_cpu_io_mixed    | 541 ms                                                                 | 582 ms: 1.08x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (5): telco, meteor_contest, asyncio_websockets, json, regex_v8

- Geometric mean (including insignificant results): 1.029x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.01x