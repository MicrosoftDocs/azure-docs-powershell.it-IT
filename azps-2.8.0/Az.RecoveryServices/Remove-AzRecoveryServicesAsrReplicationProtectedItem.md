---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 19a10312046a4c52ed1fad29732347f719065b95
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856646"
---
# <span data-ttu-id="3e761-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3e761-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="3e761-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e761-102">SYNOPSIS</span></span>
<span data-ttu-id="3e761-103">Interrompe/Disabilita la replica per un elemento protetto della replica di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="3e761-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="3e761-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e761-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e761-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e761-105">DESCRIPTION</span></span>
<span data-ttu-id="3e761-106">Il cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItem** Disabilita la replica dell'elemento protetto della replica di ripristino del sito di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="3e761-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="3e761-107">Questa operazione causa l'interruzione della replica per l'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="3e761-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="3e761-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e761-108">EXAMPLES</span></span>

### <span data-ttu-id="3e761-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e761-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="3e761-110">Avvia l'operazione di disabilitazione della replica per l'elemento protetto della replica specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3e761-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3e761-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e761-111">PARAMETERS</span></span>

### <span data-ttu-id="3e761-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e761-112">-DefaultProfile</span></span>
<span data-ttu-id="3e761-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e761-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3e761-114">-Force</span><span class="sxs-lookup"><span data-stu-id="3e761-114">-Force</span></span>
<span data-ttu-id="3e761-115">Forzare l'esecuzione del comando senza fornire un altro avviso.</span><span class="sxs-lookup"><span data-stu-id="3e761-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="3e761-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e761-116">-InputObject</span></span>
<span data-ttu-id="3e761-117">L'oggetto di input per il cmdlet: l'oggetto elemento protetto della replica ASR che corrisponde all'elemento protetto della replica per cui deve essere disabilitata la replica.</span><span class="sxs-lookup"><span data-stu-id="3e761-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="3e761-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="3e761-118">-WaitForCompletion</span></span>
<span data-ttu-id="3e761-119">Indica che il cmdlet deve attendere il completamento dell'operazione prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="3e761-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="3e761-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e761-120">-Confirm</span></span>
<span data-ttu-id="3e761-121">Specificare se è necessaria la conferma.</span><span class="sxs-lookup"><span data-stu-id="3e761-121">Specify if confirmation is required.</span></span> <span data-ttu-id="3e761-122">Impostare il valore del parametro Confirm su $false per ignorare la conferma.</span><span class="sxs-lookup"><span data-stu-id="3e761-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="3e761-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e761-123">-WhatIf</span></span>
<span data-ttu-id="3e761-124">Mostra cosa succede se il cmdlet viene eseguito senza eseguire effettivamente il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e761-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="3e761-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e761-125">CommonParameters</span></span>
<span data-ttu-id="3e761-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e761-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e761-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e761-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e761-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e761-128">INPUTS</span></span>

### <span data-ttu-id="3e761-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3e761-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="3e761-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e761-130">OUTPUTS</span></span>

### <span data-ttu-id="3e761-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3e761-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3e761-132">Note</span><span class="sxs-lookup"><span data-stu-id="3e761-132">NOTES</span></span>

## <span data-ttu-id="3e761-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e761-133">RELATED LINKS</span></span>

[<span data-ttu-id="3e761-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3e761-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="3e761-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3e761-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="3e761-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3e761-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
