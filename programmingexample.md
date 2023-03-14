# Programming Examples
[Main](README.md) | [About](about.md) | [Key Competencies](keycompetencies.md) | **Programming Examples** | [Education](education.md) | [Experience](experience.md)

The following are a few early examples of programming code based on early assignments.  

## Programming Languages

- Python
  - [Volume Calculator](#volume-calculator)
  - [Scholarship Calculator](#scholarship-calculator)
- Java Script
  - [FizzBuzz](#fizz-buzz)

### Volume Calculator

The following Python program requests user input to determine the volume of the requested shape. 

```
#Define Variables
pi = 3.141592653
    
#Define Functions
def volume_cone():
    """
    Calculate the volume of a cone
    """
    cone_radius = float(input("Enter the cone's radius: "))
    cone_height = float(input("Enter the cone's height: "))
    
    result = pi * cone_radius * cone_radius * (cone_height / 3)
    return result

def volume_cube():
    """
    Calculate the volume of a cube
    """
    cube_length = float(input("Enter the cube length: "))
    
    result = cube_length * cube_length * cube_length
    return result

def volume_cyl():
    """
    Calculate the volume of a cylinder
    """
    cyl_radius = float(input("Enter the cylinder's radius: "))
    cyl_height = float(input("Enter the cylinder's height: "))
    
    result = pi * (cyl_radius * cyl_radius) * cyl_height
    return result 

#Provide User Menu Options    
print("1. Calculate volume of a cone.")
print("2. Calculate volume of a cube.")
print("3. Calculate volumne of a cylinder.\n")

#Request User Input
user_input = int(input("Choose 1, 2, 3: "))

#Process User Input
if (user_input == 1):
    cone_volume = volume_cone()
    print(f'The volume of the cone is {cone_volume:.2f}.')

elif (user_input == 2):
    cube_volume = volume_cube()
    print(f'The volume of the cube is {cube_volume:.2f}.')

elif (user_input == 3):
    cyl_volume = volume_cyl()
    print(f'The volume of the cylinder is {cyl_volume:.2f}.')

else:
    print("Invalid user input. Goodbye")
    exit()

```

### Scholarship Calculator

```
"""
This program assists students in estimating scholarship eligiblity.
The user inputs their current HS GPA and ACT score.
The program uses the input to display to the user which award they qualify for.
"""
#create scholarship lists
scsp = ["Academic Excellence", "Star Student", "Achievement"]
scsp_amt = ["$5,000", "$3,500", "$2,000"]
scsp_GPA = [3.75, 3.25, 3.0]
scsp_ACT = [31, 28, 25]

#Display eligiblity information to user
print(f'The University has {len(scsp)} scholarships available to incoming students.')
print(f'The minimum award amount a student may be eligible for is {min(scsp_amt)}.')
print(f'The maximum award amount a student may be eligible for is {max(scsp_amt)}. \n')

print(f'The {scsp[0]} Scholarship ({scsp_amt[0]}) requires a {scsp_GPA[0]} HS GPA or a {scsp_ACT[0]} ACT score.')
print(f'The {scsp[1]} Scholarship ({scsp_amt[1]})requires a {scsp_GPA[1]} HS GPA or a {scsp_ACT[1]} ACT score.')
print(f'The {scsp[2]} Scholarship ({scsp_amt[2]})requires a {scsp_GPA[2]} HS GPA or a {scsp_ACT[2]} ACT score.')
print(f'You can only qualify for the highest value award.\n')

print("Let's determine what award you may be eligible for! \n")

#user inputs GPA and ACT Score
hs_gpa = float(input("Enter High School GPA: "))
act_score = int(input("Enter ACT Score: "))
                
#Determine award
if hs_gpa <= 4.0 and hs_gpa >= 0 and act_score <= 35 and act_score >= 0:
    if hs_gpa >= scsp_GPA[0] or act_score >= scsp_ACT[0]:
        print(f'Based on your {hs_gpa} GPA and {act_score} ACT score, you are eligible for the {scsp[0]} Scholarship.')
    elif hs_gpa >= scsp_GPA[1] or act_score >= scsp_ACT[1]:
        print(f'Based on your {hs_gpa} GPA and {act_score} ACT score, you are eligible for the {scsp[1]} Scholarship.')
    elif hs_gpa >= scsp_GPA[2] or act_score >= scsp_ACT[2]:
        print(f'Based on your {hs_gpa} GPA and {act_score} ACT score, you are eligible for the {scsp[2]} Scholarship.')
    else:
        print(f'Based on your {hs_gpa} GPA and {act_score} ACT score, you are not eligible for a scholarship.')
else:
    print("Invalid GPA or ACT Score")


```

### Fizz Buzz

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Fizz Buzz</title>
<script>

function fizzbuzz() {
	var display = document.getElementById('display');
	var displayHTML = "";
	for (i = 1; i <= 100; i++) {
		if (i % 3 === 0 && i % 5 === 0) {
			displayHTML += "<p>" + "FizzBuzz" + "</p>";
		} else if (i % 3 === 0) {
			displayHTML += "<p>" + "Fizz" + "</p>";
		} else if (i % 5 === 0) {
			displayHTML += "<p>" + "Buzz" + "</p>";
		} else {
		displayHTML += "<p>" + i + "</p>";}
	}
	display.innerHTML = displayHTML
}

</script>

</head>

<body onload="fizzbuzz()">
<div id="display">

</div>
</body>

</html>
```
