---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193661"
---
# <span data-ttu-id="38792-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="38792-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="38792-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38792-102">SYNOPSIS</span></span>
<span data-ttu-id="38792-103">Imposta il contesto del Vault di servizi di ripristino da usare per le successive operazioni di ripristino dei siti di Azure nella sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38792-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="38792-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38792-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38792-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38792-105">DESCRIPTION</span></span>
<span data-ttu-id="38792-106">Il cmdlet **set-AzRecoveryServicesAsrVaultContext** imposta il contesto di archiviazione del sito di ripristino di Azure per ulteriori operazioni.</span><span class="sxs-lookup"><span data-stu-id="38792-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="38792-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38792-107">EXAMPLES</span></span>

### <span data-ttu-id="38792-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38792-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="38792-109">Imposta il contesto del Vault nell'archivio di servizi di ripristino specificato per le successive operazioni di ripristino di Azure sito nella sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38792-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="38792-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38792-110">PARAMETERS</span></span>

### <span data-ttu-id="38792-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38792-111">-DefaultProfile</span></span>
<span data-ttu-id="38792-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38792-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38792-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="38792-113">-Vault</span></span>
<span data-ttu-id="38792-114">Oggetto Vault di servizi di ripristino che corrisponde all'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="38792-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="38792-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38792-115">-Confirm</span></span>
<span data-ttu-id="38792-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38792-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38792-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38792-117">-WhatIf</span></span>
<span data-ttu-id="38792-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38792-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38792-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38792-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38792-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38792-120">CommonParameters</span></span>
<span data-ttu-id="38792-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38792-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38792-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38792-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38792-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38792-123">INPUTS</span></span>

### <span data-ttu-id="38792-124">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="38792-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="38792-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38792-125">OUTPUTS</span></span>

### <span data-ttu-id="38792-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="38792-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="38792-127">Note</span><span class="sxs-lookup"><span data-stu-id="38792-127">NOTES</span></span>

## <span data-ttu-id="38792-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38792-128">RELATED LINKS</span></span>