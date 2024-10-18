# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 2e950e3
- commit date: 2024-10-18
- overall geometric mean: 1.01x slower
- HPT reliability: 93.31%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                   |
| docutils       | 2.62 sec                                                     | 2.59 sec: 1.01x faster                                 |
| html5lib       | 67.0 ms                                                      | 63.0 ms: 1.06x faster                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| coroutines       | 23.6 ms                                                      | 22.3 ms: 1.06x faster                                  |
| async_generators | 377 ms                                                       | 369 ms: 1.02x faster                                   |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                 |
| Geometric mean   | (ref)                                                        | 1.02x faster                                           |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                   |
| float          | 77.5 ms                                                      | 78.1 ms: 1.01x slower                                  |
| nbody          | 85.1 ms                                                      | 92.4 ms: 1.09x slower                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 129 ms: 1.02x faster                                   |
| regex_dna      | 180 ms                                                       | 179 ms: 1.01x faster                                   |
| regex_v8       | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                  |
| regex_effbot   | 3.08 ms                                                      | 3.28 ms: 1.06x slower                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 26.1 us: 1.03x faster                                  |
| unpickle             | 14.3 us                                                      | 13.9 us: 1.03x faster                                  |
| unpickle_list        | 4.71 us                                                      | 4.58 us: 1.03x faster                                  |
| pickle_list          | 4.93 us                                                      | 4.84 us: 1.02x faster                                  |
| xml_etree_generate   | 85.4 ms                                                      | 84.8 ms: 1.01x faster                                  |
| xml_etree_process    | 59.3 ms                                                      | 59.1 ms: 1.00x faster                                  |
| pickle_dict          | 32.5 us                                                      | 32.7 us: 1.00x slower                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 96.1 ms: 1.01x slower                                  |
| unpickle_pure_python | 210 us                                                       | 215 us: 1.02x slower                                   |
| pickle_pure_python   | 294 us                                                       | 305 us: 1.04x slower                                   |
| tomli_loads          | 2.01 sec                                                     | 2.09 sec: 1.04x slower                                 |
| json_dumps           | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                  |
| Geometric mean       | (ref)                                                        | 1.01x slower                                           |

Benchmark hidden because not significant (2): pickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.41 ms: 1.00x slower                                  |
| python_startup         | 11.0 ms                                                      | 11.0 ms: 1.00x slower                                  |
| Geometric mean         | (ref)                                                        | 1.00x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                  |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                  |
| genshi_text     | 21.5 ms                                                      | 22.4 ms: 1.04x slower                                  |
| django_template | 34.1 ms                                                      | 35.8 ms: 1.05x slower                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                           |

All benchmarks:
===============

