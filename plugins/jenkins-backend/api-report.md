## API Report File for "@backstage/plugin-jenkins-backend"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { CatalogClient } from '@backstage/catalog-client';
import { Config } from '@backstage/config';
import { EntityName } from '@backstage/catalog-model';
import express from 'express';
import { Logger as Logger_2 } from 'winston';

// Warning: (ae-missing-release-tag) "createRouter" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export function createRouter(options: RouterOptions): Promise<express.Router>;

// Warning: (ae-missing-release-tag) "DefaultJenkinsInfoProvider" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public
export class DefaultJenkinsInfoProvider implements JenkinsInfoProvider {
  // (undocumented)
  static fromConfig(options: {
    config: Config;
    catalog: CatalogClient;
  }): DefaultJenkinsInfoProvider;
  // (undocumented)
  getInstance(opt: {
    entityRef: EntityName;
    jobFullName?: string;
  }): Promise<JenkinsInfo>;
  // (undocumented)
  static readonly NEW_JENKINS_ANNOTATION = 'jenkins.io/job-full-name';
  // (undocumented)
  static readonly OLD_JENKINS_ANNOTATION = 'jenkins.io/github-folder';
}

// Warning: (ae-missing-release-tag) "JenkinsInfo" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface JenkinsInfo {
  // (undocumented)
  baseUrl: string;
  // (undocumented)
  headers?: Record<string, string | string[]>;
  // (undocumented)
  jobFullName: string;
}

// Warning: (ae-missing-release-tag) "JenkinsInfoProvider" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface JenkinsInfoProvider {
  // (undocumented)
  getInstance(options: {
    entityRef: EntityName;
    jobFullName?: string;
  }): Promise<JenkinsInfo>;
}

// Warning: (ae-missing-release-tag) "RouterOptions" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface RouterOptions {
  // (undocumented)
  jenkinsInfoProvider: JenkinsInfoProvider;
  // (undocumented)
  logger: Logger_2;
}

// (No @packageDocumentation comment for this package)
```