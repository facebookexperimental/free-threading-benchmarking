# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_129201_gc_mark_pr
- machine: linux-x86_64
- commit hash: e12dd2e
- commit date: 2025-01-30
- overall geometric mean: 1.085x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 305 ms: 1.18x slower                                                     |
| docutils       | 2.62 sec                                                     | 2.76 sec: 1.06x slower                                                   |
| html5lib       | 67.0 ms                                                      | 68.5 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                        | 1.08x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 574 ms: 1.59x faster                                                     |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.45x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 354 ms: 1.30x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 320 ms: 1.29x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 260 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 502 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 532 ms: 1.25x faster                                                     |
| async_tree_none            | 354 ms                                                       | 288 ms: 1.23x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 23.1 ms: 1.02x faster                                                    |
| async_generators           | 377 ms                                                       | 376 ms: 1.00x faster                                                     |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 191 ms: 1.13x faster                                                     |
| float          | 77.5 ms                                                      | 75.6 ms: 1.02x faster                                                    |
| nbody          | 85.1 ms                                                      | 131 ms: 1.54x slower                                                     |
| Geometric mean | (ref)                                                        | 1.10x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.74 ms: 1.12x faster                                                    |
| regex_dna      | 180 ms                                                       | 181 ms: 1.00x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                                    |
| regex_compile  | 132 ms                                                       | 149 ms: 1.13x slower                                                     |
| Geometric mean | (ref)                                                        | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.3 ms: 1.07x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 96.3 ms: 1.13x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.29 sec: 1.14x slower                                                   |
| xml_etree_process    | 59.3 ms                                                      | 68.5 ms: 1.15x slower                                                    |
| json_loads           | 27.0 us                                                      | 31.4 us: 1.16x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 245 us: 1.17x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 12.8 ms: 1.21x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 379 us: 1.29x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.82 ms: 1.33x slower                                                    |
| python_startup         | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 59.6 ms: 1.22x slower                                                    |
| django_template | 34.1 ms                                                      | 43.1 ms: 1.26x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 27.5 ms: 1.27x slower                                                    |
| mako            | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 574 ms: 1.59x faster                                                     |
| async_tree_io              | 876 ms                                                       | 606 ms: 1.45x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 354 ms: 1.30x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 320 ms: 1.29x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 260 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 502 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 532 ms: 1.25x faster                                                     |
| async_tree_none            | 354 ms                                                       | 288 ms: 1.23x faster                                                     |
| deepcopy                   | 355 us                                                       | 312 us: 1.14x faster                                                     |
| pidigits                   | 217 ms                                                       | 191 ms: 1.13x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.74 ms: 1.12x faster                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.04 us: 1.08x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.3 ms: 1.07x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                                     |
| go                         | 141 ms                                                       | 135 ms: 1.04x faster                                                     |
| scimark_sor                | 134 ms                                                       | 130 ms: 1.03x faster                                                     |
| float                      | 77.5 ms                                                      | 75.6 ms: 1.02x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 18.7 ms: 1.02x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 23.1 ms: 1.02x faster                                                    |
| deepcopy_memo              | 39.1 us                                                      | 38.2 us: 1.02x faster                                                    |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                     |
| async_generators           | 377 ms                                                       | 376 ms: 1.00x faster                                                     |
| regex_dna                  | 180 ms                                                       | 181 ms: 1.00x slower                                                     |
| gc_traversal               | 3.14 ms                                                      | 3.19 ms: 1.02x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 3.18 us: 1.02x slower                                                    |
| html5lib                   | 67.0 ms                                                      | 68.5 ms: 1.02x slower                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.63 sec: 1.04x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.18 sec: 1.05x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.76 sec: 1.06x slower                                                   |
| scimark_fft                | 349 ms                                                       | 378 ms: 1.08x slower                                                     |
| logging_silent             | 103 ns                                                       | 112 ns: 1.09x slower                                                     |
| dulwich_log                | 74.8 ms                                                      | 82.1 ms: 1.10x slower                                                    |
| json                       | 4.93 ms                                                      | 5.42 ms: 1.10x slower                                                    |
| telco                      | 7.82 ms                                                      | 8.66 ms: 1.11x slower                                                    |
| pyflate                    | 449 ms                                                       | 502 ms: 1.12x slower                                                     |
| pprint_safe_repr           | 738 ms                                                       | 826 ms: 1.12x slower                                                     |
| mdp                        | 2.36 sec                                                     | 2.65 sec: 1.13x slower                                                   |
| regex_compile              | 132 ms                                                       | 149 ms: 1.13x slower                                                     |
| xml_etree_generate         | 85.4 ms                                                      | 96.3 ms: 1.13x slower                                                    |
| pprint_pformat             | 1.50 sec                                                     | 1.70 sec: 1.14x slower                                                   |
| sqlglot_normalize          | 106 ms                                                       | 120 ms: 1.14x slower                                                     |
| tomli_loads                | 2.01 sec                                                     | 2.29 sec: 1.14x slower                                                   |
| generators                 | 28.8 ms                                                      | 33.1 ms: 1.15x slower                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.43 ms: 1.15x slower                                                    |
| xml_etree_process          | 59.3 ms                                                      | 68.5 ms: 1.15x slower                                                    |
| thrift                     | 778 us                                                       | 901 us: 1.16x slower                                                     |
| sqlglot_optimize           | 52.7 ms                                                      | 61.0 ms: 1.16x slower                                                    |
| json_loads                 | 27.0 us                                                      | 31.4 us: 1.16x slower                                                    |
| coverage                   | 83.0 ms                                                      | 96.7 ms: 1.17x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 245 us: 1.17x slower                                                     |
| logging_simple             | 6.16 us                                                      | 7.24 us: 1.18x slower                                                    |
| 2to3                       | 260 ms                                                       | 305 ms: 1.18x slower                                                     |
| logging_format             | 6.84 us                                                      | 8.19 us: 1.20x slower                                                    |
| chaos                      | 57.3 ms                                                      | 68.6 ms: 1.20x slower                                                    |
| sympy_sum                  | 156 ms                                                       | 187 ms: 1.20x slower                                                     |
| sympy_expand               | 457 ms                                                       | 550 ms: 1.20x slower                                                     |
| json_dumps                 | 10.5 ms                                                      | 12.8 ms: 1.21x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 24.0 ms: 1.21x slower                                                    |
| comprehensions             | 16.5 us                                                      | 20.0 us: 1.21x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 1.89 ms: 1.21x slower                                                    |
| hexiom                     | 5.99 ms                                                      | 7.30 ms: 1.22x slower                                                    |
| scimark_lu                 | 113 ms                                                       | 137 ms: 1.22x slower                                                     |
| sympy_str                  | 275 ms                                                       | 335 ms: 1.22x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 59.6 ms: 1.22x slower                                                    |
| nqueens                    | 78.6 ms                                                      | 96.3 ms: 1.22x slower                                                    |
| richards                   | 45.2 ms                                                      | 55.9 ms: 1.24x slower                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 81.5 ms: 1.25x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 1.57 ms: 1.25x slower                                                    |
| django_template            | 34.1 ms                                                      | 43.1 ms: 1.26x slower                                                    |
| richards_super             | 51.6 ms                                                      | 65.6 ms: 1.27x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 27.5 ms: 1.27x slower                                                    |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                     |
| raytrace                   | 253 ms                                                       | 325 ms: 1.28x slower                                                     |
| pickle_pure_python         | 294 us                                                       | 379 us: 1.29x slower                                                     |
| create_gc_cycles           | 1.34 ms                                                      | 1.73 ms: 1.29x slower                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 87.8 ms: 1.29x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 201 us: 1.30x slower                                                     |
| fannkuch                   | 370 ms                                                       | 490 ms: 1.32x slower                                                     |
| python_startup_no_site     | 7.39 ms                                                      | 9.82 ms: 1.33x slower                                                    |
| mako                       | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                    |
| python_startup             | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 4.57 ms: 1.46x slower                                                    |
| nbody                      | 85.1 ms                                                      | 131 ms: 1.54x slower                                                     |
| bench_thread_pool          | 919 us                                                       | 3.31 ms: 3.60x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 92.6 ms: 8.43x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.13x slower                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250130-3.14.0a4+-e12dd2e-NOGIL/bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4+-e12dd2e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.085x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.34x