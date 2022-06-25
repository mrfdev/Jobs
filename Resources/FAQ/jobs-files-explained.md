# FAQ - Jobs/ files Explained

<topMenu>

---

We recently separated all the job files into their own files. This has made the creation and management of jobs a lot easier than before

You can rest easy if you are still running a Jobs version with the old `jobConfig`.

As you update to a new version of Jobs, all your old jobs will automatically be separated into files under `~/plugin/Jobs/Jobs`, keeping all your settings and customization. There's no data loss, so you don't need to worry.

Jobs will move the old configuration into FileBackups. If you don't need it, feel free to remove it after testing that everything works as it should.

The new system makes creating additional jobs easy. First, create a file with the job title as the name and .yml as the file type. It should look like this `newjob.yml`.

Now you can look at the example job file and start creating. It's in the same directory as the separated jobs files, but you can also [file find the example file online](https://github.com/Zrips/Jobs/blob/master/src/main/resources/jobs/_EXAMPLE.yml).

Alternatively, you can just copy an existing job and edit it directly if that feels more comfortable.

