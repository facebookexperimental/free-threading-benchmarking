# Results vs. 3.13.0rc2

- fork: DinoV
- ref: local_type_cache
- machine: linux-x86_64
- commit hash: 1b02bc2
- commit date: 2025-02-12
- overall geometric mean: 1.080x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 304 ms: 1.17x slower                                              |
| docutils       | 2.63 sec                                                               | 2.83 sec: 1.08x slower                                            |
| html5lib       | 68.6 ms                                                                | 71.8 ms: 1.05x slower                                             |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 579 ms: 1.56x faster                                              |
| async_tree_io              | 881 ms                                                                 | 608 ms: 1.45x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 352 ms: 1.31x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 321 ms: 1.28x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 262 ms: 1.27x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 509 ms: 1.24x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 541 ms: 1.23x faster                                              |
| async_tree_none            | 353 ms                                                                 | 289 ms: 1.22x faster                                              |
| async_generators           | 375 ms                                                                 | 376 ms: 1.00x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.22x faster                                                      |

Benchmark hidden because not significant (2): asyncio_websockets, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 203 ms: 1.07x faster                                              |
| float          | 76.7 ms                                                                | 76.4 ms: 1.00x faster                                             |
| nbody          | 85.3 ms                                                                | 131 ms: 1.54x slower                                              |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.74 ms: 1.17x faster                                             |
| regex_dna      | 189 ms                                                                 | 180 ms: 1.05x faster                                              |
| regex_v8       | 23.2 ms                                                                | 23.8 ms: 1.03x slower                                             |
| regex_compile  | 131 ms                                                                 | 151 ms: 1.15x slower                                              |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.3 ms: 1.07x faster                                             |
| xml_etree_parse      | 136 ms                                                                 | 127 ms: 1.07x faster                                              |
| xml_etree_generate   | 85.4 ms                                                                | 96.3 ms: 1.13x slower                                             |
| json_loads           | 27.3 us                                                                | 31.0 us: 1.13x slower                                             |
| xml_etree_process    | 59.2 ms                                                                | 68.1 ms: 1.15x slower                                             |
| tomli_loads          | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                            |
| unpickle_pure_python | 208 us                                                                 | 247 us: 1.18x slower                                              |
| json_dumps           | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                             |
| pickle_pure_python   | 292 us                                                                 | 372 us: 1.28x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 9.63 ms: 1.30x slower                                             |
| python_startup         | 11.0 ms                                                                | 15.4 ms: 1.39x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.35x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 58.9 ms: 1.20x slower                                             |
| django_template | 34.2 ms                                                                | 41.7 ms: 1.22x slower                                             |
| genshi_text     | 21.7 ms                                                                | 28.0 ms: 1.29x slower                                             |
| mako            | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.75 ms: 1.90x faster                                             |
| async_tree_io_tg           | 901 ms                                                                 | 579 ms: 1.56x faster                                              |
| async_tree_io              | 881 ms                                                                 | 608 ms: 1.45x faster                                              |
| async_tree_memoization     | 459 ms                                                                 | 352 ms: 1.31x faster                                              |
| async_tree_memoization_tg  | 410 ms                                                                 | 321 ms: 1.28x faster                                              |
| async_tree_none_tg         | 333 ms                                                                 | 262 ms: 1.27x faster                                              |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 509 ms: 1.24x faster                                              |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 541 ms: 1.23x faster                                              |
| async_tree_none            | 353 ms                                                                 | 289 ms: 1.22x faster                                              |
| regex_effbot               | 3.21 ms                                                                | 2.74 ms: 1.17x faster                                             |
| deepcopy                   | 357 us                                                                 | 305 us: 1.17x faster                                              |
| sqlite_synth               | 2.25 us                                                                | 2.05 us: 1.10x faster                                             |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.3 ms: 1.07x faster                                             |
| xml_etree_parse            | 136 ms                                                                 | 127 ms: 1.07x faster                                              |
| pidigits                   | 216 ms                                                                 | 203 ms: 1.07x faster                                              |
| regex_dna                  | 189 ms                                                                 | 180 ms: 1.05x faster                                              |
| spectral_norm              | 108 ms                                                                 | 106 ms: 1.02x faster                                              |
| scimark_sor                | 134 ms                                                                 | 132 ms: 1.01x faster                                              |
| deepcopy_memo              | 38.1 us                                                                | 37.6 us: 1.01x faster                                             |
| go                         | 141 ms                                                                 | 139 ms: 1.01x faster                                              |
| pathlib                    | 19.3 ms                                                                | 19.1 ms: 1.01x faster                                             |
| float                      | 76.7 ms                                                                | 76.4 ms: 1.00x faster                                             |
| async_generators           | 375 ms                                                                 | 376 ms: 1.00x slower                                              |
| deepcopy_reduce            | 3.12 us                                                                | 3.18 us: 1.02x slower                                             |
| regex_v8                   | 23.2 ms                                                                | 23.8 ms: 1.03x slower                                             |
| html5lib                   | 68.6 ms                                                                | 71.8 ms: 1.05x slower                                             |
| create_gc_cycles           | 1.33 ms                                                                | 1.40 ms: 1.05x slower                                             |
| bpe_tokeniser              | 4.46 sec                                                               | 4.69 sec: 1.05x slower                                            |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.06x slower                                            |
| docutils                   | 2.63 sec                                                               | 2.83 sec: 1.08x slower                                            |
| json                       | 4.98 ms                                                                | 5.41 ms: 1.08x slower                                             |
| telco                      | 7.77 ms                                                                | 8.45 ms: 1.09x slower                                             |
| pyflate                    | 449 ms                                                                 | 493 ms: 1.10x slower                                              |
| dulwich_log                | 74.5 ms                                                                | 82.4 ms: 1.11x slower                                             |
| generators                 | 28.5 ms                                                                | 31.7 ms: 1.11x slower                                             |
| scimark_fft                | 348 ms                                                                 | 388 ms: 1.12x slower                                              |
| logging_silent             | 98.2 ns                                                                | 110 ns: 1.12x slower                                              |
| xml_etree_generate         | 85.4 ms                                                                | 96.3 ms: 1.13x slower                                             |
| sqlglot_normalize          | 106 ms                                                                 | 119 ms: 1.13x slower                                              |
| json_loads                 | 27.3 us                                                                | 31.0 us: 1.13x slower                                             |
| pprint_safe_repr           | 719 ms                                                                 | 815 ms: 1.13x slower                                              |
| regex_compile              | 131 ms                                                                 | 151 ms: 1.15x slower                                              |
| xml_etree_process          | 59.2 ms                                                                | 68.1 ms: 1.15x slower                                             |
| sqlglot_optimize           | 52.7 ms                                                                | 60.9 ms: 1.16x slower                                             |
| pprint_pformat             | 1.46 sec                                                               | 1.69 sec: 1.16x slower                                            |
| logging_simple             | 6.14 us                                                                | 7.15 us: 1.16x slower                                             |
| thrift                     | 772 us                                                                 | 901 us: 1.17x slower                                              |
| 2to3                       | 259 ms                                                                 | 304 ms: 1.17x slower                                              |
| tomli_loads                | 2.01 sec                                                               | 2.36 sec: 1.17x slower                                            |
| mdp                        | 2.34 sec                                                               | 2.76 sec: 1.18x slower                                            |
| unpickle_pure_python       | 208 us                                                                 | 247 us: 1.18x slower                                              |
| coverage                   | 82.5 ms                                                                | 98.0 ms: 1.19x slower                                             |
| logging_format             | 6.92 us                                                                | 8.28 us: 1.20x slower                                             |
| genshi_xml                 | 49.1 ms                                                                | 58.9 ms: 1.20x slower                                             |
| json_dumps                 | 10.6 ms                                                                | 12.8 ms: 1.20x slower                                             |
| comprehensions             | 16.6 us                                                                | 19.9 us: 1.20x slower                                             |
| sympy_expand               | 454 ms                                                                 | 546 ms: 1.20x slower                                              |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.21x slower                                              |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.76 ms: 1.21x slower                                             |
| django_template            | 34.2 ms                                                                | 41.7 ms: 1.22x slower                                             |
| sympy_str                  | 274 ms                                                                 | 334 ms: 1.22x slower                                              |
| sympy_integrate            | 19.7 ms                                                                | 24.1 ms: 1.22x slower                                             |
| scimark_lu                 | 112 ms                                                                 | 137 ms: 1.22x slower                                              |
| chaos                      | 56.3 ms                                                                | 69.3 ms: 1.23x slower                                             |
| sqlglot_transpile          | 1.55 ms                                                                | 1.92 ms: 1.23x slower                                             |
| hexiom                     | 5.95 ms                                                                | 7.36 ms: 1.24x slower                                             |
| nqueens                    | 77.7 ms                                                                | 96.1 ms: 1.24x slower                                             |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.4 ms: 1.27x slower                                             |
| typing_runtime_protocols   | 156 us                                                                 | 197 us: 1.27x slower                                              |
| richards                   | 44.4 ms                                                                | 56.5 ms: 1.27x slower                                             |
| pickle_pure_python         | 292 us                                                                 | 372 us: 1.28x slower                                              |
| sqlglot_parse              | 1.25 ms                                                                | 1.59 ms: 1.28x slower                                             |
| meteor_contest             | 101 ms                                                                 | 130 ms: 1.28x slower                                              |
| genshi_text                | 21.7 ms                                                                | 28.0 ms: 1.29x slower                                             |
| crypto_pyaes               | 68.2 ms                                                                | 87.8 ms: 1.29x slower                                             |
| richards_super             | 50.4 ms                                                                | 65.3 ms: 1.30x slower                                             |
| python_startup_no_site     | 7.41 ms                                                                | 9.63 ms: 1.30x slower                                             |
| fannkuch                   | 376 ms                                                                 | 490 ms: 1.30x slower                                              |
| raytrace                   | 250 ms                                                                 | 328 ms: 1.31x slower                                              |
| python_startup             | 11.0 ms                                                                | 15.4 ms: 1.39x slower                                             |
| mako                       | 11.2 ms                                                                | 15.8 ms: 1.41x slower                                             |
| deltablue                  | 3.10 ms                                                                | 4.72 ms: 1.52x slower                                             |
| nbody                      | 85.3 ms                                                                | 131 ms: 1.54x slower                                              |
| bench_thread_pool          | 924 us                                                                 | 3.32 ms: 3.60x slower                                             |
| bench_mp_pool              | 11.0 ms                                                                | 95.2 ms: 8.65x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                                      |

Benchmark hidden because not significant (3): asyncio_websockets, pylint, coroutines
Ignored benchmarks (14) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250212-3.14.0a4+-1b02bc2-NOGIL/bm-20250212-vultr-x86_64-DinoV-local_type_cache-3.14.0a4+-1b02bc2.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.080x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x