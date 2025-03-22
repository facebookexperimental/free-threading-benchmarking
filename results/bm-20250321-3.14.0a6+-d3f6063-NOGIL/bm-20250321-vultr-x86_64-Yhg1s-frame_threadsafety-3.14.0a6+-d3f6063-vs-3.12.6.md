# Results vs. 3.12.6

- fork: Yhg1s
- ref: frame_threadsafety
- machine: linux-x86_64
- commit hash: d3f6063
- commit date: 2025-03-21
- overall geometric mean: 1.045x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 297 ms: 1.13x slower                                                |
| docutils       | 2.64 sec                                               | 2.76 sec: 1.05x slower                                              |
| html5lib       | 63.6 ms                                                | 71.2 ms: 1.12x slower                                               |
| Geometric mean | (ref)                                                  | 1.10x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 551 ms: 2.01x faster                                                |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.88x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 298 ms: 1.87x faster                                                |
| async_tree_io              | 1.08 sec                                               | 588 ms: 1.84x faster                                                |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.68x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 332 ms: 1.67x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 535 ms: 1.35x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 568 ms: 1.26x faster                                                |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                               |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                        |

Benchmark hidden because not significant (2): async_generators, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.1 ms: 1.03x faster                                               |
| pidigits       | 184 ms                                                 | 216 ms: 1.17x slower                                                |
| nbody          | 89.3 ms                                                | 137 ms: 1.53x slower                                                |
| Geometric mean | (ref)                                                  | 1.20x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.85 ms: 1.11x faster                                               |
| regex_dna      | 168 ms                                                 | 172 ms: 1.02x slower                                                |
| regex_v8       | 20.6 ms                                                | 21.3 ms: 1.03x slower                                               |
| regex_compile  | 142 ms                                                 | 157 ms: 1.10x slower                                                |
| Geometric mean | (ref)                                                  | 1.01x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 88.0 ms: 1.10x faster                                               |
| xml_etree_parse      | 139 ms                                                 | 129 ms: 1.07x faster                                                |
| tomli_loads          | 2.11 sec                                               | 2.34 sec: 1.11x slower                                              |
| json_loads           | 26.5 us                                                | 29.6 us: 1.11x slower                                               |
| xml_etree_generate   | 85.2 ms                                                | 97.2 ms: 1.14x slower                                               |
| unpickle_pure_python | 221 us                                                 | 254 us: 1.15x slower                                                |
| pickle_pure_python   | 308 us                                                 | 360 us: 1.17x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 70.5 ms: 1.20x slower                                               |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.26x slower                                               |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 11.1 ms: 1.55x slower                                               |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                               |
| Geometric mean         | (ref)                                                  | 1.56x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.6 ms: 1.19x slower                                               |
| django_template | 34.7 ms                                                | 42.7 ms: 1.23x slower                                               |
| genshi_text     | 22.8 ms                                                | 28.6 ms: 1.25x slower                                               |
| mako            | 11.0 ms                                                | 15.9 ms: 1.44x slower                                               |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 551 ms: 2.01x faster                                                |
| gc_traversal               | 3.46 ms                                                | 1.79 ms: 1.93x faster                                               |
| async_tree_none_tg         | 446 ms                                                 | 238 ms: 1.88x faster                                                |
| async_tree_memoization_tg  | 560 ms                                                 | 298 ms: 1.87x faster                                                |
| async_tree_io              | 1.08 sec                                               | 588 ms: 1.84x faster                                                |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.68x faster                                                |
| async_tree_memoization     | 555 ms                                                 | 332 ms: 1.67x faster                                                |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 535 ms: 1.35x faster                                                |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 568 ms: 1.26x faster                                                |
| deepcopy                   | 352 us                                                 | 310 us: 1.13x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.85 ms: 1.11x faster                                               |
| sqlite_synth               | 2.20 us                                                | 1.99 us: 1.11x faster                                               |
| xml_etree_iterparse        | 96.7 ms                                                | 88.0 ms: 1.10x faster                                               |
| pathlib                    | 21.5 ms                                                | 19.7 ms: 1.09x faster                                               |
| dulwich_log                | 78.9 ms                                                | 72.8 ms: 1.08x faster                                               |
| xml_etree_parse            | 139 ms                                                 | 129 ms: 1.07x faster                                                |
| float                      | 80.8 ms                                                | 78.1 ms: 1.03x faster                                               |
| deepcopy_memo              | 40.3 us                                                | 39.2 us: 1.03x faster                                               |
| coroutines                 | 23.9 ms                                                | 23.3 ms: 1.03x faster                                               |
| generators                 | 32.2 ms                                                | 31.5 ms: 1.02x faster                                               |
| json                       | 5.02 ms                                                | 5.07 ms: 1.01x slower                                               |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.02x slower                                              |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.02x slower                                                |
| bpe_tokeniser              | 4.74 sec                                               | 4.86 sec: 1.03x slower                                              |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.03x slower                                                |
| deepcopy_reduce            | 3.08 us                                                | 3.17 us: 1.03x slower                                               |
| regex_v8                   | 20.6 ms                                                | 21.3 ms: 1.03x slower                                               |
| logging_silent             | 109 ns                                                 | 114 ns: 1.04x slower                                                |
| docutils                   | 2.64 sec                                               | 2.76 sec: 1.05x slower                                              |
| comprehensions             | 19.8 us                                                | 20.8 us: 1.05x slower                                               |
| go                         | 139 ms                                                 | 146 ms: 1.05x slower                                                |
| scimark_sor                | 130 ms                                                 | 137 ms: 1.05x slower                                                |
| thrift                     | 791 us                                                 | 855 us: 1.08x slower                                                |
| sqlalchemy_imperative      | 21.8 ms                                                | 23.6 ms: 1.08x slower                                               |
| raytrace                   | 299 ms                                                 | 326 ms: 1.09x slower                                                |
| logging_simple             | 6.63 us                                                | 7.29 us: 1.10x slower                                               |
| sqlalchemy_declarative     | 143 ms                                                 | 157 ms: 1.10x slower                                                |
| regex_compile              | 142 ms                                                 | 157 ms: 1.10x slower                                                |
| chaos                      | 62.8 ms                                                | 69.4 ms: 1.11x slower                                               |
| tomli_loads                | 2.11 sec                                               | 2.34 sec: 1.11x slower                                              |
| json_loads                 | 26.5 us                                                | 29.6 us: 1.11x slower                                               |
| pyflate                    | 448 ms                                                 | 499 ms: 1.11x slower                                                |
| sympy_sum                  | 166 ms                                                 | 185 ms: 1.12x slower                                                |
| logging_format             | 7.35 us                                                | 8.21 us: 1.12x slower                                               |
| html5lib                   | 63.6 ms                                                | 71.2 ms: 1.12x slower                                               |
| deltablue                  | 3.45 ms                                                | 3.86 ms: 1.12x slower                                               |
| 2to3                       | 264 ms                                                 | 297 ms: 1.13x slower                                                |
| pprint_safe_repr           | 743 ms                                                 | 843 ms: 1.13x slower                                                |
| xml_etree_generate         | 85.2 ms                                                | 97.2 ms: 1.14x slower                                               |
| sympy_integrate            | 20.5 ms                                                | 23.5 ms: 1.14x slower                                               |
| sympy_str                  | 292 ms                                                 | 334 ms: 1.15x slower                                                |
| mdp                        | 2.42 sec                                               | 2.78 sec: 1.15x slower                                              |
| unpickle_pure_python       | 221 us                                                 | 254 us: 1.15x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.75 sec: 1.15x slower                                              |
| crypto_pyaes               | 76.6 ms                                                | 89.0 ms: 1.16x slower                                               |
| pickle_pure_python         | 308 us                                                 | 360 us: 1.17x slower                                                |
| scimark_fft                | 342 ms                                                 | 400 ms: 1.17x slower                                                |
| pidigits                   | 184 ms                                                 | 216 ms: 1.17x slower                                                |
| sympy_expand               | 468 ms                                                 | 549 ms: 1.17x slower                                                |
| genshi_xml                 | 50.2 ms                                                | 59.6 ms: 1.19x slower                                               |
| xml_etree_process          | 59.0 ms                                                | 70.5 ms: 1.20x slower                                               |
| richards                   | 45.9 ms                                                | 55.2 ms: 1.20x slower                                               |
| typing_runtime_protocols   | 163 us                                                 | 196 us: 1.20x slower                                                |
| scimark_monte_carlo        | 68.4 ms                                                | 83.2 ms: 1.22x slower                                               |
| nqueens                    | 80.1 ms                                                | 97.8 ms: 1.22x slower                                               |
| django_template            | 34.7 ms                                                | 42.7 ms: 1.23x slower                                               |
| richards_super             | 51.9 ms                                                | 64.0 ms: 1.23x slower                                               |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.24x slower                                               |
| hexiom                     | 6.17 ms                                                | 7.69 ms: 1.25x slower                                               |
| genshi_text                | 22.8 ms                                                | 28.6 ms: 1.25x slower                                               |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.26x slower                                               |
| scimark_lu                 | 114 ms                                                 | 144 ms: 1.26x slower                                                |
| meteor_contest             | 104 ms                                                 | 133 ms: 1.28x slower                                                |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.71 ms: 1.30x slower                                               |
| fannkuch                   | 372 ms                                                 | 500 ms: 1.34x slower                                                |
| coverage                   | 71.4 ms                                                | 97.6 ms: 1.37x slower                                               |
| telco                      | 6.53 ms                                                | 9.06 ms: 1.39x slower                                               |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.44x slower                                               |
| nbody                      | 89.3 ms                                                | 137 ms: 1.53x slower                                                |
| python_startup_no_site     | 7.16 ms                                                | 11.1 ms: 1.55x slower                                               |
| python_startup             | 9.93 ms                                                | 15.7 ms: 1.58x slower                                               |
| bench_thread_pool          | 941 us                                                 | 3.16 ms: 3.35x slower                                               |
| bench_mp_pool              | 10.8 ms                                                | 96.4 ms: 8.92x slower                                               |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                        |

Benchmark hidden because not significant (3): pylint, async_generators, asyncio_websockets
Ignored benchmarks (19) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250321-3.14.0a6+-d3f6063-NOGIL/bm-20250321-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6+-d3f6063.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.045x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.38x