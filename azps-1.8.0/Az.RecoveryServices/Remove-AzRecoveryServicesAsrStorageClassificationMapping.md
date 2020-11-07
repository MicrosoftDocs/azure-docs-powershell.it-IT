---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c76c2ebf40f360820ec3eef719b33142daacdbac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677586"
---
# <span data-ttu-id="3950b-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3950b-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="3950b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3950b-102">SYNOPSIS</span></span>
<span data-ttu-id="3950b-103">Elimina il mapping della classificazione dello spazio di archiviazione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="3950b-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="3950b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3950b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3950b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3950b-105">DESCRIPTION</span></span>
<span data-ttu-id="3950b-106">Il cmdlet **Remove-AzRecoveryServicesAsrStorageClassificationMapping** Elimina il mapping di classificazione dello spazio di archiviazione del ripristino di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="3950b-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="3950b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3950b-107">EXAMPLES</span></span>

### <span data-ttu-id="3950b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3950b-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="3950b-109">Avvia l'eliminazione del mapping di classificazione dello spazio di archiviazione specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3950b-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3950b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3950b-110">PARAMETERS</span></span>

### <span data-ttu-id="3950b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3950b-111">-DefaultProfile</span></span>
<span data-ttu-id="3950b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3950b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3950b-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3950b-113">-InputObject</span></span>
<span data-ttu-id="3950b-114">L'oggetto di input per il cmdlet: l'oggetto di mapping della classificazione di archiviazione ASR corrispondente al mapping di classificazione dello spazio di archiviazione ASR da eliminare.</span><span class="sxs-lookup"><span data-stu-id="3950b-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="3950b-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3950b-115">-Confirm</span></span>
<span data-ttu-id="3950b-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3950b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3950b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3950b-117">-WhatIf</span></span>
<span data-ttu-id="3950b-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3950b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3950b-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3950b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3950b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3950b-120">CommonParameters</span></span>
<span data-ttu-id="3950b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3950b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3950b-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3950b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3950b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3950b-123">INPUTS</span></span>

### <span data-ttu-id="3950b-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3950b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="3950b-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3950b-125">OUTPUTS</span></span>

### <span data-ttu-id="3950b-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3950b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3950b-127">Note</span><span class="sxs-lookup"><span data-stu-id="3950b-127">NOTES</span></span>

## <span data-ttu-id="3950b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3950b-128">RELATED LINKS</span></span>

[<span data-ttu-id="3950b-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3950b-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="3950b-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="3950b-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
