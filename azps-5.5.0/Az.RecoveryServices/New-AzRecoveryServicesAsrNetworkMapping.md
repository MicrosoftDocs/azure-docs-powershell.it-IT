---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dca68a4f6315ee124c927d0efb0ff0eb95bf1663
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191374"
---
# <span data-ttu-id="c32bd-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c32bd-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="c32bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c32bd-102">SYNOPSIS</span></span>
<span data-ttu-id="c32bd-103">Crea un mapping di rete ASR tra due reti.</span><span class="sxs-lookup"><span data-stu-id="c32bd-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="c32bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c32bd-104">SYNTAX</span></span>

### <span data-ttu-id="c32bd-105">EnterpriseToEnterprise (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c32bd-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c32bd-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="c32bd-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c32bd-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="c32bd-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c32bd-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c32bd-108">DESCRIPTION</span></span>
<span data-ttu-id="c32bd-109">Il cmdlet **New-AzRecoveryServicesAsrNetworkMapping** avvia l'operazione di creazione di un mapping di rete ASR tra due reti e restituisce l'oggetto processo ASR per il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c32bd-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c32bd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c32bd-110">EXAMPLES</span></span>

### <span data-ttu-id="c32bd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c32bd-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="c32bd-112">Avvia l'operazione di creazione del mapping di rete usando il nome specificato, le reti primarie e di ripristino e restituisce un processo ASR per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c32bd-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="c32bd-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c32bd-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="c32bd-114">Avvia il mapping di rete per l'operazione di creazione usando il nome specificato, le reti primarie e di ripristino e restituisce un processo A MATRICE per tenere traccia dell'operazione (scenario Da Azure ad Azure).</span><span class="sxs-lookup"><span data-stu-id="c32bd-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="c32bd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c32bd-115">PARAMETERS</span></span>

### <span data-ttu-id="c32bd-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="c32bd-116">-AzureToAzure</span></span>
<span data-ttu-id="c32bd-117">Contrassegnare per creare uno scenario AzureToAzure.</span><span class="sxs-lookup"><span data-stu-id="c32bd-117">Flag to create AzureToAzure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c32bd-118">-DefaultProfile</span></span>
<span data-ttu-id="c32bd-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c32bd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c32bd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c32bd-120">-Name</span></span>
<span data-ttu-id="c32bd-121">Nome del mapping di rete ASR da creare.</span><span class="sxs-lookup"><span data-stu-id="c32bd-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="c32bd-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="c32bd-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="c32bd-123">Specifica l'ID di rete virtuale di Azure della rete primaria per il mapping.</span><span class="sxs-lookup"><span data-stu-id="c32bd-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32bd-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="c32bd-124">-PrimaryFabric</span></span>
<span data-ttu-id="c32bd-125">Specifica il tessuto ASR in cui creare il mapping.</span><span class="sxs-lookup"><span data-stu-id="c32bd-125">Specifies the ASR fabric where mapping should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32bd-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="c32bd-126">-PrimaryNetwork</span></span>
<span data-ttu-id="c32bd-127">Specifica l'oggetto di rete principale per il mapping di rete ASR.</span><span class="sxs-lookup"><span data-stu-id="c32bd-127">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c32bd-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="c32bd-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="c32bd-129">Specifica l'ID di rete Azure di ripristino per il mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="c32bd-129">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32bd-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="c32bd-130">-RecoveryFabric</span></span>
<span data-ttu-id="c32bd-131">Oggetto tessuto Azure Site Recovery corrispondente all'area geografica azure di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c32bd-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32bd-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="c32bd-132">-RecoveryNetwork</span></span>
<span data-ttu-id="c32bd-133">Specifica l'oggetto di rete di recupero per il mapping di rete ASR.</span><span class="sxs-lookup"><span data-stu-id="c32bd-133">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c32bd-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c32bd-134">-Confirm</span></span>
<span data-ttu-id="c32bd-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c32bd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c32bd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c32bd-136">-WhatIf</span></span>
<span data-ttu-id="c32bd-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c32bd-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c32bd-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c32bd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c32bd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c32bd-139">CommonParameters</span></span>
<span data-ttu-id="c32bd-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c32bd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c32bd-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c32bd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c32bd-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="c32bd-142">INPUTS</span></span>

### <span data-ttu-id="c32bd-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="c32bd-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="c32bd-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c32bd-144">OUTPUTS</span></span>

### <span data-ttu-id="c32bd-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="c32bd-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c32bd-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="c32bd-146">NOTES</span></span>

## <span data-ttu-id="c32bd-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c32bd-147">RELATED LINKS</span></span>

[<span data-ttu-id="c32bd-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c32bd-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="c32bd-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c32bd-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
