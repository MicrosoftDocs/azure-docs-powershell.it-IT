---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 01AE09A8-B779-475A-9E86-776E0774E89E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: d9a1e26691ab0ea1be04365747f97d8fc6111672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515995"
---
# <span data-ttu-id="1a2bc-101">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1a2bc-101">Get-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="1a2bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="1a2bc-103">Ottiene informazioni sui mapping di rete di ripristino del sito per il Vault corrente.</span><span class="sxs-lookup"><span data-stu-id="1a2bc-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a2bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a2bc-104">SYNTAX</span></span>

### <span data-ttu-id="1a2bc-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a2bc-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a2bc-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="1a2bc-106">EnterpriseToEnterprise</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a2bc-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="1a2bc-107">EnterpriseToAzure</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> [-Azure]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a2bc-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="1a2bc-108">EnterpriseToAzureLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-Azure] -PrimaryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a2bc-109">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="1a2bc-109">EnterpriseToEnterpriseLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a2bc-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a2bc-110">DESCRIPTION</span></span>
<span data-ttu-id="1a2bc-111">Il cmdlet **Get-AzureRmSiteRecoveryNetworkMapping** ottiene le informazioni sui mapping di rete di ripristino dei siti di Azure per il Vault di ripristino del sito corrente.</span><span class="sxs-lookup"><span data-stu-id="1a2bc-111">The **Get-AzureRmSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="1a2bc-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a2bc-112">EXAMPLES</span></span>

## <span data-ttu-id="1a2bc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a2bc-113">PARAMETERS</span></span>

### <span data-ttu-id="1a2bc-114">-Azure</span><span class="sxs-lookup"><span data-stu-id="1a2bc-114">-Azure</span></span>
<span data-ttu-id="1a2bc-115">Indica che il comando ottiene un elenco dei mapping di rete per le reti nel server primario mappato alle reti virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a2bc-115">Indicates that the command gets a list of network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a2bc-116">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="1a2bc-116">-PrimaryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a2bc-117">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="1a2bc-117">-PrimaryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToAzureLegacy, EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a2bc-118">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="1a2bc-118">-RecoveryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a2bc-119">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="1a2bc-119">-RecoveryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a2bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a2bc-120">-DefaultProfile</span></span>
<span data-ttu-id="1a2bc-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a2bc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a2bc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a2bc-122">CommonParameters</span></span>
<span data-ttu-id="1a2bc-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a2bc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a2bc-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a2bc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a2bc-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a2bc-125">INPUTS</span></span>

### <span data-ttu-id="1a2bc-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="1a2bc-126">ASRFabric</span></span>
<span data-ttu-id="1a2bc-127">Il parametro ' PrimaryFabric ' accetta il valore di tipo ' ASRFabric ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1a2bc-127">Parameter 'PrimaryFabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="1a2bc-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="1a2bc-128">ASRServer</span></span>
<span data-ttu-id="1a2bc-129">Il parametro ' PrimaryServer ' accetta il valore di tipo ' ASRServer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1a2bc-129">Parameter 'PrimaryServer' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="1a2bc-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a2bc-130">OUTPUTS</span></span>

### <span data-ttu-id="1a2bc-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetworkMapping]</span><span class="sxs-lookup"><span data-stu-id="1a2bc-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping]</span></span>

## <span data-ttu-id="1a2bc-132">Note</span><span class="sxs-lookup"><span data-stu-id="1a2bc-132">NOTES</span></span>

## <span data-ttu-id="1a2bc-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a2bc-133">RELATED LINKS</span></span>

[<span data-ttu-id="1a2bc-134">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1a2bc-134">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="1a2bc-135">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1a2bc-135">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
