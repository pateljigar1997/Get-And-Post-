# Get-And-Post-
HttpClient.Post &amp; HttpClient.Get 
-----------Example--------------
 public IActionResult CategoryFilterSearch(ClientCommonModel<Category> model,int page=1,int pageSize=10)
{
        ClientCommonModel<Category> obj = new ClientCommonModel<Category>();
        HttpClient client = _api.Intial();
        var postTask = client.PostAsJsonAsync("Home/CategoryFilterSearch?pageSize="+pageSize+"&page="+page,model);
        postTask.Wait();
}
