fish_comp = dependency('fish', required: false)

if get_option('fish-completions')
	fish_files = files(
		'completions/fish/grim.fish',
	)
	if fish_comp.found()
		fish_install_dir = fish_comp.get_pkgconfig_variable('completionsdir')
	else
		fish_install_dir = join_paths(datadir, 'fish', 'vendor_completions.d')
	endif
	install_data(fish_files, install_dir: fish_install_dir)
endif
