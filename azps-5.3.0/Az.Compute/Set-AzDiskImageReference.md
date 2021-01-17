---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 78a6c3bf85fae4fab9c5b9a06c366760b55804fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488208"
---
# <span data-ttu-id="3dedf-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="3dedf-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="3dedf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3dedf-102">SYNOPSIS</span></span>
<span data-ttu-id="3dedf-103">Imposta le proprietà di riferimento dell'immagine in un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="3dedf-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="3dedf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dedf-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dedf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dedf-105">DESCRIPTION</span></span>
<span data-ttu-id="3dedf-106">Il cmdlet **set-AzDiskImageReference** imposta le proprietà di riferimento dell'immagine su un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="3dedf-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="3dedf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dedf-107">EXAMPLES</span></span>

### <span data-ttu-id="3dedf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3dedf-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="3dedf-109">Il primo comando crea un oggetto disco locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3dedf-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="3dedf-110">Imposta anche il tipo di sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="3dedf-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="3dedf-111">Il secondo comando imposta l'ID immagine e l'unità logica numero 0 per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="3dedf-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="3dedf-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3dedf-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3dedf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3dedf-113">PARAMETERS</span></span>

### <span data-ttu-id="3dedf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dedf-114">-DefaultProfile</span></span>
<span data-ttu-id="3dedf-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dedf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-116">-Disco</span><span class="sxs-lookup"><span data-stu-id="3dedf-116">-Disk</span></span>
<span data-ttu-id="3dedf-117">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="3dedf-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-118">-ID</span><span class="sxs-lookup"><span data-stu-id="3dedf-118">-Id</span></span>
<span data-ttu-id="3dedf-119">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="3dedf-119">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="3dedf-120">-Lun</span></span>
<span data-ttu-id="3dedf-121">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="3dedf-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3dedf-122">-Confirm</span></span>
<span data-ttu-id="3dedf-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dedf-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dedf-124">-WhatIf</span></span>
<span data-ttu-id="3dedf-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dedf-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dedf-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dedf-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dedf-127">CommonParameters</span></span>
<span data-ttu-id="3dedf-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dedf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dedf-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dedf-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dedf-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3dedf-130">INPUTS</span></span>

### <span data-ttu-id="3dedf-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="3dedf-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="3dedf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3dedf-132">System.String</span></span>

### <span data-ttu-id="3dedf-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3dedf-133">System.Int32</span></span>

## <span data-ttu-id="3dedf-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dedf-134">OUTPUTS</span></span>

### <span data-ttu-id="3dedf-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="3dedf-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="3dedf-136">Note</span><span class="sxs-lookup"><span data-stu-id="3dedf-136">NOTES</span></span>

## <span data-ttu-id="3dedf-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dedf-137">RELATED LINKS</span></span>
