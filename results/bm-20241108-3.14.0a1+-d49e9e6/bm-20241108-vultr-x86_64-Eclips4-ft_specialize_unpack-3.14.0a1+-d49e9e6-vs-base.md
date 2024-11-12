# Results vs. base

- fork: Eclips4
- ref: ft_specialize_unpack
- machine: linux-x86_64
- commit hash: d49e9e6
- commit date: 2024-11-08
- overall geometric mean: 1.00x faster
- HPT reliability: 93.71%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 2.60 sec                                                               | 2.61 sec: 1.00x slower                                                  |
| html5lib       | 65.1 ms                                                                | 66.2 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_generators | 369 ms                                                                 | 366 ms: 1.01x faster                                                    |
| coroutines       | 23.2 ms                                                                | 23.3 ms: 1.01x slower                                                   |
| Geometric mean   | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (3): asyncio_tcp_ssl, asyncio_websockets, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 79.9 ms                                                                | 78.1 ms: 1.02x faster                                                   |
| pidigits       | 224 ms                                                                 | 224 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 186 ms                                                                 | 183 ms: 1.02x faster                                                    |
| regex_compile  | 131 ms                                                                 | 129 ms: 1.02x faster                                                    |
| regex_effbot   | 3.07 ms                                                                | 3.35 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_loads           | 26.5 us                                                                | 26.0 us: 1.02x faster                                                   |
| unpickle_pure_python | 216 us                                                                 | 214 us: 1.01x faster                                                    |
| pickle_pure_python   | 319 us                                                                 | 317 us: 1.01x faster                                                    |
| pickle_dict          | 32.4 us                                                                | 32.2 us: 1.00x faster                                                   |
| json_dumps           | 11.5 ms                                                                | 11.6 ms: 1.00x slower                                                   |
| xml_etree_process    | 59.1 ms                                                                | 59.5 ms: 1.01x slower                                                   |
| tomli_loads          | 2.09 sec                                                               | 2.11 sec: 1.01x slower                                                  |
| xml_etree_parse      | 135 ms                                                                 | 137 ms: 1.01x slower                                                    |
| unpickle             | 13.8 us                                                                | 14.0 us: 1.02x slower                                                   |
| xml_etree_generate   | 84.3 ms                                                                | 85.9 ms: 1.02x slower                                                   |
| pickle               | 12.3 us                                                                | 12.6 us: 1.03x slower                                                   |
| unpickle_list        | 4.85 us                                                                | 4.99 us: 1.03x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (2): pickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 11.1 ms                                                                | 11.1 ms: 1.00x faster                                                   |
| python_startup_no_site | 7.49 ms                                                                | 7.48 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 22.6 ms                                                                | 22.3 ms: 1.01x faster                                                   |
| django_template | 35.4 ms                                                                | 34.9 ms: 1.01x faster                                                   |
| mako            | 11.7 ms                                                                | 11.8 ms: 1.00x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark               | bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1+-85036c8 | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|-------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| unpack_sequence         | 51.1 ns                                                                | 45.5 ns: 1.12x faster                                                   |
| gc_traversal            | 3.46 ms                                                                | 3.25 ms: 1.06x faster                                                   |
| logging_silent          | 106 ns                                                                 | 103 ns: 1.03x faster                                                    |
| float                   | 79.9 ms                                                                | 78.1 ms: 1.02x faster                                                   |
| deepcopy_memo           | 30.6 us                                                                | 29.9 us: 1.02x faster                                                   |
| regex_dna               | 186 ms                                                                 | 183 ms: 1.02x faster                                                    |
| json_loads              | 26.5 us                                                                | 26.0 us: 1.02x faster                                                   |
| raytrace                | 263 ms                                                                 | 259 ms: 1.02x faster                                                    |
| regex_compile           | 131 ms                                                                 | 129 ms: 1.02x faster                                                    |
| genshi_text             | 22.6 ms                                                                | 22.3 ms: 1.01x faster                                                   |
| telco                   | 7.52 ms                                                                | 7.43 ms: 1.01x faster                                                   |
| scimark_sor             | 135 ms                                                                 | 133 ms: 1.01x faster                                                    |
| django_template         | 35.4 ms                                                                | 34.9 ms: 1.01x faster                                                   |
| deltablue               | 3.25 ms                                                                | 3.21 ms: 1.01x faster                                                   |
| sqlglot_parse           | 1.30 ms                                                                | 1.28 ms: 1.01x faster                                                   |
| unpickle_pure_python    | 216 us                                                                 | 214 us: 1.01x faster                                                    |
| go                      | 122 ms                                                                 | 121 ms: 1.01x faster                                                    |
| pyflate                 | 449 ms                                                                 | 445 ms: 1.01x faster                                                    |
| deepcopy_reduce         | 2.64 us                                                                | 2.61 us: 1.01x faster                                                   |
| mdp                     | 2.37 sec                                                               | 2.35 sec: 1.01x faster                                                  |
| async_generators        | 369 ms                                                                 | 366 ms: 1.01x faster                                                    |
| sqlglot_transpile       | 1.59 ms                                                                | 1.58 ms: 1.01x faster                                                   |
| deepcopy                | 264 us                                                                 | 262 us: 1.01x faster                                                    |
| pprint_pformat          | 1.46 sec                                                               | 1.46 sec: 1.01x faster                                                  |
| richards_super          | 51.8 ms                                                                | 51.5 ms: 1.01x faster                                                   |
| richards                | 45.9 ms                                                                | 45.6 ms: 1.01x faster                                                   |
| pickle_pure_python      | 319 us                                                                 | 317 us: 1.01x faster                                                    |
| pprint_safe_repr        | 707 ms                                                                 | 704 ms: 1.00x faster                                                    |
| pickle_dict             | 32.4 us                                                                | 32.2 us: 1.00x faster                                                   |
| pidigits                | 224 ms                                                                 | 224 ms: 1.00x faster                                                    |
| python_startup          | 11.1 ms                                                                | 11.1 ms: 1.00x faster                                                   |
| python_startup_no_site  | 7.49 ms                                                                | 7.48 ms: 1.00x faster                                                   |
| coverage                | 81.1 ms                                                                | 81.3 ms: 1.00x slower                                                   |
| crypto_pyaes            | 66.7 ms                                                                | 66.9 ms: 1.00x slower                                                   |
| mako                    | 11.7 ms                                                                | 11.8 ms: 1.00x slower                                                   |
| docutils                | 2.60 sec                                                               | 2.61 sec: 1.00x slower                                                  |
| json_dumps              | 11.5 ms                                                                | 11.6 ms: 1.00x slower                                                   |
| xml_etree_process       | 59.1 ms                                                                | 59.5 ms: 1.01x slower                                                   |
| coroutines              | 23.2 ms                                                                | 23.3 ms: 1.01x slower                                                   |
| hexiom                  | 5.92 ms                                                                | 5.97 ms: 1.01x slower                                                   |
| sympy_integrate         | 19.7 ms                                                                | 19.9 ms: 1.01x slower                                                   |
| bench_thread_pool       | 1.01 ms                                                                | 1.02 ms: 1.01x slower                                                   |
| tomli_loads             | 2.09 sec                                                               | 2.11 sec: 1.01x slower                                                  |
| xml_etree_parse         | 135 ms                                                                 | 137 ms: 1.01x slower                                                    |
| sympy_sum               | 152 ms                                                                 | 154 ms: 1.01x slower                                                    |
| logging_format          | 6.67 us                                                                | 6.77 us: 1.01x slower                                                   |
| html5lib                | 65.1 ms                                                                | 66.2 ms: 1.02x slower                                                   |
| generators              | 28.8 ms                                                                | 29.3 ms: 1.02x slower                                                   |
| unpickle                | 13.8 us                                                                | 14.0 us: 1.02x slower                                                   |
| xml_etree_generate      | 84.3 ms                                                                | 85.9 ms: 1.02x slower                                                   |
| sqlite_synth            | 2.19 us                                                                | 2.24 us: 1.02x slower                                                   |
| fannkuch                | 369 ms                                                                 | 377 ms: 1.02x slower                                                    |
| pickle                  | 12.3 us                                                                | 12.6 us: 1.03x slower                                                   |
| unpickle_list           | 4.85 us                                                                | 4.99 us: 1.03x slower                                                   |
| spectral_norm           | 109 ms                                                                 | 113 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult | 4.50 ms                                                                | 4.66 ms: 1.03x slower                                                   |
| regex_effbot            | 3.07 ms                                                                | 3.35 ms: 1.09x slower                                                   |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (31): genshi_xml, pathlib, pylint, bench_mp_pool, scimark_monte_carlo, create_gc_cycles, pycparser, sqlglot_optimize, sqlglot_normalize, asyncio_tcp_ssl, chaos, json, pickle_list, typing_runtime_protocols, meteor_contest, dulwich_log, 2to3, bpe_tokeniser, asyncio_websockets, sympy_str, nbody, xml_etree_iterparse, asyncio_tcp, nqueens, logging_simple, thrift, sympy_expand, scimark_fft, scimark_lu, regex_v8, comprehensions

# HPT report

- Reliability score: 93.71% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x