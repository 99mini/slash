# usePrevious

한 단계 이전에 인자로 주어졌던 값을 반환합니다. 이전 값이 없을 경우 인자로 주어진 값을 그대로 반환합니다.

```ts
// value: 저장할 값
function usePrevious<T>(value): T;
```

## Example

```ts
const { data: stores } = useStores();
const previousStores = usePrevious(stores);
const isStoreChanged = stores !== previousStores;

useEffect(() => {
  if (isStoreChanged) {
    onStoreChange();
  }
}, [isStoreChanged, onStoreChange]);
```
