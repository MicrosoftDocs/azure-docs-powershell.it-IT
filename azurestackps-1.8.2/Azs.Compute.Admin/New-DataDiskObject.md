---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37d41ae2ec772cc755436bc01c3c4009c9c30f5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030249"
---
# <span data-ttu-id="18d95-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="18d95-101">New-DataDiskObject</span></span>

## <span data-ttu-id="18d95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18d95-102">SYNOPSIS</span></span>
<span data-ttu-id="18d95-103">Crea un disco di dati usato per creare una nuova immagine della piattaforma della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18d95-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="18d95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18d95-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="18d95-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18d95-105">DESCRIPTION</span></span>
<span data-ttu-id="18d95-106">Crea un oggetto che contiene informazioni su un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="18d95-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="18d95-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18d95-107">EXAMPLES</span></span>

### <span data-ttu-id="18d95-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="18d95-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="18d95-109">Creare un nuovo oggetto disco dati.</span><span class="sxs-lookup"><span data-stu-id="18d95-109">Create a new data disk object.</span></span>

## <span data-ttu-id="18d95-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18d95-110">PARAMETERS</span></span>

### <span data-ttu-id="18d95-111">-Lun</span><span class="sxs-lookup"><span data-stu-id="18d95-111">-Lun</span></span>
<span data-ttu-id="18d95-112">Numero di unità logica.</span><span class="sxs-lookup"><span data-stu-id="18d95-112">Logical unit number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18d95-113">-URI</span><span class="sxs-lookup"><span data-stu-id="18d95-113">-Uri</span></span>
<span data-ttu-id="18d95-114">Posizione del modello di disco.</span><span class="sxs-lookup"><span data-stu-id="18d95-114">Location of the disk template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18d95-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18d95-115">CommonParameters</span></span>
<span data-ttu-id="18d95-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18d95-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18d95-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18d95-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18d95-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18d95-118">INPUTS</span></span>

## <span data-ttu-id="18d95-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18d95-119">OUTPUTS</span></span>

## <span data-ttu-id="18d95-120">Note</span><span class="sxs-lookup"><span data-stu-id="18d95-120">NOTES</span></span>

## <span data-ttu-id="18d95-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18d95-121">RELATED LINKS</span></span>

