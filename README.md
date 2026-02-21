# rank-cat-emotional-resonance

Ranks cat pictures by emotional resonance — the depth and immediacy of genuine feeling each image is likely to provoke in a viewer. The core question is simple: *does this picture make you feel something real, and how powerfully does it do so?*

## How It Works

`rank-cat-emotional-resonance` is a **vector function**. It accepts an array of cat images (minimum 2) and returns a normalized score vector that ranks them relative to each other. Images that provoke stronger emotional responses receive higher scores. The scores sum to 1, representing each image's share of the total emotional resonance across the set.

Technical quality, composition, breed, and aesthetic polish are deliberately ignored. A blurry phone snapshot of a kitten doing something unexpectedly tender can — and should — outrank a pristine studio portrait of a cat sitting still, if the snapshot makes you feel more.

## Input

| Field | Type | Description |
|-------|------|-------------|
| `input` | `array` (min 2 items) | A collection of cat pictures to rank by emotional resonance. |
| `input[n]` | `image` | A picture of a cat to evaluate for the depth and immediacy of emotional response it provokes. |

Images arrive without metadata, captions, or backstory. The function evaluates each image cold — relying entirely on what the image itself communicates — because emotional resonance must live in the image, not in an explanation.

## Output

A normalized vector of numbers (one per input image) that sum to 1. Each value represents the relative emotional resonance of the corresponding image within the set. Higher values indicate images that provoke stronger, more genuine emotional responses.

## What It Evaluates

Emotional resonance is not a single property. It is the product of three distinct qualities, each evaluated independently by a dedicated sub-function. An image may be strong in one dimension and weak in another; the interplay between all three determines the final ranking.

### 1. Immediacy of Impact — [{{ .Task0 }}](https://github.com/{{ .Owner }}/{{ .Task0 }})

The speed and involuntariness of the emotional reaction. Does this image hit the viewer before they have time to think? A reflexive laugh, a sudden gasp, an involuntary softening of the face — these are signs of high immediacy. The emotional content is front and center, seizing attention the instant the image registers. No study, no context, no interpretation required. This dimension measures the gut-punch moment: the first half-second of contact.

### 2. Depth of Feeling — [{{ .Task1 }}](https://github.com/{{ .Owner }}/{{ .Task1 }})

The weight and staying power of the emotional response beyond the initial reaction. Does the image make the viewer linger, return, remember? High-depth images capture something that gestures toward larger human experiences — tenderness, vulnerability, innocence, companionship, wonder — in a way that settles beneath the surface and resurfaces unbidden later. This dimension measures not just whether the viewer reacts, but whether the feeling endures.

### 3. Urge to Share — [{{ .Task2 }}](https://github.com/{{ .Owner }}/{{ .Task2 }})

The compulsion to immediately show the image to someone else. An image that scores highly here carries an emotional charge so potent that experiencing it alone feels incomplete — it makes sharing feel like a reflex, not a choice. This dimension captures the universality and transferability of the emotional response: the confidence that the image will reliably land for nearly anyone who sees it. It serves as a natural check on the other two dimensions, filtering out reactions that are too mild to share or too personal to transfer.

## Use Cases

- **Social media curation** — Surface the cat images most likely to stop someone mid-scroll from a large pool of community submissions.
- **Greeting card design** — Identify the image that will make a stranger in a store pick up a card and smile involuntarily.
- **Animal shelter adoption pages** — Feature the photos most likely to create an immediate emotional bond between a potential adopter and a cat they have never met.
- **Content ranking** — Provide a principled, consistent way to separate images that make people *feel* from images that merely *show*, at any scale.

## Philosophy

Without emotional resonance, a cat picture is just documentation — proof that a cat existed in a place at a time. With it, a cat picture becomes a small gift. This function measures the gift: the catch in your breath, the softening behind your eyes, and the hand that reaches for the phone to send the picture to someone you love. Everything else is just photography.
