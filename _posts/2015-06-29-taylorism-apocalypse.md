---
title: "Taylorism against Apocalypse"
reveal_theme: serif.css
reveal_transition: linear
---

# Taylorism against Apocalypse


Openstack meetup 2015-06-30

---

## What's Apocalypse?

End of civilisation, no more activity 

---

<p class="stretch">
![individual survival decline by number]({{ site.baseurl }}/assets/img/apocalysm/survieapocalypse1.png)
</p>

Individual survival regarding number of entities

--

<p class="stretch">
![global survival increase at a certain point]({{ site.baseurl }}/assets/img/apocalysm/survieapocalypse2.png)
</p>

Global survival regarding number of entities

--

<p class="stretch">
![Google is better than you]({{ site.baseurl }}/assets/img/apocalysm/survieapocalypse3.png)
</p>

--

<p class="stretch">
![keep calm and zerg rush]({{ site.baseurl }}/assets/img/apocalysm/zerg-rush.png)
</p>

---

## How to manage so many entities?

### How to be efficient with them?

---

<p class="stretch">
![Frederick Taylor]({{ site.baseurl }}/assets/img/apocalysm/taylor.jpg)
</p>

--

1. Replace rule-of-thumb work methods with methods based on a scientific study of the tasks.
2. Scientifically select, train, and develop each employee rather than passively leaving them to train themselves.
3. Provide "Detailed instruction and supervision of each worker in the performance of that worker's discrete task" (Montgomery 1997: 250).
4. Divide work nearly equally between managers and workers, so that the managers apply scientific management principles to planning the work and the workers actually perform the tasks.

---

## Applying to Automobile

--

<p class="stretch">
![Renault  C5 (1906)]({{ site.baseurl }}/assets/img/apocalysm/img-5.jpg)
</p>

Workshop Pre-Taylorism

--

<p class="stretch">
![Renault  C5 (1922)]({{ site.baseurl }}/assets/img/apocalysm/img-8.jpg)
</p>

Post-Taylorism operation

--

<p class="stretch">
![Renault  C5 instructions (1922)]({{ site.baseurl }}/assets/img/apocalysm/img-9.jpg)
</p>

Associated instructions

---

## Applying to Computing

--

### 1

* Replace rule-of-thumb work methods with methods based on a scientific study of the tasks.

Don't redo what you have done before.  
Scalability and automation need new way of thinking.

--

### 2

* Scientifically select, train, and develop each employee rather than passively leaving them to train themselves.

Measure and improve component by component.

--

### 3

* Provide "Detailed instruction and supervision of each worker in the performance of that worker's discrete task" (Montgomery 1997: 250).

In order to be able to replace any component, you must have tests.

--

### 4

* Divide work nearly equally between managers and workers, so that the managers apply scientific management principles to planning the work and the workers actually perform the tasks.

You should have orchestrators and dedicated services.

---

## Principles

--

### Believe in *Judgment Day*

It will happen to you

Never trust anyone, including your components and your cloud provider.

--

### Done is better than perfect

Always manage a way to go out for something better.

---

## Best practices

--

### Use and abuse of queuing.

Divide your workflow into simple tasks.

--

### Scale (hire) at will

You shouldn't worry about a bigger task at some point.  
Just hire some new workers.

--

### Stay focused on your business

To keep velocity, use external services.

Ex: LBaaS, Trove, **aaS

--

### Formalize interactions between components

Ex: RESTful API

--

### Manage life cycle in your application

* Versionnize API
* Manage data upgrade smoothly

--

### Rolling upgrade

--

### Immutable infrastructure

Try to mount `/` in `RO` and watch the world burn

--

### Chaos Monkey is quite fun

Chaos Kong even more!

--

### Never Never do something you can't test

Never Never Never

Did I say enough "Never"?

--

### Avoid remote management

No more SSH / VNC ...

--

### 12factor

Override configuration via environment variables

---

## Organization

--

### Try Devops

Put some ops in your dev team

--

<p class="stretch">
![prosper]({{ site.baseurl }}/assets/img/spock/spock.jpg)
</p>
