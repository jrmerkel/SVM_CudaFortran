svm: svm.cuf data_load.cuf makefile
	nvfortran -o svm -Minfo=accel -stdpar -cuda svm.cuf data_load.cuf

unittests: unit_tests.cuf svm_unit.cuf gpu_svm_unit.cuf data_load.cuf makefile
	nvfortran -o unit_test -Minfo=accel -stdpar -cuda unit_tests.cuf svm_unit.cuf gpu_svm_unit.cuf data_load.cuf

gpu_svm: gpu_svm.cuf data_load.cuf makefile
	nvfortran -o gpu_svm -g  -Minfo=accel -Minline=gpu_kernel -O2 -Mlarge_arrays -cuda -stdpar gpu_svm.cuf data_load.cuf
