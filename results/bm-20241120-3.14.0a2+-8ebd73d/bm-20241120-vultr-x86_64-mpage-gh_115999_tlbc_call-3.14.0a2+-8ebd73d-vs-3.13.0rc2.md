# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 8ebd73d
- commit date: 2024-11-20
- overall geometric mean: 1.02x slower
- HPT reliability: 90.85%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 255 ms: 1.02x faster                                                 |
| docutils       | 2.62 sec                                                     | 2.59 sec: 1.01x faster                                               |
| html5lib       | 67.0 ms                                                      | 64.9 ms: 1.03x faster                                                |
| Geometric mean | (ref)                                                        | 1.02x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| coroutines       | 23.6 ms                                                      | 23.1 ms: 1.02x faster                                                |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.53 sec: 1.01x slower                                               |
| async_generators | 377 ms                                                       | 385 ms: 1.02x slower                                                 |
| Geometric mean   | (ref)                                                        | 1.00x slower                                                         |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.17x faster                                                 |
| float          | 77.5 ms                                                      | 79.8 ms: 1.03x slower                                                |
| nbody          | 85.1 ms                                                      | 95.2 ms: 1.12x slower                                                |
| Geometric mean | (ref)                                                        | 1.00x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.70 ms: 1.14x faster                                                |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                 |
| regex_compile  | 132 ms                                                       | 130 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                         |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 25.0 us: 1.08x faster                                                |
| pickle_dict          | 32.5 us                                                      | 31.0 us: 1.05x faster                                                |
| unpickle             | 14.3 us                                                      | 13.9 us: 1.03x faster                                                |
| xml_etree_generate   | 85.4 ms                                                      | 84.8 ms: 1.01x faster                                                |
| unpickle_list        | 4.71 us                                                      | 4.68 us: 1.01x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 96.4 ms: 1.02x slower                                                |
| pickle_list          | 4.93 us                                                      | 5.02 us: 1.02x slower                                                |
| unpickle_pure_python | 210 us                                                       | 216 us: 1.03x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.13 sec: 1.06x slower                                               |
| pickle_pure_python   | 294 us                                                       | 314 us: 1.07x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                |
| pickle               | 11.3 us                                                      | 12.4 us: 1.09x slower                                                |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                         |

