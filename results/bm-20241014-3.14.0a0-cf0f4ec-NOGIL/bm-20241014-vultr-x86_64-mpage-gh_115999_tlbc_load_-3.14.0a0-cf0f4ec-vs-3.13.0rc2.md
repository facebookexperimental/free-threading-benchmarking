# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: cf0f4ec
- commit date: 2024-10-14
- overall geometric mean: 1.48x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.33x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 404 ms: 1.56x slower                                                 |
| docutils       | 2.62 sec                                                     | 3.22 sec: 1.23x slower                                               |
| html5lib       | 67.0 ms                                                      | 100 ms: 1.49x slower                                                 |
| tornado_http   | 114 ms                                                       | 158 ms: 1.39x slower                                                 |
| Geometric mean | (ref)                                                        | 1.41x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_tcp      | 505 ms                                                       | 569 ms: 1.13x slower                                                 |
| coroutines       | 23.6 ms                                                      | 28.1 ms: 1.19x slower                                                |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.81 sec: 1.20x slower                                               |
| async_generators | 377 ms                                                       | 482 ms: 1.28x slower                                                 |
| Geometric mean   | (ref)                                                        | 1.15x slower                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                 |
| float          | 77.5 ms                                                      | 145 ms: 1.87x slower                                                 |
| nbody          | 85.1 ms                                                      | 184 ms: 2.16x slower                                                 |
| Geometric mean | (ref)                                                        | 1.51x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.06 ms: 1.01x faster                                                |
| regex_dna      | 180 ms                                                       | 189 ms: 1.05x slower                                                 |
| regex_v8       | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                |
| regex_compile  | 132 ms                                                       | 204 ms: 1.54x slower                                                 |
| Geometric mean | (ref)                                                        | 1.15x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                 |
| pickle_dict          | 32.5 us                                                      | 31.7 us: 1.02x faster                                                |
| pickle               | 11.3 us                                                      | 11.1 us: 1.02x faster                                                |
| pickle_list          | 4.93 us                                                      | 4.85 us: 1.02x faster                                                |
| unpickle             | 14.3 us                                                      | 14.9 us: 1.04x slower                                                |
| json_loads           | 27.0 us                                                      | 28.7 us: 1.06x slower                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 102 ms: 1.07x slower                                                 |
| unpickle_list        | 4.71 us                                                      | 5.21 us: 1.11x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 106 ms: 1.24x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 14.6 ms: 1.39x slower                                                |
| xml_etree_process    | 59.3 ms                                                      | 85.8 ms: 1.45x slower                                                |
| tomli_loads          | 2.01 sec                                                     | 2.99 sec: 1.49x slower                                               |
| unpickle_pure_python | 210 us                                                       | 379 us: 1.80x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 557 us: 1.89x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.21x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                |
| python_startup         | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                |
| Geometric mean         | (ref)                                                        | 1.40x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 73.0 ms: 1.50x slower                                                |
| genshi_text     | 21.5 ms                                                      | 35.7 ms: 1.66x slower                                                |
| django_template | 34.1 ms                                                      | 58.0 ms: 1.70x slower                                                |
| mako            | 11.3 ms                                                      | 20.0 ms: 1.76x slower                                                |
| Geometric mean  | (ref)                                                        | 1.65x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.45 ms: 1.28x faster                                                |
| create_gc_cycles         | 1.34 ms                                                      | 1.10 ms: 1.21x faster                                                |
| pidigits                 | 217 ms                                                       | 184 ms: 1.18x faster                                                 |
| xml_etree_parse          | 136 ms                                                       | 132 ms: 1.03x faster                                                 |
| pickle_dict              | 32.5 us                                                      | 31.7 us: 1.02x faster                                                |
| pickle                   | 11.3 us                                                      | 11.1 us: 1.02x faster                                                |
| pickle_list              | 4.93 us                                                      | 4.85 us: 1.02x faster                                                |
| regex_effbot             | 3.08 ms                                                      | 3.06 ms: 1.01x faster                                                |
| unpickle                 | 14.3 us                                                      | 14.9 us: 1.04x slower                                                |
| json                     | 4.93 ms                                                      | 5.16 ms: 1.05x slower                                                |
| regex_dna                | 180 ms                                                       | 189 ms: 1.05x slower                                                 |
| deepcopy                 | 355 us                                                       | 376 us: 1.06x slower                                                 |
| json_loads               | 27.0 us                                                      | 28.7 us: 1.06x slower                                                |
| xml_etree_iterparse      | 94.9 ms                                                      | 102 ms: 1.07x slower                                                 |
| sqlite_synth             | 2.21 us                                                      | 2.42 us: 1.10x slower                                                |
| regex_v8                 | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                |
| pathlib                  | 19.2 ms                                                      | 21.2 ms: 1.10x slower                                                |
| unpickle_list            | 4.71 us                                                      | 5.21 us: 1.11x slower                                                |
| scimark_fft              | 349 ms                                                       | 392 ms: 1.12x slower                                                 |
| asyncio_tcp              | 505 ms                                                       | 569 ms: 1.13x slower                                                 |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.34 ms: 1.13x slower                                                |
| deepcopy_memo            | 39.1 us                                                      | 46.0 us: 1.18x slower                                                |
| coroutines               | 23.6 ms                                                      | 28.1 ms: 1.19x slower                                                |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.81 sec: 1.20x slower                                               |
| coverage                 | 83.0 ms                                                      | 99.6 ms: 1.20x slower                                                |
| telco                    | 7.82 ms                                                      | 9.49 ms: 1.21x slower                                                |
| docutils                 | 2.62 sec                                                     | 3.22 sec: 1.23x slower                                               |
| xml_etree_generate       | 85.4 ms                                                      | 106 ms: 1.24x slower                                                 |
| mdp                      | 2.36 sec                                                     | 2.96 sec: 1.26x slower                                               |
| deepcopy_reduce          | 3.11 us                                                      | 3.92 us: 1.26x slower                                                |
| pylint                   | 317 ms                                                       | 400 ms: 1.26x slower                                                 |
| async_generators         | 377 ms                                                       | 482 ms: 1.28x slower                                                 |
| bpe_tokeniser            | 4.45 sec                                                     | 5.76 sec: 1.30x slower                                               |
| spectral_norm            | 111 ms                                                       | 145 ms: 1.31x slower                                                 |
| dulwich_log              | 74.8 ms                                                      | 99.4 ms: 1.33x slower                                                |
| meteor_contest           | 102 ms                                                       | 136 ms: 1.33x slower                                                 |
| nqueens                  | 78.6 ms                                                      | 108 ms: 1.37x slower                                                 |
| generators               | 28.8 ms                                                      | 39.6 ms: 1.37x slower                                                |
| python_startup_no_site   | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                |
| typing_runtime_protocols | 155 us                                                       | 213 us: 1.38x slower                                                 |
| tornado_http             | 114 ms                                                       | 158 ms: 1.39x slower                                                 |
| json_dumps               | 10.5 ms                                                      | 14.6 ms: 1.39x slower                                                |
| python_startup           | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                |
| xml_etree_process        | 59.3 ms                                                      | 85.8 ms: 1.45x slower                                                |
| pycparser                | 1.12 sec                                                     | 1.64 sec: 1.47x slower                                               |
| fannkuch                 | 370 ms                                                       | 547 ms: 1.48x slower                                                 |
| tomli_loads              | 2.01 sec                                                     | 2.99 sec: 1.49x slower                                               |
| html5lib                 | 67.0 ms                                                      | 100 ms: 1.49x slower                                                 |
| genshi_xml               | 48.8 ms                                                      | 73.0 ms: 1.50x slower                                                |
| sqlglot_normalize        | 106 ms                                                       | 158 ms: 1.50x slower                                                 |
| sqlglot_optimize         | 52.7 ms                                                      | 80.0 ms: 1.52x slower                                                |
| regex_compile            | 132 ms                                                       | 204 ms: 1.54x slower                                                 |
| crypto_pyaes             | 67.9 ms                                                      | 105 ms: 1.55x slower                                                 |
| 2to3                     | 260 ms                                                       | 404 ms: 1.56x slower                                                 |
| pprint_safe_repr         | 738 ms                                                       | 1.15 sec: 1.56x slower                                               |
| sympy_integrate          | 19.8 ms                                                      | 31.6 ms: 1.59x slower                                                |
| thrift                   | 778 us                                                       | 1.24 ms: 1.59x slower                                                |
| pprint_pformat           | 1.50 sec                                                     | 2.40 sec: 1.60x slower                                               |
| genshi_text              | 21.5 ms                                                      | 35.7 ms: 1.66x slower                                                |
| pyflate                  | 449 ms                                                       | 750 ms: 1.67x slower                                                 |
| django_template          | 34.1 ms                                                      | 58.0 ms: 1.70x slower                                                |
| mako                     | 11.3 ms                                                      | 20.0 ms: 1.76x slower                                                |
| comprehensions           | 16.5 us                                                      | 29.3 us: 1.78x slower                                                |
| unpickle_pure_python     | 210 us                                                       | 379 us: 1.80x slower                                                 |
| scimark_monte_carlo      | 65.4 ms                                                      | 119 ms: 1.82x slower                                                 |
| scimark_lu               | 113 ms                                                       | 206 ms: 1.83x slower                                                 |
| logging_format           | 6.84 us                                                      | 12.5 us: 1.83x slower                                                |
| logging_simple           | 6.16 us                                                      | 11.4 us: 1.85x slower                                                |
| richards                 | 45.2 ms                                                      | 83.8 ms: 1.85x slower                                                |
| float                    | 77.5 ms                                                      | 145 ms: 1.87x slower                                                 |
| sympy_str                | 275 ms                                                       | 517 ms: 1.88x slower                                                 |
| hexiom                   | 5.99 ms                                                      | 11.3 ms: 1.88x slower                                                |
| pickle_pure_python       | 294 us                                                       | 557 us: 1.89x slower                                                 |
| scimark_sor              | 134 ms                                                       | 257 ms: 1.91x slower                                                 |
| richards_super           | 51.6 ms                                                      | 101 ms: 1.95x slower                                                 |
| chaos                    | 57.3 ms                                                      | 114 ms: 1.99x slower                                                 |
| logging_silent           | 103 ns                                                       | 207 ns: 2.01x slower                                                 |
| go                       | 141 ms                                                       | 286 ms: 2.03x slower                                                 |
| sqlglot_transpile        | 1.56 ms                                                      | 3.23 ms: 2.07x slower                                                |
| nbody                    | 85.1 ms                                                      | 184 ms: 2.16x slower                                                 |
| sqlglot_parse            | 1.25 ms                                                      | 2.78 ms: 2.22x slower                                                |
| sympy_expand             | 457 ms                                                       | 1.02 sec: 2.23x slower                                               |
| sympy_sum                | 156 ms                                                       | 369 ms: 2.37x slower                                                 |
| raytrace                 | 253 ms                                                       | 617 ms: 2.44x slower                                                 |
| deltablue                | 3.12 ms                                                      | 8.61 ms: 2.75x slower                                                |
| unpack_sequence          | 44.8 ns                                                      | 132 ns: 2.94x slower                                                 |
| bench_thread_pool        | 919 us                                                       | 3.44 ms: 3.75x slower                                                |
| bench_mp_pool            | 11.0 ms                                                      | 71.1 ms: 6.47x slower                                                |
| Geometric mean           | (ref)                                                        | 1.48x slower                                                         |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.38x
- 95% likely to have a slowdown of 1.37x
- 99% likely to have a slowdown of 1.33x

# Memory
- memory change: 1.21x