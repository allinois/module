# moduleПодключение к БД:
App.xaml.cs -> public static Model.DB_Name DB;

Создание подключения:
MainWindow.cs -> App.DB = new Model.DB_Name();

Обработчик отключения:
App.Current.Shutdown();

Отображение данных:
 <ListView >
     <ListView.View>
         <GridView>
             <GridViewColumn Header="1 значение" DisplayMemberBinding="{Binding Table_name.Stolbec_name}"/>
             <GridViewColumn Header="2 значение"/>
             <GridViewColumn Header="3 значение"/>
             <GridViewColumn Header="4 значение"/>
             
         </GridView>
     </ListView.View>
 </ListView>

Сортировка по категориям:
if (checkBoxSort.SelectedIndex > 0)
{
	case 1:
		Сортировка по убыванию
		request = request.OrderBy(x => x.request_data).ToList();
	case 2:
		Сортировка по возрастанию
		request = request.OrderByDescription(x => x.request_data).ToList();
}

Поиск по значению:
string Search = textBoxName.Text;
request = request.Whwrw( x => x.visitor.Visitor_name.Equals(Search)).ToList();






