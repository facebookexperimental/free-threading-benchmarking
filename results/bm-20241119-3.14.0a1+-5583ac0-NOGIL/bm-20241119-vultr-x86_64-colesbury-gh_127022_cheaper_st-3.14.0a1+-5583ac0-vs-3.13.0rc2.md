# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_127022_cheaper_st
- machine: linux-x86_64
- commit hash: 5583ac0
- commit date: 2024-11-19
- overall geometric mean: 1.55x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.39x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 412 ms: 1.59x slower                                                      |
| docutils       | 2.62 sec                                                     | 3.37 sec: 1.29x slower                                                    |
| html5lib       | 67.0 ms                                                      | 106 ms: 1.58x slower                                                      |
| Geometric mean | (ref)                                                        | 1.48x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|--------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| asyncio_websockets | 520 ms                                                       | 518 ms: 1.00x faster                                                      |
| asyncio_tcp        | 505 ms                                                       | 580 ms: 1.15x slower                                                      |
| asyncio_tcp_ssl    | 1.51 sec                                                     | 1.81 sec: 1.20x slower                                                    |
| async_generators   | 377 ms                                                       | 493 ms: 1.31x slower                                                      |
| coroutines         | 23.6 ms                                                      | 31.0 ms: 1.31x slower                                                     |
| Geometric mean     | (ref)                                                        | 1.19x slower                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.16x faster                                                      |
| float          | 77.5 ms                                                      | 150 ms: 1.94x slower                                                      |
| nbody          | 85.1 ms                                                      | 199 ms: 2.34x slower                                                      |
| Geometric mean | (ref)                                                        | 1.57x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.82 ms: 1.09x faster                                                     |
| regex_dna      | 180 ms                                                       | 180 ms: 1.00x faster                                                      |
| regex_v8       | 22.7 ms                                                      | 24.6 ms: 1.09x slower                                                     |
| regex_compile  | 132 ms                                                       | 228 ms: 1.73x slower                                                      |
| Geometric mean | (ref)                                                        | 1.14x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                      |
| pickle_dict          | 32.5 us                                                      | 31.9 us: 1.02x faster                                                     |
| unpickle             | 14.3 us                                                      | 14.6 us: 1.02x slower                                                     |
| pickle_list          | 4.93 us                                                      | 5.17 us: 1.05x slower                                                     |
| pickle               | 11.3 us                                                      | 11.9 us: 1.05x slower                                                     |
| json_loads           | 27.0 us                                                      | 28.6 us: 1.06x slower                                                     |
| unpickle_list        | 4.71 us                                                      | 5.20 us: 1.10x slower                                                     |
| xml_etree_iterparse  | 94.9 ms                                                      | 109 ms: 1.15x slower                                                      |
| xml_etree_generate   | 85.4 ms                                                      | 112 ms: 1.31x slower                                                      |
| json_dumps           | 10.5 ms                                                      | 15.4 ms: 1.46x slower                                                     |
| xml_etree_process    | 59.3 ms                                                      | 91.8 ms: 1.55x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 3.18 sec: 1.58x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 422 us: 2.01x slower                                                      |
| pickle_pure_python   | 294 us                                                       | 621 us: 2.11x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.27x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                     |
| python_startup         | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.40x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 81.5 ms: 1.67x slower                                                     |
| mako            | 11.3 ms                                                      | 20.7 ms: 1.83x slower                                                     |
| genshi_text     | 21.5 ms                                                      | 40.2 ms: 1.86x slower                                                     |
| django_template | 34.1 ms                                                      | 64.4 ms: 1.89x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.81x slower                                                              |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|--------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.36 ms: 1.33x faster                                                     |
| create_gc_cycles         | 1.34 ms                                                      | 1.13 ms: 1.18x faster                                                     |
| pidigits                 | 217 ms                                                       | 186 ms: 1.16x faster                                                      |
| regex_effbot             | 3.08 ms                                                      | 2.82 ms: 1.09x faster                                                     |
| xml_etree_parse          | 136 ms                                                       | 132 ms: 1.03x faster                                                      |
| pickle_dict              | 32.5 us                                                      | 31.9 us: 1.02x faster                                                     |
| asyncio_websockets       | 520 ms                                                       | 518 ms: 1.00x faster                                                      |
| regex_dna                | 180 ms                                                       | 180 ms: 1.00x faster                                                      |
| unpickle                 | 14.3 us                                                      | 14.6 us: 1.02x slower                                                     |
| pickle_list              | 4.93 us                                                      | 5.17 us: 1.05x slower                                                     |
| pickle                   | 11.3 us                                                      | 11.9 us: 1.05x slower                                                     |
| json_loads               | 27.0 us                                                      | 28.6 us: 1.06x slower                                                     |
| json                     | 4.93 ms                                                      | 5.27 ms: 1.07x slower                                                     |
| regex_v8                 | 22.7 ms                                                      | 24.6 ms: 1.09x slower                                                     |
| sqlite_synth             | 2.21 us                                                      | 2.42 us: 1.10x slower                                                     |
| unpickle_list            | 4.71 us                                                      | 5.20 us: 1.10x slower                                                     |
| pathlib                  | 19.2 ms                                                      | 21.7 ms: 1.13x slower                                                     |
| asyncio_tcp              | 505 ms                                                       | 580 ms: 1.15x slower                                                      |
| xml_etree_iterparse      | 94.9 ms                                                      | 109 ms: 1.15x slower                                                      |
| scimark_fft              | 349 ms                                                       | 417 ms: 1.19x slower                                                      |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.81 sec: 1.20x slower                                                    |
| telco                    | 7.82 ms                                                      | 9.42 ms: 1.20x slower                                                     |
| deepcopy                 | 355 us                                                       | 431 us: 1.21x slower                                                      |
| coverage                 | 83.0 ms                                                      | 103 ms: 1.24x slower                                                      |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.95 ms: 1.26x slower                                                     |
| docutils                 | 2.62 sec                                                     | 3.37 sec: 1.29x slower                                                    |
| mdp                      | 2.36 sec                                                     | 3.05 sec: 1.29x slower                                                    |
| async_generators         | 377 ms                                                       | 493 ms: 1.31x slower                                                      |
| xml_etree_generate       | 85.4 ms                                                      | 112 ms: 1.31x slower                                                      |
| coroutines               | 23.6 ms                                                      | 31.0 ms: 1.31x slower                                                     |
| pylint                   | 317 ms                                                       | 420 ms: 1.32x slower                                                      |
| deepcopy_memo            | 39.1 us                                                      | 52.9 us: 1.35x slower                                                     |
| meteor_contest           | 102 ms                                                       | 138 ms: 1.36x slower                                                      |
| dulwich_log              | 74.8 ms                                                      | 103 ms: 1.38x slower                                                      |
| bpe_tokeniser            | 4.45 sec                                                     | 6.13 sec: 1.38x slower                                                    |
| python_startup_no_site   | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                     |
| generators               | 28.8 ms                                                      | 40.2 ms: 1.40x slower                                                     |
| python_startup           | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                     |
| deepcopy_reduce          | 3.11 us                                                      | 4.43 us: 1.42x slower                                                     |
| spectral_norm            | 111 ms                                                       | 161 ms: 1.45x slower                                                      |
| json_dumps               | 10.5 ms                                                      | 15.4 ms: 1.46x slower                                                     |
| nqueens                  | 78.6 ms                                                      | 115 ms: 1.46x slower                                                      |
| pycparser                | 1.12 sec                                                     | 1.69 sec: 1.52x slower                                                    |
| xml_etree_process        | 59.3 ms                                                      | 91.8 ms: 1.55x slower                                                     |
| fannkuch                 | 370 ms                                                       | 572 ms: 1.55x slower                                                      |
| html5lib                 | 67.0 ms                                                      | 106 ms: 1.58x slower                                                      |
| tomli_loads              | 2.01 sec                                                     | 3.18 sec: 1.58x slower                                                    |
| crypto_pyaes             | 67.9 ms                                                      | 108 ms: 1.59x slower                                                      |
| 2to3                     | 260 ms                                                       | 412 ms: 1.59x slower                                                      |
| typing_runtime_protocols | 155 us                                                       | 248 us: 1.61x slower                                                      |
| thrift                   | 778 us                                                       | 1.26 ms: 1.62x slower                                                     |
| sympy_integrate          | 19.8 ms                                                      | 33.1 ms: 1.67x slower                                                     |
| genshi_xml               | 48.8 ms                                                      | 81.5 ms: 1.67x slower                                                     |
| sqlglot_normalize        | 106 ms                                                       | 180 ms: 1.71x slower                                                      |
| sqlglot_optimize         | 52.7 ms                                                      | 90.7 ms: 1.72x slower                                                     |
| regex_compile            | 132 ms                                                       | 228 ms: 1.73x slower                                                      |
| pyflate                  | 449 ms                                                       | 778 ms: 1.73x slower                                                      |
| pprint_safe_repr         | 738 ms                                                       | 1.32 sec: 1.78x slower                                                    |
| mako                     | 11.3 ms                                                      | 20.7 ms: 1.83x slower                                                     |
| pprint_pformat           | 1.50 sec                                                     | 2.74 sec: 1.83x slower                                                    |
| comprehensions           | 16.5 us                                                      | 30.3 us: 1.84x slower                                                     |
| genshi_text              | 21.5 ms                                                      | 40.2 ms: 1.86x slower                                                     |
| django_template          | 34.1 ms                                                      | 64.4 ms: 1.89x slower                                                     |
| logging_simple           | 6.16 us                                                      | 11.9 us: 1.93x slower                                                     |
| logging_format           | 6.84 us                                                      | 13.2 us: 1.93x slower                                                     |
| scimark_monte_carlo      | 65.4 ms                                                      | 126 ms: 1.93x slower                                                      |
| float                    | 77.5 ms                                                      | 150 ms: 1.94x slower                                                      |
| sympy_str                | 275 ms                                                       | 540 ms: 1.96x slower                                                      |
| scimark_sor              | 134 ms                                                       | 269 ms: 2.00x slower                                                      |
| unpickle_pure_python     | 210 us                                                       | 422 us: 2.01x slower                                                      |
| richards                 | 45.2 ms                                                      | 91.9 ms: 2.03x slower                                                     |
| logging_silent           | 103 ns                                                       | 212 ns: 2.06x slower                                                      |
| hexiom                   | 5.99 ms                                                      | 12.4 ms: 2.07x slower                                                     |
| richards_super           | 51.6 ms                                                      | 109 ms: 2.10x slower                                                      |
| chaos                    | 57.3 ms                                                      | 121 ms: 2.10x slower                                                      |
| pickle_pure_python       | 294 us                                                       | 621 us: 2.11x slower                                                      |
| sqlglot_transpile        | 1.56 ms                                                      | 3.31 ms: 2.12x slower                                                     |
| go                       | 141 ms                                                       | 303 ms: 2.15x slower                                                      |
| scimark_lu               | 113 ms                                                       | 247 ms: 2.19x slower                                                      |
| sqlglot_parse            | 1.25 ms                                                      | 2.84 ms: 2.28x slower                                                     |
| sympy_expand             | 457 ms                                                       | 1.05 sec: 2.30x slower                                                    |
| nbody                    | 85.1 ms                                                      | 199 ms: 2.34x slower                                                      |
| raytrace                 | 253 ms                                                       | 618 ms: 2.45x slower                                                      |
| sympy_sum                | 156 ms                                                       | 381 ms: 2.45x slower                                                      |
| deltablue                | 3.12 ms                                                      | 9.10 ms: 2.91x slower                                                     |
| unpack_sequence          | 44.8 ns                                                      | 147 ns: 3.28x slower                                                      |
| bench_thread_pool        | 919 us                                                       | 3.49 ms: 3.80x slower                                                     |
| bench_mp_pool            | 11.0 ms                                                      | 72.5 ms: 6.59x slower                                                     |
| Geometric mean           | (ref)                                                        | 1.55x slower                                                              |
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.47x
- 95% likely to have a slowdown of 1.44x
- 99% likely to have a slowdown of 1.39x

# Memory
- memory change: 1.21x