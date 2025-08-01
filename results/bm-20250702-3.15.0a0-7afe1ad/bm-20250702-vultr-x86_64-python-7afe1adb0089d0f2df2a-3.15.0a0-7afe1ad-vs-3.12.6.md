# Results vs. 3.12.6

- fork: python
- ref: 7afe1adb0089d0f2df2a
- machine: linux-x86_64
- commit hash: 7afe1ad
- commit date: 2025-07-02
- overall geometric mean: 1.071x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                |
| html5lib       | 63.6 ms                                                | 60.9 ms: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 256 ms: 1.82x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 599 ms: 1.81x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 617 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.77x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 315 ms: 1.76x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 510 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 505 ms: 1.42x faster                                                  |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.05x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.4 ms: 1.12x faster                                                 |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.57 ms: 1.23x faster                                                 |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| regex_dna      | 168 ms                                                 | 164 ms: 1.03x faster                                                  |
| regex_v8       | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.91 sec: 1.10x faster                                                |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 93.7 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.2 ms                                                | 83.3 ms: 1.02x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 57.8 ms: 1.02x faster                                                 |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| json_loads           | 26.5 us                                                | 28.8 us: 1.09x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.32 ms: 1.02x slower                                                 |
| python_startup         | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.8 ms: 1.10x faster                                                 |
| genshi_xml      | 50.2 ms                                                | 48.6 ms: 1.03x faster                                                 |
| django_template | 34.7 ms                                                | 34.4 ms: 1.01x faster                                                 |
| mako            | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.15 sec: 2.10x faster                                                |
| async_tree_none            | 464 ms                                                 | 256 ms: 1.82x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 599 ms: 1.81x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 617 ms: 1.80x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 312 ms: 1.79x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 253 ms: 1.77x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 315 ms: 1.76x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 510 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 505 ms: 1.42x faster                                                  |
| deepcopy                   | 352 us                                                 | 251 us: 1.40x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 29.0 us: 1.39x faster                                                 |
| go                         | 139 ms                                                 | 102 ms: 1.36x faster                                                  |
| comprehensions             | 19.8 us                                                | 15.4 us: 1.29x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.57 ms: 1.23x faster                                                 |
| scimark_sor                | 130 ms                                                 | 107 ms: 1.21x faster                                                  |
| raytrace                   | 299 ms                                                 | 250 ms: 1.20x faster                                                  |
| generators                 | 32.2 ms                                                | 27.1 ms: 1.19x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 66.8 ms: 1.18x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.63 us: 1.17x faster                                                 |
| logging_silent             | 109 ns                                                 | 93.4 ns: 1.17x faster                                                 |
| deltablue                  | 3.45 ms                                                | 2.99 ms: 1.15x faster                                                 |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                  |
| async_generators           | 384 ms                                                 | 338 ms: 1.14x faster                                                  |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                                  |
| spectral_norm              | 110 ms                                                 | 97.1 ms: 1.13x faster                                                 |
| richards                   | 45.9 ms                                                | 40.5 ms: 1.13x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.19 sec: 1.13x faster                                                |
| chaos                      | 62.8 ms                                                | 55.8 ms: 1.13x faster                                                 |
| richards_super             | 51.9 ms                                                | 46.3 ms: 1.12x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 68.7 ms: 1.12x faster                                                 |
| float                      | 80.8 ms                                                | 72.4 ms: 1.12x faster                                                 |
| pyflate                    | 448 ms                                                 | 402 ms: 1.11x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.97 us: 1.11x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 61.9 ms: 1.11x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.91 sec: 1.10x faster                                                |
| genshi_text                | 22.8 ms                                                | 20.8 ms: 1.10x faster                                                 |
| hexiom                     | 6.17 ms                                                | 5.67 ms: 1.09x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.0 ms: 1.08x faster                                                 |
| logging_format             | 7.35 us                                                | 6.79 us: 1.08x faster                                                 |
| sympy_str                  | 292 ms                                                 | 270 ms: 1.08x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 155 ms: 1.07x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.42 sec: 1.07x faster                                                |
| typing_runtime_protocols   | 163 us                                                 | 152 us: 1.07x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.09 sec: 1.07x faster                                                |
| pprint_safe_repr           | 743 ms                                                 | 695 ms: 1.07x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 249 ms: 1.06x faster                                                  |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.05x faster                                                 |
| meteor_contest             | 104 ms                                                 | 98.9 ms: 1.05x faster                                                 |
| html5lib                   | 63.6 ms                                                | 60.9 ms: 1.04x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 133 ms: 1.04x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                |
| nqueens                    | 80.1 ms                                                | 77.3 ms: 1.04x faster                                                 |
| thrift                     | 791 us                                                 | 765 us: 1.03x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.6 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 93.7 ms: 1.03x faster                                                 |
| scimark_fft                | 342 ms                                                 | 333 ms: 1.03x faster                                                  |
| regex_dna                  | 168 ms                                                 | 164 ms: 1.03x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.2 ms                                                | 83.3 ms: 1.02x faster                                                 |
| xml_etree_process          | 59.0 ms                                                | 57.8 ms: 1.02x faster                                                 |
| sympy_expand               | 468 ms                                                 | 459 ms: 1.02x faster                                                  |
| django_template            | 34.7 ms                                                | 34.4 ms: 1.01x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.24 us: 1.02x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.0 ms: 1.02x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 7.32 ms: 1.02x slower                                                 |
| json                       | 5.02 ms                                                | 5.15 ms: 1.02x slower                                                 |
| fannkuch                   | 372 ms                                                 | 385 ms: 1.03x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                 |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                 |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.8 us: 1.09x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.06 ms: 1.13x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.96 ms: 1.13x slower                                                 |
| coverage                   | 71.4 ms                                                | 83.5 ms: 1.17x slower                                                 |
| python_startup             | 9.93 ms                                                | 12.6 ms: 1.27x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 4.41 ms: 1.27x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.95 ms: 1.79x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 102 ms: 9.49x slower                                                  |
| telco                      | 6.53 ms                                                | 158 ms: 24.17x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (3): pickle_pure_python, nbody, asyncio_websockets
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.16x