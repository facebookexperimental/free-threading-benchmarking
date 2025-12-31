# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: linux-x86_64
- commit hash: 564677c
- commit date: 2025-12-31
- overall geometric mean: 1.085x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 245 ms: 1.06x faster                                                       |
| html5lib       | 67.0 ms                                                      | 63.2 ms: 1.06x faster                                                      |
| Geometric mean | (ref)                                                        | 1.04x faster                                                               |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io              | 876 ms                                                       | 532 ms: 1.65x faster                                                       |
| async_tree_io_tg           | 913 ms                                                       | 570 ms: 1.60x faster                                                       |
| async_tree_memoization     | 461 ms                                                       | 289 ms: 1.60x faster                                                       |
| async_tree_none            | 354 ms                                                       | 232 ms: 1.52x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 231 ms: 1.46x faster                                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 288 ms: 1.44x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 474 ms: 1.40x faster                                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 474 ms: 1.35x faster                                                       |
| async_generators           | 377 ms                                                       | 365 ms: 1.03x faster                                                       |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                                      |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                       |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 60.3 ms: 1.28x faster                                                      |
| nbody          | 85.1 ms                                                      | 75.8 ms: 1.12x faster                                                      |
| pidigits       | 217 ms                                                       | 203 ms: 1.06x faster                                                       |
| Geometric mean | (ref)                                                        | 1.15x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.69 ms: 1.15x faster                                                      |
| regex_compile  | 132 ms                                                       | 123 ms: 1.08x faster                                                       |
| regex_v8       | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                      |
| regex_dna      | 180 ms                                                       | 173 ms: 1.04x faster                                                       |
| Geometric mean | (ref)                                                        | 1.08x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                       | 175 us: 1.20x faster                                                       |
| xml_etree_iterparse  | 94.9 ms                                                      | 83.0 ms: 1.14x faster                                                      |
| xml_etree_process    | 59.3 ms                                                      | 53.3 ms: 1.11x faster                                                      |
| json_dumps           | 10.5 ms                                                      | 9.57 ms: 1.10x faster                                                      |
| xml_etree_generate   | 85.4 ms                                                      | 78.5 ms: 1.09x faster                                                      |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                       |
| pickle_pure_python   | 294 us                                                       | 280 us: 1.05x faster                                                       |
| tomli_loads          | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                     |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.08x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.36 ms: 1.00x faster                                                      |
| python_startup         | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako           | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                      |
| genshi_text    | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                                      |
| genshi_xml     | 48.8 ms                                                      | 52.2 ms: 1.07x slower                                                      |
| Geometric mean | (ref)                                                        | 1.01x faster                                                               |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 17.9 ms: 2.52x faster                                                      |
| richards_super             | 51.6 ms                                                      | 21.5 ms: 2.40x faster                                                      |
| mdp                        | 2.36 sec                                                     | 1.43 sec: 1.65x faster                                                     |
| async_tree_io              | 876 ms                                                       | 532 ms: 1.65x faster                                                       |
| async_tree_io_tg           | 913 ms                                                       | 570 ms: 1.60x faster                                                       |
| async_tree_memoization     | 461 ms                                                       | 289 ms: 1.60x faster                                                       |
| deepcopy_memo              | 39.1 us                                                      | 24.8 us: 1.57x faster                                                      |
| async_tree_none            | 354 ms                                                       | 232 ms: 1.52x faster                                                       |
| go                         | 141 ms                                                       | 94.9 ms: 1.48x faster                                                      |
| deepcopy                   | 355 us                                                       | 242 us: 1.47x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 231 ms: 1.46x faster                                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 288 ms: 1.44x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 474 ms: 1.40x faster                                                       |
| scimark_sor                | 134 ms                                                       | 97.8 ms: 1.37x faster                                                      |
| scimark_fft                | 349 ms                                                       | 259 ms: 1.35x faster                                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 474 ms: 1.35x faster                                                       |
| float                      | 77.5 ms                                                      | 60.3 ms: 1.28x faster                                                      |
| scimark_monte_carlo        | 65.4 ms                                                      | 51.5 ms: 1.27x faster                                                      |
| spectral_norm              | 111 ms                                                       | 87.5 ms: 1.27x faster                                                      |
| deepcopy_reduce            | 3.11 us                                                      | 2.51 us: 1.24x faster                                                      |
| logging_silent             | 103 ns                                                       | 82.9 ns: 1.24x faster                                                      |
| pyflate                    | 449 ms                                                       | 364 ms: 1.23x faster                                                       |
| deltablue                  | 3.12 ms                                                      | 2.54 ms: 1.23x faster                                                      |
| unpickle_pure_python       | 210 us                                                       | 175 us: 1.20x faster                                                       |
| pprint_safe_repr           | 738 ms                                                       | 641 ms: 1.15x faster                                                       |
| regex_effbot               | 3.08 ms                                                      | 2.69 ms: 1.15x faster                                                      |
| scimark_lu                 | 113 ms                                                       | 98.2 ms: 1.15x faster                                                      |
| chaos                      | 57.3 ms                                                      | 50.1 ms: 1.14x faster                                                      |
| xml_etree_iterparse        | 94.9 ms                                                      | 83.0 ms: 1.14x faster                                                      |
| nbody                      | 85.1 ms                                                      | 75.8 ms: 1.12x faster                                                      |
| pprint_pformat             | 1.50 sec                                                     | 1.33 sec: 1.12x faster                                                     |
| xml_etree_process          | 59.3 ms                                                      | 53.3 ms: 1.11x faster                                                      |
| json_dumps                 | 10.5 ms                                                      | 9.57 ms: 1.10x faster                                                      |
| bpe_tokeniser              | 4.45 sec                                                     | 4.08 sec: 1.09x faster                                                     |
| logging_simple             | 6.16 us                                                      | 5.66 us: 1.09x faster                                                      |
| xml_etree_generate         | 85.4 ms                                                      | 78.5 ms: 1.09x faster                                                      |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                      |
| regex_compile              | 132 ms                                                       | 123 ms: 1.08x faster                                                       |
| mako                       | 11.3 ms                                                      | 10.5 ms: 1.08x faster                                                      |
| dulwich_log                | 74.8 ms                                                      | 69.8 ms: 1.07x faster                                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.40 ms: 1.07x faster                                                      |
| logging_format             | 6.84 us                                                      | 6.41 us: 1.07x faster                                                      |
| pidigits                   | 217 ms                                                       | 203 ms: 1.06x faster                                                       |
| 2to3                       | 260 ms                                                       | 245 ms: 1.06x faster                                                       |
| html5lib                   | 67.0 ms                                                      | 63.2 ms: 1.06x faster                                                      |
| thrift                     | 778 us                                                       | 736 us: 1.06x faster                                                       |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                       |
| pickle_pure_python         | 294 us                                                       | 280 us: 1.05x faster                                                       |
| fannkuch                   | 370 ms                                                       | 352 ms: 1.05x faster                                                       |
| typing_runtime_protocols   | 155 us                                                       | 148 us: 1.05x faster                                                       |
| regex_v8                   | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                      |
| regex_dna                  | 180 ms                                                       | 173 ms: 1.04x faster                                                       |
| async_generators           | 377 ms                                                       | 365 ms: 1.03x faster                                                       |
| meteor_contest             | 102 ms                                                       | 98.5 ms: 1.03x faster                                                      |
| coverage                   | 83.0 ms                                                      | 80.7 ms: 1.03x faster                                                      |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                      |
| generators                 | 28.8 ms                                                      | 28.2 ms: 1.02x faster                                                      |
| genshi_text                | 21.5 ms                                                      | 21.1 ms: 1.02x faster                                                      |
| tomli_loads                | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                     |
| sqlite_synth               | 2.21 us                                                      | 2.18 us: 1.01x faster                                                      |
| crypto_pyaes               | 67.9 ms                                                      | 67.1 ms: 1.01x faster                                                      |
| json                       | 4.93 ms                                                      | 4.87 ms: 1.01x faster                                                      |
| python_startup_no_site     | 7.39 ms                                                      | 7.36 ms: 1.00x faster                                                      |
| raytrace                   | 253 ms                                                       | 258 ms: 1.02x slower                                                       |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                                      |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                      |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                       |
| hexiom                     | 5.99 ms                                                      | 6.35 ms: 1.06x slower                                                      |
| genshi_xml                 | 48.8 ms                                                      | 52.2 ms: 1.07x slower                                                      |
| sympy_integrate            | 19.8 ms                                                      | 21.3 ms: 1.08x slower                                                      |
| nqueens                    | 78.6 ms                                                      | 86.9 ms: 1.11x slower                                                      |
| sympy_expand               | 457 ms                                                       | 514 ms: 1.13x slower                                                       |
| pycparser                  | 1.12 sec                                                     | 1.27 sec: 1.14x slower                                                     |
| python_startup             | 11.0 ms                                                      | 12.6 ms: 1.15x slower                                                      |
| sympy_sum                  | 156 ms                                                       | 180 ms: 1.15x slower                                                       |
| sympy_str                  | 275 ms                                                       | 323 ms: 1.18x slower                                                       |
| create_gc_cycles           | 1.34 ms                                                      | 1.93 ms: 1.44x slower                                                      |
| bench_thread_pool          | 919 us                                                       | 1.33 ms: 1.44x slower                                                      |
| gc_traversal               | 3.14 ms                                                      | 4.56 ms: 1.45x slower                                                      |
| bench_mp_pool              | 11.0 ms                                                      | 203 ms: 18.48x slower                                                      |
| telco                      | 7.82 ms                                                      | 145 ms: 18.50x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                               |

Benchmark hidden because not significant (3): django_template, docutils, pylint
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251231-3.15.0a3+-564677c-JIT/bm-20251231-vultr-x86_64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-564677c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.085x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.18x