---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdfb3714bbabcacd2805dc4198e2cfffde3f0e8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857541"
---
# <span data-ttu-id="6ef48-101">New-AzsDataDiskObject</span><span class="sxs-lookup"><span data-stu-id="6ef48-101">New-AzsDataDiskObject</span></span>

## <span data-ttu-id="6ef48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ef48-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef48-103">Crea un disco di dati usato per creare una nuova immagine della piattaforma della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6ef48-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="6ef48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ef48-104">SYNTAX</span></span>

```
New-AzsDataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="6ef48-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ef48-105">DESCRIPTION</span></span>
<span data-ttu-id="6ef48-106">Crea un oggetto che contiene informazioni su un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="6ef48-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="6ef48-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ef48-107">EXAMPLES</span></span>

### <span data-ttu-id="6ef48-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6ef48-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="6ef48-109">Creare un nuovo oggetto disco dati.</span><span class="sxs-lookup"><span data-stu-id="6ef48-109">Create a new data disk object.</span></span>

## <span data-ttu-id="6ef48-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ef48-110">PARAMETERS</span></span>

### <span data-ttu-id="6ef48-111">-Lun</span><span class="sxs-lookup"><span data-stu-id="6ef48-111">-Lun</span></span>
<span data-ttu-id="6ef48-112">Numero di unità logica.</span><span class="sxs-lookup"><span data-stu-id="6ef48-112">Logical unit number.</span></span>

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

### <span data-ttu-id="6ef48-113">-URI</span><span class="sxs-lookup"><span data-stu-id="6ef48-113">-Uri</span></span>
<span data-ttu-id="6ef48-114">Posizione del modello di disco.</span><span class="sxs-lookup"><span data-stu-id="6ef48-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="6ef48-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef48-115">CommonParameters</span></span>
<span data-ttu-id="6ef48-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ef48-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef48-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ef48-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef48-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ef48-118">INPUTS</span></span>

## <span data-ttu-id="6ef48-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ef48-119">OUTPUTS</span></span>

## <span data-ttu-id="6ef48-120">Note</span><span class="sxs-lookup"><span data-stu-id="6ef48-120">NOTES</span></span>

## <span data-ttu-id="6ef48-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ef48-121">RELATED LINKS</span></span>

