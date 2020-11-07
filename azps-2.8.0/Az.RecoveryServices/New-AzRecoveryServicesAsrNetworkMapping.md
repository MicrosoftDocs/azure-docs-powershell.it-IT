---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 0af3ffc25571273ebe572ee315b4e3c97de8f116
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855669"
---
# <span data-ttu-id="2c14e-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2c14e-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="2c14e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c14e-102">SYNOPSIS</span></span>
<span data-ttu-id="2c14e-103">Crea un mapping di rete ASR tra due reti.</span><span class="sxs-lookup"><span data-stu-id="2c14e-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="2c14e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c14e-104">SYNTAX</span></span>

### <span data-ttu-id="2c14e-105">EnterpriseToEnterprise (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2c14e-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c14e-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="2c14e-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c14e-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="2c14e-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c14e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c14e-108">DESCRIPTION</span></span>
<span data-ttu-id="2c14e-109">Il cmdlet **New-AzRecoveryServicesAsrNetworkMapping** avvia l'operazione di creazione di un mapping di rete ASR tra due reti e restituisce l'oggetto processo ASR per il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2c14e-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2c14e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c14e-110">EXAMPLES</span></span>

### <span data-ttu-id="2c14e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2c14e-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="2c14e-112">Avvia l'operazione di creazione del mapping di rete con il nome specificato, le reti primarie e di ripristino e restituisce un processo ASR per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2c14e-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="2c14e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2c14e-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="2c14e-114">Avvia il mapping di rete per l'operazione di creazione usando il nome specificato, le reti primarie e di ripristino e restituisce un processo ASR per tenere traccia dell'operazione (scenario di Azure in Azure).</span><span class="sxs-lookup"><span data-stu-id="2c14e-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="2c14e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c14e-115">PARAMETERS</span></span>

### <span data-ttu-id="2c14e-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="2c14e-116">-AzureToAzure</span></span>
<span data-ttu-id="2c14e-117">{{Fill AzureToAzure Description}}</span><span class="sxs-lookup"><span data-stu-id="2c14e-117">{{Fill AzureToAzure Description}}</span></span>

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

### <span data-ttu-id="2c14e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c14e-118">-DefaultProfile</span></span>
<span data-ttu-id="2c14e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c14e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2c14e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c14e-120">-Name</span></span>
<span data-ttu-id="2c14e-121">Nome del mapping di rete ASR da creare.</span><span class="sxs-lookup"><span data-stu-id="2c14e-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="2c14e-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="2c14e-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="2c14e-123">Specifica l'ID rete virtuale Azure della rete principale per il mapping.</span><span class="sxs-lookup"><span data-stu-id="2c14e-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

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

### <span data-ttu-id="2c14e-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="2c14e-124">-PrimaryFabric</span></span>
<span data-ttu-id="2c14e-125">Specifica il tessuto ASR in cui deve essere creato il mapping.</span><span class="sxs-lookup"><span data-stu-id="2c14e-125">Specifies the ASR fabric where mapping should be created.</span></span>

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

### <span data-ttu-id="2c14e-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="2c14e-126">-PrimaryNetwork</span></span>
<span data-ttu-id="2c14e-127">Specifica l'oggetto di rete principale per il mapping di rete ASR.</span><span class="sxs-lookup"><span data-stu-id="2c14e-127">Specifies the primary network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="2c14e-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="2c14e-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="2c14e-129">Specifica l'ID di rete di Azure recupero per il mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="2c14e-129">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="2c14e-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="2c14e-130">-RecoveryFabric</span></span>
<span data-ttu-id="2c14e-131">Oggetto tessuto di recupero del sito di Azure che corrisponde all'area di ripristino di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c14e-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

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

### <span data-ttu-id="2c14e-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="2c14e-132">-RecoveryNetwork</span></span>
<span data-ttu-id="2c14e-133">Specifica l'oggetto rete di ripristino per il mapping di rete ASR.</span><span class="sxs-lookup"><span data-stu-id="2c14e-133">Specifies the recovery network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="2c14e-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2c14e-134">-Confirm</span></span>
<span data-ttu-id="2c14e-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c14e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c14e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c14e-136">-WhatIf</span></span>
<span data-ttu-id="2c14e-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c14e-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c14e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c14e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c14e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c14e-139">CommonParameters</span></span>
<span data-ttu-id="2c14e-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c14e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c14e-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c14e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c14e-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c14e-142">INPUTS</span></span>

### <span data-ttu-id="2c14e-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="2c14e-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="2c14e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c14e-144">OUTPUTS</span></span>

### <span data-ttu-id="2c14e-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2c14e-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2c14e-146">Note</span><span class="sxs-lookup"><span data-stu-id="2c14e-146">NOTES</span></span>

## <span data-ttu-id="2c14e-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c14e-147">RELATED LINKS</span></span>

[<span data-ttu-id="2c14e-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2c14e-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="2c14e-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2c14e-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
