# Results vs. 3.12.6

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: 5a139fe
- commit date: 2025-04-08
- overall geometric mean: 1.008x slower
- HPT reliability: 98.28%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 289 ms: 1.10x slower                                                  |
| docutils       | 2.64 sec                                               | 2.77 sec: 1.05x slower                                                |
| html5lib       | 63.6 ms                                                | 70.0 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 538 ms: 2.06x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.91x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 567 ms: 1.91x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 293 ms: 1.91x faster                                                  |
| async_tree_none            | 464 ms                                                 | 267 ms: 1.74x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 321 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 516 ms: 1.39x faster                                                  |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                  |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.51x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.4 ms: 1.15x faster                                                 |
| pidigits       | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| nbody          | 89.3 ms                                                | 116 ms: 1.30x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                 |
| regex_compile  | 142 ms                                                 | 151 ms: 1.06x slower                                                  |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.0 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.25 sec: 1.07x slower                                                |
| unpickle_pure_python | 221 us                                                 | 240 us: 1.09x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 343 us: 1.12x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.6 ms: 1.12x slower                                                 |
| json_loads           | 26.5 us                                                | 30.5 us: 1.15x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.2 ms: 1.17x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.2 ms: 1.57x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 58.5 ms: 1.17x slower                                                 |
| genshi_text     | 22.8 ms                                                | 27.3 ms: 1.20x slower                                                 |
| django_template | 34.7 ms                                                | 41.9 ms: 1.21x slower                                                 |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.25x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 538 ms: 2.06x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 234 ms: 1.91x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 567 ms: 1.91x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 293 ms: 1.91x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.82 ms: 1.90x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.36 sec: 1.78x faster                                                |
| async_tree_none            | 464 ms                                                 | 267 ms: 1.74x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 321 ms: 1.73x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 486 ms: 1.49x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 516 ms: 1.39x faster                                                  |
| deepcopy                   | 352 us                                                 | 298 us: 1.18x faster                                                  |
| float                      | 80.8 ms                                                | 70.4 ms: 1.15x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.0 ms: 1.11x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                 |
| deepcopy_memo              | 40.3 us                                                | 36.7 us: 1.10x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.02 us: 1.09x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 73.7 ms: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| go                         | 139 ms                                                 | 133 ms: 1.05x faster                                                  |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.62 sec: 1.03x faster                                                |
| deepcopy_reduce            | 3.08 us                                                | 3.02 us: 1.02x faster                                                 |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                 |
| scimark_sor                | 130 ms                                                 | 128 ms: 1.01x faster                                                  |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| comprehensions             | 19.8 us                                                | 20.1 us: 1.01x slower                                                 |
| chaos                      | 62.8 ms                                                | 63.6 ms: 1.01x slower                                                 |
| raytrace                   | 299 ms                                                 | 303 ms: 1.01x slower                                                  |
| logging_silent             | 109 ns                                                 | 110 ns: 1.01x slower                                                  |
| generators                 | 32.2 ms                                                | 33.0 ms: 1.02x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.2 ms: 1.03x slower                                                 |
| json                       | 5.02 ms                                                | 5.24 ms: 1.04x slower                                                 |
| scimark_fft                | 342 ms                                                 | 358 ms: 1.05x slower                                                  |
| pidigits                   | 184 ms                                                 | 193 ms: 1.05x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.77 sec: 1.05x slower                                                |
| pyflate                    | 448 ms                                                 | 475 ms: 1.06x slower                                                  |
| regex_compile              | 142 ms                                                 | 151 ms: 1.06x slower                                                  |
| tomli_loads                | 2.11 sec                                               | 2.25 sec: 1.07x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 798 ms: 1.07x slower                                                  |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.75 ms: 1.09x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 240 us: 1.09x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.66 sec: 1.10x slower                                                |
| 2to3                       | 264 ms                                                 | 289 ms: 1.10x slower                                                  |
| html5lib                   | 63.6 ms                                                | 70.0 ms: 1.10x slower                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                                  |
| logging_simple             | 6.63 us                                                | 7.32 us: 1.10x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 84.6 ms: 1.10x slower                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.1 ms: 1.11x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.11x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 343 us: 1.12x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 23.0 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 95.6 ms: 1.12x slower                                                 |
| logging_format             | 7.35 us                                                | 8.24 us: 1.12x slower                                                 |
| nqueens                    | 80.1 ms                                                | 90.2 ms: 1.13x slower                                                 |
| sympy_str                  | 292 ms                                                 | 329 ms: 1.13x slower                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 77.5 ms: 1.13x slower                                                 |
| hexiom                     | 6.17 ms                                                | 7.07 ms: 1.15x slower                                                 |
| json_loads                 | 26.5 us                                                | 30.5 us: 1.15x slower                                                 |
| sympy_expand               | 468 ms                                                 | 545 ms: 1.16x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 58.5 ms: 1.17x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.13 ms: 1.17x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 134 ms: 1.17x slower                                                  |
| richards                   | 45.9 ms                                                | 53.8 ms: 1.17x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 69.2 ms: 1.17x slower                                                 |
| richards_super             | 51.9 ms                                                | 61.2 ms: 1.18x slower                                                 |
| genshi_text                | 22.8 ms                                                | 27.3 ms: 1.20x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 197 us: 1.20x slower                                                  |
| django_template            | 34.7 ms                                                | 41.9 ms: 1.21x slower                                                 |
| meteor_contest             | 104 ms                                                 | 128 ms: 1.23x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.24x slower                                                 |
| fannkuch                   | 372 ms                                                 | 463 ms: 1.24x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.38 ms: 1.27x slower                                                 |
| nbody                      | 89.3 ms                                                | 116 ms: 1.30x slower                                                  |
| telco                      | 6.53 ms                                                | 8.55 ms: 1.31x slower                                                 |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                 |
| coverage                   | 71.4 ms                                                | 108 ms: 1.52x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 11.2 ms: 1.57x slower                                                 |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.35x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 96.2 ms: 8.91x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (3): pylint, pycparser, asyncio_websockets
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250408-3.14.0a7+-5a139fe-NOGIL/bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.008x slower

# HPT report

- Reliability score: 98.28% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x