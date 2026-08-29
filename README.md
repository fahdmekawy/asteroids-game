# Asteroids Game

A classic Asteroids arcade game clone built in Python with [Pygame](https://www.pygame.org/). Pilot a ship, dodge asteroids, and blast them into smaller pieces before they get you.

## Features

- Player-controlled ship with rotation and thrust-based movement
- Procedurally spawning asteroid field
- Shooting mechanic with a cooldown timer
- Collision detection between the player, asteroids, and shots
- Asteroids split into smaller fragments when hit
- Simple event/state logging

## Requirements

- Python 3.13+
- [pygame](https://www.pygame.org/) 2.6.1

## Installation

This project uses [uv](https://docs.astral.sh/uv/) for dependency management (a `uv.lock` file is included).

```bash
# Clone the repository
git clone https://github.com/fahdmekawy/asteroids-game.git
cd asteroids-game

# Install dependencies with uv
uv sync
```

Alternatively, using plain `pip`:

```bash
git clone https://github.com/fahdmekawy/asteroids-game.git
cd asteroids-game

python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

pip install pygame==2.6.1
```

## Running the Game

With `uv`:

```bash
uv run main.py
```

Or with a plain virtual environment:

```bash
python main.py
```

## Controls

| Key     | Action        |
| ------- | ------------- |
| `W`     | Move forward  |
| `S`     | Move backward |
| `A`     | Rotate left   |
| `D`     | Rotate right  |
| `Space` | Shoot         |

Destroy asteroids before they collide with your ship — colliding with one ends the game.

## Project Structure

```
.
├── main.py            # Game loop and entry point
├── player.py           # Player ship: movement, rotation, shooting
├── asteroid.py          # Asteroid behavior and splitting logic
├── asteroidfield.py       # Spawns asteroids over time
├── shot.py             # Projectile behavior
├── circleshape.py         # Shared base class for circular game objects
├── constants.py          # Game configuration (speeds, sizes, screen dimensions, etc.)
├── logger.py            # Event/state logging
└── pyproject.toml         # Project metadata and dependencies
```

## License

No license specified.
