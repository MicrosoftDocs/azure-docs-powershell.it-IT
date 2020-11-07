---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: a341e634c9c426843b5eb217c2f13102abc30ae4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855758"
---
# <span data-ttu-id="aac77-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="aac77-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="aac77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aac77-102">SYNOPSIS</span></span>
<span data-ttu-id="aac77-103">Ottiene i mapping di classificazione di archiviazione ASR.</span><span class="sxs-lookup"><span data-stu-id="aac77-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="aac77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aac77-104">SYNTAX</span></span>

### <span data-ttu-id="aac77-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aac77-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aac77-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="aac77-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aac77-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aac77-107">DESCRIPTION</span></span>
<span data-ttu-id="aac77-108">Il cmdlet **Get-AzRecoveryServicesAsrStorageClassificationMapping** ottiene i dettagli di un mapping della classificazione di archiviazione ASR.</span><span class="sxs-lookup"><span data-stu-id="aac77-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="aac77-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aac77-109">EXAMPLES</span></span>

### <span data-ttu-id="aac77-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aac77-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="aac77-111">Elenca tutti i mapping di classificazione dello spazio di archiviazione corrispondenti alla classificazione di archiviazione specificata.</span><span class="sxs-lookup"><span data-stu-id="aac77-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="aac77-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aac77-112">PARAMETERS</span></span>

### <span data-ttu-id="aac77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac77-113">-DefaultProfile</span></span>
<span data-ttu-id="aac77-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aac77-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="aac77-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="aac77-115">-Name</span></span>
<span data-ttu-id="aac77-116">Specifica il nome del mapping di classificazione dello spazio di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="aac77-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="aac77-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="aac77-117">-StorageClassification</span></span>
<span data-ttu-id="aac77-118">Specifica un oggetto di classificazione dello spazio di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="aac77-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="aac77-119">Il cmdlet ottiene i mapping di classificazione di archiviazione ASR corrispondenti alla classificazione di archiviazione specificata</span><span class="sxs-lookup"><span data-stu-id="aac77-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="aac77-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac77-120">CommonParameters</span></span>
<span data-ttu-id="aac77-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aac77-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac77-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aac77-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac77-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aac77-123">INPUTS</span></span>

### <span data-ttu-id="aac77-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="aac77-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="aac77-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aac77-125">OUTPUTS</span></span>

### <span data-ttu-id="aac77-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="aac77-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="aac77-127">Note</span><span class="sxs-lookup"><span data-stu-id="aac77-127">NOTES</span></span>

## <span data-ttu-id="aac77-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aac77-128">RELATED LINKS</span></span>

[<span data-ttu-id="aac77-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="aac77-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="aac77-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="aac77-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
