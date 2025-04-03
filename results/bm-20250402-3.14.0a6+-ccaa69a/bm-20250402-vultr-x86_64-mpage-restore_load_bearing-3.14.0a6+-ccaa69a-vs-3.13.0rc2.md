# Results vs. 3.13.0rc2

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: ccaa69a
- commit date: 2025-04-02
- overall geometric mean: 1.032x faster
- HPT reliability: 86.83%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 255 ms: 1.02x faster                                                  |
| docutils       | 2.63 sec                                                               | 2.62 sec: 1.00x faster                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 901 ms                                                                 | 636 ms: 1.42x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 327 ms: 1.41x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 636 ms: 1.39x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 513 ms: 1.30x faster                                                  |
| async_tree_memoization_tg  | 410 ms                                                                 | 330 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 510 ms: 1.24x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 269 ms: 1.24x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 287 ms: 1.23x faster                                                  |
| async_generators           | 375 ms                                                                 | 338 ms: 1.11x faster                                                  |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.22x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 76.7 ms                                                                | 72.4 ms: 1.06x faster                                                 |
| pidigits       | 216 ms                                                                 | 206 ms: 1.05x faster                                                  |
| nbody          | 85.3 ms                                                                | 95.9 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                 |
| regex_dna      | 189 ms                                                                 | 173 ms: 1.09x faster                                                  |
| regex_v8       | 23.2 ms                                                                | 21.6 ms: 1.07x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.08x faster                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                                 | 131 ms: 1.04x faster                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.00 sec: 1.01x faster                                                |
| json_loads           | 27.3 us                                                                | 27.5 us: 1.01x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                                | 86.2 ms: 1.01x slower                                                 |
| xml_etree_process    | 59.2 ms                                                                | 61.7 ms: 1.04x slower                                                 |
| unpickle_pure_python | 208 us                                                                 | 222 us: 1.07x slower                                                  |
| json_dumps           | 10.6 ms                                                                | 11.4 ms: 1.07x slower                                                 |
| pickle_pure_python   | 292 us                                                                 | 317 us: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 8.65 ms: 1.17x slower                                                 |
| python_startup         | 11.0 ms                                                                | 15.1 ms: 1.37x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                | 50.3 ms: 1.03x slower                                                 |
| django_template | 34.2 ms                                                                | 37.0 ms: 1.08x slower                                                 |
| mako            | 11.2 ms                                                                | 12.2 ms: 1.09x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.34 sec                                                               | 1.19 sec: 1.97x faster                                                |
| async_tree_io_tg           | 901 ms                                                                 | 636 ms: 1.42x faster                                                  |
| async_tree_memoization     | 459 ms                                                                 | 327 ms: 1.41x faster                                                  |
| async_tree_io              | 881 ms                                                                 | 636 ms: 1.39x faster                                                  |
| deepcopy                   | 357 us                                                                 | 261 us: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                                 | 513 ms: 1.30x faster                                                  |
| deepcopy_memo              | 38.1 us                                                                | 30.2 us: 1.26x faster                                                 |
| async_tree_memoization_tg  | 410 ms                                                                 | 330 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed_tg | 634 ms                                                                 | 510 ms: 1.24x faster                                                  |
| async_tree_none_tg         | 333 ms                                                                 | 269 ms: 1.24x faster                                                  |
| async_tree_none            | 353 ms                                                                 | 287 ms: 1.23x faster                                                  |
| go                         | 141 ms                                                                 | 117 ms: 1.21x faster                                                  |
| regex_effbot               | 3.21 ms                                                                | 2.77 ms: 1.16x faster                                                 |
| deepcopy_reduce            | 3.12 us                                                                | 2.71 us: 1.15x faster                                                 |
| scimark_sor                | 134 ms                                                                 | 116 ms: 1.15x faster                                                  |
| async_generators           | 375 ms                                                                 | 338 ms: 1.11x faster                                                  |
| pylint                     | 317 ms                                                                 | 288 ms: 1.10x faster                                                  |
| regex_dna                  | 189 ms                                                                 | 173 ms: 1.09x faster                                                  |
| spectral_norm              | 108 ms                                                                 | 99.4 ms: 1.08x faster                                                 |
| dulwich_log                | 74.5 ms                                                                | 68.8 ms: 1.08x faster                                                 |
| regex_v8                   | 23.2 ms                                                                | 21.6 ms: 1.07x faster                                                 |
| pyflate                    | 449 ms                                                                 | 422 ms: 1.07x faster                                                  |
| float                      | 76.7 ms                                                                | 72.4 ms: 1.06x faster                                                 |
| scimark_sparse_mat_mult    | 4.75 ms                                                                | 4.51 ms: 1.05x faster                                                 |
| pidigits                   | 216 ms                                                                 | 206 ms: 1.05x faster                                                  |
| scimark_fft                | 348 ms                                                                 | 331 ms: 1.05x faster                                                  |
| scimark_monte_carlo        | 65.8 ms                                                                | 62.6 ms: 1.05x faster                                                 |
| telco                      | 7.77 ms                                                                | 7.45 ms: 1.04x faster                                                 |
| xml_etree_parse            | 136 ms                                                                 | 131 ms: 1.04x faster                                                  |
| sqlite_synth               | 2.25 us                                                                | 2.19 us: 1.03x faster                                                 |
| bpe_tokeniser              | 4.46 sec                                                               | 4.34 sec: 1.03x faster                                                |
| coverage                   | 82.5 ms                                                                | 80.4 ms: 1.03x faster                                                 |
| 2to3                       | 259 ms                                                                 | 255 ms: 1.02x faster                                                  |
| json                       | 4.98 ms                                                                | 4.93 ms: 1.01x faster                                                 |
| richards                   | 44.4 ms                                                                | 44.0 ms: 1.01x faster                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.00 sec: 1.01x faster                                                |
| docutils                   | 2.63 sec                                                               | 2.62 sec: 1.00x faster                                                |
| sympy_integrate            | 19.7 ms                                                                | 19.8 ms: 1.00x slower                                                 |
| json_loads                 | 27.3 us                                                                | 27.5 us: 1.01x slower                                                 |
| pathlib                    | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                                | 86.2 ms: 1.01x slower                                                 |
| chaos                      | 56.3 ms                                                                | 57.2 ms: 1.02x slower                                                 |
| logging_format             | 6.92 us                                                                | 7.04 us: 1.02x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                                |
| coroutines                 | 23.3 ms                                                                | 23.8 ms: 1.02x slower                                                 |
| crypto_pyaes               | 68.2 ms                                                                | 69.6 ms: 1.02x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 159 us: 1.02x slower                                                  |
| logging_simple             | 6.14 us                                                                | 6.30 us: 1.03x slower                                                 |
| genshi_xml                 | 49.1 ms                                                                | 50.3 ms: 1.03x slower                                                 |
| scimark_lu                 | 112 ms                                                                 | 116 ms: 1.03x slower                                                  |
| logging_silent             | 98.2 ns                                                                | 101 ns: 1.03x slower                                                  |
| sympy_str                  | 274 ms                                                                 | 283 ms: 1.03x slower                                                  |
| pprint_safe_repr           | 719 ms                                                                 | 743 ms: 1.03x slower                                                  |
| generators                 | 28.5 ms                                                                | 29.6 ms: 1.04x slower                                                 |
| xml_etree_process          | 59.2 ms                                                                | 61.7 ms: 1.04x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 6.21 ms: 1.04x slower                                                 |
| comprehensions             | 16.6 us                                                                | 17.3 us: 1.05x slower                                                 |
| pprint_pformat             | 1.46 sec                                                               | 1.52 sec: 1.05x slower                                                |
| sympy_sum                  | 154 ms                                                                 | 162 ms: 1.05x slower                                                  |
| raytrace                   | 250 ms                                                                 | 263 ms: 1.05x slower                                                  |
| sympy_expand               | 454 ms                                                                 | 478 ms: 1.05x slower                                                  |
| fannkuch                   | 376 ms                                                                 | 398 ms: 1.06x slower                                                  |
| nqueens                    | 77.7 ms                                                                | 82.5 ms: 1.06x slower                                                 |
| unpickle_pure_python       | 208 us                                                                 | 222 us: 1.07x slower                                                  |
| json_dumps                 | 10.6 ms                                                                | 11.4 ms: 1.07x slower                                                 |
| django_template            | 34.2 ms                                                                | 37.0 ms: 1.08x slower                                                 |
| pickle_pure_python         | 292 us                                                                 | 317 us: 1.09x slower                                                  |
| mako                       | 11.2 ms                                                                | 12.2 ms: 1.09x slower                                                 |
| deltablue                  | 3.10 ms                                                                | 3.41 ms: 1.10x slower                                                 |
| nbody                      | 85.3 ms                                                                | 95.9 ms: 1.12x slower                                                 |
| bench_thread_pool          | 924 us                                                                 | 1.07 ms: 1.15x slower                                                 |
| python_startup_no_site     | 7.41 ms                                                                | 8.65 ms: 1.17x slower                                                 |
| gc_traversal               | 3.32 ms                                                                | 4.49 ms: 1.35x slower                                                 |
| python_startup             | 11.0 ms                                                                | 15.1 ms: 1.37x slower                                                 |
| create_gc_cycles           | 1.33 ms                                                                | 1.85 ms: 1.38x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                                | 89.4 ms: 8.13x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (6): richards_super, xml_etree_iterparse, asyncio_websockets, regex_compile, meteor_contest, genshi_text
Ignored benchmarks (20) of results/bm-20240920-3.13.0rc2-4981ec5/bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (12) of results/bm-20250402-3.14.0a6+-ccaa69a/bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.032x faster

# HPT report

- Reliability score: 86.83% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x