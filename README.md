1. To update pip deps
bazel run //:pip_requirements.update

2. To run ray tests (using mnist as example https://docs.ray.io/en/latest/train/examples/pytorch/torch_fashion_mnist_example.htmlg)
bazel test //:main --cache_test_results=no --test_output=all

```
Number of trials: 1/1 (1 TERMINATED)
+--------------------------+------------+--------------------+--------+------------------+---------+--------------+---------------------+
| Trial name               | status     | loc                |   iter |   total time (s) |    loss |   _timestamp |   _time_this_iter_s |
|--------------------------+------------+--------------------+--------+------------------+---------+--------------+---------------------|
| TorchTrainer_41141_00000 | TERMINATED | 172.30.123.56:2447 |      4 |          38.8896 | 1.76848 |   1682558710 |             8.31216 |
+--------------------------+------------+--------------------+--------+------------------+---------+--------------+---------------------+


Last result: {'loss': 1.7684828468189118, '_timestamp': 1682558710, '_time_this_iter_s': 8.312156438827515, '_training_iteration': 4, 'time_this_iter_s': 8.315929651260376, 'done': True, 'timesteps_total': None, 'episodes_total': None, 'training_iteration': 4, 'trial_id': '41141_00000', 'experiment_id': 'e1d527b7509b49b588bb23552d5350da', 'date': '2023-04-27_01-25-10', 'timestamp': 1682558710, 'time_total_s': 38.88955903053284, 'pid': 2447, 'hostname': 'wb-tor-GQNY2W2', 'node_ip': '172.30.123.56', 'config': {'train_loop_config': {'lr': 0.001, 'batch_size': 64, 'epochs': 4}}, 'time_since_restore': 38.88955903053284, 'timesteps_since_restore': 0, 'iterations_since_restore': 4, 'warmup_time': 0.1694958209991455, 'experiment_tag': '0'}
================================================================================
```