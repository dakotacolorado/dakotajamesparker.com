<template>
  <v-container grid-list-xs>
    <v-layout row wrap>
      <v-flex xs12>
        <v-card>
          <v-card-title class="headline" style="color:rgb(66,66,66,0.8);height:80px" >
            <v-layout row justify-center>
              <h2 style="text-align:center">Dynamic Resume</h2>
            </v-layout>
          </v-card-title>

          <v-divider></v-divider>

          <v-card-text>
            <h1>About Me</h1><br>
            <p>
              I am a math based problem solver.
              Through my undergradute education I developed a deep understanding of quantatitive thinking and practices.
              This expertise has enabled me to quickly pivot my math and physics background into a career in financial services.
              I have worked on a range of projects in data science, software development, and technology architecture.
              As my career progresses I hope to grow my insight into mathematics and its applications;
              specifically I'm interested in studying information theory applied to artificial intellegence.
            </p>
          </v-card-text>

          <v-divider></v-divider>

          <v-card-text>
            <h1>Career Timeline</h1><br>
            <v-divider></v-divider>
            <v-timeline dense :style="{'margin-left': $vuetify.breakpoint.smAndDown ?  '0px' : '140px'}">

              <!-- UCCS -->
              <v-timeline-item
                fill-dot
                color="#000000"
                large
                >
                <template v-slot:icon>
                    <img style="width:44px; height:34px" src="https://www.logolynx.com/images/logolynx/46/46a748ef1945eccba4911bb1089ea893.png" title="University of Colorado at Colorado Springs, 2014-2015">
                    <span v-if="!$vuetify.breakpoint.smAndDown" class="headline font-weight-bold" style="position:absolute; width:140px;left:-130px">2014 - 2015</span>
                </template>
                <v-card color="#000000" dark>
                  <v-expansion-panels dark style="background-color:black">
                    <v-expansion-panel color="black">
                      <v-expansion-panel-header style="background-color:black"  class="subtitle-1">
                        <v-card-title class="title">
                          <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                            <strong style="color:#CFB87C">UC Colorado Springs, Physics Tutor</strong><br>
                            <span class="subtitle-2">Concurrent with High School</span><br>
                          </div>
                          <v-spacer></v-spacer>
                          <v-progress-circular
                            :value="85"
                            color="#CFB87C"
                            size="40"
                            width="2"
                            class="subtitle-2"
                            style="margin-top:-8px;line-height:9px;"
                            >
                            <div style="margin-top:3px; text-align:center">
                              3.4<br>
                              <span style="font-size:8px">GPA</span>
                            </div>
                          </v-progress-circular>
                        </v-card-title>
                      </v-expansion-panel-header>
                      <v-expansion-panel-content  class="subtitle-2" style="color:#A2A4A3;background-color:black">
                        <v-divider></v-divider>
                        <v-card-text v-if="!$vuetify.breakpoint.smAndDown">
                          <strong class="subtitle-1" style="color:#CFB87C;">UCCS Timeline</strong><br><br>
                          <v-timeline dense>

                            <v-timeline-item
                              fill-dot
                              color="#CFB87C"
                              small
                              >
                              <v-card color="#565A5C" light>
                                <v-expansion-panels dark style="background-color:#565A5C">
                                  <v-expansion-panel color="#565A5C">
                                    <v-expansion-panel-header  class="subtitle-1">
                                      <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                        <strong style="color:#CFB87C">AP Physics Tests</strong><br>
                                        <span class="subtitle-2">May 2014</span><br>
                                      </div>
                                    </v-expansion-panel-header>
                                    <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                      <ul>
                                        <li>Tested through the first year of college physics courses without any AP coursework (self taught)</li>
                                        <li>Placed in 2nd year physics courses at UCCS while I finished high school</li>
                                      </ul>
                                    </v-expansion-panel-content>
                                  </v-expansion-panel>
                                </v-expansion-panels>
                              </v-card>
                            </v-timeline-item>

                            <v-timeline-item
                              fill-dot
                              color="#CFB87C"
                              small
                              >
                              <v-card color="#565A5C" light>
                                <v-expansion-panels dark style="background-color:#565A5C">
                                  <v-expansion-panel color="#565A5C">
                                    <v-expansion-panel-header  class="subtitle-1">
                                      <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                        <strong style="color:#CFB87C">Physics Tutor</strong><br>
                                        <span class="subtitle-2">Science Learning Center, January 2015 - May 2015</span><br>
                                      </div>
                                    </v-expansion-panel-header>
                                    <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                      <ul>
                                        <li>Tutored students on first and second year college physics topics during my last semester of high school</li>
                                      </ul><br>
                                    </v-expansion-panel-content>
                                  </v-expansion-panel>
                                </v-expansion-panels>
                              </v-card>
                            </v-timeline-item>

                          </v-timeline>
                        </v-card-text>
                        <v-card-text v-else>
                          <strong class="subtitle-1" style="color:#CFB87C;">UCCS Timeline</strong><br><br>
                          <v-expansion-panels dark style="background-color:#565A5C">

                            <v-expansion-panel color="#565A5C">
                              <v-expansion-panel-header  class="subtitle-1">
                                <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                  <strong style="color:#CFB87C">AP Physics Tests</strong><br>
                                  <span class="subtitle-2">May 2014</span><br>
                                </div>
                              </v-expansion-panel-header>
                              <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                <ul>
                                  <li>Tested through the first year of college physics courses without any AP coursework (self taught)</li>
                                  <li>Placed in 2nd year physics courses at UCCS while I finished high school</li>
                                </ul>
                              </v-expansion-panel-content>
                            </v-expansion-panel>

                            <v-expansion-panel color="#565A5C">
                              <v-expansion-panel-header  class="subtitle-1">
                                <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                  <strong style="color:#CFB87C">Physics Tutor</strong><br>
                                  <span class="subtitle-2">Science Learning Center, January 2015 - May 2015</span><br>
                                </div>
                              </v-expansion-panel-header>
                              <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                <ul>
                                  <li>Tutored students on first and second year college physics topics during my last semester of high school</li>
                                </ul><br>
                              </v-expansion-panel-content>
                            </v-expansion-panel>

                          </v-expansion-panels>
                        </v-card-text>
                      </v-expansion-panel-content>
                    </v-expansion-panel>
                  </v-expansion-panels>
                </v-card>
              </v-timeline-item>

              <!-- CU Boulder -->
              <v-timeline-item
                fill-dot
                color="#000000"
                large
                >
                <template v-slot:icon>
                    <img style="width:34px; height:34px" src="https://www.cu.edu/sites/default/files/cu-standalone.png" title="University of Colorado, Boulder 2015-2018">
                    <span v-if="!$vuetify.breakpoint.smAndDown" class="headline font-weight-bold" style="position:absolute; width:140px;left:-130px">2015 - 2018</span>
                </template>
                <v-card color="#000000" dark>
                  <v-expansion-panels dark style="background-color:black">
                    <v-expansion-panel color="black">
                      <v-expansion-panel-header style="background-color:black"  class="subtitle-1">
                        <v-card-title class="title">
                          <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                            <strong style="color:#CFB87C">CU Boulder, B.S. Applied Mathematics </strong><br>
                            <span class="subtitle-2">Computer Science and Physics Minors</span><br>
                          </div>
                          <v-spacer></v-spacer>
                          <v-progress-circular
                            :value="95"
                            color="#CFB87C"
                            size="40"
                            width="2"
                            class="subtitle-2"
                            style="margin-top:-8px;line-height:9px;"
                            >
                            <div style="margin-top:3px; text-align:center">
                              3.8<br>
                              <span style="font-size:8px">GPA</span>
                            </div>
                          </v-progress-circular>
                        </v-card-title>
                      </v-expansion-panel-header>
                      <v-expansion-panel-content  class="subtitle-2" style="color:#A2A4A3;background-color:black">
                        <v-divider></v-divider>
                        <v-card-text v-if="!$vuetify.breakpoint.smAndDown">
                          <strong class="subtitle-1" style="color:#CFB87C;">CU Timeline</strong><br><br>
                          <v-timeline dense>

                            <v-timeline-item
                              fill-dot
                              color="#CFB87C"
                              small
                              >
                              <v-card color="#565A5C" light>
                                <v-expansion-panels dark style="background-color:#565A5C">
                                  <v-expansion-panel color="#565A5C">
                                    <v-expansion-panel-header  class="subtitle-1">
                                      <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                        <strong style="color:#CFB87C">Condensed Matter Physics Research Assistant</strong><br>
                                        <span class="subtitle-2">Dessau Lab, May 2016 - May 2017</span><br>
                                      </div>
                                    </v-expansion-panel-header>
                                    <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                      <ul>
                                        <li>Preformed critical temperature testing on superconducting materials</li>
                                        <li>Studied the BCS theory for superconductors and Cooper pairing</li>
                                      </ul><br>
                                      <v-layout row justify-center>
                                        <v-btn style="margin:2px;color:#CFB87C" outlined small href="https://codepen.io/dakota-parker/full/vwbEpJ" target="_blank">Phonon Visual (D3)</v-btn>
                                        <v-btn style="margin:2px;color:#CFB87C" outlined small href="https://drive.google.com/file/d/0B9ONIqGGOceOVzdZTHcxcFhNNUk/view?usp=sharing" target="_blank">BCS Presentation</v-btn>
                                        <v-btn style="margin:2px;color:#CFB87C" outlined small href="https://spot.colorado.edu/~dessau/" target="_blank">Dessau Group</v-btn>
                                      </v-layout>
                                    </v-expansion-panel-content>
                                  </v-expansion-panel>
                                </v-expansion-panels>
                              </v-card>
                            </v-timeline-item>

                            <v-timeline-item
                              fill-dot
                              color="#CFB87C"
                              small
                              >
                              <v-card color="#565A5C" light>
                                <v-expansion-panels dark style="background-color:#565A5C">
                                  <v-expansion-panel color="#565A5C">
                                    <v-expansion-panel-header  class="subtitle-1">
                                      <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                        <strong style="color:#CFB87C">Math Tutor</strong><br>
                                        <span class="subtitle-2">MARC, August 2017 - May 2018</span><br>
                                      </div>
                                    </v-expansion-panel-header>
                                    <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                      <ul>
                                        <li>Tutored students on physics and math topics ranging from first year algebra to graduate level statistics</li>
                                      </ul><br>
                                      <v-layout row justify-center>
                                        <v-btn style="margin:2px;color:#CFB87C" outlined small href="https://math.colorado.edu/marc/" target="_blank">Math Academic Resource Center (MARC)</v-btn>
                                      </v-layout>
                                    </v-expansion-panel-content>
                                  </v-expansion-panel>
                                </v-expansion-panels>
                              </v-card>
                            </v-timeline-item>

                            <v-timeline-item
                              fill-dot
                              color="#CFB87C"
                              small
                              >
                              <v-card color="#565A5C" light>
                                <v-expansion-panels dark style="background-color:#565A5C">
                                  <v-expansion-panel color="#565A5C">
                                    <v-expansion-panel-header  class="subtitle-1">
                                      <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                        <strong style="color:#CFB87C">HackCU 2018, 4th Place</strong><br>
                                        <span class="subtitle-2">CU Hackathon, February 2018</span><br>
                                      </div>
                                    </v-expansion-panel-header>
                                    <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                      <ul>
                                        <li>
                                          Used the Facebook graph API, the IBM Watson API, Python, and R to statistically correlate Facebook sentiment to the stock price for gun companies
                                        </li>
                                        <li>
                                          Won 1st palce in the OppenheimerFunds challenge and was recruited by OppenheimerFunds (now Invesco)
                                        </li>
                                      </ul><br>
                                      <v-layout row justify-center>
                                        <v-btn style="margin:2px;color:#CFB87C" outlined small href="https://hackcu.org/" target="_blank">CU Hackathon</v-btn>
                                      </v-layout>
                                    </v-expansion-panel-content>
                                  </v-expansion-panel>
                                </v-expansion-panels>
                              </v-card>
                            </v-timeline-item>

                          </v-timeline>
                        </v-card-text>
                        <v-card-text v-else>
                          <strong class="subtitle-1" style="color:#CFB87C;">CU Timeline</strong><br><br>
                          <v-expansion-panels dark style="background-color:#565A5C">

                            <v-expansion-panel color="#565A5C">
                              <v-expansion-panel-header  class="subtitle-1">
                                <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                  <strong style="color:#CFB87C">Condensed Matter Physics Research Assistant</strong><br>
                                  <span class="subtitle-2">Dessau Lab, May 2016 - May 2017</span><br>
                                </div>
                              </v-expansion-panel-header>
                              <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                <ul>
                                  <li>Preformed critical temperature testing on superconducting materials</li>
                                  <li>Studied the BCS theory for superconductors and Cooper pairing</li>
                                </ul><br>
                                <v-layout row justify-center>
                                  <v-btn style="margin:2px;color:#CFB87C" outlined small href="https://codepen.io/dakota-parker/full/vwbEpJ" target="_blank">Phonon Visual (D3)</v-btn>
                                  <v-btn style="margin:2px;color:#CFB87C" outlined small href="https://drive.google.com/file/d/0B9ONIqGGOceOVzdZTHcxcFhNNUk/view?usp=sharing" target="_blank">BCS Presentation</v-btn>
                                  <v-btn style="margin:2px;color:#CFB87C" outlined small href="https://spot.colorado.edu/~dessau/" target="_blank">Dessau Group</v-btn>
                                </v-layout>
                              </v-expansion-panel-content>
                            </v-expansion-panel>

                            <v-expansion-panel color="#565A5C">
                              <v-expansion-panel-header  class="subtitle-1">
                                <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                  <strong style="color:#CFB87C">Math Tutor</strong><br>
                                  <span class="subtitle-2">MARC, August 2017 - May 2018</span><br>
                                </div>
                              </v-expansion-panel-header>
                              <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                <ul>
                                  <li>Tutored students on physics and math topics ranging from first year algebra to graduate level statistics</li>
                                </ul><br>
                                <v-layout row justify-center>
                                  <v-btn style="margin:2px;color:#CFB87C" outlined small href="https://math.colorado.edu/marc/" target="_blank">MARC</v-btn>
                                </v-layout>
                              </v-expansion-panel-content>
                            </v-expansion-panel>

                            <v-expansion-panel color="#565A5C">
                              <v-expansion-panel-header  class="subtitle-1">
                                <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                  <strong style="color:#CFB87C">HackCU 2018, 4th Place</strong><br>
                                  <span class="subtitle-2">CU Hackathon, February 2018</span><br>
                                </div>
                              </v-expansion-panel-header>
                              <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                <ul>
                                  <li>
                                    Used the Facebook graph API, the IBM Watson API, python, and R to statistically correlate Facebook sentiment to the stock price for gun companies.
                                  </li>
                                  <li>
                                    Won 1st palce in the OppenheimerFunds challenge and was recruited by OppenheimerFunds (now Invesco).
                                  </li>
                                </ul><br>
                                <v-layout row justify-center>
                                  <v-btn style="margin:2px;color:#CFB87C" outlined small href="https://hackcu.org/" target="_blank">CU Hackathon</v-btn>
                                </v-layout>
                              </v-expansion-panel-content>
                            </v-expansion-panel>

                          </v-expansion-panels>
                        </v-card-text>
                        <v-divider></v-divider>
                        <v-card-text>
                          <strong class="subtitle-1" style="color:#CFB87C;">Coursework and Projects</strong><br><br>
                          <v-expansion-panels dark style="background-color:#565A5C">

                            <v-expansion-panel color="#565A5C">
                              <v-expansion-panel-header  class="subtitle-1">
                                <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                  <strong style="color:#CFB87C">Mathematics Coursework</strong><br>
                                  <span class="subtitle-2">Numerical Analysis, Applied Probability, Random Graph Theory, Fourier Series, Complex Analysis</span><br>
                                </div>
                              </v-expansion-panel-header>
                              <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                <ul>
                                  <li>
                                    <strong>Numerical Methods for Solving PDEs</strong>
                                    <v-btn style="margin-top:-4px; margin-left:4px; color:#CFB87C" outlined x-small href="https://drive.google.com/file/d/1sDitwDxf63r0tNicaxl_o-y_EZiRu1FQ/view?usp=sharing" target="_blank">Paper</v-btn>
                                    <v-btn style="margin-top:-4px; margin-left:4px; color:#CFB87C" outlined x-small href="https://www.youtube.com/watch?v=us6hhVkBRRQ" target="_blank">Video 1</v-btn>
                                    <v-btn style="margin-top:-4px; margin-left:4px; color:#CFB87C" outlined x-small href="https://www.youtube.com/watch?v=us6hhVkBRRQ" target="_blank">Video 2</v-btn>
                                    <br>
                                    <i class="caption">
                                      Used MATLAB to generate 1d and 2d numerical simulations to the wave equation
                                    </i>

                                  </li>
                                  <li>
                                    <strong>Signal Processing and Aliasing</strong>
                                    <v-btn style="margin-top:-4px; margin-left:4px; color:#CFB87C" outlined x-small href="https://drive.google.com/file/d/1Ru_EUd2K9EszeVeyPbnGcxmYh__YaU3b/view?usp=sharing" target="_blank">Paper</v-btn>
                                    <v-btn style="margin-top:-4px; margin-left:4px; color:#CFB87C" outlined x-small href="https://www.youtube.com/watch?v=gDaVOsYWF0E" target="_blank">Video 1</v-btn>
                                    <v-btn style="margin-top:-4px; margin-left:4px; color:#CFB87C" outlined x-small href="https://www.youtube.com/watch?v=fK4covoOXuk" target="_blank">Video 2</v-btn>
                                    <br>
                                    <i class="caption">
                                      Used MATLAB to sample signals and calculate the discrete Fourier transform on the result
                                    </i>
                                  </li>
                                  <li>
                                    <strong>Complex Analysis of Airfoils</strong>
                                    <v-btn style="margin-top:-4px; margin-left:4px; color:#CFB87C" outlined x-small href="https://drive.google.com/file/d/0B9ONIqGGOceOVUtpQUxkS29lY3c/view?usp=sharing" target="_blank">Paper</v-btn>
                                    <br>
                                    <i class="caption">
                                      Studied the applications of complex analysis in modeling 2d airfoil dynamics
                                    </i>
                                  </li>
                                </ul><br>
                              </v-expansion-panel-content>
                            </v-expansion-panel>

                            <v-expansion-panel color="#565A5C">
                              <v-expansion-panel-header  class="subtitle-1">
                                <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                  <strong style="color:#CFB87C">Physics Coursework</strong><br>
                                  <span class="subtitle-2">Statistical Mechanics, Quantum Mechanics, Classical Mechanics, Electricity and Magnetism, Condensed Matter</span><br>
                                </div>
                              </v-expansion-panel-header>
                              <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                <ul>

                                  <li>
                                    <strong>Quantum Mechanics Coursework (LaTeX)</strong>
                                    <v-btn style="margin-top:-4px; margin-left:4px; color:#CFB87C" outlined x-small href="https://drive.google.com/file/d/1IEuaee_kboxKa2VLINHt2RLlXrB2m3D3/view?usp=sharing" target="_blank">HW2</v-btn>
                                    <v-btn style="margin-top:-4px; margin-left:4px; color:#CFB87C" outlined x-small href="https://drive.google.com/file/d/1IC1ywzcfO3HXwfe1Ak-l_ia9ZiMBseDt/view?usp=sharing" target="_blank">HW3</v-btn>
                                    <br>
                                    <i class="caption">
                                      Work sample using an infinite-dimensional Hilbert space and tensors (operators) in this space
                                    </i>
                                  </li>

                                  <li>
                                    <strong>BCS Theory of Superconductors</strong>
                                    <v-btn style="margin-top:-4px; margin-left:4px; color:#CFB87C" outlined x-small href="https://drive.google.com/file/d/0B9ONIqGGOceOVzdZTHcxcFhNNUk/view?usp=sharing" target="_blank">Presentation</v-btn>
                                    <br>
                                    <i class="caption">
                                      Presentation of BSC theory and a slide-by-slide breakdown of the proof
                                    </i>
                                  </li>

                                  <li>
                                    <strong>Light Controlled Amplifier</strong>
                                    <v-btn style="margin-top:-4px; margin-left:4px; color:#CFB87C" outlined x-small href="https://www.youtube.com/watch?v=Uq-bOpU5Vk4" target="_blank">Demo</v-btn>
                                    <br>
                                    <i class="caption">
                                      Used oscilloscopes, op-amps, transistors, etc to construct a light controlled speaker
                                    </i>
                                  </li>


                                </ul><br>
                              </v-expansion-panel-content>
                            </v-expansion-panel>

                            <v-expansion-panel color="#565A5C">
                              <v-expansion-panel-header  class="subtitle-1">
                                <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                  <strong style="color:#CFB87C">Computer Science Coursework</strong><br>
                                  <span class="subtitle-2">Software Development, Algorithms, Numerical Methods, Statistical Methods,</span><br>
                                </div>
                              </v-expansion-panel-header>
                              <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                <ul>

                                  <li>
                                    <strong>Angry Bird Force Simulation</strong>
                                    <v-btn style="margin-top:-4px; margin-left:4px; color:#CFB87C" outlined x-small href="https://drive.google.com/file/d/1vOseeJmivMUg7m-3-Ww-B2xRVNEvw7GY/view?usp=sharing" target="_blank">Code</v-btn>
                                    <v-btn style="margin-top:-4px; margin-left:4px; color:#CFB87C" outlined x-small href="https://www.youtube.com/watch?v=4HNF84P7WQI" target="_blank">Video</v-btn>
                                    <br>
                                    <i class="caption">
                                      Used MATLAB to generate a flock of angry birds
                                    </i>

                                  </li>

                                  <li>
                                    <strong>Recursive Hexagonal Tileing</strong>
                                    <v-btn style="margin-top:-4px; margin-left:4px; color:#CFB87C" outlined x-small href="https://codepen.io/dakota-parker/pen/oRmxdM?editors=1010" target="_blank">Codepen</v-btn>
                                    <br>
                                    <i class="caption">
                                      Used JavaScript to write a recursive algorithm to tile hexagons into a larger hexagon
                                    </i>
                                  </li>

                                </ul><br>
                              </v-expansion-panel-content>
                            </v-expansion-panel>

                          </v-expansion-panels>
                        </v-card-text>
                      </v-expansion-panel-content>
                    </v-expansion-panel>
                  </v-expansion-panels>
                </v-card>
              </v-timeline-item>

              <!-- OppenheimerFunds -->
              <v-timeline-item
                fill-dot
                color="white"
                large
                >
                <template v-slot:icon>
                    <img style="width:38px; height:38px" src="https://media.glassdoor.com/sqll/16878/oppenheimerfunds-squarelogo.png" title="OppenheimerFunds 2018-2019">
                    <span v-if="!$vuetify.breakpoint.smAndDown" class="headline font-weight-bold" style="position:absolute; width:140px;left:-130px">2018 - 2019</span>
                </template>

                <v-card color="white" dark style="border:solid;border-color:black;border-width:4px" flat outlined>
                  <v-expansion-panels light style="background-color:#565A5C">

                    <v-expansion-panel color="#565A5C">
                      <v-expansion-panel-header style="background-color:white" class="subtitle-1">
                        <v-card-title class="title">
                          <div style="max-width:370px;line-height:20px;color:#A2A4A3">
                            <strong style="color:black">OppenheimerFunds, Solutions Architect </strong><br>
                            <span class="subtitle-2">Greater Denver Area</span><br>
                          </div>
                        </v-card-title>
                      </v-expansion-panel-header>
                      <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                        <v-divider light></v-divider>

                        <v-card-text v-if="!$vuetify.breakpoint.smAndDown">
                          <strong class="subtitle-1" style="color:black;">OppenheimerFunds Timeline</strong><br><br>
                          <v-timeline dense>

                            <v-timeline-item
                              fill-dot
                              color="black"
                              small
                              >
                              <v-card color="#565A5C" light>
                                <v-expansion-panels light style="background-color:#565A5C">
                                  <v-expansion-panel color="#565A5C">
                                    <v-expansion-panel-header  class="subtitle-1">
                                      <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                        <strong style="color:black">Enterprise Architecture Intern</strong><br>
                                        <span class="subtitle-2">May 2018 - August 2018</span><br>
                                      </div>
                                    </v-expansion-panel-header>
                                    <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                      <ul>
                                        <li>Used Python3 and R to statistically determine dependent applications within the OppenheimerFunds microservice architecture</li>
                                        <li>Built D3 visuals for the companies microservice architecture network</li>
                                      </ul><br>
                                      <v-layout row justify-center>
                                        <v-btn style="margin:2px;color:black" outlined small href="https://codepen.io/dakota-parker/pen/yWmqZy" target="_blank">D3 Force Graph Sample</v-btn>
                                      </v-layout>
                                    </v-expansion-panel-content>
                                  </v-expansion-panel>
                                </v-expansion-panels>
                              </v-card>
                            </v-timeline-item>

                            <v-timeline-item
                              fill-dot
                              color="black"
                              small
                              >
                              <v-card color="#565A5C" light>
                                <v-expansion-panels style="background-color:#565A5C">
                                  <v-expansion-panel color="#565A5C">
                                    <v-expansion-panel-header  class="subtitle-1">
                                      <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                        <strong style="color:black">Solutions Architect</strong><br>
                                        <span class="subtitle-2">August 2018 - May 2019</span><br>
                                      </div>
                                    </v-expansion-panel-header>
                                    <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                      <ul>
                                        <li>Built and deployed proof-of-concept Vue and Angular web applictions for data visualization, managment, and analytics</li>
                                        <li>Used Python to design statistical cost models around IT service downtime</li>
                                      </ul><br>
                                    </v-expansion-panel-content>
                                  </v-expansion-panel>
                                </v-expansion-panels>
                              </v-card>
                            </v-timeline-item>

                            <v-timeline-item
                              fill-dot
                              color="black"
                              small
                              >
                              <v-card color="#565A5C" light>
                                <v-expansion-panels light style="background-color:#565A5C">
                                  <v-expansion-panel color="#565A5C">
                                    <v-expansion-panel-header  class="subtitle-1">
                                      <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                        <strong style="color:black">Hackenheimer 2019, Above and Beyond Award</strong><br>
                                        <span class="subtitle-2">OppenheimerFunds Hackathon, February 2019</span><br>
                                      </div>
                                    </v-expansion-panel-header>
                                    <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3">
                                      <ul>
                                        <li>
                                          Used the Django framework to build a web tool that calculated and visualized the time-weighted returns for different advisors
                                        </li>
                                        <li>
                                          Used the Tensorflow with Python to build a chatbot for the web tool from scratch
                                        </li>
                                        <li>
                                          Won the above and beyond award presented by senior leadership
                                        </li>
                                      </ul><br>
                                    </v-expansion-panel-content>
                                  </v-expansion-panel>
                                </v-expansion-panels>
                              </v-card>
                            </v-timeline-item>

                          </v-timeline>
                        </v-card-text>

                        <v-card-text v-else>
                          <strong class="subtitle-1" style="color:black;">OppenheimerFunds Timeline</strong><br><br>
                          <v-expansion-panels dark style="background-color:white">

                            <v-expansion-panel color="white">
                              <v-expansion-panel-header  class="subtitle-1" style="background-color:white">
                                <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                  <strong style="color:black">Enterprise Architecture Intern</strong><br>
                                  <span class="subtitle-2">May 2018 - August 2018</span><br>
                                </div>
                              </v-expansion-panel-header>
                              <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3;background-color:white">
                                <ul>
                                  <li>Used Python3 and R to statistically determine dependent applications within the OppenheimerFunds microservice architecture</li>
                                  <li>Built D3 visuals for the companies microservice architecture network</li>
                                </ul>
                                <v-layout row justify-center>
                                  <v-btn style="margin:2px;color:black" outlined small href="https://codepen.io/dakota-parker/pen/yWmqZy" target="_blank">D3 Force Graph Sample</v-btn>
                                </v-layout>
                              </v-expansion-panel-content>
                            </v-expansion-panel>

                            <v-expansion-panel color="white">
                              <v-expansion-panel-header  class="subtitle-1" style="background-color:white">
                                <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                  <strong style="color:black">Solutions Architect</strong><br>
                                  <span class="subtitle-2">August 2018 - May 2019</span><br>
                                </div>
                              </v-expansion-panel-header>
                              <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3;background-color:white">
                                <ul>
                                  <li>Built and deployed proof-of-concept Vue and Angular web applictions for data visualization, managment, and analytics</li>
                                  <li>Used Python to design statistical cost models around IT service downtime</li>
                                </ul>
                              </v-expansion-panel-content>
                            </v-expansion-panel>

                            <v-expansion-panel color="white">
                              <v-expansion-panel-header  class="subtitle-1" style="background-color:white">
                                <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                  <strong style="color:black">Hackenheimer 2019, Above and Beyond Award</strong><br>
                                  <span class="subtitle-2">OppenheimerFunds Hackathon, February 2019</span><br>
                                </div>
                              </v-expansion-panel-header>
                              <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3;background-color:white">
                                <ul>
                                  <li>
                                    Used the Django framework to build a web tool that calculated and visualized the time-weighted returns for different advisors
                                  </li>
                                  <li>
                                    Won the above and beyond award presented by senior leadership
                                  </li>
                                </ul>
                              </v-expansion-panel-content>
                            </v-expansion-panel>

                          </v-expansion-panels>
                        </v-card-text>

                      </v-expansion-panel-content>
                    </v-expansion-panel>
                  </v-expansion-panels>
                </v-card>
              </v-timeline-item>


              <!-- Invesco -->
              <v-timeline-item
                fill-dot
                color="#001a7b"
                large
                >
                <template v-slot:icon>
                    <v-avatar>
                      <img style="width:56px; height:56px;" src='https://media.licdn.com/dms/image/C4D0BAQGlINbhv1qsdQ/company-logo_400_400/0?e=1574899200&v=beta&t=B73kIIJ5Zb9E6trzgyHDpbn-kvuQWvV0pchWRtumaSQ' title="Invesco, 2019-Current">

                    </v-avatar>
                    <span v-if="!$vuetify.breakpoint.smAndDown" class="headline font-weight-bold" style="position:absolute; width:140px;left:-130px">2019 - Now</span>
                </template>

                <v-card color="#001a7b" dark flat>
                  <v-expansion-panels dark style="background-color:#001a7b">
                    <v-expansion-panel color="#001a7b" class='elevation-0'>
                      <v-expansion-panel-header style="background-color:#001a7b" class="subtitle-1">
                        <v-card-title class="title">
                          <div style="max-width:400px;line-height:20px;color:#A2A4A3">
                            <strong style="color:white">Invesco, Analytics Associate </strong><br>
                            <span class="subtitle-2">Greater Denver Area (Remote for New York based team)</span><br>
                          </div>
                        </v-card-title>
                      </v-expansion-panel-header>
                      <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3;background-color:#001a7b" >
                        <v-divider dark></v-divider>

                        <v-card-text v-if="!$vuetify.breakpoint.smAndDown">
                          <strong class="subtitle-1" style="color:white;">Invesco Timeline</strong><br><br>
                          <v-timeline dense>

                            <v-timeline-item
                              fill-dot
                              color="white"
                              small
                              >
                              <v-card light>
                                <v-expansion-panels light>
                                  <v-expansion-panel light >
                                    <v-expansion-panel-header light class="subtitle-1" style="background-color:#001a7b">
                                      <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                        <strong style="color:white">Analytics Associate</strong><br>
                                        <span class="subtitle-2">May 2019 - Now</span><br>
                                      </div>
                                    </v-expansion-panel-header>
                                    <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3;background-color:#001a7b">
                                      <ul>
                                        <li>Built Vue web applictions for data visualization and analytics</li>
                                        <li>Used Python to manage and extract analytics from client data</li>
                                      </ul><br>
                                    </v-expansion-panel-content>
                                  </v-expansion-panel>
                                </v-expansion-panels>
                              </v-card>
                            </v-timeline-item>

                          </v-timeline>
                        </v-card-text>

                        <v-card-text v-else>
                          <strong class="subtitle-1" style="color:white;">Invesco Timeline</strong><br><br>
                          <v-expansion-panels light style="background-color:#001a7b">

                            <v-expansion-panel light>
                              <v-expansion-panel-header  class="subtitle-1"  style="background-color:white">
                                <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                  <strong style="color:black">Analytics Associate</strong><br>
                                  <span class="subtitle-2">May 2019 - Now</span><br>
                                </div>
                                <template v-slot:actions>
                                  <v-icon color="teal">mdi-check</v-icon>
                                </template>
                              </v-expansion-panel-header>
                              <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3; background-color:white">
                                <ul>
                                  <li>Built and deployed proof-of-concept Vue and Angular web applictions for data visualization, managment, and analytics</li>
                                  <li>Used Python to design statistical cost models around IT service downtime</li>
                                </ul><br>
                              </v-expansion-panel-content>
                            </v-expansion-panel>

                          </v-expansion-panels>
                        </v-card-text>

                      </v-expansion-panel-content>
                    </v-expansion-panel>
                  </v-expansion-panels>
                </v-card>
              </v-timeline-item>


              <!-- Enterprise Network -->
              <v-timeline-item
                fill-dot
                color="rgb(110,220,220)"
                large
                >
                <template v-slot:icon>
                    <h2 style="color:rgb(66,66,66)">EN</h2>
                    <span v-if="!$vuetify.breakpoint.smAndDown" class="headline font-weight-bold" style="position:absolute; width:140px;left:-130px">2019 - Now</span>
                </template>

                <v-card dark flat>
                  <v-expansion-panels>
                    <v-expansion-panel color="#A2A4A3" class='elevation-0'>
                      <v-expansion-panel-header class="subtitle-1">
                        <v-card-title class="title">
                          <div style="max-width:420px;line-height:20px;color:#A2A4A3">
                            <strong style="color:#A2A4A3">Enterprise<span style="color:rgb(110,220,220)">Network</span>, Independent Developer</strong><br>
                            <span class="subtitle-2">Greater Denver Area</span><br>
                          </div>
                        </v-card-title>
                      </v-expansion-panel-header>
                      <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3;">
                        <v-divider dark></v-divider>

                        <v-card-text v-if="!$vuetify.breakpoint.smAndDown">
                          <strong class="subtitle-1" style="color:#A2A4A3;">EnterpriseNetwork Timeline</strong><br><br>
                          <v-timeline dense>

                            <v-timeline-item
                              fill-dot
                              color="#A2A4A3"
                              small
                              >
                              <v-card light>
                                <v-expansion-panels>
                                  <v-expansion-panel light >
                                    <v-expansion-panel-header light style="background-color:rgb(66,66,66)" class="subtitle-1">
                                      <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                        <strong style="color:white">Alpha Development Stage</strong><br>
                                        <span class="subtitle-2">August 2019 - Now</span><br>
                                      </div>
                                    </v-expansion-panel-header>
                                    <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3;background-color:rgb(66,66,66)">
                                      <ul>
                                        <li>Used AWS S3, Cloudfront, and Route 53, to publicly host a Vue web application</li>
                                        <li>Used AWS Cognito and Amplify to add user authentication, sign-in, and managment</li>
                                        <li>Used AWS Lambda and DynamoDB to establish a REST API to support user data storage</li>
                                        <li>Used Vue, D3, and Vuetify to build interactive dashboards supporting data managment and visualization</li>
                                      </ul><br>
                                    </v-expansion-panel-content>
                                  </v-expansion-panel>
                                </v-expansion-panels>
                              </v-card>
                            </v-timeline-item>

                            <v-timeline-item
                              fill-dot
                              color="#A2A4A3"
                              small
                              >
                              <v-card light>
                                <v-expansion-panels>
                                  <v-expansion-panel light >
                                    <v-expansion-panel-header light style="background-color:rgb(66,66,66)" class="subtitle-1">
                                      <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                        <strong style="color:white">Alpha Deployment</strong><br>
                                        <span class="subtitle-2">August 29, 2019</span><br>
                                      </div>
                                      <v-spacer></v-spacer>
                                      <v-btn outlined color="rgb(110,220,220)" max-width=220 small href="https://enterprisenetwork.app/#" target="_blank">EnterpriseNetwork.app</v-btn>
                                      <v-spacer></v-spacer>
                                    </v-expansion-panel-header>
                                    <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3;background-color:rgb(66,66,66)">
                                      <ul>
                                        <li>Purchased domain and securly hosted the web application</li>
                                        <li>Started to collect user interviews and market information</li>
                                      </ul><br>
                                    </v-expansion-panel-content>
                                  </v-expansion-panel>
                                </v-expansion-panels>
                              </v-card>
                            </v-timeline-item>

                          </v-timeline>
                        </v-card-text>

                        <v-card-text v-else>
                          <strong class="subtitle-1" style="color:#A2A4A3;">EnterpriseNetwork Timeline</strong><br><br>
                          <v-expansion-panels dark style="background-color:rgb(110,220,220)">

                            <v-expansion-panel light >
                              <v-expansion-panel-header light style="background-color:rgb(66,66,66)" class="subtitle-1">
                                <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                  <strong style="color:white">Alpha Development Stage</strong><br>
                                  <span class="subtitle-2">August 2019 - Now</span><br>
                                </div>
                              </v-expansion-panel-header>
                              <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3;background-color:rgb(66,66,66)">
                                <ul>
                                  <li>Used AWS S3, Cloudfront, and Route 53, to publicly host a Vue web application</li>
                                  <li>Used AWS Cognito and Amplify to add user authentication, sign-in, and managment</li>
                                  <li>Used AWS Lambda and DynamoDB to establish a REST API to support user data storage</li>
                                  <li>Used Vue, D3, and Vuetify to build interactive dashboards supporting data managment and visualization</li>
                                </ul><br>
                              </v-expansion-panel-content>
                            </v-expansion-panel>

                            <v-expansion-panel light >
                              <v-expansion-panel-header light style="background-color:rgb(66,66,66)" class="subtitle-1">
                                <div style="max-width:360px;line-height:20px;color:#A2A4A3">
                                  <strong style="color:white">Alpha Deployment</strong><br>
                                  <span class="subtitle-2">August 29, 2019</span><br>
                                </div>
                                <v-spacer></v-spacer>
                                <v-btn flat outlined color="rgb(110,220,220)" max-width=220 small href="https://enterprisenetwork.app/#" target="_blank">EnterpriseNetwork.app</v-btn>
                                <v-spacer></v-spacer>
                              </v-expansion-panel-header>
                              <v-expansion-panel-content class="subtitle-2" style="color:#A2A4A3;background-color:rgb(66,66,66)">
                                <ul>
                                  <li>Purchased domain and securly hosted the web application</li>
                                  <li>Started to collect user interviews and market information</li>
                                </ul><br>
                              </v-expansion-panel-content>
                            </v-expansion-panel>

                          </v-expansion-panels>
                        </v-card-text>

                      </v-expansion-panel-content>
                    </v-expansion-panel>
                  </v-expansion-panels>
                </v-card>
              </v-timeline-item>


            </v-timeline>
            <v-divider></v-divider>
          </v-card-text>

          <v-divider></v-divider>
          <v-card-text>
            <h1>Skills and Projects</h1><br>
            <v-layout wrap>
              <v-flex xs12 md4>
                <v-card outlined>
                  <v-card-text >
                    <strong style="margin:11px 10px;font-size:18px">Computer Skills</strong>
                    <strong style="float:right;margin-right:10px">Skill</strong>
                    <v-divider></v-divider>
                    <v-treeview
                      :items="coding_skills"
                      dense
                      hoverable
                      open-on-click
                      >
                      <template v-slot:append="{ item, open }">
                        <v-progress-circular style="font-size:10px" v-if="item.confidence" :value="item.confidence/5*100" :color="confidenceColor[item.confidence]">{{item.confidence}}/5</v-progress-circular>
                      </template>
                    </v-treeview>
                  </v-card-text>
                </v-card>
              </v-flex>
              <v-flex xs12 md4>
                <v-card outlined>
                  <v-card-text >
                    <strong style="margin:11px 10px;font-size:18px">Math Topics</strong>
                    <strong style="float:right;margin-right:10px"></strong>
                    <v-divider></v-divider>
                    <v-treeview
                      :items="math_skills"
                      dense
                      hoverable
                      open-on-click
                      >
                      <template v-slot:append="{ item, open }">
                        <v-progress-circular style="font-size:10px" v-if="item.confidence" :value="item.confidence/5*100" :color="confidenceColor[item.confidence]">{{item.confidence}}/5</v-progress-circular>
                      </template>
                    </v-treeview>
                  </v-card-text>
                </v-card>
              </v-flex>
              <v-flex xs12 md4>
                <v-card outlined>
                  <v-card-text >
                    <strong style="margin:11px 10px;font-size:18px">Coding Languages</strong>
                    <strong style="float:right;margin-right:10px">Skill</strong>
                    <v-divider></v-divider>
                    <v-treeview
                      :items="coding_skills"
                      dense
                      hoverable
                      open-on-click
                      >
                      <template v-slot:append="{ item, open }">
                        <v-progress-circular style="font-size:10px" v-if="item.confidence" :value="item.confidence/5*100" :color="confidenceColor[item.confidence]">{{item.confidence}}/5</v-progress-circular>
                      </template>
                    </v-treeview>
                  </v-card-text>
                </v-card>
              </v-flex>
            </v-layout>
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>


