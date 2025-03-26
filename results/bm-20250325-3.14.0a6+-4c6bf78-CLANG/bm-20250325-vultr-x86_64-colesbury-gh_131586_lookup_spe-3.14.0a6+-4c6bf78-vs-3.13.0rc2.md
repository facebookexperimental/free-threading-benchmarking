# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_131586_lookup_spe
- machine: linux-x86_64
- commit hash: 4c6bf78
- commit date: 2025-03-25
- overall geometric mean: 1.102x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 244 ms: 1.06x faster                                                      |
| docutils       | 2.63 sec                                                               | 2.52 sec: 1.04x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 298 ms: 1.54x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 586 ms: 1.51x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 603 ms: 1.50x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 289 ms: 1.42x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 473 ms: 1.41x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 451 ms: 1.41x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 241 ms: 1.38x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 260 ms: 1.36x faster                                                      |
| async_generators           | 375 ms                                                                 | 313 ms: 1.20x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 20.5 ms: 1.14x faster                                                     |
| Geometric mean             | (ref)                                                                  | 1.34x faster                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                                      |
| float          | 76.7 ms                                                                | 68.9 ms: 1.11x faster                                                     |
| nbody          | 85.3 ms                                                                | 81.2 ms: 1.05x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.10x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.99 ms: 1.07x faster                                                     |
| regex_compile  | 131 ms                                                                 | 122 ms: 1.07x faster                                                      |
| regex_v8       | 23.2 ms                                                                | 21.8 ms: 1.07x faster                                                     |
| regex_dna      | 189 ms                                                                 | 184 ms: 1.03x faster                                                      |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                               | 1.76 sec: 1.14x faster                                                    |
| xml_etree_process    | 59.2 ms                                                                | 55.4 ms: 1.07x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 81.3 ms: 1.05x faster                                                     |
| json_loads           | 27.3 us                                                                | 26.6 us: 1.03x faster                                                     |
| unpickle_pure_python | 208 us                                                                 | 204 us: 1.02x faster                                                      |
| pickle_pure_python   | 292 us                                                                 | 296 us: 1.02x slower                                                      |
| xml_etree_iterparse  | 94.4 ms                                                                | 96.2 ms: 1.02x slower                                                     |
| json_dumps           | 10.6 ms                                                                | 11.6 ms: 1.09x slower                                                     |
| xml_etree_parse      | 136 ms                                                                 | 149 ms: 1.09x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.62 ms: 1.16x slower                                                     |
| python_startup         | 11.0 ms                                                                | 14.9 ms: 1.35x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.25x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text     | 21.7 ms                                                                | 19.3 ms: 1.13x faster                                                     |
| genshi_xml      | 49.1 ms                                                                | 45.4 ms: 1.08x faster                                                     |
| django_template | 34.2 ms                                                                | 32.6 ms: 1.05x faster                                                     |
| mako            | 11.2 ms                                                                | 11.5 ms: 1.02x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.06x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_memoization     | 459 ms                                                                 | 298 ms: 1.54x faster                                                      |
| deepcopy                   | 357 us                                                                 | 234 us: 1.53x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 586 ms: 1.51x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 603 ms: 1.50x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 289 ms: 1.42x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 473 ms: 1.41x faster                                                      |
| deepcopy_memo              | 38.1 us                                                                | 27.0 us: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 451 ms: 1.41x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 241 ms: 1.38x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 260 ms: 1.36x faster                                                      |
| go                         | 141 ms                                                                 | 104 ms: 1.36x faster                                                      |
| scimark_sor                | 134 ms                                                                 | 99.2 ms: 1.35x faster                                                     |
| deepcopy_reduce            | 3.12 us                                                                | 2.33 us: 1.34x faster                                                     |
| spectral_norm              | 108 ms                                                                 | 80.6 ms: 1.33x faster                                                     |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 3.62 ms: 1.31x faster                                                     |
| scimark_fft                | 348 ms                                                                 | 275 ms: 1.27x faster                                                      |
| async_generators           | 375 ms                                                                 | 313 ms: 1.20x faster                                                      |
| scimark_monte_carlo        | 65.8 ms                                                                | 56.0 ms: 1.18x faster                                                     |
| pylint                     | 317 ms                                                                 | 271 ms: 1.17x faster                                                      |
| pyflate                    | 449 ms                                                                 | 387 ms: 1.16x faster                                                      |
| richards                   | 44.4 ms                                                                | 38.3 ms: 1.16x faster                                                     |
| tomli_loads                | 2.01 sec                                                               | 1.76 sec: 1.14x faster                                                    |
| telco                      | 7.77 ms                                                                | 6.82 ms: 1.14x faster                                                     |
| coroutines                 | 23.3 ms                                                                | 20.5 ms: 1.14x faster                                                     |
| logging_silent             | 98.2 ns                                                                | 86.3 ns: 1.14x faster                                                     |
| dulwich_log                | 74.5 ms                                                                | 65.6 ms: 1.13x faster                                                     |
| richards_super             | 50.4 ms                                                                | 44.4 ms: 1.13x faster                                                     |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                                      |
| genshi_text                | 21.7 ms                                                                | 19.3 ms: 1.13x faster                                                     |
| coverage                   | 82.5 ms                                                                | 73.6 ms: 1.12x faster                                                     |
| comprehensions             | 16.6 us                                                                | 14.8 us: 1.12x faster                                                     |
| chaos                      | 56.3 ms                                                                | 50.5 ms: 1.12x faster                                                     |
| scimark_lu                 | 112 ms                                                                 | 101 ms: 1.11x faster                                                      |
| float                      | 76.7 ms                                                                | 68.9 ms: 1.11x faster                                                     |
| logging_format             | 6.92 us                                                                | 6.28 us: 1.10x faster                                                     |
| logging_simple             | 6.14 us                                                                | 5.59 us: 1.10x faster                                                     |
| hexiom                     | 5.95 ms                                                                | 5.44 ms: 1.09x faster                                                     |
| deltablue                  | 3.10 ms                                                                | 2.84 ms: 1.09x faster                                                     |
| bpe_tokeniser              | 4.46 sec                                                               | 4.12 sec: 1.08x faster                                                    |
| genshi_xml                 | 49.1 ms                                                                | 45.4 ms: 1.08x faster                                                     |
| generators                 | 28.5 ms                                                                | 26.5 ms: 1.08x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.99 ms: 1.07x faster                                                     |
| regex_compile              | 131 ms                                                                 | 122 ms: 1.07x faster                                                      |
| nqueens                    | 77.7 ms                                                                | 72.5 ms: 1.07x faster                                                     |
| typing_runtime_protocols   | 156 us                                                                 | 146 us: 1.07x faster                                                      |
| xml_etree_process          | 59.2 ms                                                                | 55.4 ms: 1.07x faster                                                     |
| regex_v8                   | 23.2 ms                                                                | 21.8 ms: 1.07x faster                                                     |
| thrift                     | 772 us                                                                 | 726 us: 1.06x faster                                                      |
| 2to3                       | 259 ms                                                                 | 244 ms: 1.06x faster                                                      |
| sympy_integrate            | 19.7 ms                                                                | 18.6 ms: 1.06x faster                                                     |
| raytrace                   | 250 ms                                                                 | 238 ms: 1.05x faster                                                      |
| nbody                      | 85.3 ms                                                                | 81.2 ms: 1.05x faster                                                     |
| xml_etree_generate         | 85.4 ms                                                                | 81.3 ms: 1.05x faster                                                     |
| django_template            | 34.2 ms                                                                | 32.6 ms: 1.05x faster                                                     |
| docutils                   | 2.63 sec                                                               | 2.52 sec: 1.04x faster                                                    |
| sympy_str                  | 274 ms                                                                 | 263 ms: 1.04x faster                                                      |
| pycparser                  | 1.12 sec                                                               | 1.08 sec: 1.04x faster                                                    |
| sqlite_synth               | 2.25 us                                                                | 2.16 us: 1.04x faster                                                     |
| pathlib                    | 19.3 ms                                                                | 18.7 ms: 1.03x faster                                                     |
| json_loads                 | 27.3 us                                                                | 26.6 us: 1.03x faster                                                     |
| sympy_sum                  | 154 ms                                                                 | 150 ms: 1.03x faster                                                      |
| sympy_expand               | 454 ms                                                                 | 441 ms: 1.03x faster                                                      |
| regex_dna                  | 189 ms                                                                 | 184 ms: 1.03x faster                                                      |
| unpickle_pure_python       | 208 us                                                                 | 204 us: 1.02x faster                                                      |
| json                       | 4.98 ms                                                                | 4.89 ms: 1.02x faster                                                     |
| pprint_safe_repr           | 719 ms                                                                 | 711 ms: 1.01x faster                                                      |
| pprint_pformat             | 1.46 sec                                                               | 1.44 sec: 1.01x faster                                                    |
| crypto_pyaes               | 68.2 ms                                                                | 67.9 ms: 1.00x faster                                                     |
| fannkuch                   | 376 ms                                                                 | 379 ms: 1.01x slower                                                      |
| pickle_pure_python         | 292 us                                                                 | 296 us: 1.02x slower                                                      |
| xml_etree_iterparse        | 94.4 ms                                                                | 96.2 ms: 1.02x slower                                                     |
| mako                       | 11.2 ms                                                                | 11.5 ms: 1.02x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 104 ms: 1.02x slower                                                      |
| mdp                        | 2.34 sec                                                               | 2.45 sec: 1.05x slower                                                    |
| bench_thread_pool          | 924 us                                                                 | 1.01 ms: 1.09x slower                                                     |
| json_dumps                 | 10.6 ms                                                                | 11.6 ms: 1.09x slower                                                     |
| xml_etree_parse            | 136 ms                                                                 | 149 ms: 1.09x slower                                                      |
| python_startup_no_site     | 7.41 ms                                                                | 8.62 ms: 1.16x slower                                                     |
| gc_traversal               | 3.32 ms                                                                | 4.38 ms: 1.32x slower                                                     |
| python_startup             | 11.0 ms                                                                | 14.9 ms: 1.35x slower                                                     |
| create_gc_cycles           | 1.33 ms                                                                | 1.92 ms: 1.44x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                                | 87.8 ms: 7.98x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.07x faster                                                              |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (19) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250325-3.14.0a6+-4c6bf78-CLANG/bm-20250325-vultr-x86_64-colesbury-gh_131586_lookup_spe-3.14.0a6+-4c6bf78.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.102x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.15x