# **React Shaders** [![lusat minzip package size](https://img.shields.io/bundlephobia/minzip/react-shaders?label=zipped)](https://www.npmjs.com/package/react-shaders) [![lusat package version](https://img.shields.io/npm/v/react-shaders.svg?colorB=green)](https://www.npmjs.com/package/react-shaders) [![lusat license](https://img.shields.io/npm/l/react-shaders.svg?colorB=lightgrey)](https://github.com/rysanacom/react-shaders/blob/main/LICENSE)

**React Shaders** is an open source library for creating GLSL/WebGL shaders with support for modern shader bindings like those in Shadertoy. `react-shaders` is built on top of [Morgan Villedieu's `shadertoy-react`](https://github.com/mvilledieu/shadertoy-react).

<table>
<tr>
<th width="440px"><code>index.tsx</code> (React)</th>
<th width="440px"><code>example.glsl</code> (GLSL)</th>
</tr>
<tr>
<td>

```jsx
import { Shader } from 'react-shaders'
import code from './example.glsl'

return (
  <Shader fs={code} />
)
```

</td>
<td>

```glsl
void mainImage(out vec4 O,in vec2 I){
  I=.5-(I/iResolution.xy);
  vec3 col=.5+vec3(I,.5*sin(iTime));
  I*=vec2(1.,iResolution.y/iResolution.x);
  float z=.5*sin((dot(I,I)+iTime*5e-2)/.01);
  O=vec4(col*(1.+z),1.);}
```

</td>
</tr>
</table>

### Installation

<table>
<tr>
<td>

```bash
npm i react-shaders
```

</td>
<td>

```bash
pnpm i react-shaders
```

</td>
<td>

```bash
bun add react-shaders
```

</td>
</tr>
</table>
