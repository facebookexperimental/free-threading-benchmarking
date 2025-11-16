# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: jit_Ft_llvm_19
- machine: linux-x86_64
- commit hash: afae648
- commit date: 2025-11-16
- overall geometric mean: 1.048x slower
- HPT reliability: 82.22%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.42x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 286 ms: 1.10x slower                                                       |
| html5lib       | 67.0 ms                                                      | 74.0 ms: 1.10x slower                                                      |
| Geometric mean | (ref)                                                        | 1.10x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 541 ms: 1.69x faster                                                       |
| async_tree_io              | 876 ms                                                       | 562 ms: 1.56x faster                                                       |
| async_tree_memoization     | 461 ms                                                       | 320 ms: 1.44x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 234 ms: 1.44x faster                                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 292 ms: 1.42x faster                                                       |
| async_tree_none            | 354 ms                                                       | 262 ms: 1.35x faster                                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 540 ms: 1.18x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 565 ms: 1.18x faster                                                       |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                       |
| coroutines                 | 23.6 ms                                                      | 24.5 ms: 1.04x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 57.4 ms: 1.35x faster                                                      |
| pidigits       | 217 ms                                                       | 217 ms: 1.00x slower                                                       |
| nbody          | 85.1 ms                                                      | 105 ms: 1.24x slower                                                       |
| Geometric mean | (ref)                                                        | 1.03x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                      |
| regex_v8       | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                      |
| regex_dna      | 180 ms                                                       | 179 ms: 1.00x faster                                                       |
| regex_compile  | 132 ms                                                       | 149 ms: 1.13x slower                                                       |
| Geometric mean | (ref)                                                        | 1.00x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|---------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| xml_etree_iterparse | 94.9 ms                                                      | 86.4 ms: 1.10x faster                                                      |
| xml_etree_parse     | 136 ms                                                       | 131 ms: 1.04x faster                                                       |
| json_dumps          | 10.5 ms                                                      | 10.9 ms: 1.03x slower                                                      |
| xml_etree_generate  | 85.4 ms                                                      | 90.7 ms: 1.06x slower                                                      |
| xml_etree_process   | 59.3 ms                                                      | 64.5 ms: 1.09x slower                                                      |
| pickle_pure_python  | 294 us                                                       | 335 us: 1.14x slower                                                       |
| json_loads          | 27.0 us                                                      | 31.5 us: 1.17x slower                                                      |
| Geometric mean      | (ref)                                                        | 1.04x slower                                                               |

