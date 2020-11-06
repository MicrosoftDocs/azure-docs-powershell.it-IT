---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: de9e07da334e252db4af87819d2719b5251b576c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508035"
---
# <span data-ttu-id="e1df2-101">Update-AzureRmRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="e1df2-101">Update-AzureRmRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="e1df2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1df2-102">SYNOPSIS</span></span>
<span data-ttu-id="e1df2-103">Spingere gli aggiornamenti degli agenti del servizio mobilità in computer protetti.</span><span class="sxs-lookup"><span data-stu-id="e1df2-103">Push mobility service agent updates to protected machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1df2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1df2-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1df2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1df2-105">DESCRIPTION</span></span>
<span data-ttu-id="e1df2-106">Il cmdlet **Update-AzureRmRecoveryServicesAsrMobilityService** cerca di spingere gli aggiornamenti degli agenti del servizio di mobilità in computer protetti (se è disponibile un aggiornamento).</span><span class="sxs-lookup"><span data-stu-id="e1df2-106">The **Update-AzureRmRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="e1df2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1df2-107">EXAMPLES</span></span>

### <span data-ttu-id="e1df2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e1df2-108">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="e1df2-109">Processo per tenere traccia dell'agente di servizio Moblility dell'elemento Protected Update Replication.</span><span class="sxs-lookup"><span data-stu-id="e1df2-109">Job to track Update Replication Protected Item's Moblility Service Agent.</span></span>

## <span data-ttu-id="e1df2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1df2-110">PARAMETERS</span></span>

### <span data-ttu-id="e1df2-111">-Account</span><span class="sxs-lookup"><span data-stu-id="e1df2-111">-Account</span></span>
<span data-ttu-id="e1df2-112">ID account RunAs da usare per spingere l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e1df2-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="e1df2-113">Deve essere uno dall'elenco di account RunAs nel tessuto ASR corrispondente al computer da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="e1df2-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1df2-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e1df2-114">-Confirm</span></span>
<span data-ttu-id="e1df2-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1df2-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1df2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1df2-116">-DefaultProfile</span></span>
<span data-ttu-id="e1df2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1df2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1df2-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e1df2-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e1df2-119">Elemento protetto della replica del ripristino del sito di Azure da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="e1df2-119">Azure Site Recovery replication protected item to be updated.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1df2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1df2-120">-WhatIf</span></span>
<span data-ttu-id="e1df2-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1df2-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1df2-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1df2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1df2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1df2-123">CommonParameters</span></span>
<span data-ttu-id="e1df2-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1df2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1df2-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1df2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1df2-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1df2-126">INPUTS</span></span>

### <span data-ttu-id="e1df2-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e1df2-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e1df2-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1df2-128">OUTPUTS</span></span>

### <span data-ttu-id="e1df2-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e1df2-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e1df2-130">Note</span><span class="sxs-lookup"><span data-stu-id="e1df2-130">NOTES</span></span>

## <span data-ttu-id="e1df2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1df2-131">RELATED LINKS</span></span>
