# actions-demo

To use this Charm, simply:

```bash
mkdir trusty
git clone https://github.com/binary132/actions-demo trusty/actions-demo
juju deploy local:trusty/actions-demo
```

This Charm specifies two Actions: `run` and `report`.  `run` executes an
arbitrary script given in a params file such as:

```yaml
# params.yaml
command: "echo \"hello world\""
```

Two samples have been given as `run-sample-fail.yaml` and `run-sample-ok.yaml`.

---

```bash
juju action defined
# ...

juju action do actions-demo/0 <action name> [--params run-sample-ok.yaml]
# ... <UUID>

juju action fetch <UUID>
# ... results
```
