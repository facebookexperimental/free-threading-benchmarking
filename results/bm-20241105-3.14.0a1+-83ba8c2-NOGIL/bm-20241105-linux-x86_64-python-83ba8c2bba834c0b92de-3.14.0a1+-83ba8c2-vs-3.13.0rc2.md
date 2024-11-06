# Results vs. 3.13.0rc2

- fork: python
- ref: 83ba8c2bba834c0b92de
- machine: linux-x86_64
- commit hash: 83ba8c2
- commit date: 2024-11-05
- overall geometric mean: 1.60x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.46x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 704 ms: 1.58x slower                                                   |
| docutils       | 4.01 sec                                                     | 5.08 sec: 1.27x slower                                                 |
| html5lib       | 92.6 ms                                                      | 148 ms: 1.60x slower                                                   |
| Geometric mean | (ref)                                                        | 1.47x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|--------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp        | 948 ms                                                       | 1.07 sec: 1.13x slower                                                 |
| asyncio_tcp_ssl    | 2.77 sec                                                     | 3.31 sec: 1.19x slower                                                 |
| asyncio_websockets | 766 ms                                                       | 1.02 sec: 1.34x slower                                                 |
| coroutines         | 30.9 ms                                                      | 41.5 ms: 1.35x slower                                                  |
| async_generators   | 567 ms                                                       | 769 ms: 1.36x slower                                                   |
| Geometric mean     | (ref)                                                        | 1.27x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 230 ms: 1.99x slower                                                   |
| nbody          | 119 ms                                                       | 328 ms: 2.76x slower                                                   |
| Geometric mean | (ref)                                                        | 1.77x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 303 ms: 1.08x slower                                                   |
| regex_v8       | 32.8 ms                                                      | 35.9 ms: 1.09x slower                                                  |
| regex_effbot   | 4.74 ms                                                      | 5.22 ms: 1.10x slower                                                  |
| regex_compile  | 182 ms                                                       | 328 ms: 1.80x slower                                                   |
| Geometric mean | (ref)                                                        | 1.24x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_list          | 6.86 us                                                      | 6.00 us: 1.14x faster                                                  |
| pickle               | 15.1 us                                                      | 16.1 us: 1.06x slower                                                  |
| unpickle_list        | 6.68 us                                                      | 8.17 us: 1.22x slower                                                  |
| unpickle             | 20.5 us                                                      | 26.6 us: 1.30x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 172 ms: 1.41x slower                                                   |
| json_loads           | 34.3 us                                                      | 48.5 us: 1.41x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 21.5 ms: 1.52x slower                                                  |
| tomli_loads          | 2.78 sec                                                     | 4.45 sec: 1.60x slower                                                 |
| xml_etree_process    | 85.9 ms                                                      | 140 ms: 1.63x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 622 us: 2.14x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 907 us: 2.18x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.33x slower                                                           |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_dict, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.9 ms: 1.30x slower                                                  |
| python_startup         | 22.4 ms                                                      | 29.2 ms: 1.30x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.30x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 147 ms: 2.04x slower                                                   |
| django_template | 44.3 ms                                                      | 92.0 ms: 2.08x slower                                                  |
| mako            | 15.9 ms                                                      | 33.8 ms: 2.12x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 67.2 ms: 2.12x slower                                                  |
| Geometric mean  | (ref)                                                        | 2.09x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| create_gc_cycles         | 2.41 ms                                                      | 2.00 ms: 1.21x faster                                                  |
| pickle_list              | 6.86 us                                                      | 6.00 us: 1.14x faster                                                  |
| pickle                   | 15.1 us                                                      | 16.1 us: 1.06x slower                                                  |
| gc_traversal             | 5.70 ms                                                      | 6.13 ms: 1.07x slower                                                  |
| regex_dna                | 282 ms                                                       | 303 ms: 1.08x slower                                                   |
| regex_v8                 | 32.8 ms                                                      | 35.9 ms: 1.09x slower                                                  |
| regex_effbot             | 4.74 ms                                                      | 5.22 ms: 1.10x slower                                                  |
| asyncio_tcp              | 948 ms                                                       | 1.07 sec: 1.13x slower                                                 |
| sqlite_synth             | 3.99 us                                                      | 4.74 us: 1.19x slower                                                  |
| asyncio_tcp_ssl          | 2.77 sec                                                     | 3.31 sec: 1.19x slower                                                 |
| unpickle_list            | 6.68 us                                                      | 8.17 us: 1.22x slower                                                  |
| pathlib                  | 29.9 ms                                                      | 36.6 ms: 1.22x slower                                                  |
| telco                    | 12.2 ms                                                      | 15.2 ms: 1.25x slower                                                  |
| docutils                 | 4.01 sec                                                     | 5.08 sec: 1.27x slower                                                 |
| deepcopy                 | 498 us                                                       | 637 us: 1.28x slower                                                   |
| bench_thread_pool        | 2.89 ms                                                      | 3.74 ms: 1.29x slower                                                  |
| unpickle                 | 20.5 us                                                      | 26.6 us: 1.30x slower                                                  |
| scimark_fft              | 473 ms                                                       | 614 ms: 1.30x slower                                                   |
| python_startup_no_site   | 15.3 ms                                                      | 19.9 ms: 1.30x slower                                                  |
| pylint                   | 470 ms                                                       | 610 ms: 1.30x slower                                                   |
| python_startup           | 22.4 ms                                                      | 29.2 ms: 1.30x slower                                                  |
| mdp                      | 3.80 sec                                                     | 4.99 sec: 1.31x slower                                                 |
| json                     | 6.51 ms                                                      | 8.55 ms: 1.31x slower                                                  |
| asyncio_websockets       | 766 ms                                                       | 1.02 sec: 1.34x slower                                                 |
| coroutines               | 30.9 ms                                                      | 41.5 ms: 1.35x slower                                                  |
| coverage                 | 107 ms                                                       | 145 ms: 1.35x slower                                                   |
| async_generators         | 567 ms                                                       | 769 ms: 1.36x slower                                                   |
| fannkuch                 | 547 ms                                                       | 761 ms: 1.39x slower                                                   |
| xml_etree_generate       | 122 ms                                                       | 172 ms: 1.41x slower                                                   |
| json_loads               | 34.3 us                                                      | 48.5 us: 1.41x slower                                                  |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 9.62 ms: 1.42x slower                                                  |
| meteor_contest           | 150 ms                                                       | 220 ms: 1.47x slower                                                   |
| json_dumps               | 14.1 ms                                                      | 21.5 ms: 1.52x slower                                                  |
| deepcopy_reduce          | 4.10 us                                                      | 6.30 us: 1.54x slower                                                  |
| spectral_norm            | 157 ms                                                       | 244 ms: 1.56x slower                                                   |
| dulwich_log              | 93.7 ms                                                      | 146 ms: 1.56x slower                                                   |
| sympy_integrate          | 30.2 ms                                                      | 47.3 ms: 1.57x slower                                                  |
| crypto_pyaes             | 100 ms                                                       | 158 ms: 1.58x slower                                                   |
| 2to3                     | 445 ms                                                       | 704 ms: 1.58x slower                                                   |
| html5lib                 | 92.6 ms                                                      | 148 ms: 1.60x slower                                                   |
| tomli_loads              | 2.78 sec                                                     | 4.45 sec: 1.60x slower                                                 |
| nqueens                  | 112 ms                                                       | 181 ms: 1.62x slower                                                   |
| deepcopy_memo            | 50.1 us                                                      | 81.5 us: 1.63x slower                                                  |
| xml_etree_process        | 85.9 ms                                                      | 140 ms: 1.63x slower                                                   |
| bpe_tokeniser            | 6.28 sec                                                     | 10.5 sec: 1.67x slower                                                 |
| pycparser                | 1.57 sec                                                     | 2.63 sec: 1.67x slower                                                 |
| generators               | 40.0 ms                                                      | 67.3 ms: 1.68x slower                                                  |
| typing_runtime_protocols | 226 us                                                       | 385 us: 1.71x slower                                                   |
| pyflate                  | 664 ms                                                       | 1.14 sec: 1.71x slower                                                 |
| thrift                   | 1.10 ms                                                      | 1.93 ms: 1.75x slower                                                  |
| pprint_safe_repr         | 987 ms                                                       | 1.78 sec: 1.80x slower                                                 |
| regex_compile            | 182 ms                                                       | 328 ms: 1.80x slower                                                   |
| scimark_monte_carlo      | 90.6 ms                                                      | 164 ms: 1.81x slower                                                   |
| pprint_pformat           | 1.94 sec                                                     | 3.58 sec: 1.84x slower                                                 |
| sqlglot_optimize         | 74.7 ms                                                      | 141 ms: 1.88x slower                                                   |
| sympy_str                | 379 ms                                                       | 721 ms: 1.90x slower                                                   |
| richards                 | 65.5 ms                                                      | 127 ms: 1.93x slower                                                   |
| sqlglot_normalize        | 140 ms                                                       | 271 ms: 1.94x slower                                                   |
| richards_super           | 73.2 ms                                                      | 144 ms: 1.96x slower                                                   |
| logging_simple           | 8.56 us                                                      | 16.9 us: 1.98x slower                                                  |
| float                    | 116 ms                                                       | 230 ms: 1.99x slower                                                   |
| scimark_sor              | 179 ms                                                       | 358 ms: 2.00x slower                                                   |
| genshi_xml               | 72.1 ms                                                      | 147 ms: 2.04x slower                                                   |
| comprehensions           | 22.2 us                                                      | 45.7 us: 2.06x slower                                                  |
| django_template          | 44.3 ms                                                      | 92.0 ms: 2.08x slower                                                  |
| logging_silent           | 130 ns                                                       | 272 ns: 2.10x slower                                                   |
| logging_format           | 9.24 us                                                      | 19.5 us: 2.11x slower                                                  |
| chaos                    | 83.6 ms                                                      | 176 ms: 2.11x slower                                                   |
| mako                     | 15.9 ms                                                      | 33.8 ms: 2.12x slower                                                  |
| genshi_text              | 31.7 ms                                                      | 67.2 ms: 2.12x slower                                                  |
| unpickle_pure_python     | 290 us                                                       | 622 us: 2.14x slower                                                   |
| go                       | 191 ms                                                       | 409 ms: 2.14x slower                                                   |
| pickle_pure_python       | 416 us                                                       | 907 us: 2.18x slower                                                   |
| hexiom                   | 8.11 ms                                                      | 17.9 ms: 2.21x slower                                                  |
| sympy_expand             | 601 ms                                                       | 1.33 sec: 2.22x slower                                                 |
| scimark_lu               | 146 ms                                                       | 326 ms: 2.23x slower                                                   |
| sympy_sum                | 210 ms                                                       | 476 ms: 2.27x slower                                                   |
| sqlglot_transpile        | 2.20 ms                                                      | 5.25 ms: 2.39x slower                                                  |
| sqlglot_parse            | 1.76 ms                                                      | 4.35 ms: 2.48x slower                                                  |
| raytrace                 | 344 ms                                                       | 872 ms: 2.53x slower                                                   |
| nbody                    | 119 ms                                                       | 328 ms: 2.76x slower                                                   |
| deltablue                | 4.44 ms                                                      | 12.8 ms: 2.89x slower                                                  |
| unpack_sequence          | 74.3 ns                                                      | 227 ns: 3.06x slower                                                   |
| bench_mp_pool            | 18.7 ms                                                      | 61.6 ms: 3.30x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.60x slower                                                           |

Benchmark hidden because not significant (4): xml_etree_parse, pickle_dict, pidigits, xml_etree_iterparse
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.56x
- 95% likely to have a slowdown of 1.53x
- 99% likely to have a slowdown of 1.46x

# Memory
- memory change: 1.19x