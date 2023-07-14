# NFT card component

![Design preview for the NFT preview card component coding challenge](./design/desktop-preview.jpg)

This is a solution to the NFT preview card component challenge on Frontend Mentor. Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## The challenge
Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

## What I learned

I learned the trick to using position absolute to achieve the hover effect on the image:

```css
/* make sure img container is RELATIVE to PARENT*/
#img_wrapper {
    position: relative;
    border-radius: 8px;
}

#img_wrapper>img {
    display: block;
    width: 100%;
    height: 100%;
    border-radius: 8px;
}

#img_wrapper:hover {
    background-color: var(--mainCyan);
    transition: 0.75s ease-in-out;
}

#img_wrapper:hover>img {
    opacity: 0.5;
}

#cardOverlay {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    display: none;
}


#img_wrapper:hover #cardOverlay {
    display: block;
}

#img_wrapper:hover {
    cursor: pointer;
}

#cardOverlay img {
    width: 50px;
    height: 50px;
}
```

### Acknowledgments

[Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U) for the actual challenge