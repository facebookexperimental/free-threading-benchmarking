# Results vs. 3.13.0rc2

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: d6ea4f1
- commit date: 2024-12-13
- overall geometric mean: 1.222x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 365 ms: 1.41x slower                                                     |
| docutils       | 2.62 sec                                                     | 3.07 sec: 1.18x slower                                                   |
| html5lib       | 67.0 ms                                                      | 95.0 ms: 1.42x slower                                                    |
| Geometric mean | (ref)                                                        | 1.33x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 765 ms: 1.19x faster                                                     |
| async_tree_io              | 876 ms                                                       | 793 ms: 1.11x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 593 ms: 1.08x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 620 ms: 1.07x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 446 ms: 1.03x faster                                                     |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                    |
| async_tree_none            | 354 ms                                                       | 362 ms: 1.02x slower                                                     |
| async_generators           | 377 ms                                                       | 438 ms: 1.16x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                             |

Benchmark hidden because not significant (3): async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                     |
| float          | 77.5 ms                                                      | 113 ms: 1.46x slower                                                     |
| nbody          | 85.1 ms                                                      | 126 ms: 1.48x slower                                                     |
| Geometric mean | (ref)                                                        | 1.22x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                    |
| regex_dna      | 180 ms                                                       | 183 ms: 1.02x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 24.1 ms: 1.06x slower                                                    |
| regex_compile  | 132 ms                                                       | 172 ms: 1.30x slower                                                     |
| Geometric mean | (ref)                                                        | 1.06x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 90.4 ms: 1.05x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| json_loads           | 27.0 us                                                      | 28.6 us: 1.06x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 96.5 ms: 1.13x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 73.1 ms: 1.23x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.60 sec: 1.30x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 14.1 ms: 1.34x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 326 us: 1.55x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 492 us: 1.67x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.22x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                    |
| python_startup         | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 62.9 ms: 1.29x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 31.2 ms: 1.45x slower                                                    |
| django_template | 34.1 ms                                                      | 50.5 ms: 1.48x slower                                                    |
| mako            | 11.3 ms                                                      | 17.6 ms: 1.55x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.44x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 765 ms: 1.19x faster                                                     |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                     |
| async_tree_io              | 876 ms                                                       | 793 ms: 1.11x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                    |
| deepcopy                   | 355 us                                                       | 323 us: 1.10x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 593 ms: 1.08x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 620 ms: 1.07x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.4 ms: 1.05x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 446 ms: 1.03x faster                                                     |
| sqlite_synth               | 2.21 us                                                      | 2.18 us: 1.01x faster                                                    |
| deepcopy_memo              | 39.1 us                                                      | 38.8 us: 1.01x faster                                                    |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.02x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                    |
| json                       | 4.93 ms                                                      | 5.05 ms: 1.02x slower                                                    |
| async_tree_none            | 354 ms                                                       | 362 ms: 1.02x slower                                                     |
| pathlib                    | 19.2 ms                                                      | 20.1 ms: 1.05x slower                                                    |
| json_loads                 | 27.0 us                                                      | 28.6 us: 1.06x slower                                                    |
| regex_v8                   | 22.7 ms                                                      | 24.1 ms: 1.06x slower                                                    |
| spectral_norm              | 111 ms                                                       | 120 ms: 1.08x slower                                                     |
| scimark_fft                | 349 ms                                                       | 384 ms: 1.10x slower                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 3.45 us: 1.11x slower                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 4.93 sec: 1.11x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.70 ms: 1.11x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 3.52 ms: 1.12x slower                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 96.5 ms: 1.13x slower                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.39 ms: 1.15x slower                                                    |
| async_generators           | 377 ms                                                       | 438 ms: 1.16x slower                                                     |
| docutils                   | 2.62 sec                                                     | 3.07 sec: 1.18x slower                                                   |
| pylint                     | 317 ms                                                       | 376 ms: 1.19x slower                                                     |
| mdp                        | 2.36 sec                                                     | 2.89 sec: 1.23x slower                                                   |
| nqueens                    | 78.6 ms                                                      | 96.8 ms: 1.23x slower                                                    |
| xml_etree_process          | 59.3 ms                                                      | 73.1 ms: 1.23x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 92.9 ms: 1.24x slower                                                    |
| coverage                   | 83.0 ms                                                      | 104 ms: 1.25x slower                                                     |
| sqlglot_normalize          | 106 ms                                                       | 133 ms: 1.26x slower                                                     |
| pycparser                  | 1.12 sec                                                     | 1.43 sec: 1.28x slower                                                   |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                     |
| typing_runtime_protocols   | 155 us                                                       | 199 us: 1.29x slower                                                     |
| genshi_xml                 | 48.8 ms                                                      | 62.9 ms: 1.29x slower                                                    |
| sqlglot_optimize           | 52.7 ms                                                      | 68.3 ms: 1.30x slower                                                    |
| tomli_loads                | 2.01 sec                                                     | 2.60 sec: 1.30x slower                                                   |
| regex_compile              | 132 ms                                                       | 172 ms: 1.30x slower                                                     |
| pprint_safe_repr           | 738 ms                                                       | 962 ms: 1.30x slower                                                     |
| generators                 | 28.8 ms                                                      | 37.6 ms: 1.31x slower                                                    |
| thrift                     | 778 us                                                       | 1.03 ms: 1.32x slower                                                    |
| crypto_pyaes               | 67.9 ms                                                      | 90.0 ms: 1.33x slower                                                    |
| fannkuch                   | 370 ms                                                       | 492 ms: 1.33x slower                                                     |
| json_dumps                 | 10.5 ms                                                      | 14.1 ms: 1.34x slower                                                    |
| pprint_pformat             | 1.50 sec                                                     | 2.00 sec: 1.34x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.37x slower                                                    |
| python_startup_no_site     | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                    |
| 2to3                       | 260 ms                                                       | 365 ms: 1.41x slower                                                     |
| html5lib                   | 67.0 ms                                                      | 95.0 ms: 1.42x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 31.2 ms: 1.45x slower                                                    |
| richards_super             | 51.6 ms                                                      | 75.4 ms: 1.46x slower                                                    |
| float                      | 77.5 ms                                                      | 113 ms: 1.46x slower                                                     |
| richards                   | 45.2 ms                                                      | 66.8 ms: 1.48x slower                                                    |
| django_template            | 34.1 ms                                                      | 50.5 ms: 1.48x slower                                                    |
| nbody                      | 85.1 ms                                                      | 126 ms: 1.48x slower                                                     |
| sympy_integrate            | 19.8 ms                                                      | 29.5 ms: 1.49x slower                                                    |
| pyflate                    | 449 ms                                                       | 673 ms: 1.50x slower                                                     |
| mako                       | 11.3 ms                                                      | 17.6 ms: 1.55x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 326 us: 1.55x slower                                                     |
| python_startup             | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                                    |
| scimark_lu                 | 113 ms                                                       | 180 ms: 1.60x slower                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 105 ms: 1.60x slower                                                     |
| hexiom                     | 5.99 ms                                                      | 9.63 ms: 1.61x slower                                                    |
| logging_simple             | 6.16 us                                                      | 9.97 us: 1.62x slower                                                    |
| logging_format             | 6.84 us                                                      | 11.1 us: 1.62x slower                                                    |
| comprehensions             | 16.5 us                                                      | 26.8 us: 1.63x slower                                                    |
| chaos                      | 57.3 ms                                                      | 95.0 ms: 1.66x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 492 us: 1.67x slower                                                     |
| scimark_sor                | 134 ms                                                       | 230 ms: 1.71x slower                                                     |
| go                         | 141 ms                                                       | 241 ms: 1.71x slower                                                     |
| sympy_str                  | 275 ms                                                       | 474 ms: 1.72x slower                                                     |
| sqlglot_transpile          | 1.56 ms                                                      | 2.69 ms: 1.73x slower                                                    |
| logging_silent             | 103 ns                                                       | 180 ns: 1.75x slower                                                     |
| sqlglot_parse              | 1.25 ms                                                      | 2.33 ms: 1.87x slower                                                    |
| raytrace                   | 253 ms                                                       | 489 ms: 1.94x slower                                                     |
| sympy_expand               | 457 ms                                                       | 952 ms: 2.08x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 348 ms: 2.24x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 7.35 ms: 2.35x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 3.41 ms: 3.72x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 108 ms: 9.83x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.33x slower                                                             |

Benchmark hidden because not significant (3): async_tree_none_tg, asyncio_websockets, async_tree_memoization_tg
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-d6ea4f1-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.222x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.22x
- 95% likely to have a slowdown of 1.20x
- 99% likely to have a slowdown of 1.17x

# Memory
- memory change: 1.32x