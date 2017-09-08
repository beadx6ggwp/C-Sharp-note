# 工科程式筆記

# System.IO

## `Directory Class`

CreateDirectory(path) : 在指定的path中建立資料夾。<br>
如下所示，將會在C:\User\david中創建test這個資料夾，**如果User、david也不存在，就會一併建立**。
```csharp
Directory.CreateDirectory(@"C:\User\david\test");
```

Delete(path, recursive) : 刪除path指定的資料夾。<br>
如下所示，將會刪除C:\User\david中的test這個資料夾。<br>
recursive則用來指定是否刪除其子資料夾與檔案，預設為false。
```csharp
Directory.Delete(@"C:\User\david\test");
```

Exists(path) : 回傳path指定的資料夾是否存在，是就回傳true，否則回傳false，如下所示，