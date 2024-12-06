# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: b22403e
- commit date: 2024-12-05
- overall geometric mean: 1.065x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 258 ms: 1.02x faster                                                  |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 618 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 624 ms: 1.74x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.72x faster                                                  |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 338 ms: 1.64x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.44x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.3 ms: 1.07x faster                                                 |
| async_generators           | 384 ms                                                 | 368 ms: 1.05x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.7 ms: 1.03x faster                                                 |
| pidigits       | 184 ms                                                 | 185 ms: 1.00x slower                                                  |
| nbody          | 89.3 ms                                                | 94.5 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.81 ms: 1.13x faster                                                 |
| regex_compile  | 142 ms                                                 | 130 ms: 1.09x faster                                                  |
| regex_dna      | 168 ms                                                 | 168 ms: 1.00x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| json_loads           | 26.5 us                                                | 25.2 us: 1.05x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 91.9 ms: 1.05x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 216 us: 1.02x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 313 us: 1.02x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 60.0 ms: 1.02x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 86.9 ms: 1.02x slower                                                 |
| json_dumps           | 10.4 ms                                                | 11.3 ms: 1.10x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                 |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.0 ms: 1.04x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 50.5 ms: 1.01x slower                                                 |
| django_template | 34.7 ms                                                | 35.4 ms: 1.02x slower                                                 |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 618 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 624 ms: 1.74x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.72x faster                                                  |
| async_tree_none            | 464 ms                                                 | 276 ms: 1.68x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 338 ms: 1.64x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 498 ms: 1.44x faster                                                  |
| deepcopy                   | 352 us                                                 | 263 us: 1.34x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 30.9 us: 1.31x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                 |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 66.3 ms: 1.16x faster                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.0 ms: 1.14x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.81 ms: 1.13x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                 |
| raytrace                   | 299 ms                                                 | 266 ms: 1.13x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 127 ms: 1.12x faster                                                  |
| pylint                     | 319 ms                                                 | 284 ms: 1.12x faster                                                  |
| generators                 | 32.2 ms                                                | 29.0 ms: 1.11x faster                                                 |
| json                       | 5.02 ms                                                | 4.58 ms: 1.10x faster                                                 |
| regex_compile              | 142 ms                                                 | 130 ms: 1.09x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.35 sec: 1.09x faster                                                |
| logging_simple             | 6.63 us                                                | 6.15 us: 1.08x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.3 ms: 1.07x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                  |
| thrift                     | 791 us                                                 | 738 us: 1.07x faster                                                  |
| chaos                      | 62.8 ms                                                | 58.7 ms: 1.07x faster                                                 |
| sympy_str                  | 292 ms                                                 | 276 ms: 1.06x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.27 ms: 1.05x faster                                                 |
| json_loads                 | 26.5 us                                                | 25.2 us: 1.05x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 91.9 ms: 1.05x faster                                                 |
| logging_format             | 7.35 us                                                | 6.99 us: 1.05x faster                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 65.3 ms: 1.05x faster                                                 |
| async_generators           | 384 ms                                                 | 368 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.46 sec: 1.04x faster                                                |
| sqlglot_transpile          | 1.67 ms                                                | 1.61 ms: 1.04x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 75.9 ms: 1.04x faster                                                 |
| genshi_text                | 22.8 ms                                                | 22.0 ms: 1.04x faster                                                 |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 718 ms: 1.04x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.98 ms: 1.03x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                |
| float                      | 80.8 ms                                                | 78.7 ms: 1.03x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 20.1 ms: 1.02x faster                                                 |
| 2to3                       | 264 ms                                                 | 258 ms: 1.02x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 216 us: 1.02x faster                                                  |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 161 us: 1.02x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                                  |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.02x faster                                                  |
| scimark_fft                | 342 ms                                                 | 337 ms: 1.01x faster                                                  |
| sympy_expand               | 468 ms                                                 | 465 ms: 1.01x faster                                                  |
| regex_dna                  | 168 ms                                                 | 168 ms: 1.00x slower                                                  |
| pidigits                   | 184 ms                                                 | 185 ms: 1.00x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 50.5 ms: 1.01x slower                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 53.9 ms: 1.01x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 108 ms: 1.01x slower                                                  |
| nqueens                    | 80.1 ms                                                | 81.0 ms: 1.01x slower                                                 |
| richards                   | 45.9 ms                                                | 46.5 ms: 1.01x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 313 us: 1.02x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 60.0 ms: 1.02x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 86.9 ms: 1.02x slower                                                 |
| richards_super             | 51.9 ms                                                | 53.0 ms: 1.02x slower                                                 |
| django_template            | 34.7 ms                                                | 35.4 ms: 1.02x slower                                                 |
| sqlite_synth               | 2.20 us                                                | 2.25 us: 1.02x slower                                                 |
| scimark_sor                | 130 ms                                                 | 134 ms: 1.03x slower                                                  |
| fannkuch                   | 372 ms                                                 | 385 ms: 1.03x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                 |
| mdp                        | 2.42 sec                                               | 2.54 sec: 1.05x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.62 ms: 1.05x slower                                                 |
| nbody                      | 89.3 ms                                                | 94.5 ms: 1.06x slower                                                 |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.09x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.10x slower                                                 |
| coverage                   | 71.4 ms                                                | 79.5 ms: 1.11x slower                                                 |
| telco                      | 6.53 ms                                                | 7.34 ms: 1.12x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.7 ms: 1.15x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.29 ms: 1.24x slower                                                 |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.70x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 88.8 ms: 8.22x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (3): spectral_norm, tomli_loads, pyflate
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241205-3.14.0a2+-b22403e/bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.065x faster

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.11x