CONFIG STATE BUILDER 
github: https://github.com/data-storage-lab/ConfD

The configuration state builder is a script which generates configuration states to be tested/used in the ConfD-plugins.
There are actually two scripts which handle generating states. The first is config_state_builder, which creates valid states to be used in most of the plugings. There is also violate_config_state_builder, which creates intentionally invalid states to be used in plugin #2 
The script requires a couple of json file inputs:

	mke2fs_constraings.json - Generated from the Dependency Analyzer script. Describes configuration parameter constraints. 
	default_config.json     - Hand-crafted json which describes the default configuration a FS tool uses. 
	
	
Running the script:

	python3 config_state_builder.py <max_depth> <max_final_states>
	
	Example:
	python3 config_state_builder.py 3 1000
	
	
	
	python3 violate_config_state_builder.py <max_depth> <max_final_states> <mis-spell enable (true) or disable (false)>
	
	Example:
	python3 violate_config_state_builder.py 3 1000 true

Reading the results:
	
	The script outputs to the terminal runtime information. Every time a new valid state is generated it notes the depth, total number of states generated, current state, and current configuration parameter being modified. This information is useful for debuging. 
	
	There is also a file generated called output.txt. This file contains all the final states generated, in a format that can be used by ConfD-plugins. 
