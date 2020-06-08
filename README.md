# prueba
Imports MySql.Data.MySqlClient

Module Conex
    Public con As MySqlConnection
    Public Sub connexion_mysql()
        con = New MySqlConnection
        con.ConnectionString = "server=localhost;" & "user id= root;" & "password= 12346789;" & "database = proveedor;"
        Try
            con.Open()
            MsgBox("Conexión Abierta con Éxito")
            con.Close()
        Catch mierror As MySqlException
            MsgBox("Error de Conexión a la base de datos:" & mierror.Message)
            End
        Finally
            con.Dispose()
        End Try
    End Sub
End Module
