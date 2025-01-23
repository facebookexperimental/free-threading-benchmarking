# Results vs. 3.12.6

- fork: nascheme
- ref: gh_129201_gc_mark_pr
- machine: linux-x86_64
- commit hash: 1b4e8c3
- commit date: 2025-01-22
- overall geometric mean: 1.071x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 307 ms: 1.17x slower                                                     |
| docutils       | 2.64 sec                                               | 2.82 sec: 1.07x slower                                                   |
| html5lib       | 63.6 ms                                                | 71.3 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                  | 1.12x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 240 ms: 1.86x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                                     |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 583 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 621 ms: 1.15x faster                                                     |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                     |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.3 ms: 1.07x faster                                                    |
| pidigits       | 184 ms                                                 | 221 ms: 1.20x slower                                                     |
| nbody          | 89.3 ms                                                | 135 ms: 1.51x slower                                                     |
| Geometric mean | (ref)                                                  | 1.19x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.95 ms: 1.07x faster                                                    |
| regex_compile  | 142 ms                                                 | 150 ms: 1.05x slower                                                     |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                     |
| regex_v8       | 20.6 ms                                                | 24.1 ms: 1.17x slower                                                    |
| Geometric mean | (ref)                                                  | 1.06x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 2.31 sec: 1.10x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 248 us: 1.13x slower                                                     |
| json_loads           | 26.5 us                                                | 30.5 us: 1.15x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 373 us: 1.21x slower                                                     |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.25x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.17x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.78 ms: 1.37x slower                                                    |
| python_startup         | 9.93 ms                                                | 15.5 ms: 1.56x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 60.0 ms: 1.20x slower                                                    |
| genshi_text     | 22.8 ms                                                | 28.1 ms: 1.23x slower                                                    |
| django_template | 34.7 ms                                                | 43.2 ms: 1.25x slower                                                    |
| mako            | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 579 ms: 1.92x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 240 ms: 1.86x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                                     |
| async_tree_none            | 464 ms                                                 | 288 ms: 1.61x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 350 ms: 1.59x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 583 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 621 ms: 1.15x faster                                                     |
| pathlib                    | 21.5 ms                                                | 18.8 ms: 1.15x faster                                                    |
| deepcopy                   | 352 us                                                 | 312 us: 1.13x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.95 ms: 1.07x faster                                                    |
| float                      | 80.8 ms                                                | 75.3 ms: 1.07x faster                                                    |
| deepcopy_memo              | 40.3 us                                                | 37.7 us: 1.07x faster                                                    |
| async_generators           | 384 ms                                                 | 370 ms: 1.04x faster                                                     |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                     |
| generators                 | 32.2 ms                                                | 31.8 ms: 1.01x faster                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.69 sec: 1.01x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                                   |
| scimark_sor                | 130 ms                                                 | 134 ms: 1.03x slower                                                     |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                    |
| dulwich_log                | 78.9 ms                                                | 82.1 ms: 1.04x slower                                                    |
| logging_silent             | 109 ns                                                 | 114 ns: 1.05x slower                                                     |
| regex_compile              | 142 ms                                                 | 150 ms: 1.05x slower                                                     |
| deepcopy_reduce            | 3.08 us                                                | 3.25 us: 1.05x slower                                                    |
| comprehensions             | 19.8 us                                                | 21.0 us: 1.06x slower                                                    |
| json                       | 5.02 ms                                                | 5.34 ms: 1.06x slower                                                    |
| docutils                   | 2.64 sec                                               | 2.82 sec: 1.07x slower                                                   |
| logging_simple             | 6.63 us                                                | 7.22 us: 1.09x slower                                                    |
| chaos                      | 62.8 ms                                                | 68.6 ms: 1.09x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.31 sec: 1.10x slower                                                   |
| pyflate                    | 448 ms                                                 | 494 ms: 1.10x slower                                                     |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.1 ms: 1.11x slower                                                    |
| raytrace                   | 299 ms                                                 | 331 ms: 1.11x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 825 ms: 1.11x slower                                                     |
| regex_dna                  | 168 ms                                                 | 186 ms: 1.11x slower                                                     |
| scimark_fft                | 342 ms                                                 | 382 ms: 1.12x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                                   |
| html5lib                   | 63.6 ms                                                | 71.3 ms: 1.12x slower                                                    |
| mdp                        | 2.42 sec                                               | 2.72 sec: 1.12x slower                                                   |
| unpickle_pure_python       | 221 us                                                 | 248 us: 1.13x slower                                                     |
| logging_format             | 7.35 us                                                | 8.30 us: 1.13x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 188 ms: 1.13x slower                                                     |
| sqlglot_normalize          | 107 ms                                                 | 121 ms: 1.14x slower                                                     |
| sqlglot_transpile          | 1.67 ms                                                | 1.91 ms: 1.14x slower                                                    |
| sqlalchemy_declarative     | 143 ms                                                 | 163 ms: 1.14x slower                                                     |
| json_loads                 | 26.5 us                                                | 30.5 us: 1.15x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 88.1 ms: 1.15x slower                                                    |
| sympy_str                  | 292 ms                                                 | 336 ms: 1.15x slower                                                     |
| sqlglot_parse              | 1.36 ms                                                | 1.57 ms: 1.16x slower                                                    |
| sqlglot_optimize           | 53.3 ms                                                | 61.7 ms: 1.16x slower                                                    |
| thrift                     | 791 us                                                 | 916 us: 1.16x slower                                                     |
| 2to3                       | 264 ms                                                 | 307 ms: 1.17x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 24.1 ms: 1.17x slower                                                    |
| sympy_expand               | 468 ms                                                 | 548 ms: 1.17x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 24.2 ms: 1.18x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 135 ms: 1.19x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 60.0 ms: 1.20x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 81.8 ms: 1.20x slower                                                    |
| nqueens                    | 80.1 ms                                                | 95.9 ms: 1.20x slower                                                    |
| pidigits                   | 184 ms                                                 | 221 ms: 1.20x slower                                                     |
| hexiom                     | 6.17 ms                                                | 7.43 ms: 1.20x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 373 us: 1.21x slower                                                     |
| richards                   | 45.9 ms                                                | 55.7 ms: 1.21x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.40 ms: 1.23x slower                                                    |
| genshi_text                | 22.8 ms                                                | 28.1 ms: 1.23x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 202 us: 1.23x slower                                                     |
| django_template            | 34.7 ms                                                | 43.2 ms: 1.25x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.25x slower                                                    |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                     |
| richards_super             | 51.9 ms                                                | 65.3 ms: 1.26x slower                                                    |
| fannkuch                   | 372 ms                                                 | 476 ms: 1.28x slower                                                     |
| telco                      | 6.53 ms                                                | 8.63 ms: 1.32x slower                                                    |
| deltablue                  | 3.45 ms                                                | 4.69 ms: 1.36x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 9.78 ms: 1.37x slower                                                    |
| coverage                   | 71.4 ms                                                | 97.9 ms: 1.37x slower                                                    |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.44x slower                                                    |
| nbody                      | 89.3 ms                                                | 135 ms: 1.51x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.71 ms: 1.56x slower                                                    |
| python_startup             | 9.93 ms                                                | 15.5 ms: 1.56x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 5.43 ms: 1.57x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 3.32 ms: 3.52x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 95.2 ms: 8.82x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.12x slower                                                             |

Benchmark hidden because not significant (3): asyncio_websockets, go, pylint
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list, xml_etree_generate, xml_etree_iterparse, xml_etree_parse, xml_etree_process
Ignored benchmarks (6) of results/bm-20250122-3.14.0a4+-1b4e8c3-NOGIL/bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.071x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x