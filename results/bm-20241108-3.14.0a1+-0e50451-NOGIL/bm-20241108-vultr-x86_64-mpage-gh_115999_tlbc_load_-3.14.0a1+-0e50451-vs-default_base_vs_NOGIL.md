# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_tlbc_load_
- machine: linux-x86_64
- commit hash: 0e50451
- commit date: 2024-11-08
- overall geometric mean: 1.48x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.35x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                 | 410 ms: 1.61x slower                                                  |
| docutils       | 2.61 sec                                                               | 3.31 sec: 1.27x slower                                                |
| html5lib       | 65.2 ms                                                                | 105 ms: 1.62x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.49x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_tcp      | 507 ms                                                                 | 581 ms: 1.15x slower                                                  |
| asyncio_tcp_ssl  | 1.52 sec                                                               | 1.83 sec: 1.20x slower                                                |
| coroutines       | 23.2 ms                                                                | 28.9 ms: 1.24x slower                                                 |
| async_generators | 368 ms                                                                 | 480 ms: 1.30x slower                                                  |
| Geometric mean   | (ref)                                                                  | 1.17x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 223 ms                                                                 | 182 ms: 1.22x faster                                                  |
| float          | 79.8 ms                                                                | 149 ms: 1.87x slower                                                  |
| nbody          | 94.5 ms                                                                | 199 ms: 2.11x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.48x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 186 ms                                                                 | 186 ms: 1.00x slower                                                  |
| regex_v8       | 24.6 ms                                                                | 25.1 ms: 1.02x slower                                                 |
| regex_compile  | 131 ms                                                                 | 212 ms: 1.62x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle               | 12.6 us                                                                | 12.0 us: 1.05x faster                                                 |
| pickle_list          | 5.26 us                                                                | 5.13 us: 1.03x faster                                                 |
| xml_etree_parse      | 136 ms                                                                 | 134 ms: 1.02x faster                                                  |
| pickle_dict          | 31.8 us                                                                | 31.6 us: 1.01x faster                                                 |
| unpickle_list        | 4.82 us                                                                | 5.01 us: 1.04x slower                                                 |
| unpickle             | 13.7 us                                                                | 14.6 us: 1.06x slower                                                 |
| xml_etree_iterparse  | 95.9 ms                                                                | 106 ms: 1.10x slower                                                  |
| json_loads           | 26.0 us                                                                | 29.4 us: 1.13x slower                                                 |
| json_dumps           | 11.6 ms                                                                | 14.7 ms: 1.27x slower                                                 |
| xml_etree_generate   | 84.5 ms                                                                | 109 ms: 1.29x slower                                                  |
| tomli_loads          | 2.09 sec                                                               | 3.12 sec: 1.49x slower                                                |
| xml_etree_process    | 59.1 ms                                                                | 89.3 ms: 1.51x slower                                                 |
| unpickle_pure_python | 215 us                                                                 | 389 us: 1.81x slower                                                  |
| pickle_pure_python   | 316 us                                                                 | 577 us: 1.82x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.21x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.47 ms                                                                | 10.2 ms: 1.37x slower                                                 |
| python_startup         | 11.1 ms                                                                | 15.6 ms: 1.41x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.39x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.1 ms                                                                | 74.3 ms: 1.48x slower                                                 |
| genshi_text     | 22.5 ms                                                                | 36.2 ms: 1.60x slower                                                 |
| django_template | 35.0 ms                                                                | 59.2 ms: 1.69x slower                                                 |
| mako            | 11.8 ms                                                                | 20.2 ms: 1.70x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.62x slower                                                          |

All benchmarks:
===============

