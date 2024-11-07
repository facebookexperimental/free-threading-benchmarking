# Results vs. 3.13.0rc2

- fork: python
- ref: 2a6b6b33dfe0f3c435ab
- machine: linux-x86_64
- commit hash: 2a6b6b3
- commit date: 2024-11-06
- overall geometric mean: 1.57x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.40x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 417 ms: 1.61x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.41 sec: 1.30x slower                                                 |
| html5lib       | 67.0 ms                                                      | 107 ms: 1.60x slower                                                   |
| Geometric mean | (ref)                                                        | 1.50x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 520 ms                                                       | 516 ms: 1.01x faster                                                   |
| asyncio_tcp        | 505 ms                                                       | 584 ms: 1.16x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                                     | 1.84 sec: 1.22x slower                                                 |
| coroutines         | 23.6 ms                                                      | 31.2 ms: 1.32x slower                                                  |
| async_generators   | 377 ms                                                       | 499 ms: 1.32x slower                                                   |
| Geometric mean     | (ref)                                                        | 1.20x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 188 ms: 1.15x faster                                                   |
| float          | 77.5 ms                                                      | 152 ms: 1.96x slower                                                   |
| nbody          | 85.1 ms                                                      | 205 ms: 2.41x slower                                                   |
| Geometric mean | (ref)                                                        | 1.60x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 3.19 ms: 1.03x slower                                                  |
| regex_dna      | 180 ms                                                       | 189 ms: 1.05x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 25.2 ms: 1.11x slower                                                  |
| regex_compile  | 132 ms                                                       | 233 ms: 1.76x slower                                                   |
| Geometric mean | (ref)                                                        | 1.21x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_list          | 4.93 us                                                      | 4.73 us: 1.04x faster                                                  |
| pickle               | 11.3 us                                                      | 10.9 us: 1.04x faster                                                  |
| pickle_dict          | 32.5 us                                                      | 31.4 us: 1.04x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 134 ms: 1.02x faster                                                   |
| unpickle             | 14.3 us                                                      | 14.9 us: 1.04x slower                                                  |
| unpickle_list        | 4.71 us                                                      | 4.91 us: 1.04x slower                                                  |
| json_loads           | 27.0 us                                                      | 29.9 us: 1.11x slower                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 110 ms: 1.15x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 114 ms: 1.33x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 15.2 ms: 1.45x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 94.9 ms: 1.60x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 3.22 sec: 1.61x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 417 us: 1.99x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 627 us: 2.13x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.26x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 82.2 ms: 1.69x slower                                                  |
| mako            | 11.3 ms                                                      | 20.6 ms: 1.82x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 40.3 ms: 1.87x slower                                                  |
| django_template | 34.1 ms                                                      | 64.9 ms: 1.90x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.82x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.47 ms: 1.27x faster                                                  |
| create_gc_cycles         | 1.34 ms                                                      | 1.13 ms: 1.18x faster                                                  |
| pidigits                 | 217 ms                                                       | 188 ms: 1.15x faster                                                   |
| pickle_list              | 4.93 us                                                      | 4.73 us: 1.04x faster                                                  |
| pickle                   | 11.3 us                                                      | 10.9 us: 1.04x faster                                                  |
| pickle_dict              | 32.5 us                                                      | 31.4 us: 1.04x faster                                                  |
| xml_etree_parse          | 136 ms                                                       | 134 ms: 1.02x faster                                                   |
| asyncio_websockets       | 520 ms                                                       | 516 ms: 1.01x faster                                                   |
| regex_effbot             | 3.08 ms                                                      | 3.19 ms: 1.03x slower                                                  |
| unpickle                 | 14.3 us                                                      | 14.9 us: 1.04x slower                                                  |
| unpickle_list            | 4.71 us                                                      | 4.91 us: 1.04x slower                                                  |
| regex_dna                | 180 ms                                                       | 189 ms: 1.05x slower                                                   |
| json_loads               | 27.0 us                                                      | 29.9 us: 1.11x slower                                                  |
| json                     | 4.93 ms                                                      | 5.46 ms: 1.11x slower                                                  |
| regex_v8                 | 22.7 ms                                                      | 25.2 ms: 1.11x slower                                                  |
| sqlite_synth             | 2.21 us                                                      | 2.48 us: 1.12x slower                                                  |
| xml_etree_iterparse      | 94.9 ms                                                      | 110 ms: 1.15x slower                                                   |
| asyncio_tcp              | 505 ms                                                       | 584 ms: 1.16x slower                                                   |
| pathlib                  | 19.2 ms                                                      | 22.3 ms: 1.16x slower                                                  |
| telco                    | 7.82 ms                                                      | 9.36 ms: 1.20x slower                                                  |
| scimark_fft              | 349 ms                                                       | 418 ms: 1.20x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.84 sec: 1.22x slower                                                 |
| coverage                 | 83.0 ms                                                      | 102 ms: 1.23x slower                                                   |
| deepcopy                 | 355 us                                                       | 437 us: 1.23x slower                                                   |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 6.10 ms: 1.30x slower                                                  |
| docutils                 | 2.62 sec                                                     | 3.41 sec: 1.30x slower                                                 |
| coroutines               | 23.6 ms                                                      | 31.2 ms: 1.32x slower                                                  |
| async_generators         | 377 ms                                                       | 499 ms: 1.32x slower                                                   |
| xml_etree_generate       | 85.4 ms                                                      | 114 ms: 1.33x slower                                                   |
| pylint                   | 317 ms                                                       | 424 ms: 1.34x slower                                                   |
| mdp                      | 2.36 sec                                                     | 3.16 sec: 1.34x slower                                                 |
| meteor_contest           | 102 ms                                                       | 138 ms: 1.36x slower                                                   |
| deepcopy_memo            | 39.1 us                                                      | 53.1 us: 1.36x slower                                                  |
| bpe_tokeniser            | 4.45 sec                                                     | 6.14 sec: 1.38x slower                                                 |
| python_startup_no_site   | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                  |
| dulwich_log              | 74.8 ms                                                      | 104 ms: 1.39x slower                                                   |
| python_startup           | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                  |
| json_dumps               | 10.5 ms                                                      | 15.2 ms: 1.45x slower                                                  |
| nqueens                  | 78.6 ms                                                      | 115 ms: 1.46x slower                                                   |
| deepcopy_reduce          | 3.11 us                                                      | 4.55 us: 1.46x slower                                                  |
| generators               | 28.8 ms                                                      | 42.5 ms: 1.48x slower                                                  |
| spectral_norm            | 111 ms                                                       | 166 ms: 1.49x slower                                                   |
| fannkuch                 | 370 ms                                                       | 565 ms: 1.53x slower                                                   |
| pycparser                | 1.12 sec                                                     | 1.74 sec: 1.56x slower                                                 |
| crypto_pyaes             | 67.9 ms                                                      | 108 ms: 1.58x slower                                                   |
| html5lib                 | 67.0 ms                                                      | 107 ms: 1.60x slower                                                   |
| xml_etree_process        | 59.3 ms                                                      | 94.9 ms: 1.60x slower                                                  |
| tomli_loads              | 2.01 sec                                                     | 3.22 sec: 1.61x slower                                                 |
| 2to3                     | 260 ms                                                       | 417 ms: 1.61x slower                                                   |
| typing_runtime_protocols | 155 us                                                       | 251 us: 1.62x slower                                                   |
| thrift                   | 778 us                                                       | 1.30 ms: 1.67x slower                                                  |
| sympy_integrate          | 19.8 ms                                                      | 33.2 ms: 1.67x slower                                                  |
| genshi_xml               | 48.8 ms                                                      | 82.2 ms: 1.69x slower                                                  |
| sqlglot_normalize        | 106 ms                                                       | 181 ms: 1.72x slower                                                   |
| sqlglot_optimize         | 52.7 ms                                                      | 90.9 ms: 1.72x slower                                                  |
| pyflate                  | 449 ms                                                       | 775 ms: 1.73x slower                                                   |
| regex_compile            | 132 ms                                                       | 233 ms: 1.76x slower                                                   |
| pprint_safe_repr         | 738 ms                                                       | 1.33 sec: 1.80x slower                                                 |
| mako                     | 11.3 ms                                                      | 20.6 ms: 1.82x slower                                                  |
| pprint_pformat           | 1.50 sec                                                     | 2.75 sec: 1.84x slower                                                 |
| genshi_text              | 21.5 ms                                                      | 40.3 ms: 1.87x slower                                                  |
| comprehensions           | 16.5 us                                                      | 30.8 us: 1.87x slower                                                  |
| django_template          | 34.1 ms                                                      | 64.9 ms: 1.90x slower                                                  |
| float                    | 77.5 ms                                                      | 152 ms: 1.96x slower                                                   |
| scimark_monte_carlo      | 65.4 ms                                                      | 128 ms: 1.96x slower                                                   |
| sympy_str                | 275 ms                                                       | 543 ms: 1.98x slower                                                   |
| unpickle_pure_python     | 210 us                                                       | 417 us: 1.99x slower                                                   |
| richards                 | 45.2 ms                                                      | 90.6 ms: 2.00x slower                                                  |
| logging_format           | 6.84 us                                                      | 13.8 us: 2.01x slower                                                  |
| logging_simple           | 6.16 us                                                      | 12.6 us: 2.04x slower                                                  |
| scimark_sor              | 134 ms                                                       | 275 ms: 2.04x slower                                                   |
| hexiom                   | 5.99 ms                                                      | 12.4 ms: 2.08x slower                                                  |
| logging_silent           | 103 ns                                                       | 214 ns: 2.08x slower                                                   |
| go                       | 141 ms                                                       | 299 ms: 2.12x slower                                                   |
| pickle_pure_python       | 294 us                                                       | 627 us: 2.13x slower                                                   |
| richards_super           | 51.6 ms                                                      | 111 ms: 2.14x slower                                                   |
| sqlglot_transpile        | 1.56 ms                                                      | 3.34 ms: 2.14x slower                                                  |
| chaos                    | 57.3 ms                                                      | 123 ms: 2.15x slower                                                   |
| scimark_lu               | 113 ms                                                       | 248 ms: 2.21x slower                                                   |
| sqlglot_parse            | 1.25 ms                                                      | 2.87 ms: 2.30x slower                                                  |
| sympy_expand             | 457 ms                                                       | 1.06 sec: 2.31x slower                                                 |
| nbody                    | 85.1 ms                                                      | 205 ms: 2.41x slower                                                   |
| sympy_sum                | 156 ms                                                       | 382 ms: 2.45x slower                                                   |
| raytrace                 | 253 ms                                                       | 635 ms: 2.51x slower                                                   |
| deltablue                | 3.12 ms                                                      | 9.22 ms: 2.95x slower                                                  |
| unpack_sequence          | 44.8 ns                                                      | 153 ns: 3.41x slower                                                   |
| bench_thread_pool        | 919 us                                                       | 3.49 ms: 3.80x slower                                                  |
| bench_mp_pool            | 11.0 ms                                                      | 72.6 ms: 6.60x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.57x slower                                                           |
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.48x
- 95% likely to have a slowdown of 1.46x
- 99% likely to have a slowdown of 1.40x

# Memory
- memory change: 1.22x