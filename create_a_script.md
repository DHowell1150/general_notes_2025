Create a Script or Template

If you want to make this process even faster next time, create a shell script:

    #!/bin/bash

    echo "Project name:"
    read name

    rails new $name --database=postgresql
    cd $name
    git init
    gh repo create $name --public --source=. --remote=origin --push
    code .

Save as new_rails_project.sh, make it executable, and run it anytime.

(You’ll need GitHub CLI gh installed for that gh repo create to work.)

____
🔁 Next Time

Just run:

    rails new your-next-project --database=postgresql
    cd your-next-project
    git init
    git remote add origin https://github.com/YOU/your-next-project.git
    git add .
    git commit -m "Initial commit"
    git push -u origin main
    code .

