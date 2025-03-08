./xopp2pdf-with-nested.sh input_folder output_folder(writer/data)

tree data --noreport -X -o data.xml


git add -A
git commit -m "Updated"
git push

#!/bin/bash

inputFolder="/home/akash/doc/books/"
projectFolder="/home/akash/doc/projects/library/"

cd $inputFolder
$projectFolder/xopp2pdf-with-nested.sh . $projectFolder/data/
cd $projectFolder

echo "Run the following in  $projectFolder"
tree data --noreport -X -o data.xml
git add -A
git commit -m 'updated'
git push



