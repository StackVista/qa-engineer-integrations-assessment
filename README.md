# StackState QA Engineer Integrations Assessment

This is the StackState QA Engineer assessment. The assessment is intended to give us insight into your abilities, approach and general working habits. We view your performance on this assessment as indicative of the work you will deliver as a StackState QA Engineer.

The assessment consists of two assignments to prepare beforehand and a presentation about your implementation of the assignment at the StackState office or remotely.

*Please keep the subject of the assessment confidential so we can use it again in the future*. This means *don't* post it on a publicly accessible site such as github.com.

If you have any questions about the assessment, please contact us via email at **mvanvliet@stackstate.com**.


# Assignment 1: Agile testing

For this assignment, suppose you start a new job as a QA Engineer at a new company. This company builds and sells software products. It is your job to take ownership of the QA process for one of the products and ensure the quality of the delivered end product.

Here is a high level description of the software development process:

* there are 2 Scrum teams working on the product you are assigned to. Each sprint is 2 weeks long.
* prior to the sprint starting, the team has a planning meeting with the Product Owner (PO) to determine the scope of the sprint.
* the sprint finishes with a demo where the team shows the delivered user stories to the PO and other relevant stakeholders.
* after 4 sprints, all the work completed is bundled into a release and delivered to the company's customers.
* since there are no dedicated QA Engineers, the developers themselves now test the user stories before marking them as done.
* in the last sprint before creating a release, both Scrum teams have a "hardening" sprint in which they test the software and fix any bugs they might find.

Within each sprint, the engineers follow the following process:

* the Scrum board for the team has columns To Do, In Progress, Testing, Done
* stories are picked up from the To Do column and moved to the In Progress column
* engineers implement the stories, sometimes individually, sometimes as a pair
* finished stories are moved to the Testing column
* stories in the Testing column are reviewed by other engineers
* after the review, the stories are moved to Done

As the single QA Engineer for this product, how would you ensure quality in the final product? What activities would you do at which points in the development process?

Please cover the following in your answer:

* how would you work with your team members in the activities they do in the sprint?
* how would you want to be involved in the different phases of the Scrum process to ensure quality?
* how would you optimise the release cycle, including the "hardening" sprint?


# Assignment 2: Test tooling

In this assignment, you will be testing a part of the StackState platform, the agent. The agent's job is to collect data from an external system or host and send this to StackState so it can be integrated into the IT landscape map. The agent can be configured to collect certain types of information via it's configuration file.

For this assignment you will need to be running docker on your laptop.

Start by cloning the QA Engineer assessment [github repo](https://github.com/StackVista/qa-engineer-integrations-assessment).

The repo contains a script to run the agent docker container, as well as configuration files for the agent. Before running the example, you need to configure the sample project with your StackState instance URL and API key. The StackState instance URL can point to your local laptop, you can use a dummy API key.

Use these commands to run the agent:

```
export STS_API_KEY=my-api-key
export STS_STS_URL=http://host.docker.internal:8000/stsAgent
./run.sh
```

This command runs the StackState agent in a docker container, sending it's output to a port on your local laptop.

You can capture the traffic produced by the agent by installing a capturing proxy in the middle, for example [HTTP Proxy](https://httptoolkit.tech/):

![HTTP Toolkit example](http-proxy-example.png)

## Testing

Your assignment is to test the following features of the StackState agent:

* the ability to specify host tags
* the ability to filter out detected processes via the process blacklist

Obviously, automate the tests as much as possible.

## Documentation

The agent documentation can be found on the [StackState docs site](https://docs.stackstate.com/stackpacks/integrations/agent).

# Presentation

The assessment presentation will be done either in person in the StackState office or remotely. You are free to deliver your presentation in any form but we expect you to cover both assignments described above.

Here are some special considerations for the assessment presentation.

**StackState office**

* If you are using a presentation, either bring a USB key with the presentation on it or a laptop to show the presentation.
* There will be a projector present at the office. Please bring the necessary cables.

**Remote**

* We will use **Zoom** for screen sharing and audio.
* In case of problems, have **Google Hangouts** setup as a backup. Please test this before the assessment.


Good luck with the assignment!
