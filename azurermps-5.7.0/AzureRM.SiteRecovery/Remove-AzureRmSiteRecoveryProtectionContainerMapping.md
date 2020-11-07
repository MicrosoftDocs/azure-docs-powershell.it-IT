---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 27c90687b212c0ed41dcb080df1be5686a876725
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687424"
---
# <span data-ttu-id="db1db-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="db1db-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="db1db-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db1db-102">SYNOPSIS</span></span>
<span data-ttu-id="db1db-103">Rimuove un mapping del contenitore di protezione del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="db1db-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db1db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db1db-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db1db-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db1db-105">DESCRIPTION</span></span>
<span data-ttu-id="db1db-106">Il cmdlet **Remove-AzureRmSiteRecoveryProtectionContainerMapping** rimuove un mapping del contenitore di protezione del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="db1db-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="db1db-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db1db-107">EXAMPLES</span></span>

## <span data-ttu-id="db1db-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db1db-108">PARAMETERS</span></span>

### <span data-ttu-id="db1db-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db1db-109">-DefaultProfile</span></span>
<span data-ttu-id="db1db-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db1db-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db1db-111">-Force</span><span class="sxs-lookup"><span data-stu-id="db1db-111">-Force</span></span>
<span data-ttu-id="db1db-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="db1db-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db1db-113">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="db1db-113">-ProtectionContainerMapping</span></span>
<span data-ttu-id="db1db-114">Specifica l'oggetto mapping contenitore di protezione di Azure site.</span><span class="sxs-lookup"><span data-stu-id="db1db-114">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db1db-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db1db-115">-Confirm</span></span>
<span data-ttu-id="db1db-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db1db-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db1db-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db1db-117">-WhatIf</span></span>
<span data-ttu-id="db1db-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db1db-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="db1db-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db1db-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db1db-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db1db-120">CommonParameters</span></span>
<span data-ttu-id="db1db-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db1db-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db1db-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db1db-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db1db-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db1db-123">INPUTS</span></span>

### <span data-ttu-id="db1db-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="db1db-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="db1db-125">Il parametro ' ProtectionContainerMapping ' accetta il valore di tipo ' ASRProtectionContainerMapping ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="db1db-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="db1db-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db1db-126">OUTPUTS</span></span>

### <span data-ttu-id="db1db-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="db1db-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="db1db-128">Note</span><span class="sxs-lookup"><span data-stu-id="db1db-128">NOTES</span></span>

## <span data-ttu-id="db1db-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db1db-129">RELATED LINKS</span></span>

[<span data-ttu-id="db1db-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="db1db-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="db1db-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="db1db-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
