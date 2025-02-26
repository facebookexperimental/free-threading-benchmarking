# Results vs. 3.13.0rc2

- fork: python
- ref: 0ef4ffeefd1737c18dc9
- machine: linux-x86_64
- commit hash: 0ef4ffe
- commit date: 2025-02-25
- overall geometric mean: 1.057x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 250 ms: 1.04x faster                                                   |
| docutils       | 2.63 sec                                                               | 2.54 sec: 1.04x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 597 ms: 1.51x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 603 ms: 1.46x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 482 ms: 1.38x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 258 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 472 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 253 ms: 1.32x faster                                                   |
| async_generators           | 375 ms                                                                 | 318 ms: 1.18x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 21.4 ms: 1.09x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.30x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 70.3 ms: 1.09x faster                                                  |
| pidigits       | 216 ms                                                                 | 208 ms: 1.04x faster                                                   |
| nbody          | 85.3 ms                                                                | 86.9 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.65 ms: 1.21x faster                                                  |
| regex_dna      | 189 ms                                                                 | 171 ms: 1.10x faster                                                   |
| regex_compile  | 131 ms                                                                 | 124 ms: 1.06x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 24.7 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.07x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.89 sec: 1.06x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.06x faster                                                   |
| xml_etree_iterparse  | 94.4 ms                                                                | 90.4 ms: 1.04x faster                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 82.0 ms: 1.04x faster                                                  |
| xml_etree_process    | 59.2 ms                                                                | 57.0 ms: 1.04x faster                                                  |
| unpickle_pure_python | 208 us                                                                 | 211 us: 1.01x slower                                                   |
| json_loads           | 27.3 us                                                                | 28.0 us: 1.02x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 11.1 ms: 1.05x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 307 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.51 ms: 1.01x slower                                                  |
| python_startup         | 11.0 ms                                                                | 14.7 ms: 1.34x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 20.4 ms: 1.07x faster                                                  |
| django_template | 34.2 ms                                                                | 32.4 ms: 1.05x faster                                                  |
| genshi_xml      | 49.1 ms                                                                | 47.7 ms: 1.03x faster                                                  |
| mako            | 11.2 ms                                                                | 11.6 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.03x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 597 ms: 1.51x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 312 ms: 1.47x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 603 ms: 1.46x faster                                                   |
| deepcopy                   | 357 us                                                                 | 245 us: 1.46x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 482 ms: 1.38x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 258 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 472 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 253 ms: 1.32x faster                                                   |
| deepcopy_memo              | 38.1 us                                                                | 29.1 us: 1.31x faster                                                  |
| go                         | 141 ms                                                                 | 111 ms: 1.26x faster                                                   |
| deepcopy_reduce            | 3.12 us                                                                | 2.53 us: 1.23x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.65 ms: 1.21x faster                                                  |
| scimark_sor                | 134 ms                                                                 | 112 ms: 1.19x faster                                                   |
| spectral_norm              | 108 ms                                                                 | 90.5 ms: 1.19x faster                                                  |
| async_generators           | 375 ms                                                                 | 318 ms: 1.18x faster                                                   |
| pylint                     | 317 ms                                                                 | 274 ms: 1.16x faster                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.15 ms: 1.14x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 309 ms: 1.13x faster                                                   |
| pyflate                    | 449 ms                                                                 | 402 ms: 1.12x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 171 ms: 1.10x faster                                                   |
| float                      | 76.7 ms                                                                | 70.3 ms: 1.09x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 21.4 ms: 1.09x faster                                                  |
| telco                      | 7.77 ms                                                                | 7.19 ms: 1.08x faster                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.15 sec: 1.07x faster                                                 |
| generators                 | 28.5 ms                                                                | 26.7 ms: 1.07x faster                                                  |
| genshi_text                | 21.7 ms                                                                | 20.4 ms: 1.07x faster                                                  |
| thrift                     | 772 us                                                                 | 726 us: 1.06x faster                                                   |
| tomli_loads                | 2.01 sec                                                               | 1.89 sec: 1.06x faster                                                 |
| richards_super             | 50.4 ms                                                                | 47.4 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 677 ms: 1.06x faster                                                   |
| richards                   | 44.4 ms                                                                | 41.9 ms: 1.06x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.06x faster                                                   |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.3 ms: 1.06x faster                                                  |
| regex_compile              | 131 ms                                                                 | 124 ms: 1.06x faster                                                   |
| logging_simple             | 6.14 us                                                                | 5.82 us: 1.06x faster                                                  |
| django_template            | 34.2 ms                                                                | 32.4 ms: 1.05x faster                                                  |
| hexiom                     | 5.95 ms                                                                | 5.67 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.46 sec                                                               | 1.39 sec: 1.05x faster                                                 |
| xml_etree_iterparse        | 94.4 ms                                                                | 90.4 ms: 1.04x faster                                                  |
| logging_format             | 6.92 us                                                                | 6.63 us: 1.04x faster                                                  |
| pidigits                   | 216 ms                                                                 | 208 ms: 1.04x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 82.0 ms: 1.04x faster                                                  |
| comprehensions             | 16.6 us                                                                | 15.9 us: 1.04x faster                                                  |
| nqueens                    | 77.7 ms                                                                | 74.7 ms: 1.04x faster                                                  |
| xml_etree_process          | 59.2 ms                                                                | 57.0 ms: 1.04x faster                                                  |
| coverage                   | 82.5 ms                                                                | 79.5 ms: 1.04x faster                                                  |
| 2to3                       | 259 ms                                                                 | 250 ms: 1.04x faster                                                   |
| docutils                   | 2.63 sec                                                               | 2.54 sec: 1.04x faster                                                 |
| sqlglot_optimize           | 52.7 ms                                                                | 51.0 ms: 1.03x faster                                                  |
| genshi_xml                 | 49.1 ms                                                                | 47.7 ms: 1.03x faster                                                  |
| chaos                      | 56.3 ms                                                                | 54.8 ms: 1.03x faster                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 152 us: 1.03x faster                                                   |
| fannkuch                   | 376 ms                                                                 | 366 ms: 1.03x faster                                                   |
| sympy_str                  | 274 ms                                                                 | 267 ms: 1.03x faster                                                   |
| deltablue                  | 3.10 ms                                                                | 3.02 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.20 us: 1.02x faster                                                  |
| sympy_integrate            | 19.7 ms                                                                | 19.3 ms: 1.02x faster                                                  |
| sympy_sum                  | 154 ms                                                                 | 151 ms: 1.02x faster                                                   |
| meteor_contest             | 101 ms                                                                 | 99.2 ms: 1.02x faster                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 67.0 ms: 1.02x faster                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.53 ms: 1.02x faster                                                  |
| scimark_lu                 | 112 ms                                                                 | 111 ms: 1.02x faster                                                   |
| sqlglot_parse              | 1.25 ms                                                                | 1.23 ms: 1.01x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 19.1 ms: 1.01x faster                                                  |
| dulwich_log                | 74.5 ms                                                                | 75.0 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 211 us: 1.01x slower                                                   |
| python_startup_no_site     | 7.41 ms                                                                | 7.51 ms: 1.01x slower                                                  |
| nbody                      | 85.3 ms                                                                | 86.9 ms: 1.02x slower                                                  |
| json_loads                 | 27.3 us                                                                | 28.0 us: 1.02x slower                                                  |
| raytrace                   | 250 ms                                                                 | 257 ms: 1.03x slower                                                   |
| mako                       | 11.2 ms                                                                | 11.6 ms: 1.03x slower                                                  |
| mdp                        | 2.34 sec                                                               | 2.42 sec: 1.03x slower                                                 |
| json_dumps                 | 10.6 ms                                                                | 11.1 ms: 1.05x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 307 us: 1.05x slower                                                   |
| regex_v8                   | 23.2 ms                                                                | 24.7 ms: 1.06x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 1.03 ms: 1.12x slower                                                  |
| gc_traversal               | 3.32 ms                                                                | 4.21 ms: 1.27x slower                                                  |
| python_startup             | 11.0 ms                                                                | 14.7 ms: 1.34x slower                                                  |
| create_gc_cycles           | 1.33 ms                                                                | 1.81 ms: 1.36x slower                                                  |
| sqlglot_normalize          | 106 ms                                                                 | 280 ms: 2.65x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                                | 88.3 ms: 8.03x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (5): pycparser, sympy_expand, asyncio_websockets, json, logging_silent
Ignored benchmarks (15) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.057x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.10x