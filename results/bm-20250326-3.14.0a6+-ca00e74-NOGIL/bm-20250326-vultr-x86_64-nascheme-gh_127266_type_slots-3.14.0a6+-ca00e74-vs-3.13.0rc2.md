# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: ca00e74
- commit date: 2025-03-26
- overall geometric mean: 1.076x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 299 ms: 1.15x slower                                                     |
| docutils       | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                                   |
| html5lib       | 68.6 ms                                                                | 72.3 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 548 ms: 1.64x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 583 ms: 1.51x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 237 ms: 1.41x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 331 ms: 1.39x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 298 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 476 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 512 ms: 1.30x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                     |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                                    |
| async_generators           | 375 ms                                                                 | 383 ms: 1.02x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 204 ms: 1.06x faster                                                     |
| float          | 76.7 ms                                                                | 78.4 ms: 1.02x slower                                                    |
| nbody          | 85.3 ms                                                                | 135 ms: 1.58x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.76 ms: 1.16x faster                                                    |
| regex_v8       | 23.2 ms                                                                | 22.1 ms: 1.05x faster                                                    |
| regex_dna      | 189 ms                                                                 | 185 ms: 1.02x faster                                                     |
| regex_compile  | 131 ms                                                                 | 159 ms: 1.21x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.8 ms: 1.08x faster                                                    |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.05x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 94.8 ms: 1.11x slower                                                    |
| json_loads           | 27.3 us                                                                | 30.5 us: 1.12x slower                                                    |
| xml_etree_process    | 59.2 ms                                                                | 69.2 ms: 1.17x slower                                                    |
| tomli_loads          | 2.01 sec                                                               | 2.37 sec: 1.18x slower                                                   |
| json_dumps           | 10.6 ms                                                                | 13.0 ms: 1.22x slower                                                    |
| unpickle_pure_python | 208 us                                                                 | 259 us: 1.24x slower                                                     |
| pickle_pure_python   | 292 us                                                                 | 363 us: 1.24x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                                    |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.9 ms: 1.22x slower                                                    |
| django_template | 34.2 ms                                                                | 42.5 ms: 1.24x slower                                                    |
| genshi_text     | 21.7 ms                                                                | 28.3 ms: 1.30x slower                                                    |
| mako            | 11.2 ms                                                                | 16.1 ms: 1.43x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.30x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.82 ms: 1.83x faster                                                    |
| async_tree_io_tg           | 901 ms                                                                 | 548 ms: 1.64x faster                                                     |
| async_tree_io              | 881 ms                                                                 | 583 ms: 1.51x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 237 ms: 1.41x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 331 ms: 1.39x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 298 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 476 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 512 ms: 1.30x faster                                                     |
| async_tree_none            | 353 ms                                                                 | 276 ms: 1.28x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.76 ms: 1.16x faster                                                    |
| deepcopy                   | 357 us                                                                 | 312 us: 1.14x faster                                                     |
| sqlite_synth               | 2.25 us                                                                | 2.00 us: 1.12x faster                                                    |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.8 ms: 1.08x faster                                                    |
| pidigits                   | 216 ms                                                                 | 204 ms: 1.06x faster                                                     |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.05x faster                                                     |
| regex_v8                   | 23.2 ms                                                                | 22.1 ms: 1.05x faster                                                    |
| regex_dna                  | 189 ms                                                                 | 185 ms: 1.02x faster                                                     |
| dulwich_log                | 74.5 ms                                                                | 73.4 ms: 1.01x faster                                                    |
| coroutines                 | 23.3 ms                                                                | 23.5 ms: 1.01x slower                                                    |
| deepcopy_reduce            | 3.12 us                                                                | 3.18 us: 1.02x slower                                                    |
| float                      | 76.7 ms                                                                | 78.4 ms: 1.02x slower                                                    |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                    |
| async_generators           | 375 ms                                                                 | 383 ms: 1.02x slower                                                     |
| scimark_sor                | 134 ms                                                                 | 137 ms: 1.03x slower                                                     |
| create_gc_cycles           | 1.33 ms                                                                | 1.37 ms: 1.03x slower                                                    |
| go                         | 141 ms                                                                 | 145 ms: 1.03x slower                                                     |
| deepcopy_memo              | 38.1 us                                                                | 39.9 us: 1.05x slower                                                    |
| json                       | 4.98 ms                                                                | 5.24 ms: 1.05x slower                                                    |
| html5lib                   | 68.6 ms                                                                | 72.3 ms: 1.05x slower                                                    |
| spectral_norm              | 108 ms                                                                 | 113 ms: 1.05x slower                                                     |
| docutils                   | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.07x slower                                                   |
| generators                 | 28.5 ms                                                                | 31.1 ms: 1.09x slower                                                    |
| bpe_tokeniser              | 4.46 sec                                                               | 4.88 sec: 1.10x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 94.8 ms: 1.11x slower                                                    |
| json_loads                 | 27.3 us                                                                | 30.5 us: 1.12x slower                                                    |
| thrift                     | 772 us                                                                 | 870 us: 1.13x slower                                                     |
| scimark_fft                | 348 ms                                                                 | 396 ms: 1.14x slower                                                     |
| 2to3                       | 259 ms                                                                 | 299 ms: 1.15x slower                                                     |
| pyflate                    | 449 ms                                                                 | 518 ms: 1.15x slower                                                     |
| telco                      | 7.77 ms                                                                | 9.00 ms: 1.16x slower                                                    |
| mdp                        | 2.34 sec                                                               | 2.72 sec: 1.16x slower                                                   |
| pprint_safe_repr           | 719 ms                                                                 | 836 ms: 1.16x slower                                                     |
| xml_etree_process          | 59.2 ms                                                                | 69.2 ms: 1.17x slower                                                    |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.57 ms: 1.17x slower                                                    |
| tomli_loads                | 2.01 sec                                                               | 2.37 sec: 1.18x slower                                                   |
| logging_simple             | 6.14 us                                                                | 7.27 us: 1.18x slower                                                    |
| logging_silent             | 98.2 ns                                                                | 116 ns: 1.19x slower                                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.73 sec: 1.19x slower                                                   |
| sympy_integrate            | 19.7 ms                                                                | 23.8 ms: 1.20x slower                                                    |
| sympy_expand               | 454 ms                                                                 | 547 ms: 1.20x slower                                                     |
| regex_compile              | 131 ms                                                                 | 159 ms: 1.21x slower                                                     |
| sympy_sum                  | 154 ms                                                                 | 187 ms: 1.21x slower                                                     |
| sympy_str                  | 274 ms                                                                 | 334 ms: 1.22x slower                                                     |
| logging_format             | 6.92 us                                                                | 8.44 us: 1.22x slower                                                    |
| genshi_xml                 | 49.1 ms                                                                | 59.9 ms: 1.22x slower                                                    |
| richards                   | 44.4 ms                                                                | 54.2 ms: 1.22x slower                                                    |
| json_dumps                 | 10.6 ms                                                                | 13.0 ms: 1.22x slower                                                    |
| scimark_lu                 | 112 ms                                                                 | 137 ms: 1.22x slower                                                     |
| chaos                      | 56.3 ms                                                                | 69.5 ms: 1.23x slower                                                    |
| typing_runtime_protocols   | 156 us                                                                 | 193 us: 1.24x slower                                                     |
| unpickle_pure_python       | 208 us                                                                 | 259 us: 1.24x slower                                                     |
| django_template            | 34.2 ms                                                                | 42.5 ms: 1.24x slower                                                    |
| pickle_pure_python         | 292 us                                                                 | 363 us: 1.24x slower                                                     |
| comprehensions             | 16.6 us                                                                | 20.8 us: 1.25x slower                                                    |
| deltablue                  | 3.10 ms                                                                | 3.88 ms: 1.25x slower                                                    |
| richards_super             | 50.4 ms                                                                | 63.2 ms: 1.25x slower                                                    |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.4 ms: 1.27x slower                                                    |
| nqueens                    | 77.7 ms                                                                | 98.6 ms: 1.27x slower                                                    |
| crypto_pyaes               | 68.2 ms                                                                | 87.2 ms: 1.28x slower                                                    |
| hexiom                     | 5.95 ms                                                                | 7.68 ms: 1.29x slower                                                    |
| meteor_contest             | 101 ms                                                                 | 132 ms: 1.30x slower                                                     |
| genshi_text                | 21.7 ms                                                                | 28.3 ms: 1.30x slower                                                    |
| coverage                   | 82.5 ms                                                                | 108 ms: 1.31x slower                                                     |
| raytrace                   | 250 ms                                                                 | 327 ms: 1.31x slower                                                     |
| fannkuch                   | 376 ms                                                                 | 503 ms: 1.34x slower                                                     |
| python_startup             | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                                    |
| mako                       | 11.2 ms                                                                | 16.1 ms: 1.43x slower                                                    |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                    |
| nbody                      | 85.3 ms                                                                | 135 ms: 1.58x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 3.17 ms: 3.43x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                                | 96.9 ms: 8.81x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                             |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250326-3.14.0a6+-ca00e74-NOGIL/bm-20250326-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6+-ca00e74.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.076x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.36x