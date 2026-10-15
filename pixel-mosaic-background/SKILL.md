---
name: pixel-mosaic-background
description: Edit any supplied image—people, architecture, products, landscapes, animals, vehicles, food, interiors, artwork, or other subjects—while preserving its subject, composition, regional character, culture, and materials, then express selected surroundings with solid high-saturation 3D voxel blocks that scale from large nearby to small in the distance. Use for vivid source-faithful voxel stylization; do not use for privacy pixelation, flat pixel filters, dull low-saturation rendering, or replacing the source with a generic themed world.
---

# Pixel Mosaic Background

Transform any existing image into a polished, vivid, source-faithful hybrid scene: its focal subject, place identity, and original visual language remain dominant, while selected surroundings become solid three-dimensional voxel forms. Give the blocks clear geometry, tactile volume, convincing depth, and rich color without imposing a new theme. The focal subject may be a person, building, product, landscape feature, animal, vehicle, plant, food item, interior, artwork, or another clearly identifiable element.

## Required input

Use at least one user-supplied image as the edit target. If it is only available as a local file, inspect it with the image-viewing tool before editing. Treat additional images as style references only when the user says so.

Use the built-in image generation/editing tool by default. Classify it as `identity-preserve` when a person or recognizable animal is central, and as `precise-object-edit` for buildings, products, landscapes, vehicles, interiors, food, artwork, and other subjects.

## Visual contract

First identify the focal subject from the image and the user's wording. Preserve these unless the user explicitly asks to change them:

- the subject's defining identity, silhouette, geometry, proportions, materials, surface details, colors, condition, and spatial orientation;
- the original crop, camera angle, perspective, depth relationships, horizon, and focal-subject placement;
- the image's dominant palette, lighting direction, mood, weather, time of day, and photographic or illustrative character;
- the location's regional identity, architectural vernacular, cultural traces, age, patina, signage, everyday objects, and lived-in atmosphere;
- important foreground objects and their spatial relationship to the focal subject.

When the source depicts Chongqing, preserve recognizable mountain-city qualities present in the image: steep and layered circulation, dense vertical space, old-lane or riverside character, gray weathered masonry and plaster, dark green painted details, warm wood or bamboo, red handwritten signage, local teahouse atmosphere, and authentic everyday clutter. Use only the traits actually visible; do not add landmark clichés or replace the location with a fantasy version of Chongqing.

Apply subject-specific protection:

- **People:** preserve facial features, body proportions, pose, gaze, expression, skin tone, hairstyle, outfit, and accessories.
- **Architecture/interiors:** preserve footprint, massing, façade layout, windows, doors, roofline, structural rhythm, materials, signage, and architectural era. Do not invent floors or distort load-bearing geometry.
- **Products/vehicles:** preserve exact shape, proportions, functional parts, packaging, controls, material finish, branding, and readable labels when essential.
- **Landscapes/nature:** preserve terrain contours, skyline, horizon, watercourse, major vegetation, season, weather, and geographic character.
- **Animals/plants/food:** preserve species or type, anatomy or natural structure, markings, texture, color, arrangement, and freshness or condition.
- **Artwork/graphics:** preserve the original motif, layout, palette, line character, and medium unless the user requests a broader restyle.

Apply the effect selectively:

