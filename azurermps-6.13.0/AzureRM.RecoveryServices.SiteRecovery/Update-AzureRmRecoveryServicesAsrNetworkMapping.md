---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: fb92ec38bcbe7addb23f274616cde0fd84ebbafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509144"
---
# <span data-ttu-id="9303d-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9303d-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="9303d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9303d-102">SYNOPSIS</span></span>
<span data-ttu-id="9303d-103">Aggiorna il mapping della rete di ripristino del sito Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="9303d-103">Updates the specified azure site recovery network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9303d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9303d-104">SYNTAX</span></span>

### <span data-ttu-id="9303d-105">ByNetworkObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9303d-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9303d-106">ById</span><span class="sxs-lookup"><span data-stu-id="9303d-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9303d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9303d-107">DESCRIPTION</span></span>
<span data-ttu-id="9303d-108">Il cmdlet **Update-AzureRmRecoveryServicesAsrNetworkMapping** aggiorna il mapping di rete di ripristino del sito di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="9303d-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="9303d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9303d-109">EXAMPLES</span></span>

### <span data-ttu-id="9303d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9303d-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="9303d-111">Avvia l'operazione di mapping della rete di aggiornamento usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9303d-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9303d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9303d-112">PARAMETERS</span></span>

### <span data-ttu-id="9303d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9303d-113">-DefaultProfile</span></span>
<span data-ttu-id="9303d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9303d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9303d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9303d-115">-InputObject</span></span>
<span data-ttu-id="9303d-116">Input Object: specifica l'oggetto mapping di rete ASR che corrisponde al mapping di rete ASR da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="9303d-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="9303d-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="9303d-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="9303d-118">Specifica l'ID di rete di Azure recupero per il mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="9303d-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="9303d-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="9303d-119">-RecoveryNetwork</span></span>
<span data-ttu-id="9303d-120">Specifica l'oggetto rete di ripristino per il mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="9303d-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="9303d-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9303d-121">-Confirm</span></span>
<span data-ttu-id="9303d-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9303d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9303d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9303d-123">-WhatIf</span></span>
<span data-ttu-id="9303d-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9303d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9303d-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9303d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9303d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9303d-126">CommonParameters</span></span>
<span data-ttu-id="9303d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9303d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9303d-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9303d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9303d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9303d-129">INPUTS</span></span>

### <span data-ttu-id="9303d-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9303d-130">None</span></span>

## <span data-ttu-id="9303d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9303d-131">OUTPUTS</span></span>

### <span data-ttu-id="9303d-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9303d-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9303d-133">Note</span><span class="sxs-lookup"><span data-stu-id="9303d-133">NOTES</span></span>

## <span data-ttu-id="9303d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9303d-134">RELATED LINKS</span></span>
