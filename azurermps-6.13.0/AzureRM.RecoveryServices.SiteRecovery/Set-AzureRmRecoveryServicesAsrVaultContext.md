---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 3d0761ff05a0cdcd775a234b4da0a50d27c2ba08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509172"
---
# <span data-ttu-id="db7ad-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="db7ad-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="db7ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db7ad-102">SYNOPSIS</span></span>
<span data-ttu-id="db7ad-103">Imposta il contesto del Vault di servizi di ripristino da usare per le successive operazioni di ripristino dei siti di Azure nella sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="db7ad-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db7ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db7ad-104">SYNTAX</span></span>

### <span data-ttu-id="db7ad-105">AzureRecoveryServicesVault (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db7ad-105">AzureRecoveryServicesVault (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db7ad-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="db7ad-106">ByResourceId</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db7ad-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db7ad-107">DESCRIPTION</span></span>
<span data-ttu-id="db7ad-108">Il cmdlet **set-AzureRmRecoveryServicesAsrVaultContext** imposta il contesto di archiviazione del sito di ripristino di Azure per ulteriori operazioni.</span><span class="sxs-lookup"><span data-stu-id="db7ad-108">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="db7ad-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db7ad-109">EXAMPLES</span></span>

### <span data-ttu-id="db7ad-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db7ad-110">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="db7ad-111">Imposta il contesto del Vault nell'archivio di servizi di ripristino specificato per le successive operazioni di ripristino di Azure sito nella sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="db7ad-111">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="db7ad-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db7ad-112">PARAMETERS</span></span>

### <span data-ttu-id="db7ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db7ad-113">-DefaultProfile</span></span>
<span data-ttu-id="db7ad-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db7ad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db7ad-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db7ad-115">-ResourceId</span></span>
<span data-ttu-id="db7ad-116">Specifica l'ID risorsa di recoveryservices Vault da impostare come contesto del Vault.</span><span class="sxs-lookup"><span data-stu-id="db7ad-116">Specifies the recoveryservices vault resource id to be set as Vault context.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db7ad-117">-Vault</span><span class="sxs-lookup"><span data-stu-id="db7ad-117">-Vault</span></span>
<span data-ttu-id="db7ad-118">Oggetto Vault di servizi di ripristino che corrisponde all'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="db7ad-118">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db7ad-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db7ad-119">-Confirm</span></span>
<span data-ttu-id="db7ad-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db7ad-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db7ad-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db7ad-121">-WhatIf</span></span>
<span data-ttu-id="db7ad-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db7ad-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db7ad-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db7ad-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db7ad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db7ad-124">CommonParameters</span></span>
<span data-ttu-id="db7ad-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db7ad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db7ad-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db7ad-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db7ad-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db7ad-127">INPUTS</span></span>

### <span data-ttu-id="db7ad-128">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="db7ad-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="db7ad-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db7ad-129">OUTPUTS</span></span>

### <span data-ttu-id="db7ad-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="db7ad-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="db7ad-131">Note</span><span class="sxs-lookup"><span data-stu-id="db7ad-131">NOTES</span></span>

## <span data-ttu-id="db7ad-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db7ad-132">RELATED LINKS</span></span>
