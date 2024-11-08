# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: 0e50451
- commit date: 2024-11-08
- overall geometric mean: 1.49x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.35x slower
- Memory change: 1.24x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 410 ms: 1.56x slower                                                  |
| docutils       | 2.64 sec                                               | 3.31 sec: 1.25x slower                                                |
| html5lib       | 63.6 ms                                                | 105 ms: 1.66x slower                                                  |
| Geometric mean | (ref)                                                  | 1.48x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|--------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 521 ms: 1.01x slower                                                  |
| asyncio_tcp        | 519 ms                                                 | 581 ms: 1.12x slower                                                  |
| coroutines         | 23.9 ms                                                | 28.9 ms: 1.21x slower                                                 |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.83 sec: 1.22x slower                                                |
| async_generators   | 384 ms                                                 | 480 ms: 1.25x slower                                                  |
| Geometric mean     | (ref)                                                  | 1.16x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 182 ms: 1.01x faster                                                  |
| float          | 80.8 ms                                                | 149 ms: 1.85x slower                                                  |
| nbody          | 89.3 ms                                                | 199 ms: 2.23x slower                                                  |
| Geometric mean | (ref)                                                  | 1.60x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.20 ms: 1.01x slower                                                 |
| regex_dna      | 168 ms                                                 | 186 ms: 1.11x slower                                                  |
| regex_v8       | 20.6 ms                                                | 25.1 ms: 1.22x slower                                                 |
| regex_compile  | 142 ms                                                 | 212 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                  | 1.19x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.04x faster                                                  |
| pickle_dict          | 31.8 us                                                | 31.6 us: 1.01x faster                                                 |
| unpickle             | 14.1 us                                                | 14.6 us: 1.04x slower                                                 |
| unpickle_list        | 4.67 us                                                | 5.01 us: 1.07x slower                                                 |
| pickle_list          | 4.77 us                                                | 5.13 us: 1.08x slower                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 106 ms: 1.10x slower                                                  |
| pickle               | 10.9 us                                                | 12.0 us: 1.10x slower                                                 |
| json_loads           | 26.5 us                                                | 29.4 us: 1.11x slower                                                 |
| xml_etree_generate   | 85.2 ms                                                | 109 ms: 1.28x slower                                                  |
| json_dumps           | 10.4 ms                                                | 14.7 ms: 1.42x slower                                                 |
| tomli_loads          | 2.11 sec                                               | 3.12 sec: 1.48x slower                                                |
| xml_etree_process    | 59.0 ms                                                | 89.3 ms: 1.51x slower                                                 |
| unpickle_pure_python | 221 us                                                 | 389 us: 1.76x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 577 us: 1.87x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.24x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.58x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 74.3 ms: 1.48x slower                                                 |
| genshi_text     | 22.8 ms                                                | 36.2 ms: 1.59x slower                                                 |
| django_template | 34.7 ms                                                | 59.2 ms: 1.71x slower                                                 |
| mako            | 11.0 ms                                                | 20.2 ms: 1.83x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.65x slower                                                          |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|--------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.46 ms: 1.41x faster                                                 |
| xml_etree_parse          | 139 ms                                                 | 134 ms: 1.04x faster                                                  |
| pidigits                 | 184 ms                                                 | 182 ms: 1.01x faster                                                  |
| pathlib                  | 21.5 ms                                                | 21.4 ms: 1.01x faster                                                 |
| pickle_dict              | 31.8 us                                                | 31.6 us: 1.01x faster                                                 |
| asyncio_websockets       | 517 ms                                                 | 521 ms: 1.01x slower                                                  |
| regex_effbot             | 3.17 ms                                                | 3.20 ms: 1.01x slower                                                 |
| create_gc_cycles         | 1.09 ms                                                | 1.11 ms: 1.02x slower                                                 |
| unpickle                 | 14.1 us                                                | 14.6 us: 1.04x slower                                                 |
| json                     | 5.02 ms                                                | 5.35 ms: 1.07x slower                                                 |
| unpickle_list            | 4.67 us                                                | 5.01 us: 1.07x slower                                                 |
| pickle_list              | 4.77 us                                                | 5.13 us: 1.08x slower                                                 |
| xml_etree_iterparse      | 96.7 ms                                                | 106 ms: 1.10x slower                                                  |
| pickle                   | 10.9 us                                                | 12.0 us: 1.10x slower                                                 |
| deepcopy                 | 352 us                                                 | 387 us: 1.10x slower                                                  |
| sqlite_synth             | 2.20 us                                                | 2.43 us: 1.10x slower                                                 |
| json_loads               | 26.5 us                                                | 29.4 us: 1.11x slower                                                 |
| regex_dna                | 168 ms                                                 | 186 ms: 1.11x slower                                                  |
| asyncio_tcp              | 519 ms                                                 | 581 ms: 1.12x slower                                                  |
| deepcopy_memo            | 40.3 us                                                | 46.7 us: 1.16x slower                                                 |
| scimark_fft              | 342 ms                                                 | 410 ms: 1.20x slower                                                  |
| coroutines               | 23.9 ms                                                | 28.9 ms: 1.21x slower                                                 |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.83 sec: 1.22x slower                                                |
| regex_v8                 | 20.6 ms                                                | 25.1 ms: 1.22x slower                                                 |
| bpe_tokeniser            | 4.74 sec                                               | 5.79 sec: 1.22x slower                                                |
| async_generators         | 384 ms                                                 | 480 ms: 1.25x slower                                                  |
| docutils                 | 2.64 sec                                               | 3.31 sec: 1.25x slower                                                |
| xml_etree_generate       | 85.2 ms                                                | 109 ms: 1.28x slower                                                  |
| generators               | 32.2 ms                                                | 41.3 ms: 1.28x slower                                                 |
| pylint                   | 319 ms                                                 | 409 ms: 1.28x slower                                                  |
| dulwich_log              | 78.9 ms                                                | 103 ms: 1.30x slower                                                  |
| meteor_contest           | 104 ms                                                 | 136 ms: 1.31x slower                                                  |
| mdp                      | 2.42 sec                                               | 3.19 sec: 1.32x slower                                                |
| deepcopy_reduce          | 3.08 us                                                | 4.10 us: 1.33x slower                                                 |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.97 ms: 1.36x slower                                                 |
| typing_runtime_protocols | 163 us                                                 | 226 us: 1.38x slower                                                  |
| nqueens                  | 80.1 ms                                                | 112 ms: 1.40x slower                                                  |
| crypto_pyaes             | 76.6 ms                                                | 108 ms: 1.41x slower                                                  |
| telco                    | 6.53 ms                                                | 9.19 ms: 1.41x slower                                                 |
| coverage                 | 71.4 ms                                                | 101 ms: 1.41x slower                                                  |
| spectral_norm            | 110 ms                                                 | 156 ms: 1.41x slower                                                  |
| json_dumps               | 10.4 ms                                                | 14.7 ms: 1.42x slower                                                 |
| python_startup_no_site   | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                 |
| pycparser                | 1.17 sec                                               | 1.68 sec: 1.43x slower                                                |
| tomli_loads              | 2.11 sec                                               | 3.12 sec: 1.48x slower                                                |
| genshi_xml               | 50.2 ms                                                | 74.3 ms: 1.48x slower                                                 |
| regex_compile            | 142 ms                                                 | 212 ms: 1.49x slower                                                  |
| comprehensions           | 19.8 us                                                | 29.8 us: 1.50x slower                                                 |
| fannkuch                 | 372 ms                                                 | 562 ms: 1.51x slower                                                  |
| xml_etree_process        | 59.0 ms                                                | 89.3 ms: 1.51x slower                                                 |
| sqlglot_optimize         | 53.3 ms                                                | 82.1 ms: 1.54x slower                                                 |
| sqlglot_normalize        | 107 ms                                                 | 164 ms: 1.54x slower                                                  |
| 2to3                     | 264 ms                                                 | 410 ms: 1.56x slower                                                  |
| sympy_integrate          | 20.5 ms                                                | 32.2 ms: 1.57x slower                                                 |
| pprint_safe_repr         | 743 ms                                                 | 1.17 sec: 1.57x slower                                                |
| python_startup           | 9.93 ms                                                | 15.6 ms: 1.58x slower                                                 |
| genshi_text              | 22.8 ms                                                | 36.2 ms: 1.59x slower                                                 |
| pprint_pformat           | 1.52 sec                                               | 2.42 sec: 1.59x slower                                                |
| thrift                   | 791 us                                                 | 1.27 ms: 1.60x slower                                                 |
| html5lib                 | 63.6 ms                                                | 105 ms: 1.66x slower                                                  |
| pyflate                  | 448 ms                                                 | 758 ms: 1.69x slower                                                  |
| django_template          | 34.7 ms                                                | 59.2 ms: 1.71x slower                                                 |
| unpickle_pure_python     | 221 us                                                 | 389 us: 1.76x slower                                                  |
| logging_format           | 7.35 us                                                | 13.1 us: 1.78x slower                                                 |
| logging_simple           | 6.63 us                                                | 11.8 us: 1.79x slower                                                 |
| sympy_str                | 292 ms                                                 | 527 ms: 1.81x slower                                                  |
| scimark_monte_carlo      | 68.4 ms                                                | 124 ms: 1.81x slower                                                  |
| mako                     | 11.0 ms                                                | 20.2 ms: 1.83x slower                                                 |
| float                    | 80.8 ms                                                | 149 ms: 1.85x slower                                                  |
| pickle_pure_python       | 308 us                                                 | 577 us: 1.87x slower                                                  |
| richards                 | 45.9 ms                                                | 86.7 ms: 1.89x slower                                                 |
| scimark_lu               | 114 ms                                                 | 216 ms: 1.89x slower                                                  |
| chaos                    | 62.8 ms                                                | 119 ms: 1.89x slower                                                  |
| logging_silent           | 109 ns                                                 | 208 ns: 1.91x slower                                                  |
| hexiom                   | 6.17 ms                                                | 11.8 ms: 1.92x slower                                                 |
| sqlglot_transpile        | 1.67 ms                                                | 3.24 ms: 1.94x slower                                                 |
| richards_super           | 51.9 ms                                                | 104 ms: 2.00x slower                                                  |
| sqlglot_parse            | 1.36 ms                                                | 2.82 ms: 2.08x slower                                                 |
| scimark_sor              | 130 ms                                                 | 271 ms: 2.09x slower                                                  |
| go                       | 139 ms                                                 | 292 ms: 2.10x slower                                                  |
| raytrace                 | 299 ms                                                 | 637 ms: 2.13x slower                                                  |
| sympy_expand             | 468 ms                                                 | 1.03 sec: 2.21x slower                                                |
| nbody                    | 89.3 ms                                                | 199 ms: 2.23x slower                                                  |
| sympy_sum                | 166 ms                                                 | 372 ms: 2.24x slower                                                  |
| deltablue                | 3.45 ms                                                | 8.90 ms: 2.58x slower                                                 |
| unpack_sequence          | 52.1 ns                                                | 137 ns: 2.64x slower                                                  |
| bench_thread_pool        | 941 us                                                 | 3.46 ms: 3.67x slower                                                 |
| bench_mp_pool            | 10.8 ms                                                | 72.1 ms: 6.67x slower                                                 |
| Geometric mean           | (ref)                                                  | 1.49x slower                                                          |
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.41x
- 95% likely to have a slowdown of 1.40x
- 99% likely to have a slowdown of 1.35x

# Memory
- memory change: 1.24x