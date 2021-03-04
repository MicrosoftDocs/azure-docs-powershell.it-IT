---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: f7d71d0e69f83633d02832bd3f54554be1fa0ba0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953246"
---
# <span data-ttu-id="5f1f8-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5f1f8-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="5f1f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f1f8-102">SYNOPSIS</span></span>
<span data-ttu-id="5f1f8-103">Elimina il mapping del contenitore di Azure Site Protection specificato.</span><span class="sxs-lookup"><span data-stu-id="5f1f8-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="5f1f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f1f8-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f1f8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5f1f8-105">DESCRIPTION</span></span>
<span data-ttu-id="5f1f8-106">Il cmdlet **Remove-AzRecoveryServicesAsrProtectionContainerMapping** elimina il mapping del contenitore di protezione di Azure Site Recovery specificato.</span><span class="sxs-lookup"><span data-stu-id="5f1f8-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="5f1f8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f1f8-107">EXAMPLES</span></span>

### <span data-ttu-id="5f1f8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5f1f8-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="5f1f8-109">Avvia l'eliminazione del mapping del contenitore di protezione specificato e restituisce il processo a matrice usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5f1f8-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5f1f8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f1f8-110">PARAMETERS</span></span>

### <span data-ttu-id="5f1f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f1f8-111">-DefaultProfile</span></span>
<span data-ttu-id="5f1f8-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f1f8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5f1f8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5f1f8-113">-Force</span></span>
<span data-ttu-id="5f1f8-114">Forzare l'esecuzione del comando senza visualizzare altri avvisi.</span><span class="sxs-lookup"><span data-stu-id="5f1f8-114">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f1f8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f1f8-115">-InputObject</span></span>
<span data-ttu-id="5f1f8-116">Oggetto di input per il cmdlet: oggetto di mapping del contenitore di protezione ASR corrispondente al contenitore di protezione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="5f1f8-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f1f8-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f1f8-117">-Confirm</span></span>
<span data-ttu-id="5f1f8-118">Specificare se è necessaria una conferma.</span><span class="sxs-lookup"><span data-stu-id="5f1f8-118">Specify if confirmation is required.</span></span> <span data-ttu-id="5f1f8-119">Impostare il valore del parametro confirm su $false per ignorare la conferma</span><span class="sxs-lookup"><span data-stu-id="5f1f8-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="5f1f8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f1f8-120">-WhatIf</span></span>
<span data-ttu-id="5f1f8-121">Mostra cosa accadrebbe se il cmdlet viene eseguito senza effettivamente eseguirlo.</span><span class="sxs-lookup"><span data-stu-id="5f1f8-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="5f1f8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f1f8-122">CommonParameters</span></span>
<span data-ttu-id="5f1f8-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f1f8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f1f8-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5f1f8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f1f8-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="5f1f8-125">INPUTS</span></span>

### <span data-ttu-id="5f1f8-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5f1f8-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="5f1f8-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f1f8-127">OUTPUTS</span></span>

### <span data-ttu-id="5f1f8-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="5f1f8-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5f1f8-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="5f1f8-129">NOTES</span></span>

## <span data-ttu-id="5f1f8-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f1f8-130">RELATED LINKS</span></span>

[<span data-ttu-id="5f1f8-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5f1f8-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="5f1f8-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5f1f8-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
