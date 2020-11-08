---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8dcab2bcaeafbc5304de72b8bcf539a6f4a53934
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020582"
---
# <span data-ttu-id="3c157-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3c157-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="3c157-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c157-102">SYNOPSIS</span></span>
<span data-ttu-id="3c157-103">Elimina il mapping della classificazione dello spazio di archiviazione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="3c157-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="3c157-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c157-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c157-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c157-105">DESCRIPTION</span></span>
<span data-ttu-id="3c157-106">Il cmdlet **Remove-AzRecoveryServicesAsrStorageClassificationMapping** Elimina il mapping di classificazione dello spazio di archiviazione del ripristino di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="3c157-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="3c157-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c157-107">EXAMPLES</span></span>

### <span data-ttu-id="3c157-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3c157-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="3c157-109">Avvia l'eliminazione del mapping di classificazione dello spazio di archiviazione specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3c157-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3c157-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c157-110">PARAMETERS</span></span>

### <span data-ttu-id="3c157-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c157-111">-DefaultProfile</span></span>
<span data-ttu-id="3c157-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c157-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3c157-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c157-113">-InputObject</span></span>
<span data-ttu-id="3c157-114">L'oggetto di input per il cmdlet: l'oggetto di mapping della classificazione di archiviazione ASR corrispondente al mapping di classificazione dello spazio di archiviazione ASR da eliminare.</span><span class="sxs-lookup"><span data-stu-id="3c157-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="3c157-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3c157-115">-Confirm</span></span>
<span data-ttu-id="3c157-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c157-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c157-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c157-117">-WhatIf</span></span>
<span data-ttu-id="3c157-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c157-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c157-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c157-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c157-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c157-120">CommonParameters</span></span>
<span data-ttu-id="3c157-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c157-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c157-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c157-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c157-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c157-123">INPUTS</span></span>

### <span data-ttu-id="3c157-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3c157-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="3c157-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c157-125">OUTPUTS</span></span>

### <span data-ttu-id="3c157-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3c157-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3c157-127">Note</span><span class="sxs-lookup"><span data-stu-id="3c157-127">NOTES</span></span>

## <span data-ttu-id="3c157-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c157-128">RELATED LINKS</span></span>

[<span data-ttu-id="3c157-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3c157-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="3c157-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3c157-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
