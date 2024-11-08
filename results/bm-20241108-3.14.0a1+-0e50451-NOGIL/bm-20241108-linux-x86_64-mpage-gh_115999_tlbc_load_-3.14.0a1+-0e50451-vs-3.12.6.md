# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: 0e50451
- commit date: 2024-11-08
- overall geometric mean: 1.42x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.30x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 656 ms: 1.44x slower                                                  |
| docutils       | 4.00 sec                                               | 4.56 sec: 1.14x slower                                                |
| html5lib       | 88.9 ms                                                | 141 ms: 1.59x slower                                                  |
| Geometric mean | (ref)                                                  | 1.38x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_tcp_ssl  | 2.81 sec                                               | 3.21 sec: 1.14x slower                                                |
| asyncio_tcp      | 923 ms                                                 | 1.08 sec: 1.17x slower                                                |
| async_generators | 589 ms                                                 | 706 ms: 1.20x slower                                                  |
| coroutines       | 29.5 ms                                                | 41.5 ms: 1.41x slower                                                 |
| Geometric mean   | (ref)                                                  | 1.17x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 271 ms: 1.08x slower                                                  |
| float          | 123 ms                                                 | 188 ms: 1.53x slower                                                  |
| nbody          | 119 ms                                                 | 266 ms: 2.24x slower                                                  |
| Geometric mean | (ref)                                                  | 1.55x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 278 ms                                                 | 299 ms: 1.07x slower                                                  |
| regex_v8       | 32.5 ms                                                | 36.2 ms: 1.11x slower                                                 |
| regex_compile  | 187 ms                                                 | 290 ms: 1.55x slower                                                  |
| Geometric mean | (ref)                                                  | 1.17x slower                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 45.5 us: 1.16x faster                                                 |
| xml_etree_parse      | 241 ms                                                 | 216 ms: 1.11x faster                                                  |
| pickle               | 16.4 us                                                | 17.4 us: 1.06x slower                                                 |
| json_loads           | 37.9 us                                                | 43.1 us: 1.14x slower                                                 |
| unpickle_list        | 6.83 us                                                | 8.36 us: 1.22x slower                                                 |
| xml_etree_generate   | 127 ms                                                 | 157 ms: 1.23x slower                                                  |
| json_dumps           | 14.3 ms                                                | 19.4 ms: 1.35x slower                                                 |
| tomli_loads          | 2.88 sec                                               | 4.03 sec: 1.40x slower                                                |
| xml_etree_process    | 83.7 ms                                                | 122 ms: 1.45x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 759 us: 1.74x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 530 us: 1.77x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.19x slower                                                          |

