# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 699f4e9
- commit date: 2024-12-17
- overall geometric mean: 1.040x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 256 ms: 1.02x faster                                                     |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 615 ms: 1.49x faster                                                     |
| async_tree_io              | 876 ms                                                       | 628 ms: 1.39x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 334 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.30x faster                                                     |
| async_tree_none            | 354 ms                                                       | 278 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 569 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 547 ms: 1.17x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 22.1 ms: 1.06x faster                                                    |
| async_generators           | 377 ms                                                       | 355 ms: 1.06x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 76.4 ms: 1.01x faster                                                    |
| nbody          | 85.1 ms                                                      | 89.6 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                        | 1.01x slower                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                    |
| regex_dna      | 180 ms                                                       | 165 ms: 1.09x faster                                                     |
| regex_compile  | 132 ms                                                       | 127 ms: 1.04x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 23.5 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                        | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.2 ms: 1.04x faster                                                    |
| json_loads           | 27.0 us                                                      | 26.2 us: 1.03x faster                                                    |
| xml_etree_process    | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 83.8 ms: 1.02x faster                                                    |
| tomli_loads          | 2.01 sec                                                     | 1.98 sec: 1.01x faster                                                   |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.02x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 11.3 ms: 1.07x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 320 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.52 ms: 1.02x slower                                                    |
| python_startup         | 11.0 ms                                                      | 14.7 ms: 1.33x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 21.9 ms: 1.02x slower                                                    |
| genshi_xml      | 48.8 ms                                                      | 50.0 ms: 1.02x slower                                                    |
| django_template | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 615 ms: 1.49x faster                                                     |
| deepcopy                   | 355 us                                                       | 254 us: 1.40x faster                                                     |
| async_tree_io              | 876 ms                                                       | 628 ms: 1.39x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 334 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 30.0 us: 1.30x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 258 ms: 1.30x faster                                                     |
| async_tree_none            | 354 ms                                                       | 278 ms: 1.27x faster                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 2.59 us: 1.20x faster                                                    |
| go                         | 141 ms                                                       | 119 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 569 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 547 ms: 1.17x faster                                                     |
| spectral_norm              | 111 ms                                                       | 97.2 ms: 1.14x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                    |
| pylint                     | 317 ms                                                       | 282 ms: 1.13x faster                                                     |
| scimark_fft                | 349 ms                                                       | 315 ms: 1.11x faster                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.29 ms: 1.10x faster                                                    |
| regex_dna                  | 180 ms                                                       | 165 ms: 1.09x faster                                                     |
| telco                      | 7.82 ms                                                      | 7.21 ms: 1.08x faster                                                    |
| generators                 | 28.8 ms                                                      | 26.9 ms: 1.07x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 22.1 ms: 1.06x faster                                                    |
| async_generators           | 377 ms                                                       | 355 ms: 1.06x faster                                                     |
| thrift                     | 778 us                                                       | 733 us: 1.06x faster                                                     |
| coverage                   | 83.0 ms                                                      | 78.3 ms: 1.06x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                     |
| pyflate                    | 449 ms                                                       | 425 ms: 1.05x faster                                                     |
| scimark_sor                | 134 ms                                                       | 128 ms: 1.05x faster                                                     |
| pprint_safe_repr           | 738 ms                                                       | 706 ms: 1.04x faster                                                     |
| bpe_tokeniser              | 4.45 sec                                                     | 4.27 sec: 1.04x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.2 ms: 1.04x faster                                                    |
| regex_compile              | 132 ms                                                       | 127 ms: 1.04x faster                                                     |
| pprint_pformat             | 1.50 sec                                                     | 1.45 sec: 1.03x faster                                                   |
| json_loads                 | 27.0 us                                                      | 26.2 us: 1.03x faster                                                    |
| richards_super             | 51.6 ms                                                      | 50.1 ms: 1.03x faster                                                    |
| richards                   | 45.2 ms                                                      | 43.9 ms: 1.03x faster                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.4 ms: 1.03x faster                                                    |
| json                       | 4.93 ms                                                      | 4.78 ms: 1.03x faster                                                    |
| sympy_sum                  | 156 ms                                                       | 152 ms: 1.03x faster                                                     |
| crypto_pyaes               | 67.9 ms                                                      | 66.2 ms: 1.02x faster                                                    |
| sqlglot_normalize          | 106 ms                                                       | 103 ms: 1.02x faster                                                     |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 110 ms: 1.02x faster                                                     |
| xml_etree_process          | 59.3 ms                                                      | 58.2 ms: 1.02x faster                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 83.8 ms: 1.02x faster                                                    |
| 2to3                       | 260 ms                                                       | 256 ms: 1.02x faster                                                     |
| mdp                        | 2.36 sec                                                     | 2.32 sec: 1.02x faster                                                   |
| sympy_str                  | 275 ms                                                       | 271 ms: 1.01x faster                                                     |
| float                      | 77.5 ms                                                      | 76.4 ms: 1.01x faster                                                    |
| tomli_loads                | 2.01 sec                                                     | 1.98 sec: 1.01x faster                                                   |
| logging_simple             | 6.16 us                                                      | 6.10 us: 1.01x faster                                                    |
| sqlglot_optimize           | 52.7 ms                                                      | 52.3 ms: 1.01x faster                                                    |
| hexiom                     | 5.99 ms                                                      | 5.95 ms: 1.01x faster                                                    |
| sympy_expand               | 457 ms                                                       | 454 ms: 1.01x faster                                                     |
| sympy_integrate            | 19.8 ms                                                      | 19.8 ms: 1.00x faster                                                    |
| asyncio_websockets         | 520 ms                                                       | 522 ms: 1.00x slower                                                     |
| nqueens                    | 78.6 ms                                                      | 79.0 ms: 1.01x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 75.5 ms: 1.01x slower                                                    |
| logging_format             | 6.84 us                                                      | 6.92 us: 1.01x slower                                                    |
| mako                       | 11.3 ms                                                      | 11.5 ms: 1.01x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.02x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 3.17 ms: 1.02x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 21.9 ms: 1.02x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 7.52 ms: 1.02x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 1.59 ms: 1.02x slower                                                    |
| chaos                      | 57.3 ms                                                      | 58.4 ms: 1.02x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 1.28 ms: 1.02x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 50.0 ms: 1.02x slower                                                    |
| logging_silent             | 103 ns                                                       | 105 ns: 1.03x slower                                                     |
| django_template            | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                    |
| fannkuch                   | 370 ms                                                       | 381 ms: 1.03x slower                                                     |
| raytrace                   | 253 ms                                                       | 260 ms: 1.03x slower                                                     |
| regex_v8                   | 22.7 ms                                                      | 23.5 ms: 1.03x slower                                                    |
| nbody                      | 85.1 ms                                                      | 89.6 ms: 1.05x slower                                                    |
| comprehensions             | 16.5 us                                                      | 17.5 us: 1.07x slower                                                    |
| json_dumps                 | 10.5 ms                                                      | 11.3 ms: 1.07x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 320 us: 1.09x slower                                                     |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.13x slower                                                    |
| python_startup             | 11.0 ms                                                      | 14.7 ms: 1.33x slower                                                    |
| create_gc_cycles           | 1.34 ms                                                      | 1.85 ms: 1.38x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 4.42 ms: 1.41x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 88.5 ms: 8.05x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                             |

Benchmark hidden because not significant (5): meteor_contest, sqlite_synth, pycparser, pidigits, typing_runtime_protocols
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241217-3.14.0a2+-699f4e9/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-699f4e9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.040x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.09x