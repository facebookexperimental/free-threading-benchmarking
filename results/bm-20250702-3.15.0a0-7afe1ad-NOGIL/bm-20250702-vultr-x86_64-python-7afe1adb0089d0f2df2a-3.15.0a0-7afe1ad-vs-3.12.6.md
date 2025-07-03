# Results vs. 3.12.6

- fork: python
- ref: 7afe1adb0089d0f2df2a
- machine: linux-x86_64
- commit hash: 7afe1ad
- commit date: 2025-07-02
- overall geometric mean: 1.021x slower
- HPT reliability: 89.47%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 283 ms: 1.07x slower                                                  |
| docutils       | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 65.0 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 527 ms: 2.11x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 285 ms: 1.96x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 553 ms: 1.96x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 228 ms: 1.96x faster                                                  |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 522 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 545 ms: 1.31x faster                                                  |
| async_generators           | 384 ms                                                 | 369 ms: 1.04x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.51x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 69.5 ms: 1.16x faster                                                 |
| pidigits       | 184 ms                                                 | 206 ms: 1.12x slower                                                  |
| nbody          | 89.3 ms                                                | 124 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.75 ms: 1.15x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.5 ms: 1.00x faster                                                 |
| regex_compile  | 142 ms                                                 | 142 ms: 1.00x faster                                                  |
| regex_dna      | 168 ms                                                 | 172 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.1 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                |
| unpickle_pure_python | 221 us                                                 | 230 us: 1.04x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 335 us: 1.09x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 94.9 ms: 1.11x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                 |
| json_loads           | 26.5 us                                                | 31.1 us: 1.17x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.3 ms: 1.18x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.53 ms: 1.33x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.46x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 39.0 ms: 1.13x slower                                                 |
| genshi_xml      | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.2 ms: 1.15x slower                                                 |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.21x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 527 ms: 2.11x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 285 ms: 1.96x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 553 ms: 1.96x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 228 ms: 1.96x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.87 ms: 1.85x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                                |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.80x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 313 ms: 1.77x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 522 ms: 1.38x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 545 ms: 1.31x faster                                                  |
| deepcopy                   | 352 us                                                 | 290 us: 1.21x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 34.3 us: 1.17x faster                                                 |
| float                      | 80.8 ms                                                | 69.5 ms: 1.16x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.75 ms: 1.15x faster                                                 |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.6 us: 1.13x faster                                                 |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 87.1 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.7 ms: 1.10x faster                                                 |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.40 sec: 1.08x faster                                                |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.06x faster                                                  |
| async_generators           | 384 ms                                                 | 369 ms: 1.04x faster                                                  |
| logging_silent             | 109 ns                                                 | 105 ns: 1.04x faster                                                  |
| pylint                     | 319 ms                                                 | 308 ms: 1.03x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.02x faster                                                |
| generators                 | 32.2 ms                                                | 31.7 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| regex_v8                   | 20.6 ms                                                | 20.5 ms: 1.00x faster                                                 |
| regex_compile              | 142 ms                                                 | 142 ms: 1.00x faster                                                  |
| spectral_norm              | 110 ms                                                 | 110 ms: 1.00x faster                                                  |
| raytrace                   | 299 ms                                                 | 303 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.3 ms: 1.01x slower                                                 |
| docutils                   | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                |
| pyflate                    | 448 ms                                                 | 457 ms: 1.02x slower                                                  |
| html5lib                   | 63.6 ms                                                | 65.0 ms: 1.02x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.15 sec: 1.02x slower                                                |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.03x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.85 us: 1.03x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.38 ms: 1.03x slower                                                 |
| deltablue                  | 3.45 ms                                                | 3.57 ms: 1.04x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 230 us: 1.04x slower                                                  |
| pprint_safe_repr           | 743 ms                                                 | 777 ms: 1.05x slower                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.60 sec: 1.05x slower                                                |
| json                       | 5.02 ms                                                | 5.33 ms: 1.06x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                 |
| 2to3                       | 264 ms                                                 | 283 ms: 1.07x slower                                                  |
| sympy_str                  | 292 ms                                                 | 313 ms: 1.07x slower                                                  |
| scimark_fft                | 342 ms                                                 | 367 ms: 1.07x slower                                                  |
| logging_format             | 7.35 us                                                | 7.92 us: 1.08x slower                                                 |
| sympy_sum                  | 166 ms                                                 | 180 ms: 1.08x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 335 us: 1.09x slower                                                  |
| nqueens                    | 80.1 ms                                                | 87.7 ms: 1.10x slower                                                 |
| thrift                     | 791 us                                                 | 874 us: 1.10x slower                                                  |
| xml_etree_generate         | 85.2 ms                                                | 94.9 ms: 1.11x slower                                                 |
| richards                   | 45.9 ms                                                | 51.3 ms: 1.12x slower                                                 |
| pidigits                   | 184 ms                                                 | 206 ms: 1.12x slower                                                  |
| sympy_expand               | 468 ms                                                 | 525 ms: 1.12x slower                                                  |
| django_template            | 34.7 ms                                                | 39.0 ms: 1.13x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 129 ms: 1.13x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 87.0 ms: 1.14x slower                                                 |
| richards_super             | 51.9 ms                                                | 59.0 ms: 1.14x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 77.8 ms: 1.14x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 186 us: 1.14x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.2 ms: 1.15x slower                                                 |
| meteor_contest             | 104 ms                                                 | 119 ms: 1.15x slower                                                  |
| xml_etree_process          | 59.0 ms                                                | 68.8 ms: 1.17x slower                                                 |
| json_loads                 | 26.5 us                                                | 31.1 us: 1.17x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.3 ms: 1.18x slower                                                 |
| fannkuch                   | 372 ms                                                 | 454 ms: 1.22x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.38 ms: 1.22x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.44 ms: 1.32x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.53 ms: 1.33x slower                                                 |
| nbody                      | 89.3 ms                                                | 124 ms: 1.39x slower                                                  |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                 |
| coverage                   | 71.4 ms                                                | 111 ms: 1.55x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.9 ms: 1.60x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.18 ms: 3.38x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 9.96x slower                                                  |
| telco                      | 6.53 ms                                                | 175 ms: 26.80x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                          |

Benchmark hidden because not significant (2): deepcopy_reduce, chaos
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.021x slower

# HPT report

- Reliability score: 89.47% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x