Benchmark hidden because not significant (2): unpickle_pure_python, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.51 ms: 1.29x slower                                                      |
| python_startup         | 11.0 ms                                                      | 15.9 ms: 1.45x slower                                                      |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 42.4 ms: 1.24x slower                                                      |
| mako            | 11.3 ms                                                      | 14.3 ms: 1.26x slower                                                      |
| genshi_text     | 21.5 ms                                                      | 28.9 ms: 1.34x slower                                                      |
| genshi_xml      | 48.8 ms                                                      | 69.8 ms: 1.43x slower                                                      |
| Geometric mean  | (ref)                                                        | 1.32x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 541 ms: 1.69x faster                                                       |
| richards                   | 45.2 ms                                                      | 27.4 ms: 1.65x faster                                                      |
| gc_traversal               | 3.14 ms                                                      | 1.93 ms: 1.63x faster                                                      |
| richards_super             | 51.6 ms                                                      | 32.8 ms: 1.58x faster                                                      |
| async_tree_io              | 876 ms                                                       | 562 ms: 1.56x faster                                                       |
| mdp                        | 2.36 sec                                                     | 1.62 sec: 1.46x faster                                                     |
| async_tree_memoization     | 461 ms                                                       | 320 ms: 1.44x faster                                                       |
| async_tree_none_tg         | 336 ms                                                       | 234 ms: 1.44x faster                                                       |
| async_tree_memoization_tg  | 414 ms                                                       | 292 ms: 1.42x faster                                                       |
| float                      | 77.5 ms                                                      | 57.4 ms: 1.35x faster                                                      |
| async_tree_none            | 354 ms                                                       | 262 ms: 1.35x faster                                                       |
| deepcopy_memo              | 39.1 us                                                      | 30.0 us: 1.30x faster                                                      |
| deepcopy                   | 355 us                                                       | 299 us: 1.19x faster                                                       |
| scimark_fft                | 349 ms                                                       | 295 ms: 1.18x faster                                                       |
| scimark_sor                | 134 ms                                                       | 114 ms: 1.18x faster                                                       |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 540 ms: 1.18x faster                                                       |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 565 ms: 1.18x faster                                                       |
| go                         | 141 ms                                                       | 123 ms: 1.15x faster                                                       |
| xml_etree_iterparse        | 94.9 ms                                                      | 86.4 ms: 1.10x faster                                                      |
| spectral_norm              | 111 ms                                                       | 101 ms: 1.10x faster                                                       |
| sqlite_synth               | 2.21 us                                                      | 2.01 us: 1.10x faster                                                      |
| regex_effbot               | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                      |
| bpe_tokeniser              | 4.45 sec                                                     | 4.17 sec: 1.07x faster                                                     |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.06x faster                                                      |
| logging_silent             | 103 ns                                                       | 97.3 ns: 1.05x faster                                                      |
| pyflate                    | 449 ms                                                       | 427 ms: 1.05x faster                                                       |
| regex_v8                   | 22.7 ms                                                      | 21.7 ms: 1.05x faster                                                      |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                       |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                       |
| deepcopy_reduce            | 3.11 us                                                      | 3.06 us: 1.02x faster                                                      |
| regex_dna                  | 180 ms                                                       | 179 ms: 1.00x faster                                                       |
| pidigits                   | 217 ms                                                       | 217 ms: 1.00x slower                                                       |
| json_dumps                 | 10.5 ms                                                      | 10.9 ms: 1.03x slower                                                      |
| coroutines                 | 23.6 ms                                                      | 24.5 ms: 1.04x slower                                                      |
| pprint_safe_repr           | 738 ms                                                       | 777 ms: 1.05x slower                                                       |
| dulwich_log                | 74.8 ms                                                      | 79.4 ms: 1.06x slower                                                      |
| xml_etree_generate         | 85.4 ms                                                      | 90.7 ms: 1.06x slower                                                      |
| pylint                     | 317 ms                                                       | 337 ms: 1.06x slower                                                       |
| json                       | 4.93 ms                                                      | 5.28 ms: 1.07x slower                                                      |
| pycparser                  | 1.12 sec                                                     | 1.21 sec: 1.08x slower                                                     |
| generators                 | 28.8 ms                                                      | 31.1 ms: 1.08x slower                                                      |
| xml_etree_process          | 59.3 ms                                                      | 64.5 ms: 1.09x slower                                                      |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.12 ms: 1.09x slower                                                      |
| scimark_lu                 | 113 ms                                                       | 124 ms: 1.10x slower                                                       |
| scimark_monte_carlo        | 65.4 ms                                                      | 71.9 ms: 1.10x slower                                                      |
| 2to3                       | 260 ms                                                       | 286 ms: 1.10x slower                                                       |
| html5lib                   | 67.0 ms                                                      | 74.0 ms: 1.10x slower                                                      |
| pprint_pformat             | 1.50 sec                                                     | 1.66 sec: 1.11x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 3.48 ms: 1.12x slower                                                      |
| regex_compile              | 132 ms                                                       | 149 ms: 1.13x slower                                                       |
| meteor_contest             | 102 ms                                                       | 115 ms: 1.13x slower                                                       |
| logging_simple             | 6.16 us                                                      | 6.98 us: 1.13x slower                                                      |
| chaos                      | 57.3 ms                                                      | 65.0 ms: 1.13x slower                                                      |
| fannkuch                   | 370 ms                                                       | 420 ms: 1.14x slower                                                       |
| pickle_pure_python         | 294 us                                                       | 335 us: 1.14x slower                                                       |
| create_gc_cycles           | 1.34 ms                                                      | 1.52 ms: 1.14x slower                                                      |
| thrift                     | 778 us                                                       | 889 us: 1.14x slower                                                       |
| comprehensions             | 16.5 us                                                      | 19.1 us: 1.16x slower                                                      |
| logging_format             | 6.84 us                                                      | 7.94 us: 1.16x slower                                                      |
| json_loads                 | 27.0 us                                                      | 31.5 us: 1.17x slower                                                      |
| nqueens                    | 78.6 ms                                                      | 95.2 ms: 1.21x slower                                                      |
| sympy_integrate            | 19.8 ms                                                      | 24.1 ms: 1.22x slower                                                      |
| nbody                      | 85.1 ms                                                      | 105 ms: 1.24x slower                                                       |
| django_template            | 34.1 ms                                                      | 42.4 ms: 1.24x slower                                                      |
| hexiom                     | 5.99 ms                                                      | 7.54 ms: 1.26x slower                                                      |
| mako                       | 11.3 ms                                                      | 14.3 ms: 1.26x slower                                                      |
| typing_runtime_protocols   | 155 us                                                       | 196 us: 1.27x slower                                                       |
| crypto_pyaes               | 67.9 ms                                                      | 85.9 ms: 1.27x slower                                                      |
| python_startup_no_site     | 7.39 ms                                                      | 9.51 ms: 1.29x slower                                                      |
| sympy_sum                  | 156 ms                                                       | 200 ms: 1.29x slower                                                       |
| raytrace                   | 253 ms                                                       | 326 ms: 1.29x slower                                                       |
| sympy_expand               | 457 ms                                                       | 595 ms: 1.30x slower                                                       |
| sympy_str                  | 275 ms                                                       | 367 ms: 1.34x slower                                                       |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.34x slower                                                       |
| genshi_text                | 21.5 ms                                                      | 28.9 ms: 1.34x slower                                                      |
| genshi_xml                 | 48.8 ms                                                      | 69.8 ms: 1.43x slower                                                      |
| python_startup             | 11.0 ms                                                      | 15.9 ms: 1.45x slower                                                      |
| bench_mp_pool              | 11.0 ms                                                      | 16.2 ms: 1.47x slower                                                      |
| bench_thread_pool          | 919 us                                                       | 3.19 ms: 3.47x slower                                                      |
| telco                      | 7.82 ms                                                      | 181 ms: 23.12x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                               |

Benchmark hidden because not significant (2): unpickle_pure_python, tomli_loads
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_generators, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, docutils, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (7) of results/bm-20251116-3.15.0a1+-afae648-JIT,NOGIL/bm-20251116-vultr-x86_64-Fidget%2dSpinner-jit_Ft_llvm_19-3.15.0a1+-afae648.json: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.048x slower

# HPT report

- Reliability score: 82.22% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.42x