using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.IO;

namespace Kids2ProSports
{
    public partial class UploadFiles : System.Web.UI.Page
    {
        protected void Page_Load(object sender, EventArgs e)
        {
            if (!Page.IsPostBack)
            {
                // file uploaded and destination folder from Uploadify
               
            }
        }
        public void ProcessRequest(HttpContext context)
        {

            var fileData = Request.Files[0];
            var foldername = Request["folder"];
            // builds destination folder path
            var root = Server.MapPath("/");
            var folderpath = Path.Combine(root, "");
            // creates destination folder 
            if (!Directory.Exists(folderpath))
            {
                Directory.CreateDirectory(folderpath);
            }
            // saves file
            var fileName = Path.GetFileName(fileData.FileName);
            var fileSavePath = folderpath + "/" + fileName;
            fileData.SaveAs(fileSavePath);

                //HttpPostedFile file = context.Request.Files("Filedata");
                //string filename = file.FileName;
                //string filepath = HttpContext.Current.Server.MapPath("~").ToString() + "\\Uploads\\" + filename;
                //file.SaveAs(filepath);
           
        }
    }
}