# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: e051157
- commit date: 2024-11-18
- overall geometric mean: 1.00x slower
- HPT reliability: 98.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.60 sec                                                               | 2.62 sec: 1.01x slower                                                |
| html5lib       | 63.7 ms                                                                | 65.3 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_generators | 383 ms                                                                 | 378 ms: 1.01x faster                                                  |
| Geometric mean   | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (4): coroutines, asyncio_websockets, asyncio_tcp_ssl, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 96.2 ms                                                                | 92.5 ms: 1.04x faster                                                 |
| float          | 78.6 ms                                                                | 79.2 ms: 1.01x slower                                                 |
| pidigits       | 186 ms                                                                 | 223 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 23.1 ms                                                                | 22.9 ms: 1.01x faster                                                 |
| regex_compile  | 131 ms                                                                 | 130 ms: 1.01x faster                                                  |
| regex_effbot   | 3.28 ms                                                                | 3.27 ms: 1.00x faster                                                 |
| regex_dna      | 181 ms                                                                 | 183 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 33.7 us                                                                | 32.3 us: 1.04x faster                                                 |
| pickle_list          | 5.28 us                                                                | 5.13 us: 1.03x faster                                                 |
| xml_etree_generate   | 86.1 ms                                                                | 84.5 ms: 1.02x faster                                                 |
| xml_etree_process    | 60.0 ms                                                                | 59.0 ms: 1.02x faster                                                 |
| json_dumps           | 11.5 ms                                                                | 11.5 ms: 1.01x faster                                                 |
| json_loads           | 25.1 us                                                                | 24.9 us: 1.01x faster                                                 |
| pickle_pure_python   | 315 us                                                                 | 314 us: 1.00x faster                                                  |
| unpickle_pure_python | 215 us                                                                 | 215 us: 1.00x slower                                                  |
| unpickle_list        | 4.73 us                                                                | 4.75 us: 1.00x slower                                                 |
| xml_etree_parse      | 136 ms                                                                 | 137 ms: 1.01x slower                                                  |
| xml_etree_iterparse  | 95.5 ms                                                                | 96.1 ms: 1.01x slower                                                 |
| pickle               | 12.2 us                                                                | 12.3 us: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): tomli_loads, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.1 ms                                                                | 11.2 ms: 1.01x slower                                                 |
| python_startup_no_site | 7.46 ms                                                                | 7.51 ms: 1.01x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako           | 11.9 ms                                                                | 11.6 ms: 1.02x faster                                                 |
| genshi_xml     | 50.8 ms                                                                | 50.3 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): django_template, genshi_text

All benchmarks:
===============

