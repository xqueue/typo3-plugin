# Typo3 - Maileon Integration Package

## Minimal Dependencies

* TYPO3 CMS 12.4.x or 13.4.x for Typo3 - Maileon Integration Package 3.2.x
* TYPO3 CMS 11.5.0 or 12.4.99 for Typo3 - Maileon Integration Package 3.1.x
* TYPO3 CMS 10.4 or 11.4.99 for Typo3 - Maileon Integration Package 3.x
* TYPO3 CMS 9.5 or 10.4 for Typo3 - Maileon Integration Package 2.5.x
* TYPO3 CMS 8.7 or 9.5 for Typo3 - Maileon Integration Package 2.4.x
* TYPO3 CMS 7.6 for Typo3 - Maileon Integration Package 1.0.x

## Workflow (settings in TYPO3 and Maileon are necessary)

* **TYPO3:** Install plugin
* **TYPO3:** Include static template "Configuration for Typo 3 - Maileon integration (typo3_maileon_integration)" (typoscript)
* **TYPO3:** Configure constants (see below)
* **Maileon:** Configure the three pages (Einstellungen => Seitenverwaltung). Append "&ci=[CONTACT|ID]&cs=[CONTACT|CHECKSUM]" for activation and unsubscription
* **Maileon:** Set the pages for DOI (Double Opt-In: Bestätigungsseite und Fehlerseite)
* **Maileon:** Set the page for unsubscription (Grundeinstellungen: "Standard-Abmeldeseite")
* **Maileon:** Create a DOI-Mailing (pages for DOI must exist) und activate it (Einstellungen => DOI-Mailing)
* **Maileon:** Create API-Key with all permissions (Einstellungen => API-Keys)
* **TYPO3:** Insert new "General Plugin" element and select "Subscription form" in "Plugin" tab
* **TYPO3:** Optional: style form with css
* **TYPO3:** Configure constants


### Example constants configuration

```
plugin.tx_typo3maileonintegration {
	settings {
		apiKey = XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
		doiMailingKey = AbCD1EFg
		debug = 0
		targetPermission = 5
	}
}
```

## Documentation

* [User Documentation](https://xqueue.atlassian.net/wiki/spaces/MSI/pages/2399174657/Typo3)
