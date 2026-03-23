

## Section 1 — Location and Jurisdiction

[REQUIRED]

property_name:
property_owner:
property_address:
city:
state_province:
county_parish_district:
country:
postal_code:
gps_latitude:
gps_longitude:
jurisdiction_primary:
jurisdiction_secondary:
parcel_number:
legal_description:
land_registry_reference:
building_department_name:
building_department_phone:
building_department_address:
building_department_hours:
building_department_url:
health_department_name:
health_department_phone:
zoning_department_name:
zoning_department_phone:

---

## Section 2 — Climate and Environmental

[REQUIRED — drives insulation, HVAC, foundation, and structural calculations]

climate_zone_framework:
climate_zone:
temperature_winter_design:
temperature_summer_design:
temperature_record_low:
temperature_record_high:
annual_rainfall_inches_mm:
annual_snowfall_inches_mm:
ground_snow_load:
roof_snow_load:
wind_speed_design:
wind_exposure_category:
seismic_design_category:
seismic_site_class:
frost_depth:
humidity_classification:
latitude_decimal:
average_sun_hours_per_day:
prevailing_wind_direction:
soil_type:
soil_bearing_capacity:
soil_classification:
expansive_soil_flag:
high_water_table_flag:
high_water_table_depth:
flood_zone_designation:
flood_zone_source:
wildfire_risk_zone:
tornado_risk_zone:
hurricane_risk_zone:

---

## Section 3 — Infrastructure and Utilities

[REQUIRED — drives cascade calculations across all buildings on property]

electrical_service_provider:
electrical_service_size:
electrical_service_voltage:
electrical_service_frequency:
electrical_meter_location:
electrical_panel_location:
electrical_panel_capacity:
electrical_panel_spaces_available:
electrical_system_standard:
generator_present:
generator_size_kw:
generator_fuel_type:
generator_transfer_switch_type:
generator_transfer_switch_location:
generator_location:
solar_present:
solar_array_size_kw:
solar_panel_count:
solar_inverter_type:
solar_battery_present:
solar_battery_size_kwh:
solar_grid_tied:
solar_array_location:
water_source:
water_service_provider:
water_service_size:
water_pressure_psi:
water_meter_location:
water_line_material:
water_line_depth:
water_line_route:
well_present:
well_location:
well_depth:
well_yield_gpm:
well_pump_size:
well_pump_location:
well_pressure_tank_location:
well_setback_radius:
well_registration_number:
septic_present:
septic_system_type:
septic_permitted_capacity_bedrooms:
septic_permitted_capacity_gpd:
septic_tank_location:
septic_tank_size_gallons:
septic_drain_field_location:
septic_drain_field_area:
septic_permit_number:
septic_installation_date:
septic_last_pumped:
greywater_system_present:
greywater_approval_status:
gas_service_type:
gas_service_provider:
gas_meter_location:
propane_tank_present:
propane_tank_size_gallons:
propane_tank_location:
propane_tank_ownership:
propane_supplier:
propane_total_btu_load:
internet_provider:
internet_service_type:
internet_speed_mbps:
internet_connection_location:
cell_signal_strength:
cell_carrier:
driveway_type:
driveway_surface:
driveway_width:
driveway_length:
driveway_max_vehicle_weight:
emergency_vehicle_access:
gate_present:
gate_type:
gate_location:
drainage_direction:
drainage_outlets:
retention_pond_present:
retention_pond_location:
tile_drainage_present:
tile_drainage_map_available:

---

## Section 4 — Zoning and Legal

[REQUIRED — determines what can be built, where, and under what conditions]

zoning_classification:
zoning_description:
zoning_overlay_districts:
permitted_use_residential:
permitted_use_agricultural:
permitted_use_commercial:
permitted_use_industrial:
permitted_use_accessory_structures:
permitted_use_home_occupation:
permitted_use_short_term_rental:
setback_front:
setback_rear:
setback_side_left:
setback_side_right:
setback_from_well:
setback_from_septic:
setback_from_water_feature:
setback_from_wetland:
setback_from_road_centerline:
setback_from_easement:
maximum_building_height:
maximum_structure_height:
maximum_lot_coverage_percent:
maximum_impervious_surface_percent:
maximum_accessory_structure_size:
maximum_accessory_structure_count:
accessory_structure_height_limit:
accessory_structure_setback_notes:
utility_easement_locations:
utility_easement_widths:
access_easement_locations:
drainage_easement_locations:
conservation_easement_present:
conservation_easement_details:
right_of_way_locations:
right_of_way_widths:
wetland_present:
wetland_location:
wetland_setback_required:
floodplain_present:
floodplain_designation:
floodplain_restrictions:
protected_species_flag:
protected_species_notes:
ownership_status:
purchase_date:
title_clear:
title_insurance_present:
survey_complete:
survey_date:
survey_file_location:
hoa_present:
hoa_name:
hoa_restrictions:

---

## Section 5 — Existing Structures

[Complete one entry per existing structure on the property]

# Copy the block below for each existing structure
# Add as many blocks as needed

