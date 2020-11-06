---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: be16ff2145a4442861fd985dfbb55da63f010e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509671"
---
# <span data-ttu-id="3c728-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="3c728-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="3c728-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c728-102">SYNOPSIS</span></span>
<span data-ttu-id="3c728-103">Cambiare la replica da un server processo a un altro per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="3c728-103">Switch replication from one Process server to another for load balancing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c728-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c728-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric>
 -SourceProcessServer <ASRProcessServer> -TargetProcessServer <ASRProcessServer>
 [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c728-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c728-105">DESCRIPTION</span></span>
<span data-ttu-id="3c728-106">**Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** commuta lo spostamento dei dati di replica per le macchine virtuali specificate o un server di processo specificato nel server di processo di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="3c728-106">The **Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="3c728-107">Usato per il bilanciamento del carico o la replica di commutazione tra i server di processo.</span><span class="sxs-lookup"><span data-stu-id="3c728-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="3c728-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c728-108">EXAMPLES</span></span>

### <span data-ttu-id="3c728-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3c728-109">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="3c728-110">Processo per tenere traccia del passaggio del server di processo per tutti gli elementi protetti dalla replica dall'origine al server dei processi di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3c728-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="3c728-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3c728-111">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="3c728-112">Processo per tenere traccia del server di processo di commutazione per l'elemento protetto della replica passato dall'origine al server dei processi di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3c728-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="3c728-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c728-113">PARAMETERS</span></span>

### <span data-ttu-id="3c728-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3c728-114">-Confirm</span></span>
<span data-ttu-id="3c728-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c728-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c728-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c728-116">-DefaultProfile</span></span>
<span data-ttu-id="3c728-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c728-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c728-118">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="3c728-118">-Fabric</span></span>
<span data-ttu-id="3c728-119">Tessuto di ripristino del sito corrispondente al server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="3c728-119">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c728-120">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3c728-120">-ReplicationProtectedItem</span></span>
<span data-ttu-id="3c728-121">Elenco di elementi protetti da replica di cui è possibile cambiare il server di processo.</span><span class="sxs-lookup"><span data-stu-id="3c728-121">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c728-122">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="3c728-122">-SourceProcessServer</span></span>
<span data-ttu-id="3c728-123">Il server di processo per disattivare la replica.</span><span class="sxs-lookup"><span data-stu-id="3c728-123">The Process server to switch replication out from.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c728-124">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="3c728-124">-TargetProcessServer</span></span>
<span data-ttu-id="3c728-125">Il server di processo per cambiare la replica.</span><span class="sxs-lookup"><span data-stu-id="3c728-125">The Process server to switch replication to.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c728-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c728-126">-WhatIf</span></span>
<span data-ttu-id="3c728-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c728-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c728-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c728-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c728-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c728-129">CommonParameters</span></span>
<span data-ttu-id="3c728-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c728-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c728-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c728-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c728-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c728-132">INPUTS</span></span>

### <span data-ttu-id="3c728-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3c728-133">None</span></span>

## <span data-ttu-id="3c728-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c728-134">OUTPUTS</span></span>

### <span data-ttu-id="3c728-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3c728-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3c728-136">Note</span><span class="sxs-lookup"><span data-stu-id="3c728-136">NOTES</span></span>

## <span data-ttu-id="3c728-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c728-137">RELATED LINKS</span></span>
