# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: e051157
- commit date: 2024-11-18
- overall geometric mean: 1.57x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.40x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 417 ms: 1.61x slower                                                  |
| docutils       | 2.62 sec                                                     | 3.38 sec: 1.29x slower                                                |
| html5lib       | 67.0 ms                                                      | 105 ms: 1.57x slower                                                  |
| Geometric mean | (ref)                                                        | 1.48x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|--------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets | 520 ms                                                       | 518 ms: 1.01x faster                                                  |
| asyncio_tcp        | 505 ms                                                       | 584 ms: 1.16x slower                                                  |
| asyncio_tcp_ssl    | 1.51 sec                                                     | 1.82 sec: 1.20x slower                                                |
| async_generators   | 377 ms                                                       | 490 ms: 1.30x slower                                                  |
| coroutines         | 23.6 ms                                                      | 31.5 ms: 1.34x slower                                                 |
| Geometric mean     | (ref)                                                        | 1.19x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                  |
| float          | 77.5 ms                                                      | 153 ms: 1.97x slower                                                  |
| nbody          | 85.1 ms                                                      | 205 ms: 2.42x slower                                                  |
| Geometric mean | (ref)                                                        | 1.59x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.99 ms: 1.03x faster                                                 |
| regex_dna      | 180 ms                                                       | 189 ms: 1.05x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                 |
| regex_compile  | 132 ms                                                       | 229 ms: 1.73x slower                                                  |
| Geometric mean | (ref)                                                        | 1.18x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 32.0 us: 1.02x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 135 ms: 1.01x faster                                                  |
| json_loads           | 27.0 us                                                      | 28.6 us: 1.06x slower                                                 |
| pickle_list          | 4.93 us                                                      | 5.23 us: 1.06x slower                                                 |
| unpickle_list        | 4.71 us                                                      | 5.06 us: 1.07x slower                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 109 ms: 1.15x slower                                                  |
| pickle               | 11.3 us                                                      | 13.5 us: 1.19x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 113 ms: 1.33x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 15.3 ms: 1.46x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 93.4 ms: 1.57x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 3.24 sec: 1.61x slower                                                |
| unpickle_pure_python | 210 us                                                       | 423 us: 2.01x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 622 us: 2.11x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.29x slower                                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 82.9 ms: 1.70x slower                                                 |
| mako            | 11.3 ms                                                      | 20.8 ms: 1.84x slower                                                 |
| django_template | 34.1 ms                                                      | 64.9 ms: 1.90x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 41.0 ms: 1.90x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.83x slower                                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|--------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.38 ms: 1.32x faster                                                 |
| pidigits                 | 217 ms                                                       | 185 ms: 1.17x faster                                                  |
| create_gc_cycles         | 1.34 ms                                                      | 1.15 ms: 1.16x faster                                                 |
| regex_effbot             | 3.08 ms                                                      | 2.99 ms: 1.03x faster                                                 |
| pickle_dict              | 32.5 us                                                      | 32.0 us: 1.02x faster                                                 |
| xml_etree_parse          | 136 ms                                                       | 135 ms: 1.01x faster                                                  |
| asyncio_websockets       | 520 ms                                                       | 518 ms: 1.01x faster                                                  |
| regex_dna                | 180 ms                                                       | 189 ms: 1.05x slower                                                  |
| json_loads               | 27.0 us                                                      | 28.6 us: 1.06x slower                                                 |
| pickle_list              | 4.93 us                                                      | 5.23 us: 1.06x slower                                                 |
| unpickle_list            | 4.71 us                                                      | 5.06 us: 1.07x slower                                                 |
| json                     | 4.93 ms                                                      | 5.30 ms: 1.08x slower                                                 |
| regex_v8                 | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                 |
| sqlite_synth             | 2.21 us                                                      | 2.47 us: 1.12x slower                                                 |
| pathlib                  | 19.2 ms                                                      | 21.7 ms: 1.13x slower                                                 |
| xml_etree_iterparse      | 94.9 ms                                                      | 109 ms: 1.15x slower                                                  |
| asyncio_tcp              | 505 ms                                                       | 584 ms: 1.16x slower                                                  |
| telco                    | 7.82 ms                                                      | 9.29 ms: 1.19x slower                                                 |
| pickle                   | 11.3 us                                                      | 13.5 us: 1.19x slower                                                 |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.82 sec: 1.20x slower                                                |
| scimark_fft              | 349 ms                                                       | 425 ms: 1.22x slower                                                  |
| deepcopy                 | 355 us                                                       | 433 us: 1.22x slower                                                  |
| coverage                 | 83.0 ms                                                      | 102 ms: 1.23x slower                                                  |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 6.05 ms: 1.29x slower                                                 |
| docutils                 | 2.62 sec                                                     | 3.38 sec: 1.29x slower                                                |
| async_generators         | 377 ms                                                       | 490 ms: 1.30x slower                                                  |
| xml_etree_generate       | 85.4 ms                                                      | 113 ms: 1.33x slower                                                  |
| pylint                   | 317 ms                                                       | 422 ms: 1.33x slower                                                  |
| coroutines               | 23.6 ms                                                      | 31.5 ms: 1.34x slower                                                 |
| mdp                      | 2.36 sec                                                     | 3.16 sec: 1.34x slower                                                |
| meteor_contest           | 102 ms                                                       | 137 ms: 1.35x slower                                                  |
| deepcopy_memo            | 39.1 us                                                      | 53.6 us: 1.37x slower                                                 |
| bpe_tokeniser            | 4.45 sec                                                     | 6.16 sec: 1.39x slower                                                |
| python_startup_no_site   | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                 |
| dulwich_log              | 74.8 ms                                                      | 105 ms: 1.40x slower                                                  |
| python_startup           | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| spectral_norm            | 111 ms                                                       | 159 ms: 1.44x slower                                                  |
| generators               | 28.8 ms                                                      | 41.5 ms: 1.44x slower                                                 |
| json_dumps               | 10.5 ms                                                      | 15.3 ms: 1.46x slower                                                 |
| deepcopy_reduce          | 3.11 us                                                      | 4.59 us: 1.48x slower                                                 |
| nqueens                  | 78.6 ms                                                      | 116 ms: 1.48x slower                                                  |
| fannkuch                 | 370 ms                                                       | 564 ms: 1.53x slower                                                  |
| pycparser                | 1.12 sec                                                     | 1.73 sec: 1.55x slower                                                |
| html5lib                 | 67.0 ms                                                      | 105 ms: 1.57x slower                                                  |
| xml_etree_process        | 59.3 ms                                                      | 93.4 ms: 1.57x slower                                                 |
| crypto_pyaes             | 67.9 ms                                                      | 109 ms: 1.60x slower                                                  |
| 2to3                     | 260 ms                                                       | 417 ms: 1.61x slower                                                  |
| tomli_loads              | 2.01 sec                                                     | 3.24 sec: 1.61x slower                                                |
| typing_runtime_protocols | 155 us                                                       | 252 us: 1.63x slower                                                  |
| thrift                   | 778 us                                                       | 1.30 ms: 1.67x slower                                                 |
| sympy_integrate          | 19.8 ms                                                      | 33.3 ms: 1.68x slower                                                 |
| genshi_xml               | 48.8 ms                                                      | 82.9 ms: 1.70x slower                                                 |
| sqlglot_normalize        | 106 ms                                                       | 182 ms: 1.72x slower                                                  |
| sqlglot_optimize         | 52.7 ms                                                      | 91.3 ms: 1.73x slower                                                 |
| regex_compile            | 132 ms                                                       | 229 ms: 1.73x slower                                                  |
| pyflate                  | 449 ms                                                       | 786 ms: 1.75x slower                                                  |
| pprint_safe_repr         | 738 ms                                                       | 1.33 sec: 1.81x slower                                                |
| mako                     | 11.3 ms                                                      | 20.8 ms: 1.84x slower                                                 |
| pprint_pformat           | 1.50 sec                                                     | 2.77 sec: 1.85x slower                                                |
| comprehensions           | 16.5 us                                                      | 30.6 us: 1.86x slower                                                 |
| django_template          | 34.1 ms                                                      | 64.9 ms: 1.90x slower                                                 |
| genshi_text              | 21.5 ms                                                      | 41.0 ms: 1.90x slower                                                 |
| float                    | 77.5 ms                                                      | 153 ms: 1.97x slower                                                  |
| logging_simple           | 6.16 us                                                      | 12.2 us: 1.98x slower                                                 |
| sympy_str                | 275 ms                                                       | 543 ms: 1.98x slower                                                  |
| scimark_monte_carlo      | 65.4 ms                                                      | 130 ms: 1.98x slower                                                  |
| logging_format           | 6.84 us                                                      | 13.6 us: 1.99x slower                                                 |
| scimark_sor              | 134 ms                                                       | 270 ms: 2.01x slower                                                  |
| unpickle_pure_python     | 210 us                                                       | 423 us: 2.01x slower                                                  |
| richards                 | 45.2 ms                                                      | 91.6 ms: 2.03x slower                                                 |
| hexiom                   | 5.99 ms                                                      | 12.5 ms: 2.09x slower                                                 |
| logging_silent           | 103 ns                                                       | 216 ns: 2.11x slower                                                  |
| pickle_pure_python       | 294 us                                                       | 622 us: 2.11x slower                                                  |
| sqlglot_transpile        | 1.56 ms                                                      | 3.33 ms: 2.14x slower                                                 |
| go                       | 141 ms                                                       | 301 ms: 2.14x slower                                                  |
| chaos                    | 57.3 ms                                                      | 124 ms: 2.16x slower                                                  |
| richards_super           | 51.6 ms                                                      | 113 ms: 2.19x slower                                                  |
| scimark_lu               | 113 ms                                                       | 248 ms: 2.21x slower                                                  |
| sqlglot_parse            | 1.25 ms                                                      | 2.88 ms: 2.30x slower                                                 |
| sympy_expand             | 457 ms                                                       | 1.06 sec: 2.32x slower                                                |
| nbody                    | 85.1 ms                                                      | 205 ms: 2.42x slower                                                  |
| sympy_sum                | 156 ms                                                       | 382 ms: 2.46x slower                                                  |
| raytrace                 | 253 ms                                                       | 647 ms: 2.56x slower                                                  |
| deltablue                | 3.12 ms                                                      | 9.26 ms: 2.96x slower                                                 |
| unpack_sequence          | 44.8 ns                                                      | 142 ns: 3.17x slower                                                  |
| bench_thread_pool        | 919 us                                                       | 3.49 ms: 3.80x slower                                                 |
| bench_mp_pool            | 11.0 ms                                                      | 72.7 ms: 6.61x slower                                                 |
| Geometric mean           | (ref)                                                        | 1.57x slower                                                          |

Benchmark hidden because not significant (1): unpickle
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.47x
- 95% likely to have a slowdown of 1.45x
- 99% likely to have a slowdown of 1.40x

# Memory
- memory change: 1.21x