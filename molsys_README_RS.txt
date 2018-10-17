NOTES:_

from_CIF reads a cif and adds atosmand bond to a molecular graph
(in strcucture_data.py)

mg = MolecularGraph(name=clean(cifname))

#add atom nodes
    id = cifobj.block_order.index('atoms')
    atheads = cifobj._headings[id]
    for atom_data in zip(*[data[i] for i in atheads]):
        kwargs = {a:j.strip() for a, j in zip(atheads, atom_data)}
        mg.add_atomic_node(**kwargs)

    # add bond edges, if they exist
    try:
        id = cifobj.block_order.index('bonds')
        bondheads = cifobj._headings[id]
        for bond_data in zip(*[data[i] for i in bondheads]):
            kwargs = {a:j.strip() for a, j in zip(bondheads, bond_data)}
            mg.add_bond_edge(**kwargs)

to do:
generate a mg object and fill from mol object in molsys

make a sim object from LammpsSimulation and with set_graph and set_cell add molecular graph 
to it.

then sim.assign_force_fields() makes the force field (what does sim.compute_simulation_size()
and sim.merge_graphs() do?)

then sim.write_lammps_files() writes files via
construct_data_file() in lammps_main.py

(and construct_input_file())


We could replace ff2lammps completely by this thing for UFF and UFF4MOF ....

