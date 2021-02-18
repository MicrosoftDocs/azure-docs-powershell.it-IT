---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8dcab2bcaeafbc5304de72b8bcf539a6f4a53934
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206186"
---
# <span data-ttu-id="2e8f0-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2e8f0-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="2e8f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e8f0-102">SYNOPSIS</span></span>
<span data-ttu-id="2e8f0-103">Elimina il mapping di classificazione di archiviazione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="2e8f0-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="2e8f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e8f0-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e8f0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2e8f0-105">DESCRIPTION</span></span>
<span data-ttu-id="2e8f0-106">Il cmdlet **Remove-AzRecoveryServicesAsrStorageClassificationMapping** elimina il mapping della classificazione di archiviazione di Azure Site Recovery specificato.</span><span class="sxs-lookup"><span data-stu-id="2e8f0-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="2e8f0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e8f0-107">EXAMPLES</span></span>

### <span data-ttu-id="2e8f0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2e8f0-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="2e8f0-109">Avvia l'eliminazione del mapping della classificazione di archiviazione specificata e restituisce il processo a matrice usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2e8f0-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2e8f0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e8f0-110">PARAMETERS</span></span>

### <span data-ttu-id="2e8f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e8f0-111">-DefaultProfile</span></span>
<span data-ttu-id="2e8f0-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8f0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2e8f0-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e8f0-113">-InputObject</span></span>
<span data-ttu-id="2e8f0-114">Oggetto di input per il cmdlet: oggetto di mapping della classificazione di archiviazione ASR corrispondente al mapping della classificazione di archiviazione ASR da eliminare.</span><span class="sxs-lookup"><span data-stu-id="2e8f0-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="2e8f0-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e8f0-115">-Confirm</span></span>
<span data-ttu-id="2e8f0-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e8f0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e8f0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e8f0-117">-WhatIf</span></span>
<span data-ttu-id="2e8f0-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e8f0-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e8f0-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e8f0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e8f0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e8f0-120">CommonParameters</span></span>
<span data-ttu-id="2e8f0-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e8f0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e8f0-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e8f0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e8f0-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="2e8f0-123">INPUTS</span></span>

### <span data-ttu-id="2e8f0-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2e8f0-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="2e8f0-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e8f0-125">OUTPUTS</span></span>

### <span data-ttu-id="2e8f0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="2e8f0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2e8f0-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="2e8f0-127">NOTES</span></span>

## <span data-ttu-id="2e8f0-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e8f0-128">RELATED LINKS</span></span>

[<span data-ttu-id="2e8f0-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2e8f0-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="2e8f0-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2e8f0-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
