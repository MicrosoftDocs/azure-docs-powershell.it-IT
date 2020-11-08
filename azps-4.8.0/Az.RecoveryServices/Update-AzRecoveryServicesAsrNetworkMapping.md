---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188964"
---
# <span data-ttu-id="82f2f-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="82f2f-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="82f2f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="82f2f-103">Aggiorna il mapping della rete di ripristino del sito Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="82f2f-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="82f2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82f2f-104">SYNTAX</span></span>

### <span data-ttu-id="82f2f-105">ByNetworkObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82f2f-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82f2f-106">ById</span><span class="sxs-lookup"><span data-stu-id="82f2f-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82f2f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82f2f-107">DESCRIPTION</span></span>
<span data-ttu-id="82f2f-108">Il cmdlet **Update-AzRecoveryServicesAsrNetworkMapping** aggiorna il mapping di rete di ripristino del sito di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="82f2f-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="82f2f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82f2f-109">EXAMPLES</span></span>

### <span data-ttu-id="82f2f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="82f2f-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="82f2f-111">Avvia l'operazione di mapping della rete di aggiornamento usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="82f2f-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="82f2f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82f2f-112">PARAMETERS</span></span>

### <span data-ttu-id="82f2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f2f-113">-DefaultProfile</span></span>
<span data-ttu-id="82f2f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82f2f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="82f2f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82f2f-115">-InputObject</span></span>
<span data-ttu-id="82f2f-116">Input Object: specifica l'oggetto mapping di rete ASR che corrisponde al mapping di rete ASR da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="82f2f-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82f2f-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="82f2f-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="82f2f-118">Specifica l'ID di rete di Azure recupero per il mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="82f2f-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f2f-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="82f2f-119">-RecoveryNetwork</span></span>
<span data-ttu-id="82f2f-120">Specifica l'oggetto rete di ripristino per il mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="82f2f-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f2f-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="82f2f-121">-Confirm</span></span>
<span data-ttu-id="82f2f-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82f2f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82f2f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82f2f-123">-WhatIf</span></span>
<span data-ttu-id="82f2f-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82f2f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82f2f-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82f2f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82f2f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f2f-126">CommonParameters</span></span>
<span data-ttu-id="82f2f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82f2f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f2f-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82f2f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f2f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82f2f-129">INPUTS</span></span>

### <span data-ttu-id="82f2f-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="82f2f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="82f2f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82f2f-131">OUTPUTS</span></span>

### <span data-ttu-id="82f2f-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="82f2f-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="82f2f-133">Note</span><span class="sxs-lookup"><span data-stu-id="82f2f-133">NOTES</span></span>

## <span data-ttu-id="82f2f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82f2f-134">RELATED LINKS</span></span>
