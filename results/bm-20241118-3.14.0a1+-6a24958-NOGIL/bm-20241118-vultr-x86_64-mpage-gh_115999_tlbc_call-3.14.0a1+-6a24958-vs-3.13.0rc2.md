# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 6a24958
- commit date: 2024-11-18
- overall geometric mean: 1.52x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.37x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 406 ms: 1.57x slower                                                 |
| docutils       | 2.62 sec                                                     | 3.29 sec: 1.26x slower                                               |
| html5lib       | 67.0 ms                                                      | 104 ms: 1.55x slower                                                 |
| Geometric mean | (ref)                                                        | 1.45x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|--------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_websockets | 520 ms                                                       | 516 ms: 1.01x faster                                                 |
| asyncio_tcp        | 505 ms                                                       | 581 ms: 1.15x slower                                                 |
| asyncio_tcp_ssl    | 1.51 sec                                                     | 1.83 sec: 1.21x slower                                               |
| coroutines         | 23.6 ms                                                      | 29.4 ms: 1.25x slower                                                |
| async_generators   | 377 ms                                                       | 482 ms: 1.28x slower                                                 |
| Geometric mean     | (ref)                                                        | 1.17x slower                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 183 ms: 1.18x faster                                                 |
| float          | 77.5 ms                                                      | 147 ms: 1.90x slower                                                 |
| nbody          | 85.1 ms                                                      | 198 ms: 2.33x slower                                                 |
| Geometric mean | (ref)                                                        | 1.55x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.11 ms: 1.01x slower                                                |
| regex_dna      | 180 ms                                                       | 185 ms: 1.03x slower                                                 |
| regex_v8       | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                |
| regex_compile  | 132 ms                                                       | 212 ms: 1.61x slower                                                 |
| Geometric mean | (ref)                                                        | 1.16x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 31.8 us: 1.02x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.02x faster                                                 |
| unpickle             | 14.3 us                                                      | 14.8 us: 1.03x slower                                                |
| unpickle_list        | 4.71 us                                                      | 4.95 us: 1.05x slower                                                |
| pickle_list          | 4.93 us                                                      | 5.19 us: 1.05x slower                                                |
| json_loads           | 27.0 us                                                      | 28.5 us: 1.05x slower                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 106 ms: 1.12x slower                                                 |
| pickle               | 11.3 us                                                      | 14.1 us: 1.24x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 108 ms: 1.27x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 15.0 ms: 1.43x slower                                                |
| xml_etree_process    | 59.3 ms                                                      | 88.5 ms: 1.49x slower                                                |
| tomli_loads          | 2.01 sec                                                     | 3.10 sec: 1.54x slower                                               |
| unpickle_pure_python | 210 us                                                       | 384 us: 1.83x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 577 us: 1.96x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.39x slower                                                |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 79.6 ms: 1.63x slower                                                |
| mako            | 11.3 ms                                                      | 18.8 ms: 1.66x slower                                                |
| django_template | 34.1 ms                                                      | 61.3 ms: 1.80x slower                                                |
| genshi_text     | 21.5 ms                                                      | 39.0 ms: 1.81x slower                                                |
| Geometric mean  | (ref)                                                        | 1.72x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|--------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.58 ms: 1.22x faster                                                |
| create_gc_cycles         | 1.34 ms                                                      | 1.13 ms: 1.19x faster                                                |
| pidigits                 | 217 ms                                                       | 183 ms: 1.18x faster                                                 |
| pickle_dict              | 32.5 us                                                      | 31.8 us: 1.02x faster                                                |
| xml_etree_parse          | 136 ms                                                       | 133 ms: 1.02x faster                                                 |
| asyncio_websockets       | 520 ms                                                       | 516 ms: 1.01x faster                                                 |
| regex_effbot             | 3.08 ms                                                      | 3.11 ms: 1.01x slower                                                |
| regex_dna                | 180 ms                                                       | 185 ms: 1.03x slower                                                 |
| unpickle                 | 14.3 us                                                      | 14.8 us: 1.03x slower                                                |
| unpickle_list            | 4.71 us                                                      | 4.95 us: 1.05x slower                                                |
| pickle_list              | 4.93 us                                                      | 5.19 us: 1.05x slower                                                |
| json_loads               | 27.0 us                                                      | 28.5 us: 1.05x slower                                                |
| json                     | 4.93 ms                                                      | 5.21 ms: 1.06x slower                                                |
| sqlite_synth             | 2.21 us                                                      | 2.39 us: 1.08x slower                                                |
| regex_v8                 | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                |
| xml_etree_iterparse      | 94.9 ms                                                      | 106 ms: 1.12x slower                                                 |
| deepcopy                 | 355 us                                                       | 404 us: 1.14x slower                                                 |
| pathlib                  | 19.2 ms                                                      | 22.0 ms: 1.15x slower                                                |
| asyncio_tcp              | 505 ms                                                       | 581 ms: 1.15x slower                                                 |
| scimark_fft              | 349 ms                                                       | 404 ms: 1.16x slower                                                 |
| telco                    | 7.82 ms                                                      | 9.33 ms: 1.19x slower                                                |
| coverage                 | 83.0 ms                                                      | 100 ms: 1.21x slower                                                 |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.83 sec: 1.21x slower                                               |
| deepcopy_memo            | 39.1 us                                                      | 47.9 us: 1.23x slower                                                |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.80 ms: 1.23x slower                                                |
| pickle                   | 11.3 us                                                      | 14.1 us: 1.24x slower                                                |
| coroutines               | 23.6 ms                                                      | 29.4 ms: 1.25x slower                                                |
| docutils                 | 2.62 sec                                                     | 3.29 sec: 1.26x slower                                               |
| xml_etree_generate       | 85.4 ms                                                      | 108 ms: 1.27x slower                                                 |
| bpe_tokeniser            | 4.45 sec                                                     | 5.66 sec: 1.27x slower                                               |
| async_generators         | 377 ms                                                       | 482 ms: 1.28x slower                                                 |
| pylint                   | 317 ms                                                       | 411 ms: 1.30x slower                                                 |
| mdp                      | 2.36 sec                                                     | 3.06 sec: 1.30x slower                                               |
| meteor_contest           | 102 ms                                                       | 136 ms: 1.34x slower                                                 |
| deepcopy_reduce          | 3.11 us                                                      | 4.23 us: 1.36x slower                                                |
| dulwich_log              | 74.8 ms                                                      | 103 ms: 1.38x slower                                                 |
| spectral_norm            | 111 ms                                                       | 154 ms: 1.39x slower                                                 |
| python_startup_no_site   | 7.39 ms                                                      | 10.2 ms: 1.39x slower                                                |
| nqueens                  | 78.6 ms                                                      | 111 ms: 1.41x slower                                                 |
| python_startup           | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                |
| json_dumps               | 10.5 ms                                                      | 15.0 ms: 1.43x slower                                                |
| generators               | 28.8 ms                                                      | 41.9 ms: 1.46x slower                                                |
| fannkuch                 | 370 ms                                                       | 545 ms: 1.47x slower                                                 |
| pycparser                | 1.12 sec                                                     | 1.65 sec: 1.47x slower                                               |
| xml_etree_process        | 59.3 ms                                                      | 88.5 ms: 1.49x slower                                                |
| tomli_loads              | 2.01 sec                                                     | 3.10 sec: 1.54x slower                                               |
| html5lib                 | 67.0 ms                                                      | 104 ms: 1.55x slower                                                 |
| crypto_pyaes             | 67.9 ms                                                      | 105 ms: 1.55x slower                                                 |
| typing_runtime_protocols | 155 us                                                       | 242 us: 1.56x slower                                                 |
| 2to3                     | 260 ms                                                       | 406 ms: 1.57x slower                                                 |
| regex_compile            | 132 ms                                                       | 212 ms: 1.61x slower                                                 |
| sqlglot_normalize        | 106 ms                                                       | 170 ms: 1.61x slower                                                 |
| sympy_integrate          | 19.8 ms                                                      | 31.9 ms: 1.61x slower                                                |
| sqlglot_optimize         | 52.7 ms                                                      | 85.1 ms: 1.61x slower                                                |
| thrift                   | 778 us                                                       | 1.26 ms: 1.62x slower                                                |
| genshi_xml               | 48.8 ms                                                      | 79.6 ms: 1.63x slower                                                |
| pyflate                  | 449 ms                                                       | 734 ms: 1.64x slower                                                 |
| mako                     | 11.3 ms                                                      | 18.8 ms: 1.66x slower                                                |
| pprint_safe_repr         | 738 ms                                                       | 1.22 sec: 1.66x slower                                               |
| pprint_pformat           | 1.50 sec                                                     | 2.53 sec: 1.69x slower                                               |
| comprehensions           | 16.5 us                                                      | 29.0 us: 1.76x slower                                                |
| django_template          | 34.1 ms                                                      | 61.3 ms: 1.80x slower                                                |
| genshi_text              | 21.5 ms                                                      | 39.0 ms: 1.81x slower                                                |
| unpickle_pure_python     | 210 us                                                       | 384 us: 1.83x slower                                                 |
| scimark_monte_carlo      | 65.4 ms                                                      | 123 ms: 1.88x slower                                                 |
| richards                 | 45.2 ms                                                      | 85.0 ms: 1.88x slower                                                |
| float                    | 77.5 ms                                                      | 147 ms: 1.90x slower                                                 |
| logging_simple           | 6.16 us                                                      | 11.8 us: 1.91x slower                                                |
| hexiom                   | 5.99 ms                                                      | 11.5 ms: 1.91x slower                                                |
| sympy_str                | 275 ms                                                       | 527 ms: 1.92x slower                                                 |
| logging_format           | 6.84 us                                                      | 13.1 us: 1.92x slower                                                |
| scimark_sor              | 134 ms                                                       | 263 ms: 1.96x slower                                                 |
| pickle_pure_python       | 294 us                                                       | 577 us: 1.96x slower                                                 |
| chaos                    | 57.3 ms                                                      | 113 ms: 1.97x slower                                                 |
| logging_silent           | 103 ns                                                       | 202 ns: 1.97x slower                                                 |
| go                       | 141 ms                                                       | 284 ms: 2.01x slower                                                 |
| richards_super           | 51.6 ms                                                      | 106 ms: 2.05x slower                                                 |
| sqlglot_transpile        | 1.56 ms                                                      | 3.20 ms: 2.05x slower                                                |
| scimark_lu               | 113 ms                                                       | 236 ms: 2.09x slower                                                 |
| sqlglot_parse            | 1.25 ms                                                      | 2.78 ms: 2.22x slower                                                |
| sympy_expand             | 457 ms                                                       | 1.03 sec: 2.26x slower                                               |
| raytrace                 | 253 ms                                                       | 574 ms: 2.27x slower                                                 |
| nbody                    | 85.1 ms                                                      | 198 ms: 2.33x slower                                                 |
| sympy_sum                | 156 ms                                                       | 376 ms: 2.42x slower                                                 |
| deltablue                | 3.12 ms                                                      | 8.67 ms: 2.78x slower                                                |
| unpack_sequence          | 44.8 ns                                                      | 147 ns: 3.28x slower                                                 |
| bench_thread_pool        | 919 us                                                       | 3.47 ms: 3.77x slower                                                |
| bench_mp_pool            | 11.0 ms                                                      | 71.9 ms: 6.54x slower                                                |
| Geometric mean           | (ref)                                                        | 1.52x slower                                                         |
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.44x
- 95% likely to have a slowdown of 1.41x
- 99% likely to have a slowdown of 1.37x

# Memory
- memory change: 1.22x