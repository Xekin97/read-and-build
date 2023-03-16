# read-and-build
 数据读取工具

# Design
![image](https://user-images.githubusercontent.com/25792845/225559252-09279cf6-0194-4d1d-ae37-bacb33004432.png)

# Type

- Schema<Data>
- Reader<Schema>
- Builder<Output>

# Usage
```typescript
import ReadAndBuild from 'read-and-build'

interface Data {}

interface Output {}

class MySchema extends Schema<Data> {}

class MyReader extends Reader<MySchema> {}

class MyBuilder extends Builder<Output> {}

const Generator = new ReadAndBuild({
  readers: [ MyReader ],
  Schema: MySchema,
  builders: [ MyBuilder ]
})

Generator.produce(data)

```
