

class BoxComponent {
  a:string:=""
  @Input() b:string=""
  constructor(){}
  ngOnInit(){}
}
Whenever a component is created? <app-box [b]="temp"><app-box>

    1. The instance variables are loaded for the instance
	        [it is one time activitiy]
	2. Constructor executes
	        [it is one time activitty]
			at this point input type would not
			be received from parent
	3. Input Variables will be received from parent
	
	Now the component is said to be initialized
	
Yet the template would not be ready

 template is combination of parent content
 and child template
 
  appbox.html
  
  <h1>Hey</h1>
  <h3>do This </h3>
  
  <app-sample><app-sample>
  
  here, 
    <h1>Hey</h1>
  <h3>do This </h3>
  is the current component content
  
  where as,
  
    <app-sample><app-sample>
	is the child it has its own template
	need to undergo lifecycle
	
Content
  The current component template alone is called content

View

if the child component template is 
rendered and merged with parent component
template it is called view

If view is ready , it will be rendered on the
screen

upon update on any state in the component
the component will be re rendered
that is 
content and templated will be regenerated
[update of the component]


if the component is removed from the container
the component is destroyed

	
The functions which we run at any phase of the 
life cycle of a component is called as 
life cycle hook

https://v2.angular.io/resources/images/devguide/lifecycle-hooks/hooks-in-sequence.png

