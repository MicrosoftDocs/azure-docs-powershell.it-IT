---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: b19808ff7b5576c93bc81414d665e23086e524d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953134"
---
# <span data-ttu-id="8b56f-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8b56f-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="8b56f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b56f-102">SYNOPSIS</span></span>
<span data-ttu-id="8b56f-103">Elimina il mapping di classificazione di archiviazione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="8b56f-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="8b56f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b56f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b56f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8b56f-105">DESCRIPTION</span></span>
<span data-ttu-id="8b56f-106">Il cmdlet **Remove-AzRecoveryServicesAsrStorageClassificationMapping** elimina il mapping della classificazione di archiviazione di Azure Site Recovery specificato.</span><span class="sxs-lookup"><span data-stu-id="8b56f-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="8b56f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b56f-107">EXAMPLES</span></span>

### <span data-ttu-id="8b56f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8b56f-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="8b56f-109">Avvia l'eliminazione del mapping della classificazione di archiviazione specificata e restituisce il processo a matrice usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8b56f-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8b56f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b56f-110">PARAMETERS</span></span>

### <span data-ttu-id="8b56f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b56f-111">-DefaultProfile</span></span>
<span data-ttu-id="8b56f-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b56f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8b56f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b56f-113">-InputObject</span></span>
<span data-ttu-id="8b56f-114">Oggetto di input per il cmdlet: oggetto di mapping della classificazione di archiviazione ASR corrispondente al mapping della classificazione di archiviazione ASR da eliminare.</span><span class="sxs-lookup"><span data-stu-id="8b56f-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b56f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b56f-115">-Confirm</span></span>
<span data-ttu-id="8b56f-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b56f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b56f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b56f-117">-WhatIf</span></span>
<span data-ttu-id="8b56f-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b56f-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b56f-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b56f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b56f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b56f-120">CommonParameters</span></span>
<span data-ttu-id="8b56f-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b56f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b56f-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8b56f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b56f-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="8b56f-123">INPUTS</span></span>

### <span data-ttu-id="8b56f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8b56f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="8b56f-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b56f-125">OUTPUTS</span></span>

### <span data-ttu-id="8b56f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="8b56f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8b56f-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="8b56f-127">NOTES</span></span>

## <span data-ttu-id="8b56f-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b56f-128">RELATED LINKS</span></span>

[<span data-ttu-id="8b56f-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8b56f-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="8b56f-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8b56f-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
