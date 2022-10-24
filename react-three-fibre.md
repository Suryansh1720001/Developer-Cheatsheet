
# React-Three-Fiber

react-three-fiber is a React renderer over threejs. Helps to build a scene declaratively with re-usable, self-contained components that react to state, are readily interactive and will work in React's ecosystem.




## Installation

Open your project folder and run the follow ing command.

```bash
  npm install three @react-three/fiber
```
    
 ## Contents

- [Ecosystem](#ecosystem)
- [Canvas](#canvas)
- [Render Props](#render-props)
- [Events](#events)
- [Documentation](#documentation) 


## Ecosystem

- `@react-three/gltfjsx` – GLTFs into JSX components
- `@react-three/drei` – useful helpers of react-three-fiber
- `@react-three/postprocessing` – for post-processing effects
- `@react-three/flex` – used as flexbox for react-three-fiber
- `@react-three/xr` – VR/AR controllers and events for react-three-fiber
- `@react-three/cannon` – physics based hooks for react-three-fiber
- `@react-three/a11y` – accessibility tools of react-three-fiber
- `zustand` – state management for react-three-fiber
- `react-spring` – a spring-physics-based animation library of react-three-fiber
- `react-use-gesture` – mouse/touch gestures in the scene


## Canvas

The `Canvas` object is where you define your React Three Fiber Scene to render.

### A basic react-three-fibre scene
```javascript
import React from 'react'
import { Canvas } from '@react-three/fiber'

const App = () => (
  <Canvas>
    <pointLight position={[5, 5, 5]} />
    <mesh>
      <boxGeometry />
      <meshStandardMaterial color="red" />
    </mesh>
  </Canvas>
)
```


## Render Props


| PROP | DESCRIPTION     | DEFAULT                |
| :-------- | :------- | :------------------------- |
| **children** | three.js JSX elements or regular components | |
| **gl** | Props that go to the default renderer, or your own renderer. Also accepts synchronous callback e.g. `gl={canvas => new Renderer({ canvas })}` | `{}`
| **camera** | Props that go to the default camera, or your own `THREE.Camera` | `{ fov: 75, near: 0.1, far: 1000, position: [0, 0, 5] }`
| **shadows** | Props that go to `gl.shadowMap`, can also be set true for `PCFsoft` | `false`
| **raycaster** | Props that go to the default raycaster | `{}`
| **frameloop** | Available Render mode: always, demand, never | `always`
| **resize** | For: Resize config, use react-use-measure's options | `{ scroll: true, debounce: { scroll: 50, resize: 0 } }`
| **orthographic** | Creates an orthographic camera in the Scene | `false`
| **dpr** | Pixel-ratio for resolution, use` window.devicePixelRatio`, or automatic: [min, max] | `[4, 3]`
| **legacy** | Enables THREE.ColorManagement.legacyMode in three r139 | `false`
| **linear** | Switch off for automatic sRGB encoding and gamma correction | `false`
| **events** | Configuration for event manager, a function of state | `import { events } from "@react-three/fiber"`
| **eventSource** | It is the source where events are being subscribed to, HTMLElement | `React.MutableRefObject<HTMLElement>, gl.domElement.parentNode`
| **eventPrefix** | The event prefix that is cast into canvas pointer x/y events | `offset`
| **flat** | Use `THREE.NoToneMapping` instead of `THREE.ACESFilmicToneMapping` | `false`
| **onCreated** | Callback after the canvas has rendered (but not yet committed) | `(state) => {}`



## Events
`three.js` objects that use their own `raycast` method (meshes, lines, etc) can be interacted with by declaring events on them. It support pointer events, clicks and wheel-scroll. Events contain the browser event as well as the `three.js` event data (object, point, distance, etc).

Also, there's a special `onUpdate` that is called every time the object gets fresh props, it is good for things like `self => (self.verticesNeedUpdate = true)`.


```bash
  <mesh
  onClick={(e) => console.log('click')}
  onContextMenu={(e) => console.log('context menu')}
  onDoubleClick={(e) => console.log('double click')}
  onWheel={(e) => console.log('wheel spins')}
  onPointerUp={(e) => console.log('up')}
  onPointerDown={(e) => console.log('down')}
  onPointerOver={(e) => console.log('over')}
  onPointerOut={(e) => console.log('out')}
  onPointerMove={(e) => console.log('move')}
  onUpdate={(self) => console.log('props have been updated')}
/>
```


## Documentation

- [React-Three-Fibre (Canvas)](https://docs.pmnd.rs/react-three-fiber/api/canvas)
- [React-Three-Fibre (Events)](https://docs.pmnd.rs/react-three-fiber/api/events)
