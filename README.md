<b><u>Instructions for filter_LOVAlignment.py</b></u><br/>
written by the incredible Angulion (andreas.moeglich@uni-bayreuth.de)<br/>
used in Dietler et al. "Signal Transduction in Light-Oxygen-Voltage Receptors Lacking the Active-Site Glutamine" (2022)


<p>
<u>0. License</u><br/>
This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software Foundation,
Inc., 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301  USA
</p>


<p>
  <u>1. Sytem Requirements</u><br/>
- requires python3 and packages re and Bio
- tested with python 3.6.3, re 2.2.1 and Bio 1.77
- non-standard hardware is not required
</p>


<p>
<u>2. Installation Guide</u><br/>
Save this file to the same directory as the qblast XML file to be analyzed. (An example qblast file is included.) Beyond that, no dedicated installation is required.
<p/>


<p>
<u>3. Demo & Instructions for Use</u><br/>
3.1. Edit the python script in the bottom of the file according to your needs as follows:
- QUERY_SEQUENCE: this is the reference sequence you want the entries in the XML file to compare to
- POSITIONS_REQUIRED: enter the positions at which the entries must match the reference
- POSITIONS_AVOID: enter the positions at which the entries must NOT match the reference (i.e. they differ)
- TOLERANCE: optionally, specify how much mismatches are allowed in the comparison to the reference
- QBLAST_RESULT_FILE: the qblast XML input file to be parsed
- OUTPUT_FILE: the name of the fasta output file to which matching sequences are written

3.2. Execute the python script using python3 (will not work with Python 2.7). Depending on cpu and input file size, this should take a few seconds at most.

3.3. A fasta sequence file with the specified name and contents should have been generated.
<p/>