| Benchmark               | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict             | 33.7 us                                                                | 32.3 us: 1.04x faster                                                 |
| nbody                   | 96.2 ms                                                                | 92.5 ms: 1.04x faster                                                 |
| logging_silent          | 106 ns                                                                 | 103 ns: 1.03x faster                                                  |
| pickle_list             | 5.28 us                                                                | 5.13 us: 1.03x faster                                                 |
| deepcopy_memo           | 30.3 us                                                                | 29.6 us: 1.02x faster                                                 |
| mako                    | 11.9 ms                                                                | 11.6 ms: 1.02x faster                                                 |
| xml_etree_generate      | 86.1 ms                                                                | 84.5 ms: 1.02x faster                                                 |
| comprehensions          | 17.3 us                                                                | 17.0 us: 1.02x faster                                                 |
| xml_etree_process       | 60.0 ms                                                                | 59.0 ms: 1.02x faster                                                 |
| deltablue               | 3.27 ms                                                                | 3.22 ms: 1.02x faster                                                 |
| deepcopy_reduce         | 2.69 us                                                                | 2.66 us: 1.01x faster                                                 |
| async_generators        | 383 ms                                                                 | 378 ms: 1.01x faster                                                  |
| json                    | 4.66 ms                                                                | 4.60 ms: 1.01x faster                                                 |
| genshi_xml              | 50.8 ms                                                                | 50.3 ms: 1.01x faster                                                 |
| generators              | 29.3 ms                                                                | 28.9 ms: 1.01x faster                                                 |
| regex_v8                | 23.1 ms                                                                | 22.9 ms: 1.01x faster                                                 |
| thrift                  | 752 us                                                                 | 747 us: 1.01x faster                                                  |
| regex_compile           | 131 ms                                                                 | 130 ms: 1.01x faster                                                  |
| json_dumps              | 11.5 ms                                                                | 11.5 ms: 1.01x faster                                                 |
| json_loads              | 25.1 us                                                                | 24.9 us: 1.01x faster                                                 |
| chaos                   | 58.9 ms                                                                | 58.6 ms: 1.01x faster                                                 |
| deepcopy                | 265 us                                                                 | 263 us: 1.01x faster                                                  |
| richards                | 45.6 ms                                                                | 45.4 ms: 1.00x faster                                                 |
| nqueens                 | 78.9 ms                                                                | 78.5 ms: 1.00x faster                                                 |
| sqlglot_optimize        | 53.9 ms                                                                | 53.7 ms: 1.00x faster                                                 |
| raytrace                | 263 ms                                                                 | 262 ms: 1.00x faster                                                  |
| pickle_pure_python      | 315 us                                                                 | 314 us: 1.00x faster                                                  |
| regex_effbot            | 3.28 ms                                                                | 3.27 ms: 1.00x faster                                                 |
| sympy_integrate         | 19.9 ms                                                                | 19.9 ms: 1.00x slower                                                 |
| unpickle_pure_python    | 215 us                                                                 | 215 us: 1.00x slower                                                  |
| unpickle_list           | 4.73 us                                                                | 4.75 us: 1.00x slower                                                 |
| sympy_sum               | 152 ms                                                                 | 153 ms: 1.00x slower                                                  |
| dulwich_log             | 75.2 ms                                                                | 75.5 ms: 1.00x slower                                                 |
| docutils                | 2.60 sec                                                               | 2.62 sec: 1.01x slower                                                |
| sqlglot_transpile       | 1.60 ms                                                                | 1.61 ms: 1.01x slower                                                 |
| python_startup          | 11.1 ms                                                                | 11.2 ms: 1.01x slower                                                 |
| xml_etree_parse         | 136 ms                                                                 | 137 ms: 1.01x slower                                                  |
| xml_etree_iterparse     | 95.5 ms                                                                | 96.1 ms: 1.01x slower                                                 |
| python_startup_no_site  | 7.46 ms                                                                | 7.51 ms: 1.01x slower                                                 |
| float                   | 78.6 ms                                                                | 79.2 ms: 1.01x slower                                                 |
| bench_mp_pool           | 63.7 ms                                                                | 64.3 ms: 1.01x slower                                                 |
| sympy_expand            | 460 ms                                                                 | 464 ms: 1.01x slower                                                  |
| telco                   | 7.18 ms                                                                | 7.25 ms: 1.01x slower                                                 |
| go                      | 121 ms                                                                 | 122 ms: 1.01x slower                                                  |
| regex_dna               | 181 ms                                                                 | 183 ms: 1.01x slower                                                  |
| pickle                  | 12.2 us                                                                | 12.3 us: 1.01x slower                                                 |
| fannkuch                | 369 ms                                                                 | 374 ms: 1.01x slower                                                  |
| scimark_fft             | 335 ms                                                                 | 340 ms: 1.01x slower                                                  |
| meteor_contest          | 99.0 ms                                                                | 100 ms: 1.01x slower                                                  |
| crypto_pyaes            | 66.9 ms                                                                | 68.0 ms: 1.02x slower                                                 |
| pyflate                 | 445 ms                                                                 | 452 ms: 1.02x slower                                                  |
| scimark_lu              | 113 ms                                                                 | 115 ms: 1.02x slower                                                  |
| html5lib                | 63.7 ms                                                                | 65.3 ms: 1.02x slower                                                 |
| unpack_sequence         | 46.6 ns                                                                | 48.4 ns: 1.04x slower                                                 |
| gc_traversal            | 3.20 ms                                                                | 3.39 ms: 1.06x slower                                                 |
| scimark_sparse_mat_mult | 4.34 ms                                                                | 4.69 ms: 1.08x slower                                                 |
| pidigits                | 186 ms                                                                 | 223 ms: 1.20x slower                                                  |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (31): logging_simple, typing_runtime_protocols, coroutines, pylint, sympy_str, logging_format, richards_super, hexiom, bpe_tokeniser, pprint_safe_repr, bench_thread_pool, asyncio_websockets, mdp, 2to3, pprint_pformat, spectral_norm, sqlite_synth, sqlglot_normalize, asyncio_tcp_ssl, sqlglot_parse, pathlib, django_template, asyncio_tcp, scimark_monte_carlo, genshi_text, pycparser, tomli_loads, create_gc_cycles, coverage, scimark_sor, unpickle

# HPT report

- Reliability score: 98.86% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x