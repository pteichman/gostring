# gostring
A command line tool for Go string escaping binary files.

Example:

    $ gostring main.go
    "package main\n\nimport (\n\t\"fmt\"\n\t\"io/ioutil\"\n\t\"os\"\n)\n\nfunc main() {\n\tif len(os.Args) < 2 {\n\t\tfmt.Println(\"usage: gostring <file>\")\n\t\tos.Exit(1)\n\t}\n\n\tbuf, err := ioutil.ReadFile(os.Args[1])\n\tif err != nil {\n\t\tfmt.Printf(\"%s\\n\", err)\n\t\tos.Exit(1)\n\t}\n\n\tfmt.Printf(\"%q\", buf)\n}\n"