Benchmark hidden because not significant (3): pickle_list, xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.9 ms: 1.19x slower                                                 |
| python_startup         | 23.7 ms                                                | 29.8 ms: 1.26x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 109 ms: 1.61x slower                                                  |
| genshi_text     | 30.2 ms                                                | 50.7 ms: 1.68x slower                                                 |
| django_template | 44.9 ms                                                | 75.9 ms: 1.69x slower                                                 |
| mako            | 15.7 ms                                                | 30.1 ms: 1.91x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.72x slower                                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|--------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal             | 5.86 ms                                                | 4.09 ms: 1.43x faster                                                 |
| pickle_dict              | 52.7 us                                                | 45.5 us: 1.16x faster                                                 |
| xml_etree_parse          | 241 ms                                                 | 216 ms: 1.11x faster                                                  |
| sqlite_synth             | 3.87 us                                                | 4.12 us: 1.06x slower                                                 |
| pickle                   | 16.4 us                                                | 17.4 us: 1.06x slower                                                 |
| regex_dna                | 278 ms                                                 | 299 ms: 1.07x slower                                                  |
| pathlib                  | 31.6 ms                                                | 34.0 ms: 1.07x slower                                                 |
| pidigits                 | 250 ms                                                 | 271 ms: 1.08x slower                                                  |
| json                     | 6.85 ms                                                | 7.43 ms: 1.08x slower                                                 |
| deepcopy                 | 468 us                                                 | 517 us: 1.11x slower                                                  |
| regex_v8                 | 32.5 ms                                                | 36.2 ms: 1.11x slower                                                 |
| bench_thread_pool        | 3.48 ms                                                | 3.89 ms: 1.12x slower                                                 |
| json_loads               | 37.9 us                                                | 43.1 us: 1.14x slower                                                 |
| scimark_fft              | 500 ms                                                 | 569 ms: 1.14x slower                                                  |
| asyncio_tcp_ssl          | 2.81 sec                                               | 3.21 sec: 1.14x slower                                                |
| docutils                 | 4.00 sec                                               | 4.56 sec: 1.14x slower                                                |
| asyncio_tcp              | 923 ms                                                 | 1.08 sec: 1.17x slower                                                |
| pylint                   | 465 ms                                                 | 547 ms: 1.18x slower                                                  |
| python_startup_no_site   | 17.6 ms                                                | 20.9 ms: 1.19x slower                                                 |
| pycparser                | 1.79 sec                                               | 2.14 sec: 1.20x slower                                                |
| async_generators         | 589 ms                                                 | 706 ms: 1.20x slower                                                  |
| unpickle_list            | 6.83 us                                                | 8.36 us: 1.22x slower                                                 |
| xml_etree_generate       | 127 ms                                                 | 157 ms: 1.23x slower                                                  |
| deepcopy_memo            | 52.4 us                                                | 64.9 us: 1.24x slower                                                 |
| meteor_contest           | 146 ms                                                 | 182 ms: 1.24x slower                                                  |
| mdp                      | 3.97 sec                                               | 4.98 sec: 1.26x slower                                                |
| python_startup           | 23.7 ms                                                | 29.8 ms: 1.26x slower                                                 |
| deepcopy_reduce          | 4.04 us                                                | 5.15 us: 1.28x slower                                                 |
| sqlglot_normalize        | 157 ms                                                 | 207 ms: 1.32x slower                                                  |
| dulwich_log              | 100 ms                                                 | 132 ms: 1.32x slower                                                  |
| nqueens                  | 117 ms                                                 | 154 ms: 1.32x slower                                                  |
| json_dumps               | 14.3 ms                                                | 19.4 ms: 1.35x slower                                                 |
| telco                    | 9.59 ms                                                | 13.0 ms: 1.36x slower                                                 |
| bpe_tokeniser            | 6.59 sec                                               | 8.96 sec: 1.36x slower                                                |
| generators               | 41.1 ms                                                | 56.1 ms: 1.36x slower                                                 |
| tomli_loads              | 2.88 sec                                               | 4.03 sec: 1.40x slower                                                |
| coroutines               | 29.5 ms                                                | 41.5 ms: 1.41x slower                                                 |
| crypto_pyaes             | 107 ms                                                 | 151 ms: 1.41x slower                                                  |
| typing_runtime_protocols | 224 us                                                 | 318 us: 1.42x slower                                                  |
| sympy_integrate          | 29.8 ms                                                | 42.6 ms: 1.43x slower                                                 |
| fannkuch                 | 540 ms                                                 | 775 ms: 1.43x slower                                                  |
| pyflate                  | 727 ms                                                 | 1.04 sec: 1.43x slower                                                |
| 2to3                     | 456 ms                                                 | 656 ms: 1.44x slower                                                  |
| comprehensions           | 27.1 us                                                | 39.2 us: 1.45x slower                                                 |
| scimark_sparse_mat_mult  | 6.70 ms                                                | 9.71 ms: 1.45x slower                                                 |
| xml_etree_process        | 83.7 ms                                                | 122 ms: 1.45x slower                                                  |
| spectral_norm            | 156 ms                                                 | 228 ms: 1.47x slower                                                  |
| sqlglot_optimize         | 76.0 ms                                                | 112 ms: 1.48x slower                                                  |
| coverage                 | 95.4 ms                                                | 145 ms: 1.52x slower                                                  |
| float                    | 123 ms                                                 | 188 ms: 1.53x slower                                                  |
| pprint_pformat           | 1.98 sec                                               | 3.04 sec: 1.54x slower                                                |
| regex_compile            | 187 ms                                                 | 290 ms: 1.55x slower                                                  |
| pprint_safe_repr         | 967 ms                                                 | 1.51 sec: 1.56x slower                                                |
| logging_simple           | 9.45 us                                                | 14.8 us: 1.57x slower                                                 |
| thrift                   | 1.06 ms                                                | 1.67 ms: 1.57x slower                                                 |
| html5lib                 | 88.9 ms                                                | 141 ms: 1.59x slower                                                  |
| genshi_xml               | 67.6 ms                                                | 109 ms: 1.61x slower                                                  |
| scimark_monte_carlo      | 96.4 ms                                                | 155 ms: 1.61x slower                                                  |
| sympy_str                | 385 ms                                                 | 630 ms: 1.64x slower                                                  |
| richards                 | 60.3 ms                                                | 101 ms: 1.67x slower                                                  |
| genshi_text              | 30.2 ms                                                | 50.7 ms: 1.68x slower                                                 |
| django_template          | 44.9 ms                                                | 75.9 ms: 1.69x slower                                                 |
| scimark_lu               | 152 ms                                                 | 265 ms: 1.74x slower                                                  |
| pickle_pure_python       | 436 us                                                 | 759 us: 1.74x slower                                                  |
| unpickle_pure_python     | 300 us                                                 | 530 us: 1.77x slower                                                  |
| logging_format           | 9.59 us                                                | 17.3 us: 1.81x slower                                                 |
| raytrace                 | 408 ms                                                 | 754 ms: 1.85x slower                                                  |
| hexiom                   | 8.27 ms                                                | 15.5 ms: 1.87x slower                                                 |
| richards_super           | 72.8 ms                                                | 137 ms: 1.88x slower                                                  |
| chaos                    | 84.9 ms                                                | 160 ms: 1.88x slower                                                  |
| mako                     | 15.7 ms                                                | 30.1 ms: 1.91x slower                                                 |
| logging_silent           | 139 ns                                                 | 267 ns: 1.92x slower                                                  |
| sqlglot_transpile        | 2.34 ms                                                | 4.61 ms: 1.97x slower                                                 |
| sympy_sum                | 222 ms                                                 | 446 ms: 2.01x slower                                                  |
| scimark_sor              | 167 ms                                                 | 342 ms: 2.05x slower                                                  |
| sympy_expand             | 582 ms                                                 | 1.20 sec: 2.06x slower                                                |
| go                       | 172 ms                                                 | 361 ms: 2.09x slower                                                  |
| sqlglot_parse            | 1.79 ms                                                | 3.79 ms: 2.12x slower                                                 |
| nbody                    | 119 ms                                                 | 266 ms: 2.24x slower                                                  |
| deltablue                | 4.27 ms                                                | 11.3 ms: 2.64x slower                                                 |
| bench_mp_pool            | 20.7 ms                                                | 64.3 ms: 3.11x slower                                                 |
| unpack_sequence          | 60.2 ns                                                | 190 ns: 3.16x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.42x slower                                                          |

Benchmark hidden because not significant (6): pickle_list, asyncio_websockets, xml_etree_iterparse, regex_effbot, unpickle, create_gc_cycles
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.36x
- 95% likely to have a slowdown of 1.35x
- 99% likely to have a slowdown of 1.30x

# Memory
- memory change: 1.19x