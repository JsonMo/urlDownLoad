# urlDownLoad
根据一个图片的网址，将改图片存储到本地数据库中

   URL url1=new URL("要下载的图片的原网址");
   InputStream inputStream=url1.openStream();//转换成流
   String extension=jiegoushi.substring(jiegoushi.lastIndexOf(".")+1);//获取后缀名
   a = fastDFSClient.uploadFile(inputStream,extension);
   
   
   public String uploadFile(InputStream stream, String extension) throws IOException{

        StorePath storePath=storageClient.uploadFile(stream,stream.available(),extension,null);

        return getResAccessUrl(storePath);
    }
   
   
   
   
   

