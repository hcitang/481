# Drag and Drop: Source and Destination

This tutorial provides a simple example of how drag and drop works. What you will end up doing is set two `ListBoxes`: a source and a destination. You will be able to drag items from the source into a the destination, and doing so _copies_ them into the source. Exercise to the reader: set it up so that dragging an item removes it from the source.

A drag and drop operation has two main components that need to be designed and programmed in: the source and the destination. At the **source**, we need to consider at least two things: (1) When someone drags from here, what does this mean? For example, is it a copy, is it a cut and paste, etc. In Windows Explorer, default behaviour is a `Move` operation unless you do the operation with the right mouse button, in which case, it asks you at the destination what you want to do. (2) What is the data that needs to be transferred? At the source, this is programmed by using the `DoDragDrop` method.

At the **destination**, we need to actually respond to `Drop` event. Here, we would extract from the event arguments the actual data. There can actually be several pieces of data stored at the same time. For example, try highlighting some content in a web browser, and dragging the text into tools -- e.g. a text editor (Notepad) vs. a rich text editor (MS Word). Notice that the rich text editor preserves the original formatting (or tries to) while the text editor only grabs the basic text. Each editor is actually responding to the `Drop` event, but extracting the data in a different format. See the [`DataFormats`](https://msdn.microsoft.com/en-us/library/system.windows.dataformats(v=vs.110).aspx) for a list of different formats that are generally available (but note that the _source_ decides which and how many formats to support -- for instance, if we are dragging an image file, it doesn't make sense to support the `DataFormats.WaveAudio` format).

Note: Although the language and examples I am using here are Windows-based, the principles of drag and drop are roughly equivalent across platforms.

In the example below, you will implement both the source and destination of the drag and drop operation.

[](https://www.youtube.com/watch?v=cYFBMgU4j4k)

[source video](https://www.youtube.com/watch?v=cYFBMgU4j4k)

**Knowledge:** Fundamentals of drag and drop operations. Note that in the general case, you are thinking about the source and destination independently. For instance, if Windows Explorer is the source of information, you only need to worry about being the destination. Notice that `DataFormats.FileDrop` exists as a data format type for Explorer drops.