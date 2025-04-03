# Results vs. 3.12.6

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: ccaa69a
- commit date: 2025-04-02
- overall geometric mean: 1.070x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.03x faster                                                  |
| docutils       | 2.64 sec                                               | 2.62 sec: 1.01x faster                                                |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 636 ms: 1.75x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 636 ms: 1.70x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 327 ms: 1.70x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 330 ms: 1.70x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 269 ms: 1.66x faster                                                  |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 510 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 513 ms: 1.39x faster                                                  |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.43x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.4 ms: 1.12x faster                                                 |
| nbody          | 89.3 ms                                                | 95.9 ms: 1.07x slower                                                 |
| pidigits       | 184 ms                                                 | 206 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                 |
| regex_compile  | 142 ms                                                 | 132 ms: 1.08x faster                                                  |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                  |
| regex_v8       | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.00 sec: 1.06x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 94.3 ms: 1.03x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 222 us: 1.01x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 86.2 ms: 1.01x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 317 us: 1.03x slower                                                  |
| json_loads           | 26.5 us                                                | 27.5 us: 1.04x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 61.7 ms: 1.05x slower                                                 |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.65 ms: 1.21x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.1 ms: 1.52x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.8 ms: 1.05x faster                                                 |
| django_template | 34.7 ms                                                | 37.0 ms: 1.07x slower                                                 |
| mako            | 11.0 ms                                                | 12.2 ms: 1.11x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.19 sec: 2.03x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 636 ms: 1.75x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 636 ms: 1.70x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 327 ms: 1.70x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 330 ms: 1.70x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 269 ms: 1.66x faster                                                  |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 510 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 513 ms: 1.39x faster                                                  |
| deepcopy                   | 352 us                                                 | 261 us: 1.35x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 30.2 us: 1.33x faster                                                 |
| go                         | 139 ms                                                 | 117 ms: 1.19x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 68.8 ms: 1.15x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.3 us: 1.14x faster                                                 |
| raytrace                   | 299 ms                                                 | 263 ms: 1.14x faster                                                  |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.71 us: 1.14x faster                                                 |
| float                      | 80.8 ms                                                | 72.4 ms: 1.12x faster                                                 |
| scimark_sor                | 130 ms                                                 | 116 ms: 1.12x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                 |
| spectral_norm              | 110 ms                                                 | 99.4 ms: 1.11x faster                                                 |
| pylint                     | 319 ms                                                 | 288 ms: 1.10x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 69.6 ms: 1.10x faster                                                 |
| chaos                      | 62.8 ms                                                | 57.2 ms: 1.10x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 62.6 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.34 sec: 1.09x faster                                                |
| generators                 | 32.2 ms                                                | 29.6 ms: 1.09x faster                                                 |
| regex_compile              | 142 ms                                                 | 132 ms: 1.08x faster                                                  |
| logging_silent             | 109 ns                                                 | 101 ns: 1.08x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 133 ms: 1.07x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 20.4 ms: 1.07x faster                                                 |
| pyflate                    | 448 ms                                                 | 422 ms: 1.06x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 131 ms: 1.06x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 2.00 sec: 1.06x faster                                                |
| logging_simple             | 6.63 us                                                | 6.30 us: 1.05x faster                                                 |
| genshi_text                | 22.8 ms                                                | 21.8 ms: 1.05x faster                                                 |
| richards                   | 45.9 ms                                                | 44.0 ms: 1.05x faster                                                 |
| logging_format             | 7.35 us                                                | 7.04 us: 1.04x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.8 ms: 1.04x faster                                                 |
| 2to3                       | 264 ms                                                 | 255 ms: 1.03x faster                                                  |
| scimark_fft                | 342 ms                                                 | 331 ms: 1.03x faster                                                  |
| richards_super             | 51.9 ms                                                | 50.3 ms: 1.03x faster                                                 |
| sympy_str                  | 292 ms                                                 | 283 ms: 1.03x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 162 ms: 1.03x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 159 us: 1.03x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 94.3 ms: 1.03x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.02x faster                                                |
| json                       | 5.02 ms                                                | 4.93 ms: 1.02x faster                                                 |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.02x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.41 ms: 1.01x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.62 sec: 1.01x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.19 us: 1.01x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.8 ms: 1.01x faster                                                 |
| hexiom                     | 6.17 ms                                                | 6.21 ms: 1.01x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 222 us: 1.01x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 86.2 ms: 1.01x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 116 ms: 1.01x slower                                                  |
| sympy_expand               | 468 ms                                                 | 478 ms: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.51 ms: 1.03x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 317 us: 1.03x slower                                                  |
| nqueens                    | 80.1 ms                                                | 82.5 ms: 1.03x slower                                                 |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                  |
| json_loads                 | 26.5 us                                                | 27.5 us: 1.04x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 61.7 ms: 1.05x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.6 ms: 1.05x slower                                                 |
| django_template            | 34.7 ms                                                | 37.0 ms: 1.07x slower                                                 |
| fannkuch                   | 372 ms                                                 | 398 ms: 1.07x slower                                                  |
| nbody                      | 89.3 ms                                                | 95.9 ms: 1.07x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                 |
| mako                       | 11.0 ms                                                | 12.2 ms: 1.11x slower                                                 |
| pidigits                   | 184 ms                                                 | 206 ms: 1.12x slower                                                  |
| coverage                   | 71.4 ms                                                | 80.4 ms: 1.13x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.07 ms: 1.13x slower                                                 |
| telco                      | 6.53 ms                                                | 7.45 ms: 1.14x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 8.65 ms: 1.21x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.49 ms: 1.30x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.1 ms: 1.52x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.69x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 89.4 ms: 8.28x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (4): asyncio_websockets, pprint_safe_repr, pprint_pformat, genshi_xml
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250402-3.14.0a6+-ccaa69a/bm-20250402-vultr-x86_64-mpage-restore_load_bearing-3.14.0a6+-ccaa69a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.13x