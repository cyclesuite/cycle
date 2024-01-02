# Contributing
Check out our guide below for more information on how to contribute to our project.

* [Types](#types)
	* [Code](#code)
	* [Vulnerabilities](#vulnerabilities)
	* [Documentation](#documentation)
* [Releasing Changes](#releasing-changes)
* [Roadmap](#roadmap)

## Types
Please see the categories below for information on contributing to the specific categories.

### Code
We welcome code contributions for features and bugs that have been placed in our roadmap. We want to make sure no one wastes their time, so please talk to maintainers before contributing to understand what would be accepted.

> See [roadmap](#roadmap) for more information.

<!--
	You should not edit this portion unless
	given explicit permission by a maintainer.
-->

### Vulnerabilities
If you find a vulnerability, we ask that you contact us with information reguarding the vulnerability. Such information shall answer:

* How was the vulnerability was discovered?
* What is the potentional impact of the vulnerability?
* How can the vulnerability can be exploited?

If you think you can solve a vulnerability, please follow the guidelines located below.

* While testing, take measures to avoid affecting other users' experiences. If possible, you should test in your own experience.
* Please keep testing on an alternate account, generally, this account should be disclosed to us beforehand.
* Take measures to avoid disclosing vulnerabilities to others without explicitly receiving permission from a maintainer before a fix has been released. Whenever possible, we will disclose the vulnerability, solution, and contributors, once fixed.
* If you are aware that your testing may harm the reliability or integrity of our services, stop immediately and contact us.
* Do not attempt non-technical testing, such as social engineering our employees or users.

> *These instructions can also be found in our [security policy](https://github.com/cyclesuite/.github/security/policy). You should visit such to learn more.*

### Documentation
Documentation has much more of an impact than just lines of code. If you find any problem in our documentation, such as typos, bad grammar, misleading phrasing, or missing content, feel free to file issues and pull requests to fix them.

## Releasing Changes
At the moment, the process of releasing a version is manual. Please follow the steps below.

1. Update [`metadata`](metadata/contributors.json) accordingly.
	* It should be noted that we enforce two character space formatting in our `JSON` files.
	- If you'd like, you can add yourself to our contributor list. When editing, do not remove anyone from the list.
	- You should make an entry into the object with your **GitHub user identifier coming first, and your Roblox user identifier coming second.**
		- You can get your GitHub user identifier from `https://api.github.com/users/YOUR_NAME_HERE`.

	- Once you are done, it should look something like this:
	```json
	{
	  "GITHUB_USER_ID": "ROBLOX_USER_ID"
	}
	```
	```json
	{
	  "100449899": "560637180"
	}
	```

2. Run `aftman install && selene ./src` to receive any formatting that may need changed. This isn't absolutely necessary, as it will be done automatically once a pull request is opened, but this may speed things up.
	- Make sure you have [Aftman](https://github.com/LPGhatguy/aftman) installed.
3. Run `git add . && git commit -m 'Message'`
	- Make sure you have [Git](https://git-scm.com/) installed.
4. Run `git tag VERSION` an example of this is, `git tag 0.0.1`, this will provide a checkpoint to go back on.
5. Run `git push && git push --tags` to push the commit to the repository.

### What do we do with the metadata?
The metadata is used to provide interface information. Your Roblox user identifier is used to get your avatar. We will add your avatar & username to our global contributors list.

## Roadmap
While we like adding things that people enjoy, we ask that you only add features that are already approved in our roadmap. In most cases, our own developers will add these features, since they may need to be implemented in a certain way. This is why it's important to contact a maintainer before adding a **significant** feature.

It's alright to fix a bug report or add a small feature that is not in the roadmap. In cases that you are adding a small feature, you should create an issue or talk with the community to ensure that it is the best choice - maintainers are busy, so this may cut down on the amount of time it takes to implement.

## Attributions
* Adapted from [Rojo](https://github.com/rojo-rbx/rojo/blob/master/CONTRIBUTING.md)
* Adapted from [Roblox](https://hackerone.com/roblox)