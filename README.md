### tayloe downmixer
This is a simple I/Q downmixer intended for use with a soundcard for digitization, with one (very poor) revision created in a weekend, after I discovered the existence of Tayloe detectors online. Created under the influence of music. Iterations have occured, with the recommended version being the latest commit to this repo. As of writing, however, the design has not been tested in real world (but shall eventually be). The current (and likely forever) design uses a FT232H communicating over I2C to a Si5351A that is then used in a divide-by-four to create the I/Q paired LO, fed into the multiplexer. On the front end is a simple elliptical LPF with a ~30MHz rolloff, and a 1.8V bias circuit. The sample capacitors are of value 0.068uF, which are on the input of an ADA4084 operational amplifier. This is connected through bypass capacitors to the 3.5mm audio jack. For simplicity, a single rail supply is used for the operational amplifier, as the bias on the input should maintain a proper swing.\
"Inspired" by the classic "A Software Defined Radio for the Masses" Series, published in QEX (and available in this repo).\
Hardware is licensed under CERN Open Hardware Licence Version 2 - Strongly Reciprocal (LICENSE.txt)