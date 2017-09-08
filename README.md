# 工科程式筆記

# System.IO

## Directory Class

幾個常用的方法
- `CreateDirectory(path)` : 在指定的path中建立資料夾。
- `Delete(path, recursive)` : 刪除path指定的資料夾。
- `Move(sourceDirName, destDirName)`: 將sourceDirName指定的**資料夾或檔案**移動到destDirName指定的位置。
- `Exists(path)`: 回傳path指定的資料夾是否存在，是就回傳true，否則回傳false。
- `GetCurrentDirectory()` : 取得應用程式的所在資料夾，回傳String。

---

`CreateDirectory(path)` : 在指定的path中建立資料夾。<br>
如下所示，將會在C:\User\david中創建test這個資料夾，**如果User、david資料夾也不存在，就會一併建立**。
```csharp
Directory.CreateDirectory(@"C:\User\david\test");
```

---

`Delete(path, recursive)` : 刪除path指定的資料夾。<br>
如下所示，將會刪除C:\User\david中的test這個資料夾。<br>
recursive則用來指定是否刪除其子資料夾與檔案，預設為false。
```csharp
Directory.Delete(@"C:\User\david\test");
```

---
`Move(sourceDirName, destDirName)` : 將sourceDirName指定的**資料夾或檔案**移動到destDirName指定的位置。
如下所示，移動test資料夾到C:\local下，且移動後的名稱改為newtest。
```csharp
Directory.Move(@"C:\User\david\test", @"C:\local\newtest");

Directory.Move(@"C:\User\david\test.txt", @"C:\local\newtest.txt");
```

---

`Exists(path)` : 回傳path指定的資料夾是否存在，是就回傳true，否則回傳false。<br>
如下所示，將為判斷C:\User\david\test是否存在，如果不存在的話就建立，可避免出錯。
```csharp
if(Directory.Exists(@"C:\User\david\test"))
    Directory.CreateDirectory(@"C:\User\david\test");
```

---

`GetCurrentDirectory()` : 取得應用程式的所在資料夾，回傳String。

---

