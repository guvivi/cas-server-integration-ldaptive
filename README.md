# LDAP Integration for Jasig CAS Using ldaptive

## Introduction

The cas-server-integration-ldaptive library is an extension for Jasig CAS that provides LDAP integration using the
[ldaptive](http://www.ldaptive.org/) LDAP library for Java. The following CAS integration components are provided:
provided at present:

* LdapAuthenticationHandler - provides capabilities found in both FastBindAuthenticationHandler and
  BindAuthenticationHandler components.
* LdapCredentialsToPrincipalResolver - resolves principals via LDAP search.
* LdapUserDetailsService - Spring Security user details implementation.
* ConnectionFactoryMonitor - LDAP single connection monitor.
* PooledConnectionFactoryMonitor - LDAP connection pool monitor.

## Dependencies

This project requires CAS 3.5.0 or later, latest ldaptive snapshot, Spring Security and slf4j.
See the pom.xml for detailed dependency information.

## Building

mvn -DskipTests clean package

Additional configuration is required to build the software with unit tests enabled.  The *.samples files provides
templates for creating environment-specific files with data and configuration needed to execute tests.
