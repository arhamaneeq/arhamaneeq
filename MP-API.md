# MP API v0.45.8

## `MPRester.summary.search` Fields
```python
[
  'builder_meta', 
  'nsites', 'elements', 'nelements', 
  'composition', 'composition_reduced', 'formula_pretty', 'formula_anonymous', 
  'chemsys', 'volume', 'density', 'density_atomic', 'symmetry', 'property_name', 
  'material_id', 'deprecated', 'deprecation_reasons', 'last_updated', 'origins', 'warnings', 
  'structure', 'task_ids', 
  'uncorrected_energy_per_atom', 'energy_per_atom', 'formation_energy_per_atom', 'energy_above_hull', 
  'is_stable', 'equilibrium_reaction_energy_per_atom', 'decomposes_to', 
  'xas', 'grain_boundaries', 
  'band_gap', 'cbm', 'vbm', 'efermi', 'is_gap_direct', 'is_metal', 'es_source_calc_id', 'bandstructure', 'dos', 'dos_energy_up', 'dos_energy_down', 
  'is_magnetic', 'ordering', 'total_magnetization', 'total_magnetization_normalized_vol', 'total_magnetization_normalized_formula_units', 'num_magnetic_sites', 'num_unique_magnetic_sites', 'types_of_magnetic_species', 
  'bulk_modulus', 'shear_modulus', 'universal_anisotropy', 'homogeneous_poisson', 
  'e_total', 'e_ionic', 'e_electronic', 'n', 'e_ij_max', 
  'weighted_surface_energy_EV_PER_ANG2', 'weighted_surface_energy', 'weighted_work_function', 'surface_anisotropy', 'shape_factor', 
  'has_reconstructed', 'possible_species', 'has_props', 'theoretical', 'database_Ids'
]
```

### `structure` field
Data is of form
```python
Full Formula (Ag3 Au1)
Reduced Formula: Ag3Au
abc   :   4.111093   4.111093   4.111093
angles:  90.000000  90.000000  90.000000
pbc   :       True       True       True
Sites (4)
  #  SP       a     b     c    magmom
---  ----  ----  ----  ----  --------
  0  Ag     0.5  -0     0.5         0
  1  Ag    -0     0.5   0.5         0
  2  Ag     0.5   0.5  -0           0
  3  Au    -0    -0    -0          -0
```

The return type is of `pymatgen.core.structure.Structure`.
You can access lattice parameters using `.lattice`, which exposes `.abc`, `.angles`, etc.

```python
>>> print(dir(Structure))
[
  'CellType', 'DISTANCE_TOLERANCE', 'REDIRECT',
'__abstractmethods__', '__annotations__', '__class__', '__class_getitem__', '__contains__', '__delattr__', '__delitem__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__get_pydantic_core_schema__', '__get_pydantic_json_schema__', '__get_validators__', '__getattribute__', '__getitem__', '__getstate__', '__gt__', '__hash__', '__iadd__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__modify_schema__', '__module__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__sizeof__', '__slots__', '__str__', '__subclasshook__', '__weakref__', '_abc_impl', '_calculate', '_generic_json_schema', '_get_neighbor_list_py', '_prep_calculator', '_relax', '_validate_monty',
'add_oxidation_state_by_element', 'add_oxidation_state_by_guess', 'add_oxidation_state_by_site',
'add_site_property', 'add_spin_by_element', 'add_spin_by_site',
'alphabetical_formula', 'append', 'apply_operation', 'apply_strain',
'as_dataframe', 'as_dict', 'atomic_numbers', 'calc_property',
'calculate', 'cart_coords', 'charge', 'chemical_system',
'chemical_system_set', 'clear', 'composition', 'copy', 'count',
'density', 'distance_matrix', 'elements', 'extend',
'extract_cluster', 'formula', 'frac_coords', 'from_ase_atoms',
'from_dict', 'from_file', 'from_id', 'from_magnetic_spacegroup', 'from_prototype',
'from_sites', 'from_spacegroup', 'from_str', 'get_all_neighbors', 'get_all_neighbors_old',
'get_all_neighbors_py', 'get_angle', 'get_dihedral', 'get_distance',
'get_miller_index_from_site_indexes', 'get_neighbor_list', 'get_neighbors', 'get_neighbors_in_shell',
'get_neighbors_old', 'get_orderings', 'get_primitive_structure', 'get_reduced_structure',
'get_sites_in_sphere', 'get_sorted_structure', 'get_space_group_info', 'get_symmetric_neighbor_list',
'get_symmetry_dataset', 'group_by_types', 'index', 'indices_from_symbol', 'insert', 'interpolate',
'is_3d_periodic', 'is_ordered', 'is_valid', 'labels', 'lattice', 'load', 'make_supercell', 'matches',
'merge_sites', 'n_elems', 'ntypesp', 'num_sites', 'pbc', 'perturb', 'pop', 'properties', 'reduced_formula',
'relabel_sites', 'relax', 'remove', 'remove_oxidation_states', 'remove_site_property', 'remove_sites',
'remove_species', 'remove_spin', 'replace', 'replace_species', 'reverse', 'rotate_sites', 'save',
'scale_lattice', 'set_charge', 'site_properties', 'sites', 'sort', 'species', 'species_and_occu', 'substitute',
'symbol_set', 'to', 'to_ase_atoms', 'to_cell', 'to_conventional', 'to_file', 'to_json', 'to_primitive',
 'translate_sites', 'types_of_specie', 'types_of_species', 'unsafe_hash', 'unset_charge',
 'validate_monty_v1', 'validate_monty_v2', 'volume'
]
```
