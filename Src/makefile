svm: svm.cuf data_load.cuf
	nvfortran -o test -Minfo=accel -stdpar -cuda svm.cuf data_load.cuf

unittests: unit_tests.cuf svm.cuf data_load.cuf
	nvfortran -o unit_test -Minfo=accel -stdpar -cuda unit_tests.cuf svm.cuf data_load.cuf