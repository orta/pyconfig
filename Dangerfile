# Sometimes it's a README fix, or something like that - which isn't relevant for
# including in a project's CHANGELOG for example
declared_trivial = pr_title.include? "#trivial"

# Make it more obvious that a PR is a work in progress and shouldn't be merged yet
warn("PR is classed as Work in Progress") if pr_title.include? "[WIP]"

# Warn when there is a big PR
warn("Big PR") if lines_of_code > 50

# Warn when the makefile sees changes
warn("Changes to build files") if modified_files.include?("Makefile") || modified_files.include?("Gemfile") || modified_files.include?("Dangerfile")


# Fail if changes to License or CoC
fail("Do not modify the license or Code of Conduct") if modified_files.include?("LICENSE") || modified_files.include?("contributing.md")