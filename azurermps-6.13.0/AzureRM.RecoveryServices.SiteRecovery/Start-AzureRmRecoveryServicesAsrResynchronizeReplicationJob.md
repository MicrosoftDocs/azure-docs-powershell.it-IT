---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 6ee25231b7bb8861a1294537e2f42a0bf914b994
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685562"
---
# <span data-ttu-id="3af1b-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="3af1b-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="3af1b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3af1b-102">SYNOPSIS</span></span>
<span data-ttu-id="3af1b-103">Avvia la risincronizzazione della replica.</span><span class="sxs-lookup"><span data-stu-id="3af1b-103">Starts replication resynchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3af1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3af1b-104">SYNTAX</span></span>

### <span data-ttu-id="3af1b-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3af1b-105">Default (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3af1b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3af1b-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3af1b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3af1b-107">DESCRIPTION</span></span>
<span data-ttu-id="3af1b-108">Il cmdlet **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** avvia la risincronizzazione della replica per l'elemento protetto specificato se protetto è in uno stato obbligatorio di risincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3af1b-108">The **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="3af1b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3af1b-109">EXAMPLES</span></span>

### <span data-ttu-id="3af1b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3af1b-110">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="3af1b-111">Avvia Job per risincronizzare la replica nell'elemento protetto della replica passata.</span><span class="sxs-lookup"><span data-stu-id="3af1b-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="3af1b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3af1b-112">PARAMETERS</span></span>

### <span data-ttu-id="3af1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af1b-113">-DefaultProfile</span></span>
<span data-ttu-id="3af1b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3af1b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3af1b-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3af1b-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="3af1b-116">Elemento protetto da replica ASR per risincronizzare la replica.</span><span class="sxs-lookup"><span data-stu-id="3af1b-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3af1b-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3af1b-117">-ResourceId</span></span>
<span data-ttu-id="3af1b-118">ID risorsa dell'elemento protetto da replica per la risincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3af1b-118">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af1b-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3af1b-119">-Confirm</span></span>
<span data-ttu-id="3af1b-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3af1b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3af1b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3af1b-121">-WhatIf</span></span>
<span data-ttu-id="3af1b-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3af1b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3af1b-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3af1b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3af1b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af1b-124">CommonParameters</span></span>
<span data-ttu-id="3af1b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3af1b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af1b-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3af1b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af1b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3af1b-127">INPUTS</span></span>

### <span data-ttu-id="3af1b-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3af1b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="3af1b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3af1b-129">OUTPUTS</span></span>

### <span data-ttu-id="3af1b-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3af1b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3af1b-131">Note</span><span class="sxs-lookup"><span data-stu-id="3af1b-131">NOTES</span></span>

## <span data-ttu-id="3af1b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3af1b-132">RELATED LINKS</span></span>
