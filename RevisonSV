<php
//go trougth each rev of the svn commit history and extract the content with this php function
///Revision\s[0-9]{0,9}|-[0-9]{0,9}/gm 

filepattern='test/*.php';
$tagpattern='/\<\?\n\/\*\n\{\(\'([^\']+)\'\)\}\n\*\/\n\?\>/';

$files=glob($filepattern);

foreach ($files as $file)
{ 
$content=file_get_contents($file);  $count=preg_match_all($tagpattern,$content,$matches);  

if ($count<1) continue;
//Whatever you want to do with the matches! 

foreach ($matches[1] as $match) echo "$file: $match\n";
} 


?>
