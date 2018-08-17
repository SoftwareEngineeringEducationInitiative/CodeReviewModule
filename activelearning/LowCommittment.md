# Overview

One approach to introducing code review in the classroom is to show snippets of code and ask students to pair together to identify defects with it. The pairs must write a concise description of the defect. The instructor will ask for groups to share their answers. Instructors are encouraged to act as a moderator and encourage discussion about the code and the group's contribution. This activity can be done entirely in class with no preparation needed by the students. 

Some examples are shown below. It should be relatively easy for an instructor to create examples like these. Just think back to mistakes you have made in the past and make them an example.


# Code Examples to Be Shown in Class

## Example 1

```
string p[] = {"George Washington", "Abe Lincoln", "Herbert Hoover"};
```

**Problems:**

- poorly named variable

## Example 2

```
string presidents[] = {"George Washington", "Abe Lincoln", "Herbert Hoover"};
for(int i = 0;i < 3;i++)
{
	//create a copy of the string
	string* p_copy = new string(presidents[i]);
	
	//find where the first and last name are separated
	int pos = p_copy->find(" ");
	
	//print the first name, a comma, and then the last name
	cout<<p_copy->substr(pos);
	cout<<", ";
	cout<<p_copy->substr(0, pos);
}

```

**Problems:**

- memory leak on each copy, dynamic memory not even needed- a local variable would have been fine
- find returns a size_t not an int (which is an unsigned int)
- subtr is capturing the space as part of the last name
- should we check that a space is actually found??
- bad comment when printing the name- should be last, a comma, then first name

## Example 3

```
char acceptableCharacters[] = {'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', '@', '.', '-'}

string testEmail = "mark@mail.com";

for(int i = 0;i < testEmail.length();i++)
{
	for(int j = 0;j < 28;j++)
	{
		if(testEmail[i] != acceptableCharacters[j])
		{
			cout<<"Invalid email address"<<endl;
		}
	}
}
```

**Problems:**

- incorrect loop condition- there are 29 elements in the array the loop only checks 28
- problem with the algorithm- just because the if evaluates to true doesn't mean that we have an invalid email. 
