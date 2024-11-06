# Results vs. 3.12.6

- fork: python
- ref: 83ba8c2bba834c0b92de
- machine: linux-x86_64
- commit hash: 83ba8c2
- commit date: 2024-11-05
- overall geometric mean: 1.55x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.38x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 418 ms: 1.59x slower                                                   |
| docutils       | 2.64 sec                                               | 3.40 sec: 1.29x slower                                                 |
| html5lib       | 63.6 ms                                                | 107 ms: 1.68x slower                                                   |
| Geometric mean | (ref)                                                  | 1.51x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp      | 519 ms                                                 | 586 ms: 1.13x slower                                                   |
| asyncio_tcp_ssl  | 1.51 sec                                               | 1.84 sec: 1.22x slower                                                 |
| coroutines       | 23.9 ms                                                | 30.4 ms: 1.27x slower                                                  |
| async_generators | 384 ms                                                 | 494 ms: 1.28x slower                                                   |
| Geometric mean   | (ref)                                                  | 1.18x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                   |
| float          | 80.8 ms                                                | 155 ms: 1.92x slower                                                   |
| nbody          | 89.3 ms                                                | 198 ms: 2.22x slower                                                   |
| Geometric mean | (ref)                                                  | 1.63x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.08 ms: 1.03x faster                                                  |
| regex_dna      | 168 ms                                                 | 185 ms: 1.10x slower                                                   |
| regex_v8       | 20.6 ms                                                | 25.6 ms: 1.25x slower                                                  |
| regex_compile  | 142 ms                                                 | 231 ms: 1.62x slower                                                   |
| Geometric mean | (ref)                                                  | 1.21x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle               | 10.9 us                                                | 10.6 us: 1.04x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.03x faster                                                   |
| pickle_dict          | 31.8 us                                                | 31.3 us: 1.01x faster                                                  |
| pickle_list          | 4.77 us                                                | 4.71 us: 1.01x faster                                                  |
| unpickle_list        | 4.67 us                                                | 5.00 us: 1.07x slower                                                  |
| unpickle             | 14.1 us                                                | 15.2 us: 1.08x slower                                                  |
| json_loads           | 26.5 us                                                | 29.6 us: 1.12x slower                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 110 ms: 1.14x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 113 ms: 1.33x slower                                                   |
| json_dumps           | 10.4 ms                                                | 15.2 ms: 1.47x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 3.27 sec: 1.55x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 93.9 ms: 1.59x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 422 us: 1.91x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 626 us: 2.03x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.26x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.51x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 83.2 ms: 1.66x slower                                                  |
| genshi_text     | 22.8 ms                                                | 41.1 ms: 1.80x slower                                                  |
| django_template | 34.7 ms                                                | 65.2 ms: 1.88x slower                                                  |
| mako            | 11.0 ms                                                | 21.0 ms: 1.91x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.81x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.47 ms: 1.40x faster                                                  |
| pickle                   | 10.9 us                                                | 10.6 us: 1.04x faster                                                  |
| xml_etree_parse          | 139 ms                                                 | 134 ms: 1.03x faster                                                   |
| regex_effbot             | 3.17 ms                                                | 3.08 ms: 1.03x faster                                                  |
| pickle_dict              | 31.8 us                                                | 31.3 us: 1.01x faster                                                  |
| pickle_list              | 4.77 us                                                | 4.71 us: 1.01x faster                                                  |
| pidigits                 | 184 ms                                                 | 186 ms: 1.01x slower                                                   |
| pathlib                  | 21.5 ms                                                | 22.2 ms: 1.03x slower                                                  |
| create_gc_cycles         | 1.09 ms                                                | 1.13 ms: 1.04x slower                                                  |
| unpickle_list            | 4.67 us                                                | 5.00 us: 1.07x slower                                                  |
| unpickle                 | 14.1 us                                                | 15.2 us: 1.08x slower                                                  |
| json                     | 5.02 ms                                                | 5.46 ms: 1.09x slower                                                  |
| regex_dna                | 168 ms                                                 | 185 ms: 1.10x slower                                                   |
| sqlite_synth             | 2.20 us                                                | 2.45 us: 1.11x slower                                                  |
| json_loads               | 26.5 us                                                | 29.6 us: 1.12x slower                                                  |
| asyncio_tcp              | 519 ms                                                 | 586 ms: 1.13x slower                                                   |
| xml_etree_iterparse      | 96.7 ms                                                | 110 ms: 1.14x slower                                                   |
| scimark_fft              | 342 ms                                                 | 415 ms: 1.21x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.84 sec: 1.22x slower                                                 |
| deepcopy                 | 352 us                                                 | 435 us: 1.24x slower                                                   |
| regex_v8                 | 20.6 ms                                                | 25.6 ms: 1.25x slower                                                  |
| coroutines               | 23.9 ms                                                | 30.4 ms: 1.27x slower                                                  |
| async_generators         | 384 ms                                                 | 494 ms: 1.28x slower                                                   |
| mdp                      | 2.42 sec                                               | 3.12 sec: 1.29x slower                                                 |
| docutils                 | 2.64 sec                                               | 3.40 sec: 1.29x slower                                                 |
| bpe_tokeniser            | 4.74 sec                                               | 6.15 sec: 1.30x slower                                                 |
| generators               | 32.2 ms                                                | 42.2 ms: 1.31x slower                                                  |
| dulwich_log              | 78.9 ms                                                | 105 ms: 1.33x slower                                                   |
| xml_etree_generate       | 85.2 ms                                                | 113 ms: 1.33x slower                                                   |
| pylint                   | 319 ms                                                 | 424 ms: 1.33x slower                                                   |
| deepcopy_memo            | 40.3 us                                                | 53.8 us: 1.34x slower                                                  |
| meteor_contest           | 104 ms                                                 | 138 ms: 1.34x slower                                                   |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 6.03 ms: 1.37x slower                                                  |
| crypto_pyaes             | 76.6 ms                                                | 109 ms: 1.43x slower                                                   |
| python_startup_no_site   | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                  |
| telco                    | 6.53 ms                                                | 9.39 ms: 1.44x slower                                                  |
| coverage                 | 71.4 ms                                                | 104 ms: 1.45x slower                                                   |
| nqueens                  | 80.1 ms                                                | 116 ms: 1.45x slower                                                   |
| pycparser                | 1.17 sec                                               | 1.72 sec: 1.47x slower                                                 |
| json_dumps               | 10.4 ms                                                | 15.2 ms: 1.47x slower                                                  |
| deepcopy_reduce          | 3.08 us                                                | 4.55 us: 1.48x slower                                                  |
| spectral_norm            | 110 ms                                                 | 164 ms: 1.48x slower                                                   |
| fannkuch                 | 372 ms                                                 | 564 ms: 1.52x slower                                                   |
| typing_runtime_protocols | 163 us                                                 | 248 us: 1.52x slower                                                   |
| comprehensions           | 19.8 us                                                | 30.7 us: 1.55x slower                                                  |
| tomli_loads              | 2.11 sec                                               | 3.27 sec: 1.55x slower                                                 |
| 2to3                     | 264 ms                                                 | 418 ms: 1.59x slower                                                   |
| python_startup           | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                  |
| xml_etree_process        | 59.0 ms                                                | 93.9 ms: 1.59x slower                                                  |
| thrift                   | 791 us                                                 | 1.27 ms: 1.61x slower                                                  |
| sympy_integrate          | 20.5 ms                                                | 33.2 ms: 1.61x slower                                                  |
| regex_compile            | 142 ms                                                 | 231 ms: 1.62x slower                                                   |
| genshi_xml               | 50.2 ms                                                | 83.2 ms: 1.66x slower                                                  |
| html5lib                 | 63.6 ms                                                | 107 ms: 1.68x slower                                                   |
| sqlglot_normalize        | 107 ms                                                 | 181 ms: 1.70x slower                                                   |
| sqlglot_optimize         | 53.3 ms                                                | 91.0 ms: 1.71x slower                                                  |
| pyflate                  | 448 ms                                                 | 786 ms: 1.75x slower                                                   |
| pprint_safe_repr         | 743 ms                                                 | 1.34 sec: 1.80x slower                                                 |
| genshi_text              | 22.8 ms                                                | 41.1 ms: 1.80x slower                                                  |
| pprint_pformat           | 1.52 sec                                               | 2.78 sec: 1.83x slower                                                 |
| sympy_str                | 292 ms                                                 | 543 ms: 1.86x slower                                                   |
| logging_format           | 7.35 us                                                | 13.8 us: 1.88x slower                                                  |
| django_template          | 34.7 ms                                                | 65.2 ms: 1.88x slower                                                  |
| scimark_monte_carlo      | 68.4 ms                                                | 129 ms: 1.89x slower                                                   |
| logging_simple           | 6.63 us                                                | 12.5 us: 1.89x slower                                                  |
| mako                     | 11.0 ms                                                | 21.0 ms: 1.91x slower                                                  |
| unpickle_pure_python     | 221 us                                                 | 422 us: 1.91x slower                                                   |
| float                    | 80.8 ms                                                | 155 ms: 1.92x slower                                                   |
| chaos                    | 62.8 ms                                                | 125 ms: 1.98x slower                                                   |
| richards                 | 45.9 ms                                                | 92.2 ms: 2.01x slower                                                  |
| sqlglot_transpile        | 1.67 ms                                                | 3.39 ms: 2.03x slower                                                  |
| hexiom                   | 6.17 ms                                                | 12.5 ms: 2.03x slower                                                  |
| pickle_pure_python       | 308 us                                                 | 626 us: 2.03x slower                                                   |
| logging_silent           | 109 ns                                                 | 223 ns: 2.04x slower                                                   |
| scimark_sor              | 130 ms                                                 | 274 ms: 2.11x slower                                                   |
| sqlglot_parse            | 1.36 ms                                                | 2.91 ms: 2.15x slower                                                  |
| scimark_lu               | 114 ms                                                 | 246 ms: 2.15x slower                                                   |
| richards_super           | 51.9 ms                                                | 112 ms: 2.16x slower                                                   |
| raytrace                 | 299 ms                                                 | 651 ms: 2.18x slower                                                   |
| go                       | 139 ms                                                 | 306 ms: 2.20x slower                                                   |
| nbody                    | 89.3 ms                                                | 198 ms: 2.22x slower                                                   |
| sympy_expand             | 468 ms                                                 | 1.06 sec: 2.26x slower                                                 |
| sympy_sum                | 166 ms                                                 | 383 ms: 2.30x slower                                                   |
| deltablue                | 3.45 ms                                                | 9.54 ms: 2.77x slower                                                  |
| unpack_sequence          | 52.1 ns                                                | 146 ns: 2.81x slower                                                   |
| bench_thread_pool        | 941 us                                                 | 3.49 ms: 3.71x slower                                                  |
| bench_mp_pool            | 10.8 ms                                                | 72.7 ms: 6.74x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.55x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.45x
- 95% likely to have a slowdown of 1.44x
- 99% likely to have a slowdown of 1.38x

# Memory
- memory change: 1.23x