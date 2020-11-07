---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37d41ae2ec772cc755436bc01c3c4009c9c30f5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859710"
---
# <span data-ttu-id="47e83-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="47e83-101">New-DataDiskObject</span></span>

## <span data-ttu-id="47e83-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47e83-102">SYNOPSIS</span></span>
<span data-ttu-id="47e83-103">Crea un disco di dati usato per creare una nuova immagine della piattaforma della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="47e83-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="47e83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47e83-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="47e83-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47e83-105">DESCRIPTION</span></span>
<span data-ttu-id="47e83-106">Crea un oggetto che contiene informazioni su un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="47e83-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="47e83-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47e83-107">EXAMPLES</span></span>

### <span data-ttu-id="47e83-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="47e83-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="47e83-109">Creare un nuovo oggetto disco dati.</span><span class="sxs-lookup"><span data-stu-id="47e83-109">Create a new data disk object.</span></span>

## <span data-ttu-id="47e83-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47e83-110">PARAMETERS</span></span>

### <span data-ttu-id="47e83-111">-Lun</span><span class="sxs-lookup"><span data-stu-id="47e83-111">-Lun</span></span>
<span data-ttu-id="47e83-112">Numero di unità logica.</span><span class="sxs-lookup"><span data-stu-id="47e83-112">Logical unit number.</span></span>

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

### <span data-ttu-id="47e83-113">-URI</span><span class="sxs-lookup"><span data-stu-id="47e83-113">-Uri</span></span>
<span data-ttu-id="47e83-114">Posizione del modello di disco.</span><span class="sxs-lookup"><span data-stu-id="47e83-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="47e83-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e83-115">CommonParameters</span></span>
<span data-ttu-id="47e83-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47e83-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e83-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47e83-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e83-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47e83-118">INPUTS</span></span>

## <span data-ttu-id="47e83-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47e83-119">OUTPUTS</span></span>

## <span data-ttu-id="47e83-120">Note</span><span class="sxs-lookup"><span data-stu-id="47e83-120">NOTES</span></span>

## <span data-ttu-id="47e83-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47e83-121">RELATED LINKS</span></span>