export default {
  data: ()=>({
    coding_skills:[
      {
        id: 2,
        name: 'JavaScript',
        confidence: 3,
        children:[
          {
            id:3,
            name: 'VueJS',
            confidence: 4
          },
          {
            id:3,
            name: 'Vuetify',
            confidence: 4
          },
          {
            id:4,
            name: 'D3',
            confidence: 4
          },
          {
            id:5,
            name: 'AWS Amplify',
            confidence: 2
          },
          {
            id:6,
            name: 'AngularJS',
            confidence: 2
          },
        ]
      },
      {
        id: 7,
        name: 'Python',
        confidence: 3,
        children:[
          {
            id:8,
            name: 'Numpy and Scipy',
            confidence: 4
          },
          {
            id:9,
            name: 'Pandas',
            confidence: 3
          },
          {
            id:10,
            name: 'Tensorflow',
            confidence: 2
          },
          {
            id:11,
            name: 'Django',
            confidence: 1
          },
        ]
      },
      {
        id: 12,
        name: 'MATLAB',
        confidence: 3,
      },
      {
        id: 13,
        name: 'Mathematica',
        confidence: 5,
      },
      {
        id: 14,
        name: 'HTML/CSS',
        confidence: 4,
      },
    ],
    math_skills:[
      {
        id: 1,
        name: 'Linear Algebra',
        confidence: 4,
        children:[
          {
            id:11,
            name: 'Matrices and Linear Equations',
            confidence: 5
          },
          {
            id:12,
            name: 'Vector Spaces',
            confidence: 4
          },
          {
            id:12,
            name: 'Matrix Decompostions and Relations',
            confidence: 3
          },
          {
            id:13,
            name: 'Multilinear Algebra',
            confidence: 2
          },
        ]
      },
      {
        id: 2,
        name: 'Numerical Analysis',
        confidence: 4,
        children:[
          {
            id:22,
            name: 'Numerical Linear Algebra',
            confidence: 3
          },
          {
            id:21,
            name: 'Numerical Quadrature',
            confidence: 4
          },
          {
            id:23,
            name: 'Numerical PDEs and ODEs',
            confidence: 3
          },
          {
            id:23,
            name: 'Optimization Algorithms',
            confidence: 3
          },
        ]
      },
      {
        id: 3,
        name: 'Probability and Stats',
        confidence: 4,
        children:[
          {
            id:31,
            name: 'Network Graph Theory',
            confidence: 3
          },
          {
            id:32,
            name: '',
            confidence: 3
          },
          {
            id:33,
            name: 'Network Graph Theory',
            confidence: 3
          },
        ]
      },
      {
        id: 4,
        name: 'Calculus',
        confidence: 5,
      },
      {
        id: 5,
        name: 'Complex Analysis',
        confidence: 4,
      },
    ],
    confidenceColor:{
      1: 'rgb(200,200,150)',
      2: 'rgb(170,210,150)',
      3: 'rgb(140,230,150)',
      4: 'rgb(110,240,150)',
      5: 'rgb(80,250,150)',
    }
  }),
  computed: {

  },
  methods:{

  },
  mounted(){
  }
};
</script>
