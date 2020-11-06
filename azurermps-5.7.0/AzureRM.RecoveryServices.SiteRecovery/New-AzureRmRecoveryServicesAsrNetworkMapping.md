---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: a989b93b2c2ac2a1c292b736275da5cb91c7042d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518047"
---
# <span data-ttu-id="5bb53-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5bb53-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="5bb53-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5bb53-102">SYNOPSIS</span></span>
<span data-ttu-id="5bb53-103">Crea un mapping di rete ASR tra due reti.</span><span class="sxs-lookup"><span data-stu-id="5bb53-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bb53-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5bb53-104">SYNTAX</span></span>

### <span data-ttu-id="5bb53-105">EnterpriseToEnterprise (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5bb53-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bb53-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="5bb53-106">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bb53-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="5bb53-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bb53-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bb53-108">DESCRIPTION</span></span>
<span data-ttu-id="5bb53-109">Il cmdlet **New-AzureRmRecoveryServicesAsrNetworkMapping** avvia l'operazione di creazione di un mapping di rete ASR tra due reti e restituisce l'oggetto processo ASR per il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5bb53-109">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5bb53-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5bb53-110">EXAMPLES</span></span>

### <span data-ttu-id="5bb53-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5bb53-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="5bb53-112">Avvia l'operazione di creazione del mapping di rete con il nome specificato, le reti primarie e di ripristino e restituisce un processo ASR per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5bb53-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="5bb53-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5bb53-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="5bb53-114">Avvia il mapping di rete per l'operazione di creazione usando il nome specificato, le reti primarie e di ripristino e restituisce un processo ASR per tenere traccia dell'operazione (scenario di Azure in Azure).</span><span class="sxs-lookup"><span data-stu-id="5bb53-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="5bb53-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5bb53-115">PARAMETERS</span></span>

### <span data-ttu-id="5bb53-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="5bb53-116">-AzureToAzure</span></span>
<span data-ttu-id="5bb53-117">Parametro switch che specifica che il mapping di rete da creare verrà usato per la replica di macchine virtuali di Azure tra due aree di Azure.</span><span class="sxs-lookup"><span data-stu-id="5bb53-117">Switch parameter specifying that the network mapping being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb53-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5bb53-118">-Confirm</span></span>
<span data-ttu-id="5bb53-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bb53-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bb53-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bb53-120">-DefaultProfile</span></span>
<span data-ttu-id="5bb53-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5bb53-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb53-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5bb53-122">-Name</span></span>
<span data-ttu-id="5bb53-123">Nome del mapping di rete ASR da creare.</span><span class="sxs-lookup"><span data-stu-id="5bb53-123">Name of the ASR network mapping to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb53-124">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="5bb53-124">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="5bb53-125">Specifica l'ID rete virtuale Azure della rete principale per il mapping.</span><span class="sxs-lookup"><span data-stu-id="5bb53-125">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb53-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="5bb53-126">-PrimaryFabric</span></span>
<span data-ttu-id="5bb53-127">Specifica il tessuto ASR in cui deve essere creato il mapping.</span><span class="sxs-lookup"><span data-stu-id="5bb53-127">Specifes the ASR fabric where mapping should be created.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb53-128">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="5bb53-128">-PrimaryNetwork</span></span>
<span data-ttu-id="5bb53-129">Specifica l'oggetto di rete principale per il mapping di rete ASR.</span><span class="sxs-lookup"><span data-stu-id="5bb53-129">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb53-130">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="5bb53-130">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="5bb53-131">Specifica l'ID di rete di Azure recupero per il mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="5bb53-131">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb53-132">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="5bb53-132">-RecoveryFabric</span></span>
<span data-ttu-id="5bb53-133">Oggetto tessuto di recupero del sito di Azure che corrisponde all'area di ripristino di Azure.</span><span class="sxs-lookup"><span data-stu-id="5bb53-133">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb53-134">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="5bb53-134">-RecoveryNetwork</span></span>
<span data-ttu-id="5bb53-135">Specifica l'oggetto rete di ripristino per il mapping di rete ASR.</span><span class="sxs-lookup"><span data-stu-id="5bb53-135">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb53-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bb53-136">-WhatIf</span></span>
<span data-ttu-id="5bb53-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5bb53-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bb53-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5bb53-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bb53-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bb53-139">CommonParameters</span></span>
<span data-ttu-id="5bb53-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bb53-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bb53-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bb53-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bb53-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5bb53-142">INPUTS</span></span>

### <span data-ttu-id="5bb53-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="5bb53-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="5bb53-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5bb53-144">OUTPUTS</span></span>

### <span data-ttu-id="5bb53-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5bb53-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5bb53-146">Note</span><span class="sxs-lookup"><span data-stu-id="5bb53-146">NOTES</span></span>

## <span data-ttu-id="5bb53-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5bb53-147">RELATED LINKS</span></span>

[<span data-ttu-id="5bb53-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5bb53-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="5bb53-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="5bb53-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
