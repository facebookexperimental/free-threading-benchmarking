# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 6a24958
- commit date: 2024-11-18
- overall geometric mean: 1.04x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 420 ms                                                                 | 406 ms: 1.03x faster                                                 |
| docutils       | 3.40 sec                                                               | 3.29 sec: 1.03x faster                                               |
| html5lib       | 105 ms                                                                 | 104 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| coroutines       | 31.2 ms                                                                | 29.4 ms: 1.06x faster                                                |
| async_generators | 490 ms                                                                 | 482 ms: 1.02x faster                                                 |
| Geometric mean   | (ref)                                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (3): asyncio_tcp, asyncio_websockets, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 206 ms                                                                 | 198 ms: 1.04x faster                                                 |
| float          | 152 ms                                                                 | 147 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 230 ms                                                                 | 212 ms: 1.08x faster                                                 |
| regex_dna      | 184 ms                                                                 | 185 ms: 1.01x slower                                                 |
| regex_v8       | 24.7 ms                                                                | 25.0 ms: 1.01x slower                                                |
| regex_effbot   | 2.96 ms                                                                | 3.11 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| unpickle_pure_python | 429 us                                                                 | 384 us: 1.12x faster                                                 |
| pickle_pure_python   | 630 us                                                                 | 577 us: 1.09x faster                                                 |
| xml_etree_process    | 94.1 ms                                                                | 88.5 ms: 1.06x faster                                                |
| xml_etree_generate   | 115 ms                                                                 | 108 ms: 1.06x faster                                                 |
| tomli_loads          | 3.25 sec                                                               | 3.10 sec: 1.05x faster                                               |
| xml_etree_iterparse  | 110 ms                                                                 | 106 ms: 1.04x faster                                                 |
| pickle_dict          | 32.4 us                                                                | 31.8 us: 1.02x faster                                                |
| json_dumps           | 15.3 ms                                                                | 15.0 ms: 1.01x faster                                                |
| json_loads           | 28.7 us                                                                | 28.5 us: 1.01x faster                                                |
| unpickle_list        | 4.88 us                                                                | 4.95 us: 1.01x slower                                                |
| pickle               | 12.4 us                                                                | 14.1 us: 1.13x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                |
| python_startup         | 15.8 ms                                                                | 15.7 ms: 1.00x faster                                                |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 21.1 ms                                                                | 18.8 ms: 1.12x faster                                                |
| django_template | 66.5 ms                                                                | 61.3 ms: 1.09x faster                                                |
| genshi_xml      | 84.0 ms                                                                | 79.6 ms: 1.06x faster                                                |
| genshi_text     | 41.1 ms                                                                | 39.0 ms: 1.05x faster                                                |
| Geometric mean  | (ref)                                                                  | 1.08x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| deepcopy_memo            | 54.1 us                                                                | 47.9 us: 1.13x faster                                                |
| mako                     | 21.1 ms                                                                | 18.8 ms: 1.12x faster                                                |
| unpickle_pure_python     | 429 us                                                                 | 384 us: 1.12x faster                                                 |
| raytrace                 | 632 ms                                                                 | 574 ms: 1.10x faster                                                 |
| hexiom                   | 12.6 ms                                                                | 11.5 ms: 1.10x faster                                                |
| chaos                    | 124 ms                                                                 | 113 ms: 1.10x faster                                                 |
| richards                 | 93.3 ms                                                                | 85.0 ms: 1.10x faster                                                |
| pprint_pformat           | 2.77 sec                                                               | 2.53 sec: 1.10x faster                                               |
| pickle_pure_python       | 630 us                                                                 | 577 us: 1.09x faster                                                 |
| pprint_safe_repr         | 1.34 sec                                                               | 1.22 sec: 1.09x faster                                               |
| bpe_tokeniser            | 6.15 sec                                                               | 5.66 sec: 1.09x faster                                               |
| django_template          | 66.5 ms                                                                | 61.3 ms: 1.09x faster                                                |
| sqlglot_normalize        | 184 ms                                                                 | 170 ms: 1.08x faster                                                 |
| deepcopy_reduce          | 4.58 us                                                                | 4.23 us: 1.08x faster                                                |
| logging_silent           | 219 ns                                                                 | 202 ns: 1.08x faster                                                 |
| regex_compile            | 230 ms                                                                 | 212 ms: 1.08x faster                                                 |
| deepcopy                 | 437 us                                                                 | 404 us: 1.08x faster                                                 |
| pyflate                  | 793 ms                                                                 | 734 ms: 1.08x faster                                                 |
| sqlglot_optimize         | 91.5 ms                                                                | 85.1 ms: 1.07x faster                                                |
| pycparser                | 1.75 sec                                                               | 1.65 sec: 1.06x faster                                               |
| xml_etree_process        | 94.1 ms                                                                | 88.5 ms: 1.06x faster                                                |
| deltablue                | 9.22 ms                                                                | 8.67 ms: 1.06x faster                                                |
| comprehensions           | 30.9 us                                                                | 29.0 us: 1.06x faster                                                |
| xml_etree_generate       | 115 ms                                                                 | 108 ms: 1.06x faster                                                 |
| spectral_norm            | 163 ms                                                                 | 154 ms: 1.06x faster                                                 |
| unpack_sequence          | 156 ns                                                                 | 147 ns: 1.06x faster                                                 |
| coroutines               | 31.2 ms                                                                | 29.4 ms: 1.06x faster                                                |
| go                       | 300 ms                                                                 | 284 ms: 1.06x faster                                                 |
| genshi_xml               | 84.0 ms                                                                | 79.6 ms: 1.06x faster                                                |
| nqueens                  | 116 ms                                                                 | 111 ms: 1.05x faster                                                 |
| genshi_text              | 41.1 ms                                                                | 39.0 ms: 1.05x faster                                                |
| logging_simple           | 12.4 us                                                                | 11.8 us: 1.05x faster                                                |
| tomli_loads              | 3.25 sec                                                               | 3.10 sec: 1.05x faster                                               |
| scimark_lu               | 247 ms                                                                 | 236 ms: 1.05x faster                                                 |
| scimark_monte_carlo      | 128 ms                                                                 | 123 ms: 1.05x faster                                                 |
| sympy_integrate          | 33.3 ms                                                                | 31.9 ms: 1.04x faster                                                |
| fannkuch                 | 568 ms                                                                 | 545 ms: 1.04x faster                                                 |
| scimark_fft              | 420 ms                                                                 | 404 ms: 1.04x faster                                                 |
| richards_super           | 110 ms                                                                 | 106 ms: 1.04x faster                                                 |
| nbody                    | 206 ms                                                                 | 198 ms: 1.04x faster                                                 |
| sqlglot_transpile        | 3.32 ms                                                                | 3.20 ms: 1.04x faster                                                |
| sympy_str                | 546 ms                                                                 | 527 ms: 1.04x faster                                                 |
| xml_etree_iterparse      | 110 ms                                                                 | 106 ms: 1.04x faster                                                 |
| typing_runtime_protocols | 250 us                                                                 | 242 us: 1.03x faster                                                 |
| float                    | 152 ms                                                                 | 147 ms: 1.03x faster                                                 |
| crypto_pyaes             | 109 ms                                                                 | 105 ms: 1.03x faster                                                 |
| thrift                   | 1.30 ms                                                                | 1.26 ms: 1.03x faster                                                |
| docutils                 | 3.40 sec                                                               | 3.29 sec: 1.03x faster                                               |
| 2to3                     | 420 ms                                                                 | 406 ms: 1.03x faster                                                 |
| sqlglot_parse            | 2.86 ms                                                                | 2.78 ms: 1.03x faster                                                |
| sympy_expand             | 1.07 sec                                                               | 1.03 sec: 1.03x faster                                               |
| logging_format           | 13.5 us                                                                | 13.1 us: 1.03x faster                                                |
| meteor_contest           | 140 ms                                                                 | 136 ms: 1.03x faster                                                 |
| scimark_sor              | 271 ms                                                                 | 263 ms: 1.03x faster                                                 |
| pylint                   | 423 ms                                                                 | 411 ms: 1.03x faster                                                 |
| coverage                 | 103 ms                                                                 | 100 ms: 1.03x faster                                                 |
| mdp                      | 3.14 sec                                                               | 3.06 sec: 1.02x faster                                               |
| pickle_dict              | 32.4 us                                                                | 31.8 us: 1.02x faster                                                |
| sympy_sum                | 384 ms                                                                 | 376 ms: 1.02x faster                                                 |
| json                     | 5.31 ms                                                                | 5.21 ms: 1.02x faster                                                |
| dulwich_log              | 105 ms                                                                 | 103 ms: 1.02x faster                                                 |
| async_generators         | 490 ms                                                                 | 482 ms: 1.02x faster                                                 |
| sqlite_synth             | 2.43 us                                                                | 2.39 us: 1.01x faster                                                |
| html5lib                 | 105 ms                                                                 | 104 ms: 1.01x faster                                                 |
| json_dumps               | 15.3 ms                                                                | 15.0 ms: 1.01x faster                                                |
| bench_mp_pool            | 72.8 ms                                                                | 71.9 ms: 1.01x faster                                                |
| scimark_sparse_mat_mult  | 5.87 ms                                                                | 5.80 ms: 1.01x faster                                                |
| create_gc_cycles         | 1.14 ms                                                                | 1.13 ms: 1.01x faster                                                |
| bench_thread_pool        | 3.50 ms                                                                | 3.47 ms: 1.01x faster                                                |
| json_loads               | 28.7 us                                                                | 28.5 us: 1.01x faster                                                |
| python_startup_no_site   | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                                |
| python_startup           | 15.8 ms                                                                | 15.7 ms: 1.00x faster                                                |
| regex_dna                | 184 ms                                                                 | 185 ms: 1.01x slower                                                 |
| generators               | 41.5 ms                                                                | 41.9 ms: 1.01x slower                                                |
| regex_v8                 | 24.7 ms                                                                | 25.0 ms: 1.01x slower                                                |
| unpickle_list            | 4.88 us                                                                | 4.95 us: 1.01x slower                                                |
| regex_effbot             | 2.96 ms                                                                | 3.11 ms: 1.05x slower                                                |
| gc_traversal             | 2.38 ms                                                                | 2.58 ms: 1.08x slower                                                |
| pickle                   | 12.4 us                                                                | 14.1 us: 1.13x slower                                                |
| Geometric mean           | (ref)                                                                  | 1.04x faster                                                         |

Benchmark hidden because not significant (9): pathlib, asyncio_tcp, xml_etree_parse, telco, asyncio_websockets, pickle_list, pidigits, asyncio_tcp_ssl, unpickle

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.00x