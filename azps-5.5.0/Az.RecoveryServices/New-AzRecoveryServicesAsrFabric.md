---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192887"
---
# <span data-ttu-id="ba1c4-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ba1c4-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="ba1c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba1c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ba1c4-103">Crea un tessuto Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="ba1c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba1c4-104">SYNTAX</span></span>

### <span data-ttu-id="ba1c4-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ba1c4-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba1c4-106">Azure</span><span class="sxs-lookup"><span data-stu-id="ba1c4-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba1c4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ba1c4-107">DESCRIPTION</span></span>
<span data-ttu-id="ba1c4-108">Il cmdlet **New-AzRecoveryServicesAsrFabric** crea un tessuto azure site recovery del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="ba1c4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba1c4-109">EXAMPLES</span></span>

### <span data-ttu-id="ba1c4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ba1c4-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="ba1c4-111">Avvia la creazione di tessuto con il nome passato e restituisce il processo a matrice usato per tenere traccia dell'operazione di creazione di tessuto.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="ba1c4-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ba1c4-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="ba1c4-113">Avvia la creazione di tessuto azure con il nome passato e restituisce il processo A MATRICE usato per tenere traccia dell'operazione di creazione di tessuto.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="ba1c4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba1c4-114">PARAMETERS</span></span>

### <span data-ttu-id="ba1c4-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="ba1c4-115">-Azure</span></span>
<span data-ttu-id="ba1c4-116">Parametro Switch specifica di creare tessuto azure.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-116">Switch parameter specifies to create azure fabric.</span></span>

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

### <span data-ttu-id="ba1c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba1c4-117">-DefaultProfile</span></span>
<span data-ttu-id="ba1c4-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ba1c4-119">-Location</span><span class="sxs-lookup"><span data-stu-id="ba1c4-119">-Location</span></span>
<span data-ttu-id="ba1c4-120">Specifica l'area Azure corrispondente all'oggetto Tessuto da creare.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="ba1c4-121">L'oggetto tessuto Azure Site Recovery rappresenta un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="ba1c4-122">Per le macchine virtuali da replicare tra due aree azure, un tessuto primario rappresenta l'area azure principale e il tessuto di recupero.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="ba1c4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ba1c4-123">-Name</span></span>
<span data-ttu-id="ba1c4-124">Specifica il nome di Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="ba1c4-125">-Type</span><span class="sxs-lookup"><span data-stu-id="ba1c4-125">-Type</span></span>
<span data-ttu-id="ba1c4-126">Specifica il tipo di tessuto Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="ba1c4-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba1c4-127">-Confirm</span></span>
<span data-ttu-id="ba1c4-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba1c4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba1c4-129">-WhatIf</span></span>
<span data-ttu-id="ba1c4-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba1c4-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba1c4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba1c4-132">CommonParameters</span></span>
<span data-ttu-id="ba1c4-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba1c4-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ba1c4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba1c4-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="ba1c4-135">INPUTS</span></span>

### <span data-ttu-id="ba1c4-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ba1c4-136">None</span></span>

## <span data-ttu-id="ba1c4-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba1c4-137">OUTPUTS</span></span>

### <span data-ttu-id="ba1c4-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ba1c4-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ba1c4-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="ba1c4-139">NOTES</span></span>

## <span data-ttu-id="ba1c4-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba1c4-140">RELATED LINKS</span></span>

[<span data-ttu-id="ba1c4-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ba1c4-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="ba1c4-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ba1c4-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