- Convert roughly 25–55% of the visible background into designed pixel blocks or small 3D voxel cubes, adjusting the amount to the scene.
- Prefer secondary architecture, furniture, plants, clouds, terrain, signs, decorative objects, empty surfaces, sky, or distant scenery. Keep the focal subject and critical contact edges clean.
- Treat voxel blocks as a rendering language for existing surfaces and forms, not as new thematic content. Reconstruct the actual wall, floor, sky, water, vegetation, street, terrain, or distant architecture already present in the image.
- Build each transformed region as a coherent continuous voxel mass or tiled surface, not scattered independent squares. Sky blocks should form connected gradient layers; water blocks should form a unified reflective plane; foliage blocks should form recognizable crowns and branches; walls and ground should retain their planes, seams, and material rhythm.
- Every voxel must read as a true three-dimensional solid, not a flat square tile or pixel overlay. Show appropriate top and side faces, extrusion depth, bevel or edge definition, self-shadow, cast shadow, ambient occlusion, and overlap with neighboring cubes. Rotate and foreshorten visible faces according to the scene camera.
- Even planar regions such as sky, walls, roads, and water must use stepped slabs, extruded tiles, or layered block volumes with visible depth changes. A flat checkerboard, posterized mosaic, stair-step silhouette, or 2D pixel filter does not qualify as 3D voxel treatment.
- Maintain a clear hierarchy: a few large structural block masses, supporting medium forms, and fine distant detail. Prefer substantial readable geometry over confetti-like specks.
- Use depth-scaled block sizes as a strict perspective rule: very large cubes and thick edges in the immediate foreground, medium blocks around the focal plane, and progressively smaller, denser blocks toward the horizon and distant background. Nearby blocks should normally appear at least 4–8 times the image-space size of far-background blocks when the composition provides both depths. The transition must be gradual and follow vanishing lines, not appear as three unrelated size bands.
- Use larger foreground blocks to frame and strengthen depth without covering the subject; let distant pixels become finer and slightly lower-contrast through atmospheric perspective.
- Derive the palette directly from the source, then apply a deliberate vivid cinematic grade by default: raise saturation, color separation, local contrast, highlight glow, and material richness while keeping skin tones and protected subject colors believable. Retain the source hue families, aging, stains, weathering, and lighting temperature; intensify existing reds, greens, blues, golds, painted surfaces, foliage, sky, reflections, and practical lights rather than inventing an unrelated palette.
- Avoid gray, muddy, washed-out, low-chroma results. Neutral concrete, haze, fog, stone, and old plaster may remain neutral, but they must be balanced by clear saturated anchor colors from the source and sufficient tonal separation. Atmospheric perspective may reduce distant contrast without draining the whole image of color.
- Keep highlight color and shadow color distinct. Prefer luminous warm/cool relationships, clean chroma, deep but readable shadows, and bright controlled highlights over a uniformly gray or brown cast.
- Match perspective, shadows, reflections, depth of field, and occlusion so the mosaic elements belong in the original scene.
- Preserve some non-pixelated background, but allow selected regions to be substantially and continuously reconstructed so the effect reads as intentional art direction rather than sparse decoration.
- Where suitable, allow a few foreground voxel props to create depth, but never cover defining subject details, entrances, windows, labels, controls, faces, hands, or other focal features.

Avoid:

- pixelating or structurally altering the focal subject itself unless the user explicitly requests it;
- a uniform low-resolution filter over the entire image;
- privacy-style blur, censor mosaics, JPEG artifacts, random square noise, or broken geometry;
- flat pixel mosaics, flat color grids, 2D square overlays, posterized surfaces, or blocks with no visible thickness, side faces, lighting, or cast shadows when the requested mode is 3D voxel;
- isolated floating squares, sparse confetti blocks, disconnected particles, or holes that do not belong to an underlying surface or volume;
- replacing the whole location when selective reconstruction can achieve the requested look;
- adding game menus, HUD overlays, collectible tokens, question blocks, floating platforms, pipes, glowing pickups, characters, slogans, logos, or other game-specific motifs unless the user explicitly requests them;
- cleaning up, modernizing, fantasy-restyling, or recoloring a place in ways unsupported by the source;
- globally desaturated, gray, muddy, faded, brown-cast, or low-contrast color grading unless the user explicitly requests it;
- erasing regional character, historical wear, local signage, practical objects, or ordinary lived-in details;
- using uniform block sizes across foreground and background, or making distant blocks larger than nearby blocks without a scene-based reason;
- changing identity, anatomy, species, architectural structure, product geometry, landscape contours, branding, object count, or other defining attributes without authorization;
- watermarks or signatures.

## Editing workflow

1. Inspect the target and identify its subject class, focal subject, protected details, dominant palette, lighting, perspective, and 2–4 surrounding regions suitable for block reconstruction.
2. State each input image's role internally: edit target or style reference.
3. Build a concise edit prompt using the template below. Name invariants twice: once in the preservation section and once in the final constraints.
4. Generate one strong edit first. Preserve the original aspect ratio unless the user requests another format.
5. Inspect the result. Reject or revise it if any defining subject feature, structure, geometry, composition, source hue family, local character, cultural detail, or perspective drifts; if the result looks like a different place; if the overall image is gray, muddy, washed out, low-saturation, or low-contrast; if foreground blocks are not unmistakably larger than distant blocks; if nearby and distant blocks differ by too little to communicate depth; if cubes lack visible top/side faces, extrusion, shadows, occlusion, or overlap; if transformed regions fragment into floating confetti; or if the result reads as a flat mosaic/filter rather than solid voxel construction.
6. If revision is needed, request one targeted correction at a time, such as “restore the original façade and window spacing exactly” or “reduce the voxel treatment to the sky and distant trees only.”
7. Return the image and briefly describe which background regions were transformed. For a project-bound asset, save a non-destructive copy in the requested workspace location.

