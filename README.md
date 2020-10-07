# vPilot Custom Rule Sets for Microsoft Flight Simulator

This repository contains some default rule sets that are useful when operating on the VATSIM network with Microsoft Flight Simulator.

Core rules are contained within the `core` folder. You should only include the rule sets that match the edition of Microsoft Flight Simulator you own, and those below. For example, if you only have the Game Pass version of MSFS, with no add-ons, then only use the `Standard` rules. If you have the _Premium Deluxe_ edition, then use all three: `Standard`, `Deluxe`, and `Premium`.

The core rule sets look for an exact type match between the VATSIM reported aircraft type and the type for the MSFS model. In order to expand the availability of these custom models, you can also include the `Similar` rule sets, which also map aircraft with similar type codes to their cousins with models in MSFS. For example, a Beechcraft Baron 55 (type `BE55`) is mapped to the Beechcraft Baron G58 in MSFS when using the `Deluxe_Similar` rule set.

Rules should be ordered so that the most standard rule sets come last. In general, `Similar` rule sets should come after other, more specific rules sets, and the `core` rule sets should be placed at the bottom of your rule set list. Additional, more specific rule sets, for specific liveries, etc., should be placed above these core rules.

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
* `Carenado_M20R_Similar.vmr`
* `MSFS_Premium.vmr`
* `MSFS_Premium_Similar.vmr`
* `MSFS_Deluxe.vmr`
* `MSFS_Deluxe_Similar.vmr`
* `MSFS_Standard.vmr`
* `MSFS_Standard_Similar.vmr`

## Contributing

The list of similar aircraft is incomplete, so PRs are welcome to add additional similar aircraft. In addition, I would like to add mappings for third-party aircraft and/or livery into separate folders/files, to make it easier for people to make their world more colorful when operating in VATSIM. Any contributions here would be most welcome.
