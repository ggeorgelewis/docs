.. _targeting-configuration:

#######################
Targeting Configuration
#######################

The targeting configuration file configures the targeting system of Crafter Studio to help provide Crafter Engine with fake user properties that help drive the targeting system.
To modify the targeting configuration, click on |siteConfig| from the bottom of the *Sidebar*, then click on **Configuration** and select **Targeting Configuration** from the dropdown list.

.. image:: /_static/images/site-admin/config-open-targeting-config.png
    :alt: Configurations - Open Targeting Configuration
    :width: 65 %
    :align: center

******
Sample
******

.. code-block:: xml
    :caption: {REPOSITORY_ROOT}/sites/SITENAME/config/studio/targeting/targeting-config.xml
    :linenos:

    <?xml version="1.0" encoding="UTF-8"?>
    <!-- targeting-config.xml

        This file configures the targeting system of Crafter Studio to help provide
        Crafter Engine with fake user properties that help drive the targeting system.

        Pages, components, search, services and more can respond differently depending
        on the user properties, and content delivery can be very personalized based
        on user properties. In order to test and validate the experience, this file can
        help set these properties as KVP (key-value-pairs) that are then injected into
        the Crafter Engine's session and are made accessible using the Profile APIs.

        You can learn more about personalization and targeting here:
        http://docs.craftercms.org/en/3.0/developers/targeting.html

    <property>
        <name />
        <label />
        <description />
        <type />
        <hint />
    </property>

    Please note that valid types are limited to: dropdown, checkboxes, input.
    -->
    <targeting>

        <property>
            <name>segment</name>
            <label>Segment</label>
            <description>User segment.</description>
            <type>dropdown</type> <!-- valid types: dropdown, checkboxes, input -->
            <possible_values>
                <value>guy</value>
                <value>gal</value>
                <value></value>
            </possible_values>
            <default_value></default_value>
            <hint>Setting the segment will change content targeting to the audience selected.</hint>
        </property>

        <property>
            <name>name</name>
            <label>Name</label>
            <description>User's first and last name.</description>
            <type>input</type> <!-- valid types: dropdown, checkboxes, input -->
            <default_value>Joe Bloggs</default_value>
            <hint>Enter user's first and last name.</hint>
        </property>
    </targeting>
