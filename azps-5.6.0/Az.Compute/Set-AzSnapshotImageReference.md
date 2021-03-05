---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: 6746bc96f7c1a14d617f3147676556be7402b71c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008014"
---
# <span data-ttu-id="de3eb-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="de3eb-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="de3eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de3eb-102">SYNOPSIS</span></span>
<span data-ttu-id="de3eb-103">Imposta le proprietà di riferimento dell'immagine su un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="de3eb-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="de3eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de3eb-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de3eb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="de3eb-105">DESCRIPTION</span></span>
<span data-ttu-id="de3eb-106">Il cmdlet **Set-AzSnapshotImageReference** imposta le proprietà di riferimento per l'immagine su un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="de3eb-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="de3eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de3eb-107">EXAMPLES</span></span>

### <span data-ttu-id="de3eb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="de3eb-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="de3eb-109">Il primo comando crea un oggetto snapshot locale con dimensioni di 10 GB Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="de3eb-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="de3eb-110">Imposta anche il tipo di sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="de3eb-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="de3eb-111">Il secondo comando imposta l'ID immagine e il numero di unità 0 per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="de3eb-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="de3eb-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome 'Snapshot01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="de3eb-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="de3eb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de3eb-113">PARAMETERS</span></span>

### <span data-ttu-id="de3eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3eb-114">-DefaultProfile</span></span>
<span data-ttu-id="de3eb-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de3eb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de3eb-116">-Id</span><span class="sxs-lookup"><span data-stu-id="de3eb-116">-Id</span></span>
<span data-ttu-id="de3eb-117">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="de3eb-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="de3eb-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="de3eb-118">-Lun</span></span>
<span data-ttu-id="de3eb-119">Specifica il numero di unità logiche (LUN).</span><span class="sxs-lookup"><span data-stu-id="de3eb-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="de3eb-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="de3eb-120">-Snapshot</span></span>
<span data-ttu-id="de3eb-121">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="de3eb-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de3eb-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de3eb-122">-Confirm</span></span>
<span data-ttu-id="de3eb-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de3eb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de3eb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de3eb-124">-WhatIf</span></span>
<span data-ttu-id="de3eb-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de3eb-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de3eb-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de3eb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de3eb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3eb-127">CommonParameters</span></span>
<span data-ttu-id="de3eb-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de3eb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3eb-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="de3eb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3eb-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="de3eb-130">INPUTS</span></span>

### <span data-ttu-id="de3eb-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="de3eb-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="de3eb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="de3eb-132">System.String</span></span>

### <span data-ttu-id="de3eb-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="de3eb-133">System.Int32</span></span>

## <span data-ttu-id="de3eb-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de3eb-134">OUTPUTS</span></span>

### <span data-ttu-id="de3eb-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="de3eb-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="de3eb-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="de3eb-136">NOTES</span></span>

## <span data-ttu-id="de3eb-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de3eb-137">RELATED LINKS</span></span>
