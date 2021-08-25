# images


```
public class Test {

    public static void main(String[] args) {
        LocalDate localDate = LocalDate.now();
        localDate = localDate.plusDays(128 + 365 + 365 + 366 + 365 + 365 + 366);
        for (int i = 0; i < 365; i++) {
            localDate = localDate.plusDays(1);
            DateTimeFormatter formatter = DateTimeFormatter.ofPattern("yyyy-MM-dd");
            String date = formatter.format(localDate);

            String path = "C:/Users/12976/git/images/2028/" + date;
            File dir = new File(path);
            if (!dir.exists()) {
                dir.mkdir();

                try {
                    BufferedWriter bw=new BufferedWriter(new FileWriter(path + "/README.md"));
                    bw.close();
                } catch(IOException e){
                    e.printStackTrace();
                }
            }
        }
    }
}

```
