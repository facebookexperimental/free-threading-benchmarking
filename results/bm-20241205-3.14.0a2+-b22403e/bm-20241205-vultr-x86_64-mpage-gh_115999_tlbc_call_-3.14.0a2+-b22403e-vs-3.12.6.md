# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: b22403e
- commit date: 2024-12-05
- overall geometric mean: 1.068x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 258 ms: 1.02x faster                                                  |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 624 ms: 1.78x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.78x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 624 ms: 1.73x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.71x faster                                                  |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.69x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 339 ms: 1.64x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 501 ms: 1.43x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.07x faster                                                 |
| async_generators           | 384 ms                                                 | 364 ms: 1.06x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.45x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 77.8 ms: 1.04x faster                                                 |
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                  |
| nbody          | 89.3 ms                                                | 93.9 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.79 ms: 1.13x faster                                                 |
| regex_compile  | 142 ms                                                 | 129 ms: 1.10x faster                                                  |
| regex_dna      | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| regex_v8       | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                 |
| Geometric mean | (ref)                                                  | 1.00x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 91.7 ms: 1.06x faster                                                 |
| json_loads           | 26.5 us                                                | 25.3 us: 1.05x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 214 us: 1.03x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                |
| xml_etree_generate   | 85.2 ms                                                | 84.9 ms: 1.00x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 314 us: 1.02x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.45 ms: 1.04x slower                                                 |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.0 ms: 1.04x faster                                                 |
| django_template | 34.7 ms                                                | 36.0 ms: 1.04x slower                                                 |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 624 ms: 1.78x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 315 ms: 1.78x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 624 ms: 1.73x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 260 ms: 1.71x faster                                                  |
| async_tree_none            | 464 ms                                                 | 274 ms: 1.69x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 339 ms: 1.64x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 488 ms: 1.48x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 501 ms: 1.43x faster                                                  |
| deepcopy                   | 352 us                                                 | 261 us: 1.35x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.9 us: 1.35x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.59 us: 1.19x faster                                                 |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                 |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.0 ms: 1.15x faster                                                 |
| raytrace                   | 299 ms                                                 | 263 ms: 1.14x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.4 us: 1.14x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 67.6 ms: 1.13x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.79 ms: 1.13x faster                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 126 ms: 1.13x faster                                                  |
| generators                 | 32.2 ms                                                | 28.6 ms: 1.13x faster                                                 |
| pylint                     | 319 ms                                                 | 285 ms: 1.12x faster                                                  |
| regex_compile              | 142 ms                                                 | 129 ms: 1.10x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.33 sec: 1.09x faster                                                |
| json                       | 5.02 ms                                                | 4.59 ms: 1.09x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.16 us: 1.08x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 63.9 ms: 1.07x faster                                                 |
| chaos                      | 62.8 ms                                                | 58.8 ms: 1.07x faster                                                 |
| deltablue                  | 3.45 ms                                                | 3.22 ms: 1.07x faster                                                 |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| sympy_str                  | 292 ms                                                 | 274 ms: 1.06x faster                                                  |
| logging_format             | 7.35 us                                                | 6.92 us: 1.06x faster                                                 |
| async_generators           | 384 ms                                                 | 364 ms: 1.06x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 91.7 ms: 1.06x faster                                                 |
| thrift                     | 791 us                                                 | 751 us: 1.05x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.86 ms: 1.05x faster                                                 |
| json_loads                 | 26.5 us                                                | 25.3 us: 1.05x faster                                                 |
| meteor_contest             | 104 ms                                                 | 99.2 ms: 1.04x faster                                                 |
| sqlglot_parse              | 1.36 ms                                                | 1.30 ms: 1.04x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 75.7 ms: 1.04x faster                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 1.61 ms: 1.04x faster                                                 |
| float                      | 80.8 ms                                                | 77.8 ms: 1.04x faster                                                 |
| genshi_text                | 22.8 ms                                                | 22.0 ms: 1.04x faster                                                 |
| logging_silent             | 109 ns                                                 | 105 ns: 1.04x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 718 ms: 1.03x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                |
| sympy_integrate            | 20.5 ms                                                | 19.9 ms: 1.03x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 214 us: 1.03x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.47 sec: 1.03x faster                                                |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                  |
| 2to3                       | 264 ms                                                 | 258 ms: 1.02x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 160 us: 1.02x faster                                                  |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.02x faster                                                |
| sympy_expand               | 468 ms                                                 | 460 ms: 1.02x faster                                                  |
| scimark_fft                | 342 ms                                                 | 338 ms: 1.01x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                |
| nqueens                    | 80.1 ms                                                | 79.6 ms: 1.01x faster                                                 |
| xml_etree_generate         | 85.2 ms                                                | 84.9 ms: 1.00x faster                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 53.8 ms: 1.01x slower                                                 |
| sqlglot_normalize          | 107 ms                                                 | 108 ms: 1.01x slower                                                  |
| pidigits                   | 184 ms                                                 | 186 ms: 1.01x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                                 |
| pickle_pure_python         | 308 us                                                 | 314 us: 1.02x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.47 sec: 1.02x slower                                                |
| scimark_sor                | 130 ms                                                 | 133 ms: 1.03x slower                                                  |
| django_template            | 34.7 ms                                                | 36.0 ms: 1.04x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.57 ms: 1.04x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.45 ms: 1.04x slower                                                 |
| regex_dna                  | 168 ms                                                 | 176 ms: 1.05x slower                                                  |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                 |
| nbody                      | 89.3 ms                                                | 93.9 ms: 1.05x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.02 ms: 1.09x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.4 ms: 1.11x slower                                                 |
| telco                      | 6.53 ms                                                | 7.27 ms: 1.11x slower                                                 |
| coverage                   | 71.4 ms                                                | 79.9 ms: 1.12x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 24.7 ms: 1.20x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.42 ms: 1.28x slower                                                 |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.85 ms: 1.69x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 88.5 ms: 8.19x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (6): pyflate, fannkuch, richards, xml_etree_process, richards_super, genshi_xml
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241205-3.14.0a2+-b22403e/bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.068x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.10x