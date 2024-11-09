# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: 0e50451
- commit date: 2024-11-08
- overall geometric mean: 1.44x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.32x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 435 ms                                                                 | 656 ms: 1.51x slower                                                  |
| docutils       | 3.81 sec                                                               | 4.56 sec: 1.20x slower                                                |
| html5lib       | 87.0 ms                                                                | 141 ms: 1.62x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.43x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_tcp_ssl  | 2.75 sec                                                               | 3.21 sec: 1.17x slower                                                |
| asyncio_tcp      | 895 ms                                                                 | 1.08 sec: 1.21x slower                                                |
| async_generators | 572 ms                                                                 | 706 ms: 1.23x slower                                                  |
| coroutines       | 31.0 ms                                                                | 41.5 ms: 1.34x slower                                                 |
| Geometric mean   | (ref)                                                                  | 1.18x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 241 ms                                                                 | 271 ms: 1.12x slower                                                  |
| float          | 118 ms                                                                 | 188 ms: 1.59x slower                                                  |
| nbody          | 126 ms                                                                 | 266 ms: 2.11x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.56x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 283 ms                                                                 | 299 ms: 1.05x slower                                                  |
| regex_v8       | 33.1 ms                                                                | 36.2 ms: 1.09x slower                                                 |
| regex_compile  | 174 ms                                                                 | 290 ms: 1.67x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.18x slower                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_list          | 7.29 us                                                                | 6.77 us: 1.08x faster                                                 |
| json_loads           | 38.2 us                                                                | 43.1 us: 1.13x slower                                                 |
| unpickle             | 18.9 us                                                                | 21.6 us: 1.14x slower                                                 |
| unpickle_list        | 7.06 us                                                                | 8.36 us: 1.18x slower                                                 |
| json_dumps           | 15.8 ms                                                                | 19.4 ms: 1.23x slower                                                 |
| xml_etree_generate   | 119 ms                                                                 | 157 ms: 1.31x slower                                                  |
| xml_etree_process    | 81.7 ms                                                                | 122 ms: 1.49x slower                                                  |
| tomli_loads          | 2.67 sec                                                               | 4.03 sec: 1.51x slower                                                |
| pickle_pure_python   | 445 us                                                                 | 759 us: 1.71x slower                                                  |
| unpickle_pure_python | 302 us                                                                 | 530 us: 1.76x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.21x slower                                                          |

Benchmark hidden because not significant (4): pickle_dict, xml_etree_parse, pickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 14.7 ms                                                                | 20.9 ms: 1.42x slower                                                 |
| python_startup         | 20.7 ms                                                                | 29.8 ms: 1.44x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.43x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 48.5 ms                                                                | 75.9 ms: 1.57x slower                                                 |
| genshi_xml      | 66.0 ms                                                                | 109 ms: 1.65x slower                                                  |
| genshi_text     | 30.4 ms                                                                | 50.7 ms: 1.67x slower                                                 |
| mako            | 17.1 ms                                                                | 30.1 ms: 1.77x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.66x slower                                                          |

All benchmarks:
===============

