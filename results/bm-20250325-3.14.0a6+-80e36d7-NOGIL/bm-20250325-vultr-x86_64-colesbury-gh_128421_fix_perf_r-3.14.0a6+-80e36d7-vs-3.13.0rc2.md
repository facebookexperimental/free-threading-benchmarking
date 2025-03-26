# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_128421_fix_perf_r
- machine: linux-x86_64
- commit hash: 80e36d7
- commit date: 2025-03-25
- overall geometric mean: 1.076x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 297 ms: 1.14x slower                                                      |
| docutils       | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                                    |
| html5lib       | 68.6 ms                                                                | 72.5 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 552 ms: 1.63x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 580 ms: 1.52x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 331 ms: 1.39x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 299 ms: 1.37x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 485 ms: 1.31x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 275 ms: 1.29x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 518 ms: 1.29x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                     |
| async_generators           | 375 ms                                                                 | 391 ms: 1.04x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.27x faster                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 191 ms: 1.13x faster                                                      |
| float          | 76.7 ms                                                                | 77.7 ms: 1.01x slower                                                     |
| nbody          | 85.3 ms                                                                | 137 ms: 1.60x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.76 ms: 1.17x faster                                                     |
| regex_v8       | 23.2 ms                                                                | 20.9 ms: 1.11x faster                                                     |
| regex_dna      | 189 ms                                                                 | 175 ms: 1.08x faster                                                      |
| regex_compile  | 131 ms                                                                 | 157 ms: 1.19x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.4 ms                                                                | 88.1 ms: 1.07x faster                                                     |
| xml_etree_parse      | 136 ms                                                                 | 129 ms: 1.06x faster                                                      |
| json_loads           | 27.3 us                                                                | 30.5 us: 1.12x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 96.9 ms: 1.13x slower                                                     |
| tomli_loads          | 2.01 sec                                                               | 2.35 sec: 1.17x slower                                                    |
| xml_etree_process    | 59.2 ms                                                                | 70.9 ms: 1.20x slower                                                     |
| json_dumps           | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                     |
| unpickle_pure_python | 208 us                                                                 | 254 us: 1.22x slower                                                      |
| pickle_pure_python   | 292 us                                                                 | 358 us: 1.23x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                                     |
| python_startup_no_site | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 59.3 ms: 1.21x slower                                                     |
| django_template | 34.2 ms                                                                | 42.7 ms: 1.25x slower                                                     |
| genshi_text     | 21.7 ms                                                                | 28.4 ms: 1.31x slower                                                     |
| mako            | 11.2 ms                                                                | 16.0 ms: 1.43x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7 |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| gc_traversal               | 3.32 ms                                                                | 1.79 ms: 1.85x faster                                                     |
| async_tree_io_tg           | 901 ms                                                                 | 552 ms: 1.63x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 580 ms: 1.52x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 238 ms: 1.40x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 331 ms: 1.39x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 299 ms: 1.37x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 485 ms: 1.31x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 275 ms: 1.29x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 518 ms: 1.29x faster                                                      |
| regex_effbot               | 3.21 ms                                                                | 2.76 ms: 1.17x faster                                                     |
| deepcopy                   | 357 us                                                                 | 310 us: 1.15x faster                                                      |
| pidigits                   | 216 ms                                                                 | 191 ms: 1.13x faster                                                      |
| sqlite_synth               | 2.25 us                                                                | 2.02 us: 1.11x faster                                                     |
| regex_v8                   | 23.2 ms                                                                | 20.9 ms: 1.11x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 175 ms: 1.08x faster                                                      |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.1 ms: 1.07x faster                                                     |
| xml_etree_parse            | 136 ms                                                                 | 129 ms: 1.06x faster                                                      |
| dulwich_log                | 74.5 ms                                                                | 73.3 ms: 1.02x faster                                                     |
| coroutines                 | 23.3 ms                                                                | 23.2 ms: 1.01x faster                                                     |
| create_gc_cycles           | 1.33 ms                                                                | 1.35 ms: 1.01x slower                                                     |
| float                      | 76.7 ms                                                                | 77.7 ms: 1.01x slower                                                     |
| go                         | 141 ms                                                                 | 144 ms: 1.02x slower                                                      |
| scimark_sor                | 134 ms                                                                 | 138 ms: 1.03x slower                                                      |
| pathlib                    | 19.3 ms                                                                | 19.9 ms: 1.03x slower                                                     |
| deepcopy_memo              | 38.1 us                                                                | 39.6 us: 1.04x slower                                                     |
| async_generators           | 375 ms                                                                 | 391 ms: 1.04x slower                                                      |
| json                       | 4.98 ms                                                                | 5.22 ms: 1.05x slower                                                     |
| html5lib                   | 68.6 ms                                                                | 72.5 ms: 1.06x slower                                                     |
| docutils                   | 2.63 sec                                                               | 2.79 sec: 1.06x slower                                                    |
| spectral_norm              | 108 ms                                                                 | 114 ms: 1.06x slower                                                      |
| pycparser                  | 1.12 sec                                                               | 1.20 sec: 1.07x slower                                                    |
| bpe_tokeniser              | 4.46 sec                                                               | 4.84 sec: 1.09x slower                                                    |
| json_loads                 | 27.3 us                                                                | 30.5 us: 1.12x slower                                                     |
| mdp                        | 2.34 sec                                                               | 2.62 sec: 1.12x slower                                                    |
| xml_etree_generate         | 85.4 ms                                                                | 96.9 ms: 1.13x slower                                                     |
| thrift                     | 772 us                                                                 | 876 us: 1.14x slower                                                      |
| 2to3                       | 259 ms                                                                 | 297 ms: 1.14x slower                                                      |
| scimark_fft                | 348 ms                                                                 | 400 ms: 1.15x slower                                                      |
| generators                 | 28.5 ms                                                                | 32.8 ms: 1.15x slower                                                     |
| pyflate                    | 449 ms                                                                 | 518 ms: 1.15x slower                                                      |
| pprint_safe_repr           | 719 ms                                                                 | 839 ms: 1.17x slower                                                      |
| tomli_loads                | 2.01 sec                                                               | 2.35 sec: 1.17x slower                                                    |
| telco                      | 7.77 ms                                                                | 9.09 ms: 1.17x slower                                                     |
| logging_silent             | 98.2 ns                                                                | 116 ns: 1.18x slower                                                      |
| logging_simple             | 6.14 us                                                                | 7.31 us: 1.19x slower                                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.74 sec: 1.19x slower                                                    |
| sympy_integrate            | 19.7 ms                                                                | 23.5 ms: 1.19x slower                                                     |
| regex_compile              | 131 ms                                                                 | 157 ms: 1.19x slower                                                      |
| xml_etree_process          | 59.2 ms                                                                | 70.9 ms: 1.20x slower                                                     |
| sympy_sum                  | 154 ms                                                                 | 186 ms: 1.20x slower                                                      |
| coverage                   | 82.5 ms                                                                | 99.6 ms: 1.21x slower                                                     |
| genshi_xml                 | 49.1 ms                                                                | 59.3 ms: 1.21x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 549 ms: 1.21x slower                                                      |
| logging_format             | 6.92 us                                                                | 8.37 us: 1.21x slower                                                     |
| json_dumps                 | 10.6 ms                                                                | 12.9 ms: 1.21x slower                                                     |
| unpickle_pure_python       | 208 us                                                                 | 254 us: 1.22x slower                                                      |
| sympy_str                  | 274 ms                                                                 | 335 ms: 1.22x slower                                                      |
| chaos                      | 56.3 ms                                                                | 68.9 ms: 1.22x slower                                                     |
| pickle_pure_python         | 292 us                                                                 | 358 us: 1.23x slower                                                      |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 5.85 ms: 1.23x slower                                                     |
| comprehensions             | 16.6 us                                                                | 20.6 us: 1.24x slower                                                     |
| django_template            | 34.2 ms                                                                | 42.7 ms: 1.25x slower                                                     |
| richards                   | 44.4 ms                                                                | 55.9 ms: 1.26x slower                                                     |
| scimark_lu                 | 112 ms                                                                 | 142 ms: 1.26x slower                                                      |
| deltablue                  | 3.10 ms                                                                | 3.91 ms: 1.26x slower                                                     |
| nqueens                    | 77.7 ms                                                                | 98.3 ms: 1.26x slower                                                     |
| scimark_monte_carlo        | 65.8 ms                                                                | 83.5 ms: 1.27x slower                                                     |
| hexiom                     | 5.95 ms                                                                | 7.60 ms: 1.28x slower                                                     |
| richards_super             | 50.4 ms                                                                | 64.6 ms: 1.28x slower                                                     |
| crypto_pyaes               | 68.2 ms                                                                | 88.5 ms: 1.30x slower                                                     |
| typing_runtime_protocols   | 156 us                                                                 | 202 us: 1.30x slower                                                      |
| raytrace                   | 250 ms                                                                 | 325 ms: 1.30x slower                                                      |
| genshi_text                | 21.7 ms                                                                | 28.4 ms: 1.31x slower                                                     |
| meteor_contest             | 101 ms                                                                 | 133 ms: 1.31x slower                                                      |
| fannkuch                   | 376 ms                                                                 | 500 ms: 1.33x slower                                                      |
| mako                       | 11.2 ms                                                                | 16.0 ms: 1.43x slower                                                     |
| python_startup             | 11.0 ms                                                                | 15.7 ms: 1.43x slower                                                     |
| python_startup_no_site     | 7.41 ms                                                                | 11.1 ms: 1.50x slower                                                     |
| nbody                      | 85.3 ms                                                                | 137 ms: 1.60x slower                                                      |
| bench_thread_pool          | 924 us                                                                 | 3.16 ms: 3.42x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                                | 96.9 ms: 8.81x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                              |

Benchmark hidden because not significant (3): pylint, asyncio_websockets, deepcopy_reduce
Ignored benchmarks (18) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250325-3.14.0a6+-80e36d7-NOGIL/bm-20250325-vultr-x86_64-colesbury-gh_128421_fix_perf_r-3.14.0a6+-80e36d7.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.076x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.35x