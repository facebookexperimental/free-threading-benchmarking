# Results vs. 3.13.0rc2

- fork: python
- ref: 83ba8c2bba834c0b92de
- machine: linux-x86_64
- commit hash: 83ba8c2
- commit date: 2024-11-05
- overall geometric mean: 1.57x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.40x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 418 ms: 1.61x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.40 sec: 1.30x slower                                                 |
| html5lib       | 67.0 ms                                                      | 107 ms: 1.60x slower                                                   |
| Geometric mean | (ref)                                                        | 1.49x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|--------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| asyncio_tcp        | 505 ms                                                       | 586 ms: 1.16x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                                     | 1.84 sec: 1.22x slower                                                 |
| coroutines         | 23.6 ms                                                      | 30.4 ms: 1.29x slower                                                  |
| async_generators   | 377 ms                                                       | 494 ms: 1.31x slower                                                   |
| Geometric mean     | (ref)                                                        | 1.19x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 186 ms: 1.16x faster                                                   |
| float          | 77.5 ms                                                      | 155 ms: 2.00x slower                                                   |
| nbody          | 85.1 ms                                                      | 198 ms: 2.33x slower                                                   |
| Geometric mean | (ref)                                                        | 1.59x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 180 ms                                                       | 185 ms: 1.03x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 25.6 ms: 1.13x slower                                                  |
| regex_compile  | 132 ms                                                       | 231 ms: 1.75x slower                                                   |
| Geometric mean | (ref)                                                        | 1.19x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle               | 11.3 us                                                      | 10.6 us: 1.07x faster                                                  |
| pickle_list          | 4.93 us                                                      | 4.71 us: 1.05x faster                                                  |
| pickle_dict          | 32.5 us                                                      | 31.3 us: 1.04x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 134 ms: 1.02x faster                                                   |
| unpickle_list        | 4.71 us                                                      | 5.00 us: 1.06x slower                                                  |
| unpickle             | 14.3 us                                                      | 15.2 us: 1.06x slower                                                  |
| json_loads           | 27.0 us                                                      | 29.6 us: 1.10x slower                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 110 ms: 1.16x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 113 ms: 1.33x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 15.2 ms: 1.45x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 93.9 ms: 1.58x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 3.27 sec: 1.63x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 422 us: 2.01x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 626 us: 2.12x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.26x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.8 ms: 1.43x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 83.2 ms: 1.71x slower                                                  |
| mako            | 11.3 ms                                                      | 21.0 ms: 1.85x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 41.1 ms: 1.91x slower                                                  |
| django_template | 34.1 ms                                                      | 65.2 ms: 1.91x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.84x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.47 ms: 1.27x faster                                                  |
| create_gc_cycles         | 1.34 ms                                                      | 1.13 ms: 1.18x faster                                                  |
| pidigits                 | 217 ms                                                       | 186 ms: 1.16x faster                                                   |
| pickle                   | 11.3 us                                                      | 10.6 us: 1.07x faster                                                  |
| pickle_list              | 4.93 us                                                      | 4.71 us: 1.05x faster                                                  |
| pickle_dict              | 32.5 us                                                      | 31.3 us: 1.04x faster                                                  |
| xml_etree_parse          | 136 ms                                                       | 134 ms: 1.02x faster                                                   |
| asyncio_websockets       | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| regex_dna                | 180 ms                                                       | 185 ms: 1.03x slower                                                   |
| unpickle_list            | 4.71 us                                                      | 5.00 us: 1.06x slower                                                  |
| unpickle                 | 14.3 us                                                      | 15.2 us: 1.06x slower                                                  |
| json_loads               | 27.0 us                                                      | 29.6 us: 1.10x slower                                                  |
| json                     | 4.93 ms                                                      | 5.46 ms: 1.11x slower                                                  |
| sqlite_synth             | 2.21 us                                                      | 2.45 us: 1.11x slower                                                  |
| regex_v8                 | 22.7 ms                                                      | 25.6 ms: 1.13x slower                                                  |
| pathlib                  | 19.2 ms                                                      | 22.2 ms: 1.16x slower                                                  |
| xml_etree_iterparse      | 94.9 ms                                                      | 110 ms: 1.16x slower                                                   |
| asyncio_tcp              | 505 ms                                                       | 586 ms: 1.16x slower                                                   |
| scimark_fft              | 349 ms                                                       | 415 ms: 1.19x slower                                                   |
| telco                    | 7.82 ms                                                      | 9.39 ms: 1.20x slower                                                  |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.84 sec: 1.22x slower                                                 |
| deepcopy                 | 355 us                                                       | 435 us: 1.22x slower                                                   |
| coverage                 | 83.0 ms                                                      | 104 ms: 1.25x slower                                                   |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 6.03 ms: 1.28x slower                                                  |
| coroutines               | 23.6 ms                                                      | 30.4 ms: 1.29x slower                                                  |
| docutils                 | 2.62 sec                                                     | 3.40 sec: 1.30x slower                                                 |
| async_generators         | 377 ms                                                       | 494 ms: 1.31x slower                                                   |
| mdp                      | 2.36 sec                                                     | 3.12 sec: 1.32x slower                                                 |
| xml_etree_generate       | 85.4 ms                                                      | 113 ms: 1.33x slower                                                   |
| pylint                   | 317 ms                                                       | 424 ms: 1.34x slower                                                   |
| meteor_contest           | 102 ms                                                       | 138 ms: 1.36x slower                                                   |
| deepcopy_memo            | 39.1 us                                                      | 53.8 us: 1.38x slower                                                  |
| bpe_tokeniser            | 4.45 sec                                                     | 6.15 sec: 1.38x slower                                                 |
| python_startup_no_site   | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                  |
| dulwich_log              | 74.8 ms                                                      | 105 ms: 1.40x slower                                                   |
| python_startup           | 11.0 ms                                                      | 15.8 ms: 1.43x slower                                                  |
| json_dumps               | 10.5 ms                                                      | 15.2 ms: 1.45x slower                                                  |
| deepcopy_reduce          | 3.11 us                                                      | 4.55 us: 1.46x slower                                                  |
| generators               | 28.8 ms                                                      | 42.2 ms: 1.47x slower                                                  |
| spectral_norm            | 111 ms                                                       | 164 ms: 1.47x slower                                                   |
| nqueens                  | 78.6 ms                                                      | 116 ms: 1.48x slower                                                   |
| fannkuch                 | 370 ms                                                       | 564 ms: 1.53x slower                                                   |
| pycparser                | 1.12 sec                                                     | 1.72 sec: 1.54x slower                                                 |
| xml_etree_process        | 59.3 ms                                                      | 93.9 ms: 1.58x slower                                                  |
| html5lib                 | 67.0 ms                                                      | 107 ms: 1.60x slower                                                   |
| typing_runtime_protocols | 155 us                                                       | 248 us: 1.60x slower                                                   |
| 2to3                     | 260 ms                                                       | 418 ms: 1.61x slower                                                   |
| crypto_pyaes             | 67.9 ms                                                      | 109 ms: 1.61x slower                                                   |
| tomli_loads              | 2.01 sec                                                     | 3.27 sec: 1.63x slower                                                 |
| thrift                   | 778 us                                                       | 1.27 ms: 1.63x slower                                                  |
| sympy_integrate          | 19.8 ms                                                      | 33.2 ms: 1.67x slower                                                  |
| genshi_xml               | 48.8 ms                                                      | 83.2 ms: 1.71x slower                                                  |
| sqlglot_normalize        | 106 ms                                                       | 181 ms: 1.71x slower                                                   |
| sqlglot_optimize         | 52.7 ms                                                      | 91.0 ms: 1.73x slower                                                  |
| regex_compile            | 132 ms                                                       | 231 ms: 1.75x slower                                                   |
| pyflate                  | 449 ms                                                       | 786 ms: 1.75x slower                                                   |
| pprint_safe_repr         | 738 ms                                                       | 1.34 sec: 1.81x slower                                                 |
| mako                     | 11.3 ms                                                      | 21.0 ms: 1.85x slower                                                  |
| pprint_pformat           | 1.50 sec                                                     | 2.78 sec: 1.86x slower                                                 |
| comprehensions           | 16.5 us                                                      | 30.7 us: 1.87x slower                                                  |
| genshi_text              | 21.5 ms                                                      | 41.1 ms: 1.91x slower                                                  |
| django_template          | 34.1 ms                                                      | 65.2 ms: 1.91x slower                                                  |
| scimark_monte_carlo      | 65.4 ms                                                      | 129 ms: 1.98x slower                                                   |
| sympy_str                | 275 ms                                                       | 543 ms: 1.98x slower                                                   |
| float                    | 77.5 ms                                                      | 155 ms: 2.00x slower                                                   |
| unpickle_pure_python     | 210 us                                                       | 422 us: 2.01x slower                                                   |
| logging_format           | 6.84 us                                                      | 13.8 us: 2.02x slower                                                  |
| logging_simple           | 6.16 us                                                      | 12.5 us: 2.03x slower                                                  |
| scimark_sor              | 134 ms                                                       | 274 ms: 2.04x slower                                                   |
| richards                 | 45.2 ms                                                      | 92.2 ms: 2.04x slower                                                  |
| hexiom                   | 5.99 ms                                                      | 12.5 ms: 2.09x slower                                                  |
| pickle_pure_python       | 294 us                                                       | 626 us: 2.12x slower                                                   |
| logging_silent           | 103 ns                                                       | 223 ns: 2.17x slower                                                   |
| richards_super           | 51.6 ms                                                      | 112 ms: 2.17x slower                                                   |
| chaos                    | 57.3 ms                                                      | 125 ms: 2.17x slower                                                   |
| sqlglot_transpile        | 1.56 ms                                                      | 3.39 ms: 2.17x slower                                                  |
| go                       | 141 ms                                                       | 306 ms: 2.18x slower                                                   |
| scimark_lu               | 113 ms                                                       | 246 ms: 2.18x slower                                                   |
| sympy_expand             | 457 ms                                                       | 1.06 sec: 2.31x slower                                                 |
| nbody                    | 85.1 ms                                                      | 198 ms: 2.33x slower                                                   |
| sqlglot_parse            | 1.25 ms                                                      | 2.91 ms: 2.33x slower                                                  |
| sympy_sum                | 156 ms                                                       | 383 ms: 2.46x slower                                                   |
| raytrace                 | 253 ms                                                       | 651 ms: 2.58x slower                                                   |
| deltablue                | 3.12 ms                                                      | 9.54 ms: 3.05x slower                                                  |
| unpack_sequence          | 44.8 ns                                                      | 146 ns: 3.26x slower                                                   |
| bench_thread_pool        | 919 us                                                       | 3.49 ms: 3.80x slower                                                  |
| bench_mp_pool            | 11.0 ms                                                      | 72.7 ms: 6.62x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.57x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.48x
- 95% likely to have a slowdown of 1.46x
- 99% likely to have a slowdown of 1.40x

# Memory
- memory change: 1.21x