DropEditText
============

like a spinner but can edit 

Ч����ʾ��

![image](https://github.com/qibin0506/DropEditText/blob/master/image/1.png)

![image](https://github.com/qibin0506/DropEditText/blob/master/image/2.png)

![image](https://github.com/qibin0506/DropEditText/blob/master/image/3.png)


ʹ�÷���:
�ڲ����ļ����ã�

<org.loader.view.DropEditText
	android:id="@+id/drop_edit"
	android:layout_width="200dip"
	android:layout_height="wrap_content"
	drop:drawableRight="@drawable/drop"
	drop:dropMode="flower_parent" />
		
<org.loader.view.DropEditText
	android:id="@+id/drop_edit2"
	android:layout_width="200dip"
	android:layout_height="wrap_content"
	drop:drawableRight="@drawable/drop"
	drop:dropMode="wrap_content"
	drop:hint="DropEditText" />

��Activity�У�
DropEditText drop1 = (DropEditText) findViewById(R.id.drop_edit);
		DropEditText drop2 = (DropEditText) findViewById(R.id.drop_edit2);
		
		drop1.setAdapter(new BaseAdapter() {
			private List<String> mList = new ArrayList<String>() {
				{
					add("����ѡ�� one");
					add("����ѡ�� two");
					add("����ѡ�� three");
					add("����ѡ�� four");
					add("����ѡ�� five");
					add("����ѡ�� six");
					add("����ѡ�� 7��ôƴ���ţ�");
				}
			};

			@Override
			public int getCount() {
				return mList.size();
			}

			@Override
			public Object getItem(int position) {
				return mList.get(position);
			}

			@Override
			public long getItemId(int position) {
				return position;
			}

			@Override
			public View getView(int position, View convertView, ViewGroup parent) {
				TextView tv = new TextView(MainActivity.this);
				tv.setText(mList.get(position));
				return tv;
			}
		});
		
		drop2.setAdapter(new BaseAdapter() {
			private List<String> mList = new ArrayList<String>() {
				{
					add("����ѡ�� one");
					add("����ѡ�� two");
					add("����ѡ�� three");
					add("����ѡ�� four");
					add("����ѡ�� five");
					add("����ѡ�� six");
					add("����ѡ�� 7��ôƴ���ţ�");
				}
			};

			@Override
			public int getCount() {
				return mList.size();
			}

			@Override
			public Object getItem(int position) {
				return mList.get(position);
			}

			@Override
			public long getItemId(int position) {
				return position;
			}

			@Override
			public View getView(int position, View convertView, ViewGroup parent) {
				TextView tv = new TextView(MainActivity.this);
				tv.setText(mList.get(position));
				return tv;
			}
		});