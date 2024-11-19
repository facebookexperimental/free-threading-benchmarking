# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: e051157
- commit date: 2024-11-18
- overall geometric mean: 1.02x slower
- HPT reliability: 96.25%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                                  |
| html5lib       | 67.0 ms                                                      | 65.3 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| coroutines      | 23.6 ms                                                      | 22.7 ms: 1.04x faster                                                 |
| asyncio_tcp_ssl | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (3): asyncio_tcp, asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 79.2 ms: 1.02x slower                                                 |
| pidigits       | 217 ms                                                       | 223 ms: 1.03x slower                                                  |
| nbody          | 85.1 ms                                                      | 92.5 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 132 ms                                                       | 130 ms: 1.02x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 22.9 ms: 1.01x slower                                                 |
| regex_dna      | 180 ms                                                       | 183 ms: 1.01x slower                                                  |
| regex_effbot   | 3.08 ms                                                      | 3.27 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                        | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 24.9 us: 1.08x faster                                                 |
| unpickle             | 14.3 us                                                      | 13.7 us: 1.05x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 84.5 ms: 1.01x faster                                                 |
| pickle_dict          | 32.5 us                                                      | 32.3 us: 1.01x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 59.0 ms: 1.01x faster                                                 |
| unpickle_list        | 4.71 us                                                      | 4.75 us: 1.01x slower                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 96.1 ms: 1.01x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 215 us: 1.03x slower                                                  |
| pickle_list          | 4.93 us                                                      | 5.13 us: 1.04x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                |
| pickle_pure_python   | 294 us                                                       | 314 us: 1.07x slower                                                  |
| pickle               | 11.3 us                                                      | 12.3 us: 1.08x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                      | 11.2 ms: 1.02x slower                                                 |
| python_startup_no_site | 7.39 ms                                                      | 7.51 ms: 1.02x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.02x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 50.3 ms: 1.03x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 22.3 ms: 1.04x slower                                                 |
| django_template | 34.1 ms                                                      | 35.7 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|--------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| deepcopy                 | 355 us                                                       | 263 us: 1.35x faster                                                  |
| deepcopy_memo            | 39.1 us                                                      | 29.6 us: 1.32x faster                                                 |
| deepcopy_reduce          | 3.11 us                                                      | 2.66 us: 1.17x faster                                                 |
| go                       | 141 ms                                                       | 122 ms: 1.15x faster                                                  |
| json_loads               | 27.0 us                                                      | 24.9 us: 1.08x faster                                                 |
| telco                    | 7.82 ms                                                      | 7.25 ms: 1.08x faster                                                 |
| json                     | 4.93 ms                                                      | 4.60 ms: 1.07x faster                                                 |
| pathlib                  | 19.2 ms                                                      | 18.3 ms: 1.05x faster                                                 |
| unpickle                 | 14.3 us                                                      | 13.7 us: 1.05x faster                                                 |
| thrift                   | 778 us                                                       | 747 us: 1.04x faster                                                  |
| coroutines               | 23.6 ms                                                      | 22.7 ms: 1.04x faster                                                 |
| pprint_safe_repr         | 738 ms                                                       | 716 ms: 1.03x faster                                                  |
| scimark_fft              | 349 ms                                                       | 340 ms: 1.03x faster                                                  |
| html5lib                 | 67.0 ms                                                      | 65.3 ms: 1.03x faster                                                 |
| bpe_tokeniser            | 4.45 sec                                                     | 4.35 sec: 1.02x faster                                                |
| coverage                 | 83.0 ms                                                      | 81.3 ms: 1.02x faster                                                 |
| pprint_pformat           | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                |
| 2to3                     | 260 ms                                                       | 255 ms: 1.02x faster                                                  |
| regex_compile            | 132 ms                                                       | 130 ms: 1.02x faster                                                  |
| sympy_sum                | 156 ms                                                       | 153 ms: 1.02x faster                                                  |
| spectral_norm            | 111 ms                                                       | 110 ms: 1.01x faster                                                  |
| meteor_contest           | 102 ms                                                       | 100 ms: 1.01x faster                                                  |
| xml_etree_generate       | 85.4 ms                                                      | 84.5 ms: 1.01x faster                                                 |
| hexiom                   | 5.99 ms                                                      | 5.93 ms: 1.01x faster                                                 |
| sqlite_synth             | 2.21 us                                                      | 2.19 us: 1.01x faster                                                 |
| pickle_dict              | 32.5 us                                                      | 32.3 us: 1.01x faster                                                 |
| xml_etree_process        | 59.3 ms                                                      | 59.0 ms: 1.01x faster                                                 |
| richards                 | 45.2 ms                                                      | 45.4 ms: 1.00x slower                                                 |
| sympy_integrate          | 19.8 ms                                                      | 19.9 ms: 1.00x slower                                                 |
| scimark_monte_carlo      | 65.4 ms                                                      | 65.6 ms: 1.00x slower                                                 |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.52 sec: 1.01x slower                                                |
| unpickle_list            | 4.71 us                                                      | 4.75 us: 1.01x slower                                                 |
| pyflate                  | 449 ms                                                       | 452 ms: 1.01x slower                                                  |
| logging_simple           | 6.16 us                                                      | 6.21 us: 1.01x slower                                                 |
| dulwich_log              | 74.8 ms                                                      | 75.5 ms: 1.01x slower                                                 |
| sqlglot_normalize        | 106 ms                                                       | 107 ms: 1.01x slower                                                  |
| fannkuch                 | 370 ms                                                       | 374 ms: 1.01x slower                                                  |
| regex_v8                 | 22.7 ms                                                      | 22.9 ms: 1.01x slower                                                 |
| scimark_sor              | 134 ms                                                       | 136 ms: 1.01x slower                                                  |
| xml_etree_iterparse      | 94.9 ms                                                      | 96.1 ms: 1.01x slower                                                 |
| logging_format           | 6.84 us                                                      | 6.93 us: 1.01x slower                                                 |
| typing_runtime_protocols | 155 us                                                       | 157 us: 1.01x slower                                                  |
| regex_dna                | 180 ms                                                       | 183 ms: 1.01x slower                                                  |
| sympy_expand             | 457 ms                                                       | 464 ms: 1.02x slower                                                  |
| pycparser                | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                |
| python_startup           | 11.0 ms                                                      | 11.2 ms: 1.02x slower                                                 |
| python_startup_no_site   | 7.39 ms                                                      | 7.51 ms: 1.02x slower                                                 |
| sqlglot_optimize         | 52.7 ms                                                      | 53.7 ms: 1.02x slower                                                 |
| mako                     | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                 |
| scimark_lu               | 113 ms                                                       | 115 ms: 1.02x slower                                                  |
| float                    | 77.5 ms                                                      | 79.2 ms: 1.02x slower                                                 |
| chaos                    | 57.3 ms                                                      | 58.6 ms: 1.02x slower                                                 |
| unpickle_pure_python     | 210 us                                                       | 215 us: 1.03x slower                                                  |
| create_gc_cycles         | 1.34 ms                                                      | 1.37 ms: 1.03x slower                                                 |
| pidigits                 | 217 ms                                                       | 223 ms: 1.03x slower                                                  |
| sqlglot_transpile        | 1.56 ms                                                      | 1.61 ms: 1.03x slower                                                 |
| genshi_xml               | 48.8 ms                                                      | 50.3 ms: 1.03x slower                                                 |
| comprehensions           | 16.5 us                                                      | 17.0 us: 1.03x slower                                                 |
| deltablue                | 3.12 ms                                                      | 3.22 ms: 1.03x slower                                                 |
| genshi_text              | 21.5 ms                                                      | 22.3 ms: 1.04x slower                                                 |
| raytrace                 | 253 ms                                                       | 262 ms: 1.04x slower                                                  |
| pickle_list              | 4.93 us                                                      | 5.13 us: 1.04x slower                                                 |
| sqlglot_parse            | 1.25 ms                                                      | 1.30 ms: 1.04x slower                                                 |
| django_template          | 34.1 ms                                                      | 35.7 ms: 1.05x slower                                                 |
| tomli_loads              | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                |
| regex_effbot             | 3.08 ms                                                      | 3.27 ms: 1.06x slower                                                 |
| pickle_pure_python       | 294 us                                                       | 314 us: 1.07x slower                                                  |
| unpack_sequence          | 44.8 ns                                                      | 48.4 ns: 1.08x slower                                                 |
| gc_traversal             | 3.14 ms                                                      | 3.39 ms: 1.08x slower                                                 |
| pickle                   | 11.3 us                                                      | 12.3 us: 1.08x slower                                                 |
| nbody                    | 85.1 ms                                                      | 92.5 ms: 1.09x slower                                                 |
| json_dumps               | 10.5 ms                                                      | 11.5 ms: 1.09x slower                                                 |
| bench_thread_pool        | 919 us                                                       | 1.01 ms: 1.10x slower                                                 |
| bench_mp_pool            | 11.0 ms                                                      | 64.3 ms: 5.85x slower                                                 |
| Geometric mean           | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (14): sympy_str, scimark_sparse_mat_mult, richards_super, nqueens, asyncio_tcp, docutils, mdp, asyncio_websockets, pylint, crypto_pyaes, xml_etree_parse, async_generators, logging_silent, generators
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 96.25% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x