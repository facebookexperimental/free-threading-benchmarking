# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 65a6ad3
- commit date: 2025-01-16
- overall geometric mean: 1.088x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                  |
| docutils       | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 615 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                  |
| async_tree_none            | 464 ms                                                 | 272 ms: 1.71x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 329 ms: 1.69x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 473 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 495 ms: 1.44x faster                                                  |
| async_generators           | 384 ms                                                 | 325 ms: 1.18x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.06x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.8 ms: 1.14x faster                                                 |
| nbody          | 89.3 ms                                                | 87.3 ms: 1.02x faster                                                 |
| pidigits       | 184 ms                                                 | 191 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                 |
| regex_compile  | 142 ms                                                 | 127 ms: 1.12x faster                                                  |
| regex_dna      | 168 ms                                                 | 177 ms: 1.06x slower                                                  |
| regex_v8       | 20.6 ms                                                | 23.4 ms: 1.13x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.90 sec: 1.11x faster                                                |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 90.4 ms: 1.07x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 215 us: 1.03x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 83.8 ms: 1.02x faster                                                 |
| pickle_pure_python   | 308 us                                                 | 313 us: 1.02x slower                                                  |
| json_loads           | 26.5 us                                                | 27.6 us: 1.04x slower                                                 |
| json_dumps           | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.48 ms: 1.04x slower                                                 |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 48.8 ms: 1.03x faster                                                 |
| django_template | 34.7 ms                                                | 36.0 ms: 1.04x slower                                                 |
| mako            | 11.0 ms                                                | 11.7 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.00x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 304 ms: 1.84x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 615 ms: 1.80x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 608 ms: 1.78x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 255 ms: 1.75x faster                                                  |
| async_tree_none            | 464 ms                                                 | 272 ms: 1.71x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 329 ms: 1.69x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 473 ms: 1.53x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 495 ms: 1.44x faster                                                  |
| deepcopy                   | 352 us                                                 | 260 us: 1.35x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.9 us: 1.35x faster                                                 |
| go                         | 139 ms                                                 | 115 ms: 1.21x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                 |
| async_generators           | 384 ms                                                 | 325 ms: 1.18x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.8 us: 1.18x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.71 ms: 1.17x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.65 us: 1.16x faster                                                 |
| spectral_norm              | 110 ms                                                 | 95.4 ms: 1.15x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 66.8 ms: 1.15x faster                                                 |
| chaos                      | 62.8 ms                                                | 54.9 ms: 1.14x faster                                                 |
| generators                 | 32.2 ms                                                | 28.2 ms: 1.14x faster                                                 |
| raytrace                   | 299 ms                                                 | 262 ms: 1.14x faster                                                  |
| float                      | 80.8 ms                                                | 70.8 ms: 1.14x faster                                                 |
| scimark_sor                | 130 ms                                                 | 114 ms: 1.13x faster                                                  |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.23 sec: 1.12x faster                                                |
| regex_compile              | 142 ms                                                 | 127 ms: 1.12x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.6 ms: 1.11x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.90 sec: 1.11x faster                                                |
| sqlalchemy_declarative     | 143 ms                                                 | 129 ms: 1.10x faster                                                  |
| scimark_fft                | 342 ms                                                 | 314 ms: 1.09x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.18 ms: 1.09x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.25 ms: 1.08x faster                                                 |
| pyflate                    | 448 ms                                                 | 415 ms: 1.08x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 63.4 ms: 1.08x faster                                                 |
| sympy_sum                  | 166 ms                                                 | 154 ms: 1.08x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.55 ms: 1.08x faster                                                 |
| richards                   | 45.9 ms                                                | 42.8 ms: 1.07x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 90.4 ms: 1.07x faster                                                 |
| genshi_text                | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                 |
| coroutines                 | 23.9 ms                                                | 22.5 ms: 1.06x faster                                                 |
| richards_super             | 51.9 ms                                                | 48.9 ms: 1.06x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.25 us: 1.06x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                |
| sympy_str                  | 292 ms                                                 | 275 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 703 ms: 1.06x faster                                                  |
| thrift                     | 791 us                                                 | 750 us: 1.06x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.85 ms: 1.06x faster                                                 |
| logging_format             | 7.35 us                                                | 6.97 us: 1.05x faster                                                 |
| meteor_contest             | 104 ms                                                 | 98.8 ms: 1.05x faster                                                 |
| logging_silent             | 109 ns                                                 | 104 ns: 1.05x faster                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.20 ms: 1.05x faster                                                 |
| typing_runtime_protocols   | 163 us                                                 | 156 us: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                |
| dulwich_log                | 78.9 ms                                                | 76.0 ms: 1.04x faster                                                 |
| 2to3                       | 264 ms                                                 | 254 ms: 1.04x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.9 ms: 1.03x faster                                                 |
| genshi_xml                 | 50.2 ms                                                | 48.8 ms: 1.03x faster                                                 |
| nqueens                    | 80.1 ms                                                | 78.0 ms: 1.03x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 215 us: 1.03x faster                                                  |
| nbody                      | 89.3 ms                                                | 87.3 ms: 1.02x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                                  |
| sympy_expand               | 468 ms                                                 | 460 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 83.8 ms: 1.02x faster                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 52.4 ms: 1.02x faster                                                 |
| sqlglot_normalize          | 107 ms                                                 | 105 ms: 1.01x faster                                                  |
| json                       | 5.02 ms                                                | 4.98 ms: 1.01x faster                                                 |
| fannkuch                   | 372 ms                                                 | 377 ms: 1.01x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 313 us: 1.02x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.49 sec: 1.03x slower                                                |
| pidigits                   | 184 ms                                                 | 191 ms: 1.04x slower                                                  |
| django_template            | 34.7 ms                                                | 36.0 ms: 1.04x slower                                                 |
| json_loads                 | 26.5 us                                                | 27.6 us: 1.04x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.48 ms: 1.04x slower                                                 |
| regex_dna                  | 168 ms                                                 | 177 ms: 1.06x slower                                                  |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.07x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.04 ms: 1.10x slower                                                 |
| coverage                   | 71.4 ms                                                | 78.8 ms: 1.10x slower                                                 |
| telco                      | 6.53 ms                                                | 7.21 ms: 1.11x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 23.4 ms: 1.13x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.38 ms: 1.27x slower                                                 |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.68x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 88.9 ms: 8.23x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                          |

Benchmark hidden because not significant (2): sqlite_synth, xml_etree_process
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250116-3.14.0a4+-65a6ad3/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.088x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.11x