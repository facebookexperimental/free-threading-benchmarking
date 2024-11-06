# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_integ
- machine: linux-x86_64
- commit hash: 0a68813
- commit date: 2024-10-31
- overall geometric mean: 1.47x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.38x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 688 ms: 1.51x slower                                                 |
| docutils       | 4.00 sec                                               | 4.88 sec: 1.22x slower                                               |
| html5lib       | 88.9 ms                                                | 146 ms: 1.64x slower                                                 |
| tornado_http   | 266 ms                                                 | 332 ms: 1.25x slower                                                 |
| Geometric mean | (ref)                                                  | 1.39x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|--------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_tcp_ssl    | 2.81 sec                                               | 3.21 sec: 1.14x slower                                               |
| asyncio_tcp        | 923 ms                                                 | 1.08 sec: 1.17x slower                                               |
| async_generators   | 589 ms                                                 | 735 ms: 1.25x slower                                                 |
| asyncio_websockets | 748 ms                                                 | 1.02 sec: 1.36x slower                                               |
| coroutines         | 29.5 ms                                                | 40.4 ms: 1.37x slower                                                |
| Geometric mean     | (ref)                                                  | 1.25x slower                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 237 ms: 1.05x faster                                                 |
| float          | 123 ms                                                 | 216 ms: 1.75x slower                                                 |
| nbody          | 119 ms                                                 | 309 ms: 2.59x slower                                                 |
| Geometric mean | (ref)                                                  | 1.63x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 278 ms                                                 | 298 ms: 1.07x slower                                                 |
| regex_v8       | 32.5 ms                                                | 35.9 ms: 1.11x slower                                                |
| regex_compile  | 187 ms                                                 | 311 ms: 1.67x slower                                                 |
| Geometric mean | (ref)                                                  | 1.19x slower                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 43.4 us: 1.22x faster                                                |
| pickle_list          | 6.97 us                                                | 5.97 us: 1.17x faster                                                |
| xml_etree_parse      | 241 ms                                                 | 229 ms: 1.05x faster                                                 |
| json_loads           | 37.9 us                                                | 43.0 us: 1.14x slower                                                |
| unpickle             | 21.2 us                                                | 25.7 us: 1.21x slower                                                |
| unpickle_list        | 6.83 us                                                | 8.31 us: 1.22x slower                                                |
| xml_etree_generate   | 127 ms                                                 | 165 ms: 1.30x slower                                                 |
| json_dumps           | 14.3 ms                                                | 20.4 ms: 1.42x slower                                                |
| tomli_loads          | 2.88 sec                                               | 4.33 sec: 1.50x slower                                               |
| xml_etree_process    | 83.7 ms                                                | 128 ms: 1.53x slower                                                 |
| unpickle_pure_python | 300 us                                                 | 521 us: 1.74x slower                                                 |
| pickle_pure_python   | 436 us                                                 | 769 us: 1.77x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.21x slower                                                         |