| Benchmark                | bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-linux-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|--------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal             | 5.47 ms                                                                | 4.09 ms: 1.34x faster                                                 |
| create_gc_cycles         | 2.34 ms                                                                | 2.02 ms: 1.16x faster                                                 |
| bench_mp_pool            | 74.4 ms                                                                | 64.3 ms: 1.16x faster                                                 |
| pickle_list              | 7.29 us                                                                | 6.77 us: 1.08x faster                                                 |
| regex_dna                | 283 ms                                                                 | 299 ms: 1.05x slower                                                  |
| regex_v8                 | 33.1 ms                                                                | 36.2 ms: 1.09x slower                                                 |
| json                     | 6.65 ms                                                                | 7.43 ms: 1.12x slower                                                 |
| pidigits                 | 241 ms                                                                 | 271 ms: 1.12x slower                                                  |
| json_loads               | 38.2 us                                                                | 43.1 us: 1.13x slower                                                 |
| unpickle                 | 18.9 us                                                                | 21.6 us: 1.14x slower                                                 |
| scimark_fft              | 492 ms                                                                 | 569 ms: 1.16x slower                                                  |
| asyncio_tcp_ssl          | 2.75 sec                                                               | 3.21 sec: 1.17x slower                                                |
| dulwich_log              | 112 ms                                                                 | 132 ms: 1.18x slower                                                  |
| unpickle_list            | 7.06 us                                                                | 8.36 us: 1.18x slower                                                 |
| pylint                   | 461 ms                                                                 | 547 ms: 1.19x slower                                                  |
| docutils                 | 3.81 sec                                                               | 4.56 sec: 1.20x slower                                                |
| asyncio_tcp              | 895 ms                                                                 | 1.08 sec: 1.21x slower                                                |
| json_dumps               | 15.8 ms                                                                | 19.4 ms: 1.23x slower                                                 |
| bench_thread_pool        | 3.17 ms                                                                | 3.89 ms: 1.23x slower                                                 |
| telco                    | 10.6 ms                                                                | 13.0 ms: 1.23x slower                                                 |
| async_generators         | 572 ms                                                                 | 706 ms: 1.23x slower                                                  |
| pathlib                  | 27.0 ms                                                                | 34.0 ms: 1.26x slower                                                 |
| coverage                 | 113 ms                                                                 | 145 ms: 1.28x slower                                                  |
| pycparser                | 1.66 sec                                                               | 2.14 sec: 1.29x slower                                                |
| meteor_contest           | 139 ms                                                                 | 182 ms: 1.30x slower                                                  |
| xml_etree_generate       | 119 ms                                                                 | 157 ms: 1.31x slower                                                  |
| mdp                      | 3.78 sec                                                               | 4.98 sec: 1.32x slower                                                |
| coroutines               | 31.0 ms                                                                | 41.5 ms: 1.34x slower                                                 |
| generators               | 41.0 ms                                                                | 56.1 ms: 1.37x slower                                                 |
| typing_runtime_protocols | 229 us                                                                 | 318 us: 1.39x slower                                                  |
| deepcopy_reduce          | 3.63 us                                                                | 5.15 us: 1.42x slower                                                 |
| python_startup_no_site   | 14.7 ms                                                                | 20.9 ms: 1.42x slower                                                 |
| python_startup           | 20.7 ms                                                                | 29.8 ms: 1.44x slower                                                 |
| deepcopy                 | 359 us                                                                 | 517 us: 1.44x slower                                                  |
| sqlglot_normalize        | 143 ms                                                                 | 207 ms: 1.44x slower                                                  |
| nqueens                  | 106 ms                                                                 | 154 ms: 1.45x slower                                                  |
| scimark_sparse_mat_mult  | 6.57 ms                                                                | 9.71 ms: 1.48x slower                                                 |
| xml_etree_process        | 81.7 ms                                                                | 122 ms: 1.49x slower                                                  |
| crypto_pyaes             | 101 ms                                                                 | 151 ms: 1.49x slower                                                  |
| sqlglot_optimize         | 74.7 ms                                                                | 112 ms: 1.50x slower                                                  |
| spectral_norm            | 151 ms                                                                 | 228 ms: 1.51x slower                                                  |
| 2to3                     | 435 ms                                                                 | 656 ms: 1.51x slower                                                  |
| tomli_loads              | 2.67 sec                                                               | 4.03 sec: 1.51x slower                                                |
| sympy_integrate          | 28.1 ms                                                                | 42.6 ms: 1.52x slower                                                 |
| fannkuch                 | 509 ms                                                                 | 775 ms: 1.52x slower                                                  |
| thrift                   | 1.09 ms                                                                | 1.67 ms: 1.53x slower                                                 |
| bpe_tokeniser            | 5.86 sec                                                               | 8.96 sec: 1.53x slower                                                |
| deepcopy_memo            | 41.5 us                                                                | 64.9 us: 1.56x slower                                                 |
| django_template          | 48.5 ms                                                                | 75.9 ms: 1.57x slower                                                 |
| pyflate                  | 660 ms                                                                 | 1.04 sec: 1.58x slower                                                |
| richards                 | 63.6 ms                                                                | 101 ms: 1.59x slower                                                  |
| pprint_pformat           | 1.92 sec                                                               | 3.04 sec: 1.59x slower                                                |
| pprint_safe_repr         | 948 ms                                                                 | 1.51 sec: 1.59x slower                                                |
| float                    | 118 ms                                                                 | 188 ms: 1.59x slower                                                  |
| html5lib                 | 87.0 ms                                                                | 141 ms: 1.62x slower                                                  |
| genshi_xml               | 66.0 ms                                                                | 109 ms: 1.65x slower                                                  |
| genshi_text              | 30.4 ms                                                                | 50.7 ms: 1.67x slower                                                 |
| regex_compile            | 174 ms                                                                 | 290 ms: 1.67x slower                                                  |
| pickle_pure_python       | 445 us                                                                 | 759 us: 1.71x slower                                                  |
| comprehensions           | 22.6 us                                                                | 39.2 us: 1.73x slower                                                 |
| scimark_lu               | 152 ms                                                                 | 265 ms: 1.74x slower                                                  |
| scimark_monte_carlo      | 88.5 ms                                                                | 155 ms: 1.76x slower                                                  |
| unpickle_pure_python     | 302 us                                                                 | 530 us: 1.76x slower                                                  |
| mako                     | 17.1 ms                                                                | 30.1 ms: 1.77x slower                                                 |
| sympy_str                | 354 ms                                                                 | 630 ms: 1.78x slower                                                  |
| logging_simple           | 8.12 us                                                                | 14.8 us: 1.83x slower                                                 |
| hexiom                   | 8.39 ms                                                                | 15.5 ms: 1.84x slower                                                 |
| logging_format           | 9.26 us                                                                | 17.3 us: 1.87x slower                                                 |
| chaos                    | 85.3 ms                                                                | 160 ms: 1.87x slower                                                  |
| richards_super           | 71.5 ms                                                                | 137 ms: 1.92x slower                                                  |
| sympy_expand             | 623 ms                                                                 | 1.20 sec: 1.93x slower                                                |
| logging_silent           | 136 ns                                                                 | 267 ns: 1.97x slower                                                  |
| sqlglot_transpile        | 2.25 ms                                                                | 4.61 ms: 2.05x slower                                                 |
| scimark_sor              | 162 ms                                                                 | 342 ms: 2.11x slower                                                  |
| nbody                    | 126 ms                                                                 | 266 ms: 2.11x slower                                                  |
| raytrace                 | 347 ms                                                                 | 754 ms: 2.17x slower                                                  |
| sympy_sum                | 205 ms                                                                 | 446 ms: 2.17x slower                                                  |
| sqlglot_parse            | 1.72 ms                                                                | 3.79 ms: 2.20x slower                                                 |
| go                       | 157 ms                                                                 | 361 ms: 2.29x slower                                                  |
| deltablue                | 4.60 ms                                                                | 11.3 ms: 2.45x slower                                                 |
| unpack_sequence          | 59.3 ns                                                                | 190 ns: 3.21x slower                                                  |
| Geometric mean           | (ref)                                                                  | 1.44x slower                                                          |

Benchmark hidden because not significant (7): pickle_dict, asyncio_websockets, xml_etree_parse, pickle, regex_effbot, xml_etree_iterparse, sqlite_synth

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.40x
- 95% likely to have a slowdown of 1.37x
- 99% likely to have a slowdown of 1.32x

# Memory
- memory change: 1.18x