---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: ad4fe186a07adb2b9f90222d3caf8def1ecbefdc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997441"
---
# <span data-ttu-id="220d7-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="220d7-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="220d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="220d7-102">SYNOPSIS</span></span>
<span data-ttu-id="220d7-103">Imposta il contesto della vault dei servizi di ripristino da usare per le successive operazioni di Ripristino siti di Azure nella sessione di PowerShell corrente.</span><span class="sxs-lookup"><span data-stu-id="220d7-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="220d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="220d7-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="220d7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="220d7-105">DESCRIPTION</span></span>
<span data-ttu-id="220d7-106">Il cmdlet **Set-AzRecoveryServicesAsrVaultContext** imposta il contesto del vault di Ripristino siti di Azure per altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="220d7-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="220d7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="220d7-107">EXAMPLES</span></span>

### <span data-ttu-id="220d7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="220d7-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="220d7-109">Imposta il contesto del vault sul vault dei servizi di ripristino specificato per le successive operazioni di Ripristino siti di Azure nella sessione di PowerShell corrente.</span><span class="sxs-lookup"><span data-stu-id="220d7-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="220d7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="220d7-110">PARAMETERS</span></span>

### <span data-ttu-id="220d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="220d7-111">-DefaultProfile</span></span>
<span data-ttu-id="220d7-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="220d7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="220d7-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="220d7-113">-Vault</span></span>
<span data-ttu-id="220d7-114">Oggetto vault dei servizi di ripristino corrispondente al vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="220d7-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="220d7-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="220d7-115">-Confirm</span></span>
<span data-ttu-id="220d7-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="220d7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="220d7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="220d7-117">-WhatIf</span></span>
<span data-ttu-id="220d7-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="220d7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="220d7-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="220d7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="220d7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="220d7-120">CommonParameters</span></span>
<span data-ttu-id="220d7-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="220d7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="220d7-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="220d7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="220d7-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="220d7-123">INPUTS</span></span>

### <span data-ttu-id="220d7-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="220d7-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="220d7-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="220d7-125">OUTPUTS</span></span>

### <span data-ttu-id="220d7-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="220d7-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="220d7-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="220d7-127">NOTES</span></span>

## <span data-ttu-id="220d7-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="220d7-128">RELATED LINKS</span></span>
