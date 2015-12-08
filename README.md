# Sardroid Dockerfiles
Dockerfiles related to running the SAR server inside Docker, maybe even the [LayersBox](https://github.com/learning-layers/LayersBox)!

See server itself [here!](https://github.com/melonmanchan/sardroid-server)

## How do I configure the app itself to use LayersBox?

Go right [here](https://github.com/melonmanchan/sardroid/blob/master/app/js/app.js#L44), and configure the PeerJS options to match your layersbox. Currently, something akin to the following should work:

```javascript
                peerjs: {
                    host: '188.166.88.67',
                    port: 443,
                    path: 'sardroid/peerjs',
                    debug: 3,
                    secure: true,
                    config: {'iceServers': [
                        { 'url': 'stun:stun.l.google.com:19302' },
                        { 'url': 'stun:stun1.l.google.com:19302' },
                        { 'url': 'stun:stun2.l.google.com:19302' },
                        { 'url': 'stun:stun3.l.google.com:19302' }
                    ]}},
```

Licence
-------

```
Copyright 2015 Aalto University

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
