<script>
    import { Toolbar, ToolbarButton, ToolbarGroup, Textarea, Button } from 'flowbite-svelte';
    import Food from '../Food.svelte';
    import Navegator from '../Navegator.svelte';
    import { Label, Input, InputAddon, ButtonGroup } from 'flowbite-svelte'
    
    let textareaprops = {
    id: 'message',
    name: 'message',
    label: 'Your message',
    rows: 4,
    placeholder: 'Leave a comment...',
  };
</script>

<Navegator/>
  <div class="p-20 mx-10">
    <div class="mb-6">
      <Label for="input-group-1" class="block mb-2">Your Email</Label>
      <Input id="email" type="email" placeholder="name@flowbite.com">
      <svg slot="left" aria-hidden="true" class="w-5 h-5 text-gray-500 dark:text-gray-400" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"></path><path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"></path></svg>
      </Input>
  </div>
  <div class="mb-6">
      <Label for="website-admin" class="block mb-2">Username</Label>
      <ButtonGroup class="w-full">
        <InputAddon>
        <svg aria-hidden="true" class="w-5 h-5 text-gray-500 dark:text-gray-400" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"></path><path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"></path></svg>
        </InputAddon>
        <Input id="website-admin" placeholder="Name" />
      </ButtonGroup>
    </div>
    <form>
      <Textarea class="mb-4" placeholder="Write a comment">
        <div slot="footer" class="flex items-center justify-between">
        <Button type="submit">Post comment</Button>
        <Toolbar embedded>
          <ToolbarButton name="Attach file"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6"><path stroke-linecap="round" stroke-linejoin="round" d="M18.375 12.739l-7.693 7.693a4.5 4.5 0 01-6.364-6.364l10.94-10.94A3 3 0 1119.5 7.372L8.552 18.32m.009-.01l-.01.01m5.699-9.941l-7.81 7.81a1.5 1.5 0 002.112 2.13" /></svg></ToolbarButton>
          <ToolbarButton name="Set location"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6"><path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" /><path stroke-linecap="round" stroke-linejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" /></svg></ToolbarButton>
          <ToolbarButton name="Upload image"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6"><path stroke-linecap="round" stroke-linejoin="round" d="M2.25 15.75l5.159-5.159a2.25 2.25 0 013.182 0l5.159 5.159m-1.5-1.5l1.409-1.409a2.25 2.25 0 013.182 0l2.909 2.909m-18 3.75h16.5a1.5 1.5 0 001.5-1.5V6a1.5 1.5 0 00-1.5-1.5H3.75A1.5 1.5 0 002.25 6v12a1.5 1.5 0 001.5 1.5zm10.5-11.25h.008v.008h-.008V8.25zm.375 0a.375.375 0 11-.75 0 .375.375 0 01.75 0z" /></svg></ToolbarButton>
        </Toolbar>
        </div>
      </Textarea>
    </form>
    <p class="ml-auto text-xs text-gray-500 dark:text-gray-400">Remember, contributions to this topic should follow our <a href="/" class="text-blue-600 dark:text-blue-500 hover:underline">Community Guidelines</a>.</p>
  </div>
<Food/>