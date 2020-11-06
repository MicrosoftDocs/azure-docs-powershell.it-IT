---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 121d45d626a226542f495cd197781b795823b1fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520341"
---
# <span data-ttu-id="a8675-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a8675-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="a8675-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8675-102">SYNOPSIS</span></span>
<span data-ttu-id="a8675-103">Rimuove un elemento protetto della replica di ripristino di Azure sito.</span><span class="sxs-lookup"><span data-stu-id="a8675-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8675-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8675-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8675-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8675-105">DESCRIPTION</span></span>
<span data-ttu-id="a8675-106">Il cmdlet **Remove-AzureRmSiteRecoveryReplicationProtectedItem** rimuove un elemento protetto della replica di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="a8675-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="a8675-107">Questa operazione causa l'interruzione della replica per l'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="a8675-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="a8675-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8675-108">EXAMPLES</span></span>

## <span data-ttu-id="a8675-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8675-109">PARAMETERS</span></span>

### <span data-ttu-id="a8675-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8675-110">-DefaultProfile</span></span>
<span data-ttu-id="a8675-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8675-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8675-112">-Force</span><span class="sxs-lookup"><span data-stu-id="a8675-112">-Force</span></span>
<span data-ttu-id="a8675-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a8675-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8675-114">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a8675-114">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a8675-115">Specifica l'oggetto elemento protetto da replica.</span><span class="sxs-lookup"><span data-stu-id="a8675-115">Specifies the Replication Protected Item object.</span></span>

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

### <span data-ttu-id="a8675-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a8675-116">-WaitForCompletion</span></span>
<span data-ttu-id="a8675-117">Indica che il cmdlet attende il completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a8675-117">Indicates that the cmdlet waits for the operation to complete.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8675-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8675-118">-Confirm</span></span>
<span data-ttu-id="a8675-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8675-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8675-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8675-120">-WhatIf</span></span>
<span data-ttu-id="a8675-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8675-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a8675-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8675-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8675-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8675-123">CommonParameters</span></span>
<span data-ttu-id="a8675-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8675-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8675-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8675-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8675-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8675-126">INPUTS</span></span>

### <span data-ttu-id="a8675-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a8675-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="a8675-128">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a8675-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="a8675-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8675-129">OUTPUTS</span></span>

### <span data-ttu-id="a8675-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a8675-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a8675-131">Note</span><span class="sxs-lookup"><span data-stu-id="a8675-131">NOTES</span></span>

## <span data-ttu-id="a8675-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8675-132">RELATED LINKS</span></span>

[<span data-ttu-id="a8675-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a8675-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="a8675-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a8675-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="a8675-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a8675-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
