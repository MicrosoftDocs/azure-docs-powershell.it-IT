---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: e1d5dd0c8548b52fde37044d304269358a11af70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687677"
---
# <span data-ttu-id="fbdb3-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fbdb3-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="fbdb3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbdb3-102">SYNOPSIS</span></span>
<span data-ttu-id="fbdb3-103">Rimuove un elemento protetto della replica di ripristino di Azure sito.</span><span class="sxs-lookup"><span data-stu-id="fbdb3-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbdb3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbdb3-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbdb3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbdb3-105">DESCRIPTION</span></span>
<span data-ttu-id="fbdb3-106">Il cmdlet **Remove-AzureRmSiteRecoveryReplicationProtectedItem** rimuove un elemento protetto della replica di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="fbdb3-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="fbdb3-107">Questa operazione causa l'interruzione della replica per l'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="fbdb3-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="fbdb3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbdb3-108">EXAMPLES</span></span>

## <span data-ttu-id="fbdb3-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbdb3-109">PARAMETERS</span></span>

### <span data-ttu-id="fbdb3-110">-Force</span><span class="sxs-lookup"><span data-stu-id="fbdb3-110">-Force</span></span>
<span data-ttu-id="fbdb3-111">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fbdb3-111">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbdb3-112">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fbdb3-112">-ReplicationProtectedItem</span></span>
<span data-ttu-id="fbdb3-113">Specifica l'oggetto elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="fbdb3-113">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbdb3-114">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="fbdb3-114">-WaitForCompletion</span></span>
<span data-ttu-id="fbdb3-115">Indica che il cmdlet attende il completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fbdb3-115">Indicates that the cmdlet waits for the operation to complete.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbdb3-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fbdb3-116">-Confirm</span></span>
<span data-ttu-id="fbdb3-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbdb3-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbdb3-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbdb3-118">-WhatIf</span></span>
<span data-ttu-id="fbdb3-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbdb3-119">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="fbdb3-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbdb3-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbdb3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbdb3-121">-DefaultProfile</span></span>
<span data-ttu-id="fbdb3-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbdb3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbdb3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbdb3-123">CommonParameters</span></span>
<span data-ttu-id="fbdb3-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbdb3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbdb3-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbdb3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbdb3-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbdb3-126">INPUTS</span></span>

### <span data-ttu-id="fbdb3-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fbdb3-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="fbdb3-128">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fbdb3-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="fbdb3-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbdb3-129">OUTPUTS</span></span>

### <span data-ttu-id="fbdb3-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fbdb3-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fbdb3-131">Note</span><span class="sxs-lookup"><span data-stu-id="fbdb3-131">NOTES</span></span>

## <span data-ttu-id="fbdb3-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbdb3-132">RELATED LINKS</span></span>

[<span data-ttu-id="fbdb3-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fbdb3-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="fbdb3-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fbdb3-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="fbdb3-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fbdb3-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
