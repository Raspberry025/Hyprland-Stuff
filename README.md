# Hyprland-Stuff

A curated Hyprland configuration focused on understanding and experimenting with modern Wayland compositor behavior. This repository captures practical configuration patterns for window management, input handling, and workspace control using Hyprland’s declarative configuration model.

The project is intentionally minimal. It prioritizes clarity, discoverability, and hands-on learning over completeness or opinionated defaults.

---

## Description

This repository centers around a single root configuration file, [`hyprland.conf`](./hyprland.conf), which defines how Hyprland behaves at runtime. The configuration demonstrates how Hyprland exposes compositor behavior through a readable, text-based configuration rather than plugins or scripting layers.

The setup is designed for developers interested in:
- Wayland-native desktop environments
- Declarative system configuration
- Keyboard-driven workflows
- Lightweight user-space customization without heavy tooling

---

## Techniques Demonstrated

The configuration uses several Hyprland and Wayland concepts that are useful beyond basic setups:

- **Declarative window rules**  
  Window behavior (floating, tiling, workspace assignment) is defined using rule-based matching instead of runtime hooks.  
  https://wiki.hypr.land/Configuring/Window-Rules/

- **Keyboard-centric input mapping**  
  Keybindings drive workspace navigation and window control with minimal reliance on pointer input.  
  Wayland input concepts:  
  https://wayland.freedesktop.org/docs/html/

- **Dynamic workspace management**  
  Workspaces are managed dynamically rather than being statically enumerated.  
  https://wiki.hypr.land/Configuring/Workspaces/

- **Separation of compositor logic from UI tooling**  
  The configuration avoids embedding UI concerns directly, allowing external tools to integrate cleanly.

---

## Technologies and Ecosystem Components

While this repository does not bundle external libraries, it relies on and interacts with the following non-obvious technologies relevant to experienced developers:

- **Hyprland** — Wayland compositor  
  https://github.com/hyprwm/Hyprland

- **Wayland** — Display server protocol  
  https://wayland.freedesktop.org/

- **wlroots** — Modular Wayland compositor library (used internally by Hyprland)  
  https://gitlab.freedesktop.org/wlroots/wlroots

- **libinput** — Linux input subsystem  
  https://wayland.freedesktop.org/libinput/doc/latest/

No third-party UI frameworks, themes, or fonts are bundled in this repository. The configuration is intentionally compositor-focused.

---

## Project Structure

```text
.
├── hyprland.conf
└── README.md
```
---

hyprland.conf
- The primary Hyprland configuration file. All behavior—keybindings, workspace logic, and window rules—is defined here.
- The flat structure is intentional to keep the configuration easy to audit, fork, and adapt.

## Scope and Intent

This repository is not a distribution, framework, or turnkey desktop setup. It exists to document experimentation and serve as a reference point for developers evaluating Hyprland or Wayland-based workflows.

---

If you want next steps, I can:
- Tighten this further for **portfolio / recruiter review**
- Add a **design rationale section**
- Annotate `hyprland.conf` with inline explanations
- Expand this into a **dotfiles-style repository structure**

Just say which direction you want.

---
