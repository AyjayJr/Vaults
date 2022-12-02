## Part 1 DUE 11-7-2022
For this assignment, you will need to render a cube at the center of the world.

The cube vertices are as follow:

vertices =      \[ 1,  1,  1,      -1,  1,  1,     -1, -1,  1,             // v0-v1-v2 (front)
                       -1,-1, 1,        1,-1, 1,        1, 1, 1,               // v2-v3-v0

                        1, 1, 1,   1,-1, 1,   1,-1,-1,      // v0-v3-v4 (right)  
                        1,-1,-1,   1, 1,-1,   1, 1, 1,      // v4-v5-v0

                        1, 1, 1,   1, 1,-1,  -1, 1,-1,      // v0-v5-v6 (top)  
                       -1, 1,-1,  -1, 1, 1,   1, 1, 1,      // v6-v1-v0

                       -1, 1, 1,  -1, 1,-1,  -1,-1,-1,      // v1-v6-v7 (left)  
                       -1,-1,-1,  -1,-1, 1,  -1, 1, 1,      // v7-v2-v1

                       -1,-1,-1,   1,-1,-1,   1,-1, 1,      // v7-v4-v3 (bottom)  
                        1,-1, 1,  -1,-1, 1,  -1,-1,-1,      // v3-v2-v7

                        1,-1,-1,  -1,-1,-1,  -1, 1,-1,      // v4-v7-v6 (back)  
                       -1, 1,-1,   1, 1,-1,   1,-1,-1 ]

There are no normals or uvs.

Create a modelMatrix, a viewMatrix and a projectionMatrix.

set modelMatrix to be the identity matrix

set viewMatrix to look at the center of the cube (0,0,0) from a distance 3 away along the z axis.

set projectionMatrix to be a perspective matrix.

Pass them as uniforms to your shaders and transform the input vertices correctly.

Finally, assign an outColor by using gl_FragCoord.

vec4( gl_FragCoord.xy * vec2(1.f/canvasWidth,1.f/canvasHeight), 0,1);

canvasHeight and canvasWidth must be sent as uniforms to the shader.

you should obtain something like this:
![[Pasted image 20221105205946.png]]
