---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: a0de6cc5594b019275cb14785cbae3b969d44301
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686144"
---
# <span data-ttu-id="35d9a-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="35d9a-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="35d9a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="35d9a-103">Rimuove un mapping del contenitore di protezione del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="35d9a-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35d9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35d9a-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35d9a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="35d9a-106">Il cmdlet **Remove-AzureRmSiteRecoveryProtectionContainerMapping** rimuove un mapping del contenitore di protezione del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="35d9a-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="35d9a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35d9a-107">EXAMPLES</span></span>

## <span data-ttu-id="35d9a-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35d9a-108">PARAMETERS</span></span>

### <span data-ttu-id="35d9a-109">-Force</span><span class="sxs-lookup"><span data-stu-id="35d9a-109">-Force</span></span>
<span data-ttu-id="35d9a-110">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="35d9a-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="35d9a-111">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="35d9a-111">-ProtectionContainerMapping</span></span>
<span data-ttu-id="35d9a-112">Specifica l'oggetto mapping contenitore di protezione di Azure site.</span><span class="sxs-lookup"><span data-stu-id="35d9a-112">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35d9a-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="35d9a-113">-Confirm</span></span>
<span data-ttu-id="35d9a-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35d9a-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d9a-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35d9a-115">-WhatIf</span></span>
<span data-ttu-id="35d9a-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35d9a-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="35d9a-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35d9a-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d9a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d9a-118">-DefaultProfile</span></span>
<span data-ttu-id="35d9a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35d9a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35d9a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d9a-120">CommonParameters</span></span>
<span data-ttu-id="35d9a-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35d9a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d9a-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35d9a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d9a-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35d9a-123">INPUTS</span></span>

### <span data-ttu-id="35d9a-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="35d9a-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="35d9a-125">Il parametro ' ProtectionContainerMapping ' accetta il valore di tipo ' ASRProtectionContainerMapping ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="35d9a-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="35d9a-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35d9a-126">OUTPUTS</span></span>

### <span data-ttu-id="35d9a-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="35d9a-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="35d9a-128">Note</span><span class="sxs-lookup"><span data-stu-id="35d9a-128">NOTES</span></span>

## <span data-ttu-id="35d9a-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35d9a-129">RELATED LINKS</span></span>

[<span data-ttu-id="35d9a-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="35d9a-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="35d9a-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="35d9a-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
