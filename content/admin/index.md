---
title: Enterprise Administrators
redirect_from:
  - /enterprise/admin/hidden/migrating-from-github-fi/
  - /enterprise/admin
intro: Documentation and guides for enterprise administrators, system administrators, and security specialists who {% if enterpriseServerVersions contains currentVersion %}deploy, {% endif %}configure{% if enterpriseServerVersions contains currentVersion %},{% endif %} and manage {% data variables.product.product_name %}.
versions:
  enterprise-server: '*'
  github-ae: '*'
---

{% link_with_intro /overview %}

{% link_with_intro /installation %}

{% link_with_intro /configuration %}

{% link_with_intro /authentication %}

{% link_with_intro /user-management %}

{% link_with_intro /policies %}

{% link_with_intro /enterprise-management %}

{% link_with_intro /github-actions %}

{% link_with_intro /packages %}

{% link_with_intro /enterprise-support %}

{% link_with_intro /release-notes %}
<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
                      http://maven.apache.org/xsd/settings-1.0.0.xsd">

  <activeProfiles>
    <activeProfile>github</activeProfile>
  </activeProfiles>

  <profiles>
    <profile>
      <id>github</id>
      <repositories>
        <repository>
          <id>central</id>
          <url>https://repo1.maven.org/maven2</url>
        </repository>
        <repository>
          <id>github</id>
          <url>https://maven.pkg.github.com/OWNER/*</url>
          <snapshots>
            <enabled>true</enabled>
          </snapshots>
        </repository>
      </repositories>
    </profile>
  </profiles>

  <servers>
    <server>
      <id>github</id>
      <username>USERNAME</username>
      <password>TOKEN</password>
    </server>
  </servers>
</settings>

