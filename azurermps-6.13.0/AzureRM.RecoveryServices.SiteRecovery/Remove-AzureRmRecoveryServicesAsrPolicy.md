---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: dcc0424cd1d6dbd823793a3dc77e813c6e182176
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687780"
---
# <span data-ttu-id="7a7a6-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7a7a6-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="7a7a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7a6-103">Elimina i criteri di replica ASR specificati dall'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7a7a6-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a7a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a7a6-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a7a6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a7a6-105">DESCRIPTION</span></span>
<span data-ttu-id="7a7a6-106">Il cmdlet **Remove-AzureRmRecoveryServicesAsrPolicy** ha eliminato i criteri di replica specificati dall'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7a7a6-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="7a7a6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a7a6-107">EXAMPLES</span></span>

### <span data-ttu-id="7a7a6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7a7a6-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="7a7a6-109">Avvia l'eliminazione dei criteri di replica specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7a7a6-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7a7a6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a7a6-110">PARAMETERS</span></span>

### <span data-ttu-id="7a7a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7a6-111">-DefaultProfile</span></span>
<span data-ttu-id="7a7a6-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a7a6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a7a6-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a7a6-113">-InputObject</span></span>
<span data-ttu-id="7a7a6-114">Oggetto di input per il cmdlet: l'oggetto Criteri di replica ASR che corrisponde ai criteri di replica da eliminare.</span><span class="sxs-lookup"><span data-stu-id="7a7a6-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a7a6-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7a7a6-115">-Confirm</span></span>
<span data-ttu-id="7a7a6-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a7a6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a7a6-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a7a6-117">-WhatIf</span></span>
<span data-ttu-id="7a7a6-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a7a6-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a7a6-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a7a6-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a7a6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7a6-120">CommonParameters</span></span>
<span data-ttu-id="7a7a6-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a7a6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7a6-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a7a6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7a6-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a7a6-123">INPUTS</span></span>

### <span data-ttu-id="7a7a6-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="7a7a6-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="7a7a6-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a7a6-125">OUTPUTS</span></span>

### <span data-ttu-id="7a7a6-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="7a7a6-126">System.Object</span></span>

## <span data-ttu-id="7a7a6-127">Note</span><span class="sxs-lookup"><span data-stu-id="7a7a6-127">NOTES</span></span>

## <span data-ttu-id="7a7a6-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a7a6-128">RELATED LINKS</span></span>

[<span data-ttu-id="7a7a6-129">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7a7a6-129">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="7a7a6-130">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7a7a6-130">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
