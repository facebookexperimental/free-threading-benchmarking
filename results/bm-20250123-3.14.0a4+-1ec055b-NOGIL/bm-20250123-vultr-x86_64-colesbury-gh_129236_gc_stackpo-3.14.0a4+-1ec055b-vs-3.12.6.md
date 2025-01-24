# Results vs. 3.12.6

- fork: colesbury
- ref: gh_129236_gc_stackpo
- machine: linux-x86_64
- commit hash: 1ec055b
- commit date: 2025-01-23
- overall geometric mean: 1.048x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 303 ms: 1.15x slower                                                      |
| docutils       | 2.64 sec                                               | 2.82 sec: 1.07x slower                                                    |
| html5lib       | 63.6 ms                                                | 68.4 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                  | 1.10x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 578 ms: 1.92x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 611 ms: 1.77x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 321 ms: 1.74x faster                                                      |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 353 ms: 1.57x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 507 ms: 1.42x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 538 ms: 1.33x faster                                                      |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                                      |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                      |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.8 ms: 1.07x faster                                                     |
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                                      |
| nbody          | 89.3 ms                                                | 132 ms: 1.48x slower                                                      |
| Geometric mean | (ref)                                                  | 1.13x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                     |
| regex_compile  | 142 ms                                                 | 150 ms: 1.05x slower                                                      |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                      |
| regex_v8       | 20.6 ms                                                | 24.0 ms: 1.17x slower                                                     |
| Geometric mean | (ref)                                                  | 1.04x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.2 ms: 1.11x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.08x faster                                                      |
| tomli_loads          | 2.11 sec                                               | 2.34 sec: 1.11x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 246 us: 1.11x slower                                                      |
| xml_etree_generate   | 85.2 ms                                                | 96.7 ms: 1.13x slower                                                     |
| json_loads           | 26.5 us                                                | 30.6 us: 1.15x slower                                                     |
| xml_etree_process    | 59.0 ms                                                | 69.3 ms: 1.17x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 375 us: 1.22x slower                                                      |
| json_dumps           | 10.4 ms                                                | 13.1 ms: 1.27x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.60 ms: 1.34x slower                                                     |
| python_startup         | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.8 ms: 1.19x slower                                                     |
| genshi_text     | 22.8 ms                                                | 27.4 ms: 1.20x slower                                                     |
| django_template | 34.7 ms                                                | 44.0 ms: 1.27x slower                                                     |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| gc_traversal               | 3.46 ms                                                | 1.66 ms: 2.08x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 578 ms: 1.92x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 252 ms: 1.77x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 611 ms: 1.77x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 321 ms: 1.74x faster                                                      |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 353 ms: 1.57x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 507 ms: 1.42x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 538 ms: 1.33x faster                                                      |
| pathlib                    | 21.5 ms                                                | 18.9 ms: 1.14x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                     |
| deepcopy                   | 352 us                                                 | 316 us: 1.11x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 87.2 ms: 1.11x faster                                                     |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.08x faster                                                      |
| float                      | 80.8 ms                                                | 75.8 ms: 1.07x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.08 us: 1.06x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 38.4 us: 1.05x faster                                                     |
| generators                 | 32.2 ms                                                | 31.4 ms: 1.03x faster                                                     |
| async_generators           | 384 ms                                                 | 375 ms: 1.03x faster                                                      |
| coroutines                 | 23.9 ms                                                | 23.5 ms: 1.02x faster                                                     |
| go                         | 139 ms                                                 | 137 ms: 1.02x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                      |
| bpe_tokeniser              | 4.74 sec                                               | 4.72 sec: 1.00x faster                                                    |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                                    |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                                      |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                                      |
| comprehensions             | 19.8 us                                                | 20.6 us: 1.04x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.19 us: 1.04x slower                                                     |
| logging_silent             | 109 ns                                                 | 113 ns: 1.04x slower                                                      |
| scimark_sor                | 130 ms                                                 | 136 ms: 1.04x slower                                                      |
| dulwich_log                | 78.9 ms                                                | 82.5 ms: 1.05x slower                                                     |
| regex_compile              | 142 ms                                                 | 150 ms: 1.05x slower                                                      |
| mdp                        | 2.42 sec                                               | 2.59 sec: 1.07x slower                                                    |
| docutils                   | 2.64 sec                                               | 2.82 sec: 1.07x slower                                                    |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                      |
| json                       | 5.02 ms                                                | 5.39 ms: 1.07x slower                                                     |
| html5lib                   | 63.6 ms                                                | 68.4 ms: 1.08x slower                                                     |
| raytrace                   | 299 ms                                                 | 327 ms: 1.09x slower                                                      |
| logging_simple             | 6.63 us                                                | 7.27 us: 1.10x slower                                                     |
| pyflate                    | 448 ms                                                 | 495 ms: 1.10x slower                                                      |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.1 ms: 1.11x slower                                                     |
| chaos                      | 62.8 ms                                                | 69.7 ms: 1.11x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 826 ms: 1.11x slower                                                      |
| tomli_loads                | 2.11 sec                                               | 2.34 sec: 1.11x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 246 us: 1.11x slower                                                      |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                                    |
| scimark_fft                | 342 ms                                                 | 383 ms: 1.12x slower                                                      |
| sympy_sum                  | 166 ms                                                 | 187 ms: 1.13x slower                                                      |
| xml_etree_generate         | 85.2 ms                                                | 96.7 ms: 1.13x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.14x slower                                                      |
| crypto_pyaes               | 76.6 ms                                                | 87.1 ms: 1.14x slower                                                     |
| sqlglot_transpile          | 1.67 ms                                                | 1.91 ms: 1.14x slower                                                     |
| logging_format             | 7.35 us                                                | 8.41 us: 1.14x slower                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 164 ms: 1.15x slower                                                      |
| sympy_str                  | 292 ms                                                 | 335 ms: 1.15x slower                                                      |
| 2to3                       | 264 ms                                                 | 303 ms: 1.15x slower                                                      |
| thrift                     | 791 us                                                 | 909 us: 1.15x slower                                                      |
| json_loads                 | 26.5 us                                                | 30.6 us: 1.15x slower                                                     |
| sqlglot_optimize           | 53.3 ms                                                | 61.8 ms: 1.16x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 24.0 ms: 1.17x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 1.59 ms: 1.17x slower                                                     |
| sympy_expand               | 468 ms                                                 | 548 ms: 1.17x slower                                                      |
| xml_etree_process          | 59.0 ms                                                | 69.3 ms: 1.17x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 24.3 ms: 1.18x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 81.0 ms: 1.18x slower                                                     |
| hexiom                     | 6.17 ms                                                | 7.30 ms: 1.18x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 59.8 ms: 1.19x slower                                                     |
| genshi_text                | 22.8 ms                                                | 27.4 ms: 1.20x slower                                                     |
| richards                   | 45.9 ms                                                | 55.2 ms: 1.20x slower                                                     |
| nqueens                    | 80.1 ms                                                | 96.3 ms: 1.20x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 375 us: 1.22x slower                                                      |
| scimark_lu                 | 114 ms                                                 | 139 ms: 1.22x slower                                                      |
| richards_super             | 51.9 ms                                                | 63.8 ms: 1.23x slower                                                     |
| typing_runtime_protocols   | 163 us                                                 | 202 us: 1.24x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.49 ms: 1.25x slower                                                     |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.26x slower                                                      |
| json_dumps                 | 10.4 ms                                                | 13.1 ms: 1.27x slower                                                     |
| django_template            | 34.7 ms                                                | 44.0 ms: 1.27x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.40 ms: 1.29x slower                                                     |
| fannkuch                   | 372 ms                                                 | 480 ms: 1.29x slower                                                      |
| telco                      | 6.53 ms                                                | 8.44 ms: 1.29x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 9.60 ms: 1.34x slower                                                     |
| deltablue                  | 3.45 ms                                                | 4.63 ms: 1.34x slower                                                     |
| coverage                   | 71.4 ms                                                | 97.7 ms: 1.37x slower                                                     |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                     |
| nbody                      | 89.3 ms                                                | 132 ms: 1.48x slower                                                      |
| python_startup             | 9.93 ms                                                | 15.3 ms: 1.54x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.53x slower                                                     |
| bench_mp_pool              | 10.8 ms                                                | 95.0 ms: 8.80x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                              |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250123-3.14.0a4+-1ec055b-NOGIL/bm-20250123-vultr-x86_64-colesbury-gh_129236_gc_stackpo-3.14.0a4+-1ec055b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.048x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.36x