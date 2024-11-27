# Results vs. 3.12.6

- fork: corona10
- ref: gh_115999_binary_sub
- machine: linux-x86_64
- commit hash: 6e2f5fe
- commit date: 2024-11-28
- overall geometric mean: 1.036x faster
- HPT reliability: 99.89%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 257 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 391 ms: 1.43x faster                                                     |
| async_tree_none            | 464 ms                                                 | 335 ms: 1.39x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 411 ms: 1.35x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 348 ms: 1.28x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 876 ms: 1.27x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 864 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 666 ms: 1.08x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 668 ms: 1.07x faster                                                     |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.19x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 89.3 ms                                                | 95.4 ms: 1.07x slower                                                    |
| pidigits       | 184 ms                                                 | 223 ms: 1.21x slower                                                     |
| Geometric mean | (ref)                                                  | 1.09x slower                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                    |
| regex_compile  | 142 ms                                                 | 130 ms: 1.09x faster                                                     |
| regex_dna      | 168 ms                                                 | 174 ms: 1.03x slower                                                     |
| regex_v8       | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                  | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 26.5 us                                                | 25.0 us: 1.06x faster                                                    |
| unpickle_pure_python | 221 us                                                 | 215 us: 1.03x faster                                                     |
| tomli_loads          | 2.11 sec                                               | 2.12 sec: 1.01x slower                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 97.7 ms: 1.01x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 60.2 ms: 1.02x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 318 us: 1.03x slower                                                     |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.43 ms: 1.04x slower                                                    |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.2 ms: 1.03x faster                                                    |
| genshi_xml      | 50.2 ms                                                | 50.8 ms: 1.01x slower                                                    |
| django_template | 34.7 ms                                                | 35.6 ms: 1.03x slower                                                    |
| mako            | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 391 ms: 1.43x faster                                                     |
| async_tree_none            | 464 ms                                                 | 335 ms: 1.39x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 411 ms: 1.35x faster                                                     |
| deepcopy                   | 352 us                                                 | 261 us: 1.35x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 30.2 us: 1.34x faster                                                    |
| async_tree_none_tg         | 446 ms                                                 | 348 ms: 1.28x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 876 ms: 1.27x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 864 ms: 1.25x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.66 ms: 1.19x faster                                                    |
| pylint                     | 319 ms                                                 | 270 ms: 1.18x faster                                                     |
| pathlib                    | 21.5 ms                                                | 18.3 ms: 1.17x faster                                                    |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                     |
| deepcopy_reduce            | 3.08 us                                                | 2.68 us: 1.15x faster                                                    |
| comprehensions             | 19.8 us                                                | 17.3 us: 1.14x faster                                                    |
| raytrace                   | 299 ms                                                 | 265 ms: 1.13x faster                                                     |
| sqlalchemy_declarative     | 143 ms                                                 | 127 ms: 1.12x faster                                                     |
| crypto_pyaes               | 76.6 ms                                                | 68.5 ms: 1.12x faster                                                    |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.6 ms: 1.11x faster                                                    |
| generators                 | 32.2 ms                                                | 29.1 ms: 1.11x faster                                                    |
| json                       | 5.02 ms                                                | 4.56 ms: 1.10x faster                                                    |
| regex_compile              | 142 ms                                                 | 130 ms: 1.09x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 666 ms: 1.08x faster                                                     |
| coroutines                 | 23.9 ms                                                | 22.1 ms: 1.08x faster                                                    |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                     |
| logging_simple             | 6.63 us                                                | 6.19 us: 1.07x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 668 ms: 1.07x faster                                                     |
| thrift                     | 791 us                                                 | 741 us: 1.07x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.45 sec: 1.06x faster                                                   |
| logging_format             | 7.35 us                                                | 6.92 us: 1.06x faster                                                    |
| json_loads                 | 26.5 us                                                | 25.0 us: 1.06x faster                                                    |
| sympy_str                  | 292 ms                                                 | 275 ms: 1.06x faster                                                     |
| deltablue                  | 3.45 ms                                                | 3.26 ms: 1.06x faster                                                    |
| chaos                      | 62.8 ms                                                | 59.5 ms: 1.06x faster                                                    |
| sqlglot_transpile          | 1.67 ms                                                | 1.60 ms: 1.04x faster                                                    |
| sqlglot_parse              | 1.36 ms                                                | 1.30 ms: 1.04x faster                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.46 sec: 1.04x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                   |
| meteor_contest             | 104 ms                                                 | 100 ms: 1.03x faster                                                     |
| pprint_safe_repr           | 743 ms                                                 | 719 ms: 1.03x faster                                                     |
| sympy_integrate            | 20.5 ms                                                | 19.9 ms: 1.03x faster                                                    |
| dulwich_log                | 78.9 ms                                                | 76.4 ms: 1.03x faster                                                    |
| mdp                        | 2.42 sec                                               | 2.34 sec: 1.03x faster                                                   |
| async_generators           | 384 ms                                                 | 373 ms: 1.03x faster                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 66.4 ms: 1.03x faster                                                    |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.03x faster                                                     |
| hexiom                     | 6.17 ms                                                | 5.99 ms: 1.03x faster                                                    |
| genshi_text                | 22.8 ms                                                | 22.2 ms: 1.03x faster                                                    |
| unpickle_pure_python       | 221 us                                                 | 215 us: 1.03x faster                                                     |
| 2to3                       | 264 ms                                                 | 257 ms: 1.02x faster                                                     |
| nqueens                    | 80.1 ms                                                | 78.7 ms: 1.02x faster                                                    |
| scimark_fft                | 342 ms                                                 | 338 ms: 1.01x faster                                                     |
| sqlglot_normalize          | 107 ms                                                 | 107 ms: 1.00x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 115 ms: 1.01x slower                                                     |
| tomli_loads                | 2.11 sec                                               | 2.12 sec: 1.01x slower                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 53.6 ms: 1.01x slower                                                    |
| richards_super             | 51.9 ms                                                | 52.4 ms: 1.01x slower                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 97.7 ms: 1.01x slower                                                    |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                     |
| genshi_xml                 | 50.2 ms                                                | 50.8 ms: 1.01x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 60.2 ms: 1.02x slower                                                    |
| django_template            | 34.7 ms                                                | 35.6 ms: 1.03x slower                                                    |
| spectral_norm              | 110 ms                                                 | 114 ms: 1.03x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.53 ms: 1.03x slower                                                    |
| pickle_pure_python         | 308 us                                                 | 318 us: 1.03x slower                                                     |
| regex_dna                  | 168 ms                                                 | 174 ms: 1.03x slower                                                     |
| scimark_sor                | 130 ms                                                 | 135 ms: 1.04x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 7.43 ms: 1.04x slower                                                    |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.04x slower                                                    |
| fannkuch                   | 372 ms                                                 | 391 ms: 1.05x slower                                                     |
| nbody                      | 89.3 ms                                                | 95.4 ms: 1.07x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                    |
| telco                      | 6.53 ms                                                | 7.18 ms: 1.10x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                    |
| regex_v8                   | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                    |
| coverage                   | 71.4 ms                                                | 81.0 ms: 1.13x slower                                                    |
| gc_traversal               | 3.46 ms                                                | 3.96 ms: 1.14x slower                                                    |
| pidigits                   | 184 ms                                                 | 223 ms: 1.21x slower                                                     |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.96 ms: 1.80x slower                                                    |
| bench_mp_pool              | 10.8 ms                                                | 85.9 ms: 7.96x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (9): logging_silent, sympy_expand, richards, xml_etree_parse, xml_etree_generate, docutils, sqlite_synth, float, pyflate
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241128-3.14.0a2+-6e2f5fe/bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.036x faster

# HPT report

- Reliability score: 99.89% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x