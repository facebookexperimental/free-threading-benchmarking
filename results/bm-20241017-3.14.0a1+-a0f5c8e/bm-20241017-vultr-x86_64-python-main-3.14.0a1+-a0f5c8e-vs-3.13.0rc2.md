# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a0f5c8e
- commit date: 2024-10-17
- overall geometric mean: 1.01x slower
- HPT reliability: 52.04%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                   |
| docutils       | 2.62 sec                                                     | 2.59 sec: 1.01x faster                                 |
| html5lib       | 67.0 ms                                                      | 62.7 ms: 1.07x faster                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| coroutines       | 23.6 ms                                                      | 22.4 ms: 1.05x faster                                  |
| async_generators | 377 ms                                                       | 371 ms: 1.02x faster                                   |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                 |
| Geometric mean   | (ref)                                                        | 1.01x faster                                           |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                   |
| float          | 77.5 ms                                                      | 78.3 ms: 1.01x slower                                  |
| nbody          | 85.1 ms                                                      | 92.4 ms: 1.09x slower                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| regex_dna      | 180 ms                                                       | 174 ms: 1.04x faster                                   |
| regex_effbot   | 3.08 ms                                                      | 2.98 ms: 1.03x faster                                  |
| regex_compile  | 132 ms                                                       | 129 ms: 1.02x faster                                   |
| regex_v8       | 22.7 ms                                                      | 23.0 ms: 1.01x slower                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| unpickle             | 14.3 us                                                      | 13.5 us: 1.06x faster                                  |
| pickle_dict          | 32.5 us                                                      | 31.3 us: 1.04x faster                                  |
| json_loads           | 27.0 us                                                      | 26.1 us: 1.03x faster                                  |
| xml_etree_parse      | 136 ms                                                       | 135 ms: 1.01x faster                                   |
| pickle_list          | 4.93 us                                                      | 4.90 us: 1.01x faster                                  |
| xml_etree_process    | 59.3 ms                                                      | 59.0 ms: 1.01x faster                                  |
| pickle               | 11.3 us                                                      | 11.6 us: 1.02x slower                                  |
| unpickle_list        | 4.71 us                                                      | 4.85 us: 1.03x slower                                  |
| unpickle_pure_python | 210 us                                                       | 217 us: 1.03x slower                                   |
| pickle_pure_python   | 294 us                                                       | 307 us: 1.04x slower                                   |
| tomli_loads          | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                 |
| json_dumps           | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                  |
| Geometric mean       | (ref)                                                        | 1.01x slower                                           |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 11.0 ms                                                      | 11.1 ms: 1.01x slower                                  |
| python_startup_no_site | 7.39 ms                                                      | 7.45 ms: 1.01x slower                                  |
| Geometric mean         | (ref)                                                        | 1.01x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                  |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                  |
| genshi_text     | 21.5 ms                                                      | 22.2 ms: 1.03x slower                                  |
| django_template | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                  |
| Geometric mean  | (ref)                                                        | 1.03x slower                                           |

All benchmarks:
===============

