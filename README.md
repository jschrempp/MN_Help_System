# MN_Help_System
## Overview.
This repository contains information that describes the Help Button System that is installed at Maker Nexus.  The Help
Button System leverages LoRa and Particle.io technology to allow members to call for assistance from staff without
the member losing sight of their in-process work.  The main document to read is the "MN_Help_System_Technical_Desicption_Document"
that is located in the "Documents" folder of this repository.

Maker Nexus is a 501(c)(3) non-profit makerspace located in Sunnyvale CA.  Maker Nexus is housed in a 28,000 square foot
facility that is sectioned off into various shop areas to prevent the spread of fire and dust.

Maker Nexus has two policies that are important to the Help Button System:
1. A designated staff member (called the MOD) must be present and on-duty in the facility whenever it is open to members.
2. Members should always be in sight of their project whenever they are using power tools.

A member who needs assistance must have a way to summon the MOD from their work location regardless of where the MOD is
at that moment.  The MOD might very well be out of sight of the member.  The purpose of the Help Button System is to provide
a way for members to summon the MOD to their work location without the member losing sight of their work and regardless of where
in the facility the MOD is at that time.

Battery operated wireless "Help Buttons" are placed throughout the Maker Nexus facility.  Help Buttons are located within the
line of sight of any work location within the facility.  Help Buttons are programmed (via jumpers) to identify specific locations
within Maker Nexus, e.g. "woodshop".  When a member presses a Help Button, a wireless LoRa message is sent to a central Hub.  LoRa technology
allows messages to get through to the Hub across firewalls and other barriers within the large facility.  The LoRa message contains
a location code for the Help Button. Because the Help Buttons are battery powered, they can easily be placed anywhere in the facility.

The Hub receives LoRa messages from Help Buttons.  Software in the Hub validates and replies to the Help Button messages.  The Hub publishes
this information to the Particle Cloud.  "Annunciator" devices within the Maker Nexus facility use Particle.io technology to subscribe
to Hub-published events.  Annunciators are placed throughout Maker Nexus so that audible announcements that are played through 
intenal loudspeakers can be heard anywhere within the facility.  The MOD can then respond to the member's request for assistance
by going to the announced location.

Additional capabilities of the Help Button System include:
1. An Android app that simulates Help Button messages to the Hub and allows an MOD to play pre-recorded administrative messages on the Annunciators.
2. An "Event Timer" that automates playing of certain administrative messages through the Annunciators at specific times of the day.

## Technologies.
The Maker Nexus Help Button System leverages key technologies that are useful for other projects:

1.  LoRa technology provides low power, very long range communication of short messages.  Help Buttons are adapted from LoRa-based,
battery operated sensors that we have developed for use on multiple projects.

2. Particle technology, including cloud based publish and subscribe, webhooks, and Particle's REST API.  The Help Button System
uses many aspects of Particle technology that we have previously employed on many other projects.

The "MN_Help_System_Technical_Description_Document" in the "Documents" folder provides references to GitHub repositories that 
contain open source technical details of these technologies.

## Contents of this Repository.
The "Documents" folder contains a technical description of the Help Button System, see: https://github.com/TeamPracticalProjects/MN_Help_System/blob/main/Documents/MN_Help_System_Technical_Description_Document.pdf.

This folder also contains a document describing how to configure a Help Button for deployment within Maker Nexus:  https://github.com/TeamPracticalProjects/MN_Help_System/blob/main/Documents/Configuring%20a%20Help%20Button%20for%20MN.pdf

The technical description document provides references to other repositories that contain detailed technical information about Help
Buttons, Hubs and Annunciators including technical documents, source code, electronic and mechancial CAD files, and other information.

