# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: e517ccb
- commit date: 2024-12-02
- overall geometric mean: 1.007x slower
- HPT reliability: 96.93%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 259 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                        | 1.00x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|---------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization    | 461 ms                                                       | 409 ms: 1.13x faster                                                     |
| async_tree_none           | 354 ms                                                       | 334 ms: 1.06x faster                                                     |
| async_tree_memoization_tg | 414 ms                                                       | 392 ms: 1.06x faster                                                     |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 635 ms: 1.05x faster                                                     |
| coroutines                | 23.6 ms                                                      | 22.6 ms: 1.04x faster                                                    |
| async_tree_io             | 876 ms                                                       | 851 ms: 1.03x faster                                                     |
| async_tree_io_tg          | 913 ms                                                       | 892 ms: 1.02x faster                                                     |
| async_generators          | 377 ms                                                       | 373 ms: 1.01x faster                                                     |
| asyncio_websockets        | 520 ms                                                       | 523 ms: 1.00x slower                                                     |
| Geometric mean            | (ref)                                                        | 1.03x faster                                                             |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 216 ms: 1.00x faster                                                     |
| float          | 77.5 ms                                                      | 82.1 ms: 1.06x slower                                                    |
| nbody          | 85.1 ms                                                      | 94.9 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                        | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.82 ms: 1.09x faster                                                    |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                     |
| regex_compile  | 132 ms                                                       | 130 ms: 1.01x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                        | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 24.9 us: 1.08x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 138 ms: 1.01x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 86.7 ms: 1.01x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 61.0 ms: 1.03x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 217 us: 1.03x slower                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 98.7 ms: 1.04x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.13 sec: 1.06x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.09x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 323 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.03x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.36 ms: 1.00x faster                                                    |
| python_startup         | 11.0 ms                                                      | 14.5 ms: 1.32x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 50.2 ms: 1.03x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 22.3 ms: 1.04x slower                                                    |
| django_template | 34.1 ms                                                      | 35.7 ms: 1.04x slower                                                    |
| mako            | 11.3 ms                                                      | 12.1 ms: 1.06x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|---------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| deepcopy                  | 355 us                                                       | 263 us: 1.35x faster                                                     |
| deepcopy_memo             | 39.1 us                                                      | 31.2 us: 1.25x faster                                                    |
| deepcopy_reduce           | 3.11 us                                                      | 2.63 us: 1.18x faster                                                    |
| pylint                    | 317 ms                                                       | 271 ms: 1.17x faster                                                     |
| go                        | 141 ms                                                       | 122 ms: 1.15x faster                                                     |
| async_tree_memoization    | 461 ms                                                       | 409 ms: 1.13x faster                                                     |
| regex_effbot              | 3.08 ms                                                      | 2.82 ms: 1.09x faster                                                    |
| json                      | 4.93 ms                                                      | 4.52 ms: 1.09x faster                                                    |
| json_loads                | 27.0 us                                                      | 24.9 us: 1.08x faster                                                    |
| telco                     | 7.82 ms                                                      | 7.33 ms: 1.07x faster                                                    |
| async_tree_none           | 354 ms                                                       | 334 ms: 1.06x faster                                                     |
| async_tree_memoization_tg | 414 ms                                                       | 392 ms: 1.06x faster                                                     |
| pathlib                   | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                    |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 635 ms: 1.05x faster                                                     |
| coverage                  | 83.0 ms                                                      | 79.3 ms: 1.05x faster                                                    |
| thrift                    | 778 us                                                       | 744 us: 1.05x faster                                                     |
| coroutines                | 23.6 ms                                                      | 22.6 ms: 1.04x faster                                                    |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 4.53 ms: 1.04x faster                                                    |
| async_tree_io             | 876 ms                                                       | 851 ms: 1.03x faster                                                     |
| async_tree_io_tg          | 913 ms                                                       | 892 ms: 1.02x faster                                                     |
| scimark_fft               | 349 ms                                                       | 342 ms: 1.02x faster                                                     |
| regex_dna                 | 180 ms                                                       | 177 ms: 1.02x faster                                                     |
| regex_compile             | 132 ms                                                       | 130 ms: 1.01x faster                                                     |
| async_generators          | 377 ms                                                       | 373 ms: 1.01x faster                                                     |
| pprint_safe_repr          | 738 ms                                                       | 729 ms: 1.01x faster                                                     |
| pprint_pformat            | 1.50 sec                                                     | 1.48 sec: 1.01x faster                                                   |
| sympy_sum                 | 156 ms                                                       | 154 ms: 1.01x faster                                                     |
| meteor_contest            | 102 ms                                                       | 101 ms: 1.01x faster                                                     |
| python_startup_no_site    | 7.39 ms                                                      | 7.36 ms: 1.00x faster                                                    |
| 2to3                      | 260 ms                                                       | 259 ms: 1.00x faster                                                     |
| pidigits                  | 217 ms                                                       | 216 ms: 1.00x faster                                                     |
| asyncio_websockets        | 520 ms                                                       | 523 ms: 1.00x slower                                                     |
| scimark_sor               | 134 ms                                                       | 135 ms: 1.01x slower                                                     |
| hexiom                    | 5.99 ms                                                      | 6.04 ms: 1.01x slower                                                    |
| pyflate                   | 449 ms                                                       | 453 ms: 1.01x slower                                                     |
| scimark_monte_carlo       | 65.4 ms                                                      | 66.0 ms: 1.01x slower                                                    |
| xml_etree_parse           | 136 ms                                                       | 138 ms: 1.01x slower                                                     |
| sympy_expand              | 457 ms                                                       | 462 ms: 1.01x slower                                                     |
| pycparser                 | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                   |
| sympy_integrate           | 19.8 ms                                                      | 20.1 ms: 1.01x slower                                                    |
| nqueens                   | 78.6 ms                                                      | 79.6 ms: 1.01x slower                                                    |
| xml_etree_generate        | 85.4 ms                                                      | 86.7 ms: 1.01x slower                                                    |
| dulwich_log               | 74.8 ms                                                      | 76.1 ms: 1.02x slower                                                    |
| logging_simple            | 6.16 us                                                      | 6.28 us: 1.02x slower                                                    |
| sqlglot_normalize         | 106 ms                                                       | 108 ms: 1.02x slower                                                     |
| generators                | 28.8 ms                                                      | 29.4 ms: 1.02x slower                                                    |
| crypto_pyaes              | 67.9 ms                                                      | 69.4 ms: 1.02x slower                                                    |
| sqlglot_optimize          | 52.7 ms                                                      | 54.1 ms: 1.03x slower                                                    |
| xml_etree_process         | 59.3 ms                                                      | 61.0 ms: 1.03x slower                                                    |
| genshi_xml                | 48.8 ms                                                      | 50.2 ms: 1.03x slower                                                    |
| typing_runtime_protocols  | 155 us                                                       | 159 us: 1.03x slower                                                     |
| sqlglot_transpile         | 1.56 ms                                                      | 1.61 ms: 1.03x slower                                                    |
| chaos                     | 57.3 ms                                                      | 59.1 ms: 1.03x slower                                                    |
| unpickle_pure_python      | 210 us                                                       | 217 us: 1.03x slower                                                     |
| logging_format            | 6.84 us                                                      | 7.08 us: 1.04x slower                                                    |
| richards_super            | 51.6 ms                                                      | 53.5 ms: 1.04x slower                                                    |
| genshi_text               | 21.5 ms                                                      | 22.3 ms: 1.04x slower                                                    |
| xml_etree_iterparse       | 94.9 ms                                                      | 98.7 ms: 1.04x slower                                                    |
| fannkuch                  | 370 ms                                                       | 385 ms: 1.04x slower                                                     |
| richards                  | 45.2 ms                                                      | 47.1 ms: 1.04x slower                                                    |
| django_template           | 34.1 ms                                                      | 35.7 ms: 1.04x slower                                                    |
| sqlglot_parse             | 1.25 ms                                                      | 1.31 ms: 1.05x slower                                                    |
| spectral_norm             | 111 ms                                                       | 117 ms: 1.05x slower                                                     |
| float                     | 77.5 ms                                                      | 82.1 ms: 1.06x slower                                                    |
| raytrace                  | 253 ms                                                       | 268 ms: 1.06x slower                                                     |
| mdp                       | 2.36 sec                                                     | 2.50 sec: 1.06x slower                                                   |
| deltablue                 | 3.12 ms                                                      | 3.32 ms: 1.06x slower                                                    |
| tomli_loads               | 2.01 sec                                                     | 2.13 sec: 1.06x slower                                                   |
| mako                      | 11.3 ms                                                      | 12.1 ms: 1.06x slower                                                    |
| comprehensions            | 16.5 us                                                      | 17.6 us: 1.07x slower                                                    |
| logging_silent            | 103 ns                                                       | 110 ns: 1.07x slower                                                     |
| json_dumps                | 10.5 ms                                                      | 11.4 ms: 1.09x slower                                                    |
| regex_v8                  | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                    |
| pickle_pure_python        | 294 us                                                       | 323 us: 1.10x slower                                                     |
| bench_thread_pool         | 919 us                                                       | 1.02 ms: 1.11x slower                                                    |
| nbody                     | 85.1 ms                                                      | 94.9 ms: 1.12x slower                                                    |
| gc_traversal              | 3.14 ms                                                      | 3.94 ms: 1.26x slower                                                    |
| python_startup            | 11.0 ms                                                      | 14.5 ms: 1.32x slower                                                    |
| create_gc_cycles          | 1.34 ms                                                      | 1.93 ms: 1.45x slower                                                    |
| bench_mp_pool             | 11.0 ms                                                      | 85.8 ms: 7.80x slower                                                    |
| Geometric mean            | (ref)                                                        | 1.03x slower                                                             |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed_tg, bpe_tokeniser, docutils, sympy_str, scimark_lu, sqlite_synth, async_tree_none_tg
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241202-3.14.0a2+-e517ccb/bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 96.93% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x