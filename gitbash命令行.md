#github的命令行
##
>先创建一个文件

>回到创建的文件


     mkdir learngit
     cd learngit
     pwd


    上面的pwd用于反馈文件路径；


> 使用ssh方式连接github


    ssh -T git@github.com


>在本地文件里创建文件，格式：git add <filename>


    git add hellogit.c 
    生成该文件到仓库；


>在本地文件里提交文件到仓库


    git commit -m"这个m的参数其实提示你提交的文件的意义；"
    eg.  git commit -m"这是一个简单的文件"


>上传文件到github的网站里


    git push origin master
    github的仓库默认是origin；