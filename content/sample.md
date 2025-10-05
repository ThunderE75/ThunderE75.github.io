+++
title = "Showcase"
type = "blank"
indexable = false
+++
# Showcase

## Shortcodes
Links with icon
<!-- > syntax: {{< syntax >}}{{< linkIcon "https://youtube.com" "fa-brands fa-youtube" "My Video" >}}{{< /syntax >}} -->



{{< callout type="info" title="Custom Title" hideTitle=false showIcon=false foldable=true collapsed=true >}}
This Opinion callout hides both icon and title, but is foldable.
{{< /callout >}}

---
{{< callout type="note" >}}
This is a basic Note callout.
{{< /callout >}}

{{< callout type="abstract" foldable=true collapsed=true >}}
This Abstract callout starts folded.
{{< /callout >}}

{{< callout type="info" showIcon=false >}}
This Info callout hides the icon.
{{< /callout >}}

{{< callout type="tip" hideTitle=true >}}
This Tip callout hides the title text.
{{< /callout >}}

{{< callout type="success" foldable=true >}}
This Success callout is foldable and open by default.
{{< /callout >}}

{{< callout type="question" foldable=true collapsed=true >}}
This Question callout starts folded.
{{< /callout >}}

{{< callout type="warning" >}}
This Warning callout is standard (not foldable).
{{< /callout >}}

{{< callout type="failure" foldable=true >}}
This Failure callout is foldable and open by default.
{{< /callout >}}

{{< callout type="danger" foldable=true collapsed=true >}}
This Danger callout starts collapsed.
{{< /callout >}}

{{< callout type="bug" >}}
This Bug callout shows an icon and title.
{{< /callout >}}

{{< callout type="example" foldable=true >}}
This Example callout demonstrates foldable content.
{{< /callout >}}

{{< callout type="quote" foldable=true collapsed=true >}}
This Quote callout starts collapsed.
{{< /callout >}}

{{< callout type="opinion" hideTitle=true showIcon=false foldable=true >}}
This Opinion callout hides both icon and title, but is foldable.
{{< /callout >}}




- {{< kbd "Ctrl ⌃" >}}
- {{< kbd "Shift ⇧" >}}
- {{< kbd "Alt ⎇" >}}
- {{< kbd "Tab ↹" >}}
- {{< kbd "Backspace ←" >}}
- {{< kbd "Del ⌫" >}}
- {{< kbd "⊞ Win" >}}

- {{< linkicon "https://zsh.sourceforge.io/" "fa-solid fa-globe" "web">}}
- {{< linkicon "https://github.com/aristocratos/btop" "fa-brands fa-github" "Github/Repo">}}
- {{< linkicon "https://github.com/Xurdejl" "fa-solid fa-user" "Github/User" >}}
- {{< linkicon "https://github.com/Xurdejl" "fa-brands fa-google" "Google" >}}
- {{< linkicon "https://www.youtube.com/watch?v=dQw4w9WgXcQ" "fa-brands fa-youtube" "Youtube" >}}
- {{< linkicon "https://www.tomshardware.com/how-to/delete-efi-system-partition-windows" "fa-solid fa-blog" "Blog">}}

# Ideas
- ~~mpv guide~~
- Obsidian Rice
- Zen Rice
- glance setup
- use highlight shortcode ~~Syntax Highlighting & copy option~~

- Cool software, 
    - Files UXP, 


{{< img src="../../images/posts/mpv_showcase.png" caption="This is a caption" credit="Unsplash" creditURL="https://unsplash.com" >}}


{{< highlight bat "style=doom-one">}}
git clone https://github.com/ThunderE75/mpv-scripts %APPDATA%\mpv
{{< /highlight >}}

{{< highlight bat "style=onedark">}}
git clone https://github.com/ThunderE75/mpv-scripts %APPDATA%\mpv
{{< /highlight >}}

{{< highlight bat "style=vulcan">}}
git clone https://github.com/ThunderE75/mpv-scripts %APPDATA%\mpv
{{< /highlight >}}

{{< highlight bat "style=xcode-dark">}}
git clone https://github.com/ThunderE75/mpv-scripts %APPDATA%\mpv
{{< /highlight >}}

---

{{< highlight bat >}}
git clone https://github.com/ThunderE75/mpv-scripts %APPDATA%\mpv
{{< /highlight >}}

{{< highlight java >}}
class Solution {
    public ListNode removeNthFromEnd(ListNode head, int n) {
        ListNode res = new ListNode(0, head);
        ListNode slow = res;
        ListNode fast = head;

        // making the distance fixed
        for (int i = 0; i < n; i++)
            fast = fast.next;
        
        while (fast != null) {
            fast = fast.next;
            slow = slow.next;
        }

        slow.next = slow.next.next;
        return res.next;
    }
}
{{< /highlight >}}

--- 
- what 

{{< highlight java "lineNos=inline, style=doom-one">}}
class Solution {
    public ListNode removeNthFromEnd(ListNode head, int n) {
        ListNode res = new ListNode(0, head);
        ListNode slow = res;
        ListNode fast = head;

        // making the distance fixed
        for (int i = 0; i < n; i++)
            fast = fast.next;
        
        while (fast != null) {
            fast = fast.next;
            slow = slow.next;
        }

        slow.next = slow.next.next;
        return res.next;
    }
}
{{< /highlight >}}

{{< highlight java "style=onedark">}}
class Solution {
    public ListNode removeNthFromEnd(ListNode head, int n) {
        ListNode res = new ListNode(0, head);
        ListNode slow = res;
        ListNode fast = head;

        // making the distance fixed
        for (int i = 0; i < n; i++)
            fast = fast.next;
        
        while (fast != null) {
            fast = fast.next;
            slow = slow.next;
        }

        slow.next = slow.next.next;
        return res.next;
    }
}
{{< /highlight >}}

{{< highlight java "style=vulcan">}}
class Solution {
    public ListNode removeNthFromEnd(ListNode head, int n) {
        ListNode res = new ListNode(0, head);
        ListNode slow = res;
        ListNode fast = head;

        // making the distance fixed
        for (int i = 0; i < n; i++)
            fast = fast.next;
        
        while (fast != null) {
            fast = fast.next;
            slow = slow.next;
        }

        slow.next = slow.next.next;
        return res.next;
    }
}
{{< /highlight >}}

{{< highlight java "style=xcode-dark">}}
class Solution {
    public ListNode removeNthFromEnd(ListNode head, int n) {
        ListNode res = new ListNode(0, head);
        ListNode slow = res;
        ListNode fast = head;

        // making the distance fixed
        for (int i = 0; i < n; i++)
            fast = fast.next;
        
        while (fast != null) {
            fast = fast.next;
            slow = slow.next;
        }

        slow.next = slow.next.next;
        return res.next;
    }
}
{{< /highlight >}}