Benchmark hidden because not significant (2): pickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.4 ms: 1.10x slower                                                |
| python_startup         | 23.7 ms                                                | 29.2 ms: 1.23x slower                                                |
| Geometric mean         | (ref)                                                  | 1.16x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 117 ms: 1.74x slower                                                 |
| django_template | 44.9 ms                                                | 83.1 ms: 1.85x slower                                                |
| mako            | 15.7 ms                                                | 30.6 ms: 1.94x slower                                                |
| genshi_text     | 30.2 ms                                                | 62.1 ms: 2.06x slower                                                |
| Geometric mean  | (ref)                                                  | 1.89x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-linux-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict              | 52.7 us                                                | 43.4 us: 1.22x faster                                                |
| pickle_list              | 6.97 us                                                | 5.97 us: 1.17x faster                                                |
| gc_traversal             | 5.86 ms                                                | 5.04 ms: 1.16x faster                                                |
| pidigits                 | 250 ms                                                 | 237 ms: 1.05x faster                                                 |
| xml_etree_parse          | 241 ms                                                 | 229 ms: 1.05x faster                                                 |
| regex_dna                | 278 ms                                                 | 298 ms: 1.07x slower                                                 |
| pathlib                  | 31.6 ms                                                | 34.3 ms: 1.09x slower                                                |
| sqlite_synth             | 3.87 us                                                | 4.23 us: 1.09x slower                                                |
| python_startup_no_site   | 17.6 ms                                                | 19.4 ms: 1.10x slower                                                |
| regex_v8                 | 32.5 ms                                                | 35.9 ms: 1.11x slower                                                |
| scimark_fft              | 500 ms                                                 | 564 ms: 1.13x slower                                                 |
| json_loads               | 37.9 us                                                | 43.0 us: 1.14x slower                                                |
| asyncio_tcp_ssl          | 2.81 sec                                               | 3.21 sec: 1.14x slower                                               |
| asyncio_tcp              | 923 ms                                                 | 1.08 sec: 1.17x slower                                               |
| deepcopy                 | 468 us                                                 | 555 us: 1.19x slower                                                 |
| json                     | 6.85 ms                                                | 8.26 ms: 1.21x slower                                                |
| unpickle                 | 21.2 us                                                | 25.7 us: 1.21x slower                                                |
| unpickle_list            | 6.83 us                                                | 8.31 us: 1.22x slower                                                |
| docutils                 | 4.00 sec                                               | 4.88 sec: 1.22x slower                                               |
| python_startup           | 23.7 ms                                                | 29.2 ms: 1.23x slower                                                |
| scimark_sparse_mat_mult  | 6.70 ms                                                | 8.27 ms: 1.23x slower                                                |
| pylint                   | 465 ms                                                 | 577 ms: 1.24x slower                                                 |
| tornado_http             | 266 ms                                                 | 332 ms: 1.25x slower                                                 |
| async_generators         | 589 ms                                                 | 735 ms: 1.25x slower                                                 |
| deepcopy_memo            | 52.4 us                                                | 67.9 us: 1.29x slower                                                |
| mdp                      | 3.97 sec                                               | 5.15 sec: 1.30x slower                                               |
| xml_etree_generate       | 127 ms                                                 | 165 ms: 1.30x slower                                                 |
| nqueens                  | 117 ms                                                 | 158 ms: 1.35x slower                                                 |
| asyncio_websockets       | 748 ms                                                 | 1.02 sec: 1.36x slower                                               |
| meteor_contest           | 146 ms                                                 | 200 ms: 1.36x slower                                                 |
| pycparser                | 1.79 sec                                               | 2.45 sec: 1.37x slower                                               |
| coroutines               | 29.5 ms                                                | 40.4 ms: 1.37x slower                                                |
| dulwich_log              | 100 ms                                                 | 139 ms: 1.39x slower                                                 |
| bpe_tokeniser            | 6.59 sec                                               | 9.26 sec: 1.41x slower                                               |
| fannkuch                 | 540 ms                                                 | 766 ms: 1.42x slower                                                 |
| json_dumps               | 14.3 ms                                                | 20.4 ms: 1.42x slower                                                |
| generators               | 41.1 ms                                                | 58.8 ms: 1.43x slower                                                |
| crypto_pyaes             | 107 ms                                                 | 154 ms: 1.43x slower                                                 |
| deepcopy_reduce          | 4.04 us                                                | 5.79 us: 1.44x slower                                                |
| sqlglot_normalize        | 157 ms                                                 | 229 ms: 1.46x slower                                                 |
| telco                    | 9.59 ms                                                | 14.1 ms: 1.47x slower                                                |
| pyflate                  | 727 ms                                                 | 1.08 sec: 1.48x slower                                               |
| coverage                 | 95.4 ms                                                | 141 ms: 1.48x slower                                                 |
| spectral_norm            | 156 ms                                                 | 231 ms: 1.48x slower                                                 |
| sympy_integrate          | 29.8 ms                                                | 44.6 ms: 1.50x slower                                                |
| tomli_loads              | 2.88 sec                                               | 4.33 sec: 1.50x slower                                               |
| 2to3                     | 456 ms                                                 | 688 ms: 1.51x slower                                                 |
| xml_etree_process        | 83.7 ms                                                | 128 ms: 1.53x slower                                                 |
| typing_runtime_protocols | 224 us                                                 | 347 us: 1.55x slower                                                 |
| sqlglot_optimize         | 76.0 ms                                                | 119 ms: 1.56x slower                                                 |
| scimark_monte_carlo      | 96.4 ms                                                | 153 ms: 1.59x slower                                                 |
| pprint_safe_repr         | 967 ms                                                 | 1.55 sec: 1.61x slower                                               |
| pprint_pformat           | 1.98 sec                                               | 3.22 sec: 1.63x slower                                               |
| html5lib                 | 88.9 ms                                                | 146 ms: 1.64x slower                                                 |
| thrift                   | 1.06 ms                                                | 1.74 ms: 1.65x slower                                                |
| regex_compile            | 187 ms                                                 | 311 ms: 1.67x slower                                                 |
| comprehensions           | 27.1 us                                                | 45.2 us: 1.67x slower                                                |
| sympy_str                | 385 ms                                                 | 660 ms: 1.71x slower                                                 |
| genshi_xml               | 67.6 ms                                                | 117 ms: 1.74x slower                                                 |
| unpickle_pure_python     | 300 us                                                 | 521 us: 1.74x slower                                                 |
| float                    | 123 ms                                                 | 216 ms: 1.75x slower                                                 |
| pickle_pure_python       | 436 us                                                 | 769 us: 1.77x slower                                                 |
| logging_simple           | 9.45 us                                                | 16.8 us: 1.78x slower                                                |
| logging_silent           | 139 ns                                                 | 249 ns: 1.79x slower                                                 |
| richards                 | 60.3 ms                                                | 109 ms: 1.80x slower                                                 |
| scimark_lu               | 152 ms                                                 | 274 ms: 1.80x slower                                                 |
| raytrace                 | 408 ms                                                 | 744 ms: 1.82x slower                                                 |
| django_template          | 44.9 ms                                                | 83.1 ms: 1.85x slower                                                |
| logging_format           | 9.59 us                                                | 17.9 us: 1.86x slower                                                |
| hexiom                   | 8.27 ms                                                | 15.7 ms: 1.90x slower                                                |
| richards_super           | 72.8 ms                                                | 140 ms: 1.92x slower                                                 |
| mako                     | 15.7 ms                                                | 30.6 ms: 1.94x slower                                                |
| chaos                    | 84.9 ms                                                | 166 ms: 1.96x slower                                                 |
| sqlglot_transpile        | 2.34 ms                                                | 4.70 ms: 2.01x slower                                                |
| genshi_text              | 30.2 ms                                                | 62.1 ms: 2.06x slower                                                |
| scimark_sor              | 167 ms                                                 | 344 ms: 2.06x slower                                                 |
| go                       | 172 ms                                                 | 361 ms: 2.10x slower                                                 |
| sympy_sum                | 222 ms                                                 | 477 ms: 2.15x slower                                                 |
| sympy_expand             | 582 ms                                                 | 1.27 sec: 2.18x slower                                               |
| sqlglot_parse            | 1.79 ms                                                | 4.10 ms: 2.29x slower                                                |
| nbody                    | 119 ms                                                 | 309 ms: 2.59x slower                                                 |
| deltablue                | 4.27 ms                                                | 11.8 ms: 2.77x slower                                                |
| bench_mp_pool            | 20.7 ms                                                | 58.4 ms: 2.82x slower                                                |
| unpack_sequence          | 60.2 ns                                                | 218 ns: 3.63x slower                                                 |
| Geometric mean           | (ref)                                                  | 1.47x slower                                                         |

Benchmark hidden because not significant (5): pickle, create_gc_cycles, regex_effbot, xml_etree_iterparse, bench_thread_pool
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.41x
- 95% likely to have a slowdown of 1.39x
- 99% likely to have a slowdown of 1.38x

# Memory
- memory change: 1.19x