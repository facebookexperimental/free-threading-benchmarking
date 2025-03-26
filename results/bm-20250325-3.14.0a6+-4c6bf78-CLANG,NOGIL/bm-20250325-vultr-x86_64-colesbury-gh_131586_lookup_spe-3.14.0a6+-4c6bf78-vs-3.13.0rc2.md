# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_131586_lookup_spe
- machine: linux-x86_64
- commit hash: 4c6bf78
- commit date: 2025-03-25
- overall geometric mean: 1.011x faster
- HPT reliability: 86.40%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 277 ms: 1.07x slower                                                      |
| docutils       | 2.63 sec                                                               | 2.65 sec: 1.01x slower                                                    |
| html5lib       | 68.6 ms                                                                | 63.1 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 491 ms: 1.83x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 529 ms: 1.67x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 215 ms: 1.55x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 269 ms: 1.52x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 303 ms: 1.52x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 428 ms: 1.48x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 463 ms: 1.44x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 253 ms: 1.40x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 19.3 ms: 1.21x faster                                                     |
| async_generators           | 375 ms                                                                 | 331 ms: 1.13x faster                                                      |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                      |
| Geometric mean             | (ref)                                                                  | 1.41x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 186 ms: 1.16x faster                                                      |
| float          | 76.7 ms                                                                | 68.5 ms: 1.12x faster                                                     |
| nbody          | 85.3 ms                                                                | 121 ms: 1.41x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 23.2 ms                                                                | 20.5 ms: 1.13x faster                                                     |
| regex_effbot   | 3.21 ms                                                                | 3.01 ms: 1.07x faster                                                     |
| regex_dna      | 189 ms                                                                 | 184 ms: 1.03x faster                                                      |
| regex_compile  | 131 ms                                                                 | 139 ms: 1.06x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 87.2 ms: 1.08x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 85.8 ms: 1.00x slower                                                     |
| tomli_loads          | 2.01 sec                                                               | 2.07 sec: 1.03x slower                                                    |
| xml_etree_process    | 59.2 ms                                                                | 61.4 ms: 1.04x slower                                                     |
| xml_etree_parse      | 136 ms                                                                 | 144 ms: 1.06x slower                                                      |
| json_loads           | 27.3 us                                                                | 29.6 us: 1.08x slower                                                     |
| unpickle_pure_python | 208 us                                                                 | 227 us: 1.09x slower                                                      |
| pickle_pure_python   | 292 us                                                                 | 328 us: 1.12x slower                                                      |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.22x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.06x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                                     |
| python_startup_no_site | 7.41 ms                                                                | 11.0 ms: 1.48x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.44x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 53.0 ms: 1.08x slower                                                     |
| django_template | 34.2 ms                                                                | 37.1 ms: 1.09x slower                                                     |
| genshi_text     | 21.7 ms                                                                | 24.7 ms: 1.14x slower                                                     |
| mako            | 11.2 ms                                                                | 15.0 ms: 1.33x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.15x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 491 ms: 1.83x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 529 ms: 1.67x faster                                                      |
| gc_traversal               | 3.32 ms                                                                | 2.06 ms: 1.61x faster                                                     |
| async_tree_none_tg         | 333 ms                                                                 | 215 ms: 1.55x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 269 ms: 1.52x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 303 ms: 1.52x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 428 ms: 1.48x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 463 ms: 1.44x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 253 ms: 1.40x faster                                                      |
| deepcopy                   | 357 us                                                                 | 273 us: 1.31x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 19.3 ms: 1.21x faster                                                     |
| scimark_sor                | 134 ms                                                                 | 112 ms: 1.19x faster                                                      |
| spectral_norm              | 108 ms                                                                 | 91.5 ms: 1.17x faster                                                     |
| pidigits                   | 216 ms                                                                 | 186 ms: 1.16x faster                                                      |
| sqlite_synth               | 2.25 us                                                                | 1.98 us: 1.13x faster                                                     |
| regex_v8                   | 23.2 ms                                                                | 20.5 ms: 1.13x faster                                                     |
| async_generators           | 375 ms                                                                 | 331 ms: 1.13x faster                                                      |
| deepcopy_reduce            | 3.12 us                                                                | 2.78 us: 1.12x faster                                                     |
| float                      | 76.7 ms                                                                | 68.5 ms: 1.12x faster                                                     |
| go                         | 141 ms                                                                 | 126 ms: 1.12x faster                                                      |
| deepcopy_memo              | 38.1 us                                                                | 34.1 us: 1.12x faster                                                     |
| html5lib                   | 68.6 ms                                                                | 63.1 ms: 1.09x faster                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 87.2 ms: 1.08x faster                                                     |
| pylint                     | 317 ms                                                                 | 293 ms: 1.08x faster                                                      |
| logging_silent             | 98.2 ns                                                                | 91.9 ns: 1.07x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 3.01 ms: 1.07x faster                                                     |
| scimark_fft                | 348 ms                                                                 | 329 ms: 1.06x faster                                                      |
| dulwich_log                | 74.5 ms                                                                | 70.6 ms: 1.05x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 184 ms: 1.03x faster                                                      |
| generators                 | 28.5 ms                                                                | 27.8 ms: 1.03x faster                                                     |
| pathlib                    | 19.3 ms                                                                | 18.9 ms: 1.02x faster                                                     |
| bpe_tokeniser              | 4.46 sec                                                               | 4.43 sec: 1.01x faster                                                    |
| asyncio_websockets         | 517 ms                                                                 | 515 ms: 1.00x faster                                                      |
| xml_etree_generate         | 85.4 ms                                                                | 85.8 ms: 1.00x slower                                                     |
| docutils                   | 2.63 sec                                                               | 2.65 sec: 1.01x slower                                                    |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.82 ms: 1.02x slower                                                     |
| pycparser                  | 1.12 sec                                                               | 1.15 sec: 1.02x slower                                                    |
| tomli_loads                | 2.01 sec                                                               | 2.07 sec: 1.03x slower                                                    |
| scimark_lu                 | 112 ms                                                                 | 116 ms: 1.03x slower                                                      |
| xml_etree_process          | 59.2 ms                                                                | 61.4 ms: 1.04x slower                                                     |
| json                       | 4.98 ms                                                                | 5.17 ms: 1.04x slower                                                     |
| telco                      | 7.77 ms                                                                | 8.10 ms: 1.04x slower                                                     |
| pyflate                    | 449 ms                                                                 | 471 ms: 1.05x slower                                                      |
| comprehensions             | 16.6 us                                                                | 17.5 us: 1.05x slower                                                     |
| xml_etree_parse            | 136 ms                                                                 | 144 ms: 1.06x slower                                                      |
| regex_compile              | 131 ms                                                                 | 139 ms: 1.06x slower                                                      |
| 2to3                       | 259 ms                                                                 | 277 ms: 1.07x slower                                                      |
| thrift                     | 772 us                                                                 | 830 us: 1.08x slower                                                      |
| scimark_monte_carlo        | 65.8 ms                                                                | 70.8 ms: 1.08x slower                                                     |
| chaos                      | 56.3 ms                                                                | 60.6 ms: 1.08x slower                                                     |
| genshi_xml                 | 49.1 ms                                                                | 53.0 ms: 1.08x slower                                                     |
| json_loads                 | 27.3 us                                                                | 29.6 us: 1.08x slower                                                     |
| richards                   | 44.4 ms                                                                | 48.1 ms: 1.08x slower                                                     |
| django_template            | 34.2 ms                                                                | 37.1 ms: 1.09x slower                                                     |
| nqueens                    | 77.7 ms                                                                | 84.5 ms: 1.09x slower                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 783 ms: 1.09x slower                                                      |
| unpickle_pure_python       | 208 us                                                                 | 227 us: 1.09x slower                                                      |
| sympy_integrate            | 19.7 ms                                                                | 21.6 ms: 1.09x slower                                                     |
| logging_format             | 6.92 us                                                                | 7.58 us: 1.10x slower                                                     |
| logging_simple             | 6.14 us                                                                | 6.76 us: 1.10x slower                                                     |
| deltablue                  | 3.10 ms                                                                | 3.43 ms: 1.11x slower                                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.61 sec: 1.11x slower                                                    |
| sympy_sum                  | 154 ms                                                                 | 172 ms: 1.11x slower                                                      |
| typing_runtime_protocols   | 156 us                                                                 | 174 us: 1.12x slower                                                      |
| sympy_str                  | 274 ms                                                                 | 307 ms: 1.12x slower                                                      |
| richards_super             | 50.4 ms                                                                | 56.5 ms: 1.12x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 509 ms: 1.12x slower                                                      |
| pickle_pure_python         | 292 us                                                                 | 328 us: 1.12x slower                                                      |
| hexiom                     | 5.95 ms                                                                | 6.70 ms: 1.13x slower                                                     |
| genshi_text                | 21.7 ms                                                                | 24.7 ms: 1.14x slower                                                     |
| raytrace                   | 250 ms                                                                 | 286 ms: 1.15x slower                                                      |
| coverage                   | 82.5 ms                                                                | 95.1 ms: 1.15x slower                                                     |
| fannkuch                   | 376 ms                                                                 | 438 ms: 1.17x slower                                                      |
| mdp                        | 2.34 sec                                                               | 2.74 sec: 1.17x slower                                                    |
| crypto_pyaes               | 68.2 ms                                                                | 81.6 ms: 1.20x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 123 ms: 1.21x slower                                                      |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.22x slower                                                     |
| mako                       | 11.2 ms                                                                | 15.0 ms: 1.33x slower                                                     |
| python_startup             | 11.0 ms                                                                | 15.5 ms: 1.41x slower                                                     |
| nbody                      | 85.3 ms                                                                | 121 ms: 1.41x slower                                                      |
| python_startup_no_site     | 7.41 ms                                                                | 11.0 ms: 1.48x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 3.11 ms: 3.37x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                                | 94.9 ms: 8.63x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                              |

Benchmark hidden because not significant (1): create_gc_cycles
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250325-3.14.0a6+-4c6bf78-CLANG,NOGIL/bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.011x faster

# HPT report

- Reliability score: 86.40% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x