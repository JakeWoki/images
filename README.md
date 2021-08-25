# images


```
public class Test {



    public static void main(String[] args) {
        LocalDate localDate = LocalDate.now();
        localDate = localDate.plusDays(128 + 365 + 365 + 366 + 365 + 365 + 366);
        for (int i = 0; i < 365; i++) {
            localDate = localDate.plusDays(1);
            DateTimeFormatter formatter = DateTimeFormatter.ofPattern("yyyy-MM-dd");
            String value = formatter.format(localDate);

            String path = "C:/Users/12976/git/images/2028/" + value;
            File dir = new File(path);
            if (!dir.exists()) {// 判断目录是否存在
                dir.mkdir();

                try {
                    BufferedWriter bw=new BufferedWriter(new FileWriter(path + "/README.md"));
                    bw.close();//一定要关闭文件
                } catch(IOException e){
                    e.printStackTrace();
                }
            }
        }
    }
}

```
