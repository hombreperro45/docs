# Shaders

## Cg shader spec 

The Cg shader spec used in RetroArch and other libretro frontends supports both single-pass
Cg shaders as well as multi-pass shaders. It uses a custom Cg preset format (.cgp).

### Example Cg preset

    shaders = 2
    shader0 = 4xBR-v3.9.cg
    scale_type0 = source
    scale0 = 4.0
    filter_linear0 = false
    shader1 = dummy.cg
    filter_linear1 = true

## GLSL shader spec

GLSL shader support exists to be compatible in case Cg shader cannot be supported, which is the case
for OpenGL ES, and EGL contexts (KMS mode in Linux for one).

Like Cg shaders, GLSL shaders represents a single pass, and requires a preset file
to describe how multiple shaders are combined. The extension is .glsl.

As GLSL shaders are normally placed in two different files (vertex, fragment), 
making it very impractical to select in a menu. This is worked around by using
compiler defines in order to be equivalent to Cg shaders.

### Example GLSL shader

    varying vec2 tex_coord;
    #if defined(VERTEX)
    attribute vec2 TexCoord;
    attribute vec2 VertexCoord;
    uniform mat4 MVPMatrix;
    void main()
    {
        gl_Position = MVPMatrix * vec4(VertexCoord, 0.0, 1.0);
        tex_coord = TexCoord;
    }
    #elif defined(FRAGMENT)
    uniform sampler2D Texture;
    void main()
    {
        gl_FragColor = texture2D(Texture, tex_coord);
    }
    #endif

GLSL shaders must be modern style, and using ruby prefix is discouraged.

### GLSL preset

Like Cg shaders, there is a preset format. Instead of .cgp extension, .glslp extension is used. The format is exactly the same, just replace .cg shaders with .glsl. To convert a .cgp preset, rename to .glslp and replace all references to .cg shaders with .glsl.

## Converting from Cg shaders

GLSL shaders are mostly considered a compatibility format. It is possible to compile Cg shaders into GLSL shaders automatically using our [cg2glsl](https://github.com/libretro/RetroArch/blob/master/tools/cg2glsl.py) script found here. It can convert single shaders as well as batch conversion.

It relies on nVidia's cgc tool found in nvidia-cg-toolkit package.

## Common Shaders Repository

The Libretro organization hosts a [repository](https://github.com/libretro/common-shaders) on Github that contains a compilation of shaders. Users can contribute their own shaders to this repository by doing a Pull Request.
