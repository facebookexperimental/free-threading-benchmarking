# Results vs. 3.13.0rc2

- fork: python
- ref: acbd5c9c6c62dac34d2e
- machine: linux-x86_64
- commit hash: acbd5c9
- commit date: 2024-11-17
- overall geometric mean: 1.01x slower
- HPT reliability: 91.38%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.90 sec: 1.03x faster                                                 |
| html5lib       | 92.6 ms                                                      | 87.7 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_generators | 567 ms                                                       | 616 ms: 1.09x slower                                                   |
| Geometric mean   | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (4): asyncio_tcp, asyncio_websockets, asyncio_tcp_ssl, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 234 ms: 1.07x faster                                                   |
| nbody          | 119 ms                                                       | 132 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 182 ms                                                       | 173 ms: 1.05x faster                                                   |
| regex_dna      | 282 ms                                                       | 293 ms: 1.04x slower                                                   |
| regex_v8       | 32.8 ms                                                      | 34.9 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 162 ms: 1.09x faster                                                   |
| pickle_list          | 6.86 us                                                      | 7.19 us: 1.05x slower                                                  |
| pickle               | 15.1 us                                                      | 15.9 us: 1.05x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 439 us: 1.05x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 310 us: 1.07x slower                                                   |
| unpickle_list        | 6.68 us                                                      | 7.19 us: 1.08x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 15.8 ms: 1.12x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (7): pickle_dict, tomli_loads, unpickle, json_loads, xml_etree_process, xml_etree_generate, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 14.0 ms: 1.09x faster                                                  |
| python_startup         | 22.4 ms                                                      | 21.0 ms: 1.06x faster                                                  |
| Geometric mean         | (ref)                                                        | 1.08x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 67.6 ms: 1.07x faster                                                  |
| genshi_text     | 31.7 ms                                                      | 30.4 ms: 1.04x faster                                                  |
| mako            | 15.9 ms                                                      | 16.9 ms: 1.06x slower                                                  |
| django_template | 44.3 ms                                                      | 47.3 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark               | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                | 498 us                                                       | 388 us: 1.28x faster                                                   |
| unpack_sequence         | 74.3 ns                                                      | 63.1 ns: 1.18x faster                                                  |
| go                      | 191 ms                                                       | 162 ms: 1.18x faster                                                   |
| deepcopy_memo           | 50.1 us                                                      | 42.8 us: 1.17x faster                                                  |
| telco                   | 12.2 ms                                                      | 10.8 ms: 1.12x faster                                                  |
| pathlib                 | 29.9 ms                                                      | 26.9 ms: 1.11x faster                                                  |
| thrift                  | 1.10 ms                                                      | 1.00 ms: 1.09x faster                                                  |
| python_startup_no_site  | 15.3 ms                                                      | 14.0 ms: 1.09x faster                                                  |
| xml_etree_iterparse     | 177 ms                                                       | 162 ms: 1.09x faster                                                   |
| scimark_sparse_mat_mult | 6.76 ms                                                      | 6.19 ms: 1.09x faster                                                  |
| mdp                     | 3.80 sec                                                     | 3.52 sec: 1.08x faster                                                 |
| pidigits                | 251 ms                                                       | 234 ms: 1.07x faster                                                   |
| sympy_integrate         | 30.2 ms                                                      | 28.2 ms: 1.07x faster                                                  |
| genshi_xml              | 72.1 ms                                                      | 67.6 ms: 1.07x faster                                                  |
| pprint_safe_repr        | 987 ms                                                       | 926 ms: 1.07x faster                                                   |
| python_startup          | 22.4 ms                                                      | 21.0 ms: 1.06x faster                                                  |
| deepcopy_reduce         | 4.10 us                                                      | 3.87 us: 1.06x faster                                                  |
| html5lib                | 92.6 ms                                                      | 87.7 ms: 1.06x faster                                                  |
| nqueens                 | 112 ms                                                       | 106 ms: 1.06x faster                                                   |
| scimark_sor             | 179 ms                                                       | 169 ms: 1.05x faster                                                   |
| regex_compile           | 182 ms                                                       | 173 ms: 1.05x faster                                                   |
| bpe_tokeniser           | 6.28 sec                                                     | 5.98 sec: 1.05x faster                                                 |
| sqlglot_optimize        | 74.7 ms                                                      | 71.3 ms: 1.05x faster                                                  |
| genshi_text             | 31.7 ms                                                      | 30.4 ms: 1.04x faster                                                  |
| pprint_pformat          | 1.94 sec                                                     | 1.88 sec: 1.03x faster                                                 |
| docutils                | 4.01 sec                                                     | 3.90 sec: 1.03x faster                                                 |
| raytrace                | 344 ms                                                       | 354 ms: 1.03x slower                                                   |
| regex_dna               | 282 ms                                                       | 293 ms: 1.04x slower                                                   |
| pickle_list             | 6.86 us                                                      | 7.19 us: 1.05x slower                                                  |
| crypto_pyaes            | 100 ms                                                       | 105 ms: 1.05x slower                                                   |
| pickle                  | 15.1 us                                                      | 15.9 us: 1.05x slower                                                  |
| hexiom                  | 8.11 ms                                                      | 8.54 ms: 1.05x slower                                                  |
| pickle_pure_python      | 416 us                                                       | 439 us: 1.05x slower                                                   |
| mako                    | 15.9 ms                                                      | 16.9 ms: 1.06x slower                                                  |
| sqlglot_parse           | 1.76 ms                                                      | 1.87 ms: 1.06x slower                                                  |
| regex_v8                | 32.8 ms                                                      | 34.9 ms: 1.06x slower                                                  |
| generators              | 40.0 ms                                                      | 42.6 ms: 1.06x slower                                                  |
| unpickle_pure_python    | 290 us                                                       | 310 us: 1.07x slower                                                   |
| django_template         | 44.3 ms                                                      | 47.3 ms: 1.07x slower                                                  |
| dulwich_log             | 93.7 ms                                                      | 101 ms: 1.07x slower                                                   |
| deltablue               | 4.44 ms                                                      | 4.77 ms: 1.07x slower                                                  |
| unpickle_list           | 6.68 us                                                      | 7.19 us: 1.08x slower                                                  |
| sqlglot_transpile       | 2.20 ms                                                      | 2.38 ms: 1.08x slower                                                  |
| async_generators        | 567 ms                                                       | 616 ms: 1.09x slower                                                   |
| coverage                | 107 ms                                                       | 117 ms: 1.09x slower                                                   |
| logging_silent          | 130 ns                                                       | 143 ns: 1.10x slower                                                   |
| nbody                   | 119 ms                                                       | 132 ms: 1.11x slower                                                   |
| json_dumps              | 14.1 ms                                                      | 15.8 ms: 1.12x slower                                                  |
| bench_thread_pool       | 2.89 ms                                                      | 3.25 ms: 1.12x slower                                                  |
| bench_mp_pool           | 18.7 ms                                                      | 72.4 ms: 3.88x slower                                                  |
| Geometric mean          | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (38): typing_runtime_protocols, asyncio_tcp, pickle_dict, fannkuch, 2to3, richards, logging_format, spectral_norm, pycparser, tomli_loads, pylint, asyncio_websockets, unpickle, sympy_str, sympy_sum, float, json_loads, sqlite_synth, scimark_fft, richards_super, sympy_expand, create_gc_cycles, xml_etree_process, regex_effbot, gc_traversal, pyflate, asyncio_tcp_ssl, scimark_lu, xml_etree_generate, json, chaos, scimark_monte_carlo, sqlglot_normalize, meteor_contest, logging_simple, comprehensions, coroutines, xml_etree_parse
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 91.38% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x