---
layout: post
title:      "Mod4 JS project The Chore Organizer!"
date:       2021-03-15 16:05:58 -0400
permalink:  mod4_js_project_the_chore_organizer
---



My Mod4 Project the chore organizer is finally finished and am relieved to have finally gotten through the whole thing. I had a few hiccups throughout the whole thing. But I think those issues have given me way more insight into how to problem solve through coding issues such more than I like to give them credit for. Also they have taught me how to be patient while solving coding issues and sometimes it is best to just walk away for a bit and reset when things are getting stuck.

One of the main issues that I feel will follow me into future projects was loading everything onto github properly. When I began the project and created a new rails api I did not let it ignore creating its own github repository, and therefore when I tried to upload it it created a nested git which was having issues saving to the main repository. Even though it wasnt uploading properly when I was trying to commit my changes I thought it would be a simple issue to fix so I just kept on going through the project and when I had time with my cohort lead I would just bring it up. Now I know this is definitely not something I should do in a proper work environment and now it tends to look bad on my project as well but I am glad I learned this in school and not at a job. Although learning it on a main project is probably less than ideal.

Moving on to the actual project I was surprised at how comfortable I felt designing the backend. During every project I always feel like I know the information but I almost feel like I have imposter syndrome and don't actually know it. Then when I started this project it just all comes back and felt very smooth and easy to do. 

In the frontend is where things slowed down dramatically. Getting started on a certain part was probably the most frustrating or worst part for me. Once I had a direction on where I was going and finally find the way to start it tended to get much easier. Creativity has always been where I lack so having to come up with something always takes me a while to get anything going.

In the design section of the project I rather enjoyed though. I always looked at the design stuff while looking at other projects or when doing labs and always thought that looked way more complicated than the coding. But after just spending some time playing around and looking at examples online, it was kind of refreshing just working on making your code look more appealing. The one set of design code I found fun to play around with was creating the buttons that would block the elements until clicked on. For example using one of the blocks of code I used for the drop down section of choosing your family:

``let selectHouse = true
selectHouseHoldBtn.addEventListener('click', () => {
    selectHouse = !selectHouse
    if(selectHouse) {
        selectHouseHoldBtn.textContent= 'Close'
        selectForm.style.display = 'block'
        selectForm.addEventListener('submit', e => {
            e.preventDefault()
            let familyId = e.target.querySelector('#family-select').value

            let chosenFamily = HouseHold.all.find(chosenFamily => familyId == chosenFamily.id)
            clearChoreDivs()
            chosenFamily.renderChores()
            chosenFamily.renderMembers()
        })
    } else {
        selectHouseHoldBtn.textContent = "Select Your Family"
        selectForm.style.display = 'none'
    }
})``

using the style.display = 'block' would cover the form until clicked on I found after playing with it for a while. But I find discovering the little things like those is what I enoy the most about coding funny enough.

The trickiest part for me was figuring out what to do after clicking the completed button on one of my chores. I didnt want it to just keep the completed button there as it would not look right, so I decided to created a reset button just in case you clicked it and didnt mean to. What I learned to use was ``previousElementSibling``. This will return the read-only property to the previous element that it was. After much painstaking time playing around with it I finally got it to work. I'm pretty sure years down the line I'm going to look at that code and cringe at how it was written. But as the saying goes if it ain't broke dont fix it and once I got it working I decided to just let it be.
