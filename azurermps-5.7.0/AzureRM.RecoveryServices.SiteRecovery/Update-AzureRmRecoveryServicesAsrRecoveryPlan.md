---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 0cabaee1c1d9dfc8a627160ac01adaca81fe65c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519387"
---
# <span data-ttu-id="39288-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39288-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="39288-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39288-102">SYNOPSIS</span></span>
<span data-ttu-id="39288-103">Aggiorna il contenuto di un piano di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="39288-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39288-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39288-104">SYNTAX</span></span>

### <span data-ttu-id="39288-105">ByRPObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39288-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39288-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="39288-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39288-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39288-107">DESCRIPTION</span></span>
<span data-ttu-id="39288-108">Il cmdlet **Update-AzureRmRecoveryServicesAsrRecoveryPlan** aggiorna il contenuto di un piano di ripristino usando il contenuto dell'oggetto piano di ripristino ASR specificato o del file JSON di definizione del piano di ripristino ASR.</span><span class="sxs-lookup"><span data-stu-id="39288-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="39288-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39288-109">EXAMPLES</span></span>

### <span data-ttu-id="39288-110">Esempio 1: aggiornare un piano di ripristino</span><span class="sxs-lookup"><span data-stu-id="39288-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="39288-111">Avviare l'operazione di aggiornamento di un piano di ripristino usando il contenuto dell'oggetto piano di ripristino ASR specificato e restituire il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="39288-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="39288-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39288-112">PARAMETERS</span></span>

### <span data-ttu-id="39288-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="39288-113">-Confirm</span></span>
<span data-ttu-id="39288-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39288-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39288-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39288-115">-DefaultProfile</span></span>
<span data-ttu-id="39288-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39288-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39288-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39288-117">-InputObject</span></span>
<span data-ttu-id="39288-118">Oggetto di input per il cmdlet: specifica un oggetto piano di ripristino ASR, il cui contenuto viene usato per aggiornare il piano di ripristino a cui fa riferimento l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="39288-118">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39288-119">-Path</span><span class="sxs-lookup"><span data-stu-id="39288-119">-Path</span></span>
<span data-ttu-id="39288-120">Specifica il percorso del file JSON per la definizione del piano di ripristino usato per aggiornare il piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="39288-120">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39288-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39288-121">-WhatIf</span></span>
<span data-ttu-id="39288-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39288-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39288-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39288-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39288-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39288-124">CommonParameters</span></span>
<span data-ttu-id="39288-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39288-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39288-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39288-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39288-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39288-127">INPUTS</span></span>

### <span data-ttu-id="39288-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39288-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="39288-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39288-129">OUTPUTS</span></span>

### <span data-ttu-id="39288-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="39288-130">System.Object</span></span>

## <span data-ttu-id="39288-131">Note</span><span class="sxs-lookup"><span data-stu-id="39288-131">NOTES</span></span>

## <span data-ttu-id="39288-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39288-132">RELATED LINKS</span></span>

[<span data-ttu-id="39288-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39288-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="39288-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39288-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="39288-135">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39288-135">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)
