# Livestate usage on the client

```jsx
import { useLiveState, LiveStateProvider } from "livestate";

const App = () => (
  <LiveStateProvider uri="wss://try.livestate.io/socket">
    <CounterExample />
  </LiveStateProvider>
);

const counterId = "the-universal-global-counter-id";
const CounterExample = () => {
  const [state, setState] = useLiveState({
    id: counterId,
    defaultValue: { counter: 0 },
  });

  return (
    <div>
      <button onClick={() => setState({ counter: state.counter + 1 })}>
        Increment
      </button>
      <p>Counter: {state.counter}</p>
    </div>
  );
};
```

# Server (Self hosting)

Coming soon
