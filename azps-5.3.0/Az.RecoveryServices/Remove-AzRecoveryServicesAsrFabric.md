---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 095759ca2753cac4f7155430a241e0554e910fd6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475738"
---
# <span data-ttu-id="e0b09-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="e0b09-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="e0b09-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0b09-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b09-103">Elimina il tessuto di ripristino del sito di Azure specificato dall'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e0b09-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="e0b09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0b09-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0b09-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0b09-105">DESCRIPTION</span></span>
<span data-ttu-id="e0b09-106">Il cmdlet **Remove-AzRecoveryServicesAsrFabric** rimuove il tessuto di ripristino del sito di Azure specificato dall'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e0b09-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="e0b09-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0b09-107">EXAMPLES</span></span>

### <span data-ttu-id="e0b09-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e0b09-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="e0b09-109">Avvia l'eliminazione di tessuto specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e0b09-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e0b09-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0b09-110">PARAMETERS</span></span>

### <span data-ttu-id="e0b09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b09-111">-DefaultProfile</span></span>
<span data-ttu-id="e0b09-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0b09-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e0b09-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e0b09-113">-Force</span></span>
<span data-ttu-id="e0b09-114">Forzare l'esecuzione del comando senza fornire un altro avviso.</span><span class="sxs-lookup"><span data-stu-id="e0b09-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="e0b09-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0b09-115">-InputObject</span></span>
<span data-ttu-id="e0b09-116">L'oggetto di input per il cmdlet: l'oggetto tessuto ASR corrispondente al tessuto da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e0b09-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b09-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e0b09-117">-Confirm</span></span>
<span data-ttu-id="e0b09-118">Specificare se è necessaria la conferma.</span><span class="sxs-lookup"><span data-stu-id="e0b09-118">Specify if confirmation is required.</span></span> <span data-ttu-id="e0b09-119">Impostare il valore del parametro Confirm su $false per ignorare la conferma.</span><span class="sxs-lookup"><span data-stu-id="e0b09-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="e0b09-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0b09-120">-WhatIf</span></span>
<span data-ttu-id="e0b09-121">Mostra cosa succede se il cmdlet viene eseguito senza eseguire effettivamente il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0b09-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="e0b09-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b09-122">CommonParameters</span></span>
<span data-ttu-id="e0b09-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b09-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b09-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0b09-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b09-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0b09-125">INPUTS</span></span>

### <span data-ttu-id="e0b09-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e0b09-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e0b09-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0b09-127">OUTPUTS</span></span>

### <span data-ttu-id="e0b09-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e0b09-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e0b09-129">Note</span><span class="sxs-lookup"><span data-stu-id="e0b09-129">NOTES</span></span>

## <span data-ttu-id="e0b09-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0b09-130">RELATED LINKS</span></span>

[<span data-ttu-id="e0b09-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="e0b09-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="e0b09-132">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="e0b09-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
