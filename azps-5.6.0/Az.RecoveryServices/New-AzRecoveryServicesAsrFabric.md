---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: bfea43fb0f27aff6405159c0174a698d9dc2298e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003134"
---
# <span data-ttu-id="3d49a-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3d49a-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="3d49a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d49a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d49a-103">Crea un tessuto Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3d49a-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="3d49a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d49a-104">SYNTAX</span></span>

### <span data-ttu-id="3d49a-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3d49a-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d49a-106">Azure</span><span class="sxs-lookup"><span data-stu-id="3d49a-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d49a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3d49a-107">DESCRIPTION</span></span>
<span data-ttu-id="3d49a-108">Il cmdlet **New-AzRecoveryServicesAsrFabric** crea un tessuto azure site recovery del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="3d49a-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="3d49a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d49a-109">EXAMPLES</span></span>

### <span data-ttu-id="3d49a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3d49a-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="3d49a-111">Avvia la creazione di tessuto con il nome passato e restituisce il processo ASR usato per tenere traccia dell'operazione di creazione di tessuto.</span><span class="sxs-lookup"><span data-stu-id="3d49a-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="3d49a-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3d49a-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="3d49a-113">Avvia la creazione di tessuto azure con il nome passato e restituisce il processo a matrice usato per tenere traccia dell'operazione di creazione di tessuto.</span><span class="sxs-lookup"><span data-stu-id="3d49a-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="3d49a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d49a-114">PARAMETERS</span></span>

### <span data-ttu-id="3d49a-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="3d49a-115">-Azure</span></span>
<span data-ttu-id="3d49a-116">Parametro Switch specifica di creare tessuto azure.</span><span class="sxs-lookup"><span data-stu-id="3d49a-116">Switch parameter specifies to create azure fabric.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d49a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d49a-117">-DefaultProfile</span></span>
<span data-ttu-id="3d49a-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d49a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3d49a-119">-Location</span><span class="sxs-lookup"><span data-stu-id="3d49a-119">-Location</span></span>
<span data-ttu-id="3d49a-120">Specifica l'area Azure corrispondente all'oggetto Tessuto da creare.</span><span class="sxs-lookup"><span data-stu-id="3d49a-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="3d49a-121">L'oggetto tessuto Azure Site Recovery rappresenta un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="3d49a-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="3d49a-122">Per le macchine virtuali da replicare tra due aree geografiche azure, un tessuto primario rappresenta l'area azure principale e il tessuto di recupero.</span><span class="sxs-lookup"><span data-stu-id="3d49a-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: System.String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d49a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3d49a-123">-Name</span></span>
<span data-ttu-id="3d49a-124">Specifica il nome di Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="3d49a-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d49a-125">-Type</span><span class="sxs-lookup"><span data-stu-id="3d49a-125">-Type</span></span>
<span data-ttu-id="3d49a-126">Specifica il tipo di tessuto azure site recovery.</span><span class="sxs-lookup"><span data-stu-id="3d49a-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d49a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d49a-127">-Confirm</span></span>
<span data-ttu-id="3d49a-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d49a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d49a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d49a-129">-WhatIf</span></span>
<span data-ttu-id="3d49a-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d49a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d49a-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d49a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d49a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d49a-132">CommonParameters</span></span>
<span data-ttu-id="3d49a-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d49a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d49a-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d49a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d49a-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="3d49a-135">INPUTS</span></span>

### <span data-ttu-id="3d49a-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3d49a-136">None</span></span>

## <span data-ttu-id="3d49a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d49a-137">OUTPUTS</span></span>

### <span data-ttu-id="3d49a-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="3d49a-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3d49a-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="3d49a-139">NOTES</span></span>

## <span data-ttu-id="3d49a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d49a-140">RELATED LINKS</span></span>

[<span data-ttu-id="3d49a-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3d49a-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="3d49a-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3d49a-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
