# Results vs. 3.13.0rc2

- fork: python
- ref: ef4b69d2becf49daaea2
- machine: linux-x86_64
- commit hash: ef4b69d
- commit date: 2024-09-06
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 4.22 sec: 1.05x slower                                                |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization | 709 ms                                                       | 647 ms: 1.10x faster                                                  |
| async_tree_none        | 572 ms                                                       | 523 ms: 1.09x faster                                                  |
| async_tree_io_tg       | 1.40 sec                                                     | 1.33 sec: 1.06x faster                                                |
| async_generators       | 567 ms                                                       | 591 ms: 1.04x slower                                                  |
| asyncio_tcp_ssl        | 2.77 sec                                                     | 2.90 sec: 1.05x slower                                                |
| Geometric mean         | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (8): async_tree_memoization_tg, coroutines, async_tree_none_tg, async_tree_cpu_io_mixed, asyncio_websockets, asyncio_tcp, async_tree_io, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 116 ms                                                       | 125 ms: 1.08x slower                                                  |
| nbody          | 119 ms                                                       | 129 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 5.19 ms: 1.10x slower                                                 |
| regex_dna      | 282 ms                                                       | 310 ms: 1.10x slower                                                  |
| regex_v8       | 32.8 ms                                                      | 36.2 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|--------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_generate | 122 ms                                                       | 128 ms: 1.05x slower                                                  |
| pickle_list        | 6.86 us                                                      | 7.25 us: 1.06x slower                                                 |
| unpickle_list      | 6.68 us                                                      | 7.18 us: 1.07x slower                                                 |
| json_dumps         | 14.1 ms                                                      | 15.4 ms: 1.09x slower                                                 |
| xml_etree_parse    | 231 ms                                                       | 253 ms: 1.10x slower                                                  |
| json_loads         | 34.3 us                                                      | 37.8 us: 1.10x slower                                                 |
| Geometric mean     | (ref)                                                        | 1.04x slower                                                          |

