# AptEditor

This tool converts .apt files to editable .xml format and does the reverse.

## Usage

The tool is simple to use. You should have .apt and .const files together.

Type ``AptEditor xxx.apt`` in command prompt to export to .xml.

Edit the .xml file accordingly.

Type ``AptEditor xxx.xml`` again in command prompt to import back to .apt.

## Information APT files store

In NBA Live 2005-08 UI files, .apt files store data for;

- Functions used throughout game

- Position, color and visibility data for text does

- Size of the UI frame which is the entire UI component

For changing shape size, UV maps, you need to edit .ebo file. To do so you can use NEBOViewer.

## Known issues

It is not possible to add a new variable or content to apt files. We can only edit existing variables.