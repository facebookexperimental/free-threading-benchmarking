# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: linux-x86_64
- commit hash: 2e9b980
- commit date: 2026-03-15
- overall geometric mean: 1.105x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 250 ms: 1.04x faster                                                       |
| html5lib       | 67.0 ms                                                      | 60.9 ms: 1.10x faster                                                      |
| Geometric mean | (ref)                                                        | 1.05x faster                                                               |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 551 ms: 1.66x faster                                                       |
| async_tree_memoization     | 461 ms                                                       | 284 ms: 1.62x faster                                                       |
| async_tree_io              | 876 ms                                                       | 567 ms: 1.55x faster                                                       |
| async_tree_none            | 354 ms                                                       | 232 ms: 1.53x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 236 ms: 1.43x faster                                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 294 ms: 1.41x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 492 ms: 1.35x faster                                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 502 ms: 1.27x faster                                                       |
| coroutines                 | 23.6 ms                                                      | 22.1 ms: 1.07x faster                                                      |
| async_generators           | 377 ms                                                       | 354 ms: 1.06x faster                                                       |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 60.0 ms: 1.29x faster                                                      |
| nbody          | 85.1 ms                                                      | 76.8 ms: 1.11x faster                                                      |
| pidigits       | 217 ms                                                       | 208 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                        | 1.14x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                      |
| regex_v8       | 22.7 ms                                                      | 20.9 ms: 1.09x faster                                                      |
| regex_dna      | 180 ms                                                       | 168 ms: 1.07x faster                                                       |
| regex_compile  | 132 ms                                                       | 124 ms: 1.07x faster                                                       |
| Geometric mean | (ref)                                                        | 1.09x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.51 sec: 1.33x faster                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.3 ms: 1.14x faster                                                      |
| json_dumps           | 10.5 ms                                                      | 9.32 ms: 1.13x faster                                                      |
| xml_etree_process    | 59.3 ms                                                      | 53.1 ms: 1.12x faster                                                      |
| xml_etree_generate   | 85.4 ms                                                      | 79.8 ms: 1.07x faster                                                      |
| unpickle_pure_python | 210 us                                                       | 197 us: 1.07x faster                                                       |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                       |
| json_loads           | 27.0 us                                                      | 26.9 us: 1.00x faster                                                      |
| pickle_pure_python   | 294 us                                                       | 311 us: 1.06x slower                                                       |
| Geometric mean       | (ref)                                                        | 1.09x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.52 ms: 1.02x slower                                                      |
| python_startup         | 11.0 ms                                                      | 12.7 ms: 1.15x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.08x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                      |
| django_template | 34.1 ms                                                      | 31.9 ms: 1.07x faster                                                      |
| genshi_text     | 21.5 ms                                                      | 20.7 ms: 1.04x faster                                                      |
| genshi_xml      | 48.8 ms                                                      | 53.3 ms: 1.09x slower                                                      |
| Geometric mean  | (ref)                                                        | 1.02x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 18.3 ms: 2.46x faster                                                      |
| richards_super             | 51.6 ms                                                      | 22.1 ms: 2.33x faster                                                      |
| mdp                        | 2.36 sec                                                     | 1.21 sec: 1.95x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 22.4 us: 1.74x faster                                                      |
| async_tree_io_tg           | 913 ms                                                       | 551 ms: 1.66x faster                                                       |
| async_tree_memoization     | 461 ms                                                       | 284 ms: 1.62x faster                                                       |
| scimark_sor                | 134 ms                                                       | 83.6 ms: 1.61x faster                                                      |
| deepcopy                   | 355 us                                                       | 225 us: 1.58x faster                                                       |
| async_tree_io              | 876 ms                                                       | 567 ms: 1.55x faster                                                       |
| async_tree_none            | 354 ms                                                       | 232 ms: 1.53x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 236 ms: 1.43x faster                                                       |
| scimark_lu                 | 113 ms                                                       | 79.8 ms: 1.41x faster                                                      |
| spectral_norm              | 111 ms                                                       | 78.7 ms: 1.41x faster                                                      |
| async_tree_memoization_tg  | 414 ms                                                       | 294 ms: 1.41x faster                                                       |
| go                         | 141 ms                                                       | 103 ms: 1.37x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 492 ms: 1.35x faster                                                       |
| scimark_fft                | 349 ms                                                       | 261 ms: 1.34x faster                                                       |
| tomli_loads                | 2.01 sec                                                     | 1.51 sec: 1.33x faster                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 2.35 us: 1.32x faster                                                      |
| float                      | 77.5 ms                                                      | 60.0 ms: 1.29x faster                                                      |
| logging_silent             | 103 ns                                                       | 80.6 ns: 1.27x faster                                                      |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 502 ms: 1.27x faster                                                       |
| scimark_monte_carlo        | 65.4 ms                                                      | 51.7 ms: 1.26x faster                                                      |
| pyflate                    | 449 ms                                                       | 361 ms: 1.24x faster                                                       |
| deltablue                  | 3.12 ms                                                      | 2.66 ms: 1.17x faster                                                      |
| pprint_safe_repr           | 738 ms                                                       | 628 ms: 1.17x faster                                                       |
| logging_simple             | 6.16 us                                                      | 5.25 us: 1.17x faster                                                      |
| pprint_pformat             | 1.50 sec                                                     | 1.29 sec: 1.16x faster                                                     |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.3 ms: 1.14x faster                                                      |
| regex_effbot               | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                      |
| json_dumps                 | 10.5 ms                                                      | 9.32 ms: 1.13x faster                                                      |
| logging_format             | 6.84 us                                                      | 6.06 us: 1.13x faster                                                      |
| bpe_tokeniser              | 4.45 sec                                                     | 3.94 sec: 1.13x faster                                                     |
| xml_etree_process          | 59.3 ms                                                      | 53.1 ms: 1.12x faster                                                      |
| nbody                      | 85.1 ms                                                      | 76.8 ms: 1.11x faster                                                      |
| pathlib                    | 19.2 ms                                                      | 17.3 ms: 1.11x faster                                                      |
| comprehensions             | 16.5 us                                                      | 14.9 us: 1.11x faster                                                      |
| html5lib                   | 67.0 ms                                                      | 60.9 ms: 1.10x faster                                                      |
| chaos                      | 57.3 ms                                                      | 52.2 ms: 1.10x faster                                                      |
| regex_v8                   | 22.7 ms                                                      | 20.9 ms: 1.09x faster                                                      |
| nqueens                    | 78.6 ms                                                      | 72.7 ms: 1.08x faster                                                      |
| mako                       | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                      |
| dulwich_log                | 74.8 ms                                                      | 69.6 ms: 1.08x faster                                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.38 ms: 1.08x faster                                                      |
| regex_dna                  | 180 ms                                                       | 168 ms: 1.07x faster                                                       |
| django_template            | 34.1 ms                                                      | 31.9 ms: 1.07x faster                                                      |
| xml_etree_generate         | 85.4 ms                                                      | 79.8 ms: 1.07x faster                                                      |
| fannkuch                   | 370 ms                                                       | 347 ms: 1.07x faster                                                       |
| regex_compile              | 132 ms                                                       | 124 ms: 1.07x faster                                                       |
| unpickle_pure_python       | 210 us                                                       | 197 us: 1.07x faster                                                       |
| coroutines                 | 23.6 ms                                                      | 22.1 ms: 1.07x faster                                                      |
| async_generators           | 377 ms                                                       | 354 ms: 1.06x faster                                                       |
| meteor_contest             | 102 ms                                                       | 97.4 ms: 1.04x faster                                                      |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                       |
| 2to3                       | 260 ms                                                       | 250 ms: 1.04x faster                                                       |
| pidigits                   | 217 ms                                                       | 208 ms: 1.04x faster                                                       |
| genshi_text                | 21.5 ms                                                      | 20.7 ms: 1.04x faster                                                      |
| hexiom                     | 5.99 ms                                                      | 5.81 ms: 1.03x faster                                                      |
| crypto_pyaes               | 67.9 ms                                                      | 66.0 ms: 1.03x faster                                                      |
| typing_runtime_protocols   | 155 us                                                       | 151 us: 1.03x faster                                                       |
| sqlite_synth               | 2.21 us                                                      | 2.16 us: 1.02x faster                                                      |
| json                       | 4.93 ms                                                      | 4.84 ms: 1.02x faster                                                      |
| json_loads                 | 27.0 us                                                      | 26.9 us: 1.00x faster                                                      |
| sympy_integrate            | 19.8 ms                                                      | 20.1 ms: 1.01x slower                                                      |
| python_startup_no_site     | 7.39 ms                                                      | 7.52 ms: 1.02x slower                                                      |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                       |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.05x slower                                                     |
| sympy_expand               | 457 ms                                                       | 482 ms: 1.06x slower                                                       |
| pickle_pure_python         | 294 us                                                       | 311 us: 1.06x slower                                                       |
| sympy_str                  | 275 ms                                                       | 292 ms: 1.06x slower                                                       |
| sympy_sum                  | 156 ms                                                       | 168 ms: 1.08x slower                                                       |
| genshi_xml                 | 48.8 ms                                                      | 53.3 ms: 1.09x slower                                                      |
| python_startup             | 11.0 ms                                                      | 12.7 ms: 1.15x slower                                                      |
| raytrace                   | 253 ms                                                       | 297 ms: 1.18x slower                                                       |
| generators                 | 28.8 ms                                                      | 35.3 ms: 1.22x slower                                                      |
| gc_traversal               | 3.14 ms                                                      | 4.27 ms: 1.36x slower                                                      |
| create_gc_cycles           | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                                      |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.44x slower                                                      |
| bench_mp_pool              | 11.0 ms                                                      | 169 ms: 15.36x slower                                                      |
| telco                      | 7.82 ms                                                      | 155 ms: 19.86x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                               |

Benchmark hidden because not significant (4): pylint, coverage, docutils, thrift
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260315-3.15.0a7+-2e9b980-JIT/bm-20260315-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a7+-2e9b980.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.105x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.19x