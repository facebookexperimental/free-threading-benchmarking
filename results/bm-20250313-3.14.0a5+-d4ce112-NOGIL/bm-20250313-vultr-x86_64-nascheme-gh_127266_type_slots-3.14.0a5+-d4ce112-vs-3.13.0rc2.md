# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: d4ce112
- commit date: 2025-03-13
- overall geometric mean: 1.075x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 296 ms: 1.14x slower                                                     |
| docutils       | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                                   |
| html5lib       | 68.6 ms                                                                | 72.5 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 556 ms: 1.62x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 585 ms: 1.51x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 339 ms: 1.35x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 306 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 480 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 511 ms: 1.30x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 275 ms: 1.29x faster                                                     |
| async_generators           | 375 ms                                                                 | 368 ms: 1.02x faster                                                     |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 187 ms: 1.16x faster                                                     |
| float          | 76.7 ms                                                                | 77.5 ms: 1.01x slower                                                    |
| nbody          | 85.3 ms                                                                | 132 ms: 1.55x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.72 ms: 1.18x faster                                                    |
| regex_dna      | 189 ms                                                                 | 185 ms: 1.02x faster                                                     |
| regex_v8       | 23.2 ms                                                                | 23.9 ms: 1.03x slower                                                    |
| regex_compile  | 131 ms                                                                 | 157 ms: 1.20x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.6 ms: 1.08x faster                                                    |
| xml_etree_parse      | 136 ms                                                                 | 127 ms: 1.07x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 95.5 ms: 1.12x slower                                                    |
| json_loads           | 27.3 us                                                                | 30.9 us: 1.13x slower                                                    |
| tomli_loads          | 2.01 sec                                                               | 2.35 sec: 1.17x slower                                                   |
| xml_etree_process    | 59.2 ms                                                                | 70.5 ms: 1.19x slower                                                    |
| unpickle_pure_python | 208 us                                                                 | 248 us: 1.19x slower                                                     |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                                    |
| pickle_pure_python   | 292 us                                                                 | 360 us: 1.23x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.7 ms: 1.42x slower                                                    |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 60.7 ms: 1.24x slower                                                    |
| django_template | 34.2 ms                                                                | 42.5 ms: 1.24x slower                                                    |
| genshi_text     | 21.7 ms                                                                | 28.6 ms: 1.31x slower                                                    |
| mako            | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.72 ms: 1.93x faster                                                    |
| async_tree_io_tg           | 901 ms                                                                 | 556 ms: 1.62x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 585 ms: 1.51x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 339 ms: 1.35x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 306 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 480 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 511 ms: 1.30x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 275 ms: 1.29x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.72 ms: 1.18x faster                                                    |
| deepcopy                   | 357 us                                                                 | 308 us: 1.16x faster                                                     |
| pidigits                   | 216 ms                                                                 | 187 ms: 1.16x faster                                                     |
| sqlite_synth               | 2.25 us                                                                | 2.04 us: 1.10x faster                                                    |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.6 ms: 1.08x faster                                                    |
| xml_etree_parse            | 136 ms                                                                 | 127 ms: 1.07x faster                                                     |
| create_gc_cycles           | 1.33 ms                                                                | 1.31 ms: 1.02x faster                                                    |
| regex_dna                  | 189 ms                                                                 | 185 ms: 1.02x faster                                                     |
| dulwich_log                | 74.5 ms                                                                | 73.1 ms: 1.02x faster                                                    |
| async_generators           | 375 ms                                                                 | 368 ms: 1.02x faster                                                     |
| deepcopy_reduce            | 3.12 us                                                                | 3.14 us: 1.01x slower                                                    |
| scimark_sor                | 134 ms                                                                 | 134 ms: 1.01x slower                                                     |
| float                      | 76.7 ms                                                                | 77.5 ms: 1.01x slower                                                    |
| deepcopy_memo              | 38.1 us                                                                | 38.7 us: 1.02x slower                                                    |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                    |
| regex_v8                   | 23.2 ms                                                                | 23.9 ms: 1.03x slower                                                    |
| spectral_norm              | 108 ms                                                                 | 112 ms: 1.04x slower                                                     |
| html5lib                   | 68.6 ms                                                                | 72.5 ms: 1.06x slower                                                    |
| json                       | 4.98 ms                                                                | 5.31 ms: 1.07x slower                                                    |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.07x slower                                                   |
| docutils                   | 2.63 sec                                                               | 2.81 sec: 1.07x slower                                                   |
| bpe_tokeniser              | 4.46 sec                                                               | 4.79 sec: 1.07x slower                                                   |
| generators                 | 28.5 ms                                                                | 31.3 ms: 1.10x slower                                                    |
| logging_silent             | 98.2 ns                                                                | 109 ns: 1.11x slower                                                     |
| mdp                        | 2.34 sec                                                               | 2.60 sec: 1.11x slower                                                   |
| telco                      | 7.77 ms                                                                | 8.65 ms: 1.11x slower                                                    |
| pyflate                    | 449 ms                                                                 | 500 ms: 1.11x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                                | 95.5 ms: 1.12x slower                                                    |
| scimark_fft                | 348 ms                                                                 | 393 ms: 1.13x slower                                                     |
| json_loads                 | 27.3 us                                                                | 30.9 us: 1.13x slower                                                    |
| sqlglot_normalize          | 106 ms                                                                 | 120 ms: 1.14x slower                                                     |
| 2to3                       | 259 ms                                                                 | 296 ms: 1.14x slower                                                     |
| thrift                     | 772 us                                                                 | 888 us: 1.15x slower                                                     |
| sqlglot_optimize           | 52.7 ms                                                                | 61.2 ms: 1.16x slower                                                    |
| logging_simple             | 6.14 us                                                                | 7.15 us: 1.16x slower                                                    |
| pprint_safe_repr           | 719 ms                                                                 | 838 ms: 1.17x slower                                                     |
| coverage                   | 82.5 ms                                                                | 96.2 ms: 1.17x slower                                                    |
| tomli_loads                | 2.01 sec                                                               | 2.35 sec: 1.17x slower                                                   |
| logging_format             | 6.92 us                                                                | 8.10 us: 1.17x slower                                                    |
| xml_etree_process          | 59.2 ms                                                                | 70.5 ms: 1.19x slower                                                    |
| unpickle_pure_python       | 208 us                                                                 | 248 us: 1.19x slower                                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.74 sec: 1.19x slower                                                   |
| regex_compile              | 131 ms                                                                 | 157 ms: 1.20x slower                                                     |
| sympy_sum                  | 154 ms                                                                 | 185 ms: 1.20x slower                                                     |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.21x slower                                                    |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.75 ms: 1.21x slower                                                    |
| sympy_integrate            | 19.7 ms                                                                | 23.9 ms: 1.21x slower                                                    |
| sympy_expand               | 454 ms                                                                 | 552 ms: 1.22x slower                                                     |
| sympy_str                  | 274 ms                                                                 | 335 ms: 1.22x slower                                                     |
| chaos                      | 56.3 ms                                                                | 69.0 ms: 1.23x slower                                                    |
| pickle_pure_python         | 292 us                                                                 | 360 us: 1.23x slower                                                     |
| sqlglot_transpile          | 1.55 ms                                                                | 1.92 ms: 1.23x slower                                                    |
| deltablue                  | 3.10 ms                                                                | 3.82 ms: 1.23x slower                                                    |
| genshi_xml                 | 49.1 ms                                                                | 60.7 ms: 1.24x slower                                                    |
| comprehensions             | 16.6 us                                                                | 20.6 us: 1.24x slower                                                    |
| hexiom                     | 5.95 ms                                                                | 7.39 ms: 1.24x slower                                                    |
| django_template            | 34.2 ms                                                                | 42.5 ms: 1.24x slower                                                    |
| richards                   | 44.4 ms                                                                | 55.3 ms: 1.25x slower                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.2 ms: 1.26x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                                | 1.59 ms: 1.27x slower                                                    |
| richards_super             | 50.4 ms                                                                | 64.3 ms: 1.28x slower                                                    |
| scimark_lu                 | 112 ms                                                                 | 144 ms: 1.28x slower                                                     |
| crypto_pyaes               | 68.2 ms                                                                | 87.2 ms: 1.28x slower                                                    |
| typing_runtime_protocols   | 156 us                                                                 | 199 us: 1.28x slower                                                     |
| raytrace                   | 250 ms                                                                 | 320 ms: 1.28x slower                                                     |
| nqueens                    | 77.7 ms                                                                | 101 ms: 1.30x slower                                                     |
| fannkuch                   | 376 ms                                                                 | 489 ms: 1.30x slower                                                     |
| genshi_text                | 21.7 ms                                                                | 28.6 ms: 1.31x slower                                                    |
| meteor_contest             | 101 ms                                                                 | 133 ms: 1.31x slower                                                     |
| mako                       | 11.2 ms                                                                | 15.9 ms: 1.42x slower                                                    |
| python_startup             | 11.0 ms                                                                | 15.7 ms: 1.42x slower                                                    |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                    |
| nbody                      | 85.3 ms                                                                | 132 ms: 1.55x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 3.16 ms: 3.42x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 95.3 ms: 8.66x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                             |

Benchmark hidden because not significant (4): pylint, asyncio_websockets, coroutines, go
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250313-3.14.0a5+-d4ce112-NOGIL/bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5+-d4ce112.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.075x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.35x