---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bd8a06eb85658fe2ec06d65c0663550be78d1552
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509188"
---
# <span data-ttu-id="74a2b-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="74a2b-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="74a2b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="74a2b-103">Interrompe/Disabilita la replica per un elemento protetto della replica di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="74a2b-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74a2b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74a2b-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74a2b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74a2b-105">DESCRIPTION</span></span>
<span data-ttu-id="74a2b-106">Il cmdlet **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** Disabilita la replica dell'elemento protetto della replica di ripristino del sito di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="74a2b-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="74a2b-107">Questa operazione causa l'interruzione della replica per l'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="74a2b-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="74a2b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74a2b-108">EXAMPLES</span></span>

### <span data-ttu-id="74a2b-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="74a2b-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="74a2b-110">Avvia l'operazione di disabilitazione della replica per l'elemento protetto della replica specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="74a2b-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="74a2b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74a2b-111">PARAMETERS</span></span>

### <span data-ttu-id="74a2b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a2b-112">-DefaultProfile</span></span>
<span data-ttu-id="74a2b-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74a2b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="74a2b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="74a2b-114">-Force</span></span>
<span data-ttu-id="74a2b-115">Forzare l'esecuzione del comando senza fornire un altro avviso.</span><span class="sxs-lookup"><span data-stu-id="74a2b-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="74a2b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74a2b-116">-InputObject</span></span>
<span data-ttu-id="74a2b-117">L'oggetto di input per il cmdlet: l'oggetto elemento protetto della replica ASR che corrisponde all'elemento protetto della replica per cui deve essere disabilitata la replica.</span><span class="sxs-lookup"><span data-stu-id="74a2b-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74a2b-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="74a2b-118">-WaitForCompletion</span></span>
<span data-ttu-id="74a2b-119">Indica che il cmdlet deve attendere il completamento dell'operazione prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="74a2b-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="74a2b-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="74a2b-120">-Confirm</span></span>
<span data-ttu-id="74a2b-121">Specificare se è necessaria la conferma.</span><span class="sxs-lookup"><span data-stu-id="74a2b-121">Specify if confirmation is required.</span></span> <span data-ttu-id="74a2b-122">Impostare il valore del parametro Confirm su $false per ignorare la conferma.</span><span class="sxs-lookup"><span data-stu-id="74a2b-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="74a2b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74a2b-123">-WhatIf</span></span>
<span data-ttu-id="74a2b-124">Mostra cosa succede se il cmdlet viene eseguito senza eseguire effettivamente il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74a2b-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="74a2b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a2b-125">CommonParameters</span></span>
<span data-ttu-id="74a2b-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74a2b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a2b-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74a2b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a2b-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74a2b-128">INPUTS</span></span>

### <span data-ttu-id="74a2b-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="74a2b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="74a2b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74a2b-130">OUTPUTS</span></span>

### <span data-ttu-id="74a2b-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="74a2b-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="74a2b-132">Note</span><span class="sxs-lookup"><span data-stu-id="74a2b-132">NOTES</span></span>

## <span data-ttu-id="74a2b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74a2b-133">RELATED LINKS</span></span>

[<span data-ttu-id="74a2b-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="74a2b-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="74a2b-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="74a2b-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="74a2b-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="74a2b-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
