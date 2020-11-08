---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 091f8892238d88554d0e0c3502ffbeb8e8d4c154
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192223"
---
# <span data-ttu-id="f172e-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f172e-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="f172e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f172e-102">SYNOPSIS</span></span>
<span data-ttu-id="f172e-103">Crea un mapping di classificazione di archiviazione ASR nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="f172e-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="f172e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f172e-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f172e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f172e-105">DESCRIPTION</span></span>
<span data-ttu-id="f172e-106">Il cmdlet **New-AzRecoveryServicesAsrStorageClassificationMapping** crea una classificazione di archiviazione che mappa il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="f172e-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="f172e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f172e-107">EXAMPLES</span></span>

### <span data-ttu-id="f172e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f172e-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="f172e-109">Avvia l'operazione di creazione del mapping della classificazione di archiviazione con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f172e-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f172e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f172e-110">PARAMETERS</span></span>

### <span data-ttu-id="f172e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f172e-111">-DefaultProfile</span></span>
<span data-ttu-id="f172e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f172e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f172e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f172e-113">-Name</span></span>
<span data-ttu-id="f172e-114">Specifica un nome per il mapping della classificazione di archiviazione ASR.</span><span class="sxs-lookup"><span data-stu-id="f172e-114">Specifies a name for the ASR storage classification mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f172e-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="f172e-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="f172e-116">Specifica l'oggetto di classificazione dello spazio di archiviazione ASR principale per il mapping.</span><span class="sxs-lookup"><span data-stu-id="f172e-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="f172e-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="f172e-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="f172e-118">Specifica l'oggetto di classificazione dello spazio di ripristino ASR per il mapping.</span><span class="sxs-lookup"><span data-stu-id="f172e-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f172e-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f172e-119">-Confirm</span></span>
<span data-ttu-id="f172e-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f172e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f172e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f172e-121">-WhatIf</span></span>
<span data-ttu-id="f172e-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f172e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f172e-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f172e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f172e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f172e-124">CommonParameters</span></span>
<span data-ttu-id="f172e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f172e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f172e-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f172e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f172e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f172e-127">INPUTS</span></span>

### <span data-ttu-id="f172e-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="f172e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="f172e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f172e-129">OUTPUTS</span></span>

### <span data-ttu-id="f172e-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f172e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f172e-131">Note</span><span class="sxs-lookup"><span data-stu-id="f172e-131">NOTES</span></span>

## <span data-ttu-id="f172e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f172e-132">RELATED LINKS</span></span>

[<span data-ttu-id="f172e-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f172e-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="f172e-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f172e-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)