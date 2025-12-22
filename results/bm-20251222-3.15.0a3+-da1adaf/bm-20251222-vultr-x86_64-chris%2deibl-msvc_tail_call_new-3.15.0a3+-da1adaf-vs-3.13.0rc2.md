# Results vs. 3.13.0rc2

- fork: chris-eibl
- ref: msvc_tail_call_new
- machine: linux-x86_64
- commit hash: da1adaf
- commit date: 2025-12-22
- overall geometric mean: 1.036x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 247 ms: 1.05x faster                                                       |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                     |
| html5lib       | 67.0 ms                                                      | 59.4 ms: 1.13x faster                                                      |
| Geometric mean | (ref)                                                        | 1.07x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 551 ms: 1.59x faster                                                       |
| async_tree_io_tg           | 913 ms                                                       | 585 ms: 1.56x faster                                                       |
| async_tree_memoization     | 461 ms                                                       | 302 ms: 1.53x faster                                                       |
| async_tree_none            | 354 ms                                                       | 244 ms: 1.45x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.38x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 482 ms: 1.38x faster                                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 478 ms: 1.33x faster                                                       |
| async_generators           | 377 ms                                                       | 343 ms: 1.10x faster                                                       |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                               |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 71.0 ms: 1.09x faster                                                      |
| pidigits       | 217 ms                                                       | 205 ms: 1.06x faster                                                       |
| nbody          | 85.1 ms                                                      | 91.8 ms: 1.08x slower                                                      |
| Geometric mean | (ref)                                                        | 1.02x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.82 ms: 1.09x faster                                                      |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                       |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                       |
| regex_v8       | 22.7 ms                                                      | 23.0 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                        | 1.04x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|---------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| xml_etree_iterparse | 94.9 ms                                                      | 84.2 ms: 1.13x faster                                                      |
| json_dumps          | 10.5 ms                                                      | 10.0 ms: 1.05x faster                                                      |
| xml_etree_parse     | 136 ms                                                       | 131 ms: 1.04x faster                                                       |
| xml_etree_process   | 59.3 ms                                                      | 57.1 ms: 1.04x faster                                                      |
| xml_etree_generate  | 85.4 ms                                                      | 82.2 ms: 1.04x faster                                                      |
| json_loads          | 27.0 us                                                      | 27.7 us: 1.02x slower                                                      |
| pickle_pure_python  | 294 us                                                       | 307 us: 1.04x slower                                                       |
| tomli_loads         | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                     |
| Geometric mean      | (ref)                                                        | 1.02x faster                                                               |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.23 ms: 1.02x faster                                                      |
| python_startup         | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 49.3 ms: 1.01x slower                                                      |
| django_template | 34.1 ms                                                      | 35.2 ms: 1.03x slower                                                      |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                      |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                               |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.04x faster                                                     |
| async_tree_io              | 876 ms                                                       | 551 ms: 1.59x faster                                                       |
| async_tree_io_tg           | 913 ms                                                       | 585 ms: 1.56x faster                                                       |
| async_tree_memoization     | 461 ms                                                       | 302 ms: 1.53x faster                                                       |
| deepcopy_memo              | 39.1 us                                                      | 25.9 us: 1.51x faster                                                      |
| async_tree_none            | 354 ms                                                       | 244 ms: 1.45x faster                                                       |
| deepcopy                   | 355 us                                                       | 246 us: 1.45x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 243 ms: 1.38x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 482 ms: 1.38x faster                                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 305 ms: 1.36x faster                                                       |
| go                         | 141 ms                                                       | 105 ms: 1.34x faster                                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 478 ms: 1.33x faster                                                       |
| scimark_sor                | 134 ms                                                       | 107 ms: 1.26x faster                                                       |
| deepcopy_reduce            | 3.11 us                                                      | 2.65 us: 1.17x faster                                                      |
| spectral_norm              | 111 ms                                                       | 96.7 ms: 1.15x faster                                                      |
| scimark_fft                | 349 ms                                                       | 306 ms: 1.14x faster                                                       |
| html5lib                   | 67.0 ms                                                      | 59.4 ms: 1.13x faster                                                      |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.2 ms: 1.13x faster                                                      |
| pylint                     | 317 ms                                                       | 284 ms: 1.12x faster                                                       |
| pathlib                    | 19.2 ms                                                      | 17.4 ms: 1.10x faster                                                      |
| async_generators           | 377 ms                                                       | 343 ms: 1.10x faster                                                       |
| pyflate                    | 449 ms                                                       | 409 ms: 1.10x faster                                                       |
| regex_effbot               | 3.08 ms                                                      | 2.82 ms: 1.09x faster                                                      |
| float                      | 77.5 ms                                                      | 71.0 ms: 1.09x faster                                                      |
| dulwich_log                | 74.8 ms                                                      | 69.0 ms: 1.09x faster                                                      |
| richards                   | 45.2 ms                                                      | 42.1 ms: 1.07x faster                                                      |
| richards_super             | 51.6 ms                                                      | 48.2 ms: 1.07x faster                                                      |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                       |
| bpe_tokeniser              | 4.45 sec                                                     | 4.18 sec: 1.06x faster                                                     |
| scimark_lu                 | 113 ms                                                       | 106 ms: 1.06x faster                                                       |
| pprint_safe_repr           | 738 ms                                                       | 695 ms: 1.06x faster                                                       |
| pidigits                   | 217 ms                                                       | 205 ms: 1.06x faster                                                       |
| pprint_pformat             | 1.50 sec                                                     | 1.42 sec: 1.06x faster                                                     |
| 2to3                       | 260 ms                                                       | 247 ms: 1.05x faster                                                       |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.1 ms: 1.05x faster                                                      |
| json_dumps                 | 10.5 ms                                                      | 10.0 ms: 1.05x faster                                                      |
| hexiom                     | 5.99 ms                                                      | 5.72 ms: 1.05x faster                                                      |
| sympy_integrate            | 19.8 ms                                                      | 18.9 ms: 1.05x faster                                                      |
| logging_simple             | 6.16 us                                                      | 5.88 us: 1.05x faster                                                      |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                       |
| xml_etree_process          | 59.3 ms                                                      | 57.1 ms: 1.04x faster                                                      |
| xml_etree_generate         | 85.4 ms                                                      | 82.2 ms: 1.04x faster                                                      |
| logging_format             | 6.84 us                                                      | 6.64 us: 1.03x faster                                                      |
| generators                 | 28.8 ms                                                      | 28.1 ms: 1.03x faster                                                      |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                      |
| chaos                      | 57.3 ms                                                      | 56.0 ms: 1.02x faster                                                      |
| python_startup_no_site     | 7.39 ms                                                      | 7.23 ms: 1.02x faster                                                      |
| thrift                     | 778 us                                                       | 762 us: 1.02x faster                                                       |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.61 ms: 1.02x faster                                                      |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                                       |
| coverage                   | 83.0 ms                                                      | 82.0 ms: 1.01x faster                                                      |
| sympy_sum                  | 156 ms                                                       | 155 ms: 1.01x faster                                                       |
| raytrace                   | 253 ms                                                       | 255 ms: 1.01x slower                                                       |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 49.3 ms: 1.01x slower                                                      |
| regex_v8                   | 22.7 ms                                                      | 23.0 ms: 1.01x slower                                                      |
| logging_silent             | 103 ns                                                       | 104 ns: 1.02x slower                                                       |
| typing_runtime_protocols   | 155 us                                                       | 158 us: 1.02x slower                                                       |
| json                       | 4.93 ms                                                      | 5.04 ms: 1.02x slower                                                      |
| crypto_pyaes               | 67.9 ms                                                      | 69.4 ms: 1.02x slower                                                      |
| json_loads                 | 27.0 us                                                      | 27.7 us: 1.02x slower                                                      |
| sqlite_synth               | 2.21 us                                                      | 2.27 us: 1.03x slower                                                      |
| django_template            | 34.1 ms                                                      | 35.2 ms: 1.03x slower                                                      |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                      |
| fannkuch                   | 370 ms                                                       | 385 ms: 1.04x slower                                                       |
| pickle_pure_python         | 294 us                                                       | 307 us: 1.04x slower                                                       |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                       |
| tomli_loads                | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                     |
| sympy_expand               | 457 ms                                                       | 489 ms: 1.07x slower                                                       |
| deltablue                  | 3.12 ms                                                      | 3.34 ms: 1.07x slower                                                      |
| nbody                      | 85.1 ms                                                      | 91.8 ms: 1.08x slower                                                      |
| python_startup             | 11.0 ms                                                      | 12.4 ms: 1.13x slower                                                      |
| bench_thread_pool          | 919 us                                                       | 1.31 ms: 1.42x slower                                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.91 ms: 1.43x slower                                                      |
| gc_traversal               | 3.14 ms                                                      | 4.50 ms: 1.43x slower                                                      |
| telco                      | 7.82 ms                                                      | 158 ms: 20.24x slower                                                      |
| bench_mp_pool              | 11.0 ms                                                      | 373 ms: 33.96x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                               |

Benchmark hidden because not significant (6): coroutines, nqueens, meteor_contest, sympy_str, unpickle_pure_python, genshi_text
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251222-3.15.0a3+-da1adaf/bm-20251222-vultr-x86_64-chris%2deibl-msvc_tail_call_new-3.15.0a3+-da1adaf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.15x