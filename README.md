# C# DB 접속

SqlConnection dbConection()
        {
            string strDataBase = "TEST_DB";          //Database
            string strIP = "127.0.0.1";         //Ip
            string strPort = "1433";            //Port
            string strID = "nodedb";              //ID
            string strPW = "1234567890";				//PW
            
            try
            {
                SqlConnection sqlConnection = new SqlConnection();
                // DB 접속 정보
                string constring = "server=" + strIP +
                        "," + strPort +
                        ";database=" + strDataBase +
                        ";uid=" + strID +
                        ";pwd=" + strPW;
                // 접속정보를 적용
                sqlConnection.ConnectionString = constring;
                // DB연결
                sqlConnection.Open();
                return sqlConnection;
            }
            catch (Exception error)
            {
                return null;
            }
        }
