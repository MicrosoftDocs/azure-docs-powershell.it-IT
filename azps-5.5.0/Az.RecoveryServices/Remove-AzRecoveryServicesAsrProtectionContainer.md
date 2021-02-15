---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183894"
---
# <span data-ttu-id="d3e5b-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d3e5b-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="d3e5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3e5b-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e5b-103">Elimina il contenitore di protezione specificato dal suo tessuto.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="d3e5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3e5b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3e5b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d3e5b-105">DESCRIPTION</span></span>
<span data-ttu-id="d3e5b-106">Il Remove-AzRecoveryServicesAsrProtectionContainer cmdlet elimina il contenitore di Azure Site Recovery Protection specificato.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="d3e5b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3e5b-107">EXAMPLES</span></span>

### <span data-ttu-id="d3e5b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3e5b-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="d3e5b-109">Avvia l'eliminazione del contenitore di protezione specificato e restituisce il processo ASR usato per tenere traccia dell'operazione di rimozione.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="d3e5b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3e5b-110">PARAMETERS</span></span>

### <span data-ttu-id="d3e5b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e5b-111">-DefaultProfile</span></span>
<span data-ttu-id="d3e5b-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3e5b-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3e5b-113">-InputObject</span></span>
<span data-ttu-id="d3e5b-114">Specifica il contenitore di protezione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="d3e5b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3e5b-115">-Confirm</span></span>
<span data-ttu-id="d3e5b-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3e5b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3e5b-117">-WhatIf</span></span>
<span data-ttu-id="d3e5b-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3e5b-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3e5b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e5b-120">CommonParameters</span></span>
<span data-ttu-id="d3e5b-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e5b-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d3e5b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e5b-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="d3e5b-123">INPUTS</span></span>

### <span data-ttu-id="d3e5b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d3e5b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d3e5b-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3e5b-125">OUTPUTS</span></span>

### <span data-ttu-id="d3e5b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d3e5b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d3e5b-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="d3e5b-127">NOTES</span></span>

## <span data-ttu-id="d3e5b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3e5b-128">RELATED LINKS</span></span>