## Prompt template

```text
Use case: [identity-preserve for people/recognizable animals; precise-object-edit for other subjects]
Asset type: selective background style edit
Primary request: Keep the supplied image recognizably the same—including its location, culture, materials, palette, age and atmosphere—while expressing selected surrounding regions with polished 3D pixel/voxel blocks.
Input images: Image 1 is the edit target. [Other images and roles, if any.]
Focal subject: [identify the actual person, building, product, landscape feature, animal, vehicle, food item, interior, artwork, or other subject].
Preserve exactly: [list the defining attributes for this subject class]; original framing, camera angle, perspective, focal placement, regional/cultural identity, materials, weathering, signage, dominant palette, lighting direction, and overall mood.
Selective transformation: Re-express only [named surrounding regions] as coherent continuous solid 3D block masses or extruded tiled surfaces while preserving what those regions actually depict. Every cube must show camera-correct top/side faces, thickness, self-shadow, cast shadow, ambient occlusion, and overlap. Sky becomes layered stepped block volumes, water becomes an extruded reflective voxel plane, foliage becomes recognizable volumetric crowns, and planar surfaces retain their geometry through raised and recessed slabs. Target about [25–55]% of the surroundings, not the subject. Avoid isolated floating squares or sparse confetti.
Depth rule: create unmistakable near-large/far-small perspective. Use the largest and deepest blocks in the foreground, medium blocks near the subject plane, and progressively smaller, denser, shallower and lower-contrast blocks toward the horizon. Nearby cubes should usually appear 4–8 times larger than far cubes. Follow the actual vanishing point and scene depth.
Color grade: vivid high-saturation source-derived color; strong color separation; luminous highlights; rich reds, greens, blues and golds already present in the source; deep readable shadows; neutral materials remain believable but do not make the overall image gray or muddy.
Style/medium: high-end source-faithful hybrid image; original photographic or illustrative style remains dominant; solid coherent voxel geometry, cinematic light integration, realistic material response, vibrant color, and clear large/medium/fine hierarchy; no imposed game theme.
Constraints: change only the selected surrounding regions; keep protected subject and place details unchanged; preserve local identity and patina; no gray/washed-out overall grade; no whole-image pixelation; no privacy blur; no random digital noise; no uniform block size; no game props, characters, logos, new readable text, or watermark.
```

Choose the named regions from the actual image rather than using generic placeholders in the final generation prompt.

## User controls

Honor concise modifiers without requiring a questionnaire:

- `轻度`: express about 20–30% of the surroundings with sparse source-matched voxel blocks.
- `中度` (default): express about 35–50% with clear block structure while retaining ample original texture and place identity.
- `强烈`: express about 55–70% of the surroundings with more pronounced large foreground blocks, while still protecting the subject and regional character.
- A named color controls accent colors, but does not erase the source palette unless the user asks for recoloring.
- `自然色`: retain more restrained source saturation while preserving clean color separation.
- `高饱和` (default): use rich, vivid, source-derived color without clipping highlights or making skin/materials fluorescent.
- `2D 像素` favors flat square tiles and sprite-like silhouettes; `3D 体素` requires solid extruded cubes with visible faces, thickness, lighting, shadows and occlusion; otherwise use a balanced hybrid.

If the request does not specify strength, use `中度`. If it does not specify color treatment, use `高饱和`. Always apply near-large/far-small voxel perspective unless the user asks for flat 2D pixel art. If no region is named, choose surrounding regions with clear geometry and the lowest risk of damaging the focal subject. For a building that fills most of the frame, normally protect the building and transform the sky, ground, landscaping, neighboring structures, or street furniture; transform parts of the building itself only when the user explicitly requests that.
