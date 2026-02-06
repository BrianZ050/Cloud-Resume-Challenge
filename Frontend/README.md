# Frontend Technical Specification

- Create a static website that serves an html resume. 

## Resume Format Considerations

I live in the United States and resumes in word/pdf format are suppose to exclude information. eg. Age, Relationship. United States resume don't often include GPA grades. 

I'm going to use the [Harvard Resume Template format](https://careerservices.fas.harvard.edu/resources/bullet-point-resume-template/) as the basis of my resume. 

## Harvard Resume Format Generation

I know HTML quite well, so I'm going to let GenAI do the heavy lifting and generate out HTML and possible CSS and from there I will manually refactor the code to preferred standard. 

Prompt to Gemini 3:

``` text
Convert this resume format into HTML.
Please don't use a css framework.
Please use the least amount of css tags. 
```

Image provided to LLM:
![](./docs/harvard-resume-template.png)

This is the [gernated output](./docs/feb-5-2026-resume-minimal.html) which I will tweak.

This is what the generated HTML looks like unaltered: 

![](./docs/reume-minimal-rendered.png)

## HTML Adjustments

- UTF8 will support most languauges, I plan to use English so I'll leave this meta tag in. 
- Because I will be applying mobile styling to my website, I'll include the viewport meta tag width=device-width so mobile styling scales normally. 
- I'll extract out styles into its own stylesheet after I am happy with my HTML markup.
- I'll simplify my HTML makeup css selector to be as minimal as possible. 
- For the HTML page I'll use soft tabs 4 spaces because I am currently learning Python in my cs courses and that's the standard tab format. 