Benchmark hidden because not significant (2): xml_etree_process, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.42 ms: 1.00x slower                                                |
| python_startup         | 11.0 ms                                                      | 11.1 ms: 1.01x slower                                                |
| Geometric mean         | (ref)                                                        | 1.01x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                                |
| genshi_xml      | 48.8 ms                                                      | 50.6 ms: 1.04x slower                                                |
| genshi_text     | 21.5 ms                                                      | 22.4 ms: 1.04x slower                                                |
| mako            | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241120-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-8ebd73d |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| deepcopy                 | 355 us                                                       | 264 us: 1.35x faster                                                 |
| deepcopy_memo            | 39.1 us                                                      | 30.8 us: 1.27x faster                                                |
| pylint                   | 317 ms                                                       | 270 ms: 1.17x faster                                                 |
| go                       | 141 ms                                                       | 121 ms: 1.17x faster                                                 |
| deepcopy_reduce          | 3.11 us                                                      | 2.67 us: 1.17x faster                                                |
| pidigits                 | 217 ms                                                       | 186 ms: 1.17x faster                                                 |
| regex_effbot             | 3.08 ms                                                      | 2.70 ms: 1.14x faster                                                |
| json_loads               | 27.0 us                                                      | 25.0 us: 1.08x faster                                                |
| telco                    | 7.82 ms                                                      | 7.29 ms: 1.07x faster                                                |
| json                     | 4.93 ms                                                      | 4.66 ms: 1.06x faster                                                |
| pickle_dict              | 32.5 us                                                      | 31.0 us: 1.05x faster                                                |
| pathlib                  | 19.2 ms                                                      | 18.3 ms: 1.05x faster                                                |
| thrift                   | 778 us                                                       | 747 us: 1.04x faster                                                 |
| scimark_fft              | 349 ms                                                       | 337 ms: 1.04x faster                                                 |
| html5lib                 | 67.0 ms                                                      | 64.9 ms: 1.03x faster                                                |
| unpickle                 | 14.3 us                                                      | 13.9 us: 1.03x faster                                                |
| pprint_safe_repr         | 738 ms                                                       | 723 ms: 1.02x faster                                                 |
| sympy_sum                | 156 ms                                                       | 153 ms: 1.02x faster                                                 |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 4.62 ms: 1.02x faster                                                |
| 2to3                     | 260 ms                                                       | 255 ms: 1.02x faster                                                 |
| coroutines               | 23.6 ms                                                      | 23.1 ms: 1.02x faster                                                |
| regex_dna                | 180 ms                                                       | 177 ms: 1.02x faster                                                 |
| coverage                 | 83.0 ms                                                      | 81.7 ms: 1.02x faster                                                |
| regex_compile            | 132 ms                                                       | 130 ms: 1.01x faster                                                 |
| bpe_tokeniser            | 4.45 sec                                                     | 4.40 sec: 1.01x faster                                               |
| meteor_contest           | 102 ms                                                       | 101 ms: 1.01x faster                                                 |
| docutils                 | 2.62 sec                                                     | 2.59 sec: 1.01x faster                                               |
| logging_format           | 6.84 us                                                      | 6.79 us: 1.01x faster                                                |
| xml_etree_generate       | 85.4 ms                                                      | 84.8 ms: 1.01x faster                                                |
| unpickle_list            | 4.71 us                                                      | 4.68 us: 1.01x faster                                                |
| sympy_str                | 275 ms                                                       | 273 ms: 1.01x faster                                                 |
| scimark_lu               | 113 ms                                                       | 112 ms: 1.00x faster                                                 |
| python_startup_no_site   | 7.39 ms                                                      | 7.42 ms: 1.00x slower                                                |
| hexiom                   | 5.99 ms                                                      | 6.02 ms: 1.00x slower                                                |
| sympy_integrate          | 19.8 ms                                                      | 19.9 ms: 1.01x slower                                                |
| richards_super           | 51.6 ms                                                      | 52.0 ms: 1.01x slower                                                |
| sympy_expand             | 457 ms                                                       | 461 ms: 1.01x slower                                                 |
| python_startup           | 11.0 ms                                                      | 11.1 ms: 1.01x slower                                                |
| pyflate                  | 449 ms                                                       | 452 ms: 1.01x slower                                                 |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.53 sec: 1.01x slower                                               |
| dulwich_log              | 74.8 ms                                                      | 75.8 ms: 1.01x slower                                                |
| sqlglot_normalize        | 106 ms                                                       | 107 ms: 1.01x slower                                                 |
| create_gc_cycles         | 1.34 ms                                                      | 1.36 ms: 1.01x slower                                                |
| xml_etree_iterparse      | 94.9 ms                                                      | 96.4 ms: 1.02x slower                                                |
| richards                 | 45.2 ms                                                      | 46.0 ms: 1.02x slower                                                |
| fannkuch                 | 370 ms                                                       | 376 ms: 1.02x slower                                                 |
| pycparser                | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                               |
| chaos                    | 57.3 ms                                                      | 58.3 ms: 1.02x slower                                                |
| scimark_sor              | 134 ms                                                       | 137 ms: 1.02x slower                                                 |
| pickle_list              | 4.93 us                                                      | 5.02 us: 1.02x slower                                                |
| async_generators         | 377 ms                                                       | 385 ms: 1.02x slower                                                 |
| sqlglot_optimize         | 52.7 ms                                                      | 53.9 ms: 1.02x slower                                                |
| typing_runtime_protocols | 155 us                                                       | 158 us: 1.02x slower                                                 |
| generators               | 28.8 ms                                                      | 29.6 ms: 1.03x slower                                                |
| sqlglot_transpile        | 1.56 ms                                                      | 1.60 ms: 1.03x slower                                                |
| float                    | 77.5 ms                                                      | 79.8 ms: 1.03x slower                                                |
| unpickle_pure_python     | 210 us                                                       | 216 us: 1.03x slower                                                 |
| django_template          | 34.1 ms                                                      | 35.3 ms: 1.03x slower                                                |
| genshi_xml               | 48.8 ms                                                      | 50.6 ms: 1.04x slower                                                |
| spectral_norm            | 111 ms                                                       | 115 ms: 1.04x slower                                                 |
| genshi_text              | 21.5 ms                                                      | 22.4 ms: 1.04x slower                                                |
| mako                     | 11.3 ms                                                      | 11.8 ms: 1.04x slower                                                |
| sqlglot_parse            | 1.25 ms                                                      | 1.30 ms: 1.04x slower                                                |
| raytrace                 | 253 ms                                                       | 264 ms: 1.04x slower                                                 |
| unpack_sequence          | 44.8 ns                                                      | 46.8 ns: 1.04x slower                                                |
| comprehensions           | 16.5 us                                                      | 17.2 us: 1.05x slower                                                |
| tomli_loads              | 2.01 sec                                                     | 2.13 sec: 1.06x slower                                               |
| mdp                      | 2.36 sec                                                     | 2.51 sec: 1.06x slower                                               |
| pickle_pure_python       | 294 us                                                       | 314 us: 1.07x slower                                                 |
| logging_silent           | 103 ns                                                       | 110 ns: 1.07x slower                                                 |
| gc_traversal             | 3.14 ms                                                      | 3.39 ms: 1.08x slower                                                |
| json_dumps               | 10.5 ms                                                      | 11.4 ms: 1.08x slower                                                |
| pickle                   | 11.3 us                                                      | 12.4 us: 1.09x slower                                                |
| deltablue                | 3.12 ms                                                      | 3.45 ms: 1.10x slower                                                |
| bench_thread_pool        | 919 us                                                       | 1.02 ms: 1.11x slower                                                |
| nbody                    | 85.1 ms                                                      | 95.2 ms: 1.12x slower                                                |
| bench_mp_pool            | 11.0 ms                                                      | 63.5 ms: 5.78x slower                                                |
| Geometric mean           | (ref)                                                        | 1.02x slower                                                         |

Benchmark hidden because not significant (11): pprint_pformat, asyncio_tcp, scimark_monte_carlo, xml_etree_process, asyncio_websockets, logging_simple, regex_v8, sqlite_synth, xml_etree_parse, crypto_pyaes, nqueens
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 90.85% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x