| Benchmark               | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241017-vultr-x86_64-python-main-3.14.0a1+-a0f5c8e |
|-------------------------|:------------------------------------------------------------:|:------------------------------------------------------:|
| deepcopy                | 355 us                                                       | 263 us: 1.35x faster                                   |
| deepcopy_memo           | 39.1 us                                                      | 30.6 us: 1.28x faster                                  |
| deepcopy_reduce         | 3.11 us                                                      | 2.65 us: 1.17x faster                                  |
| pidigits                | 217 ms                                                       | 185 ms: 1.17x faster                                   |
| go                      | 141 ms                                                       | 121 ms: 1.16x faster                                   |
| html5lib                | 67.0 ms                                                      | 62.7 ms: 1.07x faster                                  |
| unpickle                | 14.3 us                                                      | 13.5 us: 1.06x faster                                  |
| telco                   | 7.82 ms                                                      | 7.37 ms: 1.06x faster                                  |
| scimark_sparse_mat_mult | 4.71 ms                                                      | 4.46 ms: 1.06x faster                                  |
| coroutines              | 23.6 ms                                                      | 22.4 ms: 1.05x faster                                  |
| pathlib                 | 19.2 ms                                                      | 18.3 ms: 1.05x faster                                  |
| unpack_sequence         | 44.8 ns                                                      | 42.7 ns: 1.05x faster                                  |
| pickle_dict             | 32.5 us                                                      | 31.3 us: 1.04x faster                                  |
| regex_dna               | 180 ms                                                       | 174 ms: 1.04x faster                                   |
| regex_effbot            | 3.08 ms                                                      | 2.98 ms: 1.03x faster                                  |
| json_loads              | 27.0 us                                                      | 26.1 us: 1.03x faster                                  |
| pprint_safe_repr        | 738 ms                                                       | 714 ms: 1.03x faster                                   |
| scimark_fft             | 349 ms                                                       | 340 ms: 1.03x faster                                   |
| 2to3                    | 260 ms                                                       | 253 ms: 1.03x faster                                   |
| regex_compile           | 132 ms                                                       | 129 ms: 1.02x faster                                   |
| crypto_pyaes            | 67.9 ms                                                      | 66.3 ms: 1.02x faster                                  |
| thrift                  | 778 us                                                       | 763 us: 1.02x faster                                   |
| pprint_pformat          | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                 |
| async_generators        | 377 ms                                                       | 371 ms: 1.02x faster                                   |
| bpe_tokeniser           | 4.45 sec                                                     | 4.37 sec: 1.02x faster                                 |
| json                    | 4.93 ms                                                      | 4.85 ms: 1.02x faster                                  |
| generators              | 28.8 ms                                                      | 28.4 ms: 1.01x faster                                  |
| logging_simple          | 6.16 us                                                      | 6.07 us: 1.01x faster                                  |
| docutils                | 2.62 sec                                                     | 2.59 sec: 1.01x faster                                 |
| coverage                | 83.0 ms                                                      | 82.1 ms: 1.01x faster                                  |
| xml_etree_parse         | 136 ms                                                       | 135 ms: 1.01x faster                                   |
| dulwich_log             | 74.8 ms                                                      | 74.2 ms: 1.01x faster                                  |
| logging_format          | 6.84 us                                                      | 6.79 us: 1.01x faster                                  |
| pickle_list             | 4.93 us                                                      | 4.90 us: 1.01x faster                                  |
| sympy_sum               | 156 ms                                                       | 155 ms: 1.01x faster                                   |
| xml_etree_process       | 59.3 ms                                                      | 59.0 ms: 1.01x faster                                  |
| spectral_norm           | 111 ms                                                       | 111 ms: 1.00x slower                                   |
| pyflate                 | 449 ms                                                       | 451 ms: 1.01x slower                                   |
| asyncio_tcp_ssl         | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                 |
| python_startup          | 11.0 ms                                                      | 11.1 ms: 1.01x slower                                  |
| python_startup_no_site  | 7.39 ms                                                      | 7.45 ms: 1.01x slower                                  |
| richards_super          | 51.6 ms                                                      | 52.0 ms: 1.01x slower                                  |
| sympy_expand            | 457 ms                                                       | 460 ms: 1.01x slower                                   |
| sqlglot_normalize       | 106 ms                                                       | 107 ms: 1.01x slower                                   |
| scimark_sor             | 134 ms                                                       | 136 ms: 1.01x slower                                   |
| nqueens                 | 78.6 ms                                                      | 79.3 ms: 1.01x slower                                  |
| hexiom                  | 5.99 ms                                                      | 6.05 ms: 1.01x slower                                  |
| float                   | 77.5 ms                                                      | 78.3 ms: 1.01x slower                                  |
| sympy_integrate         | 19.8 ms                                                      | 20.1 ms: 1.01x slower                                  |
| scimark_monte_carlo     | 65.4 ms                                                      | 66.2 ms: 1.01x slower                                  |
| regex_v8                | 22.7 ms                                                      | 23.0 ms: 1.01x slower                                  |
| meteor_contest          | 102 ms                                                       | 103 ms: 1.02x slower                                   |
| sqlglot_optimize        | 52.7 ms                                                      | 53.6 ms: 1.02x slower                                  |
| sqlglot_transpile       | 1.56 ms                                                      | 1.59 ms: 1.02x slower                                  |
| richards                | 45.2 ms                                                      | 46.1 ms: 1.02x slower                                  |
| genshi_xml              | 48.8 ms                                                      | 49.7 ms: 1.02x slower                                  |
| fannkuch                | 370 ms                                                       | 377 ms: 1.02x slower                                   |
| comprehensions          | 16.5 us                                                      | 16.8 us: 1.02x slower                                  |
| pickle                  | 11.3 us                                                      | 11.6 us: 1.02x slower                                  |
| mako                    | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                  |
| deltablue               | 3.12 ms                                                      | 3.21 ms: 1.03x slower                                  |
| sqlglot_parse           | 1.25 ms                                                      | 1.28 ms: 1.03x slower                                  |
| logging_silent          | 103 ns                                                       | 106 ns: 1.03x slower                                   |
| unpickle_list           | 4.71 us                                                      | 4.85 us: 1.03x slower                                  |
| genshi_text             | 21.5 ms                                                      | 22.2 ms: 1.03x slower                                  |
| django_template         | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                  |
| chaos                   | 57.3 ms                                                      | 59.3 ms: 1.03x slower                                  |
| unpickle_pure_python    | 210 us                                                       | 217 us: 1.03x slower                                   |
| pickle_pure_python      | 294 us                                                       | 307 us: 1.04x slower                                   |
| tomli_loads             | 2.01 sec                                                     | 2.10 sec: 1.05x slower                                 |
| raytrace                | 253 ms                                                       | 265 ms: 1.05x slower                                   |
| gc_traversal            | 3.14 ms                                                      | 3.32 ms: 1.06x slower                                  |
| pycparser               | 1.12 sec                                                     | 1.20 sec: 1.07x slower                                 |
| nbody                   | 85.1 ms                                                      | 92.4 ms: 1.09x slower                                  |
| json_dumps              | 10.5 ms                                                      | 11.6 ms: 1.10x slower                                  |
| bench_thread_pool       | 919 us                                                       | 1.02 ms: 1.10x slower                                  |
| bench_mp_pool           | 11.0 ms                                                      | 64.1 ms: 5.83x slower                                  |
| Geometric mean          | (ref)                                                        | 1.01x slower                                           |

Benchmark hidden because not significant (12): sqlite_synth, xml_etree_generate, asyncio_tcp, tornado_http, mdp, sympy_str, asyncio_websockets, xml_etree_iterparse, scimark_lu, pylint, typing_runtime_protocols, create_gc_cycles
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 52.04% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x