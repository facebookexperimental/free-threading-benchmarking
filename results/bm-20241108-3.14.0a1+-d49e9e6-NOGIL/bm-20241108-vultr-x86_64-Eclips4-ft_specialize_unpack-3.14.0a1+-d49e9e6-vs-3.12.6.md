# Results vs. 3.12.6

- fork: Eclips4
- ref: ft_specialize_unpack
- machine: linux-x86_64
- commit hash: d49e9e6
- commit date: 2024-11-08
- overall geometric mean: 1.52x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.36x slower
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 395 ms: 1.50x slower                                                    |
| docutils       | 2.64 sec                                               | 3.36 sec: 1.27x slower                                                  |
| html5lib       | 63.6 ms                                                | 106 ms: 1.67x slower                                                    |
| Geometric mean | (ref)                                                  | 1.47x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|--------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 521 ms: 1.01x slower                                                    |
| asyncio_tcp        | 519 ms                                                 | 583 ms: 1.12x slower                                                    |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.84 sec: 1.22x slower                                                  |
| async_generators   | 384 ms                                                 | 494 ms: 1.28x slower                                                    |
| coroutines         | 23.9 ms                                                | 31.7 ms: 1.32x slower                                                   |
| Geometric mean     | (ref)                                                  | 1.19x slower                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 185 ms: 1.01x slower                                                    |
| float          | 80.8 ms                                                | 152 ms: 1.88x slower                                                    |
| nbody          | 89.3 ms                                                | 171 ms: 1.91x slower                                                    |
| Geometric mean | (ref)                                                  | 1.54x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.03 ms: 1.04x faster                                                   |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                    |
| regex_v8       | 20.6 ms                                                | 25.0 ms: 1.21x slower                                                   |
| regex_compile  | 142 ms                                                 | 227 ms: 1.60x slower                                                    |
| Geometric mean | (ref)                                                  | 1.20x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                    |
| pickle_dict          | 31.8 us                                                | 31.6 us: 1.01x faster                                                   |
| unpickle             | 14.1 us                                                | 15.0 us: 1.07x slower                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 103 ms: 1.07x slower                                                    |
| pickle_list          | 4.77 us                                                | 5.16 us: 1.08x slower                                                   |
| pickle               | 10.9 us                                                | 12.0 us: 1.10x slower                                                   |
| unpickle_list        | 4.67 us                                                | 5.13 us: 1.10x slower                                                   |
| json_loads           | 26.5 us                                                | 29.8 us: 1.12x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 114 ms: 1.34x slower                                                    |
| json_dumps           | 10.4 ms                                                | 15.3 ms: 1.48x slower                                                   |
| tomli_loads          | 2.11 sec                                               | 3.18 sec: 1.51x slower                                                  |
| xml_etree_process    | 59.0 ms                                                | 93.0 ms: 1.58x slower                                                   |
| unpickle_pure_python | 221 us                                                 | 429 us: 1.94x slower                                                    |
| pickle_pure_python   | 308 us                                                 | 618 us: 2.01x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.27x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                   |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 79.3 ms: 1.58x slower                                                   |
| genshi_text     | 22.8 ms                                                | 40.0 ms: 1.75x slower                                                   |
| django_template | 34.7 ms                                                | 65.0 ms: 1.87x slower                                                   |
| mako            | 11.0 ms                                                | 20.7 ms: 1.88x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.77x slower                                                            |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1+-d49e9e6 |
|--------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.55 ms: 1.35x faster                                                   |
| regex_effbot             | 3.17 ms                                                | 3.03 ms: 1.04x faster                                                   |
| xml_etree_parse          | 139 ms                                                 | 133 ms: 1.04x faster                                                    |
| pickle_dict              | 31.8 us                                                | 31.6 us: 1.01x faster                                                   |
| pidigits                 | 184 ms                                                 | 185 ms: 1.01x slower                                                    |
| asyncio_websockets       | 517 ms                                                 | 521 ms: 1.01x slower                                                    |
| create_gc_cycles         | 1.09 ms                                                | 1.11 ms: 1.01x slower                                                   |
| pathlib                  | 21.5 ms                                                | 22.0 ms: 1.02x slower                                                   |
| unpickle                 | 14.1 us                                                | 15.0 us: 1.07x slower                                                   |
| xml_etree_iterparse      | 96.7 ms                                                | 103 ms: 1.07x slower                                                    |
| json                     | 5.02 ms                                                | 5.43 ms: 1.08x slower                                                   |
| pickle_list              | 4.77 us                                                | 5.16 us: 1.08x slower                                                   |
| pickle                   | 10.9 us                                                | 12.0 us: 1.10x slower                                                   |
| unpickle_list            | 4.67 us                                                | 5.13 us: 1.10x slower                                                   |
| regex_dna                | 168 ms                                                 | 185 ms: 1.10x slower                                                    |
| sqlite_synth             | 2.20 us                                                | 2.47 us: 1.12x slower                                                   |
| json_loads               | 26.5 us                                                | 29.8 us: 1.12x slower                                                   |
| asyncio_tcp              | 519 ms                                                 | 583 ms: 1.12x slower                                                    |
| deepcopy                 | 352 us                                                 | 424 us: 1.20x slower                                                    |
| regex_v8                 | 20.6 ms                                                | 25.0 ms: 1.21x slower                                                   |
| scimark_fft              | 342 ms                                                 | 416 ms: 1.22x slower                                                    |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.84 sec: 1.22x slower                                                  |
| mdp                      | 2.42 sec                                               | 2.97 sec: 1.23x slower                                                  |
| unpack_sequence          | 52.1 ns                                                | 65.8 ns: 1.26x slower                                                   |
| docutils                 | 2.64 sec                                               | 3.36 sec: 1.27x slower                                                  |
| generators               | 32.2 ms                                                | 41.2 ms: 1.28x slower                                                   |
| async_generators         | 384 ms                                                 | 494 ms: 1.28x slower                                                    |
| bpe_tokeniser            | 4.74 sec                                               | 6.12 sec: 1.29x slower                                                  |
| dulwich_log              | 78.9 ms                                                | 104 ms: 1.31x slower                                                    |
| pylint                   | 319 ms                                                 | 421 ms: 1.32x slower                                                    |
| coroutines               | 23.9 ms                                                | 31.7 ms: 1.32x slower                                                   |
| deepcopy_memo            | 40.3 us                                                | 53.5 us: 1.33x slower                                                   |
| spectral_norm            | 110 ms                                                 | 147 ms: 1.33x slower                                                    |
| xml_etree_generate       | 85.2 ms                                                | 114 ms: 1.34x slower                                                    |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.92 ms: 1.35x slower                                                   |
| meteor_contest           | 104 ms                                                 | 141 ms: 1.36x slower                                                    |
| telco                    | 6.53 ms                                                | 9.22 ms: 1.41x slower                                                   |
| crypto_pyaes             | 76.6 ms                                                | 108 ms: 1.42x slower                                                    |
| python_startup_no_site   | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                   |
| coverage                 | 71.4 ms                                                | 103 ms: 1.45x slower                                                    |
| nqueens                  | 80.1 ms                                                | 117 ms: 1.46x slower                                                    |
| pycparser                | 1.17 sec                                               | 1.72 sec: 1.47x slower                                                  |
| deepcopy_reduce          | 3.08 us                                                | 4.53 us: 1.47x slower                                                   |
| json_dumps               | 10.4 ms                                                | 15.3 ms: 1.48x slower                                                   |
| 2to3                     | 264 ms                                                 | 395 ms: 1.50x slower                                                    |
| tomli_loads              | 2.11 sec                                               | 3.18 sec: 1.51x slower                                                  |
| fannkuch                 | 372 ms                                                 | 562 ms: 1.51x slower                                                    |
| typing_runtime_protocols | 163 us                                                 | 254 us: 1.55x slower                                                    |
| comprehensions           | 19.8 us                                                | 30.9 us: 1.56x slower                                                   |
| xml_etree_process        | 59.0 ms                                                | 93.0 ms: 1.58x slower                                                   |
| python_startup           | 9.93 ms                                                | 15.7 ms: 1.58x slower                                                   |
| genshi_xml               | 50.2 ms                                                | 79.3 ms: 1.58x slower                                                   |
| regex_compile            | 142 ms                                                 | 227 ms: 1.60x slower                                                    |
| sympy_integrate          | 20.5 ms                                                | 32.9 ms: 1.60x slower                                                   |
| thrift                   | 791 us                                                 | 1.30 ms: 1.65x slower                                                   |
| sqlglot_normalize        | 107 ms                                                 | 176 ms: 1.65x slower                                                    |
| sqlglot_optimize         | 53.3 ms                                                | 89.1 ms: 1.67x slower                                                   |
| html5lib                 | 63.6 ms                                                | 106 ms: 1.67x slower                                                    |
| pyflate                  | 448 ms                                                 | 773 ms: 1.73x slower                                                    |
| pprint_safe_repr         | 743 ms                                                 | 1.29 sec: 1.74x slower                                                  |
| genshi_text              | 22.8 ms                                                | 40.0 ms: 1.75x slower                                                   |
| pprint_pformat           | 1.52 sec                                               | 2.68 sec: 1.76x slower                                                  |
| sympy_str                | 292 ms                                                 | 528 ms: 1.81x slower                                                    |
| scimark_monte_carlo      | 68.4 ms                                                | 127 ms: 1.86x slower                                                    |
| django_template          | 34.7 ms                                                | 65.0 ms: 1.87x slower                                                   |
| float                    | 80.8 ms                                                | 152 ms: 1.88x slower                                                    |
| mako                     | 11.0 ms                                                | 20.7 ms: 1.88x slower                                                   |
| logging_format           | 7.35 us                                                | 13.9 us: 1.89x slower                                                   |
| logging_simple           | 6.63 us                                                | 12.5 us: 1.89x slower                                                   |
| nbody                    | 89.3 ms                                                | 171 ms: 1.91x slower                                                    |
| chaos                    | 62.8 ms                                                | 122 ms: 1.94x slower                                                    |
| unpickle_pure_python     | 221 us                                                 | 429 us: 1.94x slower                                                    |
| scimark_sor              | 130 ms                                                 | 254 ms: 1.96x slower                                                    |
| sqlglot_transpile        | 1.67 ms                                                | 3.30 ms: 1.97x slower                                                   |
| richards                 | 45.9 ms                                                | 91.4 ms: 1.99x slower                                                   |
| pickle_pure_python       | 308 us                                                 | 618 us: 2.01x slower                                                    |
| hexiom                   | 6.17 ms                                                | 12.5 ms: 2.03x slower                                                   |
| logging_silent           | 109 ns                                                 | 222 ns: 2.03x slower                                                    |
| sqlglot_parse            | 1.36 ms                                                | 2.83 ms: 2.09x slower                                                   |
| raytrace                 | 299 ms                                                 | 628 ms: 2.10x slower                                                    |
| richards_super           | 51.9 ms                                                | 110 ms: 2.12x slower                                                    |
| scimark_lu               | 114 ms                                                 | 244 ms: 2.14x slower                                                    |
| sympy_expand             | 468 ms                                                 | 1.05 sec: 2.23x slower                                                  |
| go                       | 139 ms                                                 | 312 ms: 2.24x slower                                                    |
| sympy_sum                | 166 ms                                                 | 374 ms: 2.26x slower                                                    |
| deltablue                | 3.45 ms                                                | 9.30 ms: 2.70x slower                                                   |
| bench_thread_pool        | 941 us                                                 | 3.47 ms: 3.68x slower                                                   |
| bench_mp_pool            | 10.8 ms                                                | 72.4 ms: 6.70x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.52x slower                                                            |
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.45x
- 95% likely to have a slowdown of 1.42x
- 99% likely to have a slowdown of 1.36x

# Memory
- memory change: 1.24x