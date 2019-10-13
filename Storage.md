# Storage

## Vendor

[![WD-LOGO.png](https://i.postimg.cc/wvs6931N/WD-LOGO.png)](https://postimg.cc/G8d0QLJ3)

 **Western Digital Corporation** (abbreviated **WDC**, commonly known as simply **Western Digital** and **WD**) is an American company. It designs, manufactures and sells data technology products, including storage devices, data center systems and cloud storage services. 

## Type

[![SN500.png](https://i.postimg.cc/bJ1K6nGm/SN500.png)](https://postimg.cc/njcRrCGm)

**Product Number:**  WDS500G1B0C 

**Capacity:** 500GB

**Interface:** PCIe Gen 3 x 2

**Form Factor:** M.2 2280

**Dimensions (L x W x H):** 3.15" x 0.87" x 0.09"

## Technologies

### PCIe® NVMe™ interface

**NVM Express** (**NVMe**) or **Non-Volatile Memory Host Controller Interface Specification** (**NVMHCIS**) is an open logical device interface specification for accessing non-volatile storage media attached via a PCI Express (PCIe) bus. The acronym NVM stands for non-volatile memory, which is often NAND flash memory that comes in several physical form factors, including solid-state drives (SSDs), PCI Express (PCIe) add-in cards, M.2 cards, and other forms. NVM Express, as a logical device interface, has been designed to capitalize on the low latency and internal parallelism of solid-state storage devices.

By its design, NVM Express allows host hardware and software to fully exploit the levels of parallelism possible in modern SSDs. As a result, NVM Express reduces I/O overhead and brings various performance improvements relative to previous logical-device interfaces, including multiple long command queues, and reduced latency. (The previous interface protocols were developed for use with far slower hard disk drives (HDD) where a very lengthy delay (relative to CPU operations) exists between a request and data transfer, where data speeds are much slower than RAM speeds, and where disk rotation and seek time give rise to further optimization requirements.)

### 3D NAND

3D NAND flash is a type of flash memory in which the memory cells are stacked vertically in multiple layers.

Flash manufacturers developed 3D NAND to address challenges they encountered in scaling 2D/planar NAND technology to achieve higher densities at a lower cost per bit. Planar NAND flash technology uses a single layer of memory cells. As NAND manufacturers worked to shrink the memory cells, cell-to-cell interference caused a reduction in the reliability of planar NAND flash products.

3D NAND flash is suitable for the same types of business and consumer applications for which planar NAND is in use. Solid-state drives equipped with NAND flash can boost application performance and lower latency in comparison to traditional storage media such as hard disk drives and tape.

### TLC NAND

Storing 3 bits per cell, TLC flash is the cheapest form of flash to manufacture. The biggest disadvantage to this type of flash is that it is only suitable for consumer usage, and would not be able to meet the standards for industrial use. Read/write life cycles are considerably shorter at 3,000 to 5,000 cycles per cell.

## Pros and cons

### 500GB vs 512GB

Normally, we will assumed that the half TB model should be 512GB, however this one only provides 500GB. The missing space is actually used for **Over-Provisioning**, which improves performance and often increases the endurance of the SSD, helping the drive last longer due to the SSD Controller having more Flash NAND storage available to alleviate NAND Flash wear over its useful life. 

### PICe Gen 3 x2 vs x4

Although SN500 only support PCIe Gen 3 x2, it only needs 2 lanes. The performance increase of adding another 2 isn't large enough so that it's more like wasting 2 lanes if it use PICe Gen 3 x 4.

### TLC vs MLC

Although  Cells will survive considerably less read/write cycles compared to MLC NAND. Consumer use usually won't use that much read/write cycles at all before they switch to a new SSD.  TLC is Cheaper to manufacture which in turn leads to cheaper to market SSDs.

## Key indicators

### IO performance

[![ASSSD.png](https://i.postimg.cc/L6z8qymb/ASSSD.png)](https://postimg.cc/8jzS9mJR)

Sequential Read Performance: 1581MB/s, claimed to be 1700MB/s.

Sequential Write Performance: 1033MB/s, claimed to be 1450MB/s.

Random Read Performance and Random Write Performance is much better compared to SATA SSD and HDD.

Access Time is also quite low.

**How to:**

I used AS SSD benchmark to test IO performance.

### Cache size

[![HDTune.png](https://i.postimg.cc/FsmQ6hQT/HDTune.png)](https://postimg.cc/jC89w02f)

The 500GB version of SN500 is equipped with about 6.5GB of SLC cache, files under this size can reach peak performance mentioned above.

**How to:**

I used HD Tune Pro to write a super large file to the disk and test its write speed, turns out that after writing 6.5GB of data, the writing speed dropped, indicating that the cache size is about 6.5 GB.

### IO performance without cache

[![HDTune.png](https://i.postimg.cc/C5pVSgnL/HDTune.png)](https://postimg.cc/S2dPfHGw)

The 500GB version of SN500 can reach Sequential Write Speed at about 750MB/s after SLC cache used up.

**How to:**

Same as above, after the writing speed dropped, it shows the true writing performance of the TLC NAND.

## My comment

Super Xiang!! This is by far the most worth-purchasing SSD that I have ever met. I have another NVMe PCIe Gen3 x 4 SSD in another machine, and I tested that as well. Their performance are nearly identical. And SN500 has several shining points. First it's vendor is trust-worthy, I don't have to worry about the NAND inside is recycled or not genuine. Second it's cheap. Third the raw performance of the NAND is mind blowing, most high-end consumer SSD can not reach 750MB/s write after cache is used up, and it has a very aggressive garbage collecting algorithm, the recovering time after cache used up is very short, although this may shorten the longevity, there's nothing to worry about since it comes with a 5-Year Warranty.