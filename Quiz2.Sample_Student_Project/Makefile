biuld: KW myexe

all: build doczip

KW: collegemain.o college.o course.o
	g++ -o KW collegemain.o college.o course.o

collegemain.o: collegemain.cc
	g++ -c collegemain.cc

college.o: college.cc college.h node.h
	g++ -c college.cc

course.o: course.cc course.h
	g++ -c course.cc

clean:
	rm *.o *.class a.out

myexe:
	doxygen -g config
	doxygen config

doc:
	doxygen -u config
	doxygen config

doctgz:
	tar cvzf dac.tgz html

doczip:
	tar -cvf file.tar *
