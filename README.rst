Go Vim files
=============
I just wanted something I could use with my vim bundles for Go. I copied out
their vim supplied plugins and working on getting this to work as a normal vim
bundle.

See their LICENSE file and all that. This is merely for my own convenience in my
vim setup.

Example of my .vimrc changes for use
-------------------------------------
::

    " Highlight word and 'K' to get GoDoc output for word.
    au BufRead,BufNewFile *.go set filetype=go
    " ,m will run gomake
    au BufRead *.go set makeprg=gomake
    " ,M will run gofmt on the code to lint it
    autocmd FileType python map <buffer> <leader>M :Fmt<CR>:cw<CR>
