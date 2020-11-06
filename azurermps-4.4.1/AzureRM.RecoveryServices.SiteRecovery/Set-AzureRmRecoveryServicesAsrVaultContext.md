---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: f8d55ec80c6120f2159969ae6a58a531bea50b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513056"
---
# <span data-ttu-id="c03f5-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="c03f5-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="c03f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c03f5-102">SYNOPSIS</span></span>
<span data-ttu-id="c03f5-103">Imposta il contesto del Vault di servizi di ripristino da usare per le successive operazioni di ripristino dei siti di Azure nella sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c03f5-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c03f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c03f5-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c03f5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c03f5-105">DESCRIPTION</span></span>
<span data-ttu-id="c03f5-106">Il cmdlet **set-AzureRmRecoveryServicesAsrVaultContext** imposta il contesto di archiviazione del sito di ripristino di Azure per ulteriori operazioni.</span><span class="sxs-lookup"><span data-stu-id="c03f5-106">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="c03f5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c03f5-107">EXAMPLES</span></span>

### <span data-ttu-id="c03f5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c03f5-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="c03f5-109">Imposta il contesto del Vault nell'archivio di servizi di ripristino specificato per le successive operazioni di ripristino di Azure sito nella sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c03f5-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="c03f5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c03f5-110">PARAMETERS</span></span>

### <span data-ttu-id="c03f5-111">-Vault</span><span class="sxs-lookup"><span data-stu-id="c03f5-111">-Vault</span></span>
<span data-ttu-id="c03f5-112">Oggetto Vault di servizi di ripristino che corrisponde all'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c03f5-112">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c03f5-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c03f5-113">-Confirm</span></span>
<span data-ttu-id="c03f5-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c03f5-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c03f5-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c03f5-115">-WhatIf</span></span>
<span data-ttu-id="c03f5-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c03f5-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c03f5-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c03f5-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c03f5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c03f5-118">CommonParameters</span></span>
<span data-ttu-id="c03f5-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c03f5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c03f5-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c03f5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c03f5-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c03f5-121">INPUTS</span></span>

### <span data-ttu-id="c03f5-122">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="c03f5-122">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="c03f5-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c03f5-123">OUTPUTS</span></span>

### <span data-ttu-id="c03f5-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="c03f5-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="c03f5-125">Note</span><span class="sxs-lookup"><span data-stu-id="c03f5-125">NOTES</span></span>

## <span data-ttu-id="c03f5-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c03f5-126">RELATED LINKS</span></span>

