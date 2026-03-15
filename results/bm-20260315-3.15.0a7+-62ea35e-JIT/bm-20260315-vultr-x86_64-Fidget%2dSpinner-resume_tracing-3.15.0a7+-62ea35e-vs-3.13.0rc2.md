# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: linux-x86_64
- commit hash: 62ea35e
- commit date: 2026-03-15
- overall geometric mean: 1.095x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 249 ms: 1.04x faster                                                       |
| docutils       | 2.62 sec                                                     | 2.66 sec: 1.02x slower                                                     |
| html5lib       | 67.0 ms                                                      | 62.5 ms: 1.07x faster                                                      |
| Geometric mean | (ref)                                                        | 1.03x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 550 ms: 1.66x faster                                                       |
| async_tree_memoization     | 461 ms                                                       | 290 ms: 1.59x faster                                                       |
| async_tree_io              | 876 ms                                                       | 573 ms: 1.53x faster                                                       |
| async_tree_none            | 354 ms                                                       | 233 ms: 1.52x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 233 ms: 1.44x faster                                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 294 ms: 1.41x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 487 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 499 ms: 1.28x faster                                                       |
| coroutines                 | 23.6 ms                                                      | 22.2 ms: 1.06x faster                                                      |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                       |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 58.9 ms: 1.31x faster                                                      |
| nbody          | 85.1 ms                                                      | 76.6 ms: 1.11x faster                                                      |
| pidigits       | 217 ms                                                       | 201 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                        | 1.16x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                      |
| regex_compile  | 132 ms                                                       | 125 ms: 1.06x faster                                                       |
| regex_dna      | 180 ms                                                       | 179 ms: 1.01x faster                                                       |
| regex_v8       | 22.7 ms                                                      | 23.4 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                        | 1.03x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.55 sec: 1.29x faster                                                     |
| json_dumps           | 10.5 ms                                                      | 9.15 ms: 1.15x faster                                                      |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.8 ms: 1.13x faster                                                      |
| xml_etree_process    | 59.3 ms                                                      | 53.0 ms: 1.12x faster                                                      |
| xml_etree_generate   | 85.4 ms                                                      | 78.9 ms: 1.08x faster                                                      |
| unpickle_pure_python | 210 us                                                       | 199 us: 1.05x faster                                                       |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                       |
| json_loads           | 27.0 us                                                      | 27.7 us: 1.02x slower                                                      |
| pickle_pure_python   | 294 us                                                       | 315 us: 1.07x slower                                                       |
| Geometric mean       | (ref)                                                        | 1.08x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.53 ms: 1.02x slower                                                      |
| python_startup         | 11.0 ms                                                      | 12.7 ms: 1.16x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.09x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako           | 11.3 ms                                                      | 10.6 ms: 1.07x faster                                                      |
| genshi_text    | 21.5 ms                                                      | 20.3 ms: 1.06x faster                                                      |
| genshi_xml     | 48.8 ms                                                      | 52.4 ms: 1.07x slower                                                      |
| Geometric mean | (ref)                                                        | 1.01x faster                                                               |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 18.4 ms: 2.45x faster                                                      |
| richards_super             | 51.6 ms                                                      | 22.1 ms: 2.33x faster                                                      |
| mdp                        | 2.36 sec                                                     | 1.20 sec: 1.96x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 22.6 us: 1.73x faster                                                      |
| async_tree_io_tg           | 913 ms                                                       | 550 ms: 1.66x faster                                                       |
| scimark_sor                | 134 ms                                                       | 82.3 ms: 1.63x faster                                                      |
| async_tree_memoization     | 461 ms                                                       | 290 ms: 1.59x faster                                                       |
| deepcopy                   | 355 us                                                       | 229 us: 1.55x faster                                                       |
| async_tree_io              | 876 ms                                                       | 573 ms: 1.53x faster                                                       |
| async_tree_none            | 354 ms                                                       | 233 ms: 1.52x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 233 ms: 1.44x faster                                                       |
| spectral_norm              | 111 ms                                                       | 77.8 ms: 1.43x faster                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 294 ms: 1.41x faster                                                       |
| scimark_lu                 | 113 ms                                                       | 80.1 ms: 1.41x faster                                                      |
| go                         | 141 ms                                                       | 102 ms: 1.38x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 487 ms: 1.37x faster                                                       |
| scimark_fft                | 349 ms                                                       | 262 ms: 1.34x faster                                                       |
| float                      | 77.5 ms                                                      | 58.9 ms: 1.31x faster                                                      |
| tomli_loads                | 2.01 sec                                                     | 1.55 sec: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 499 ms: 1.28x faster                                                       |
| scimark_monte_carlo        | 65.4 ms                                                      | 51.5 ms: 1.27x faster                                                      |
| logging_silent             | 103 ns                                                       | 81.0 ns: 1.27x faster                                                      |
| deepcopy_reduce            | 3.11 us                                                      | 2.51 us: 1.24x faster                                                      |
| pyflate                    | 449 ms                                                       | 363 ms: 1.23x faster                                                       |
| deltablue                  | 3.12 ms                                                      | 2.67 ms: 1.17x faster                                                      |
| pprint_pformat             | 1.50 sec                                                     | 1.30 sec: 1.15x faster                                                     |
| json_dumps                 | 10.5 ms                                                      | 9.15 ms: 1.15x faster                                                      |
| pprint_safe_repr           | 738 ms                                                       | 649 ms: 1.14x faster                                                       |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.8 ms: 1.13x faster                                                      |
| logging_simple             | 6.16 us                                                      | 5.46 us: 1.13x faster                                                      |
| bpe_tokeniser              | 4.45 sec                                                     | 3.96 sec: 1.12x faster                                                     |
| xml_etree_process          | 59.3 ms                                                      | 53.0 ms: 1.12x faster                                                      |
| nbody                      | 85.1 ms                                                      | 76.6 ms: 1.11x faster                                                      |
| logging_format             | 6.84 us                                                      | 6.17 us: 1.11x faster                                                      |
| pathlib                    | 19.2 ms                                                      | 17.3 ms: 1.11x faster                                                      |
| chaos                      | 57.3 ms                                                      | 51.8 ms: 1.11x faster                                                      |
| comprehensions             | 16.5 us                                                      | 14.9 us: 1.10x faster                                                      |
| regex_effbot               | 3.08 ms                                                      | 2.80 ms: 1.10x faster                                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.30 ms: 1.09x faster                                                      |
| fannkuch                   | 370 ms                                                       | 341 ms: 1.09x faster                                                       |
| xml_etree_generate         | 85.4 ms                                                      | 78.9 ms: 1.08x faster                                                      |
| pidigits                   | 217 ms                                                       | 201 ms: 1.08x faster                                                       |
| nqueens                    | 78.6 ms                                                      | 73.1 ms: 1.07x faster                                                      |
| html5lib                   | 67.0 ms                                                      | 62.5 ms: 1.07x faster                                                      |
| mako                       | 11.3 ms                                                      | 10.6 ms: 1.07x faster                                                      |
| regex_compile              | 132 ms                                                       | 125 ms: 1.06x faster                                                       |
| genshi_text                | 21.5 ms                                                      | 20.3 ms: 1.06x faster                                                      |
| coroutines                 | 23.6 ms                                                      | 22.2 ms: 1.06x faster                                                      |
| dulwich_log                | 74.8 ms                                                      | 70.6 ms: 1.06x faster                                                      |
| unpickle_pure_python       | 210 us                                                       | 199 us: 1.05x faster                                                       |
| async_generators           | 377 ms                                                       | 359 ms: 1.05x faster                                                       |
| meteor_contest             | 102 ms                                                       | 96.7 ms: 1.05x faster                                                      |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                       |
| 2to3                       | 260 ms                                                       | 249 ms: 1.04x faster                                                       |
| crypto_pyaes               | 67.9 ms                                                      | 65.4 ms: 1.04x faster                                                      |
| hexiom                     | 5.99 ms                                                      | 5.82 ms: 1.03x faster                                                      |
| typing_runtime_protocols   | 155 us                                                       | 151 us: 1.02x faster                                                       |
| regex_dna                  | 180 ms                                                       | 179 ms: 1.01x faster                                                       |
| docutils                   | 2.62 sec                                                     | 2.66 sec: 1.02x slower                                                     |
| python_startup_no_site     | 7.39 ms                                                      | 7.53 ms: 1.02x slower                                                      |
| json_loads                 | 27.0 us                                                      | 27.7 us: 1.02x slower                                                      |
| sympy_integrate            | 19.8 ms                                                      | 20.4 ms: 1.03x slower                                                      |
| regex_v8                   | 22.7 ms                                                      | 23.4 ms: 1.03x slower                                                      |
| thrift                     | 778 us                                                       | 804 us: 1.03x slower                                                       |
| pycparser                  | 1.12 sec                                                     | 1.16 sec: 1.04x slower                                                     |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                       |
| pickle_pure_python         | 294 us                                                       | 315 us: 1.07x slower                                                       |
| genshi_xml                 | 48.8 ms                                                      | 52.4 ms: 1.07x slower                                                      |
| sympy_expand               | 457 ms                                                       | 492 ms: 1.08x slower                                                       |
| sympy_str                  | 275 ms                                                       | 300 ms: 1.09x slower                                                       |
| sympy_sum                  | 156 ms                                                       | 171 ms: 1.10x slower                                                       |
| python_startup             | 11.0 ms                                                      | 12.7 ms: 1.16x slower                                                      |
| raytrace                   | 253 ms                                                       | 293 ms: 1.16x slower                                                       |
| generators                 | 28.8 ms                                                      | 35.0 ms: 1.21x slower                                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.87 ms: 1.40x slower                                                      |
| bench_thread_pool          | 919 us                                                       | 1.33 ms: 1.45x slower                                                      |
| gc_traversal               | 3.14 ms                                                      | 4.64 ms: 1.48x slower                                                      |
| bench_mp_pool              | 11.0 ms                                                      | 191 ms: 17.35x slower                                                      |
| telco                      | 7.82 ms                                                      | 160 ms: 20.40x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                               |

Benchmark hidden because not significant (5): pylint, json, coverage, sqlite_synth, django_template
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260315-3.15.0a7+-62ea35e-JIT/bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-62ea35e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.095x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.19x