# ------- EXISTING STRUCTURE ENTRY -------

structure_name:
structure_type:
structure_purpose:
structure_year_built:
structure_condition:
structure_size_width:
structure_size_depth:
structure_size_height_eave:
structure_size_height_ridge:
structure_foundation_type:
structure_wall_construction:
structure_roof_type:
structure_roof_material:
structure_heated:
structure_conditioned_area:
structure_electrical_connected:
structure_electrical_panel_size:
structure_electrical_panel_location:
structure_water_connected:
structure_water_line_size:
structure_sewer_connected:
structure_sewer_type:
structure_gas_connected:
structure_gas_line_size:
structure_internet_connected:
structure_permit_on_file:
structure_permit_number:
structure_as_built_drawings_available:
structure_known_issues:
structure_planned_modifications:
structure_assigned_inventory_items:

# ------- END EXISTING STRUCTURE ENTRY -------

existing_structures_count:
existing_structures_total_sqft:
existing_structures_notes:

---

## Section 6 — International and Code Framework

[REQUIRED — drives unit system, code selection, and data sources]

country_code:
# US — United States
# CA — Canada
# AU — Australia
# GB — United Kingdom
# NZ — New Zealand

unit_system:
# us_customary — feet, inches, pounds, Fahrenheit
# metric — meters, millimeters, kilograms, Celsius

currency_code:
# USD / CAD / AUD / GBP / NZD

electrical_voltage:
electrical_frequency:
electrical_outlet_standard:
building_code_framework:
code_residential:
code_commercial:
code_electrical:
code_plumbing:
code_mechanical:
code_energy:
code_fire:
code_local_amendments:
climate_zone_framework:
seismic_design_required:
seismic_design_standard:
seismic_zone:
wind_design_standard:
data_source_flood:
data_source_soil:
data_source_wetlands:
data_source_elevation:
data_source_parcels:
data_source_well_registry:
primary_language:
secondary_language:
supplier_search_radius_primary_km_miles:
supplier_search_radius_secondary_km_miles:
supplier_search_radius_specialty_km_miles:
regional_data_gaps:

## Section 7 — Planned Structures

[Complete one entry per planned structure on the property]

# Copy the block below for each planned structure
# Add as many blocks as needed
# These become the projects that flow through
# the full suite pipeline

# ------- PLANNED STRUCTURE ENTRY -------

planned_structure_name:
planned_structure_type:
planned_structure_purpose:
planned_structure_priority:
planned_structure_timeline:
planned_structure_budget_range:
planned_structure_site_location:
planned_structure_scenario:
planned_structure_status:
# status options:
# concept — just an idea
# planning — actively being planned in suite
# permitted — permit application filed
# under_construction — build in progress
# complete — built and occupied

# ------- END PLANNED STRUCTURE ENTRY -------

planned_structures_count:
planned_structures_notes:

---

## Section 8 — Substitution Rule and Usage Notes

# HOW CLAUDE READS THIS FILE

# At the start of every session Claude reads this
# property record before any other file.
# Every tagged value in every suite file gets
# substituted with the real value from this record.

# Tag format used throughout the suite:
# [PROPERTY RECORD: field_name]

# Example substitutions:
# [PROPERTY RECORD: frost_depth] → 24 inches
# [PROPERTY RECORD: wind_speed_design] → 115 mph
# [PROPERTY RECORD: country_code] → US
# [PROPERTY RECORD: climate_zone] → 4A

# WHAT CLAUDE DOES WITH BLANK FIELDS

# Blank fields are flagged at the point of need:
# 🟢 Complete — value present and confirmed
# 🟡 Missing — value needed, instructions provided
# 🔴 Blocking — must resolve before proceeding

# Claude never guesses a blank field value.
# Claude never skips a red flagged field.
# Claude always tells the user exactly how to
# find the missing value.

# HARDCODED VALUE RULE

# If any file in the suite contains a
# property-specific value that is not tagged
# with [PROPERTY RECORD: field_name] that is
# an error. Flag it and replace it with the
# correct tag referencing this file.

# SESSION START SEQUENCE

# Every new Claude session loads files
# in this order:
# 1. core/README.md
# 2. property_record/[property_name].md  ← this file
# 3. handoffs/ relevant to current task
# 4. Files relevant to current task only

# Never load the full suite in one session.
# Load only what the current task requires.
# The property record is always loaded first.

# ADDING A NEW FIELD

# If a new field is needed:
# 1. Add it to this template first
# 2. Add it to the relevant property file
# 3. Add the substitution tag to any file
#    that needs the value
# 4. Update changelog.md with the change
# Never add a field to a property file
# without adding it to the template first.

# VERSION TRACKING

template_version: 1.0
template_created: 2026-03-22
template_created_by: Anthony Pfeifer + Claude
template_last_updated:
template_changelog: core/changelog.md

---

# END OF TEMPLATE
# Copy this file to create a new property record
# Fill in all known values
# Leave unknown values as [UNKNOWN]
# Leave non-applicable values as [NOT APPLICABLE]
# Never delete a field — blank is better than missing