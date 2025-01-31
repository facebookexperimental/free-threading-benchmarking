# Results vs. 3.12.6

- fork: nascheme
- ref: gh_129201_gc_mark_pr
- machine: linux-x86_64
- commit hash: e12dd2e
- commit date: 2025-01-30
- overall geometric mean: 1.054x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 305 ms: 1.16x slower                                                     |
| docutils       | 2.64 sec                                               | 2.76 sec: 1.05x slower                                                   |
| html5lib       | 63.6 ms                                                | 68.5 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                  | 1.09x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 574 ms: 1.93x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 320 ms: 1.75x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.71x faster                                                     |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 502 ms: 1.44x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 532 ms: 1.34x faster                                                     |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                    |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.6 ms: 1.07x faster                                                    |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                     |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                     |
| Geometric mean | (ref)                                                  | 1.13x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.74 ms: 1.16x faster                                                    |
| regex_compile  | 142 ms                                                 | 149 ms: 1.05x slower                                                     |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                     |
| regex_v8       | 20.6 ms                                                | 23.1 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                  | 1.02x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.3 ms: 1.10x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 2.29 sec: 1.08x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 245 us: 1.11x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 96.3 ms: 1.13x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 68.5 ms: 1.16x slower                                                    |
| json_loads           | 26.5 us                                                | 31.4 us: 1.18x slower                                                    |
| json_dumps           | 10.4 ms                                                | 12.8 ms: 1.23x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 379 us: 1.23x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.82 ms: 1.37x slower                                                    |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.6 ms: 1.19x slower                                                    |
| genshi_text     | 22.8 ms                                                | 27.5 ms: 1.20x slower                                                    |
| django_template | 34.7 ms                                                | 43.1 ms: 1.24x slower                                                    |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 574 ms: 1.93x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 606 ms: 1.79x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 320 ms: 1.75x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.71x faster                                                     |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 502 ms: 1.44x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 532 ms: 1.34x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.74 ms: 1.16x faster                                                    |
| pathlib                    | 21.5 ms                                                | 18.7 ms: 1.15x faster                                                    |
| deepcopy                   | 352 us                                                 | 312 us: 1.13x faster                                                     |
| xml_etree_iterparse        | 96.7 ms                                                | 88.3 ms: 1.10x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 3.19 ms: 1.08x faster                                                    |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                    |
| float                      | 80.8 ms                                                | 75.6 ms: 1.07x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 38.2 us: 1.05x faster                                                    |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                                    |
| go                         | 139 ms                                                 | 135 ms: 1.03x faster                                                     |
| async_generators           | 384 ms                                                 | 376 ms: 1.02x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.63 sec: 1.02x faster                                                   |
| spectral_norm              | 110 ms                                                 | 110 ms: 1.00x slower                                                     |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                                   |
| scimark_sor                | 130 ms                                                 | 130 ms: 1.01x slower                                                     |
| comprehensions             | 19.8 us                                                | 20.0 us: 1.01x slower                                                    |
| logging_silent             | 109 ns                                                 | 112 ns: 1.02x slower                                                     |
| generators                 | 32.2 ms                                                | 33.1 ms: 1.03x slower                                                    |
| deepcopy_reduce            | 3.08 us                                                | 3.18 us: 1.03x slower                                                    |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                     |
| dulwich_log                | 78.9 ms                                                | 82.1 ms: 1.04x slower                                                    |
| regex_compile              | 142 ms                                                 | 149 ms: 1.05x slower                                                     |
| docutils                   | 2.64 sec                                               | 2.76 sec: 1.05x slower                                                   |
| html5lib                   | 63.6 ms                                                | 68.5 ms: 1.08x slower                                                    |
| json                       | 5.02 ms                                                | 5.42 ms: 1.08x slower                                                    |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                     |
| raytrace                   | 299 ms                                                 | 325 ms: 1.08x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.29 sec: 1.08x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.24 us: 1.09x slower                                                    |
| chaos                      | 62.8 ms                                                | 68.6 ms: 1.09x slower                                                    |
| mdp                        | 2.42 sec                                               | 2.65 sec: 1.10x slower                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.0 ms: 1.10x slower                                                    |
| scimark_fft                | 342 ms                                                 | 378 ms: 1.11x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 245 us: 1.11x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 826 ms: 1.11x slower                                                     |
| logging_format             | 7.35 us                                                | 8.19 us: 1.11x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                                   |
| pyflate                    | 448 ms                                                 | 502 ms: 1.12x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 23.1 ms: 1.12x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.12x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.13x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 96.3 ms: 1.13x slower                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 1.89 ms: 1.13x slower                                                    |
| thrift                     | 791 us                                                 | 901 us: 1.14x slower                                                     |
| crypto_pyaes               | 76.6 ms                                                | 87.8 ms: 1.15x slower                                                    |
| sqlglot_optimize           | 53.3 ms                                                | 61.0 ms: 1.15x slower                                                    |
| sympy_str                  | 292 ms                                                 | 335 ms: 1.15x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 1.57 ms: 1.16x slower                                                    |
| 2to3                       | 264 ms                                                 | 305 ms: 1.16x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 68.5 ms: 1.16x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 24.0 ms: 1.17x slower                                                    |
| sympy_expand               | 468 ms                                                 | 550 ms: 1.18x slower                                                     |
| json_loads                 | 26.5 us                                                | 31.4 us: 1.18x slower                                                    |
| hexiom                     | 6.17 ms                                                | 7.30 ms: 1.18x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 59.6 ms: 1.19x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 81.5 ms: 1.19x slower                                                    |
| nqueens                    | 80.1 ms                                                | 96.3 ms: 1.20x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 137 ms: 1.20x slower                                                     |
| genshi_text                | 22.8 ms                                                | 27.5 ms: 1.20x slower                                                    |
| richards                   | 45.9 ms                                                | 55.9 ms: 1.22x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 201 us: 1.23x slower                                                     |
| json_dumps                 | 10.4 ms                                                | 12.8 ms: 1.23x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 379 us: 1.23x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.43 ms: 1.24x slower                                                    |
| django_template            | 34.7 ms                                                | 43.1 ms: 1.24x slower                                                    |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.25x slower                                                     |
| richards_super             | 51.9 ms                                                | 65.6 ms: 1.26x slower                                                    |
| fannkuch                   | 372 ms                                                 | 490 ms: 1.31x slower                                                     |
| deltablue                  | 3.45 ms                                                | 4.57 ms: 1.32x slower                                                    |
| telco                      | 6.53 ms                                                | 8.66 ms: 1.33x slower                                                    |
| coverage                   | 71.4 ms                                                | 96.7 ms: 1.35x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 9.82 ms: 1.37x slower                                                    |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                    |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                     |
| python_startup             | 9.93 ms                                                | 15.6 ms: 1.57x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.73 ms: 1.58x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.31 ms: 3.51x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 92.6 ms: 8.58x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                             |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250130-3.14.0a4+-e12dd2e-NOGIL/bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.054x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x