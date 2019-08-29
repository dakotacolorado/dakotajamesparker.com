<template>
  <svg id="resume" style="width:100vw;height:calc(100vh - 60px);">
  </svg>
</template>

<script>
// import * as math from 'mathjs'
import * as d3 from 'd3'

export default {
  data: ()=>({
    resume:{
      name: 'Dakota Parker',
      title_size: 45,
      title_y: -15,
      pre: '',
      post: '',
      body_size : 25,
      body_y: 0,
      clicked: false,
      img: 'https://media.licdn.com/dms/image/C4E03AQGd1Rf3DvR6Sg/profile-displayphoto-shrink_200_200/0?e=1572480000&v=beta&t=g5Knp8GEKIrZb3oyY42aZ-Dv5TZevDo9YLRXs-p2L08',
      img_size: 1.5,
      r: 160,
      node_color: '#262b2a',
      node_outline: '#d9f673',
      fx:0,
      fy:0,
      children: [
        {
          name: 'Education',
          title_size: 40,
          title_y: -15,
          pre: 'CU Boulder, 2015-2018',
          post: 'CU Boulder, 2015-2018',
          body_size : 20,
          body_y: 20,
          clicked: false,
          img: 'https://upload.wikimedia.org/wikipedia/en/thumb/d/d3/Colorado_Buffaloes_logo.svg/200px-Colorado_Buffaloes_logo.svg.png',
          img_size: 1,
          r: 120,
          node_color: '#A2A4A3',
          node_outline: '#CFB87C',
          distance:150,
          children: [
            {
              name: 'GPA',
              title_size: 16,
              title_y: 0,
              pre: '3.8',
              post: '3.8',
              body_size : 16,
              body_y: 16,
              clicked: false,
              r: 26,
              node_color: '#A2A4A3',
              node_outline: '#CFB87C',
              distance: -20,
            },
            {
              name: '',
              title_size: 16,
              title_y: 0,
              pre: 'Transcript',
              post: 'Transcript',
              body_size : 10,
              body_y: 5,
              clicked: false,
              r: 26,
              node_color: '#A2A4A3',
              node_outline: '#CFB87C',
              distance: -20,
            },
            {
              name: 'Applied Math',
              title_size: 16,
              title_y: 0,
              pre: 'Bachelor of Science',
              post: 'Bachelor of Science',
              body_size : 12,
              body_y: 16,
              clicked: false,
              r: 60,
              node_color: '#A2A4A3',
              node_outline: '#CFB87C',
              distance: -20,
            },
            {
              name: 'Physics',
              title_size: 14,
              title_y: 0,
              pre: 'Minor',
              post: 'Minor',
              body_size : 12,
              body_y: 16,
              clicked: false,
              r: 40,
              node_color: '#A2A4A3',
              node_outline: '#CFB87C',
              distance: -20,
            },
            {
              name: 'Computer Science',
              title_size: 10,
              title_y: 0,
              pre: 'Minor',
              post: 'Minor',
              body_size : 12,
              body_y: 16,
              clicked: false,
              r: 40,
              node_color: '#A2A4A3',
              node_outline: '#CFB87C',
              distance: -20,
            },
          ]
        },
        {
          name: 'OppenheimerFunds',
          title_size: 20,
          title_y: -5,
          pre: 'June 2018 - June 2019',
          post: 'June 2018 - June 2019',
          body_size : 14,
          body_y: 16,
          clicked: false,
          r: 100,
          node_color: 'white',
          node_outline: 'black',
          distance: 0,
          img:'https://media.glassdoor.com/sqll/16878/oppenheimerfunds-squarelogo.png',
          img_size: 1.3,
          children:[
            {
              name: 'InvescoFunds',
              title_size: 20,
              title_y: -5,
              pre: 'June 2019 - Current',
              post: 'June 2019 - Current',
              body_size : 14,
              body_y: 16,
              clicked: false,
              r: 100,
              node_color: '#001a7b',
              node_outline: 'white',
              distance: 0,
              img: 'https://media.licdn.com/dms/image/C4D0BAQGlINbhv1qsdQ/company-logo_400_400/0?e=1574899200&v=beta&t=B73kIIJ5Zb9E6trzgyHDpbn-kvuQWvV0pchWRtumaSQ',
              img_size: 1.2,
              children:[
                {
                  name: 'Analytics Assoc.',
                  title_size: 10,
                  title_y: 5,
                  pre: '',
                  post: '',
                  body_size : 14,
                  body_y: 16,
                  clicked: false,
                  r: 40,
                  node_color: '#001a7b',
                  node_outline: 'white',
                  distance: -20,
                }
              ]
            },
            {
              name: 'Solutions Arch.',
              title_size: 10,
              title_y: 5,
              pre: '',
              post: '',
              body_size : 14,
              body_y: 16,
              clicked: false,
              r: 40,
              node_color: 'white',
              node_outline: 'black',
              distance: -20,
            }
          ]
        },
        {
          name: "Projects",
          r:32,
          node_color: 'rgb(12,12,120)',
          node_outline: 'rgb(120,120,120)',

        },
        {
          name: "Skills",
          r: 20,
          node_color: 'rgb(12,12,120)',
          node_outline: 'rgb(120,120,120)',

          children: [
            {
              name: 'd3',
              r: 10,
              node_color: 'rgb(12,12,120)',
              node_outline: 'rgb(120,120,120)',

            },
            {
              name: 'JavaScript',
              r: 10,
              node_color: 'rgb(12,12,120)',
              node_outline: 'rgb(120,120,120)',

            }
          ]
        },
        {
          name: "Contact",
          r: 30,
          title_y: 5,
          node_color: '#262b2a',
          node_outline: '#d9f673',
          distance: -30

        }
      ]
    }
  }),
  computed: {
    nodes(){
      let nodes = [this.resume]
      function addChildren(children){
        for(let c in children){
          nodes.push(children[c])
          if(children[c].children)
            addChildren(children[c].children)
        }
      }
      addChildren(this.resume.children)
      return nodes
    },
    links(){
      let links = []
      function linkChildren(parent,children){
        for(let c in children){
          links.push({
            source:parent.name,
            target:children[c].name,
            length:parent.r + (children[c].distance ? children[c].distance : children[c].r)
          })
          if(children[c].children)
            linkChildren(children[c],children[c].children)
        }
      }
      linkChildren(this.resume,this.resume.children)
      return links
    }
  },
  methods:{

  },
  mounted(){
    const drag = simulation => {
      function dragstarted(d) {
        if (!d3.event.active) simulation.alphaTarget(0.3).restart();
        d.fx = d.x;
        d.fy = d.y;
      }
      function dragged(d) {
        d.fx = d3.event.x;
        d.fy = d3.event.y;
      }
      function dragended(d) {
        if (!d3.event.active) simulation.alphaTarget(0);
        d.fx = null;
        d.fy = null;
      }
      return d3.drag()
          .on("start", dragstarted)
          .on("drag", dragged)
          .on("end", dragended);
    }

    const simulation = d3.forceSimulation(this.nodes)
        .force("link", d3.forceLink(this.links)
          .id(d => d.name)
          .distance(d => d.length*1))
        .force("charge", d3.forceManyBody().strength(-600))
        .force("collide", d3.forceCollide().radius(n=>n.r))
        // .force('radial', d3.forceRadial(10).strength(-0.05))

    let svg = d3.select('#resume')
      .attr('viewBox',"-1000,-1000,2000,2000")

    const g = svg.append("g")
    svg.call(d3.zoom()
        .scaleExtent([1, 8])
        .on("zoom", zoomed))
    function zoomed() {
      g.attr("transform", d3.event.transform)
    }

    let link = g.selectAll("line")
    .data(this.links)
    .join("line")
      .attr("stroke", "#999")
      .attr("stroke-opacity", 0.6)
      .attr('stroke-width', 3)


    let node = g.selectAll(".node")
      .data(this.nodes)
      .join("g")
      .attr('class','node')
        .call(drag(simulation))

    node.append('circle')
      .attr("stroke", d=>d.node_outline)
      .attr("stroke-width", 2)
      .attr("r", d=>d.r)
      .attr('fill', d=>d.node_color)

    node.append('text')
      .attr("stroke", d=>d.node_outline)
      .attr('stroke-width', 0.6)
      .attr('fill','white')
      .text(d=>d.name)
      .attr('font-size', d=>d.title_size)
      .attr('y', d=>d.title_y)
      .attr('text-anchor','middle')
      .attr('class','node_title')

    node.append('text')
      .attr("stroke", d=>d.node_outline)
      .attr('stroke-width', 0.5)
      .text(d=>d.pre)
      .attr('font-size', d=>d.body_size)
      .attr('y', d=>d.body_y)
      .attr('text-anchor','middle')
      .attr('class','node_body')

    node.append("image")
        .attr("xlink:href", d=>d.img)
        .attr("y", d=>d.body_y+10)
        .attr("x", d=>-d.r/4*d.img_size)
        .attr("width", d=>d.r/2*d.img_size)
        .attr("height", d=>d.r/2*d.img_size)
        .attr("border-radius", d=>d.r/2)

    simulation.on("tick", () => {
      link
          .attr("x1", d => d.source.x)
          .attr("y1", d => d.source.y)
          .attr("x2", d => d.target.x)
          .attr("y2", d => d.target.y);

      node.attr("transform", d=>"translate(" + d.x + "," + d.y + ")")

    });
  }
};
</script>
