# Results vs. 3.13.0rc2

- fork: python
- ref: cc0e59f17d0fcd8ed9f3
- machine: linux-x86_64
- commit hash: cc0e59f
- commit date: 2026-11-25
- overall geometric mean: 1.063x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 253 ms: 1.03x faster                                                      |
| docutils       | 2.63 sec                                                               | 2.29 sec: 1.15x faster                                                    |
| html5lib       | 68.6 ms                                                                | 56.6 ms: 1.21x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.13x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_generators           | 375 ms                                                                 | 224 ms: 1.67x faster                                                      |
| async_tree_memoization     | 459 ms                                                                 | 334 ms: 1.38x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 659 ms: 1.34x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 506 ms: 1.32x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 687 ms: 1.31x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 519 ms: 1.22x faster                                                      |
| async_tree_memoization_tg  | 410 ms                                                                 | 341 ms: 1.20x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 278 ms: 1.20x faster                                                      |
| coroutines                 | 23.3 ms                                                                | 22.7 ms: 1.03x faster                                                     |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                      |
| Geometric mean             | (ref)                                                                  | 1.25x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 178 ms: 1.21x faster                                                      |
| float          | 76.7 ms                                                                | 71.1 ms: 1.08x faster                                                     |
| nbody          | 85.3 ms                                                                | 89.5 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.74 ms: 1.17x faster                                                     |
| regex_v8       | 23.2 ms                                                                | 21.4 ms: 1.08x faster                                                     |
| regex_dna      | 189 ms                                                                 | 179 ms: 1.05x faster                                                      |
| regex_compile  | 131 ms                                                                 | 147 ms: 1.12x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 10.6 ms                                                                | 9.13 ms: 1.16x faster                                                     |
| tomli_loads          | 2.01 sec                                                               | 1.81 sec: 1.11x faster                                                    |
| xml_etree_iterparse  | 94.4 ms                                                                | 88.9 ms: 1.06x faster                                                     |
| json_loads           | 27.3 us                                                                | 26.0 us: 1.05x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                                | 84.6 ms: 1.01x faster                                                     |
| unpickle_pure_python | 208 us                                                                 | 210 us: 1.01x slower                                                      |
| xml_etree_parse      | 136 ms                                                                 | 141 ms: 1.04x slower                                                      |
| pickle_pure_python   | 292 us                                                                 | 312 us: 1.07x slower                                                      |
| Geometric mean       | (ref)                                                                  | 1.03x faster                                                              |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 7.31 ms: 1.01x faster                                                     |
| python_startup         | 11.0 ms                                                                | 11.0 ms: 1.00x faster                                                     |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.2 ms                                                                | 34.5 ms: 1.01x slower                                                     |
| mako            | 11.2 ms                                                                | 11.7 ms: 1.04x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f |
|----------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                                 | 106 ms: 2.99x faster                                                      |
| mdp                        | 2.34 sec                                                               | 1.13 sec: 2.07x faster                                                    |
| async_generators           | 375 ms                                                                 | 224 ms: 1.67x faster                                                      |
| deepcopy                   | 357 us                                                                 | 233 us: 1.54x faster                                                      |
| typing_runtime_protocols   | 156 us                                                                 | 108 us: 1.45x faster                                                      |
| deepcopy_memo              | 38.1 us                                                                | 27.2 us: 1.40x faster                                                     |
| async_tree_memoization     | 459 ms                                                                 | 334 ms: 1.38x faster                                                      |
| go                         | 141 ms                                                                 | 102 ms: 1.37x faster                                                      |
| async_tree_io              | 881 ms                                                                 | 659 ms: 1.34x faster                                                      |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 506 ms: 1.32x faster                                                      |
| async_tree_io_tg           | 901 ms                                                                 | 687 ms: 1.31x faster                                                      |
| async_tree_none            | 353 ms                                                                 | 277 ms: 1.28x faster                                                      |
| scimark_sor                | 134 ms                                                                 | 106 ms: 1.26x faster                                                      |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 519 ms: 1.22x faster                                                      |
| deepcopy_reduce            | 3.12 us                                                                | 2.56 us: 1.22x faster                                                     |
| pidigits                   | 216 ms                                                                 | 178 ms: 1.21x faster                                                      |
| html5lib                   | 68.6 ms                                                                | 56.6 ms: 1.21x faster                                                     |
| async_tree_memoization_tg  | 410 ms                                                                 | 341 ms: 1.20x faster                                                      |
| async_tree_none_tg         | 333 ms                                                                 | 278 ms: 1.20x faster                                                      |
| spectral_norm              | 108 ms                                                                 | 90.9 ms: 1.18x faster                                                     |
| regex_effbot               | 3.21 ms                                                                | 2.74 ms: 1.17x faster                                                     |
| json_dumps                 | 10.6 ms                                                                | 9.13 ms: 1.16x faster                                                     |
| docutils                   | 2.63 sec                                                               | 2.29 sec: 1.15x faster                                                    |
| pyflate                    | 449 ms                                                                 | 392 ms: 1.14x faster                                                      |
| scimark_fft                | 348 ms                                                                 | 308 ms: 1.13x faster                                                      |
| dulwich_log                | 74.5 ms                                                                | 66.3 ms: 1.12x faster                                                     |
| tomli_loads                | 2.01 sec                                                               | 1.81 sec: 1.11x faster                                                    |
| pathlib                    | 19.3 ms                                                                | 17.7 ms: 1.09x faster                                                     |
| regex_v8                   | 23.2 ms                                                                | 21.4 ms: 1.08x faster                                                     |
| bpe_tokeniser              | 4.46 sec                                                               | 4.13 sec: 1.08x faster                                                    |
| float                      | 76.7 ms                                                                | 71.1 ms: 1.08x faster                                                     |
| hexiom                     | 5.95 ms                                                                | 5.59 ms: 1.06x faster                                                     |
| scimark_monte_carlo        | 65.8 ms                                                                | 61.9 ms: 1.06x faster                                                     |
| xml_etree_iterparse        | 94.4 ms                                                                | 88.9 ms: 1.06x faster                                                     |
| regex_dna                  | 189 ms                                                                 | 179 ms: 1.05x faster                                                      |
| json_loads                 | 27.3 us                                                                | 26.0 us: 1.05x faster                                                     |
| sqlite_synth               | 2.25 us                                                                | 2.15 us: 1.05x faster                                                     |
| comprehensions             | 16.6 us                                                                | 15.9 us: 1.05x faster                                                     |
| logging_silent             | 98.2 ns                                                                | 94.2 ns: 1.04x faster                                                     |
| scimark_lu                 | 112 ms                                                                 | 108 ms: 1.04x faster                                                      |
| json                       | 4.98 ms                                                                | 4.79 ms: 1.04x faster                                                     |
| sympy_integrate            | 19.7 ms                                                                | 19.1 ms: 1.03x faster                                                     |
| coroutines                 | 23.3 ms                                                                | 22.7 ms: 1.03x faster                                                     |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.61 ms: 1.03x faster                                                     |
| 2to3                       | 259 ms                                                                 | 253 ms: 1.03x faster                                                      |
| richards                   | 44.4 ms                                                                | 43.3 ms: 1.03x faster                                                     |
| nqueens                    | 77.7 ms                                                                | 75.8 ms: 1.03x faster                                                     |
| pycparser                  | 1.12 sec                                                               | 1.09 sec: 1.02x faster                                                    |
| crypto_pyaes               | 68.2 ms                                                                | 66.6 ms: 1.02x faster                                                     |
| richards_super             | 50.4 ms                                                                | 49.3 ms: 1.02x faster                                                     |
| logging_format             | 6.92 us                                                                | 6.78 us: 1.02x faster                                                     |
| chaos                      | 56.3 ms                                                                | 55.4 ms: 1.02x faster                                                     |
| fannkuch                   | 376 ms                                                                 | 370 ms: 1.02x faster                                                      |
| python_startup_no_site     | 7.41 ms                                                                | 7.31 ms: 1.01x faster                                                     |
| logging_simple             | 6.14 us                                                                | 6.07 us: 1.01x faster                                                     |
| xml_etree_generate         | 85.4 ms                                                                | 84.6 ms: 1.01x faster                                                     |
| python_startup             | 11.0 ms                                                                | 11.0 ms: 1.00x faster                                                     |
| unpickle_pure_python       | 208 us                                                                 | 210 us: 1.01x slower                                                      |
| django_template            | 34.2 ms                                                                | 34.5 ms: 1.01x slower                                                     |
| pprint_pformat             | 1.46 sec                                                               | 1.47 sec: 1.01x slower                                                    |
| raytrace                   | 250 ms                                                                 | 253 ms: 1.01x slower                                                      |
| coverage                   | 82.5 ms                                                                | 83.8 ms: 1.02x slower                                                     |
| thrift                     | 772 us                                                                 | 785 us: 1.02x slower                                                      |
| sympy_str                  | 274 ms                                                                 | 279 ms: 1.02x slower                                                      |
| sympy_sum                  | 154 ms                                                                 | 158 ms: 1.03x slower                                                      |
| xml_etree_parse            | 136 ms                                                                 | 141 ms: 1.04x slower                                                      |
| create_gc_cycles           | 1.33 ms                                                                | 1.38 ms: 1.04x slower                                                     |
| sympy_expand               | 454 ms                                                                 | 472 ms: 1.04x slower                                                      |
| mako                       | 11.2 ms                                                                | 11.7 ms: 1.04x slower                                                     |
| generators                 | 28.5 ms                                                                | 29.8 ms: 1.04x slower                                                     |
| deltablue                  | 3.10 ms                                                                | 3.24 ms: 1.05x slower                                                     |
| nbody                      | 85.3 ms                                                                | 89.5 ms: 1.05x slower                                                     |
| asyncio_websockets         | 517 ms                                                                 | 544 ms: 1.05x slower                                                      |
| pickle_pure_python         | 292 us                                                                 | 312 us: 1.07x slower                                                      |
| regex_compile              | 131 ms                                                                 | 147 ms: 1.12x slower                                                      |
| gc_traversal               | 3.32 ms                                                                | 3.77 ms: 1.14x slower                                                     |
| bench_thread_pool          | 924 us                                                                 | 1.34 ms: 1.45x slower                                                     |
| telco                      | 7.77 ms                                                                | 158 ms: 20.38x slower                                                     |
| bench_mp_pool              | 11.0 ms                                                                | 232 ms: 21.09x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                              |

Benchmark hidden because not significant (3): xml_etree_process, pprint_safe_repr, meteor_contest
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261125-3.16.0a2+dev-cc0e59f/bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2+dev-cc0e59f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.063x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x