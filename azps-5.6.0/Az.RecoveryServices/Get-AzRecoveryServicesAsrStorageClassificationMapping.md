---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c5dea86066fd2b7bc6bd3b2bd3eb7ac94f401895
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963806"
---
# <span data-ttu-id="36143-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="36143-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="36143-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36143-102">SYNOPSIS</span></span>
<span data-ttu-id="36143-103">Ottiene i mapping di classificazione di archiviazione ASR.</span><span class="sxs-lookup"><span data-stu-id="36143-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="36143-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36143-104">SYNTAX</span></span>

### <span data-ttu-id="36143-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36143-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36143-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="36143-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36143-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="36143-107">DESCRIPTION</span></span>
<span data-ttu-id="36143-108">Il cmdlet **Get-AzRecoveryServicesAsrStorageClassificationMapping** ottiene i dettagli di un mapping di classificazione di archiviazione ASR.</span><span class="sxs-lookup"><span data-stu-id="36143-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="36143-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36143-109">EXAMPLES</span></span>

### <span data-ttu-id="36143-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="36143-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="36143-111">Elencare tutti i mapping di classificazione di archiviazione corrispondenti alla classificazione di archiviazione specificata.</span><span class="sxs-lookup"><span data-stu-id="36143-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="36143-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36143-112">PARAMETERS</span></span>

### <span data-ttu-id="36143-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36143-113">-DefaultProfile</span></span>
<span data-ttu-id="36143-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36143-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="36143-115">-Name</span><span class="sxs-lookup"><span data-stu-id="36143-115">-Name</span></span>
<span data-ttu-id="36143-116">Specifica il nome del mapping della classificazione di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="36143-116">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36143-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="36143-117">-StorageClassification</span></span>
<span data-ttu-id="36143-118">Specifica un oggetto classificazione di archiviazione ASR.</span><span class="sxs-lookup"><span data-stu-id="36143-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="36143-119">Il cmdlet ottiene i mapping della classificazione di archiviazione ASR corrispondenti alla classificazione di archiviazione specificata</span><span class="sxs-lookup"><span data-stu-id="36143-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36143-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36143-120">CommonParameters</span></span>
<span data-ttu-id="36143-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36143-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36143-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36143-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36143-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="36143-123">INPUTS</span></span>

### <span data-ttu-id="36143-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="36143-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="36143-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36143-125">OUTPUTS</span></span>

### <span data-ttu-id="36143-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="36143-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="36143-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="36143-127">NOTES</span></span>

## <span data-ttu-id="36143-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36143-128">RELATED LINKS</span></span>

[<span data-ttu-id="36143-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="36143-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="36143-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="36143-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
