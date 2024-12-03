# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: e517ccb
- commit date: 2024-12-02
- overall geometric mean: 1.290x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 382 ms: 1.47x slower                                                     |
| docutils       | 2.62 sec                                                     | 3.22 sec: 1.23x slower                                                   |
| html5lib       | 67.0 ms                                                      | 101 ms: 1.50x slower                                                     |
| Geometric mean | (ref)                                                        | 1.39x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|---------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 871 ms: 1.05x faster                                                     |
| async_tree_io             | 876 ms                                                       | 898 ms: 1.03x slower                                                     |
| async_tree_memoization    | 461 ms                                                       | 495 ms: 1.07x slower                                                     |
| async_tree_none_tg        | 336 ms                                                       | 372 ms: 1.11x slower                                                     |
| async_tree_memoization_tg | 414 ms                                                       | 464 ms: 1.12x slower                                                     |
| async_tree_none           | 354 ms                                                       | 403 ms: 1.14x slower                                                     |
| coroutines                | 23.6 ms                                                      | 28.5 ms: 1.21x slower                                                    |
| async_generators          | 377 ms                                                       | 474 ms: 1.26x slower                                                     |
| Geometric mean            | (ref)                                                        | 1.08x slower                                                             |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                     |
| nbody          | 85.1 ms                                                      | 147 ms: 1.72x slower                                                     |
| float          | 77.5 ms                                                      | 143 ms: 1.85x slower                                                     |
| Geometric mean | (ref)                                                        | 1.39x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.97 ms: 1.04x faster                                                    |
| regex_dna      | 180 ms                                                       | 185 ms: 1.03x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 26.3 ms: 1.16x slower                                                    |
| regex_compile  | 132 ms                                                       | 195 ms: 1.48x slower                                                     |
| Geometric mean | (ref)                                                        | 1.14x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.04x faster                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 95.6 ms: 1.01x slower                                                    |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 103 ms: 1.21x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 14.4 ms: 1.37x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 83.6 ms: 1.41x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.92 sec: 1.46x slower                                                   |
| unpickle_pure_python | 210 us                                                       | 374 us: 1.78x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 560 us: 1.90x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.31x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                    |
| python_startup         | 11.0 ms                                                      | 17.6 ms: 1.60x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 68.1 ms: 1.40x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 34.6 ms: 1.61x slower                                                    |
| django_template | 34.1 ms                                                      | 55.4 ms: 1.62x slower                                                    |
| mako            | 11.3 ms                                                      | 20.2 ms: 1.78x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.60x slower                                                             |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|---------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                  | 217 ms                                                       | 184 ms: 1.18x faster                                                     |
| async_tree_io_tg          | 913 ms                                                       | 871 ms: 1.05x faster                                                     |
| regex_effbot              | 3.08 ms                                                      | 2.97 ms: 1.04x faster                                                    |
| xml_etree_parse           | 136 ms                                                       | 132 ms: 1.04x faster                                                     |
| deepcopy                  | 355 us                                                       | 357 us: 1.00x slower                                                     |
| xml_etree_iterparse       | 94.9 ms                                                      | 95.6 ms: 1.01x slower                                                    |
| json                      | 4.93 ms                                                      | 5.05 ms: 1.03x slower                                                    |
| async_tree_io             | 876 ms                                                       | 898 ms: 1.03x slower                                                     |
| regex_dna                 | 180 ms                                                       | 185 ms: 1.03x slower                                                     |
| json_loads                | 27.0 us                                                      | 27.9 us: 1.03x slower                                                    |
| sqlite_synth              | 2.21 us                                                      | 2.34 us: 1.06x slower                                                    |
| async_tree_memoization    | 461 ms                                                       | 495 ms: 1.07x slower                                                     |
| pathlib                   | 19.2 ms                                                      | 20.8 ms: 1.09x slower                                                    |
| async_tree_none_tg        | 336 ms                                                       | 372 ms: 1.11x slower                                                     |
| scimark_fft               | 349 ms                                                       | 389 ms: 1.11x slower                                                     |
| async_tree_memoization_tg | 414 ms                                                       | 464 ms: 1.12x slower                                                     |
| gc_traversal              | 3.14 ms                                                      | 3.53 ms: 1.12x slower                                                    |
| async_tree_none           | 354 ms                                                       | 403 ms: 1.14x slower                                                     |
| deepcopy_memo             | 39.1 us                                                      | 44.7 us: 1.14x slower                                                    |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.39 ms: 1.15x slower                                                    |
| telco                     | 7.82 ms                                                      | 9.01 ms: 1.15x slower                                                    |
| regex_v8                  | 22.7 ms                                                      | 26.3 ms: 1.16x slower                                                    |
| spectral_norm             | 111 ms                                                       | 130 ms: 1.17x slower                                                     |
| deepcopy_reduce           | 3.11 us                                                      | 3.73 us: 1.20x slower                                                    |
| coroutines                | 23.6 ms                                                      | 28.5 ms: 1.21x slower                                                    |
| xml_etree_generate        | 85.4 ms                                                      | 103 ms: 1.21x slower                                                     |
| coverage                  | 83.0 ms                                                      | 101 ms: 1.22x slower                                                     |
| docutils                  | 2.62 sec                                                     | 3.22 sec: 1.23x slower                                                   |
| pylint                    | 317 ms                                                       | 396 ms: 1.25x slower                                                     |
| bpe_tokeniser             | 4.45 sec                                                     | 5.58 sec: 1.25x slower                                                   |
| async_generators          | 377 ms                                                       | 474 ms: 1.26x slower                                                     |
| mdp                       | 2.36 sec                                                     | 3.07 sec: 1.30x slower                                                   |
| dulwich_log               | 74.8 ms                                                      | 99.5 ms: 1.33x slower                                                    |
| meteor_contest            | 102 ms                                                       | 137 ms: 1.35x slower                                                     |
| nqueens                   | 78.6 ms                                                      | 107 ms: 1.36x slower                                                     |
| json_dumps                | 10.5 ms                                                      | 14.4 ms: 1.37x slower                                                    |
| generators                | 28.8 ms                                                      | 39.5 ms: 1.37x slower                                                    |
| python_startup_no_site    | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                    |
| create_gc_cycles          | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                    |
| genshi_xml                | 48.8 ms                                                      | 68.1 ms: 1.40x slower                                                    |
| typing_runtime_protocols  | 155 us                                                       | 218 us: 1.41x slower                                                     |
| xml_etree_process         | 59.3 ms                                                      | 83.6 ms: 1.41x slower                                                    |
| sqlglot_optimize          | 52.7 ms                                                      | 75.2 ms: 1.43x slower                                                    |
| sqlglot_normalize         | 106 ms                                                       | 151 ms: 1.43x slower                                                     |
| pycparser                 | 1.12 sec                                                     | 1.61 sec: 1.44x slower                                                   |
| fannkuch                  | 370 ms                                                       | 535 ms: 1.45x slower                                                     |
| tomli_loads               | 2.01 sec                                                     | 2.92 sec: 1.46x slower                                                   |
| pprint_safe_repr          | 738 ms                                                       | 1.08 sec: 1.46x slower                                                   |
| 2to3                      | 260 ms                                                       | 382 ms: 1.47x slower                                                     |
| regex_compile             | 132 ms                                                       | 195 ms: 1.48x slower                                                     |
| pprint_pformat            | 1.50 sec                                                     | 2.23 sec: 1.49x slower                                                   |
| html5lib                  | 67.0 ms                                                      | 101 ms: 1.50x slower                                                     |
| crypto_pyaes              | 67.9 ms                                                      | 102 ms: 1.50x slower                                                     |
| thrift                    | 778 us                                                       | 1.21 ms: 1.55x slower                                                    |
| sympy_integrate           | 19.8 ms                                                      | 31.0 ms: 1.57x slower                                                    |
| python_startup            | 11.0 ms                                                      | 17.6 ms: 1.60x slower                                                    |
| genshi_text               | 21.5 ms                                                      | 34.6 ms: 1.61x slower                                                    |
| django_template           | 34.1 ms                                                      | 55.4 ms: 1.62x slower                                                    |
| pyflate                   | 449 ms                                                       | 728 ms: 1.62x slower                                                     |
| nbody                     | 85.1 ms                                                      | 147 ms: 1.72x slower                                                     |
| scimark_lu                | 113 ms                                                       | 199 ms: 1.76x slower                                                     |
| comprehensions            | 16.5 us                                                      | 29.2 us: 1.77x slower                                                    |
| unpickle_pure_python      | 210 us                                                       | 374 us: 1.78x slower                                                     |
| mako                      | 11.3 ms                                                      | 20.2 ms: 1.78x slower                                                    |
| scimark_sor               | 134 ms                                                       | 241 ms: 1.80x slower                                                     |
| sympy_str                 | 275 ms                                                       | 497 ms: 1.81x slower                                                     |
| float                     | 77.5 ms                                                      | 143 ms: 1.85x slower                                                     |
| logging_simple            | 6.16 us                                                      | 11.5 us: 1.86x slower                                                    |
| logging_format            | 6.84 us                                                      | 12.8 us: 1.87x slower                                                    |
| scimark_monte_carlo       | 65.4 ms                                                      | 123 ms: 1.88x slower                                                     |
| hexiom                    | 5.99 ms                                                      | 11.3 ms: 1.88x slower                                                    |
| logging_silent            | 103 ns                                                       | 194 ns: 1.89x slower                                                     |
| pickle_pure_python        | 294 us                                                       | 560 us: 1.90x slower                                                     |
| richards                  | 45.2 ms                                                      | 86.4 ms: 1.91x slower                                                    |
| richards_super            | 51.6 ms                                                      | 102 ms: 1.98x slower                                                     |
| sqlglot_transpile         | 1.56 ms                                                      | 3.10 ms: 1.99x slower                                                    |
| chaos                     | 57.3 ms                                                      | 115 ms: 2.00x slower                                                     |
| go                        | 141 ms                                                       | 284 ms: 2.02x slower                                                     |
| sqlglot_parse             | 1.25 ms                                                      | 2.70 ms: 2.16x slower                                                    |
| sympy_expand              | 457 ms                                                       | 992 ms: 2.17x slower                                                     |
| sympy_sum                 | 156 ms                                                       | 358 ms: 2.30x slower                                                     |
| raytrace                  | 253 ms                                                       | 607 ms: 2.40x slower                                                     |
| deltablue                 | 3.12 ms                                                      | 8.79 ms: 2.81x slower                                                    |
| bench_thread_pool         | 919 us                                                       | 3.39 ms: 3.69x slower                                                    |
| bench_mp_pool             | 11.0 ms                                                      | 110 ms: 10.04x slower                                                    |
| Geometric mean            | (ref)                                                        | 1.46x slower                                                             |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_cpu_io_mixed
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241202-3.14.0a2+-e517ccb-NOGIL/bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.290x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.31x
- 95% likely to have a slowdown of 1.29x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.31x