| Benchmark               | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|-------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| deepcopy                | 355 us                                                       | 262 us: 1.36x faster                                   |
| deepcopy_memo           | 39.1 us                                                      | 30.0 us: 1.30x faster                                  |
| go                      | 141 ms                                                       | 119 ms: 1.19x faster                                   |
| deepcopy_reduce         | 3.11 us                                                      | 2.65 us: 1.17x faster                                  |
| pidigits                | 217 ms                                                       | 185 ms: 1.17x faster                                   |
| scimark_sparse_mat_mult | 4.71 ms                                                      | 4.38 ms: 1.08x faster                                  |
| telco                   | 7.82 ms                                                      | 7.32 ms: 1.07x faster                                  |
| html5lib                | 67.0 ms                                                      | 63.0 ms: 1.06x faster                                  |
| coroutines              | 23.6 ms                                                      | 22.3 ms: 1.06x faster                                  |
| scimark_fft             | 349 ms                                                       | 333 ms: 1.05x faster                                   |
| pprint_safe_repr        | 738 ms                                                       | 709 ms: 1.04x faster                                   |
| pathlib                 | 19.2 ms                                                      | 18.5 ms: 1.04x faster                                  |
| json_loads              | 27.0 us                                                      | 26.1 us: 1.03x faster                                  |
| unpickle                | 14.3 us                                                      | 13.9 us: 1.03x faster                                  |
| unpickle_list           | 4.71 us                                                      | 4.58 us: 1.03x faster                                  |
| scimark_lu              | 113 ms                                                       | 109 ms: 1.03x faster                                   |
| 2to3                    | 260 ms                                                       | 253 ms: 1.03x faster                                   |
| thrift                  | 778 us                                                       | 759 us: 1.03x faster                                   |
| bpe_tokeniser           | 4.45 sec                                                     | 4.34 sec: 1.02x faster                                 |
| regex_compile           | 132 ms                                                       | 129 ms: 1.02x faster                                   |
| async_generators        | 377 ms                                                       | 369 ms: 1.02x faster                                   |
| logging_simple          | 6.16 us                                                      | 6.02 us: 1.02x faster                                  |
| crypto_pyaes            | 67.9 ms                                                      | 66.4 ms: 1.02x faster                                  |
| spectral_norm           | 111 ms                                                       | 109 ms: 1.02x faster                                   |
| json                    | 4.93 ms                                                      | 4.83 ms: 1.02x faster                                  |
| pprint_pformat          | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                 |
| hexiom                  | 5.99 ms                                                      | 5.88 ms: 1.02x faster                                  |
| logging_format          | 6.84 us                                                      | 6.72 us: 1.02x faster                                  |
| pickle_list             | 4.93 us                                                      | 4.84 us: 1.02x faster                                  |
| richards_super          | 51.6 ms                                                      | 50.9 ms: 1.01x faster                                  |
| sympy_sum               | 156 ms                                                       | 154 ms: 1.01x faster                                   |
| coverage                | 83.0 ms                                                      | 82.2 ms: 1.01x faster                                  |
| docutils                | 2.62 sec                                                     | 2.59 sec: 1.01x faster                                 |
| scimark_monte_carlo     | 65.4 ms                                                      | 64.8 ms: 1.01x faster                                  |
| scimark_sor             | 134 ms                                                       | 133 ms: 1.01x faster                                   |
| mdp                     | 2.36 sec                                                     | 2.34 sec: 1.01x faster                                 |
| xml_etree_generate      | 85.4 ms                                                      | 84.8 ms: 1.01x faster                                  |
| dulwich_log             | 74.8 ms                                                      | 74.3 ms: 1.01x faster                                  |
| sympy_str               | 275 ms                                                       | 273 ms: 1.01x faster                                   |
| regex_dna               | 180 ms                                                       | 179 ms: 1.01x faster                                   |
| xml_etree_process       | 59.3 ms                                                      | 59.1 ms: 1.00x faster                                  |
| python_startup_no_site  | 7.39 ms                                                      | 7.41 ms: 1.00x slower                                  |
| python_startup          | 11.0 ms                                                      | 11.0 ms: 1.00x slower                                  |
| pycparser               | 1.12 sec                                                     | 1.12 sec: 1.00x slower                                 |
| pickle_dict             | 32.5 us                                                      | 32.7 us: 1.00x slower                                  |
| meteor_contest          | 102 ms                                                       | 102 ms: 1.01x slower                                   |
| asyncio_tcp_ssl         | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                 |
| sqlglot_normalize       | 106 ms                                                       | 106 ms: 1.01x slower                                   |
| sympy_integrate         | 19.8 ms                                                      | 20.0 ms: 1.01x slower                                  |
| float                   | 77.5 ms                                                      | 78.1 ms: 1.01x slower                                  |
| xml_etree_iterparse     | 94.9 ms                                                      | 96.1 ms: 1.01x slower                                  |
| sqlglot_optimize        | 52.7 ms                                                      | 53.6 ms: 1.02x slower                                  |
| unpack_sequence         | 44.8 ns                                                      | 45.6 ns: 1.02x slower                                  |
| regex_v8                | 22.7 ms                                                      | 23.1 ms: 1.02x slower                                  |
| sqlglot_transpile       | 1.56 ms                                                      | 1.59 ms: 1.02x slower                                  |
| genshi_xml              | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                  |
| unpickle_pure_python    | 210 us                                                       | 215 us: 1.02x slower                                   |
| logging_silent          | 103 ns                                                       | 105 ns: 1.02x slower                                   |
| fannkuch                | 370 ms                                                       | 379 ms: 1.03x slower                                   |
| raytrace                | 253 ms                                                       | 259 ms: 1.03x slower                                   |
| chaos                   | 57.3 ms                                                      | 58.8 ms: 1.03x slower                                  |
| mako                    | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                  |
| comprehensions          | 16.5 us                                                      | 16.9 us: 1.03x slower                                  |
| deltablue               | 3.12 ms                                                      | 3.22 ms: 1.03x slower                                  |
| create_gc_cycles        | 1.34 ms                                                      | 1.38 ms: 1.03x slower                                  |
| sqlglot_parse           | 1.25 ms                                                      | 1.29 ms: 1.03x slower                                  |
| pickle_pure_python      | 294 us                                                       | 305 us: 1.04x slower                                   |
| genshi_text             | 21.5 ms                                                      | 22.4 ms: 1.04x slower                                  |
| tomli_loads             | 2.01 sec                                                     | 2.09 sec: 1.04x slower                                 |
| gc_traversal            | 3.14 ms                                                      | 3.28 ms: 1.04x slower                                  |
| django_template         | 34.1 ms                                                      | 35.8 ms: 1.05x slower                                  |
| regex_effbot            | 3.08 ms                                                      | 3.28 ms: 1.06x slower                                  |
| nbody                   | 85.1 ms                                                      | 92.4 ms: 1.09x slower                                  |
| bench_thread_pool       | 919 us                                                       | 1.01 ms: 1.10x slower                                  |
| json_dumps              | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                  |
| bench_mp_pool           | 11.0 ms                                                      | 63.3 ms: 5.76x slower                                  |
| Geometric mean          | (ref)                                                        | 1.01x slower                                           |

Benchmark hidden because not significant (13): asyncio_tcp, tornado_http, pickle, nqueens, richards, asyncio_websockets, xml_etree_parse, generators, sympy_expand, pylint, pyflate, typing_runtime_protocols, sqlite_synth
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 93.31% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x