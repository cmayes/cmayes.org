# Prompt: Port existing Zola project to Hugo.

The Cloudflare Pages build process is deprecating the v1 version of the build image. The latest, v3,
does not have Zola installed by default. Since I'm not terribly happy with the Zola project, this
is a good opportunity to port it to Hugo.

---

## Metadata

|Field| Value                                                        |
|---|--------------------------------------------------------------|
|Feature| Port personal site to Hugo                                   |
|Model| JetBrains Claude Agent (I think this uses claude-sonnet-4-6) |
|Last updated| 2026-03-22                                                   |
|Author| cmayes@cmay.es                                               |

## Prompt

```
Port the existing Zola project to Hugo. The main thing to preserve is the content. 
I'm not sure how I will apply a layout, but it will be with something natively supported by Hugo.
I am not married to the existing Zola theme.

Delete the Zola configs as we have those in version control in case we need to go back. I am 
aiming to start with a clean slate (aside from the content).

I will be deploying to Cloudflare Pages, so make any necessary adjustments to the Hugo configs to support this.

Update the README to reflect the new Hugo configs. Update the IDEA project settings to reflect the new Hugo configs.
```
