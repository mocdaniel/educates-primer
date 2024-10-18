# Live-Editing Workshops

While the authoring workflow is already quite fast by using the
`publish-workshop` and `deploy-workshop` cmdlets of the Educates CLI
or `update-workshop` from within a running session, an even better
experience would be live previews _while_ we edit our workshop
instructions.

With the Educates CLI, we can **patch** a deployed workshop to render
**local instructions** instead of the ones bundled and published with the
workshop. For this to work, however, we need [Hugo](https://gohugo.io)
installed locally.

## Installing Hugo

Hugo is a single Go binary that can be installed via package managers for
most systems.

### Installing Hugo on Linux

=== "Debian"

    ``` sh
    sudo apt install hugo
    ```

=== "Fedora"

    ``` sh
    sudo dnf install hugo
    ```

=== "SUSE"

    ``` sh
    sudo zypper install hugo
    ```

For other distributions, please look
[at the installation docs](https://gohugo.io/installation/linux/#package-managers).

### Installing Hugo ond MacOS and Windows

=== "Homebrew"

    ``` sh
    brew install hugo
    ```

=== "Choco"

    ``` sh
    choco install hugo-extended
    ```

=== "Scoop"

    ``` sh
    scoop install hugo-extended
    ```

=== "Winget"

    ``` sh
    winget install hugo-extended
    ```

## Patching a Workshop

Once Hugo is installed, we can patch a deployed workshop and start
hosting its instructions directly from our repository like this:

```sh title="Start live-editing workshops"
educates serve-workshop --patch-workshop
```

All we need to do afterwards is to start a new workshop session - it
will have its instructions updated in realtime as we edit them locally.
