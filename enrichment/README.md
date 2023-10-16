### Fields

New fields added by these scripts:

* `author_lccn` - Author's LCCN from id.loc.gov

* `author_viaf` - Author viaf.org cluster number

* `author_wikidata` - Author's Wikdiata Q number

* `wikidata_work_qid`- Work Wikdiata Q number

* `author_authorized_heading` - Author's authorized NACO heading

* `oclc/hathi_marc` - the MARC XML from respective source

* `oclc_eholdings`- from OCLC Classify - the electronic holdings count

* `oclc_holdings` -  from OCLC Classify - the total holdings count

* `oclc_owi` -  from OCLC Classify - the Classify work identfier

* `oclc_isbn`- the ISBN from the OCLC MARC

* `hathi_rights` - the rights code from Hathi Trust

* `isbn_most_common_edition`- The most common ISBN, largest holdings from all the editions.

  

### Scripts

​	Scripts with "download" are ones that talk to APIs. Scripts starting with "parse" work on data in the file.



* `download_add_missing_lccn_viaf_wikidata` - Will download the equivalent identifier from id.loc.gov,  VIAF.org, and Wikidata if it has one of the others. For example if you have VIAF but want to add Wikidata.
* `download_author_lccn` - Will download the LCCN for a creator if you have the authorized heading stored.
* `download_author_viaf` - Will download the VIAF number if you have an authorized headings, this is good for non-US creator names.
* `download_hathi_marc` - Will download the Hathi Trust MARC record as XML and store it in the file if you have a Hathi Trust identifier.
* `download_oclc_classify_title_author`- Will download the OCLC Classify record if you only have a Author name and Title. Requires OCLC WSkey API key.
* `download_oclc_classify`- Will download the OCLC Classify record if you have a OCLC number. Requires OCLC WSkey API key.
* `download_oclc_marc_from_classify_editions` - It will download the most common OCLC record for a Work and store the MARC as XML in the file. Most common means the most holdings in OCLC's records. Requires OCLC WSkey API key.
* `download_oclc_marc` - Will download the OCLC Worldcat MARC record as XML and store it in the file if you have a OCLC number. Requires OCLC WSkey API key.
* `download_viaf_via_lccn` - Will download the VIAF number if you have the LCCN number.
* `download_wikidata_qid_by_lccn` - Adds the Q number of the author if you have their LCCN number.
* `download_wikidata_reconcile_iowa` - Reconciles against Wikidata if the person was involved with the University of Iowa.
* `download_wikidata_reconcile_no_biblo`- Reconciles against Wikidata if you only have a name and have some other biographical information, allowing for multiple points of verification. Work on a confidence scoring system based on positive data matches.
* `download_wikidata_reconcile_publisher` - Adds the Q number for potential publishers from Wikidata.
* `download_wikidata_reconcile_works` - Trys to add work Q numbers for a title if you have reconciled the author to a Q number
* `parse_add_open_library_work` - Using Classify response to add OL work id based on OCLC number, unfinished.
* `parse_cut_post45_...` - a series of scripts to output the final form the the dataset.
* `parse_hathi_add_auth_name` - Parse the Hathi Trust MARC record and extract the authorized name heading.
* `parse_hathi_add_isbn_oclc` - Parse the Hathi Trust MARC record and extract the ISBN and OCLC.
* `parse_marc_add_publisher` - Parse the MARC XML and extract the publisher's name.
* `parse_oclc_add_auth_name` - Parse MARC and add the authorized heading name
* `parse_oclc_add_isbn` - Add ISBN from OCLC MARC
* `parse_oclc_classify` - Example of how to parse a OCLC Classify response
