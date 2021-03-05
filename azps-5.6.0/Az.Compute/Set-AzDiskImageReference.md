---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: aed0113b229d41665effd7904d2de2357b4b5d93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991463"
---
# <span data-ttu-id="7bf4a-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="7bf4a-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="7bf4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bf4a-102">SYNOPSIS</span></span>
<span data-ttu-id="7bf4a-103">Imposta le proprietà di riferimento immagine su un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="7bf4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bf4a-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bf4a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7bf4a-105">DESCRIPTION</span></span>
<span data-ttu-id="7bf4a-106">Il cmdlet **Set-AzDiskImageReference** imposta le proprietà di riferimento dell'immagine su un oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="7bf4a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bf4a-107">EXAMPLES</span></span>

### <span data-ttu-id="7bf4a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7bf4a-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="7bf4a-109">Il primo comando crea un oggetto disco locale con dimensioni di 10 GB Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="7bf4a-110">Imposta anche il tipo di sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="7bf4a-111">Il secondo comando imposta l'ID immagine e il numero di unità 0 per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="7bf4a-112">L'ultimo comando accetta l'oggetto disco e crea un disco con il nome 'Disk01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7bf4a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bf4a-113">PARAMETERS</span></span>

### <span data-ttu-id="7bf4a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bf4a-114">-DefaultProfile</span></span>
<span data-ttu-id="7bf4a-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bf4a-116">-Disco</span><span class="sxs-lookup"><span data-stu-id="7bf4a-116">-Disk</span></span>
<span data-ttu-id="7bf4a-117">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="7bf4a-118">-Id</span><span class="sxs-lookup"><span data-stu-id="7bf4a-118">-Id</span></span>
<span data-ttu-id="7bf4a-119">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="7bf4a-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="7bf4a-120">-Lun</span></span>
<span data-ttu-id="7bf4a-121">Specifica il numero di unità logiche (LUN).</span><span class="sxs-lookup"><span data-stu-id="7bf4a-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="7bf4a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bf4a-122">-Confirm</span></span>
<span data-ttu-id="7bf4a-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bf4a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bf4a-124">-WhatIf</span></span>
<span data-ttu-id="7bf4a-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bf4a-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bf4a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bf4a-127">CommonParameters</span></span>
<span data-ttu-id="7bf4a-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bf4a-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bf4a-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="7bf4a-130">INPUTS</span></span>

### <span data-ttu-id="7bf4a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="7bf4a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="7bf4a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7bf4a-132">System.String</span></span>

### <span data-ttu-id="7bf4a-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7bf4a-133">System.Int32</span></span>

## <span data-ttu-id="7bf4a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bf4a-134">OUTPUTS</span></span>

### <span data-ttu-id="7bf4a-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="7bf4a-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="7bf4a-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="7bf4a-136">NOTES</span></span>

## <span data-ttu-id="7bf4a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bf4a-137">RELATED LINKS</span></span>
