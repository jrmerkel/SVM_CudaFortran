svm: svm.cuf data_load.cuf
	nvfortran -o svm -Minfo=accel -stdpar -cuda svm.cuf data_load.cuf

unittests: unit_tests.cuf svm.cuf gpu_svm.cuf data_load.cuf
	nvfortran -o unit_test -Minfo=accel -stdpar -cuda unit_tests.cuf svm.cuf gpu_svm.cuf data_load.cuf

gpu_svm: gpu_svm.cuf data_load.cuf
	nvfortran -o gpu_svm -Minfo=accel -Mlarge_arrays -stdpar -cuda gpu_svm.cuf data_load.cuf
