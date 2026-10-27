# Twisted, rotating magnetar magnetosphere in general relativity

**Interactive 3D viewer:** https://nadoltitan.github.io/magnetar-pinn-3d/

Nadol Pipattikanan, Chulalongkorn University.

This page shows the magnetic field B and electric field E around a neutron star. A
physics-informed neural network (PINN) computed both. The network is trained so that its output satisfies
the force-free Maxwell equations on a Schwarzschild (curved spacetime) background. No simulation data is
used. The physics equations themselves are the loss.

Two models can be compared with the Model slider. They share the same network, recipe, spin and training
budget. The only difference is the twist.

| | Twisted | Untwisted control |
|---|---|---|
| What it is | Twisted and rotating magnetosphere, with E and B trained together | The same model trained with the twist switched off |
| Twist | Hot spot at 45 deg colatitude, alpha_0 = 2.5 | alpha = 0 everywhere, a plain dipole |
| Spin | Trained at the real spin of PSR J1745-2900 | Same |

The twisted field carries a toroidal component (B_phi) and a current-carrying hot spot on the surface. The
untwisted control has no toroidal field, so it shows what the rotating dipole looks like without the twist.

## Parameters (both models)

| Quantity | Value |
|---|---|
| Star radius R | 12 km |
| Mass M | 1.40 solar masses (GM/(c^2 R) = 0.172) |
| Surface field B0 | 1.6e10 T (1.6e14 G) |
| Spin period P | 3.76 s (PSR J1745-2900) |
| Omega R / c | 6.68e-5 |
| Light cylinder | about 1.8e5 km, far outside the plotted region |

The full table for each model appears in the viewer sidebar. Each value is marked *trained* (an input of
that training run), *supplied* (given only for display) or *derived* (computed from the others).

## Units

All quantities are SI. Distances are in km, and hovering a field line also shows r/R. B is in tesla, E is
in V/m, and charge density is in C/m^3.

## How to use

The page is one self-contained HTML file and needs no install. Open the link above, then drag to rotate
and scroll to zoom. In the sidebar you can switch E layers, B seed latitude and zoom window.
