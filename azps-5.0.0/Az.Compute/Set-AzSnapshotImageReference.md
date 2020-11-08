---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: deb122735b94ed8ac0de63330a9fbdb3ecac81d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200959"
---
# <span data-ttu-id="1c202-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="1c202-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="1c202-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c202-102">SYNOPSIS</span></span>
<span data-ttu-id="1c202-103">Imposta le proprietà di riferimento dell'immagine in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="1c202-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="1c202-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c202-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c202-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c202-105">DESCRIPTION</span></span>
<span data-ttu-id="1c202-106">Il cmdlet **set-AzSnapshotImageReference** imposta le proprietà di riferimento dell'immagine in un oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="1c202-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="1c202-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c202-107">EXAMPLES</span></span>

### <span data-ttu-id="1c202-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1c202-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="1c202-109">Il primo comando crea un oggetto snapshot locale con dimensioni 10GB in Premium_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1c202-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="1c202-110">Imposta anche il tipo di sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="1c202-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="1c202-111">Il secondo comando imposta l'ID immagine e il numero di unità logica 0 per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="1c202-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="1c202-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1c202-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1c202-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c202-113">PARAMETERS</span></span>

### <span data-ttu-id="1c202-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c202-114">-DefaultProfile</span></span>
<span data-ttu-id="1c202-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c202-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c202-116">-ID</span><span class="sxs-lookup"><span data-stu-id="1c202-116">-Id</span></span>
<span data-ttu-id="1c202-117">Specifica l'ID.</span><span class="sxs-lookup"><span data-stu-id="1c202-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="1c202-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="1c202-118">-Lun</span></span>
<span data-ttu-id="1c202-119">Specifica il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="1c202-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="1c202-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="1c202-120">-Snapshot</span></span>
<span data-ttu-id="1c202-121">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="1c202-121">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="1c202-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1c202-122">-Confirm</span></span>
<span data-ttu-id="1c202-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c202-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c202-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c202-124">-WhatIf</span></span>
<span data-ttu-id="1c202-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c202-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c202-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c202-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c202-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c202-127">CommonParameters</span></span>
<span data-ttu-id="1c202-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c202-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c202-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c202-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c202-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c202-130">INPUTS</span></span>

### <span data-ttu-id="1c202-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="1c202-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="1c202-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1c202-132">System.String</span></span>

### <span data-ttu-id="1c202-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1c202-133">System.Int32</span></span>

## <span data-ttu-id="1c202-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c202-134">OUTPUTS</span></span>

### <span data-ttu-id="1c202-135">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="1c202-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="1c202-136">Note</span><span class="sxs-lookup"><span data-stu-id="1c202-136">NOTES</span></span>

## <span data-ttu-id="1c202-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c202-137">RELATED LINKS</span></span>
