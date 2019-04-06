### simpy
---
https://bitbucket.org/simpy/simpy

```py 
import simpy

def clock(env, name, tick):
  while True:
    print(name, nv.now)
    yield env.timeout(tick)
    
env = simpy.Environment()
env.process(clock(env, 'fest', 0.5))
env.process(clock(env, 'slow', 1))
env.run(until=2)


```

```sh
pip install -U simpy
cd where/you/put/simpy/
python setup.py install
py.test --pyargs simpy
```

```
```


