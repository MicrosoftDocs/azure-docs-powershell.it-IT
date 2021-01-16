---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333331"
---
# <span data-ttu-id="d23c5-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="d23c5-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="d23c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d23c5-102">SYNOPSIS</span></span>
<span data-ttu-id="d23c5-103">Aggiungere il disco per la protezione per la macchina virtuale di Azure già protetta.</span><span class="sxs-lookup"><span data-stu-id="d23c5-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="d23c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d23c5-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d23c5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d23c5-105">DESCRIPTION</span></span>
<span data-ttu-id="d23c5-106">Il cmdlet **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** aggiunge il disco per la protezione per la macchina virtuale Azure già protetta.</span><span class="sxs-lookup"><span data-stu-id="d23c5-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="d23c5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d23c5-107">EXAMPLES</span></span>

### <span data-ttu-id="d23c5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d23c5-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="d23c5-109">Avviare l'operazione per aggiungere la configurazione del disco specificata per la protezione.</span><span class="sxs-lookup"><span data-stu-id="d23c5-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="d23c5-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d23c5-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="d23c5-111">Avviare l'operazione per aggiungere la configurazione del disco specificata per la protezione. Elemento protetto per la replica di input piping.</span><span class="sxs-lookup"><span data-stu-id="d23c5-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="d23c5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d23c5-112">PARAMETERS</span></span>

### <span data-ttu-id="d23c5-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="d23c5-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="d23c5-114">Specifica la configurazione del disco usata per la protezione del disco per lo scenario di ripristino di emergenza di Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="d23c5-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d23c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d23c5-115">-DefaultProfile</span></span>
<span data-ttu-id="d23c5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d23c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d23c5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d23c5-117">-InputObject</span></span>
<span data-ttu-id="d23c5-118">L'oggetto di input per il cmdlet: l'oggetto elemento protetto della replica ASR che corrisponde al nuovo disco che deve essere protetto.</span><span class="sxs-lookup"><span data-stu-id="d23c5-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

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

### <span data-ttu-id="d23c5-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="d23c5-119">-WaitForCompletion</span></span>
<span data-ttu-id="d23c5-120">Attendere il completamento</span><span class="sxs-lookup"><span data-stu-id="d23c5-120">Wait For Completion</span></span>

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

### <span data-ttu-id="d23c5-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d23c5-121">-Confirm</span></span>
<span data-ttu-id="d23c5-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d23c5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d23c5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d23c5-123">-WhatIf</span></span>
<span data-ttu-id="d23c5-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d23c5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d23c5-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d23c5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d23c5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d23c5-126">CommonParameters</span></span>
<span data-ttu-id="d23c5-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d23c5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d23c5-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d23c5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d23c5-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d23c5-129">INPUTS</span></span>

### <span data-ttu-id="d23c5-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d23c5-130">None</span></span>

## <span data-ttu-id="d23c5-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d23c5-131">OUTPUTS</span></span>

### <span data-ttu-id="d23c5-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d23c5-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d23c5-133">Note</span><span class="sxs-lookup"><span data-stu-id="d23c5-133">NOTES</span></span>

## <span data-ttu-id="d23c5-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d23c5-134">RELATED LINKS</span></span>
