# vPilot Custom Rule Sets for Microsoft Flight Simulator

This repository contains some default rule sets that are useful when operating
on the VATSIM network with Microsoft Flight Simulator.

Core rules are contained within the `core` folder. You should only include the
rule sets that match the edition of Microsoft Flight Simulator you own, and
those below. For example, if you only have the Game Pass version of MSFS, with
no add-ons, then only use the `Standard` rules. If you have the _Premium Deluxe_
edition, then use all three: `Standard`, `Deluxe`, and `Premium`.

The core rule sets look for an exact type match between the VATSIM reported
aircraft type and the type for the MSFS model. In order to expand the
availability of these custom models, you can also include the `Similar` rule
sets, which also map aircraft with similar type codes to their cousins with
models in MSFS. For example, a Beechcraft Baron 55 (type `BE55`) is mapped to
the Beechcraft Baron G58 in MSFS when using the `Deluxe_Similar` rule set.

Rules should be ordered so that the most standard rule sets come last. vPilot
steps through the rules and rule sets from top to bottom. The first matching
rule it hits determines the model it will use, so the most specific rules and
rule sets should appear at the top of your list. Thus, in general, `Similar`
rule sets should come after other, more specific rules sets, and the `core` rule
sets should be placed at the bottom of your rule set list. Additional, more
specific rule sets, for specific liveries, etc., should be placed above these
core rules.

* Liveries based on call sign and type code
* Liveries based on call sign and similar code
* Default models based on type code
* Default models based on similar type code
* Core rules, with similar type codes between levels

The below provides an example of an appropriate ordering:

* `KAP_Deluxe.vmr`
* `KAP_Standard.vmr`
* `KAP_Deluxe_Similar.vmr`
* `KAP_Standard_Similar.vmr`
* `Carenado_M20R.vmr`
* `Carenado_C182.vmr`
* `Carenado_M20R_Similar.vmr`
* `Carenado_C182_Similar.vmr`
* `MSFS_Premium.vmr`
* `MSFS_Premium_Similar.vmr`
* `MSFS_Deluxe.vmr`
* `MSFS_Deluxe_Similar.vmr`
* `MSFS_Standard.vmr`
* `MSFS_Standard_Similar.vmr`

## Contributing

The list of similar aircraft is incomplete, so PRs are welcome to add additional
similar aircraft. In addition, I would like to add mappings for third-party
aircraft and/or livery into separate folders/files, to make it easier for people
to make their world more colorful when operating in VATSIM. Any contributions
here would be most welcome.

## vPilot Default Rules

Included here primarily for reference, you can find the default vPilot rules for
MSFS in this repository as well. They come embedded into vPilot, so you _do not_
need to add them as a custom rule set.

## My airplane avionics keep turning off…

There's a bug currently known to Asobo where models loading into the sim can
result in your panel lights, throttle, and avionics being altered in flight.
This generally does not happen with the generic models. One workaround is to use
generic models for AI and Multiplayer traffic, as those models don't have the
systems that would interfere with the airplane you are currently flying. Those
options can be found under the Graphics settings, down near the bottom.

For users that find this bug particularly annoying, I've added a set of matching
rules that take the vPilot defaults, and swap in generic models for _all_
aircraft, so as to allow you to prevent vPilot from loading in models that will
affect your experience.

You can find that custom matching rule as `Generic_Everything.vmr`. Please file
an issue if you experience any problems with loading the models in this rule
set.
