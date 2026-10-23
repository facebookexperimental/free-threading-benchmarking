# Results vs. 3.12.6

- fork: corona10
- ref: MI_SEGMENT_SLICE_SHI
- machine: linux-x86_64
- commit hash: 2e2a547
- commit date: 2026-10-22
- overall geometric mean: 1.033x slower
- HPT reliability: 73.57%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 294 ms: 1.11x slower                                                        |
| docutils       | 2.64 sec                                               | 2.86 sec: 1.08x slower                                                      |
| html5lib       | 63.6 ms                                                | 66.9 ms: 1.05x slower                                                       |
| Geometric mean | (ref)                                                  | 1.08x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 699 ms: 1.59x faster                                                        |
| async_tree_io              | 1.08 sec                                               | 706 ms: 1.53x faster                                                        |
| async_tree_memoization_tg  | 560 ms                                                 | 399 ms: 1.40x faster                                                        |
| async_tree_none            | 464 ms                                                 | 336 ms: 1.38x faster                                                        |
| async_tree_none_tg         | 446 ms                                                 | 333 ms: 1.34x faster                                                        |
| async_tree_memoization     | 555 ms                                                 | 419 ms: 1.33x faster                                                        |
| async_generators           | 384 ms                                                 | 302 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 574 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 577 ms: 1.24x faster                                                        |
| asyncio_websockets         | 517 ms                                                 | 502 ms: 1.03x faster                                                        |
| coroutines                 | 23.9 ms                                                | 26.1 ms: 1.09x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 188 ms: 1.02x slower                                                        |
| float          | 80.8 ms                                                | 83.7 ms: 1.04x slower                                                       |
| nbody          | 89.3 ms                                                | 122 ms: 1.36x slower                                                        |
| Geometric mean | (ref)                                                  | 1.13x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.96 ms: 1.07x faster                                                       |
| regex_v8       | 20.6 ms                                                | 21.1 ms: 1.03x slower                                                       |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                        |
| regex_compile  | 142 ms                                                 | 170 ms: 1.19x slower                                                        |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                      |
| json_dumps           | 10.4 ms                                                | 10.2 ms: 1.02x faster                                                       |
| xml_etree_iterparse  | 96.7 ms                                                | 97.4 ms: 1.01x slower                                                       |
| xml_etree_parse      | 139 ms                                                 | 145 ms: 1.05x slower                                                        |
| unpickle_pure_python | 221 us                                                 | 237 us: 1.08x slower                                                        |
| pickle_pure_python   | 308 us                                                 | 343 us: 1.11x slower                                                        |
| json_loads           | 26.5 us                                                | 30.8 us: 1.16x slower                                                       |
| xml_etree_generate   | 85.2 ms                                                | 102 ms: 1.20x slower                                                        |
| xml_etree_process    | 59.0 ms                                                | 75.2 ms: 1.28x slower                                                       |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.11 ms: 1.27x slower                                                       |
| python_startup         | 9.93 ms                                                | 13.9 ms: 1.40x slower                                                       |
| Geometric mean         | (ref)                                                  | 1.33x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 41.6 ms: 1.20x slower                                                       |
| mako            | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                       |
| Geometric mean  | (ref)                                                  | 1.31x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 131 ms: 2.43x faster                                                        |
| gc_traversal               | 3.46 ms                                                | 1.81 ms: 1.91x faster                                                       |
| mdp                        | 2.42 sec                                               | 1.28 sec: 1.89x faster                                                      |
| bench_mp_pool              | 10.8 ms                                                | 6.66 ms: 1.62x faster                                                       |
| async_tree_io_tg           | 1.11 sec                                               | 699 ms: 1.59x faster                                                        |
| async_tree_io              | 1.08 sec                                               | 706 ms: 1.53x faster                                                        |
| async_tree_memoization_tg  | 560 ms                                                 | 399 ms: 1.40x faster                                                        |
| async_tree_none            | 464 ms                                                 | 336 ms: 1.38x faster                                                        |
| async_tree_none_tg         | 446 ms                                                 | 333 ms: 1.34x faster                                                        |
| async_tree_memoization     | 555 ms                                                 | 419 ms: 1.33x faster                                                        |
| deepcopy                   | 352 us                                                 | 271 us: 1.30x faster                                                        |
| async_generators           | 384 ms                                                 | 302 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 574 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 577 ms: 1.24x faster                                                        |
| deepcopy_memo              | 40.3 us                                                | 32.6 us: 1.23x faster                                                       |
| pathlib                    | 21.5 ms                                                | 18.0 ms: 1.19x faster                                                       |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                        |
| sqlite_synth               | 2.20 us                                                | 1.91 us: 1.15x faster                                                       |
| typing_runtime_protocols   | 163 us                                                 | 146 us: 1.12x faster                                                        |
| dulwich_log                | 78.9 ms                                                | 72.4 ms: 1.09x faster                                                       |
| scimark_sor                | 130 ms                                                 | 120 ms: 1.08x faster                                                        |
| bpe_tokeniser              | 4.74 sec                                               | 4.40 sec: 1.08x faster                                                      |
| comprehensions             | 19.8 us                                                | 18.5 us: 1.07x faster                                                       |
| tomli_loads                | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.96 ms: 1.07x faster                                                       |
| spectral_norm              | 110 ms                                                 | 103 ms: 1.07x faster                                                        |
| chaos                      | 62.8 ms                                                | 60.0 ms: 1.05x faster                                                       |
| deepcopy_reduce            | 3.08 us                                                | 2.96 us: 1.04x faster                                                       |
| asyncio_websockets         | 517 ms                                                 | 502 ms: 1.03x faster                                                        |
| raytrace                   | 299 ms                                                 | 293 ms: 1.02x faster                                                        |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                        |
| pyflate                    | 448 ms                                                 | 439 ms: 1.02x faster                                                        |
| json_dumps                 | 10.4 ms                                                | 10.2 ms: 1.02x faster                                                       |
| pycparser                  | 1.17 sec                                               | 1.16 sec: 1.01x faster                                                      |
| scimark_fft                | 342 ms                                                 | 338 ms: 1.01x faster                                                        |
| xml_etree_iterparse        | 96.7 ms                                                | 97.4 ms: 1.01x slower                                                       |
| pidigits                   | 184 ms                                                 | 188 ms: 1.02x slower                                                        |
| regex_v8                   | 20.6 ms                                                | 21.1 ms: 1.03x slower                                                       |
| float                      | 80.8 ms                                                | 83.7 ms: 1.04x slower                                                       |
| generators                 | 32.2 ms                                                | 33.5 ms: 1.04x slower                                                       |
| xml_etree_parse            | 139 ms                                                 | 145 ms: 1.05x slower                                                        |
| html5lib                   | 63.6 ms                                                | 66.9 ms: 1.05x slower                                                       |
| logging_simple             | 6.63 us                                                | 7.01 us: 1.06x slower                                                       |
| deltablue                  | 3.45 ms                                                | 3.65 ms: 1.06x slower                                                       |
| hexiom                     | 6.17 ms                                                | 6.58 ms: 1.07x slower                                                       |
| sympy_integrate            | 20.5 ms                                                | 22.1 ms: 1.07x slower                                                       |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                        |
| unpickle_pure_python       | 221 us                                                 | 237 us: 1.08x slower                                                        |
| logging_format             | 7.35 us                                                | 7.93 us: 1.08x slower                                                       |
| docutils                   | 2.64 sec                                               | 2.86 sec: 1.08x slower                                                      |
| json                       | 5.02 ms                                                | 5.46 ms: 1.09x slower                                                       |
| coroutines                 | 23.9 ms                                                | 26.1 ms: 1.09x slower                                                       |
| pprint_safe_repr           | 743 ms                                                 | 816 ms: 1.10x slower                                                        |
| sympy_str                  | 292 ms                                                 | 321 ms: 1.10x slower                                                        |
| sympy_sum                  | 166 ms                                                 | 184 ms: 1.11x slower                                                        |
| pprint_pformat             | 1.52 sec                                               | 1.68 sec: 1.11x slower                                                      |
| pickle_pure_python         | 308 us                                                 | 343 us: 1.11x slower                                                        |
| 2to3                       | 264 ms                                                 | 294 ms: 1.11x slower                                                        |
| nqueens                    | 80.1 ms                                                | 89.3 ms: 1.12x slower                                                       |
| scimark_monte_carlo        | 68.4 ms                                                | 77.0 ms: 1.13x slower                                                       |
| richards                   | 45.9 ms                                                | 52.2 ms: 1.14x slower                                                       |
| sympy_expand               | 468 ms                                                 | 535 ms: 1.14x slower                                                        |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.14x slower                                                        |
| crypto_pyaes               | 76.6 ms                                                | 87.8 ms: 1.15x slower                                                       |
| thrift                     | 791 us                                                 | 912 us: 1.15x slower                                                        |
| richards_super             | 51.9 ms                                                | 60.0 ms: 1.16x slower                                                       |
| json_loads                 | 26.5 us                                                | 30.8 us: 1.16x slower                                                       |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.19 ms: 1.18x slower                                                       |
| regex_compile              | 142 ms                                                 | 170 ms: 1.19x slower                                                        |
| xml_etree_generate         | 85.2 ms                                                | 102 ms: 1.20x slower                                                        |
| django_template            | 34.7 ms                                                | 41.6 ms: 1.20x slower                                                       |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.21x slower                                                        |
| create_gc_cycles           | 1.09 ms                                                | 1.34 ms: 1.23x slower                                                       |
| fannkuch                   | 372 ms                                                 | 467 ms: 1.26x slower                                                        |
| python_startup_no_site     | 7.16 ms                                                | 9.11 ms: 1.27x slower                                                       |
| xml_etree_process          | 59.0 ms                                                | 75.2 ms: 1.28x slower                                                       |
| nbody                      | 89.3 ms                                                | 122 ms: 1.36x slower                                                        |
| python_startup             | 9.93 ms                                                | 13.9 ms: 1.40x slower                                                       |
| mako                       | 11.0 ms                                                | 15.8 ms: 1.43x slower                                                       |
| bench_thread_pool          | 941 us                                                 | 1.40 ms: 1.49x slower                                                       |
| coverage                   | 71.4 ms                                                | 119 ms: 1.66x slower                                                        |
| telco                      | 6.53 ms                                                | 175 ms: 26.81x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                                |
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261022-3.16.0a1+dev-2e2a547-NOGIL/bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.033x slower

# HPT report

- Reliability score: 73.57% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x