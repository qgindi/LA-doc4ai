# Class `Au.Types.TreeBase<T>`

Base class for tree classes. The tree can be loaded/saved as XML.

```
public abstract class TreeBase<T> where T : TreeBase<T>
```

##### Type Parameters

| Name | Description |
| --- | --- |
| T |  |

##### Remarks

Implemented in the same way as `System.Xml.Linq.XContainer`.

##### Examples

Shows how to declare a `TreeBase`-derived class, load tree of nodes from an XML file, find descendant nodes, save the tree to an XML file.

```
using System.Xml;

class MyTree : TreeBase<MyTree> {
	public string Name { get; set; }
	public int Id { get; private set; }
	public bool IsFolder { get; private set; }

	public MyTree(string name, int id, bool isFolder) { Name = name; Id = id; IsFolder = isFolder; }

	//XML element -> MyTree object
	MyTree(XmlReader x, MyTree parent)
	{
		if(parent == null) { //the root XML element
			if(x.Name != "example") throw new ArgumentException("XML root element must be 'example'");
			IsFolder = true;
		} else {
			switch(x.Name) {
			case "e": break;
			case "f": IsFolder = true; break;
			default: throw new ArgumentException("XML element must be 'e' or 'f'");
			}
#if true //two ways of reading attributes
			Name = x["name"];
			Id = x["id"].ToInt();
#else
			while(x.MoveToNextAttribute()) {
				var v = x.Value;
				switch(x.Name) {
				case "name": Name = v; break;
				case "id": Id = v.ToInt(); break;
				}
			}
#endif
			if(Name.NE()) throw new ArgumentException("no 'name' attribute in XML");
			if(Id == 0) throw new ArgumentException("no 'id' attribute in XML");
		}
	}

	public static MyTree Load(string file) => XmlLoad(file, (x, p) => new MyTree(x, p));

	public void Save(string file) => XmlSave(file, (x, n) => n._XmlWrite(x));

	//MyTree object -> XML element
	void _XmlWrite(XmlWriter x)
	{
		if(Parent == null) {
			x.WriteStartElement("example");
		} else {
			x.WriteStartElement(IsFolder ? "f" : "e");
			x.WriteAttributeString("name", Name);
			x.WriteAttributeString("id", Id.ToString());
		}
	}

	public override string ToString() => $"{new string(' ', Level)}{(IsFolder ? 'f' : 'e')} {Name} ({Id})";
}

static void TNodeExample() {
	/*
	<example>
	  <e name="one" id="1" />
	  <f name="two" id="112">
		<e name="three" id="113" />
		<e name="four" id="114" />
		<f name="five" id="120">
		  <e name="six" id="121" />
		  <e name="seven" id="122" />
		</f>
	  </f>
	  <f name="eight" id="217" />
	  <e name="ten" id="144" />
	</example>
	*/

	var x = MyTree.Load(@"C:\test\example.xml");
	foreach(MyTree n in x.Descendants(true)) print.it(n);
	//print.it(x.Descendants().FirstOrDefault(k => k.Name == "seven")); //find a descendant
	//print.it(x.Descendants().Where(k => k.Level > 2)); //find some descendants
	x.Save(@"C:\test\example2.xml");
}
```

##### Inheritance

`object` → `TreeBase<T>`

Derived: `Au.More.FileTree`

### Properties

`Count`, `FirstChild`, `HasChildren`, `HasParent`, `Index`, `LastChild`, `Level`, `Next`, `Parent`, `Previous`, `RootAncestor`

### Methods

`AddChild`, `AddSibling`, `Ancestors`, `AncestorsFromRoot`, `Children`, `Descendants`, `IsAncestorOf`, `IsDescendantOf`, `IsDescendantOf`, `Remove`, `XmlLoad`, `XmlLoad`, `XmlSave`, `XmlSave`