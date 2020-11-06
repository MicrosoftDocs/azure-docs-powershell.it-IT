---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskImageReference.md
ms.openlocfilehash: 963e6f4621276eda4fdf598d571f2c2171dbc4f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518172"
---
# <span data-ttu-id="f59d6-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="f59d6-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="f59d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f59d6-102">SYNOPSIS</span></span>
<span data-ttu-id="f59d6-103">Imposta le proprietà di riferimento dell'immagine in un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="f59d6-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f59d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f59d6-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <Disk> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f59d6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f59d6-105">DESCRIPTION</span></span>
<span data-ttu-id="f59d6-106">Il cmdlet **set-AzureRmDiskImageReference** imposta le proprietà di riferimento dell'immagine su un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="f59d6-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="f59d6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f59d6-107">EXAMPLES</span></span>

### <span data-ttu-id="f59d6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f59d6-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="f59d6-109">Il primo comando crea un oggetto disco locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f59d6-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="f59d6-110">Imposta anche il tipo di sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="f59d6-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="f59d6-111">Il secondo comando imposta l'ID immagine e l'unità logica numero 0 per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="f59d6-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="f59d6-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f59d6-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f59d6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f59d6-113">PARAMETERS</span></span>

### <span data-ttu-id="f59d6-114">-Disco</span><span class="sxs-lookup"><span data-stu-id="f59d6-114">-Disk</span></span>
<span data-ttu-id="f59d6-115">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="f59d6-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f59d6-116">-ID</span><span class="sxs-lookup"><span data-stu-id="f59d6-116">-Id</span></span>
<span data-ttu-id="f59d6-117">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="f59d6-117">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59d6-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="f59d6-118">-Lun</span></span>
<span data-ttu-id="f59d6-119">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="f59d6-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59d6-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f59d6-120">-Confirm</span></span>
<span data-ttu-id="f59d6-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f59d6-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59d6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f59d6-122">-WhatIf</span></span>
<span data-ttu-id="f59d6-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f59d6-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f59d6-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f59d6-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59d6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59d6-125">CommonParameters</span></span>
<span data-ttu-id="f59d6-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f59d6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59d6-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f59d6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59d6-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f59d6-128">INPUTS</span></span>

### <span data-ttu-id="f59d6-129">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="f59d6-129">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="f59d6-130">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f59d6-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f59d6-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f59d6-131">OUTPUTS</span></span>

### <span data-ttu-id="f59d6-132">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="f59d6-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="f59d6-133">Note</span><span class="sxs-lookup"><span data-stu-id="f59d6-133">NOTES</span></span>

## <span data-ttu-id="f59d6-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f59d6-134">RELATED LINKS</span></span>

