# vlf
macro for vlf analysis
first $tar -xvf vlf.tar
to compile: $make compile_ROOT_Delphes
to run: $./vlf_analyzer <inputfile.root>  <out_vlf_file.root>
<inputfile.root> is the file from Delphes
<out_vlf_file.root> is the file with the hisograms produced by vlf_analyzer
to plot histograms edit vlfplot.cc and change the line: Tfile *f1=new Tfile("<out_vlf_file.root>")
$root -l vlfplot.cc
If you want to overlay signal and background histograms use vlfplot2.cc, changing the names of the root files inside the macro
Then $root -l vlfplot2.cc
