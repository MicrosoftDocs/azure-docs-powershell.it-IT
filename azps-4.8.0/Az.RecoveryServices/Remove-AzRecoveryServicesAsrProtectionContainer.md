---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190674"
---
# <span data-ttu-id="ea8d1-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ea8d1-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="ea8d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea8d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8d1-103">Elimina il contenitore di protezione specificato dal relativo tessuto.</span><span class="sxs-lookup"><span data-stu-id="ea8d1-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="ea8d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea8d1-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea8d1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea8d1-105">DESCRIPTION</span></span>
<span data-ttu-id="ea8d1-106">Il cmdlet Remove-AzRecoveryServicesAsrProtectionContainer Elimina il contenitore di protezione del ripristino di Azure site specificato.</span><span class="sxs-lookup"><span data-stu-id="ea8d1-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="ea8d1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea8d1-107">EXAMPLES</span></span>

### <span data-ttu-id="ea8d1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea8d1-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="ea8d1-109">Avvia l'eliminazione del contenitore di protezione specificato e restituisce il processo ASR usato per tenere traccia dell'operazione di rimozione.</span><span class="sxs-lookup"><span data-stu-id="ea8d1-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="ea8d1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea8d1-110">PARAMETERS</span></span>

### <span data-ttu-id="ea8d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea8d1-111">-DefaultProfile</span></span>
<span data-ttu-id="ea8d1-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea8d1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea8d1-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea8d1-113">-InputObject</span></span>
<span data-ttu-id="ea8d1-114">Specifica il contenitore di protezione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ea8d1-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8d1-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ea8d1-115">-Confirm</span></span>
<span data-ttu-id="ea8d1-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea8d1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea8d1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea8d1-117">-WhatIf</span></span>
<span data-ttu-id="ea8d1-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea8d1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea8d1-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea8d1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea8d1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8d1-120">CommonParameters</span></span>
<span data-ttu-id="ea8d1-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea8d1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8d1-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea8d1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8d1-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea8d1-123">INPUTS</span></span>

### <span data-ttu-id="ea8d1-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ea8d1-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="ea8d1-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea8d1-125">OUTPUTS</span></span>

### <span data-ttu-id="ea8d1-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ea8d1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ea8d1-127">Note</span><span class="sxs-lookup"><span data-stu-id="ea8d1-127">NOTES</span></span>

## <span data-ttu-id="ea8d1-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea8d1-128">RELATED LINKS</span></span>