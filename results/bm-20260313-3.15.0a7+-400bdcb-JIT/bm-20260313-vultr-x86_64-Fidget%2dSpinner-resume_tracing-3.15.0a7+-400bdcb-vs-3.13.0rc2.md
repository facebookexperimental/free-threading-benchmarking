# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: linux-x86_64
- commit hash: 400bdcb
- commit date: 2026-03-13
- overall geometric mean: 1.098x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 250 ms: 1.04x faster                                                       |
| docutils       | 2.62 sec                                                     | 2.65 sec: 1.01x slower                                                     |
| html5lib       | 67.0 ms                                                      | 61.2 ms: 1.09x faster                                                      |
| Geometric mean | (ref)                                                        | 1.04x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 550 ms: 1.66x faster                                                       |
| async_tree_memoization     | 461 ms                                                       | 287 ms: 1.61x faster                                                       |
| async_tree_io              | 876 ms                                                       | 567 ms: 1.55x faster                                                       |
| async_tree_none            | 354 ms                                                       | 232 ms: 1.52x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 233 ms: 1.45x faster                                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 292 ms: 1.42x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.35x faster                                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 505 ms: 1.26x faster                                                       |
| coroutines                 | 23.6 ms                                                      | 21.8 ms: 1.08x faster                                                      |
| async_generators           | 377 ms                                                       | 355 ms: 1.06x faster                                                       |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 59.0 ms: 1.31x faster                                                      |
| nbody          | 85.1 ms                                                      | 74.2 ms: 1.15x faster                                                      |
| pidigits       | 217 ms                                                       | 219 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                        | 1.14x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                                      |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                       |
| regex_dna      | 180 ms                                                       | 179 ms: 1.01x faster                                                       |
| regex_v8       | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                        | 1.03x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.53 sec: 1.31x faster                                                     |
| json_dumps           | 10.5 ms                                                      | 8.97 ms: 1.17x faster                                                      |
| xml_etree_iterparse  | 94.9 ms                                                      | 84.0 ms: 1.13x faster                                                      |
| xml_etree_process    | 59.3 ms                                                      | 53.1 ms: 1.12x faster                                                      |
| xml_etree_generate   | 85.4 ms                                                      | 79.2 ms: 1.08x faster                                                      |
| unpickle_pure_python | 210 us                                                       | 199 us: 1.05x faster                                                       |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                       |
| pickle_pure_python   | 294 us                                                       | 313 us: 1.06x slower                                                       |
| Geometric mean       | (ref)                                                        | 1.09x faster                                                               |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.51 ms: 1.02x slower                                                      |
| python_startup         | 11.0 ms                                                      | 12.7 ms: 1.15x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.08x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako           | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                      |
| genshi_text    | 21.5 ms                                                      | 20.3 ms: 1.06x faster                                                      |
| genshi_xml     | 48.8 ms                                                      | 51.7 ms: 1.06x slower                                                      |
| Geometric mean | (ref)                                                        | 1.02x faster                                                               |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 18.7 ms: 2.42x faster                                                      |
| richards_super             | 51.6 ms                                                      | 22.2 ms: 2.32x faster                                                      |
| mdp                        | 2.36 sec                                                     | 1.20 sec: 1.96x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 22.7 us: 1.72x faster                                                      |
| async_tree_io_tg           | 913 ms                                                       | 550 ms: 1.66x faster                                                       |
| scimark_sor                | 134 ms                                                       | 82.8 ms: 1.62x faster                                                      |
| async_tree_memoization     | 461 ms                                                       | 287 ms: 1.61x faster                                                       |
| deepcopy                   | 355 us                                                       | 225 us: 1.58x faster                                                       |
| async_tree_io              | 876 ms                                                       | 567 ms: 1.55x faster                                                       |
| async_tree_none            | 354 ms                                                       | 232 ms: 1.52x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 233 ms: 1.45x faster                                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 292 ms: 1.42x faster                                                       |
| spectral_norm              | 111 ms                                                       | 78.5 ms: 1.42x faster                                                      |
| scimark_lu                 | 113 ms                                                       | 80.0 ms: 1.41x faster                                                      |
| go                         | 141 ms                                                       | 101 ms: 1.39x faster                                                       |
| scimark_fft                | 349 ms                                                       | 256 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 495 ms: 1.35x faster                                                       |
| float                      | 77.5 ms                                                      | 59.0 ms: 1.31x faster                                                      |
| tomli_loads                | 2.01 sec                                                     | 1.53 sec: 1.31x faster                                                     |
| logging_silent             | 103 ns                                                       | 79.2 ns: 1.30x faster                                                      |
| deepcopy_reduce            | 3.11 us                                                      | 2.46 us: 1.27x faster                                                      |
| scimark_monte_carlo        | 65.4 ms                                                      | 51.7 ms: 1.26x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 505 ms: 1.26x faster                                                       |
| pyflate                    | 449 ms                                                       | 359 ms: 1.25x faster                                                       |
| pprint_safe_repr           | 738 ms                                                       | 628 ms: 1.18x faster                                                       |
| json_dumps                 | 10.5 ms                                                      | 8.97 ms: 1.17x faster                                                      |
| deltablue                  | 3.12 ms                                                      | 2.67 ms: 1.17x faster                                                      |
| pprint_pformat             | 1.50 sec                                                     | 1.30 sec: 1.15x faster                                                     |
| logging_simple             | 6.16 us                                                      | 5.36 us: 1.15x faster                                                      |
| nbody                      | 85.1 ms                                                      | 74.2 ms: 1.15x faster                                                      |
| bpe_tokeniser              | 4.45 sec                                                     | 3.93 sec: 1.13x faster                                                     |
| logging_format             | 6.84 us                                                      | 6.05 us: 1.13x faster                                                      |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.0 ms: 1.13x faster                                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.18 ms: 1.13x faster                                                      |
| xml_etree_process          | 59.3 ms                                                      | 53.1 ms: 1.12x faster                                                      |
| pathlib                    | 19.2 ms                                                      | 17.4 ms: 1.10x faster                                                      |
| regex_effbot               | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                                      |
| chaos                      | 57.3 ms                                                      | 52.2 ms: 1.10x faster                                                      |
| html5lib                   | 67.0 ms                                                      | 61.2 ms: 1.09x faster                                                      |
| fannkuch                   | 370 ms                                                       | 338 ms: 1.09x faster                                                       |
| nqueens                    | 78.6 ms                                                      | 72.5 ms: 1.08x faster                                                      |
| mako                       | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                      |
| coroutines                 | 23.6 ms                                                      | 21.8 ms: 1.08x faster                                                      |
| xml_etree_generate         | 85.4 ms                                                      | 79.2 ms: 1.08x faster                                                      |
| dulwich_log                | 74.8 ms                                                      | 70.1 ms: 1.07x faster                                                      |
| genshi_text                | 21.5 ms                                                      | 20.3 ms: 1.06x faster                                                      |
| async_generators           | 377 ms                                                       | 355 ms: 1.06x faster                                                       |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                       |
| unpickle_pure_python       | 210 us                                                       | 199 us: 1.05x faster                                                       |
| meteor_contest             | 102 ms                                                       | 97.5 ms: 1.04x faster                                                      |
| hexiom                     | 5.99 ms                                                      | 5.75 ms: 1.04x faster                                                      |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                       |
| 2to3                       | 260 ms                                                       | 250 ms: 1.04x faster                                                       |
| typing_runtime_protocols   | 155 us                                                       | 150 us: 1.03x faster                                                       |
| crypto_pyaes               | 67.9 ms                                                      | 66.0 ms: 1.03x faster                                                      |
| sqlite_synth               | 2.21 us                                                      | 2.15 us: 1.03x faster                                                      |
| json                       | 4.93 ms                                                      | 4.85 ms: 1.02x faster                                                      |
| regex_dna                  | 180 ms                                                       | 179 ms: 1.01x faster                                                       |
| coverage                   | 83.0 ms                                                      | 82.4 ms: 1.01x faster                                                      |
| pidigits                   | 217 ms                                                       | 219 ms: 1.01x slower                                                       |
| docutils                   | 2.62 sec                                                     | 2.65 sec: 1.01x slower                                                     |
| python_startup_no_site     | 7.39 ms                                                      | 7.51 ms: 1.02x slower                                                      |
| regex_v8                   | 22.7 ms                                                      | 23.2 ms: 1.02x slower                                                      |
| thrift                     | 778 us                                                       | 796 us: 1.02x slower                                                       |
| sympy_integrate            | 19.8 ms                                                      | 20.5 ms: 1.03x slower                                                      |
| pycparser                  | 1.12 sec                                                     | 1.16 sec: 1.04x slower                                                     |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                       |
| genshi_xml                 | 48.8 ms                                                      | 51.7 ms: 1.06x slower                                                      |
| pickle_pure_python         | 294 us                                                       | 313 us: 1.06x slower                                                       |
| sympy_expand               | 457 ms                                                       | 489 ms: 1.07x slower                                                       |
| comprehensions             | 16.5 us                                                      | 17.8 us: 1.08x slower                                                      |
| sympy_str                  | 275 ms                                                       | 304 ms: 1.11x slower                                                       |
| sympy_sum                  | 156 ms                                                       | 175 ms: 1.13x slower                                                       |
| python_startup             | 11.0 ms                                                      | 12.7 ms: 1.15x slower                                                      |
| raytrace                   | 253 ms                                                       | 293 ms: 1.16x slower                                                       |
| generators                 | 28.8 ms                                                      | 34.6 ms: 1.20x slower                                                      |
| gc_traversal               | 3.14 ms                                                      | 4.32 ms: 1.37x slower                                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.85 ms: 1.38x slower                                                      |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.44x slower                                                      |
| bench_mp_pool              | 11.0 ms                                                      | 182 ms: 16.56x slower                                                      |
| telco                      | 7.82 ms                                                      | 155 ms: 19.78x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                               |

Benchmark hidden because not significant (3): pylint, django_template, json_loads
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260313-3.15.0a7+-400bdcb-JIT/bm-20260313-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-400bdcb.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.098x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.19x