# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 819f30a
- commit date: 2024-10-18
- overall geometric mean: 1.50x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.36x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 411 ms: 1.56x slower                                                |
| docutils       | 2.64 sec                                               | 3.28 sec: 1.24x slower                                              |
| html5lib       | 63.6 ms                                                | 103 ms: 1.63x slower                                                |
| tornado_http   | 119 ms                                                 | 162 ms: 1.36x slower                                                |
| Geometric mean | (ref)                                                  | 1.44x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|--------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 519 ms: 1.00x slower                                                |
| asyncio_tcp        | 519 ms                                                 | 581 ms: 1.12x slower                                                |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.81 sec: 1.20x slower                                              |
| coroutines         | 23.9 ms                                                | 29.3 ms: 1.22x slower                                               |
| async_generators   | 384 ms                                                 | 525 ms: 1.37x slower                                                |
| Geometric mean     | (ref)                                                  | 1.18x slower                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                |
| float          | 80.8 ms                                                | 146 ms: 1.80x slower                                                |
| nbody          | 89.3 ms                                                | 185 ms: 2.08x slower                                                |
| Geometric mean | (ref)                                                  | 1.56x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.10 ms: 1.02x faster                                               |
| regex_dna      | 168 ms                                                 | 190 ms: 1.13x slower                                                |
| regex_v8       | 20.6 ms                                                | 26.1 ms: 1.27x slower                                               |
| regex_compile  | 142 ms                                                 | 221 ms: 1.55x slower                                                |
| Geometric mean | (ref)                                                  | 1.22x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                |
| pickle_dict          | 31.8 us                                                | 31.6 us: 1.01x faster                                               |
| pickle_list          | 4.77 us                                                | 4.84 us: 1.02x slower                                               |
| unpickle             | 14.1 us                                                | 14.5 us: 1.03x slower                                               |
| json_loads           | 26.5 us                                                | 28.2 us: 1.06x slower                                               |
| xml_etree_iterparse  | 96.7 ms                                                | 105 ms: 1.09x slower                                                |
| unpickle_list        | 4.67 us                                                | 5.18 us: 1.11x slower                                               |
| xml_etree_generate   | 85.2 ms                                                | 110 ms: 1.29x slower                                                |
| json_dumps           | 10.4 ms                                                | 15.1 ms: 1.46x slower                                               |
| xml_etree_process    | 59.0 ms                                                | 89.8 ms: 1.52x slower                                               |
| tomli_loads          | 2.11 sec                                               | 3.22 sec: 1.53x slower                                              |
| unpickle_pure_python | 221 us                                                 | 393 us: 1.78x slower                                                |
| pickle_pure_python   | 308 us                                                 | 586 us: 1.91x slower                                                |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                        |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                               |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                               |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 81.0 ms: 1.61x slower                                               |
| mako            | 11.0 ms                                                | 19.1 ms: 1.74x slower                                               |
| genshi_text     | 22.8 ms                                                | 40.3 ms: 1.77x slower                                               |
| django_template | 34.7 ms                                                | 62.5 ms: 1.80x slower                                               |
| Geometric mean  | (ref)                                                  | 1.73x slower                                                        |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a0-819f30a |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.55 ms: 1.35x faster                                               |
| xml_etree_parse          | 139 ms                                                 | 132 ms: 1.05x faster                                                |
| regex_effbot             | 3.17 ms                                                | 3.10 ms: 1.02x faster                                               |
| pickle_dict              | 31.8 us                                                | 31.6 us: 1.01x faster                                               |
| asyncio_websockets       | 517 ms                                                 | 519 ms: 1.00x slower                                                |
| pidigits                 | 184 ms                                                 | 186 ms: 1.01x slower                                                |
| pickle_list              | 4.77 us                                                | 4.84 us: 1.02x slower                                               |
| pathlib                  | 21.5 ms                                                | 21.9 ms: 1.02x slower                                               |
| unpickle                 | 14.1 us                                                | 14.5 us: 1.03x slower                                               |
| json                     | 5.02 ms                                                | 5.20 ms: 1.04x slower                                               |
| json_loads               | 26.5 us                                                | 28.2 us: 1.06x slower                                               |
| sqlite_synth             | 2.20 us                                                | 2.38 us: 1.08x slower                                               |
| xml_etree_iterparse      | 96.7 ms                                                | 105 ms: 1.09x slower                                                |
| unpickle_list            | 4.67 us                                                | 5.18 us: 1.11x slower                                               |
| asyncio_tcp              | 519 ms                                                 | 581 ms: 1.12x slower                                                |
| regex_dna                | 168 ms                                                 | 190 ms: 1.13x slower                                                |
| scimark_fft              | 342 ms                                                 | 391 ms: 1.15x slower                                                |
| deepcopy                 | 352 us                                                 | 420 us: 1.19x slower                                                |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.81 sec: 1.20x slower                                              |
| bpe_tokeniser            | 4.74 sec                                               | 5.70 sec: 1.20x slower                                              |
| coroutines               | 23.9 ms                                                | 29.3 ms: 1.22x slower                                               |
| deepcopy_memo            | 40.3 us                                                | 49.8 us: 1.24x slower                                               |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.46 ms: 1.24x slower                                               |
| docutils                 | 2.64 sec                                               | 3.28 sec: 1.24x slower                                              |
| regex_v8                 | 20.6 ms                                                | 26.1 ms: 1.27x slower                                               |
| xml_etree_generate       | 85.2 ms                                                | 110 ms: 1.29x slower                                                |
| pylint                   | 319 ms                                                 | 413 ms: 1.30x slower                                                |
| dulwich_log              | 78.9 ms                                                | 103 ms: 1.30x slower                                                |
| mdp                      | 2.42 sec                                               | 3.21 sec: 1.33x slower                                              |
| generators               | 32.2 ms                                                | 43.0 ms: 1.33x slower                                               |
| meteor_contest           | 104 ms                                                 | 139 ms: 1.35x slower                                                |
| spectral_norm            | 110 ms                                                 | 148 ms: 1.35x slower                                                |
| tornado_http             | 119 ms                                                 | 162 ms: 1.36x slower                                                |
| async_generators         | 384 ms                                                 | 525 ms: 1.37x slower                                                |
| crypto_pyaes             | 76.6 ms                                                | 107 ms: 1.40x slower                                                |
| nqueens                  | 80.1 ms                                                | 112 ms: 1.40x slower                                                |
| coverage                 | 71.4 ms                                                | 101 ms: 1.42x slower                                                |
| python_startup_no_site   | 7.16 ms                                                | 10.2 ms: 1.43x slower                                               |
| pycparser                | 1.17 sec                                               | 1.67 sec: 1.43x slower                                              |
| deepcopy_reduce          | 3.08 us                                                | 4.43 us: 1.44x slower                                               |
| telco                    | 6.53 ms                                                | 9.53 ms: 1.46x slower                                               |
| json_dumps               | 10.4 ms                                                | 15.1 ms: 1.46x slower                                               |
| fannkuch                 | 372 ms                                                 | 553 ms: 1.49x slower                                                |
| comprehensions           | 19.8 us                                                | 29.5 us: 1.49x slower                                               |
| typing_runtime_protocols | 163 us                                                 | 243 us: 1.49x slower                                                |
| xml_etree_process        | 59.0 ms                                                | 89.8 ms: 1.52x slower                                               |
| tomli_loads              | 2.11 sec                                               | 3.22 sec: 1.53x slower                                              |
| regex_compile            | 142 ms                                                 | 221 ms: 1.55x slower                                                |
| 2to3                     | 264 ms                                                 | 411 ms: 1.56x slower                                                |
| sympy_integrate          | 20.5 ms                                                | 32.3 ms: 1.57x slower                                               |
| python_startup           | 9.93 ms                                                | 15.7 ms: 1.58x slower                                               |
| genshi_xml               | 50.2 ms                                                | 81.0 ms: 1.61x slower                                               |
| thrift                   | 791 us                                                 | 1.28 ms: 1.62x slower                                               |
| sqlglot_normalize        | 107 ms                                                 | 173 ms: 1.62x slower                                                |
| html5lib                 | 63.6 ms                                                | 103 ms: 1.63x slower                                                |
| sqlglot_optimize         | 53.3 ms                                                | 87.3 ms: 1.64x slower                                               |
| pyflate                  | 448 ms                                                 | 747 ms: 1.67x slower                                                |
| pprint_safe_repr         | 743 ms                                                 | 1.26 sec: 1.70x slower                                              |
| pprint_pformat           | 1.52 sec                                               | 2.63 sec: 1.73x slower                                              |
| mako                     | 11.0 ms                                                | 19.1 ms: 1.74x slower                                               |
| genshi_text              | 22.8 ms                                                | 40.3 ms: 1.77x slower                                               |
| scimark_monte_carlo      | 68.4 ms                                                | 122 ms: 1.78x slower                                                |
| unpickle_pure_python     | 221 us                                                 | 393 us: 1.78x slower                                                |
| django_template          | 34.7 ms                                                | 62.5 ms: 1.80x slower                                               |
| float                    | 80.8 ms                                                | 146 ms: 1.80x slower                                                |
| sympy_str                | 292 ms                                                 | 533 ms: 1.83x slower                                                |
| logging_format           | 7.35 us                                                | 13.5 us: 1.83x slower                                               |
| logging_simple           | 6.63 us                                                | 12.3 us: 1.85x slower                                               |
| chaos                    | 62.8 ms                                                | 117 ms: 1.87x slower                                                |
| richards                 | 45.9 ms                                                | 86.0 ms: 1.87x slower                                               |
| hexiom                   | 6.17 ms                                                | 11.6 ms: 1.89x slower                                               |
| pickle_pure_python       | 308 us                                                 | 586 us: 1.91x slower                                                |
| logging_silent           | 109 ns                                                 | 209 ns: 1.92x slower                                                |
| sqlglot_transpile        | 1.67 ms                                                | 3.29 ms: 1.97x slower                                               |
| richards_super           | 51.9 ms                                                | 104 ms: 2.01x slower                                                |
| scimark_sor              | 130 ms                                                 | 262 ms: 2.02x slower                                                |
| scimark_lu               | 114 ms                                                 | 233 ms: 2.04x slower                                                |
| raytrace                 | 299 ms                                                 | 611 ms: 2.04x slower                                                |
| nbody                    | 89.3 ms                                                | 185 ms: 2.08x slower                                                |
| sqlglot_parse            | 1.36 ms                                                | 2.84 ms: 2.10x slower                                               |
| go                       | 139 ms                                                 | 296 ms: 2.13x slower                                                |
| sympy_expand             | 468 ms                                                 | 1.04 sec: 2.23x slower                                              |
| sympy_sum                | 166 ms                                                 | 379 ms: 2.28x slower                                                |
| deltablue                | 3.45 ms                                                | 8.71 ms: 2.53x slower                                               |
| unpack_sequence          | 52.1 ns                                                | 140 ns: 2.68x slower                                                |
| bench_thread_pool        | 941 us                                                 | 3.48 ms: 3.69x slower                                               |
| bench_mp_pool            | 10.8 ms                                                | 71.7 ms: 6.64x slower                                               |
| Geometric mean           | (ref)                                                  | 1.50x slower                                                        |

Benchmark hidden because not significant (2): pickle, create_gc_cycles
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.42x
- 95% likely to have a slowdown of 1.39x
- 99% likely to have a slowdown of 1.36x

# Memory
- memory change: 1.22x