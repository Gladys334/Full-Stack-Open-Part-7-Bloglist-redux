Exercise 7.3: Redux Basics

Goal: Create Redux slices and connect them to the bloglist app.
What I did:

Setup Redux Toolkit and created a blogSlice to manage blogs.
Added actions for setting and adding blogs.
Connected Redux store to the React app.

Example Code:
import { createSlice } from '@reduxjs/toolkit'

const blogSlice = createSlice({
  name: 'blogs',
  initialState: [],
  reducers: {
    setBlogs(state, action) {
      return action.payload
    },
    addBlog(state, action) {
      state.push(action.payload)
    }
  }
})

export const { setBlogs, addBlog } = blogSlice.actions
export default blogSlice.reducer
