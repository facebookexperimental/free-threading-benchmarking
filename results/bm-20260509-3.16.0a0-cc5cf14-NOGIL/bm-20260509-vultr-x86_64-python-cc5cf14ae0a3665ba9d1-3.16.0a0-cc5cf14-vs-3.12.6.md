# Results vs. 3.12.6

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: linux-x86_64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.038x slower
- HPT reliability: 91.91%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.64 sec                                               | 2.96 sec: 1.12x slower                                                |
| html5lib       | 63.6 ms                                                | 70.0 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                  | 1.11x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 691 ms: 1.61x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 709 ms: 1.53x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 393 ms: 1.42x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 325 ms: 1.37x faster                                                  |
| async_tree_none            | 464 ms                                                 | 340 ms: 1.37x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 419 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 573 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 584 ms: 1.22x faster                                                  |
| asyncio_tcp                | 519 ms                                                 | 463 ms: 1.12x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.02x faster                                                  |
| async_generators           | 384 ms                                                 | 387 ms: 1.01x slower                                                  |
| coroutines                 | 23.9 ms                                                | 25.0 ms: 1.04x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.68 sec: 1.12x slower                                                |
| Geometric mean             | (ref)                                                  | 1.22x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                  |
| float          | 80.8 ms                                                | 88.6 ms: 1.10x slower                                                 |
| nbody          | 89.3 ms                                                | 124 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                  | 1.17x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.94 ms: 1.08x faster                                                 |
| regex_v8       | 20.6 ms                                                | 20.2 ms: 1.02x faster                                                 |
| regex_compile  | 142 ms                                                 | 145 ms: 1.01x slower                                                  |
| regex_dna      | 168 ms                                                 | 172 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 95.4 ms: 1.01x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 140 ms: 1.01x slower                                                  |
| pickle_list          | 4.77 us                                                | 4.84 us: 1.02x slower                                                 |
| pickle_dict          | 31.8 us                                                | 32.4 us: 1.02x slower                                                 |
| json_dumps           | 10.4 ms                                                | 10.9 ms: 1.06x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 247 us: 1.12x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 347 us: 1.13x slower                                                  |
| pickle               | 10.9 us                                                | 12.6 us: 1.15x slower                                                 |
| json_loads           | 26.5 us                                                | 30.8 us: 1.16x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 101 ms: 1.19x slower                                                  |
| unpickle             | 14.1 us                                                | 17.0 us: 1.21x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.89 us: 1.26x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 74.9 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 39.6 ms: 1.14x slower                                                 |
| mako            | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 132 ms: 2.41x faster                                                  |
| gc_traversal               | 3.46 ms                                                | 1.89 ms: 1.83x faster                                                 |
| mdp                        | 2.42 sec                                               | 1.33 sec: 1.82x faster                                                |
| async_tree_io_tg           | 1.11 sec                                               | 691 ms: 1.61x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 709 ms: 1.53x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 393 ms: 1.42x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 325 ms: 1.37x faster                                                  |
| async_tree_none            | 464 ms                                                 | 340 ms: 1.37x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 419 ms: 1.32x faster                                                  |
| deepcopy                   | 352 us                                                 | 272 us: 1.29x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 31.4 us: 1.28x faster                                                 |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 573 ms: 1.26x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 584 ms: 1.22x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.3 ms: 1.18x faster                                                 |
| go                         | 139 ms                                                 | 123 ms: 1.13x faster                                                  |
| comprehensions             | 19.8 us                                                | 17.5 us: 1.13x faster                                                 |
| asyncio_tcp                | 519 ms                                                 | 463 ms: 1.12x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 1.96 us: 1.12x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.1 ms: 1.11x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.40 sec: 1.08x faster                                                |
| regex_effbot               | 3.17 ms                                                | 2.94 ms: 1.08x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.97 sec: 1.07x faster                                                |
| scimark_sor                | 130 ms                                                 | 123 ms: 1.05x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 3.01 us: 1.02x faster                                                 |
| regex_v8                   | 20.6 ms                                                | 20.2 ms: 1.02x faster                                                 |
| asyncio_websockets         | 517 ms                                                 | 509 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 95.4 ms: 1.01x faster                                                 |
| unpack_sequence            | 52.1 ns                                                | 51.5 ns: 1.01x faster                                                 |
| logging_silent             | 109 ns                                                 | 108 ns: 1.01x faster                                                  |
| spectral_norm              | 110 ms                                                 | 109 ms: 1.01x faster                                                  |
| async_generators           | 384 ms                                                 | 387 ms: 1.01x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                                |
| xml_etree_parse            | 139 ms                                                 | 140 ms: 1.01x slower                                                  |
| scimark_fft                | 342 ms                                                 | 347 ms: 1.01x slower                                                  |
| regex_compile              | 142 ms                                                 | 145 ms: 1.01x slower                                                  |
| pickle_list                | 4.77 us                                                | 4.84 us: 1.02x slower                                                 |
| pickle_dict                | 31.8 us                                                | 32.4 us: 1.02x slower                                                 |
| raytrace                   | 299 ms                                                 | 306 ms: 1.02x slower                                                  |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.03x slower                                                  |
| pyflate                    | 448 ms                                                 | 466 ms: 1.04x slower                                                  |
| coroutines                 | 23.9 ms                                                | 25.0 ms: 1.04x slower                                                 |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 10.9 ms: 1.06x slower                                                 |
| hexiom                     | 6.17 ms                                                | 6.55 ms: 1.06x slower                                                 |
| logging_simple             | 6.63 us                                                | 7.07 us: 1.07x slower                                                 |
| json                       | 5.02 ms                                                | 5.36 ms: 1.07x slower                                                 |
| logging_format             | 7.35 us                                                | 7.92 us: 1.08x slower                                                 |
| sympy_integrate            | 20.5 ms                                                | 22.2 ms: 1.08x slower                                                 |
| sympy_str                  | 292 ms                                                 | 316 ms: 1.08x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 181 ms: 1.09x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.77 ms: 1.09x slower                                                 |
| float                      | 80.8 ms                                                | 88.6 ms: 1.10x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 818 ms: 1.10x slower                                                  |
| html5lib                   | 63.6 ms                                                | 70.0 ms: 1.10x slower                                                 |
| nqueens                    | 80.1 ms                                                | 88.3 ms: 1.10x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.68 sec: 1.12x slower                                                |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                                |
| docutils                   | 2.64 sec                                               | 2.96 sec: 1.12x slower                                                |
| unpickle_pure_python       | 221 us                                                 | 247 us: 1.12x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 347 us: 1.13x slower                                                  |
| richards                   | 45.9 ms                                                | 52.4 ms: 1.14x slower                                                 |
| django_template            | 34.7 ms                                                | 39.6 ms: 1.14x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 130 ms: 1.14x slower                                                  |
| sympy_expand               | 468 ms                                                 | 536 ms: 1.15x slower                                                  |
| richards_super             | 51.9 ms                                                | 59.6 ms: 1.15x slower                                                 |
| pickle                     | 10.9 us                                                | 12.6 us: 1.15x slower                                                 |
| json_loads                 | 26.5 us                                                | 30.8 us: 1.16x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 79.5 ms: 1.16x slower                                                 |
| crypto_pyaes               | 76.6 ms                                                | 89.8 ms: 1.17x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 101 ms: 1.19x slower                                                  |
| thrift                     | 791 us                                                 | 939 us: 1.19x slower                                                  |
| unpickle                   | 14.1 us                                                | 17.0 us: 1.21x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.36 ms: 1.22x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 201 us: 1.23x slower                                                  |
| meteor_contest             | 104 ms                                                 | 129 ms: 1.24x slower                                                  |
| fannkuch                   | 372 ms                                                 | 469 ms: 1.26x slower                                                  |
| unpickle_list              | 4.67 us                                                | 5.89 us: 1.26x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 74.9 ms: 1.27x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 13.9 ms: 1.29x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.49 ms: 1.36x slower                                                 |
| nbody                      | 89.3 ms                                                | 124 ms: 1.39x slower                                                  |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.47 ms: 1.56x slower                                                 |
| coverage                   | 71.4 ms                                                | 115 ms: 1.61x slower                                                  |
| telco                      | 6.53 ms                                                | 177 ms: 27.07x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.05x slower                                                          |

Benchmark hidden because not significant (2): generators, chaos
Ignored benchmarks (18) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260509-3.16.0a0-cc5cf14-NOGIL/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.038x slower

# HPT report

- Reliability score: 91.91% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x