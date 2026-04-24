# Azure ImageGen Prompts

Current working image path in this repo: Azure `gpt-image-2` via `skills/gpt-image-2/scripts/gpt_image_2.py`.

```bash
python3 skills/gpt-image-2/scripts/gpt_image_2.py \
  --base-url "https://ryuen-mlark298-eastus2.cognitiveservices.azure.com" \
  --deployment "gpt-image-2" \
  --prompt "Original child-friendly storybook illustration for a Traditional Chinese flashcard game: a cheerful little green dragon teacher reading a blank flashcard in a sunny classroom, warm golden light, playful smile, rounded shapes, clean bold outlines, rich pastel colors, premium kids app art, no text, no letters, square composition" \
  --output examples/chinese-flashcards/assets/dragon-reader.png \
  --size 1024x1024
```

```bash
python3 skills/gpt-image-2/scripts/gpt_image_2.py \
  --base-url "https://ryuen-mlark298-eastus2.cognitiveservices.azure.com" \
  --deployment "gpt-image-2" \
  --prompt "Original premium mascot illustration for a Traditional Chinese flashcard game: a round smiling red panda classmate holding a blank flashcard, cozy playful learning corner, soft peach and cream palette, crisp outlines, fluffy texture, charming children's app art, no text, no letters, square composition" \
  --output examples/chinese-flashcards/assets/red-panda-helper.png \
  --size 1024x1024
```

```bash
python3 skills/gpt-image-2/scripts/gpt_image_2.py \
  --base-url "https://ryuen-mlark298-eastus2.cognitiveservices.azure.com" \
  --deployment "gpt-image-2" \
  --prompt "Original whimsical illustration for a Traditional Chinese flashcard game: a cute moon rabbit floating beside blank learning cards, dreamy pastel night sky, glowing stars, soft clouds, gentle smile, polished children's app artwork, clean outlines, no text, no letters, square composition" \
  --output examples/chinese-flashcards/assets/moon-rabbit.png \
  --size 1024x1024
```

Generated successfully on 2026-04-24. The game can now load the PNG assets directly.

Older MAI note: the Azure MAI helper was patched to use `/models/images/generations?api-version=2024-05-01-preview`, but the configured `MAI-Image-2` deployment still returned HTTP 500 in this repo.

Current working image path is `gpt-image-2`, not the MAI deployment. The SVG files remain as fallbacks if a PNG fails to load.
