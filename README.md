# Field Robotics Conventions

This documents the standards and conventions used in RESL for field robotics projects.

# How to use

Repositories which conform to this should link to this repo in their README.md

# Frame Convention

All frames should be expressed in East North Up (ENU) coordinate frame. 
Most IMUs and navigational frames are expressed in North East Down (NED), either convert them to ENU or use the method to deviate from the standard below

x should represent the eastward coordinate, increasing as you go eastward.
y should represent the northward coordinate, increasing as you go northward.
z should represnt the "up" (Towards space) coordinate as you go upward.

# Base Units

All base units should be expressed as [SI Base Units](https://en.wikipedia.org/wiki/SI_base_unit)

Temperature is generally expressed in celcius in most repos tho.

# Earth Coordinates

All earth coordinates should be represented as [UTM](https://en.wikipedia.org/wiki/Universal_Transverse_Mercator_coordinate_system) in the ENU frame. 

When possible, carry the zone number and zone letter. Put the zone number before the letter if using a tuple/list.

# Matrix Order

When expressing a matrix which is a list of entries, use row major ordering. That is, each row should be an entry and each column should be a component of a vector.

Example:

| x1 | y1 | z1 |
| x2 | y2 | z2 |
| .. | .. | .. |

# Deviating from this standard

When possible, don't deviate from this standard.

In some situations it is either extremely inconvenient or lossy to convert to this standard in which each method which expects a non-standard argument should be documented.

If possible contain the portion of the program which uses a nonstandard convention to a small portion.


# Coding

Python: Use PEP 8.