| Benchmark                | bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1+-54c63a3 | bm-20241108-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a1+-0e50451 |
|--------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal             | 3.37 ms                                                                | 2.46 ms: 1.37x faster                                                 |
| create_gc_cycles         | 1.37 ms                                                                | 1.11 ms: 1.24x faster                                                 |
| pidigits                 | 223 ms                                                                 | 182 ms: 1.22x faster                                                  |
| pickle                   | 12.6 us                                                                | 12.0 us: 1.05x faster                                                 |
| pickle_list              | 5.26 us                                                                | 5.13 us: 1.03x faster                                                 |
| xml_etree_parse          | 136 ms                                                                 | 134 ms: 1.02x faster                                                  |
| pickle_dict              | 31.8 us                                                                | 31.6 us: 1.01x faster                                                 |
| regex_dna                | 186 ms                                                                 | 186 ms: 1.00x slower                                                  |
| regex_v8                 | 24.6 ms                                                                | 25.1 ms: 1.02x slower                                                 |
| unpickle_list            | 4.82 us                                                                | 5.01 us: 1.04x slower                                                 |
| unpickle                 | 13.7 us                                                                | 14.6 us: 1.06x slower                                                 |
| sqlite_synth             | 2.21 us                                                                | 2.43 us: 1.10x slower                                                 |
| json                     | 4.86 ms                                                                | 5.35 ms: 1.10x slower                                                 |
| xml_etree_iterparse      | 95.9 ms                                                                | 106 ms: 1.10x slower                                                  |
| bench_mp_pool            | 63.9 ms                                                                | 72.1 ms: 1.13x slower                                                 |
| json_loads               | 26.0 us                                                                | 29.4 us: 1.13x slower                                                 |
| asyncio_tcp              | 507 ms                                                                 | 581 ms: 1.15x slower                                                  |
| pathlib                  | 18.3 ms                                                                | 21.4 ms: 1.17x slower                                                 |
| asyncio_tcp_ssl          | 1.52 sec                                                               | 1.83 sec: 1.20x slower                                                |
| scimark_fft              | 335 ms                                                                 | 410 ms: 1.22x slower                                                  |
| coroutines               | 23.2 ms                                                                | 28.9 ms: 1.24x slower                                                 |
| coverage                 | 80.6 ms                                                                | 101 ms: 1.25x slower                                                  |
| json_dumps               | 11.6 ms                                                                | 14.7 ms: 1.27x slower                                                 |
| telco                    | 7.25 ms                                                                | 9.19 ms: 1.27x slower                                                 |
| docutils                 | 2.61 sec                                                               | 3.31 sec: 1.27x slower                                                |
| pylint                   | 319 ms                                                                 | 409 ms: 1.28x slower                                                  |
| xml_etree_generate       | 84.5 ms                                                                | 109 ms: 1.29x slower                                                  |
| async_generators         | 368 ms                                                                 | 480 ms: 1.30x slower                                                  |
| scimark_sparse_mat_mult  | 4.53 ms                                                                | 5.97 ms: 1.32x slower                                                 |
| meteor_contest           | 103 ms                                                                 | 136 ms: 1.32x slower                                                  |
| bpe_tokeniser            | 4.35 sec                                                               | 5.79 sec: 1.33x slower                                                |
| mdp                      | 2.36 sec                                                               | 3.19 sec: 1.35x slower                                                |
| dulwich_log              | 75.7 ms                                                                | 103 ms: 1.35x slower                                                  |
| python_startup_no_site   | 7.47 ms                                                                | 10.2 ms: 1.37x slower                                                 |
| python_startup           | 11.1 ms                                                                | 15.6 ms: 1.41x slower                                                 |
| generators               | 29.1 ms                                                                | 41.3 ms: 1.42x slower                                                 |
| typing_runtime_protocols | 158 us                                                                 | 226 us: 1.43x slower                                                  |
| nqueens                  | 78.1 ms                                                                | 112 ms: 1.44x slower                                                  |
| spectral_norm            | 108 ms                                                                 | 156 ms: 1.44x slower                                                  |
| deepcopy                 | 263 us                                                                 | 387 us: 1.47x slower                                                  |
| pycparser                | 1.14 sec                                                               | 1.68 sec: 1.47x slower                                                |
| genshi_xml               | 50.1 ms                                                                | 74.3 ms: 1.48x slower                                                 |
| deepcopy_reduce          | 2.76 us                                                                | 4.10 us: 1.49x slower                                                 |
| tomli_loads              | 2.09 sec                                                               | 3.12 sec: 1.49x slower                                                |
| xml_etree_process        | 59.1 ms                                                                | 89.3 ms: 1.51x slower                                                 |
| fannkuch                 | 371 ms                                                                 | 562 ms: 1.51x slower                                                  |
| sqlglot_optimize         | 53.7 ms                                                                | 82.1 ms: 1.53x slower                                                 |
| sqlglot_normalize        | 106 ms                                                                 | 164 ms: 1.55x slower                                                  |
| deepcopy_memo            | 30.1 us                                                                | 46.7 us: 1.55x slower                                                 |
| genshi_text              | 22.5 ms                                                                | 36.2 ms: 1.60x slower                                                 |
| crypto_pyaes             | 66.8 ms                                                                | 108 ms: 1.61x slower                                                  |
| 2to3                     | 254 ms                                                                 | 410 ms: 1.61x slower                                                  |
| sympy_integrate          | 19.9 ms                                                                | 32.2 ms: 1.62x slower                                                 |
| regex_compile            | 131 ms                                                                 | 212 ms: 1.62x slower                                                  |
| html5lib                 | 65.2 ms                                                                | 105 ms: 1.62x slower                                                  |
| pprint_safe_repr         | 702 ms                                                                 | 1.17 sec: 1.66x slower                                                |
| pprint_pformat           | 1.45 sec                                                               | 2.42 sec: 1.67x slower                                                |
| thrift                   | 754 us                                                                 | 1.27 ms: 1.68x slower                                                 |
| pyflate                  | 450 ms                                                                 | 758 ms: 1.69x slower                                                  |
| django_template          | 35.0 ms                                                                | 59.2 ms: 1.69x slower                                                 |
| mako                     | 11.8 ms                                                                | 20.2 ms: 1.70x slower                                                 |
| comprehensions           | 17.1 us                                                                | 29.8 us: 1.74x slower                                                 |
| unpickle_pure_python     | 215 us                                                                 | 389 us: 1.81x slower                                                  |
| pickle_pure_python       | 316 us                                                                 | 577 us: 1.82x slower                                                  |
| float                    | 79.8 ms                                                                | 149 ms: 1.87x slower                                                  |
| scimark_monte_carlo      | 65.6 ms                                                                | 124 ms: 1.89x slower                                                  |
| richards                 | 45.5 ms                                                                | 86.7 ms: 1.90x slower                                                 |
| sympy_str                | 276 ms                                                                 | 527 ms: 1.91x slower                                                  |
| logging_format           | 6.77 us                                                                | 13.1 us: 1.93x slower                                                 |
| scimark_lu               | 111 ms                                                                 | 216 ms: 1.95x slower                                                  |
| logging_simple           | 6.05 us                                                                | 11.8 us: 1.96x slower                                                 |
| logging_silent           | 106 ns                                                                 | 208 ns: 1.96x slower                                                  |
| hexiom                   | 5.98 ms                                                                | 11.8 ms: 1.98x slower                                                 |
| richards_super           | 51.3 ms                                                                | 104 ms: 2.02x slower                                                  |
| sqlglot_transpile        | 1.60 ms                                                                | 3.24 ms: 2.02x slower                                                 |
| scimark_sor              | 133 ms                                                                 | 271 ms: 2.03x slower                                                  |
| chaos                    | 58.4 ms                                                                | 119 ms: 2.04x slower                                                  |
| nbody                    | 94.5 ms                                                                | 199 ms: 2.11x slower                                                  |
| sqlglot_parse            | 1.30 ms                                                                | 2.82 ms: 2.16x slower                                                 |
| sympy_expand             | 465 ms                                                                 | 1.03 sec: 2.22x slower                                                |
| go                       | 121 ms                                                                 | 292 ms: 2.42x slower                                                  |
| sympy_sum                | 153 ms                                                                 | 372 ms: 2.44x slower                                                  |
| raytrace                 | 260 ms                                                                 | 637 ms: 2.45x slower                                                  |
| unpack_sequence          | 49.8 ns                                                                | 137 ns: 2.76x slower                                                  |
| deltablue                | 3.21 ms                                                                | 8.90 ms: 2.77x slower                                                 |
| bench_thread_pool        | 1.01 ms                                                                | 3.46 ms: 3.41x slower                                                 |
| Geometric mean           | (ref)                                                                  | 1.48x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, regex_effbot

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.43x
- 95% likely to have a slowdown of 1.41x
- 99% likely to have a slowdown of 1.35x

# Memory
- memory change: 1.21x