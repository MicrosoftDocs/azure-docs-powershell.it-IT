---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189432"
---
# <span data-ttu-id="2b945-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2b945-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="2b945-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b945-102">SYNOPSIS</span></span>
<span data-ttu-id="2b945-103">Ottiene i mapping di classificazione di archiviazione ASR.</span><span class="sxs-lookup"><span data-stu-id="2b945-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="2b945-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b945-104">SYNTAX</span></span>

### <span data-ttu-id="2b945-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2b945-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b945-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="2b945-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b945-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b945-107">DESCRIPTION</span></span>
<span data-ttu-id="2b945-108">Il cmdlet **Get-AzRecoveryServicesAsrStorageClassificationMapping** ottiene i dettagli di un mapping della classificazione di archiviazione ASR.</span><span class="sxs-lookup"><span data-stu-id="2b945-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="2b945-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b945-109">EXAMPLES</span></span>

### <span data-ttu-id="2b945-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2b945-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="2b945-111">Elenca tutti i mapping di classificazione dello spazio di archiviazione corrispondenti alla classificazione di archiviazione specificata.</span><span class="sxs-lookup"><span data-stu-id="2b945-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="2b945-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b945-112">PARAMETERS</span></span>

### <span data-ttu-id="2b945-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b945-113">-DefaultProfile</span></span>
<span data-ttu-id="2b945-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b945-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2b945-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b945-115">-Name</span></span>
<span data-ttu-id="2b945-116">Specifica il nome del mapping di classificazione dello spazio di archiviazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="2b945-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="2b945-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="2b945-117">-StorageClassification</span></span>
<span data-ttu-id="2b945-118">Specifica un oggetto di classificazione dello spazio di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="2b945-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="2b945-119">Il cmdlet ottiene i mapping di classificazione di archiviazione ASR corrispondenti alla classificazione di archiviazione specificata</span><span class="sxs-lookup"><span data-stu-id="2b945-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="2b945-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b945-120">CommonParameters</span></span>
<span data-ttu-id="2b945-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b945-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b945-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b945-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b945-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b945-123">INPUTS</span></span>

### <span data-ttu-id="2b945-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2b945-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="2b945-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b945-125">OUTPUTS</span></span>

### <span data-ttu-id="2b945-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2b945-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="2b945-127">Note</span><span class="sxs-lookup"><span data-stu-id="2b945-127">NOTES</span></span>

## <span data-ttu-id="2b945-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b945-128">RELATED LINKS</span></span>

[<span data-ttu-id="2b945-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2b945-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="2b945-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2b945-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)