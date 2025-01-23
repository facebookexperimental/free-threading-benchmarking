# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_129201_gc_mark_pr
- machine: linux-x86_64
- commit hash: 1b4e8c3
- commit date: 2025-01-22
- overall geometric mean: 1.102x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 307 ms: 1.18x slower                                                     |
| docutils       | 2.62 sec                                                     | 2.82 sec: 1.08x slower                                                   |
| html5lib       | 67.0 ms                                                      | 71.3 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                        | 1.11x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 579 ms: 1.58x faster                                                     |
| async_tree_io              | 876 ms                                                       | 608 ms: 1.44x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 240 ms: 1.40x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                     |
| async_tree_none            | 354 ms                                                       | 288 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 583 ms: 1.09x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 621 ms: 1.07x faster                                                     |
| async_generators           | 377 ms                                                       | 370 ms: 1.02x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 75.3 ms: 1.03x faster                                                    |
| pidigits       | 217 ms                                                       | 221 ms: 1.02x slower                                                     |
| nbody          | 85.1 ms                                                      | 135 ms: 1.58x slower                                                     |
| Geometric mean | (ref)                                                        | 1.16x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.95 ms: 1.05x faster                                                    |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 24.1 ms: 1.06x slower                                                    |
| regex_compile  | 132 ms                                                       | 150 ms: 1.13x slower                                                     |
| Geometric mean | (ref)                                                        | 1.04x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 30.5 us: 1.13x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.31 sec: 1.15x slower                                                   |
| unpickle_pure_python | 210 us                                                       | 248 us: 1.18x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 13.0 ms: 1.23x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 373 us: 1.27x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.19x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.78 ms: 1.32x slower                                                    |
| python_startup         | 11.0 ms                                                      | 15.5 ms: 1.41x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 60.0 ms: 1.23x slower                                                    |
| django_template | 34.1 ms                                                      | 43.2 ms: 1.27x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 28.1 ms: 1.31x slower                                                    |
| mako            | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 579 ms: 1.58x faster                                                     |
| async_tree_io              | 876 ms                                                       | 608 ms: 1.44x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 240 ms: 1.40x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                     |
| async_tree_none            | 354 ms                                                       | 288 ms: 1.23x faster                                                     |
| deepcopy                   | 355 us                                                       | 312 us: 1.14x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 583 ms: 1.09x faster                                                     |
| sqlite_synth               | 2.21 us                                                      | 2.04 us: 1.08x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 621 ms: 1.07x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.95 ms: 1.05x faster                                                    |
| deepcopy_memo              | 39.1 us                                                      | 37.7 us: 1.04x faster                                                    |
| spectral_norm              | 111 ms                                                       | 108 ms: 1.03x faster                                                     |
| float                      | 77.5 ms                                                      | 75.3 ms: 1.03x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 18.8 ms: 1.02x faster                                                    |
| async_generators           | 377 ms                                                       | 370 ms: 1.02x faster                                                     |
| go                         | 141 ms                                                       | 139 ms: 1.01x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                                     |
| scimark_sor                | 134 ms                                                       | 134 ms: 1.01x faster                                                     |
| pidigits                   | 217 ms                                                       | 221 ms: 1.02x slower                                                     |
| regex_dna                  | 180 ms                                                       | 186 ms: 1.03x slower                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 3.25 us: 1.04x slower                                                    |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.69 sec: 1.06x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.18 sec: 1.06x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 24.1 ms: 1.06x slower                                                    |
| html5lib                   | 67.0 ms                                                      | 71.3 ms: 1.06x slower                                                    |
| docutils                   | 2.62 sec                                                     | 2.82 sec: 1.08x slower                                                   |
| json                       | 4.93 ms                                                      | 5.34 ms: 1.08x slower                                                    |
| scimark_fft                | 349 ms                                                       | 382 ms: 1.09x slower                                                     |
| dulwich_log                | 74.8 ms                                                      | 82.1 ms: 1.10x slower                                                    |
| pyflate                    | 449 ms                                                       | 494 ms: 1.10x slower                                                     |
| telco                      | 7.82 ms                                                      | 8.63 ms: 1.10x slower                                                    |
| generators                 | 28.8 ms                                                      | 31.8 ms: 1.10x slower                                                    |
| logging_silent             | 103 ns                                                       | 114 ns: 1.11x slower                                                     |
| pprint_safe_repr           | 738 ms                                                       | 825 ms: 1.12x slower                                                     |
| json_loads                 | 27.0 us                                                      | 30.5 us: 1.13x slower                                                    |
| regex_compile              | 132 ms                                                       | 150 ms: 1.13x slower                                                     |
| pprint_pformat             | 1.50 sec                                                     | 1.70 sec: 1.14x slower                                                   |
| sqlglot_normalize          | 106 ms                                                       | 121 ms: 1.15x slower                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.40 ms: 1.15x slower                                                    |
| tomli_loads                | 2.01 sec                                                     | 2.31 sec: 1.15x slower                                                   |
| mdp                        | 2.36 sec                                                     | 2.72 sec: 1.15x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 61.7 ms: 1.17x slower                                                    |
| logging_simple             | 6.16 us                                                      | 7.22 us: 1.17x slower                                                    |
| thrift                     | 778 us                                                       | 916 us: 1.18x slower                                                     |
| coverage                   | 83.0 ms                                                      | 97.9 ms: 1.18x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 248 us: 1.18x slower                                                     |
| 2to3                       | 260 ms                                                       | 307 ms: 1.18x slower                                                     |
| chaos                      | 57.3 ms                                                      | 68.6 ms: 1.20x slower                                                    |
| sympy_expand               | 457 ms                                                       | 548 ms: 1.20x slower                                                     |
| scimark_lu                 | 113 ms                                                       | 135 ms: 1.20x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 188 ms: 1.21x slower                                                     |
| logging_format             | 6.84 us                                                      | 8.30 us: 1.21x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 95.9 ms: 1.22x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 24.2 ms: 1.22x slower                                                    |
| sympy_str                  | 275 ms                                                       | 336 ms: 1.22x slower                                                     |
| sqlglot_transpile          | 1.56 ms                                                      | 1.91 ms: 1.23x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 60.0 ms: 1.23x slower                                                    |
| json_dumps                 | 10.5 ms                                                      | 13.0 ms: 1.23x slower                                                    |
| richards                   | 45.2 ms                                                      | 55.7 ms: 1.23x slower                                                    |
| hexiom                     | 5.99 ms                                                      | 7.43 ms: 1.24x slower                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 81.8 ms: 1.25x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 1.57 ms: 1.25x slower                                                    |
| richards_super             | 51.6 ms                                                      | 65.3 ms: 1.26x slower                                                    |
| django_template            | 34.1 ms                                                      | 43.2 ms: 1.27x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 373 us: 1.27x slower                                                     |
| create_gc_cycles           | 1.34 ms                                                      | 1.71 ms: 1.28x slower                                                    |
| comprehensions             | 16.5 us                                                      | 21.0 us: 1.28x slower                                                    |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                     |
| fannkuch                   | 370 ms                                                       | 476 ms: 1.29x slower                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 88.1 ms: 1.30x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 202 us: 1.30x slower                                                     |
| genshi_text                | 21.5 ms                                                      | 28.1 ms: 1.31x slower                                                    |
| raytrace                   | 253 ms                                                       | 331 ms: 1.31x slower                                                     |
| python_startup_no_site     | 7.39 ms                                                      | 9.78 ms: 1.32x slower                                                    |
| mako                       | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                    |
| python_startup             | 11.0 ms                                                      | 15.5 ms: 1.41x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 4.69 ms: 1.50x slower                                                    |
| nbody                      | 85.1 ms                                                      | 135 ms: 1.58x slower                                                     |
| gc_traversal               | 3.14 ms                                                      | 5.43 ms: 1.73x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 3.32 ms: 3.61x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 95.2 ms: 8.66x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.16x slower                                                             |

Benchmark hidden because not significant (1): pylint
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list, xml_etree_generate, xml_etree_iterparse, xml_etree_parse, xml_etree_process
Ignored benchmarks (8) of results/bm-20250122-3.14.0a4+-1b4e8c3-NOGIL/bm-20250122-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-1b4e8c3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.102x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.32x