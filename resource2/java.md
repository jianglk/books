### 以下是常用的代码收集，没有任何技术含量，只是填坑的积累。转载请注明出处，谢谢。
*java中的验证
`/**
     *  
     * @param  str
     * @return 验证通过返回true
     */  
 public static boolean isMobile(String str) {  
        Pattern p = null;  
        Matcher m = null;  
        boolean b = false;  
        p = Pattern.compile("^[0-9]*$"); // 验证数字   
        m = p.matcher(str);  
        b = m.matches();  
        return b;  
    }`
    
*java json 数组的转换
`List<PageData> list=new ArrayList<PageData>();
JSONArray array = JSONArray.fromObject(str);
  for (int i = 0; i < array.size(); i++) {  
            JSONObject object = (JSONObject)array.get(i);  
            PageData pd = (PageData) JSONObject.toBean(object,PageData.class);
            list.add(pd);
  }`
