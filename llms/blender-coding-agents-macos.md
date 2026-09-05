# Using Blender with coding agents on macOS

Modern frontier models have got *really good* at using Blender. I've been having a lot of fun trying this out recently - models can produce `.blend` files you can edit in Blender itself, and can also render images and even movies (by rendering a sequence of images and combining them with `ffmpeg`).

Setting this up, at least on macOS, is *really easy*. Install the Blender desktop app from [blender.org](https://www.blender.org) and then tell the coding agent:

> `Use the already install /Applications/Blender to render a scene of a pelican riding a bicycle`

That worked for me with GPT-6 Astra. You can also be a bit more explicit, to save the model some time figuring out how to use it:

> `Use Blender like this: /Applications/Blender.app/Contents/MacOS/Blender --background --python scene.py`

## A pelican riding a bicycle with GPT-6 Astra

I used GPT-6 Astra (Medium) in the ChatGPT macOS application, Codex mode:

> `Use the already install /Applications/Blender to render a scene of a pelican riding a bicycle`

2m39s later:

![A whimsical 3D illustration of a white pelican riding a turquoise bicycle with cream mudguards and silver spokes. Its wings stretch forward to grip the handlebars, and its long yellow legs bend down to the pedals. A coral scarf streams behind its neck. The pelican has a large glossy eye and a long pale yellow bill with a rounded throat pouch. Soft lighting and a muted sage-green background give the scene a pastel, toy-like appearance.](https://raw.githubusercontent.com/simonw/gpt-6-astra-blender-pelican-bicycle/refs/heads/main/outputs/pelican-bicycle.png)

[pelican-bicycle.blend](https://github.com/simonw/gpt-6-astra-blender-pelican-bicycle/blob/main/outputs/pelican-bicycle.blend), [pelican_scene.py](https://github.com/simonw/gpt-6-astra-blender-pelican-bicycle/blob/main/work/pelican_scene.py)

> `OK add a background and a lot of flair`

3m51s later:

![A whimsical pastel 3D illustration of a white pelican riding a turquoise bicycle along a pink boardwalk. It wears a cream boater hat with a pink band and a coral scarf fluttering behind it, with wings reaching for the handlebars and long yellow legs on the pedals. Three balloons trail behind, and a colorful pinwheel is mounted near the front wheel. Striped beach huts, pink-and-white parasols, and angular palm trees line the beach beneath a teal sky. Pastel triangular bunting hangs overhead, while confetti and curling streamers fill the festive scene.](https://raw.githubusercontent.com/simonw/gpt-6-astra-blender-pelican-bicycle/refs/heads/main/outputs/pelican-bicycle-festival.png)

[pelican-bicycle-festival.blend](https://github.com/simonw/gpt-6-astra-blender-pelican-bicycle/blob/main/outputs/pelican-bicycle-festival.blend), [pelican_flair.py](https://github.com/simonw/gpt-6-astra-blender-pelican-bicycle/blob/main/work/pelican_flair.py)

> `OK make it a whole lot better`

5m59s later:

![A whimsical 3D illustration of a white pelican cycling along a seaside boardwalk at sunset. It wears a cream boater hat and a coral scarf, with wings on the handlebars and long orange legs reaching the pedals of a turquoise bicycle. A wicker front basket holds pink and white flowers, and three balloons float behind. Pastel bunting stretches overhead between palm trees. Striped beach huts stand beside a teal sea with a small sailboat, beneath a large peach-colored sun. The scene has a softly lit, toy-like style.](https://raw.githubusercontent.com/simonw/gpt-6-astra-blender-pelican-bicycle/refs/heads/main/outputs/pelican-coastal-parade.png)

[pelican-coastal-parade.blend](https://github.com/simonw/gpt-6-astra-blender-pelican-bicycle/blob/main/outputs/pelican-coastal-parade.blend), [pelican_final.py](https://github.com/simonw/gpt-6-astra-blender-pelican-bicycle/blob/main/work/pelican_final.py)

The project lives [in this repo](https://github.com/simonw/gpt-6-astra-blender-pelican-bicycle), and [here's the exported transcript from Codex](https://github.com/simonw/gpt-6-astra-blender-pelican-bicycle/blob/main/codex-transcript.md).

## Creating a skill

Codex makes it pretty easy to create skills (using its built-in skill creating skill), so I finished up by prompting:

> `Create a quick skill that describes how to use the currently installed /Application/Blender based on what you learned`

It produced and installed [this Markdown skill](https://github.com/simonw/gpt-6-astra-blender-pelican-bicycle/blob/main/outputs/blender-local/SKILL.md), which I have since used for further Blender experiments with prompts like this:

> `Use your Blender Local skill to build this scene (attached image)`
