# Results vs. 3.12.6

- fork: mpage
- ref: exp_nolock
- machine: linux-x86_64
- commit hash: 4f84be5
- commit date: 2025-04-12
- overall geometric mean: 1.021x faster
- HPT reliability: 70.67%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 280 ms: 1.06x slower                                        |
| docutils       | 2.64 sec                                               | 2.68 sec: 1.02x slower                                      |
| html5lib       | 63.6 ms                                                | 64.7 ms: 1.02x slower                                       |
| Geometric mean | (ref)                                                  | 1.03x slower                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 520 ms: 2.13x faster                                        |
| async_tree_io              | 1.08 sec                                               | 547 ms: 1.98x faster                                        |
| async_tree_memoization_tg  | 560 ms                                                 | 283 ms: 1.97x faster                                        |
| async_tree_none_tg         | 446 ms                                                 | 226 ms: 1.97x faster                                        |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                        |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.79x faster                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 523 ms: 1.38x faster                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 550 ms: 1.30x faster                                        |
| async_generators           | 384 ms                                                 | 361 ms: 1.06x faster                                        |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                       |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                        |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 80.8 ms                                                | 67.5 ms: 1.20x faster                                       |
| pidigits       | 184 ms                                                 | 203 ms: 1.10x slower                                        |
| nbody          | 89.3 ms                                                | 110 ms: 1.23x slower                                        |
| Geometric mean | (ref)                                                  | 1.04x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                       |
| regex_compile  | 142 ms                                                 | 143 ms: 1.01x slower                                        |
| regex_v8       | 20.6 ms                                                | 21.1 ms: 1.03x slower                                       |
| regex_dna      | 168 ms                                                 | 184 ms: 1.09x slower                                        |
| Geometric mean | (ref)                                                  | 1.00x slower                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.0 ms: 1.11x faster                                       |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                        |
| unpickle_pure_python | 221 us                                                 | 229 us: 1.04x slower                                        |
| pickle_pure_python   | 308 us                                                 | 329 us: 1.07x slower                                        |
| xml_etree_generate   | 85.2 ms                                                | 93.0 ms: 1.09x slower                                       |
| xml_etree_process    | 59.0 ms                                                | 66.4 ms: 1.13x slower                                       |
| json_loads           | 26.5 us                                                | 30.6 us: 1.15x slower                                       |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.23x slower                                       |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.56x slower                                       |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                       |
| Geometric mean         | (ref)                                                  | 1.58x slower                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 55.4 ms: 1.10x slower                                       |
| genshi_text     | 22.8 ms                                                | 25.7 ms: 1.12x slower                                       |
| django_template | 34.7 ms                                                | 39.5 ms: 1.14x slower                                       |
| mako            | 11.0 ms                                                | 15.5 ms: 1.41x slower                                       |
| Geometric mean  | (ref)                                                  | 1.19x slower                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 520 ms: 2.13x faster                                        |
| async_tree_io              | 1.08 sec                                               | 547 ms: 1.98x faster                                        |
| async_tree_memoization_tg  | 560 ms                                                 | 283 ms: 1.97x faster                                        |
| async_tree_none_tg         | 446 ms                                                 | 226 ms: 1.97x faster                                        |
| gc_traversal               | 3.46 ms                                                | 1.77 ms: 1.96x faster                                       |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.85x faster                                      |
| async_tree_none            | 464 ms                                                 | 257 ms: 1.81x faster                                        |
| async_tree_memoization     | 555 ms                                                 | 309 ms: 1.79x faster                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 523 ms: 1.38x faster                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 550 ms: 1.30x faster                                        |
| deepcopy                   | 352 us                                                 | 286 us: 1.23x faster                                        |
| float                      | 80.8 ms                                                | 67.5 ms: 1.20x faster                                       |
| deepcopy_memo              | 40.3 us                                                | 35.1 us: 1.15x faster                                       |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                       |
| dulwich_log                | 78.9 ms                                                | 70.6 ms: 1.12x faster                                       |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                       |
| xml_etree_iterparse        | 96.7 ms                                                | 87.0 ms: 1.11x faster                                       |
| go                         | 139 ms                                                 | 126 ms: 1.10x faster                                        |
| sqlite_synth               | 2.20 us                                                | 2.01 us: 1.10x faster                                       |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                        |
| spectral_norm              | 110 ms                                                 | 102 ms: 1.08x faster                                        |
| async_generators           | 384 ms                                                 | 361 ms: 1.06x faster                                        |
| bpe_tokeniser              | 4.74 sec                                               | 4.49 sec: 1.05x faster                                      |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                        |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                      |
| pylint                     | 319 ms                                                 | 304 ms: 1.05x faster                                        |
| logging_silent             | 109 ns                                                 | 105 ns: 1.04x faster                                        |
| raytrace                   | 299 ms                                                 | 288 ms: 1.04x faster                                        |
| coroutines                 | 23.9 ms                                                | 23.1 ms: 1.04x faster                                       |
| deepcopy_reduce            | 3.08 us                                                | 2.97 us: 1.04x faster                                       |
| generators                 | 32.2 ms                                                | 31.6 ms: 1.02x faster                                       |
| comprehensions             | 19.8 us                                                | 19.5 us: 1.02x faster                                       |
| chaos                      | 62.8 ms                                                | 61.7 ms: 1.02x faster                                       |
| asyncio_websockets         | 517 ms                                                 | 515 ms: 1.00x faster                                        |
| scimark_fft                | 342 ms                                                 | 343 ms: 1.00x slower                                        |
| regex_compile              | 142 ms                                                 | 143 ms: 1.01x slower                                        |
| docutils                   | 2.64 sec                                               | 2.68 sec: 1.02x slower                                      |
| html5lib                   | 63.6 ms                                                | 64.7 ms: 1.02x slower                                       |
| regex_v8                   | 20.6 ms                                                | 21.1 ms: 1.03x slower                                       |
| pprint_safe_repr           | 743 ms                                                 | 769 ms: 1.04x slower                                        |
| unpickle_pure_python       | 221 us                                                 | 229 us: 1.04x slower                                        |
| json                       | 5.02 ms                                                | 5.21 ms: 1.04x slower                                       |
| deltablue                  | 3.45 ms                                                | 3.58 ms: 1.04x slower                                       |
| pprint_pformat             | 1.52 sec                                               | 1.59 sec: 1.04x slower                                      |
| pyflate                    | 448 ms                                                 | 470 ms: 1.05x slower                                        |
| logging_simple             | 6.63 us                                                | 7.03 us: 1.06x slower                                       |
| 2to3                       | 264 ms                                                 | 280 ms: 1.06x slower                                        |
| pickle_pure_python         | 308 us                                                 | 329 us: 1.07x slower                                        |
| logging_format             | 7.35 us                                                | 7.86 us: 1.07x slower                                       |
| sqlalchemy_declarative     | 143 ms                                                 | 153 ms: 1.07x slower                                        |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.4 ms: 1.08x slower                                       |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.08x slower                                       |
| sympy_sum                  | 166 ms                                                 | 179 ms: 1.08x slower                                        |
| crypto_pyaes               | 76.6 ms                                                | 82.7 ms: 1.08x slower                                       |
| hexiom                     | 6.17 ms                                                | 6.68 ms: 1.08x slower                                       |
| nqueens                    | 80.1 ms                                                | 86.8 ms: 1.08x slower                                       |
| sympy_str                  | 292 ms                                                 | 317 ms: 1.09x slower                                        |
| scimark_monte_carlo        | 68.4 ms                                                | 74.5 ms: 1.09x slower                                       |
| xml_etree_generate         | 85.2 ms                                                | 93.0 ms: 1.09x slower                                       |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.09x slower                                        |
| pidigits                   | 184 ms                                                 | 203 ms: 1.10x slower                                        |
| richards                   | 45.9 ms                                                | 50.7 ms: 1.10x slower                                       |
| genshi_xml                 | 50.2 ms                                                | 55.4 ms: 1.10x slower                                       |
| scimark_lu                 | 114 ms                                                 | 128 ms: 1.12x slower                                        |
| sympy_expand               | 468 ms                                                 | 525 ms: 1.12x slower                                        |
| genshi_text                | 22.8 ms                                                | 25.7 ms: 1.12x slower                                       |
| xml_etree_process          | 59.0 ms                                                | 66.4 ms: 1.13x slower                                       |
| richards_super             | 51.9 ms                                                | 59.1 ms: 1.14x slower                                       |
| django_template            | 34.7 ms                                                | 39.5 ms: 1.14x slower                                       |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.02 ms: 1.14x slower                                       |
| json_loads                 | 26.5 us                                                | 30.6 us: 1.15x slower                                       |
| typing_runtime_protocols   | 163 us                                                 | 189 us: 1.16x slower                                        |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.22x slower                                       |
| fannkuch                   | 372 ms                                                 | 455 ms: 1.22x slower                                        |
| nbody                      | 89.3 ms                                                | 110 ms: 1.23x slower                                        |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.23x slower                                       |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                        |
| telco                      | 6.53 ms                                                | 8.44 ms: 1.29x slower                                       |
| mako                       | 11.0 ms                                                | 15.5 ms: 1.41x slower                                       |
| coverage                   | 71.4 ms                                                | 109 ms: 1.52x slower                                        |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.56x slower                                       |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                       |
| bench_thread_pool          | 941 us                                                 | 3.13 ms: 3.33x slower                                       |
| bench_mp_pool              | 10.8 ms                                                | 95.4 ms: 8.83x slower                                       |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                |

Benchmark hidden because not significant (1): tomli_loads
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250412-3.14.0a7+-4f84be5-NOGIL/bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 70.67% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.37x