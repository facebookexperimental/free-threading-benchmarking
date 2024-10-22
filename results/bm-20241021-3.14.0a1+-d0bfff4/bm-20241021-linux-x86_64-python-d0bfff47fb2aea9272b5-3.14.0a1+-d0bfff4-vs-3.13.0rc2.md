# Results vs. 3.13.0rc2

- fork: python
- ref: d0bfff47fb2aea9272b5
- machine: linux-x86_64
- commit hash: d0bfff4
- commit date: 2024-10-21
- overall geometric mean: 1.01x slower
- HPT reliability: 98.61%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| html5lib       | 92.6 ms                                                      | 87.3 ms: 1.06x faster                                                  |
| tornado_http   | 251 ms                                                       | 279 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (2): 2to3, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_generators | 567 ms                                                       | 588 ms: 1.04x slower                                                   |
| Geometric mean   | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (4): asyncio_websockets, asyncio_tcp_ssl, asyncio_tcp, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 119 ms                                                       | 124 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 34.5 ms: 1.05x slower                                                  |
| regex_effbot   | 4.74 ms                                                      | 5.00 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 158 ms: 1.12x faster                                                   |
| pickle_dict          | 47.2 us                                                      | 44.7 us: 1.06x faster                                                  |
| pickle_list          | 6.86 us                                                      | 6.51 us: 1.05x faster                                                  |
| tomli_loads          | 2.78 sec                                                     | 2.88 sec: 1.04x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 15.1 ms: 1.07x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 446 us: 1.07x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 331 us: 1.14x slower                                                   |
| unpickle_list        | 6.68 us                                                      | 7.63 us: 1.14x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (6): xml_etree_generate, xml_etree_parse, xml_etree_process, unpickle, json_loads, pickle

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.3 ms                                                      | 45.7 ms: 1.03x slower                                                  |
| mako            | 15.9 ms                                                      | 16.6 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark               | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|-------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                | 498 us                                                       | 366 us: 1.36x faster                                                   |
| deepcopy_memo           | 50.1 us                                                      | 40.2 us: 1.25x faster                                                  |
| go                      | 191 ms                                                       | 163 ms: 1.17x faster                                                   |
| deepcopy_reduce         | 4.10 us                                                      | 3.61 us: 1.14x faster                                                  |
| unpack_sequence         | 74.3 ns                                                      | 66.1 ns: 1.12x faster                                                  |
| xml_etree_iterparse     | 177 ms                                                       | 158 ms: 1.12x faster                                                   |
| richards                | 65.5 ms                                                      | 59.8 ms: 1.09x faster                                                  |
| telco                   | 12.2 ms                                                      | 11.2 ms: 1.09x faster                                                  |
| html5lib                | 92.6 ms                                                      | 87.3 ms: 1.06x faster                                                  |
| gc_traversal            | 5.70 ms                                                      | 5.38 ms: 1.06x faster                                                  |
| fannkuch                | 547 ms                                                       | 517 ms: 1.06x faster                                                   |
| pickle_dict             | 47.2 us                                                      | 44.7 us: 1.06x faster                                                  |
| pickle_list             | 6.86 us                                                      | 6.51 us: 1.05x faster                                                  |
| richards_super          | 73.2 ms                                                      | 69.4 ms: 1.05x faster                                                  |
| pathlib                 | 29.9 ms                                                      | 28.5 ms: 1.05x faster                                                  |
| crypto_pyaes            | 100 ms                                                       | 96.1 ms: 1.04x faster                                                  |
| pprint_safe_repr        | 987 ms                                                       | 949 ms: 1.04x faster                                                   |
| bpe_tokeniser           | 6.28 sec                                                     | 6.08 sec: 1.03x faster                                                 |
| logging_silent          | 130 ns                                                       | 133 ns: 1.03x slower                                                   |
| raytrace                | 344 ms                                                       | 354 ms: 1.03x slower                                                   |
| django_template         | 44.3 ms                                                      | 45.7 ms: 1.03x slower                                                  |
| tomli_loads             | 2.78 sec                                                     | 2.88 sec: 1.04x slower                                                 |
| async_generators        | 567 ms                                                       | 588 ms: 1.04x slower                                                   |
| mako                    | 15.9 ms                                                      | 16.6 ms: 1.04x slower                                                  |
| sqlglot_normalize       | 140 ms                                                       | 146 ms: 1.04x slower                                                   |
| nbody                   | 119 ms                                                       | 124 ms: 1.04x slower                                                   |
| mdp                     | 3.80 sec                                                     | 3.96 sec: 1.04x slower                                                 |
| regex_v8                | 32.8 ms                                                      | 34.5 ms: 1.05x slower                                                  |
| sqlglot_optimize        | 74.7 ms                                                      | 78.7 ms: 1.05x slower                                                  |
| regex_effbot            | 4.74 ms                                                      | 5.00 ms: 1.05x slower                                                  |
| scimark_lu              | 146 ms                                                       | 155 ms: 1.06x slower                                                   |
| json                    | 6.51 ms                                                      | 6.91 ms: 1.06x slower                                                  |
| coverage                | 107 ms                                                       | 115 ms: 1.07x slower                                                   |
| json_dumps              | 14.1 ms                                                      | 15.1 ms: 1.07x slower                                                  |
| hexiom                  | 8.11 ms                                                      | 8.67 ms: 1.07x slower                                                  |
| pickle_pure_python      | 416 us                                                       | 446 us: 1.07x slower                                                   |
| scimark_sparse_mat_mult | 6.76 ms                                                      | 7.24 ms: 1.07x slower                                                  |
| sqlglot_transpile       | 2.20 ms                                                      | 2.37 ms: 1.08x slower                                                  |
| tornado_http            | 251 ms                                                       | 279 ms: 1.11x slower                                                   |
| unpickle_pure_python    | 290 us                                                       | 331 us: 1.14x slower                                                   |
| unpickle_list           | 6.68 us                                                      | 7.63 us: 1.14x slower                                                  |
| bench_mp_pool           | 18.7 ms                                                      | 69.4 ms: 3.71x slower                                                  |
| Geometric mean          | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (47): float, sympy_str, meteor_contest, bench_thread_pool, xml_etree_generate, scimark_sor, typing_runtime_protocols, xml_etree_parse, regex_compile, xml_etree_process, generators, nqueens, genshi_xml, python_startup, 2to3, deltablue, python_startup_no_site, pycparser, unpickle, pidigits, chaos, thrift, dulwich_log, sympy_integrate, asyncio_websockets, spectral_norm, scimark_monte_carlo, create_gc_cycles, docutils, comprehensions, sqlglot_parse, pprint_pformat, pyflate, scimark_fft, logging_simple, asyncio_tcp_ssl, sympy_expand, asyncio_tcp, json_loads, sympy_sum, logging_format, pickle, coroutines, regex_dna, genshi_text, sqlite_synth, pylint
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 98.61% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x