Benchmark hidden because not significant (8): pickle_dict, tomli_loads, pickle_pure_python, unpickle, xml_etree_process, pickle, xml_etree_iterparse, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 17.7 ms: 1.16x slower                                                 |
| python_startup         | 22.4 ms                                                      | 26.1 ms: 1.16x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 44.3 ms                                                      | 46.7 ms: 1.05x slower                                                 |
| mako            | 15.9 ms                                                      | 18.5 ms: 1.16x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.05x slower                                                          |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|-------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| deepcopy                | 498 us                                                       | 362 us: 1.37x faster                                                  |
| deepcopy_memo           | 50.1 us                                                      | 39.5 us: 1.27x faster                                                 |
| go                      | 191 ms                                                       | 168 ms: 1.14x faster                                                  |
| scimark_sparse_mat_mult | 6.76 ms                                                      | 6.13 ms: 1.10x faster                                                 |
| async_tree_memoization  | 709 ms                                                       | 647 ms: 1.10x faster                                                  |
| async_tree_none         | 572 ms                                                       | 523 ms: 1.09x faster                                                  |
| async_tree_io_tg        | 1.40 sec                                                     | 1.33 sec: 1.06x faster                                                |
| telco                   | 12.2 ms                                                      | 11.5 ms: 1.06x faster                                                 |
| crypto_pyaes            | 100 ms                                                       | 95.7 ms: 1.05x faster                                                 |
| scimark_sor             | 179 ms                                                       | 172 ms: 1.04x faster                                                  |
| mdp                     | 3.80 sec                                                     | 3.93 sec: 1.03x slower                                                |
| raytrace                | 344 ms                                                       | 358 ms: 1.04x slower                                                  |
| async_generators        | 567 ms                                                       | 591 ms: 1.04x slower                                                  |
| xml_etree_generate      | 122 ms                                                       | 128 ms: 1.05x slower                                                  |
| asyncio_tcp_ssl         | 2.77 sec                                                     | 2.90 sec: 1.05x slower                                                |
| docutils                | 4.01 sec                                                     | 4.22 sec: 1.05x slower                                                |
| django_template         | 44.3 ms                                                      | 46.7 ms: 1.05x slower                                                 |
| sympy_expand            | 601 ms                                                       | 635 ms: 1.06x slower                                                  |
| pickle_list             | 6.86 us                                                      | 7.25 us: 1.06x slower                                                 |
| sqlglot_parse           | 1.76 ms                                                      | 1.87 ms: 1.06x slower                                                 |
| unpickle_list           | 6.68 us                                                      | 7.18 us: 1.07x slower                                                 |
| deltablue               | 4.44 ms                                                      | 4.79 ms: 1.08x slower                                                 |
| float                   | 116 ms                                                       | 125 ms: 1.08x slower                                                  |
| gc_traversal            | 5.70 ms                                                      | 6.19 ms: 1.09x slower                                                 |
| nbody                   | 119 ms                                                       | 129 ms: 1.09x slower                                                  |
| sqlglot_normalize       | 140 ms                                                       | 152 ms: 1.09x slower                                                  |
| json_dumps              | 14.1 ms                                                      | 15.4 ms: 1.09x slower                                                 |
| regex_effbot            | 4.74 ms                                                      | 5.19 ms: 1.10x slower                                                 |
| xml_etree_parse         | 231 ms                                                       | 253 ms: 1.10x slower                                                  |
| regex_dna               | 282 ms                                                       | 310 ms: 1.10x slower                                                  |
| logging_silent          | 130 ns                                                       | 143 ns: 1.10x slower                                                  |
| json                    | 6.51 ms                                                      | 7.18 ms: 1.10x slower                                                 |
| json_loads              | 34.3 us                                                      | 37.8 us: 1.10x slower                                                 |
| regex_v8                | 32.8 ms                                                      | 36.2 ms: 1.10x slower                                                 |
| pyflate                 | 664 ms                                                       | 735 ms: 1.11x slower                                                  |
| create_gc_cycles        | 2.41 ms                                                      | 2.70 ms: 1.12x slower                                                 |
| coverage                | 107 ms                                                       | 121 ms: 1.13x slower                                                  |
| hexiom                  | 8.11 ms                                                      | 9.21 ms: 1.14x slower                                                 |
| pycparser               | 1.57 sec                                                     | 1.79 sec: 1.14x slower                                                |
| dulwich_log             | 93.7 ms                                                      | 108 ms: 1.15x slower                                                  |
| python_startup_no_site  | 15.3 ms                                                      | 17.7 ms: 1.16x slower                                                 |
| mako                    | 15.9 ms                                                      | 18.5 ms: 1.16x slower                                                 |
| python_startup          | 22.4 ms                                                      | 26.1 ms: 1.16x slower                                                 |
| bench_thread_pool       | 2.89 ms                                                      | 3.89 ms: 1.35x slower                                                 |
| bench_mp_pool           | 18.7 ms                                                      | 26.6 ms: 1.42x slower                                                 |
| Geometric mean          | (ref)                                                        | 1.03x slower                                                          |

Benchmark hidden because not significant (52): async_tree_memoization_tg, coroutines, pickle_dict, richards_super, unpack_sequence, tomli_loads, async_tree_none_tg, genshi_text, scimark_monte_carlo, sympy_integrate, comprehensions, scimark_fft, deepcopy_reduce, chaos, genshi_xml, pickle_pure_python, logging_simple, async_tree_cpu_io_mixed, unpickle, sympy_sum, richards, sqlite_synth, pidigits, xml_etree_process, 2to3, pprint_safe_repr, scimark_lu, meteor_contest, nqueens, asyncio_websockets, bpe_tokeniser, html5lib, pathlib, typing_runtime_protocols, pprint_pformat, asyncio_tcp, pickle, spectral_norm, async_tree_io, sqlglot_optimize, generators, async_tree_cpu_io_mixed_tg, xml_etree_iterparse, unpickle_pure_python, fannkuch, regex_compile, sqlglot_transpile, tornado_http, logging_format, sympy_str, thrift, pylint
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.01x