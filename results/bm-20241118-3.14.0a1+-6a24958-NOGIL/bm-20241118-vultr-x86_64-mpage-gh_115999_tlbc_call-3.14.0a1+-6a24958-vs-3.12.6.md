# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 6a24958
- commit date: 2024-11-18
- overall geometric mean: 1.49x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.34x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 406 ms: 1.54x slower                                                 |
| docutils       | 2.64 sec                                               | 3.29 sec: 1.25x slower                                               |
| html5lib       | 63.6 ms                                                | 104 ms: 1.63x slower                                                 |
| Geometric mean | (ref)                                                  | 1.46x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_tcp      | 519 ms                                                 | 581 ms: 1.12x slower                                                 |
| asyncio_tcp_ssl  | 1.51 sec                                               | 1.83 sec: 1.22x slower                                               |
| coroutines       | 23.9 ms                                                | 29.4 ms: 1.23x slower                                                |
| async_generators | 384 ms                                                 | 482 ms: 1.25x slower                                                 |
| Geometric mean   | (ref)                                                  | 1.16x slower                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 183 ms: 1.01x faster                                                 |
| float          | 80.8 ms                                                | 147 ms: 1.82x slower                                                 |
| nbody          | 89.3 ms                                                | 198 ms: 2.22x slower                                                 |
| Geometric mean | (ref)                                                  | 1.59x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.11 ms: 1.02x faster                                                |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                 |
| regex_v8       | 20.6 ms                                                | 25.0 ms: 1.21x slower                                                |
| regex_compile  | 142 ms                                                 | 212 ms: 1.49x slower                                                 |
| Geometric mean | (ref)                                                  | 1.18x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                 |
| unpickle             | 14.1 us                                                | 14.8 us: 1.05x slower                                                |
| unpickle_list        | 4.67 us                                                | 4.95 us: 1.06x slower                                                |
| json_loads           | 26.5 us                                                | 28.5 us: 1.07x slower                                                |
| pickle_list          | 4.77 us                                                | 5.19 us: 1.09x slower                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 106 ms: 1.10x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 108 ms: 1.27x slower                                                 |
| pickle               | 10.9 us                                                | 14.1 us: 1.28x slower                                                |
| json_dumps           | 10.4 ms                                                | 15.0 ms: 1.45x slower                                                |
| tomli_loads          | 2.11 sec                                               | 3.10 sec: 1.47x slower                                               |
| xml_etree_process    | 59.0 ms                                                | 88.5 ms: 1.50x slower                                                |
| unpickle_pure_python | 221 us                                                 | 384 us: 1.74x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 577 us: 1.88x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.25x slower                                                         |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 79.6 ms: 1.59x slower                                                |
| mako            | 11.0 ms                                                | 18.8 ms: 1.71x slower                                                |
| genshi_text     | 22.8 ms                                                | 39.0 ms: 1.71x slower                                                |
| django_template | 34.7 ms                                                | 61.3 ms: 1.77x slower                                                |
| Geometric mean  | (ref)                                                  | 1.69x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.58 ms: 1.34x faster                                                |
| xml_etree_parse          | 139 ms                                                 | 133 ms: 1.04x faster                                                 |
| regex_effbot             | 3.17 ms                                                | 3.11 ms: 1.02x faster                                                |
| pidigits                 | 184 ms                                                 | 183 ms: 1.01x faster                                                 |
| pathlib                  | 21.5 ms                                                | 22.0 ms: 1.02x slower                                                |
| create_gc_cycles         | 1.09 ms                                                | 1.13 ms: 1.03x slower                                                |
| json                     | 5.02 ms                                                | 5.21 ms: 1.04x slower                                                |
| unpickle                 | 14.1 us                                                | 14.8 us: 1.05x slower                                                |
| unpickle_list            | 4.67 us                                                | 4.95 us: 1.06x slower                                                |
| json_loads               | 26.5 us                                                | 28.5 us: 1.07x slower                                                |
| sqlite_synth             | 2.20 us                                                | 2.39 us: 1.09x slower                                                |
| pickle_list              | 4.77 us                                                | 5.19 us: 1.09x slower                                                |
| xml_etree_iterparse      | 96.7 ms                                                | 106 ms: 1.10x slower                                                 |
| regex_dna                | 168 ms                                                 | 185 ms: 1.10x slower                                                 |
| asyncio_tcp              | 519 ms                                                 | 581 ms: 1.12x slower                                                 |
| deepcopy                 | 352 us                                                 | 404 us: 1.15x slower                                                 |
| scimark_fft              | 342 ms                                                 | 404 ms: 1.18x slower                                                 |
| deepcopy_memo            | 40.3 us                                                | 47.9 us: 1.19x slower                                                |
| bpe_tokeniser            | 4.74 sec                                               | 5.66 sec: 1.20x slower                                               |
| regex_v8                 | 20.6 ms                                                | 25.0 ms: 1.21x slower                                                |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.83 sec: 1.22x slower                                               |
| coroutines               | 23.9 ms                                                | 29.4 ms: 1.23x slower                                                |
| docutils                 | 2.64 sec                                               | 3.29 sec: 1.25x slower                                               |
| async_generators         | 384 ms                                                 | 482 ms: 1.25x slower                                                 |
| mdp                      | 2.42 sec                                               | 3.06 sec: 1.27x slower                                               |
| xml_etree_generate       | 85.2 ms                                                | 108 ms: 1.27x slower                                                 |
| pickle                   | 10.9 us                                                | 14.1 us: 1.28x slower                                                |
| pylint                   | 319 ms                                                 | 411 ms: 1.29x slower                                                 |
| generators               | 32.2 ms                                                | 41.9 ms: 1.30x slower                                                |
| dulwich_log              | 78.9 ms                                                | 103 ms: 1.31x slower                                                 |
| meteor_contest           | 104 ms                                                 | 136 ms: 1.32x slower                                                 |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.80 ms: 1.32x slower                                                |
| deepcopy_reduce          | 3.08 us                                                | 4.23 us: 1.37x slower                                                |
| crypto_pyaes             | 76.6 ms                                                | 105 ms: 1.38x slower                                                 |
| nqueens                  | 80.1 ms                                                | 111 ms: 1.38x slower                                                 |
| spectral_norm            | 110 ms                                                 | 154 ms: 1.40x slower                                                 |
| coverage                 | 71.4 ms                                                | 100 ms: 1.41x slower                                                 |
| pycparser                | 1.17 sec                                               | 1.65 sec: 1.41x slower                                               |
| telco                    | 6.53 ms                                                | 9.33 ms: 1.43x slower                                                |
| python_startup_no_site   | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                |
| json_dumps               | 10.4 ms                                                | 15.0 ms: 1.45x slower                                                |
| fannkuch                 | 372 ms                                                 | 545 ms: 1.46x slower                                                 |
| comprehensions           | 19.8 us                                                | 29.0 us: 1.46x slower                                                |
| tomli_loads              | 2.11 sec                                               | 3.10 sec: 1.47x slower                                               |
| typing_runtime_protocols | 163 us                                                 | 242 us: 1.48x slower                                                 |
| regex_compile            | 142 ms                                                 | 212 ms: 1.49x slower                                                 |
| xml_etree_process        | 59.0 ms                                                | 88.5 ms: 1.50x slower                                                |
| 2to3                     | 264 ms                                                 | 406 ms: 1.54x slower                                                 |
| sympy_integrate          | 20.5 ms                                                | 31.9 ms: 1.55x slower                                                |
| python_startup           | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                |
| genshi_xml               | 50.2 ms                                                | 79.6 ms: 1.59x slower                                                |
| thrift                   | 791 us                                                 | 1.26 ms: 1.59x slower                                                |
| sqlglot_normalize        | 107 ms                                                 | 170 ms: 1.60x slower                                                 |
| sqlglot_optimize         | 53.3 ms                                                | 85.1 ms: 1.60x slower                                                |
| html5lib                 | 63.6 ms                                                | 104 ms: 1.63x slower                                                 |
| pyflate                  | 448 ms                                                 | 734 ms: 1.64x slower                                                 |
| pprint_safe_repr         | 743 ms                                                 | 1.22 sec: 1.65x slower                                               |
| pprint_pformat           | 1.52 sec                                               | 2.53 sec: 1.67x slower                                               |
| mako                     | 11.0 ms                                                | 18.8 ms: 1.71x slower                                                |
| genshi_text              | 22.8 ms                                                | 39.0 ms: 1.71x slower                                                |
| unpickle_pure_python     | 221 us                                                 | 384 us: 1.74x slower                                                 |
| django_template          | 34.7 ms                                                | 61.3 ms: 1.77x slower                                                |
| logging_simple           | 6.63 us                                                | 11.8 us: 1.77x slower                                                |
| logging_format           | 7.35 us                                                | 13.1 us: 1.79x slower                                                |
| scimark_monte_carlo      | 68.4 ms                                                | 123 ms: 1.79x slower                                                 |
| chaos                    | 62.8 ms                                                | 113 ms: 1.80x slower                                                 |
| sympy_str                | 292 ms                                                 | 527 ms: 1.81x slower                                                 |
| float                    | 80.8 ms                                                | 147 ms: 1.82x slower                                                 |
| richards                 | 45.9 ms                                                | 85.0 ms: 1.85x slower                                                |
| hexiom                   | 6.17 ms                                                | 11.5 ms: 1.86x slower                                                |
| logging_silent           | 109 ns                                                 | 202 ns: 1.86x slower                                                 |
| pickle_pure_python       | 308 us                                                 | 577 us: 1.88x slower                                                 |
| sqlglot_transpile        | 1.67 ms                                                | 3.20 ms: 1.91x slower                                                |
| raytrace                 | 299 ms                                                 | 574 ms: 1.92x slower                                                 |
| scimark_sor              | 130 ms                                                 | 263 ms: 2.03x slower                                                 |
| go                       | 139 ms                                                 | 284 ms: 2.04x slower                                                 |
| richards_super           | 51.9 ms                                                | 106 ms: 2.04x slower                                                 |
| sqlglot_parse            | 1.36 ms                                                | 2.78 ms: 2.05x slower                                                |
| scimark_lu               | 114 ms                                                 | 236 ms: 2.06x slower                                                 |
| sympy_expand             | 468 ms                                                 | 1.03 sec: 2.21x slower                                               |
| nbody                    | 89.3 ms                                                | 198 ms: 2.22x slower                                                 |
| sympy_sum                | 166 ms                                                 | 376 ms: 2.27x slower                                                 |
| deltablue                | 3.45 ms                                                | 8.67 ms: 2.52x slower                                                |
| unpack_sequence          | 52.1 ns                                                | 147 ns: 2.82x slower                                                 |
| bench_thread_pool        | 941 us                                                 | 3.47 ms: 3.68x slower                                                |
| bench_mp_pool            | 10.8 ms                                                | 71.9 ms: 6.66x slower                                                |
| Geometric mean           | (ref)                                                  | 1.49x slower                                                         |

Benchmark hidden because not significant (2): asyncio_websockets, pickle_dict
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.41x
- 95% likely to have a slowdown of 1.39x
- 99% likely to have a slowdown of 1.34x

# Memory
- memory change: 1.23x