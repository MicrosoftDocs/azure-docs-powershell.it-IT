---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191303"
---
# <span data-ttu-id="a9d21-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="a9d21-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="a9d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9d21-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d21-103">Imposta il contesto della vault dei servizi di ripristino da usare per le successive operazioni di Ripristino siti di Azure nella sessione di PowerShell corrente.</span><span class="sxs-lookup"><span data-stu-id="a9d21-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="a9d21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9d21-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9d21-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a9d21-105">DESCRIPTION</span></span>
<span data-ttu-id="a9d21-106">Il cmdlet **Set-AzRecoveryServicesAsrVaultContext** imposta il contesto del vault di Ripristino siti di Azure per altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="a9d21-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="a9d21-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9d21-107">EXAMPLES</span></span>

### <span data-ttu-id="a9d21-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a9d21-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="a9d21-109">Imposta il contesto del vault sul vault dei servizi di ripristino specificato per le successive operazioni di Ripristino siti di Azure nella sessione di PowerShell corrente.</span><span class="sxs-lookup"><span data-stu-id="a9d21-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="a9d21-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9d21-110">PARAMETERS</span></span>

### <span data-ttu-id="a9d21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d21-111">-DefaultProfile</span></span>
<span data-ttu-id="a9d21-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9d21-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9d21-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="a9d21-113">-Vault</span></span>
<span data-ttu-id="a9d21-114">Oggetto vault dei servizi di ripristino corrispondente al vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a9d21-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="a9d21-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9d21-115">-Confirm</span></span>
<span data-ttu-id="a9d21-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9d21-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9d21-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9d21-117">-WhatIf</span></span>
<span data-ttu-id="a9d21-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9d21-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9d21-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9d21-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9d21-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d21-120">CommonParameters</span></span>
<span data-ttu-id="a9d21-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9d21-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d21-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a9d21-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d21-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="a9d21-123">INPUTS</span></span>

### <span data-ttu-id="a9d21-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="a9d21-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a9d21-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9d21-125">OUTPUTS</span></span>

### <span data-ttu-id="a9d21-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="a9d21-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="a9d21-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="a9d21-127">NOTES</span></span>

## <span data-ttu-id="a9d21-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9d21-128">RELATED LINKS</span></span>
