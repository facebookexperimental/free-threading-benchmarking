# Results vs. 3.13.0rc2

- fork: python
- ref: 9211b3dabeacb92713ac
- machine: linux-x86_64
- commit hash: 9211b3d
- commit date: 2025-02-28
- overall geometric mean: 1.089x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 305 ms: 1.18x slower                                                   |
| docutils       | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                                 |
| html5lib       | 68.6 ms                                                                | 73.7 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 551 ms: 1.64x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 581 ms: 1.52x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 337 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 275 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 542 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 575 ms: 1.16x faster                                                   |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                                   |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.24x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 210 ms: 1.03x faster                                                   |
| float          | 76.7 ms                                                                | 76.3 ms: 1.01x faster                                                  |
| nbody          | 85.3 ms                                                                | 135 ms: 1.58x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                                  |
| regex_dna      | 189 ms                                                                 | 183 ms: 1.03x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 24.4 ms: 1.05x slower                                                  |
| regex_compile  | 131 ms                                                                 | 157 ms: 1.19x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.8 ms: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| json_loads           | 27.3 us                                                                | 29.6 us: 1.08x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                                | 95.4 ms: 1.12x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 69.5 ms: 1.17x slower                                                  |
| unpickle_pure_python | 208 us                                                                 | 251 us: 1.21x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 13.1 ms: 1.23x slower                                                  |
| pickle_pure_python   | 292 us                                                                 | 367 us: 1.26x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.64 ms: 1.30x slower                                                  |
| python_startup         | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.36x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 60.0 ms: 1.22x slower                                                  |
| django_template | 34.2 ms                                                                | 43.3 ms: 1.27x slower                                                  |
| genshi_text     | 21.7 ms                                                                | 27.9 ms: 1.28x slower                                                  |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.71 ms: 1.94x faster                                                  |
| async_tree_io_tg           | 901 ms                                                                 | 551 ms: 1.64x faster                                                   |
| async_tree_io              | 881 ms                                                                 | 581 ms: 1.52x faster                                                   |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                   |
| async_tree_memoization     | 459 ms                                                                 | 337 ms: 1.36x faster                                                   |
| async_tree_memoization_tg  | 410 ms                                                                 | 307 ms: 1.34x faster                                                   |
| async_tree_none            | 353 ms                                                                 | 275 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 542 ms: 1.17x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 575 ms: 1.16x faster                                                   |
| deepcopy                   | 357 us                                                                 | 310 us: 1.15x faster                                                   |
| regex_effbot               | 3.21 ms                                                                | 2.86 ms: 1.12x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                                  |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.8 ms: 1.08x faster                                                  |
| xml_etree_parse            | 136 ms                                                                 | 128 ms: 1.06x faster                                                   |
| regex_dna                  | 189 ms                                                                 | 183 ms: 1.03x faster                                                   |
| pidigits                   | 216 ms                                                                 | 210 ms: 1.03x faster                                                   |
| create_gc_cycles           | 1.33 ms                                                                | 1.30 ms: 1.03x faster                                                  |
| async_generators           | 375 ms                                                                 | 372 ms: 1.01x faster                                                   |
| float                      | 76.7 ms                                                                | 76.3 ms: 1.01x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                  |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                                  |
| deepcopy_reduce            | 3.12 us                                                                | 3.17 us: 1.02x slower                                                  |
| json                       | 4.98 ms                                                                | 5.12 ms: 1.03x slower                                                  |
| regex_v8                   | 23.2 ms                                                                | 24.4 ms: 1.05x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                                 |
| docutils                   | 2.63 sec                                                               | 2.80 sec: 1.07x slower                                                 |
| spectral_norm              | 108 ms                                                                 | 115 ms: 1.07x slower                                                   |
| html5lib                   | 68.6 ms                                                                | 73.7 ms: 1.07x slower                                                  |
| bpe_tokeniser              | 4.46 sec                                                               | 4.80 sec: 1.08x slower                                                 |
| scimark_sor                | 134 ms                                                                 | 144 ms: 1.08x slower                                                   |
| json_loads                 | 27.3 us                                                                | 29.6 us: 1.08x slower                                                  |
| generators                 | 28.5 ms                                                                | 31.3 ms: 1.10x slower                                                  |
| pyflate                    | 449 ms                                                                 | 498 ms: 1.11x slower                                                   |
| dulwich_log                | 74.5 ms                                                                | 82.6 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                                | 95.4 ms: 1.12x slower                                                  |
| telco                      | 7.77 ms                                                                | 8.75 ms: 1.13x slower                                                  |
| thrift                     | 772 us                                                                 | 881 us: 1.14x slower                                                   |
| logging_silent             | 98.2 ns                                                                | 112 ns: 1.14x slower                                                   |
| mdp                        | 2.34 sec                                                               | 2.68 sec: 1.14x slower                                                 |
| sqlglot_normalize          | 106 ms                                                                 | 122 ms: 1.16x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                                | 61.6 ms: 1.17x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 69.5 ms: 1.17x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 844 ms: 1.17x slower                                                   |
| 2to3                       | 259 ms                                                                 | 305 ms: 1.18x slower                                                   |
| coverage                   | 82.5 ms                                                                | 97.2 ms: 1.18x slower                                                  |
| logging_simple             | 6.14 us                                                                | 7.24 us: 1.18x slower                                                  |
| regex_compile              | 131 ms                                                                 | 157 ms: 1.19x slower                                                   |
| pprint_pformat             | 1.46 sec                                                               | 1.74 sec: 1.19x slower                                                 |
| logging_format             | 6.92 us                                                                | 8.32 us: 1.20x slower                                                  |
| unpickle_pure_python       | 208 us                                                                 | 251 us: 1.21x slower                                                   |
| comprehensions             | 16.6 us                                                                | 20.0 us: 1.21x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 188 ms: 1.22x slower                                                   |
| deltablue                  | 3.10 ms                                                                | 3.78 ms: 1.22x slower                                                  |
| genshi_xml                 | 49.1 ms                                                                | 60.0 ms: 1.22x slower                                                  |
| sympy_integrate            | 19.7 ms                                                                | 24.2 ms: 1.23x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 13.1 ms: 1.23x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 558 ms: 1.23x slower                                                   |
| chaos                      | 56.3 ms                                                                | 69.3 ms: 1.23x slower                                                  |
| richards                   | 44.4 ms                                                                | 54.7 ms: 1.23x slower                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.92 ms: 1.24x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 341 ms: 1.24x slower                                                   |
| hexiom                     | 5.95 ms                                                                | 7.45 ms: 1.25x slower                                                  |
| pickle_pure_python         | 292 us                                                                 | 367 us: 1.26x slower                                                   |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.26x slower                                                   |
| nqueens                    | 77.7 ms                                                                | 98.1 ms: 1.26x slower                                                  |
| django_template            | 34.2 ms                                                                | 43.3 ms: 1.27x slower                                                  |
| richards_super             | 50.4 ms                                                                | 63.9 ms: 1.27x slower                                                  |
| raytrace                   | 250 ms                                                                 | 319 ms: 1.28x slower                                                   |
| sqlglot_parse              | 1.25 ms                                                                | 1.59 ms: 1.28x slower                                                  |
| typing_runtime_protocols   | 156 us                                                                 | 199 us: 1.28x slower                                                   |
| genshi_text                | 21.7 ms                                                                | 27.9 ms: 1.28x slower                                                  |
| crypto_pyaes               | 68.2 ms                                                                | 88.0 ms: 1.29x slower                                                  |
| python_startup_no_site     | 7.41 ms                                                                | 9.64 ms: 1.30x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 494 ms: 1.31x slower                                                   |
| scimark_lu                 | 112 ms                                                                 | 156 ms: 1.39x slower                                                   |
| python_startup             | 11.0 ms                                                                | 15.6 ms: 1.41x slower                                                  |
| scimark_fft                | 348 ms                                                                 | 493 ms: 1.42x slower                                                   |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 95.3 ms: 1.45x slower                                                  |
| nbody                      | 85.3 ms                                                                | 135 ms: 1.58x slower                                                   |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 7.76 ms: 1.63x slower                                                  |
| bench_thread_pool          | 924 us                                                                 | 3.31 ms: 3.58x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                                | 95.0 ms: 8.64x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.14x slower                                                           |

Benchmark hidden because not significant (4): pylint, asyncio_websockets, deepcopy_memo, go
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.089x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.34x